# Диаграммы
## Диаграмма последовательности
```mermaid
sequenceDiagram
    actor User as Посетитель
    participant System as Система
    participant Model as ML-модель

    User->>System: Отправить обращение
    System->>Model: Передать текст
    Model-->>System: Вернуть ответ
    System-->>User: Показать ответ
```
## Диаграмма классов
```mermaid
classDiagram

    class User {
        +int id
        +string name
    }

    class TextRequest {
        +int id
        +string text
    }

    class TextResponse {
        +string from
        +float confidence
    }

    User "1" --> "*" TextRequest
    TextRequest "1" --> "1" TextResponse
```
