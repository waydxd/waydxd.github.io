## Introduction

### 🌟 Purpose

- Helps you **weigh the pros and cons** of architectural decisions when building on AWS.
- Teaches **best practices** for designing and operating **secure, reliable, efficient, cost-effective, and sustainable** workloads.

### 🧭 How It Works

- **Consistent Evaluation**: Measure your architecture against cloud best practices.
- **Constructive Reviews**: It’s a collaborative discussion, not an audit.
- **Foundational Questions**: Guides you in checking if your design aligns with modern cloud qualities.

### 📚 Origins & Expertise

- Draws on **years of AWS Solutions Architects’ experience** across industries.
- Continuously refined as AWS evolves and learns from customer workloads.

### 👥 Who It’s For

- CTOs, architects, developers, and operations teams designing or running cloud workloads.

### 🛠️ Supporting Tools & Resources

- **AWS Well-Architected Tool**: Free service to review and improve workloads.
- **Well-Architected Labs**: Hands-on code and documentation for applying best practices.
- **AWS Partner Program**: Certified partners who can help review and enhance your systems.

## Definition
### 🧱 The Six Pillars of the AWS Well-Architected Framework

| Pillar                           | Focus Area                                                                                                                                                                             |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Operational Excellence**       | Monitoring, incident response, and continuous improvement of operations.                                                                                                               |
| **Security**                     | Protecting data, systems, and assets through risk assessments and controls.                                                                                                            |
| **Reliability**                  | Ensuring workloads can recover from failures and meet customer demands.                                                                                                                |
| **Performance Efficiency**       | Using computing resources efficiently and adapting to changing requirements.                                                                                                           |
| **Cost Optimization**            | Avoiding unnecessary costs and maximizing value from cloud investments.                                                                                                                |
| **Sustainability** (Newly added) | Reducing energy consumption and increasing efficiency across all components of a workload by maximizing the benefits from the provisioned resources and minimizing resources required. |
### 📖 Key Terms
- **Component** – Code, config, and AWS resources that fulfill a requirement; typically an independent technical unit.
- **Workload** – A group of components ==delivering business value==; common unit of discussion for business/tech leaders.
- **Architecture** – How components interact within a workload; often visualized in architecture diagrams.
- **Milestones** – Significant changes in architecture across its lifecycle (design → production).
- **Technology Portfolio** – All workloads an organization needs to operate.
- **Level of Effort** – Categorizes the time/complexity to implement tasks:
    - **High** – Weeks to months; multiple stories/releases.   
    - **Medium** – Days to weeks; multiple releases.    
    - **Low** – Hours to days; multiple tasks.    
### ⚖️ Trade-offs Between Pillars
- Business context drives **engineering priorities**.
- Example trade-offs:
    - Improve sustainability & lower cost **↔** may reduce reliability in non-critical environments.
    - Maximize reliability for mission-critical systems **↔** may increase cost & environmental impact.
    - In e-commerce, performance directly impacts revenue and buying behavior.
- **Security** and **Operational Excellence** are typically _not_ compromised for other pillars.