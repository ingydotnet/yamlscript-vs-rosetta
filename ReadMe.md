ys-rc
==============================

Compare YAMLScript Rosetta Code Programs to Other Languages


## Synopsis

```
$ ys-rc task=99-bottles-of-beer
https://gist.github.com/...
```


## Description

[YAMLScript](https://yamlscript.org) is a programming language that has many
[example programs](https://rosettacode.org/wiki/Category:YAMLScript) on
[RosettaCode](https://rosettacode.org).

The `ys-rc` command generates a Markdown page (and optionally posts it as a
[GitHub gist page](https://gist.github.org)) that compares a YAMLScript
solution for a particular RosettaCodes task to the solutions from other common
programming languages.

The `ys-rc` command is written in YAMLScript.


## Usage

To get `ys-rc` in your `PATH`, run `source .rc` (for bash or zsh).

Or just run `bin/ys-rc <options>` directly.

You'll need to have the `ys` command [installed](
https://yamlscript.org/doc/install/).

> If you don't want to install `ys` you can just run `ys-rc` with bash:
> ```
> $ bash $(which ys-rc) <options>
> ```
> This will install the `ys` command under `/tmp/` the first time you run it.

The list of programming languages to use is in `config.yaml` and you can
it to your liking.


## CLI Options

The `ys-rc` command has a few options and `task=<task-name>` is required.
For example:

```
ys-rc task=99-bottles-of-beer config=my-config.yaml gist=false
```

* `task=<rc-task-name>` (Required) Use `ys-rc list` to see all task names.
* `gist=(true|false)` (Optional) Default is true if `token=...` or
  `YSRC_GH_TOKEN` env var is set.
  Publishes generated markdown as a GitHub Gist and prints the URL for it.
* `token=<github-token>` (Optional) Default is `YSRC_GH_TOKEN`.
  A token is needed to publish the markdown as a Gist.
* `config=<file>` (Optional) You can override the default config file.
