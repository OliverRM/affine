Index container has to be started manually

# Search

```bash
cd .devcontainer/ && docker compose up -d manticoresearch
```

# devcontainer.json

```json
    "ghcr.io/devcontainers/features/rust:1": {
      "version": "1.64.0"
    },
    "ghcr.io/devcontainers/features/docker-in-docker:2": {}
```

# Admin Portal

```bash
cp -r packages/frontend/admin/dist/ packages/backend/server/static/admin
rm packages/backend/server/static/admin/index.html
mv packages/backend/server/static/admin/selfhost.html packages/backend/server/static/admin/index.html
```
