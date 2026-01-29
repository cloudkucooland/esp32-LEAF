Clone this module with recursive enabled since LEAF is imported as a submodule:

```git clone --recursive ... ```

This repo is a quick hack to allow including LEAF as an esp32-idf component.

Include it in your project by importing it as a submodule into the components directory:

```
mkdir -p components
cd components
git submodule add ...
``` 

Right now all this does is include LEAF as a git submodule and set compile flags to make it build cleanly via idf.py from within an idf project.

Add esp32-LEAF to your main/CMakeLists.txt in the idf_component_register

```
idf_component_register(SRCS "main.c"
                    INCLUDE_DIRS "."
                    PRIV_REQUIRES ... esp32-LEAF)
```
