# Kotlin Summary Notes

This summary covers the key Kotlin concepts taught across Lab Sessions 1 to 4, plus an extra section on networking with coroutines and Retrofit.

Brief notes and examples covering language basics, OOP, functional features, generics, Jetpack Compose, and networking.

## 1. Kotlin basics and syntax

### Functions and variables

```kotlin
fun greet(name: String): String {
    return "Hello, $name!"
}

val immutableVal: Int = 10
var mutableVar: Int = 20
```

### Null safety

```kotlin
var nullableInt: Int? = null
nullableInt = 5
```

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

### String templates

```kotlin
val name = "Alice"
println("Hello, $name!")
println("Sum: ${5 + 3}")
```

## 2. Object-oriented and structural concepts

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

### Infix functions

```kotlin
infix fun Int.add(x: Int) = this + x
val sum = 5 add 10
println(sum) // 15
```

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

## 3. Functional programming and collections

### Default arguments

```kotlin
fun greet(name: String = "Guest") {
    println("Hello, $name")
}

greet()
greet(name = "Alice")
```

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

### Collections helpers

```kotlin
val immutableList = listOf(1, 2, 3)
val mutableList = mutableListOf(4, 5, 6)

val filtered = immutableList.filter { it > 1 }
val mapped = immutableList.map { it * 2 }
val grouped = immutableList.groupBy { it % 2 }
```

## 4. Generics

### Generic classes and functions

```kotlin
class Box<T>(val value: T)

fun <T> singletonList(item: T): List<T> {
    return listOf(item)
}
```

### Type constraints

```kotlin
fun <T : Comparable<T>> sortList(list: List<T>) {
    // sorting logic
}
```

### Variance

```kotlin
interface Source<out T> { fun next(): T }
interface Sink<in T> { fun accept(item: T) }
```

## 5. Kotlin in Android and Jetpack Compose

### Composables

```kotlin
@Composable
fun Greeting(name: String) {
    Text(text = "Hello, $name!")
}
```

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

### Modifier example

```kotlin
Modifier.padding(16.dp).background(Color.Red)
```

## 6. Network programming with coroutines and Retrofit

### Why networking is special

- Network requests may block the main thread; use coroutines to keep the UI responsive.

### Coroutines basics in ViewModel

```kotlin
viewModelScope.launch {
    // Coroutine code here
}
```

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

### Internet permission (AndroidManifest)

```xml
<uses-permission android:name="android.permission.INTERNET" />
```

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

### JSON parsing with kotlinx.serialization

```kotlin
@Serializable
data class MarsPhoto(
    val id: String,
    @SerialName("img_src") val imgSrc: String
)
```

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

### UI state handling

```kotlin
sealed interface MarsUiState {
    object Loading : MarsUiState
    data class Success(val photos: List<MarsPhoto>) : MarsUiState
    data class Error(val message: String) : MarsUiState
}

var marsUiState by mutableStateOf<MarsUiState>(MarsUiState.Loading)
```

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
