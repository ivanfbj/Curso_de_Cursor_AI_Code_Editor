# Platziflix

plataforma online de cursos, cada curso tiene clases, descripciones y no hay mucho más, eso es el inicio.

## stacks

### Frontend

- Typescript
- Css modules
- SASS

### Mobile

- iOS:
  - Swift
  - SwiftUI
- Android:
  - Kotlin
  - Jetpack Compose

### Backend

- Python
- FastAPI
- PostgreSQL

## Contratos

### Entidades

1. Curso
2. Clases
3. Profesor

### Contrato de Curso

```json
{
  "id": 1,
  "name": "Curso de React",
  "description": "Curso de React",
  "thumbnail": "https://via.placeholder.com/150",
  "slug": "curso-de-react",
  "created_at": "2025-07-04",
  "updated_at": "2025-07-04",
  "deleted_at": "2025-07-04",
  "teacher_id": [1, 2, 3]
}
```

### Contrato de Clases

```json
{
  "id": 1,
  "course_id": 1,
  "name": "Clase 1",
  "description": "Clase 1",
  "slug": "clase-1",
  "video_url": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
  "created_at": "2021-01-01",
  "updated_at": "2021-01-01",
  "deleted_at": "2021-01-01"
}
```

### Contrato de Profesor

```json
{
  "id": 1,
  "name": "John Doe",
  "email": "john.doe@example.com",
  "created_at": "2021-01-01",
  "updated_at": "2021-01-01",
  "deleted_at": "2021-01-01"
}
```

### Endpoints

- **GET /courses** → Listar todos los cursos  
  
  _Ejemplo de respuesta:_
  
  ```json
  [
    {
      "id": 1,
      "name": "Curso de React",
      "description": "Curso de React",
      "thumbnail": "https://via.placeholder.com/150",
      "slug": "curso-de-react"
    }
  ]
  ```

- **GET /courses/:slug** → Obtener un curso
  
  _Ejemplo de respuesta:_
  
  ```json
  
  {
    "id": 1,
    "name": "Curso de React",
    "description": "Curso de React",
    "thumbnail": "https://via.placeholder.com/150",
    "slug": "curso-de-react",
    "teacher_id": [1, 2, 3],
    "classes": [
      {
        "id": 1,
        "name": "Clase 1",
        "description": "Clase 1",
        "slug": "clase-1"
      }
    ]
  }
  
  ```

- **GET /courses/:slug/classes/:id** → Obtener una clase

  _Ejemplo de respuesta:_

  ```json
  {
    "id": 1,
    "name": "Clase 1",
    "description": "Clase 1",
    "slug": "clase-1",
    "video_url": "https://www.yotube.com/watch?fasdte87g",
    "created_at": "2021-01-01",
    "updated_at": "2021-01-01",
    "deleted_at": "2021-01-01"
  }
  ```
