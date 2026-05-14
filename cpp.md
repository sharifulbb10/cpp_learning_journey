### how to set up cpp environment?
in terminal:
```bash
sudo apt update
sudo apt install build-essential gdb cmake
# verify installation
g++ --version
```
In sublime text, add terminus package. Go to Tools->Build System->New Build System, type and save it as Terminus_Cpp.sublime-build:
```json
{
    "target": "terminus_exec",
    "cancel": "terminus_cancel_build",
    "shell_cmd": "g++ \"$file\" -o \"${file_path}/${file_base_name}\" && \"${file_path}/${file_base_name}\"",
    "working_dir": "$file_path",
    "selector": "source.c++"
}
```
With Ctrl+Shift+B pressed, select Terminal_Cpp.sublime-build. It will mainly help while accepting user-input.

