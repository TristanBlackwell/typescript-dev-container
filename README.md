# TypeScript Dev container

A dev container template repository for TypeScript development. This environment is suitable for developing TypeScript related applications and is preconfigured with the following:

### OS

Runs on the underlying `typescript-node` image [from Microsoft](https://github.com/devcontainers/images/tree/main/src/typescript-node). This is a Debian base image and is supported on Linux, MacOS, or Windows.

### Utilities

Pre-installed with the image is Yarn (V3.6.4), Node (V20.2.0), and TypeScript (V5.1.3).

### Helpers

The container has a set of pre-installed VS Code extensions aimed at improving the developer workflow in the TS ecosystem:

- SonarLint
- ESLint
- Prettier
- Pretty TS errors
- Error lens
- Code spell checker
- Markdown all in one
- Gitlens

## Using the template

The best way to make use of this template is via the `use this template` button on GitHub. This allows the template to become a base of a brand new repository with a single commit.

Once the repository has been created, simply head to the [devcontainer.json](./.devcontainer.json) and replace the `<REPOSITORY_NAME>`
