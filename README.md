# repro-crach-use-pnpm-histoire

## Related Issue
https://github.com/histoire-dev/histoire/issues/282

## Procedure

```bash 
pnpm -v
7.14.2

pnpm install

pnpm story:dev
```

## Error contents

```bash
$ pnpm story:dev

> repro-crach-use-pnpm-histoire@0.0.1 story:dev /workspace/repro-crach-use-pnpm-histoire
> histoire dev

  ➜  Local:   http://127.0.0.1:6006/
  ➜  Network: use --host to expose
Collect stories start all
Error while collecting story /workspace/repro-crach-use-pnpm-histoire/node_modules/.histoire/plugins/builtin_tailwind-tokens/Tailwind.story.js:
Error: [vite-node] Failed to load @histoire/controls
    at ViteNodeRunner.directRequest (file:///workspace/repro-crach-use-pnpm-histoire/node_modules/.pnpm/vite-node@0.22.1/node_modules/vite-node/dist/client.mjs:165:13)
    at async ViteNodeRunner.cachedRequest (file:///workspace/repro-crach-use-pnpm-histoire/node_modules/.pnpm/vite-node@0.22.1/node_modules/vite-node/dist/client.mjs:113:12)
    at async request (file:///workspace/repro-crach-use-pnpm-histoire/node_modules/.pnpm/vite-node@0.22.1/node_modules/vite-node/dist/client.mjs:136:16)
    at async histoire/dist/node/vendors/controls.js:1:238
    at async ViteNodeRunner.directRequest (file:///workspace/repro-crach-use-pnpm-histoire/node_modules/.pnpm/vite-node@0.22.1/node_modules/vite-node/dist/client.mjs:217:5)
    at async ViteNodeRunner.cachedRequest (file:///workspace/repro-crach-use-pnpm-histoire/node_modules/.pnpm/vite-node@0.22.1/node_modules/vite-node/dist/client.mjs:113:12)
    at async request (file:///workspace/repro-crach-use-pnpm-histoire/node_modules/.pnpm/vite-node@0.22.1/node_modules/vite-node/dist/client.mjs:136:16)
    at async /workspace/repro-crach-use-pnpm-histoire/node_modules/.histoire/plugins/builtin_tailwind-tokens/Tailwind.story.js:7:31
    at async ViteNodeRunner.directRequest (file:///workspace/repro-crach-use-pnpm-histoire/node_modules/.pnpm/vite-node@0.22.1/node_modules/vite-node/dist/client.mjs:217:5)
    at async ViteNodeRunner.cachedRequest (file:///workspace/repro-crach-use-pnpm-histoire/node_modules/.pnpm/vite-node@0.22.1/node_modules/vite-node/dist/client.mjs:113:12)
Collect stories end 1335 ms
```

## Additional error content

Message displayed on first startup after removing `node_modules`

```bash
$ pnpm story:dev

> repro-crach-use-pnpm-histoire@0.0.1 story:dev /workspace/repro-crach-use-pnpm-histoire
> histoire dev


 (x2)
Forced re-optimization of dependencies
Failed to resolve dependency: flexsearch, present in 'optimizeDeps.include'
Failed to resolve dependency: shiki, present in 'optimizeDeps.include'
Failed to resolve dependency: vscode-oniguruma, present in 'optimizeDeps.include'
Failed to resolve dependency: vscode-textmate, present in 'optimizeDeps.include'
Using 8 threads for story collection
Collect stories start all
  ➜  Local:   http://127.0.0.1:6006/
  ➜  Network: use --host to expose
src/lib/Counter.story.svelte 1959ms (setup:25ms, execute:24ms, run:1909ms)
Collect stories end 2529ms
```