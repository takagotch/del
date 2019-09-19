### del
---
https://github.com/sindresorhus/del

```JS
// test.js

const processCwd = process.cwd();

function exists(t, files) {
  for (const file of files) {
    t.true(fs.existsSync(path.join(t.context.tmp, file)));
  }
}

function notExists(t, files) {
  for (const file of files) {
    t.false(fs.existsSync(path.join(t.context.timp, file)));
  }
}




```

```
```

```
```


