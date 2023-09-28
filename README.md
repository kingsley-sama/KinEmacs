# KinEmacs
### Emacs Setup With Ease

```markdown
## How to watch a folder for change in Linux

**Overview**

Monitoring a folder for change in Linux is a useful task for a variety of purposes, such as automatically rebuilding a website when a file changes or automatically running a script when a new file is added to a folder.

There are two main ways to watch a folder for change in Linux:

* Using the `inotifywait` command
* Using the `watchman` command

**inotifywait**

The `inotifywait` command is a Linux command that can be used to monitor a file or directory for changes. When a change is detected, `inotifywait` will print a notification to the console.

To use `inotifywait` to monitor a folder for change, you can use the following command:

```
inotifywait -e modify,create,delete -r /path/to/folder


This command will monitor the folder `/path/to/folder` and all of its subdirectories for changes. It will print a notification to the console whenever a file is modified, created, or deleted in the folder or its subdirectories.

**watchman**

The `watchman` command is a cross-platform tool that can be used to monitor files and directories for changes. It is more powerful than `inotifywait` and can be used to create more complex triggers.

To use `watchman` to monitor a folder for change, you can use the following command:


watchman watch /path/to/folder


This command will start watching the folder `/path/to/folder` for changes. When a change is detected, `watchman` will trigger all of the actions that have been defined for that folder.

You can define actions for `watchman` using a configuration file. For example, you could create a configuration file that triggers a script to be run whenever a file is modified in the folder.

**Which method should I use?**

Which method you choose to use depends on your needs and preferences. If you need a simple way to monitor a folder for change, then `inotifywait` is a good option. If you need a more powerful and flexible way to monitor a folder for change, then `watchman` is a better option.

**Examples**

Here are some examples of how to use `inotifywait` and `watchman` to monitor a folder for change:

* Monitor the folder `/path/to/folder` for changes and print a notification to the console:


inotifywait -e modify,create,delete -r /path/to/folder


* Start watching the folder `/path/to/folder` for changes and trigger the script `/path/to/script.sh` whenever a file is modified:


watchman watch /path/to/folder
watchman trigger /path/to/folder --command /path/to/script.sh


**Conclusion**

Monitoring a folder for change in Linux is a useful task for a variety of purposes. By following the instructions in this README.md file, you can learn how to use `inotifywait` and `watchman` to monitor folders for changes.
