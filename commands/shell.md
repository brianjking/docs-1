# ee shell

Brings up a shell to run wp-cli, composer etc.

### OPTIONS

[&lt;site-name&gt;]
: Name of website to run shell on.

[\--user=&lt;user&gt;]
: Set the user to exec into shell.

[\--service=&lt;service&gt;]
: Set the service whose shell you want.
\---
default: php
\---

[\--command=&lt;command&gt;]
: Command to non-interactively run in the shell.

 ## EXAMPLES

    # Open shell for site
    $ ee shell example.com

    # Open shell with root user
    $ ee shell example.com --user=root

    # Open shell for some other service
    $ ee shell example.com --service=nginx

    # Run command non-interactively
    $ ee shell example.com --service=nginx --command='nginx -t &amp;&amp; nginx -s reload'

### GLOBAL PARAMETERS

| **Argument**    | **Description**              |
|:----------------|:-----------------------------|
| `--sites_path=<path>` | Absolute path to where all sites will be stored. |
| `--locale=<locale>` | Locale for WordPress. |
| `--le-mail=<le-mail>` | Mail-id to be used for letsencrypt. |
| `--[no-]color` | Whether to colorize the output. |
| `--debug[=<group>]` | Show all PHP errors; add verbosity to EE bootstrap. |
| `--prompt[=<assoc>]` | Prompt the user to enter values for all command arguments, or a subset specified as comma-separated values. |
| `--quiet` | Suppress informational messages. |
