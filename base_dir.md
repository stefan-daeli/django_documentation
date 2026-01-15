### BASE_DIR
---
How can we understand what BASE_DIR actually is?
Simply put, BASE_DIR is the absolute path that determines the main directory of a Django project. But where is it defined?  How can it be defined?
- It is defined in this section.
```
BASE_DIR = Path(__file__).resolve().parent.parent
```
- Definition of each function
  - The ```__file__``` variable is used to obtain the location of the file where BASE_DIR is executed. Since ```__file__``` is a string, the Path() function is used to convert it into a path object.
  ```
  Path(__file__)
  ```
  - The .resolve() function converts ```Path(__file__)``` into an absolute path (cleared of ‘.’ and ‘..’).
  - ```.parent``` takes the parent directory from the file. For example:
    ```
    project/core/settings.py
    ```
    then with ```.parent``` :
    ```
    project/core/
    ```
    Because ```.parent.parent``` (twice), then:
    ```
    project/
    ```
- The result is BASE_DIR = project/ 
