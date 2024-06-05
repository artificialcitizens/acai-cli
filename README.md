acai
=================

your ai powered terminal


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/acai.svg)](https://npmjs.org/package/acai)
[![Downloads/week](https://img.shields.io/npm/dw/acai.svg)](https://npmjs.org/package/acai)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g acai
$ acai COMMAND
running command...
$ acai (--version)
acai/0.0.0 darwin-arm64 node-v18.20.3
$ acai --help [COMMAND]
USAGE
  $ acai COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`acai hello PERSON`](#acai-hello-person)
* [`acai hello world`](#acai-hello-world)
* [`acai help [COMMAND]`](#acai-help-command)
* [`acai plugins`](#acai-plugins)
* [`acai plugins add PLUGIN`](#acai-plugins-add-plugin)
* [`acai plugins:inspect PLUGIN...`](#acai-pluginsinspect-plugin)
* [`acai plugins install PLUGIN`](#acai-plugins-install-plugin)
* [`acai plugins link PATH`](#acai-plugins-link-path)
* [`acai plugins remove [PLUGIN]`](#acai-plugins-remove-plugin)
* [`acai plugins reset`](#acai-plugins-reset)
* [`acai plugins uninstall [PLUGIN]`](#acai-plugins-uninstall-plugin)
* [`acai plugins unlink [PLUGIN]`](#acai-plugins-unlink-plugin)
* [`acai plugins update`](#acai-plugins-update)

## `acai hello PERSON`

Say hello

```
USAGE
  $ acai hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ acai hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/artificialcitizens/acai-cli/blob/v0.0.0/src/commands/hello/index.ts)_

## `acai hello world`

Say hello world

```
USAGE
  $ acai hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ acai hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/artificialcitizens/acai-cli/blob/v0.0.0/src/commands/hello/world.ts)_

## `acai help [COMMAND]`

Display help for acai.

```
USAGE
  $ acai help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for acai.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.1.0/src/commands/help.ts)_

## `acai plugins`

List installed plugins.

```
USAGE
  $ acai plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ acai plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.2.2/src/commands/plugins/index.ts)_

## `acai plugins add PLUGIN`

Installs a plugin into acai.

```
USAGE
  $ acai plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into acai.

  Uses bundled npm executable to install plugins into /Users/joshua/.local/share/acai

  Installation of a user-installed plugin will override a core plugin.

  Use the ACAI_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the ACAI_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ acai plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ acai plugins add myplugin

  Install a plugin from a github url.

    $ acai plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ acai plugins add someuser/someplugin
```

## `acai plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ acai plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ acai plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.2.2/src/commands/plugins/inspect.ts)_

## `acai plugins install PLUGIN`

Installs a plugin into acai.

```
USAGE
  $ acai plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into acai.

  Uses bundled npm executable to install plugins into /Users/joshua/.local/share/acai

  Installation of a user-installed plugin will override a core plugin.

  Use the ACAI_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the ACAI_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ acai plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ acai plugins install myplugin

  Install a plugin from a github url.

    $ acai plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ acai plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.2.2/src/commands/plugins/install.ts)_

## `acai plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ acai plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ acai plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.2.2/src/commands/plugins/link.ts)_

## `acai plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ acai plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ acai plugins unlink
  $ acai plugins remove

EXAMPLES
  $ acai plugins remove myplugin
```

## `acai plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ acai plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.2.2/src/commands/plugins/reset.ts)_

## `acai plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ acai plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ acai plugins unlink
  $ acai plugins remove

EXAMPLES
  $ acai plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.2.2/src/commands/plugins/uninstall.ts)_

## `acai plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ acai plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ acai plugins unlink
  $ acai plugins remove

EXAMPLES
  $ acai plugins unlink myplugin
```

## `acai plugins update`

Update installed plugins.

```
USAGE
  $ acai plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.2.2/src/commands/plugins/update.ts)_
<!-- commandsstop -->
