yamlscript-vs-rosetta
=====================

Compare YAMLScript Rosetta Code Programs to Other Languages


## Synopsis

```
$ ys-vs-rc task=99-bottles-of-beer
https://gist.github.com/...
```


## Description

[YAMLScript](https://yamlscript.org) is a programming language that has many
[example programs](https://rosettacode.org/wiki/Category:YAMLScript) on
[RosettaCode](https://rosettacode.org).

The `ys-vs-rc` command generates a Markdown page (and optionally posts it as a
[GitHub gist page](https://gist.github.org)) that compares a YAMLScript
solution for a particular RosettaCodes task to the solutions from other common
programming languages.

The `ys-vs-rc` command is written in YAMLScript.


## Usage

To get `ys-vs-rc` in your `PATH`, run `source .rc` (for bash or zsh).

Or just run `bin/ys-vs-rc <options>` directly.

You'll need to have the `ys` command [installed](
https://yamlscript.org/doc/install/).

> If you don't want to install `ys` you can just run `ys-vs-rc` with bash:
> ```
> $ bash $(which ys-vs-rc) <options>
> ```
> This will install the `ys` command under `/tmp/` the first time you run it.

The list of programming languages to use is in `config.yaml` and you can change
it to your liking.


## CLI Options

The `ys-vs-rc` command has a few options.
For example:

```
$ ys-vs-rc task-list
...
100-prisoners
99-bottles-of-beer
Average-loop-length
...
$ ys-vs-rc task=99-bottles-of-beer gist=true token=$gh_token
https://gist.github.com/yourstruly/79d067d2be6639a88796e6dcd0fdab60
```

* `task-list` - List the available YAMLScript programs to compare.
* `task=<rc-task-name>` - The name of the task to compare.
* `gist=(true|false)` - Default is true if `token=...` or `YSVSRC_GH_TOKEN` env
  var is set.
  Publishes generated markdown as a GitHub Gist and prints the URL for it.
* `token=<github-token>` - Default is `YSVSRC_GH_TOKEN`.
  A token is needed to publish the markdown as a Gist.
* `config=<file>` - You can override the default config file.
