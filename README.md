# This plugin is no longer maintained. Please use the [built-in plugin](https://github.com/albertlauncher/python/tree/master/jetbrains_projects) instead.

# Jetbrains-albert-plugin

This is a plugin for the albert launcher(https://albertlauncher.github.io/) which lists and lets you start projects of Jetbrains IDEs such as IntelliJ IDEA, PyCharm, GoLand, etc.

I made this project to maintain this plugin, which was originally part of the albert community plugins. The plugin itself(the python file(s)) is licensed under the GPLv3 license.

DISCLAIMER: I have no affiliation with JetBrains s.r.o. The included fallback logo `jetbrains.svg` is not my property, I am using it under the terms specified [here](https://www.jetbrains.com/company/useterms.html).

## How to install:

If you are using git, you can use the following command which will clone the repository into the right directory (respecting the XDG standard).

```
git clone https://github.com/mqus/jetbrains-albert-plugin.git ${XDG_DATA_HOME:-$HOME/.local/share}/albert/python/plugins/jetbrains-projects
```

If you don't have git, you can simply download a zip archive, extract it and move the folder containing `__init__.py` into the `.local/share/albert/python/plugins` directory in your home directory, while creating any folders that don't exist yet.

After that, you should have the following structure:
```
[...]
'- python
    '- plugins
        '- jetbrains-projects
            '- __init__.py
            '- jetbrains.svg
            '- README.md
```

Now, open your albert settings and go to Extensions and then Python. You can then activate the plugin there. You might have to restart albert if it does not show up there at first.

## How to use:

Type `jb ` in the prompt, followed by your search term. Albert should show you a list of matching projects, scraped from your "recently edited" list of your Jetbrains IDEs. It tries to match the path of your project directory (not e.g. any files or contents).

## Creating the project launcher:

For this plugin to find the editors, you need to create a command line launcher for them. This is done by opening the IDE (for example PyCharm) and then going to `Tools -> Create Command-line Launcher...`. This will create a launcher (for example, `charm`) that this plugin will be able to find.

## Contributors:

- Thomas Queste (@tomsquest)
- @iyzana
- @Sharsie
- @dsager
