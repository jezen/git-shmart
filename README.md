<h1 align="center">git-shmart</h1>

A small collection of Git wrappers. Inspired by [geelen/git-smart][0], but
implemented in Bash.

⚠️ WORK IN PROGRESS. DO NOT USE ⚠️

### Motivation

I use _git-smart_ all the time, but I sometimes have to reinstall it if I switch
Ruby versions. I don't think this tool needs Ruby as a dependency.

Also, there are some issues with the original, and the original project seems to
be no longer maintained.

### Installation

Stick [`git-shmart`][1] somewhere on your path, and source it from your shell's
_run commands_ file.

Then, add the _git-shmart_ functions as aliases in your `~/.gitconfig` file.

```sh
# ~/.gitconfig

[alias]
	sl = shmart-log
	sp = shmart-pull
	sm = shmart-merge
```

### Usage

The _git-shmart_ commands can be used like any other Git alias.

```sh
git sl
```

### Testing

You'll need to have `shunit2` installed. Install it with:

```sh
# on MacOS
brew install shunit2

# ...or on Debian
apt-get install shunit2
```

Then to run the tests:

```sh
make test
```

[0]: https://github.com/geelen/git-smart
[1]: https://github.com/jezen/git-shmart/blob/master/git-shmart
