<h1 align="center">git-shmart</h1>

A small collection of Git wrappers. Inspired by [geelen/git-smart][0], but
implemented in Bash.

### Motivation

I use _git-smart_ all the time, but I sometimes have to reinstall it if I switch
Ruby versions. I don't think this tool needs Ruby as a dependency.

Also, there are some issues with the original, and the original project seems to
be no longer maintained.

_n.b._ The `shmart-merge` command still isn't implemented.

### Usage

Clone this repository somewhere on your machine, and then add the `git-shmart`
directory to your path. The executables should be automatically available to
Git.

Upon successful installation, you will have the following commands available:

```sh
git shmart-log
git shmart-pull
```

For convenience, you should add the _git-shmart_ functions as aliases in your
`~/.gitconfig` file.

```sh
# ~/.gitconfig

[alias]
	sl = shmart-log
	sp = shmart-pull
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
