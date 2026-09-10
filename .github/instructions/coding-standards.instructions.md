---
description: 'Commenting, documentation, and TypeScript conventions for Tailspin Toys'
applyTo: '**/*.{ts,astro}'
---

# Coding Standards

## Comments and documentation

- Comment intent, constraints, and non-obvious decisions; do not restate what the code already expresses.
- Keep comments current with the implementation. Update or remove a comment when the related behavior changes.
- Use TSDoc/JSDoc for every exported function in `db/` and `src/lib/`.
- Exported function documentation must explain the purpose, each parameter, and the return value. For data-access helpers, document the injectable `db` parameter so callers understand how production and test databases are supplied.
- Reusable Astro components must document their `Props` interface and any non-obvious prop behavior. Document individual properties when their meaning, accepted values, or defaults are not obvious from the type.
- Preserve comments that explain a reason a reader could not infer from the code, such as transaction safety, cross-platform behavior, or a type-system limitation.

## TypeScript formatting and typing

- Use four spaces for indentation and keep one statement per line.
- Prefer single quotes for strings and semicolons for statement termination, matching the existing project style.
- Use explicit parameter and return types for exported functions and data-layer helpers.
- Use `import type` for type-only imports and keep imports grouped at the top of the file.
- Prefer named interfaces or type aliases for public object shapes instead of inline repeated object types.
- Keep formatting rules enforceable through ESLint; do not add a formatter-specific dependency for these conventions.
