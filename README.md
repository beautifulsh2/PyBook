# PyBook - Advanced Terminal Python Notebook  

## Overview  

PyBook is a sophisticated terminal-based interactive Python notebook designed for developers who prefer working in the command line. It combines the power of a traditional Python REPL with advanced features like code execution tracking, virtual environment management, code formatting, linting, and performance profiling.  

## Key Features  

- **Interactive Code Execution**: Execute Python code in cells and view output immediately  
- **Virtual Environment Management**: Create and activate Python virtual environments  
- **Code Quality Tools**: Built-in code formatting (autopep8) and linting  
- **Performance Profiling**: Profile code execution with cProfile integration  
- **File Management**: Create, list, and delete files directly from the interface  
- **Shell Integration**: Run system shell commands without leaving PyBook  
- **Session Persistence**: Save all code and outputs to a file for later review  
- **Rich Terminal UI**: Beautiful syntax highlighting and formatted output using Rich  

## Installation  

To install PyBook, run the following command:  

```bash  
wget https://raw.githubusercontent.com/beautifulsh2/PyBook/refs/heads/main/src/pybook.py -O pybook.py && python3 pybook.py  
```  

### Requirements  

- Python 3.6 or higher  
- Required packages (will be installed automatically if missing):  
  - `rich`  
  - `autopep8`  

## Usage  

### Basic Commands  

```
code:<your python code>      - Append and execute Python code  
install:<package name>      - Install a Python package via pip  
env:create <env_name>       - Create a virtual environment  
env:activate <env_name>     - Activate a virtual environment  
format:<your python code>   - Format your Python code using autopep8  
lint:<your python code>     - Lint your Python code for best practices  
file:create <filename>      - Create a new file  
file:list                   - List all files in the current directory  
file:delete <filename>      - Delete a file  
shell:<command>             - Run a shell command  
profile:<your python code>  - Profile your Python code for performance  
save:file                   - Save all code and outputs in a file (notes.pybook)  
exit                        - Exit the PyBook interactive shell  
```  

### Advanced Features  

#### Code Profiling  

PyBook integrates with Python's cProfile module to provide detailed performance analysis:  

```  
profile:def test_func():  
    return sum(i*i for i in range(10000))  
```  

#### Virtual Environment Management  

Full virtual environment support with creation and activation:  

```  
env:create myenv  
env:activate myenv  
```  

#### File Operations  

Manage files directly from the interface:  

```  
file:create new_script.py  
file:list  
file:delete old_script.py  
```  

## Technical Details  

### Architecture  

PyBook is built using several key Python libraries:  

- **Rich**: For beautiful terminal formatting and syntax highlighting  
- **autopep8**: For automatic code formatting to PEP8 standards  
- **cProfile/pstats**: For code performance profiling  

### Code Structure  

The application follows a modular design with clearly defined functions for each feature:  

1. **Code Execution**: `execute_code_in_file()`  
2. **Package Management**: `install_package()`  
3. **Virtual Environments**: `create_virtualenv()`, `activate_virtualenv()`  
4. **Code Quality**: `format_code()`, `lint_code()`  
5. **File Operations**: `create_file()`, `list_files()`, `delete_file()`  
6. **Profiling**: `profile_code()`  
7. **Persistence**: `save_to_file()`  

## Best Practices  

When using PyBook:  

1. Use virtual environments for project isolation  
2. Regularly save your work with `save:file`  
3. Profile performance-critical code before optimization  
4. Format and lint code before final execution  
5. Use the built-in file operations for better workflow integration  

## License  

PyBook is released under the MIT License. See the `LICENSE` file for full details.  

## Contributing  

Contributions are welcome. Please follow standard GitHub workflow:  

1. Fork the repository  
2. Create a feature branch  
3. Submit a pull request  

## Support  

For issues or feature requests, please open an issue on the GitHub repository.
