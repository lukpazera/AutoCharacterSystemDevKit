# Auto Character System Dev Kit

This repository contains a basic development toolkit for working with ACS3.

Download and install this as any other MODO kit.

When installed the kit adds its toolbar to the top MODO toolbar, on its right side.

### Debug
- **Log To File** enables logging ACS3 output to a file. The log file is in ACS3 Temp folder which is inside main ACS3 folder.
- **Clear Log** provides quick way to clear all output from the Event Log.
- **Log Entries to 512** allows for 512 lines to be visible in the Event Log window before the oldest ones get cleared (default value is much lower).
- **Log Entires to 2048** allows for 2048 lines of output in the Event Log.

### Dev Utils
- **Item Graph Links** lists all input and output graph links for a selected item. Useful when working out how MODO is using graphs to link items.
- **Item RS Graph Links** lists all input and output graph links that ACS3 (rigging system) set up on a selected item. Useful for ACS3 graph links debugging.
- **Clean Pyc Files** clears all .pyc files for ACS3 source. Useful for forcing .pyc recompilation, especially if you remove some .py source files.
- **Codebase Stats** is a fun little command that counts ACS3 codebase lines. It's not going to work out of the box though, you have to edit *CmdCountCodebaseLines* command source in *rs_cmd_dev.py* and replace *REPO_PATH* with the actual local path to ACS3 repo on your drive.

### Build
This is probably the most important section as it contains buttons to build all the rig assets and sample scenes that come with ACS3.
These assets have to be rebuilt each time one of modules is updated.
Most of the scenes can't be build with a single button click and are split into 2 or 3 actions. This is because making one big macro for these scenes would result in MODO crashing on the way.
Splitting the build process into more parts avoids that issue.
