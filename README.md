oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g viji-cli
$ viji-cli COMMAND
running command...
$ viji-cli (--version)
viji-cli/0.0.0 linux-x64 node-v18.18.0
$ viji-cli --help [COMMAND]
USAGE
  $ viji-cli COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`viji-cli hello PERSON`](#viji-cli-hello-person)
* [`viji-cli hello world`](#viji-cli-hello-world)
* [`viji-cli help [COMMANDS]`](#viji-cli-help-commands)
* [`viji-cli plugins`](#viji-cli-plugins)
* [`viji-cli plugins:install PLUGIN...`](#viji-cli-pluginsinstall-plugin)
* [`viji-cli plugins:inspect PLUGIN...`](#viji-cli-pluginsinspect-plugin)
* [`viji-cli plugins:install PLUGIN...`](#viji-cli-pluginsinstall-plugin-1)
* [`viji-cli plugins:link PLUGIN`](#viji-cli-pluginslink-plugin)
* [`viji-cli plugins:uninstall PLUGIN...`](#viji-cli-pluginsuninstall-plugin)
* [`viji-cli plugins:uninstall PLUGIN...`](#viji-cli-pluginsuninstall-plugin-1)
* [`viji-cli plugins:uninstall PLUGIN...`](#viji-cli-pluginsuninstall-plugin-2)
* [`viji-cli plugins update`](#viji-cli-plugins-update)

## `viji-cli hello PERSON`

Say hello

```
USAGE
  $ viji-cli hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/vijayashreed/viji-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `viji-cli hello world`

Say hello world

```
USAGE
  $ viji-cli hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ viji-cli hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [dist/commands/hello/world.ts](https://github.com/vijayashreed/viji-cli/blob/v0.0.0/dist/commands/hello/world.ts)_

## `viji-cli help [COMMANDS]`

Display help for viji-cli.

```
USAGE
  $ viji-cli help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for viji-cli.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.19/src/commands/help.ts)_

## `viji-cli plugins`

List installed plugins.

```
USAGE
  $ viji-cli plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ viji-cli plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.7.0/src/commands/plugins/index.ts)_

## `viji-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ viji-cli plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ viji-cli plugins add

EXAMPLES
  $ viji-cli plugins:install myplugin 

  $ viji-cli plugins:install https://github.com/someuser/someplugin

  $ viji-cli plugins:install someuser/someplugin
```

## `viji-cli plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ viji-cli plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ viji-cli plugins:inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.7.0/src/commands/plugins/inspect.ts)_

## `viji-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ viji-cli plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ viji-cli plugins add

EXAMPLES
  $ viji-cli plugins:install myplugin 

  $ viji-cli plugins:install https://github.com/someuser/someplugin

  $ viji-cli plugins:install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.7.0/src/commands/plugins/install.ts)_

## `viji-cli plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ viji-cli plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ viji-cli plugins:link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.7.0/src/commands/plugins/link.ts)_

## `viji-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ viji-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ viji-cli plugins unlink
  $ viji-cli plugins remove
```

## `viji-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ viji-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ viji-cli plugins unlink
  $ viji-cli plugins remove
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.7.0/src/commands/plugins/uninstall.ts)_

## `viji-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ viji-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ viji-cli plugins unlink
  $ viji-cli plugins remove
```

## `viji-cli plugins update`

Update installed plugins.

```
USAGE
  $ viji-cli plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v3.7.0/src/commands/plugins/update.ts)_
<!-- commandsstop -->
# oclif-cli
