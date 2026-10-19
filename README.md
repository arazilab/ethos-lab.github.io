# ETHOS Lab website

A modular static replica of the public ETHOS Lab website at [ethos-lab.org](https://www.ethos-lab.org/).

## Preview

```sh
npm install
npm run dev
```

## Build

```sh
npm run build
npm run preview
```

The build is configured for the GitHub Pages project path `/ethos-lab.github.io/`.
See [AGENTS.md](./AGENTS.md) for the Hermes contribution workflow.

## Repository setup

After creating `arazilab/ethos-lab.github.io` on GitHub:

1. Push this project to the repository's `main` branch.
2. In repository Settings, enable Pages with **GitHub Actions** as the source.
3. Add a branch rule for `main` that requires pull requests and the **Check website build / build** status check.
4. Give the Hermes agent access to the repository and ask it to follow `AGENTS.md`.

The default project-site address is `https://arazilab.github.io/ethos-lab.github.io/`.
