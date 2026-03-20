# @harpia/common

Core utilities, types, and helpers for the Harpia framework.

This package provides foundational features that powers Harpia applications, abstracting logic and configurations away from your business code to keep your application pristine.

## Included Features

### Utilities (`Utils`)
- `Utils.string`: String manipulations (camelCase, pascalCase, pluralize, singularize).
- `Utils.array`: Array manipulations.
- `Utils.date`: Date formatting and manipulation.
- `Utils.paginate`: Pagination helpers for database queries.

### Helpers
- `AppError`: Standardized error throwing with HTTP status codes.
- `ApiResponse`: Standardized API JSON responses.
- `TestCleaner`: Utility for clearing test databases intuitively.
- `Factory`: Robust database seeding factories integrated with Prisma.
- `HotReloadManager`: Core WebSocket manager for development environment live-reloading.

### Types
- Framework-level types for Observers, Mailer, Test Cleaner, Factory, and Model Keys safely coupled with Prisma logic.

## Usage
Simply import the required component directly from the package:

```ts
import { Utils, AppError } from "@harpia/common";

const formatted = Utils.string.camelCase("Hello World");
if (!formatted) {
  throw new AppError("Invalid input", 400);
}
```
