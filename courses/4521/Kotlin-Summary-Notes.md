# Kotlin Summary Notes

This summary covers the key Kotlin concepts taught across Lab Sessions 1 to 4, plus an extra section on networking with coroutines and Retrofit.

Brief notes and examples covering language basics, OOP, functional features, generics, Jetpack Compose, and networking.

## 1. Kotlin basics and syntax

Basic language constructs, control flow, and syntax essentials you'll use in nearly every Kotlin program.

### Functions and variables

```kotlin
fun greet(name: String): String {
    return "Hello, $name!"
}

val immutableVal: Int = 10
var mutableVar: Int = 20
```

This defines a simple function `greet` that returns a greeting string, and shows an immutable (`val`) and mutable (`var`) variable declaration.

### Null safety

```kotlin
var nullableInt: Int? = null
nullableInt = 5
```

Shows Kotlin's nullable type (`Int?`) which can hold `null`; assigning a value later is safe when you check for null before using it.

### Control flow

```kotlin
val x = 10
if (x > 5) {
    println("x is greater than 5")
}

for (i in 1..5 step 2) {
    println(i)
}

val result = when (x) {
    1 -> "One"
    10 -> "Ten"
    else -> "Other"
}
println(result)
```

Demonstrates `if` for branching, a `for` loop with a step, and `when` as a powerful multi-branch expression that returns a value.

### String templates

```kotlin
val name = "Alice"
println("Hello, $name!")
println("Sum: ${5 + 3}")
```

Shows string templates: `$name` inserts a variable, and `${...}` evaluates an expression inside the string.

## 2. Object-oriented and structural concepts

Core OOP features and Kotlin-specific structural types that help model data and behavior.

### Classes and constructors

```kotlin
class Person(val name: String) {
    var age: Int = 0

    constructor(name: String, age: Int) : this(name) {
        this.age = age
    }

    fun greet() = "Hi, I'm $name and I'm $age years old."
}
```

Defines a `Person` class with a primary constructor, a secondary constructor, a mutable property `age`, and a member function `greet` that returns a formatted string.

### Specialized classes

```kotlin
data class User(val id: Int, val username: String)

enum class Direction { NORTH, SOUTH, EAST, WEST }

sealed class Result {
    class Success(val data: String) : Result()
    class Error(val error: Exception) : Result()
}

object Singleton {
    fun doSomething() = println("Singleton called")
}
```

`data class` provides boilerplate (equals, toString), `enum` models a fixed set of values, `sealed class` encodes restricted hierarchies for exhaustive `when`, and `object` creates a singleton.

### Infix functions

```kotlin
infix fun Int.add(x: Int) = this + x
val sum = 5 add 10
println(sum) // 15
```

Defines an infix extension function to make `5 add 10` look like a natural language operation; useful for DSL-style APIs.

### Property delegates

```kotlin
val lazyValue: String by lazy {
    println("Computed!")
    "Hello"
}

import kotlin.properties.Delegates
var observedValue: Int by Delegates.observable(0) { prop, old, new ->
    println("$old -> $new")
}
observedValue = 10
```

Shows `by lazy` to compute a value on first access, and `Delegates.observable` to react to property changes with a callback.

## 3. Functional programming and collections

Functional-style utilities, lambdas, and collection helpers for expressive and concise data processing.

### Default arguments

```kotlin
fun greet(name: String = "Guest") {
    println("Hello, $name")
}

greet()
greet(name = "Alice")
```

Demonstrates default parameter values so callers can omit arguments and shows calling with and without named arguments.

### Lambdas and function types

```kotlin
val sum: (Int, Int) -> Int = { a, b -> a + b }
println(sum(3, 4))

val stringRepeat: String.(Int) -> String = { times -> this.repeat(times) }
println("Hi".stringRepeat(3))

val list = listOf(1, 2, 3)
list.forEach { println(it) }

val anonFunc = fun(x: Int): Int {
    if (x == 0) return -1
    return x * 2
}
println(anonFunc(5))
```

Examples of lambda literals, function types, extension function types (`String.(Int)`), collection iteration with `forEach`, and an anonymous function with an explicit `return`.

### Collections helpers

```kotlin
val immutableList = listOf(1, 2, 3)
val mutableList = mutableListOf(4, 5, 6)

val filtered = immutableList.filter { it > 1 }
val mapped = immutableList.map { it * 2 }
val grouped = immutableList.groupBy { it % 2 }
```

Shows immutable vs mutable lists and common collection operations: `filter`, `map`, and `groupBy` for transforming and grouping data.

## 4. Generics

How to write reusable, type-safe code with generic classes, functions, and variance rules.

### Generic classes and functions

```kotlin
class Box<T>(val value: T)

fun <T> singletonList(item: T): List<T> {
    return listOf(item)
}
```

A generic `Box` holds a value of any type `T`, and `singletonList` demonstrates a generic function returning a typed list.

### Type constraints

```kotlin
fun <T : Comparable<T>> sortList(list: List<T>) {
    // sorting logic
}
```

Shows constraining a generic type to `Comparable` so you can order elements inside the function.

### Variance

```kotlin
interface Source<out T> { fun next(): T }
interface Sink<in T> { fun accept(item: T) }
```

`out` marks a type as producer (covariant) and `in` as consumer (contravariant), allowing safe subtyping relationships for generics.

## 5. Kotlin in Android and Jetpack Compose

Examples and patterns for building UI with Compose and managing state, coroutines, and modifiers.

### Composables

```kotlin
@Composable
fun Greeting(name: String) {
    Text(text = "Hello, $name!")
}
```

A simple Compose `@Composable` function that emits a `Text` UI element showing a greeting.

### State management

