# aliases
A simple pure bash alias manager.

This script creates aliases using a simple file structure system.

Each alias is structured like so:
```
-[alias_name]/
|--command
|--help
|--tags
|--sudo
```
Where the folder `[alias_name]` is the name of the alias.
`command` stores the actual command executed by the alias.

`help` stores a help message.

`tags` stores searchable tags for each alias.

`sudo` is an optional file, which when present shows a little message on the help screen of an alias to indicate it needs to be run with sudo

The script ideally should be on your `$PATH`, and then `source`d after that.

### Usage
```
Usage: aliases [command] | <args>
Do not use arguments and subcommands at the same time, it won't work!

Subcommands:
  create [name] [command]: Creates a new alias with 'name', that executes 'command'
  sethelp [name]         : Opens up the help file for the alias 'name' in nano
  settags [name]         : Opens up the tags file for the alias 'name' in nano
  togglesudo [name]      : Toggles whether or not the alias 'name' is shown as needing sudo permissions when aliases -a 'name' is called

Arguments:
    -h/--help         : Shows this help message
    -l/--list         : Shows all aliases registered by this script
    -a/--alias [alias]: Shows the help message for 'alias'
    -t/--tag [search] : Shows all aliases with tags like 'search'

```
