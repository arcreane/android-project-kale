# Husky & commitlint

This project uses `Husky` and `commitlint` to enforce [Conventional Commits](https://github.com/arcreane/android-project-kale/blob/main/docs/COMMIT_CONVENTION.md) to maintain a professional R&D history and enable automated changelog generation.

## Enforcement Layers

* **Local (Husky):** Intercepts commits on machine via a `commit-msg` hook.
* **Remote (GitHub Actions):** Validates all Pushes and PRs in the cloud to ensure branch integrity.

## Tooling

* **[commitlint](https://commitlint.js.org/):** The engine that validates message structure.
* **[Husky](https://typicode.github.io/husky/):** Connects the linter to Git's lifecycle.

## ⚠️ Bypass

If absolutely necessary, bypass local hooks using:
`git commit -m "..." --no-verify`
*Note: GitHub CI will still reject the push if the format is invalid.*
