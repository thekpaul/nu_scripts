# Nushell Scripts

This is a place to share Nushell scripts with each other. If you'd like to share your scripts, fork this repository, and [create a PR](https://github.com/nushell/nu_scripts/compare) that adds it to the repo.

## Fork README

This repository is a fork from the [`nushell/nu_scripts`][upstream] repository
housing external scripts to enhance the Nushell experience.

Commits on this fork may be rebased onto any future upstream commits that
do not cause major conflicts with pre-existing downstream modifications.

### Current Dev Branches

- [`complete-git-functions`][complete-git-functions]:
  Git Custom Completions New Functionalities
  - New function `git worktree table` (commit [`c60cd5b`][c60cd5b])
- [`complete-bat-flags`][complete-bat-flags]:
  bat Custom Completions Flags Update
  - Flags updated and extended based on help message
    (commit [`d010754`][d010754])
- [`complete-winget-locale`][complete-winget-locale]:
  WinGet Custom Completions Locale Adaptation

### Forked Main Branch Changelog

- 14 May 2025
  - `git worktree table` function for **Git** from commit [`c60cd5b`][c60cd5b]
    on branch [`complete-git-functions`][complete-git-functions].
  - Flags updated and extended based on help message for **bat** from commit
    [`d010754`][d010754] on branch [`complete-bat-flags`][complete-bat-flags].

## Sections

- [aliases](./aliases/)
- [benchmarks](./benchmarks/)
- [cool-oneliners](./sourced/cool-oneliners/)
- [custom-completions](./custom-completions/) - collection of custom completions for external commands.
- [custom-menus](./custom-menus/) - collection of custom nushell menus
- [example-config](./example-config/)
- [nu-hooks](./nu-hooks/)
- [modules](./modules/) - This has its dedicated [readme](./modules/README.md)
- [nu_101](./sourced/nu_101/) - Beginner introduction to nushell concepts.
- [prompt](./modules/prompt/)
- [themes](./themes/)

## Running Scripts

You can run nushell scripts in a few different ways.

1. You can type `nu <script name>`.
2. From with nushell, you can type `source <script name>` and if the script is just a bunch of commands it will run the script. If the script is a custom command it will load those custom commands into your current scope so you can run them like any other command.

[upstream]: https://github.com/nushell/nu_scripts
[complete-git-functions]: https://github.com/thekpaul/nu_scripts/tree/complete-git-functions
[complete-bat-flags]: https://github.com/thekpaul/nu_scripts/tree/complete-bat-flags
[complete-winget-locale]: https://github.com/thekpaul/nu_scripts/tree/complete-winget-locale

[c60cd5b]: https://github.com/thekpaul/nu_scripts/commit/c60cd5bea765a52fd36cd46598bb2b02109e8b63
[d010754]: https://github.com/thekpaul/nu_scripts/commit/d01075458d7286efa1e196131e597cdc7a664224
