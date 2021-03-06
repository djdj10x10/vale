# Vale: Your Style, Our Editor

[![Build Status](https://travis-ci.org/ValeLint/vale.svg?branch=master)](https://travis-ci.org/ValeLint/vale) [![Build status](https://ci.appveyor.com/api/projects/status/snk0oo6ih1nwuf6r/branch/master?svg=true)](https://ci.appveyor.com/project/jdkato/vale/branch/master) [![Go Report Card](https://goreportcard.com/badge/github.com/ValeLint/vale)](https://goreportcard.com/report/github.com/ValeLint/vale) [![codebeat](https://codebeat.co/badges/a9b4b73a-182d-4ed7-8019-0fc5957bad91)](https://codebeat.co/projects/github-com-valelint-vale-master) [![license](https://img.shields.io/github/license/mashape/apistatus.svg)]()

![demo](https://cloud.githubusercontent.com/assets/8785025/22951386/df064226-f2bd-11e6-84e3-4cedfc098528.png)

Vale is a linter for prose&mdash;no matter if it's plain text, markup or source-code comments. It's built around a plugin system that allows it to lint against arbitrary rules. In practice, this means that it can help you adhere to entire editorial style guides or simply break writer-specific bad habits (see [Use Cases](https://github.com/ValeLint/vale/wiki/Use-Cases) for more ideas).


Here's an example of Vale's versatility:

```ini
# These options are specified in either a .vale or _vale file.
StylesPath = path/to/my/project/styles/directory
MinAlertLevel = warning

[*.{md,txt}]
BasedOnStyles = TheEconomist
vale.Editorializing = YES

[*.py]
BasedOnStyles = vale
write-good.ThereIs = YES
vale.PassiveVoice = NO
```

In this case, we are linting all Markdown and text files in our project against [The Economist](http://www.economist.com/styleguide/introduction). We are also linting Python comments against `vale` and [`write-goods`](https://github.com/btford/write-good)'s `ThereIs` rule.

Check out [the wiki](https://github.com/ValeLint/vale/wiki) to learn more!

## Features

- [X] Supports Markdown, reStructuredText, AsciiDoc, HTML, and source code
- [X] Extensible without programming experience
- [X] Standalone binaries for Windows, macOS, and Linux
- [X] Expressive, [EditorConfig-like](http://editorconfig.org/) configuration

## Installation

**macOS**

Install through [Homebrew](http://brew.sh):

```bash
$ brew tap ValeLint/vale
$ brew install vale
```

**Manually install for Windows, macOS and Linux**

Download and install an executable from the [releases page](https://github.com/valelint/vale/releases).

See the [project wiki](https://github.com/ValeLint/vale/wiki) for more information.
