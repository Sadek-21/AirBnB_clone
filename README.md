# 0x00. AirBnB clone - The Console

## 0x00.Table of Contents

* [0x01 Introduction](#0x01-Introduction)
* [0x02 Environment](#0x02-Environment)
* [0x03 Installation](#0x03-Installation)
* [0x04 Testing](#0x04-Testing)
* [0x05 Usage](#0x05-Usage)
* [0x06 Authors](#0x06-Authors)

## 0x01 Introduction

This is a team project aimed at creating a clone of [AirBnB](https://www.airbnb.com/). The console serves as a command interpreter to manage object abstractions and their storage.

For a deeper understanding of the project's background, refer to the [Wiki](https://github.com/ralexrivero/AirBnB_clone/wiki).

The console executes the following tasks:
- Creating a new object
- Retrieving an object from a file
- Performing operations on objects
- Destroying an object

### Storage

All classes are managed by the `Storage` engine within the `FileStorage` class.

## 0x02 Environment

- [Ubuntu](https://ubuntu.com/)
- [GNU Bash](https://www.gnu.org/software/bash/)
- [Python](https://www.python.org)
- [Vim](https://www.vim.org/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Git](https://git-scm.com/)
- [GitHub](https://github.com)

### Style Guidelines

- [pycodestyle (version 2.7.*)](https://pypi.org/project/pycodestyle/)
- [PEP8](https://pep8.org/)

Development and testing were conducted on Ubuntu 20.04 LTS, using Python 3.8.3. Editors utilized were VIM 8.1.2269, VSCode 1.6.1, and Atom 1.58.0. Version control was managed through Git 2.25.1.

## 0x03 Installation

```bash
git clone https://github.com/izimartin/AirBnB_clone.git
```

Navigate to the `AirBnB` directory and execute:

```bash
./console.py
```

### Execution

In interactive mode:

```bash
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb)
(hbnb)
(hbnb) quit
$
```

In Non-interactive mode:

```bash
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```

## 0x04 Testing

All tests are defined in the `tests` folder.

### Documentation

- Modules:

```python
python3 -c 'print(__import__("my_module").__doc__)'
```

- Classes:

```python
python3 -c 'print(__import__("my_module").MyClass.__doc__)'
```

- Functions (inside and outside a class):

```python
python3 -c 'print(__import__("my_module").my_function.__doc__)'
```

and

```python
python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'
```

### Python Unit Tests

- `unittest` module
- File extension: `.py`
- Files and folders start with `test_`
- Organization: for `models/base.py`, unit tests in: `tests/test_models/test_base.py`
- Execution command: `python3 -m unittest discover tests`
- or: `python3 -m unittest tests/test_models/test_base.py`

### Running Tests

#### Interactive Mode

```bash
echo "python3 -m unittest discover tests" | bash
```

#### Non-Interactive Mode

To run the tests in non-interactive mode and discover all the tests, you can use the command:

```bash
python3 -m unittest discover tests
```

## 0x05 Usage

- Start the console in interactive mode:

```bash
$ ./console.py
(hbnb)
```

- Use help to see the available commands:

```bash
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update

(hbnb)
```

- Quit the console:

```bash
(hbnb) quit
$
```

### Commands

The commands are displayed in the following format: *Command / Usage / Example with Output*

- **Create**

Creates a new instance of a given class. The class' ID is printed, and the instance is saved to the `file.json`.

```bash
create <class>
```

```bash
(hbnb) create BaseModel
6cfb47c4-a434-4da7-ac03-2122624c3762
(hbnb)
```

- **Show**

```bash
show <class> <id>
```

```bash
(hbnb) show BaseModel 6cfb47c4-a434-4da7-ac03-2122624c3762
[BaseModel] (a) [BaseModel] (6cfb47c4-a434-4da7-ac03-2122624c3762) {'id': '6cfb47c4-a434-4da7-ac03-2122624c3762', 'created_at': datetime.datetime(2021, 11, 14, 3, 28, 45, 571360), 'updated_at': datetime.datetime(2021, 11, 14, 3, 28, 45, 571389)}
(hbnb)
```

- **Destroy**

Deletes an instance of a given class with a given ID.
Update the `file.json`.

```bash
(hbnb) create User
0c98d2b8-7ffa-42b7-8009-d9d54b69a472
(hbnb) destroy User 0c98d2b8-7ffa-42b7-8009-d9d54b69a472
(hbnb) show User 0c98d2b8-7ffa-42b7-8009-d9d54b69a472
** no instance found **
(hbnb)
```

- **All**

Prints all string representations of all instances of a given class.
If no class is passed, all classes are printed.

```bash
(hbnb) create BaseModel
e45ddda9-eb80-4858-99a9-226d4f08a629
(hbnb) all BaseModel
["[BaseModel] (4c8f7ebc-257f-4ed1-b26b-e7aace459897) [BaseModel] (4c8f7ebc-257f-4ed1-b26b-e7aace459897) {'id': '4c8f7ebc-257f




## Authors

<details>
    <summary>Mohmaed Sadek</summary>
    <ul>
    <li><a href="https://github.com/Sadek-21">Github</a></li>
    </ul>
</details>
<details>
    <summary>Lamiae Grefi</summary>
    <ul>
    <li><a href="https://github.com/">Github</a></li>
    </ul>


</details>
