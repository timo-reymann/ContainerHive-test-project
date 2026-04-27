# Base Deployment Image

Minimal base image optimized for production deployments with a focus on security and small footprint.

## Features

- Minimal runtime dependencies
- Optimized for production
- Security-focused

## Usage

```dockerfile
FROM __hive__/base-deployment:v1

# Copy your application
COPY app /app
CMD ["/app"]
```
