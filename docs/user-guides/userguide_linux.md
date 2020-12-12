# Usage on Linux/Unix

## Mumble (Client)

### Installation

The best option to install Mumble is through your distribution's package repository.
Just search for `Mumble` in your package manager and install it.

If Mumble is not available or outdated in your distribution's repos, you can take a look at our [website's downloads page](https://www.mumble.info/downloads/#linux).
There you will find multiple alternatives, including official Third-Party-Repos, Snap- and Flatpak-Packages.

More information can be found in our [wiki](https://wiki.mumble.info/wiki/Installing_Mumble#Linux).

### Start

If you have installed Mumble through your distributon's package repository, you should be able to find Mumble in your start menu. No additional steps are necessary.

Otherwise go into the folder and start Mumble manually.

## Mumble Server (Murmur)

### Installation

The best option to install the Mumble Server (Murmur) is through your distribution's package repository.
Just search for `Mumble Server` or `Murmur` in your package manager and install it.

Alternatively you can also find a **Static Linux Server** package on our [website's downloads page](https://www.mumble.info/downloads/#manual-download).

### Configuration

Take a look at the [Server Configuration Guide](server_config_guide.md).

### Start

Two methods:

* Auto-Start
* Manual Start

#### Auto-Start

On many distributions the Mumble Server is started automatically on system boot.

You can also disable this and start the Server manually.

#### Manual Start

The Mumble Server should be run from the command line, so start a shell (command prompt) and go to wherever you installed Mumble. Run murmur with:

```
murmurd [-supw <password>] [-ini <inifile>] [-fg] [v]

-supw   Set a new password for the user SuperUser, which is hardcoded to
        bypass ACLs. Keep this password safe. Until you set a password,
        the SuperUser is disabled. If you use this option, murmur will
        set the password in the database and then exit.

-ini    Use an inifile other than murmur.ini, use this to run several instances
        of murmur from the same directory. Make sure each instance is using
        a separate database.

-fg     Run in the foreground, logging to standard output.

-v      More verbose logging.
```