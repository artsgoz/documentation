---
title: Development
layout: default
nav_order: 5
---

# Development

Keep business behavior in feature services, SQL and GORM operations in repositories, and HTTP translation in handlers. Register routes in the feature's `routes.go` and wire dependencies in `cmd/api`.

## Checks

Run these commands from `artsgoz-backend`:

```sh
go test ./...
go vet ./...
bash scripts/check-deps.sh
```

Service tests use small repository stubs, which keeps validation and conflict behavior fast to exercise without a live database. The application uses SQL migrations and does not call GORM `AutoMigrate` at runtime.

## Documentation locally

From this repository:

```sh
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000/documentation/` to browse the generated site.
