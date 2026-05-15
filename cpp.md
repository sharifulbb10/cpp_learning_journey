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

### first c++ script
```cpp
#include <iostream>

int main() {
	cout<<"hello world!"<<endl;
}
 ```
### type aliases
```cpp
typedef int age;
age my_age = 30;

// more cleaner
using age=int;
age my_age = 30;

// 'using' is the recommended option
```

### data types
Let's learn some common data types in c++:

```cpp
#include <iostream>
int main() {

  // integer number
  int num = 2;
  int num2 =2.36;
  std::cout << num<<'\n';
  std::cout << num2<<'\n';
  // 2
  // 2

  // float number
  double money = 1.50;
  double money2 = 5.55;
  std::cout << money<<std::endl; 
  std:: cout << money2<<std::endl;
  // 1.5
  // 5.55

  // character (single character) 
  char currency = '$';
  char singleChar = 'A';
  std::cout << currency<<std::endl;
  std::cout << singleChar<<'\n';
  // $
  // a

  // string 
  std::string name = "Shariful";
  std::string favFruit = " My favorite fruit is Banana";
  std::cout << name<<'\n';
  std::cout << favFruit<<'\n';
  // Shariful 
  // My favorite fruit is Banana;

  // boolean
  bool isStudent = true;
  bool happy = true;
  bool upset = false;
  std::cout << upset<<'\n';
  // false
}
```