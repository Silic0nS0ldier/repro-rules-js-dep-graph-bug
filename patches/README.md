# Patches

There are generated using;

1. `pnpm patch <package-name>@<package-version>`
2. Make changes in returned directory.
3. `pnpm patch-commit <directory>`
4. Make changes in `WORKSPACE.bazel`.

Webpack patches relate to resolution logic (simplifying it to help narrow down cause of issues). In the case of the CLI, it offers a rich experience around correcting missing dependencies. Overkill and ends up hiding the error when run in a non-interactive environment (e.g. `run_js_binary`).
