1. `npm i`
2. Open in IntelliJ
3. Put a breakpoint on line 2
4. Run `main.js` and debug it
5. When it stops on line 2, click to "step in"
6. It'll bring you to `assertion.ts`. Try to put a breakpoint anywhere in the file. It won't work.

If you look at `Help > Show Log in Finder > idea.log`, you'll see something like:

```
2024-03-26 17:10:43,308 [ 257715]   WARN - #o.j.r.CommandProcessor - incorrect sourcemap, several mappings for named element value
2024-03-26 17:10:43,309 [ 257716]   WARN - #o.j.r.CommandProcessor - incorrect sourcemap, several mappings for named element value as Partial<ErrorLike>
2024-03-26 17:10:43,309 [ 257716]   WARN - #o.j.r.CommandProcessor - incorrect sourcemap, several mappings for named element value
2024-03-26 17:10:43,310 [ 257717]   WARN - #o.j.r.CommandProcessor - incorrect sourcemap, several mappings for named element value as Partial<ErrorLike>
2024-03-26 17:10:43,310 [ 257717]   WARN - #o.j.r.CommandProcessor - incorrect sourcemap, several mappings for named element value as Partial<ErrorLike>
2024-03-26 17:10:43,310 [ 257717]   WARN - #o.j.r.CommandProcessor - incorrect sourcemap, several mappings for named element value as Partial<ErrorLike>
2024-03-26 17:10:44,394 [ 258801]   WARN - #c.i.j.d.JavaScriptDebugProcess - Unable to set breakpoint with null position: mock://file:///Users/mhentges/dev/backstage-sourcemap-repro/node_modules/@backstage/errors/src/errors/assertion.ts
2024-03-26 17:10:45,730 [ 260137]   WARN - #c.i.j.d.JavaScriptDebugProcess - Unable to set breakpoint with null position: mock://file:///Users/mhentges/dev/backstage-sourcemap-repro/node_modules/@backstage/errors/src/errors/assertion.ts
```
