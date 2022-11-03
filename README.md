# Repro for dependency graph representation bug

`pnpm-lock.yaml` states `webpack` should be present in `webpack-cli`'s `node_modules` scope, but its not.

Side note, `webpack` and `webpack-cli` depend on each other (cyclic dependency).

To repro run

```
bazel build //web/src/webpack-testing:baz-min
bazel build //web/src/webpack-testing:baz-min --experimental_allow_unresolved_symlinks
```
