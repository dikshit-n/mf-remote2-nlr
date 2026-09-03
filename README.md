# mf-remote2-nlr

Member micro-frontend in a **Nuxt Layers micro-frontend boilerplate**.
Lives at `github.com/dikshit-n/mf-remote2-nlr`.

## Role in the Nuxt Layers MFE

This is the **member** remote. It contributes the member-facing pages
(`/member/manage`, `/dashboard`, …) that the shell mounts through
`<NuxtPage />`. The shell extends it last so it inherits everything the
core and administration layers provide:

```ts
extends: [
  ['github:dikshit-n/mf-core-nlr#master',    { install: true }], // shared reusables
  [`github:dikshit-n/mf-remote1-nlr#master`, { install: true }], // administration micro-frontend
  [`github:dikshit-n/mf-remote2-nlr#master`, { install: true }], // ← this layer (member)
],
```

It depends on `mf-core-nlr` for the layout, navigation, design tokens, and
shared composables — it does not re-implement any of that.

## Business responsibility

**Example:** end-user-facing work — the day-to-day screens that operators
of the application use. A typical deployment of this remote owns areas
such as:

- A member-management screen (e.g. `/member/manage` in the boilerplate)
- A dashboard / overview screen (e.g. `/dashboard` in the boilerplate)
- Other member-centric workflows as the product grows

This is the "main surface" of the application — the screens a typical
user actually spends time in.

## This layer is not standalone

This repository is a **Nuxt layer**, not a runnable app. Its pages and
components are merged into the shell at build/dev time. To run it:

```sh
git clone github.com/dikshit-n/mf-shell-nlr
cd mf-shell-nlr
yarn install
yarn dev   # http://localhost:5000/member/manage
```

## Related repositories

- [`mf-shell-nlr`](https://github.com/dikshit-n/mf-shell-nlr) — the composition root (shell) that loads this layer.
- [`mf-core-nlr`](https://github.com/dikshit-n/mf-core-nlr) — shared reusables (loaded before this).
- [`mf-remote1-nlr`](https://github.com/dikshit-n/mf-remote1-nlr) — the other remote (administration).
