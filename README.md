# repro-crach-use-pnpm-histoire

## Procedure

```bash 
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
