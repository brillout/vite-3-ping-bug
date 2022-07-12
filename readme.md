Bug reproduction.

```bash
git clone git@github.com:brillout/vite3-ping-bug
cd vite3-ping-bug/
pnpm install
pnpm run dev
```

Same as single line (copy-paste me):

```shell
git clone git@github.com:brillout/vite3-ping-bug && cd vite3-ping-bug/ && pnpm install && pnpm run dev
```

Observe:

```
Server running at http://localhost:3000
url:  /__vite_ping
Why wasn't intercepted by Vite's dev middleware?
```
