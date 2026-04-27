# Go CI Image

This image provides a ready-to-use Go build environment with common CI/CD tools.

## Included Tools

- Go compiler (version specified in tags)
- Zig build tool
- Git for version control

## Usage

```dockerfile
FROM __hive__/go-ci:1.26.0

# Your build steps here
RUN go build -o myapp .
```

## Versions

Available versions are defined in `image.yml` and support semantic versioning aliases.