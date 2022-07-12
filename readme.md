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

Got to [localhost:3000](http://localhost:3000) and observe in the terminal:

```
url:  /__vite_ping
Why wasn't intercepted by Vite's dev middleware?
```

The `console.log()`S live at [/server/index.js#L32-L33](https://github.com/brillout/vite3-ping-bug/blob/685db3c0c676ea78e67c714b1cc591d11a562dbe/server/index.js#L32-L33).

Why isn't the `/__vite_ping` HTTP request intercepted by the Vite middleware at [/server/index.js#L26](https://github.com/brillout/vite3-ping-bug/blob/685db3c0c676ea78e67c714b1cc591d11a562dbe/server/index.js#L26)?
