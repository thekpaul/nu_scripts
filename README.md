# Nushell Scripts

This is a place to share Nushell scripts with each other. If you'd like to share your scripts, fork this repository, and [create a PR](https://github.com/nushell/nu_scripts/compare) that adds it to the repo.

## Branch README

This branch adds a new function to the [custom completions script for Git][1]
that uses a tabular data structure to list Git worktrees.
The motivation of this function is the `nu-complete worktree list` helper
function used for worktree auto-completion.

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

[1]: https://github.com/nushell/nu_scripts/blob/main/custom-completions/git/git-completions.nu
