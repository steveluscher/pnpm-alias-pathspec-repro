# Repro

```shell
pnpm i
cd packages/app/
pnpm turbo hello
```

# Expected outcome

Since the dependency `luigi` is aliased to `workspace:../waluigi`, I would expect the `hello` script from `waluigi/package.json` to run.

# Actual outcome

The `hello` script from `luigi/package.json` runs.

> [!NOTE]
> If you change the dependency in `app/package.json` from `"luigi": "workspace:../waluigi"` to `"luigi": "workspace:waluigi@*"` it works as expected.
