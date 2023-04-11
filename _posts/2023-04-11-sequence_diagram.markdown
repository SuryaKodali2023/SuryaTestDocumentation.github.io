```mermaid
sequenceDiagram
    participant User
    participant System
    User->>System: Send request
    System->>Database: Retrieve data
    Database-->>System: Send data
    System->>User: Send response
```%
