# Chunk upload

This test task is about implementing a feature of chunk uploading with file validation.

The main purpose is to see your code structure, code quality, and approach in general.

## Getting Started
### API

Only 1 endpoint is required:

<b>POST /v1/upload

Request:
```json
{
    "chunk": "required|file", //chunk payload
    "uuid": "required|uuid", //unique file identifier 
    "index": "required|integer", //current chunk index
    "total": "required|integer" //total number of chunks
}
```
Responses:

Chunks uploaded:
```json
{
    "status": "success"
}
```

All chunks uploaded:
```json
{
    "status": "success",
    "message": "The file has been successfully uploaded"
}
```

Validation error:
```json
{
    "status": "error",
    "message": "The file must be an image"
}
```
### Requirements

- Make it possible to upload several chunks simultaneously 
- Implement possibility to validate uploaded file (not a chunk) by Laravel validation rules
- Implement possibility to process uploaded file, fx.: resize, upload to s3, etc
- No unnecessary things in the final code like commented code, debug logs, etc
- Follow best practices as much as possible and focus on quality

### Any questions?

If you have any questions or suggestions related to the task, please submit an issue.
