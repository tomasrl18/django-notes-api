# Nota Flow API

## Description
Nota Flow is an application for managing notes. This API allows users to create, read, update, and delete notes.

## Endpoints

### Get all notes
```
GET /api/notes
```
**Response:**
```json
[
    {
        "id": 1,
        "title": "Note 1",
        "content": "Content of note 1",
        "created_at": "2023-10-01T12:00:00Z"
    },
    {
        "id": 2,
        "title": "Note 2",
        "content": "Content of note 2",
        "created_at": "2023-10-02T12:00:00Z"
    }
]
```

### Get a note by ID (TODO)
```
GET /api/notes/{id}
```
**Response:**
```json
{
    "id": 1,
    "title": "Note 1",
    "content": "Content of note 1",
    "created_at": "2023-10-01T12:00:00Z"
}
```

### Create a new note (TODO)
```
POST /api/notes
```
**Request body:**
```json
{
    "title": "New note",
    "content": "Content of the new note"
}
```
**Response:**
```json
{
    "id": 3,
    "title": "New Note",
    "content": "Content of the new note",
    "created_at": "2023-10-03T12:00:00Z"
}
```

### Update an existing note (TODO)
```
PUT /api/notes/{id}
```
**Request body:**
```json
{
    "title": "Updated Note",
    "content": "Updated content of the note"
}
```
**Response:**
```json
{
    "id": 1,
    "title": "Updated Note",
    "content": "Updated content of the note",
    "created_at": "2023-10-01T12:00:00Z"
}
```

### Delete a note (TODO)
```
DELETE /api/notes/{id}
```
**Response:**
```json
{
    "message": "Note successfully deleted"
}
```

## Autenticación (TODO)
The API uses token-based authentication. Include the token in the authorization header of each request:
```
Authorization: Bearer {token}
```

## Errors (TODO)
The API returns the following error codes:
- `400 Bad Request`: Malformed request.
- `401 Unauthorized`: Missing authentication or invalid token.
- `404 Not Found`: Note not found.
- `500 Internal Server Error`: Server error.