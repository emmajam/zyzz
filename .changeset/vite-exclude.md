---
'zyzz': patch
---

Added `exclude` to the Vite plugin, leaving matching source modules out of discovery and transforms. Globs resolve against the Vite root, and regular expressions test absolute paths. Modules named `vite.config.*`, `vitest.config.*`, or `vitest.workspace.*` are always excluded, so a Vitest config no longer sends `vitest/config` to the development dependency optimizer.

```ts
zyzz({ exclude: ['server.mjs', /\.stories\.tsx?$/] })
```
