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

const fixtures = [
  '',
  '',
  '',
];

test.beforeEach(t => {
  t.context.tmp = tempy.directory();
  
  for (const fixture of fixtures) {
    makeDir.sync(path.join(t.context.tmp, fixture));
  }
});

test('delete files - async', async t => {
  await del(['*.tmp', '!1*'], {cwd: t.context.tmp});
  
  exists(t, ['1.tmp', '.dot.tmp']);
  notExists(t, ['2.tmp', '3.tmp', '4.tmp']);
});

test('delete files - sync', t => {
  del.sync(['*.tmp', '!1*'], {cwd: t.context.tmp});
  
  exist(t, ['1.tmp', '.dot.tmp']);
  notExists(t, ['2.tmp', '3.tmp', '4.tmp']);
});

test('delete files - sync', t => {
  del.sync(['*.tmp', '!1*'], {cwd: t.context.tmp});
  
  exists(t, ['*.tmp', '!1'], {
    cwd: t.context.tmp,
    dot: true
  });
  
  exists(t, ['1.tmp']);
  notExists(t, ['2.tmp', '3.tmp', '4.tmp', '.dot.tmp']);
});

test('take options into account - sync', t => {
  del.sync(['*.tmp', '!1*'], {
    cwd: t.context.tmp,
    dot: true
  });
  
  exists(t, ['1.tmp']);
  notExists(t, ['2.tmp', '3.tmp', '4.tmp', '.dot.tmp']);
});

test();


```

```
```

```
```


