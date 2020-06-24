# GitHub Branch Renamer

A tool to rename the `master` branch for an entire account at once.

## Installation

### macOS

Install with Homebrew.

```sh
brew install erbridge/tap/github-branch-renamer
```

### Everything else

You're on your own, I'm afraid. Refer to the [`Brewfile`](Brewfile) for clues
about required dependencies.

## Usage

```
$ gbr
Rename the 'master' branch for an entire account at once.

This tool will find all repositories on GitHub belonging to an account that:

  - aren't forks
  - aren't archived or disabled
  - have their default branch set to 'master'

It will then rename the master branch to 'main' by default, and set that as the
default branch on GitHub instead of 'master'.

By default, the 'master' branch will be left untouched to prevent any accidental
data loss. If you'd like to delete those branches, set the '--delete' flag.

You must choose to either do a dry run ('--dry-run') or force the changes
('--force'). You must also specify one of '--org' or '--user' (but not both) to
select the account to collect repositories from.

USAGE
  gbr [flags]

FLAGS
  -u, --user string         The username to collect repositories in
  -o, --org string          The organization to collect repositories in
  -t, --team string         The team within the organization (optional)
  -b, --new-branch string   The new name for the master branch (defaults to
                              'main')
  -d, --delete              Delete the master branch from GitHub
  -n, --dry-run             Report what will happen, without making any changes
                               on GitHub
  -f, --force               Run for real, making changes on GitHub
  -l, --list                Print a list of all GitHub repositories that would
                               be changed and exits (implies a dry runs)
```

## Why?

The conversation about the origin of "master" as a term in technology has come
back around again recently. It's clear that Git's default branch name, `master`,
[originated from a master-slave metaphor](https://mail.gnome.org/archives/desktop-devel-list/2019-May/msg00066.html),
and even if it didn't, it still has that connotation for some people. We should
rename our branches to something else to reduce the harm our language causes.

Renaming branches can be a time consuming, manual process, especially if your
repositories are counted in the hundreds. It would be preferable to automate as
much of that as possible. This tool attempts to do that.

This tool is limited to existing repositories. Until Git changes its defaults,
new repositories will still be created with a `master` branch. See
[Leigh Brenecki's post](https://leigh.net.au/writing/git-init-main/) for how to
override that default behaviour.
