# Project memory

## Product intent & audience

- Vite + React app being deployed via a build pipeline (likely a WebContainer-based preview/deploy environment).

## Brand personality & voice

- Not yet inferred.

## Visual design & UX direction

- Uses Tailwind CSS v4 integrated via `@tailwindcss/vite` plugin (inferred from vite.config.ts import).
- TypeScript project (`vite.config.ts`).

## Decisions, constraints & rationale

- Build tool: Vite 8 with `@vitejs/plugin-react`.
- **Dependency fix applied:** esbuild bumped from `^0.25.0` to `^0.27.0 || ^0.28.0`-compatible version to satisfy Vite 8 peer dependency requirement; resolved `ERR_MODULE_NOT_FOUND` deployment failure.
- Lockfile regenerated after install fix.
- `__dirname` warning in vite.config.ts is harmless and can be ignored.
- Deployment environment downloads `@rolldown/binding-wasm32-wasi` and shows experimental WASI warnings — benign.

## Open questions & assumptions

- Tailwind version and config details not yet confirmed beyond plugin usage.
- No app-level feature/domain context inferred yet.
- Exact esbuild pinned version after bump not verified — confirm in `package.json` if revisited.