Nushell Scripts
===

This is a place to share Nushell scripts with each other.
If you'd like to share your scripts _upstream_, fork this repository and
[create a PR][up_PR] that adds it to the repo.

> [!NOTE]
> Forked from (and following) [`nushell/nu_scripts`][upstream]

## Fork README

This repository is my personal fork from the [`nushell/nu_scripts`][upstream]
repository featuring external scripts to enhance the Nushell experience.

### Maintaining the Fork

Self-tailored changes will be developed in individual "feature" branches and
merged to the [`main`][fork] branch of this fork.
If considered mature enough, these may even be formatted into
[Pull Requests][up_PR] to be submitted upstream.
"Feature" branches will only be removed if:
1. successfully merged to upstream as Pull Requests, at which time its
   corresponding commits upstream will be merged into this fork, OR
2. merged into [`main`][fork] on this fork without any plans for future
   Pull Request submission to upstream.

New commits from the upstream repository [`nushell/nu_scripts`][upstream] will
also be merged into the [`main`][fork] branch of this fork spontaneously.
Commits on this fork may be rebased onto any future upstream commits that
do not cause major conflicts with pre-existing downstream modifications.
"Feature" branches mentioned above will also undergo merges and/or rebases with
upstream commits if they are affected in any way.

### Local Usage with [Sparse Checkout][sparse-checkout]

The upstream repository [`nushell/nu_scripts`][upstream] is a "mono-repo"
containing various sections, many of which will not be used in this fork.
To save local storage, the [`sparse-checkout`][sparse-checkout] subcommand can
be used to maintain only a subset of tracked files, ignoring unused components:
```sh
git sparse-checkout set <subset>
```
This allows using only the necessary directories and files locally without any
disruptions from following the upstream mono-repo.

### Changelog

- 24 Dec 2025: New function `git worktree table` to
  [custom completions script for Git][git-complete] that uses a tabular data
  structure to list Git worktrees.
  The motivation of this function is the `nu-complete worktree list` helper
  function used for worktree auto-completion.

## Sections

- [aliases](./aliases/)
- [benchmarks](./benchmarks/)
- [cool-oneliners](./sourced/cool-oneliners/)
- [custom-completions](./custom-completions/) - collection of custom
  completions for external commands.
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
2. From with nushell, you can type `source <script name>` and if the script is
   just a bunch of commands it will run the script.
   If the script is a custom command it will load those custom commands into
   your current scope so you can run them like any other command.

[upstream]: https://github.com/nushell/nu_scripts
[up_PR]: https://github.com/nushell/nu_scripts/compare
[fork]: https://github.com/thekpaul/nu_scripts
[sparse-checkout]: https://git-scm.com/docs/git-sparse-checkout

[git-complete]: ./custom-completions/git/git-completions.nu
