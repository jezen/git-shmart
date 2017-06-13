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

Stick each of the `git-shmart` scripts somewhere on your path. Be sure to keep
the name of each script as-is. If you get permission errors when running the
commands, be sure to change their modes to executable.

```sh
chmod u+x ~/.bin/git-shmart-log
chmod u+x ~/.bin/git-shmart-pull
chmod u+x ~/.bin/git-shmart-merge
```

For convenience, you should add the _git-shmart_ functions as aliases in your
`~/.gitconfig` file.

```sh
# ~/.gitconfig

[alias]
	sl = shmart-log
	sp = shmart-pull
	sm = shmart-merge
```

### Usage

The _git-shmart_ commands should be ready to use like any other Git command,
assuming the scripts are available on your path, and you kept the file names as
they were.

If you installed all three scripts, then you should have the following three commands:

```sh
git shmart-log
git shmart-pull
git shmart-merge
```

If you set up aliases in your `~/.gitconfig`, then those should work too.

```sh
# Expands to git shmart-log
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