```kotlin
@Composable
fun DiceRoller() {
    var result by remember { mutableStateOf(1) }

    Button(onClick = { result = (1..6).random() }) {
        Text("Roll: $result")
    }
}
```

Illustrates local UI state in Compose using `remember` and `mutableStateOf`, and updating state on button clicks to recompose the UI.

### Coroutines and Flow (simple examples)

```kotlin
// Coroutine example (use proper scope in production)
GlobalScope.launch {
    delay(1000L)
    println("Coroutine done")
}

// StateFlow example
val stateFlow = MutableStateFlow(0)
stateFlow.collect { value -> println(value) }
```

Shows launching a coroutine (note: prefer structured concurrency over `GlobalScope`) and collecting a `StateFlow` which emits state updates.

### Modifier example

```kotlin
Modifier.padding(16.dp).background(Color.Red)
```

Chained `Modifier` calls add layout and styling information to Compose UI elements; here it adds padding and a red background.

## 6. Network programming with coroutines and Retrofit

Practical networking patterns: using coroutines with Retrofit, JSON parsing, and UI-state handling.

### Why networking is special

- Network requests may block the main thread; use coroutines to keep the UI responsive.

Networking should be done off the main thread (using coroutines) and UI state must reflect loading, success, and error.

### Coroutines basics in ViewModel

```kotlin
viewModelScope.launch {
    // Coroutine code here
}
```

Shows launching a coroutine tied to a ViewModel lifecycle so work is cancelled when the ViewModel is cleared.

### Retrofit setup (basic)

```kotlin
private const val BASE_URL = "https://android-kotlin-fun-mars-server.appspot.com"

private val retrofit = Retrofit.Builder()
    .addConverterFactory(ScalarsConverterFactory.create())
    .baseUrl(BASE_URL)
    .build()

interface MarsApiService {
    @GET("photos")
    suspend fun getPhotos(): String
}

object MarsApi {
    val retrofitService: MarsApiService by lazy {
        retrofit.create(MarsApiService::class.java)
    }
}
```

Builds a `Retrofit` instance and exposes a lazily-initialized service to make network calls defined by `MarsApiService`.

### Internet permission (AndroidManifest)

```xml
<uses-permission android:name="android.permission.INTERNET" />
```

Declares the Android permission required to perform network requests from the app.

### Launching network requests in ViewModel

```kotlin
private fun getMarsPhotos() {
    viewModelScope.launch {
        try {
            val listResult = MarsApi.retrofitService.getPhotos()
            marsUiState = MarsUiState.Success("Success: ${listResult.length} Mars photos retrieved")
        } catch (e: IOException) {
            marsUiState = MarsUiState.Error("Error: ${e.message}")
        }
    }
}
```

Shows making a network call inside a coroutine, handling success by updating UI state and catching IO exceptions to set an error state.

### JSON parsing with kotlinx.serialization

```kotlin
@Serializable
data class MarsPhoto(
    val id: String,
    @SerialName("img_src") val imgSrc: String
)
```

Defines a serializable data class mapping JSON fields to Kotlin properties; `@SerialName` maps `img_src` to `imgSrc`.

### Retrofit with Kotlin serialization

```kotlin
private val retrofit = Retrofit.Builder()
    .addConverterFactory(Json.asConverterFactory("application/json".toMediaType()))
    .baseUrl(BASE_URL)
    .build()

interface MarsApiService {
    @GET("photos")
    suspend fun getPhotos(): List<MarsPhoto>
}
```

Shows configuring Retrofit with a Kotlin serialization converter to parse JSON responses directly into `MarsPhoto` objects.

### UI state handling

```kotlin
sealed interface MarsUiState {
    object Loading : MarsUiState
    data class Success(val photos: List<MarsPhoto>) : MarsUiState
    data class Error(val message: String) : MarsUiState
}

var marsUiState by mutableStateOf<MarsUiState>(MarsUiState.Loading)
```

Encodes UI states as a sealed interface to make the UI react to `Loading`, `Success`, and `Error` cases in a type-safe way.

### Repository and manual DI

```kotlin
class MarsRepository(private val service: MarsApiService) {
    suspend fun getPhotos(): List<MarsPhoto> = service.getPhotos()
}

class MarsViewModel(private val repository: MarsRepository) : ViewModel() {
    // Use repository
}

val repository = MarsRepository(MarsApi.retrofitService)
val viewModel = MarsViewModel(repository)
```

The repository wraps API calls and can be injected into the ViewModel to separate concerns and make testing easier.

### Image loading with Coil in Compose

```kotlin
AsyncImage(
    model = photo.imgSrc,
    contentDescription = "Mars photo",
    modifier = Modifier.size(128.dp),
    contentScale = ContentScale.Crop
)
```

### Displaying images in a grid

```kotlin
LazyVerticalGrid(
    columns = GridCells.Fixed(2),
    modifier = Modifier.padding(4.dp)
) {
    items(photos) { photo ->
        MarsPhotoCard(photo = photo)
    }
}

@Composable
fun MarsPhotoCard(photo: MarsPhoto) {
    Card(modifier = Modifier.padding(8.dp), elevation = 4.dp) {
        AsyncImage(
            model = photo.imgSrc,
            contentDescription = photo.id,
            contentScale = ContentScale.Crop,
            modifier = Modifier
                .height(150.dp)
                .fillMaxWidth()
        )
    }
}
```

### Architecture and best practices

- Separate data layer (repository + service), ViewModel, and UI (Compose).
- Use manual dependency injection for simple projects or Dagger/Hilt for larger apps.
- Use Coil for asynchronous image loading with caching.
- Use LazyVerticalGrid (or LazyColumn) for efficient lists/grids.
- Manage UI state for loading, success, and error cases.
- Consider performance, caching, and code maintainability.
