# pz-UML

## Система: Онлайн-магазин

---

## Use Case

```mermaid
graph TD
    User -->|Купити товар| System
    Admin -->|Керувати товарами| System
```

---

## Sequence

```mermaid
sequenceDiagram
    User->>System: Обрати товар
    System-->>User: Показати товар
    User->>System: Купити
```

---

## Activity

```mermaid
flowchart TD
    A[Початок] --> B[Вибір товару]
    B --> C[Покупка]
    C --> D[Кінець]
```
