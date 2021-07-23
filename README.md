# Chunk upload

This test task is about implementing a feature of chunk uploading with file validation.

The main purpose is to see your code structure, code quality, and approach in general.

## Getting Started

### Requirements

- Make it possible to upload several chunks simultaneously 
- Implement possibility to validate uploaded file (not a chunk) by Laravel validation rules
- Implement `ChunkUploaded` and `FileUploaded` events
- Implement listener to move uploaded file to cloud storage 
- No unnecessary things in the final code like commented code, debug logs, etc
- Follow best practices as much as possible and focus on quality

We expect you to use the Laravel Facade and Builder pattern for uploader implementation.

### API

Only 1 endpoint is required: <b>POST /v1/upload</b>

#### Request
```json
{
    "chunk": "required|file",
    "uuid": "required|uuid",
    "index": "required|integer",
    "total": "required|integer"
}
```

- `chunk` - Chunk payload
- `uuid`  - Unique file identifier
- `index` - Current chunk index
- `total` - Total number of chunks

#### Responses:

#### Chunks uploaded:

```json
{
    "status": "success"
}
```

#### All chunks uploaded:

```json
{
    "status": "success",
    "message": "The file has been successfully uploaded"
}
```

#### Validation error:

```json
{
    "status": "error",
    "message": "The file must be an image"
}
```

### Any questions?

If you have any questions or suggestions related to the task, please submit an issue.
