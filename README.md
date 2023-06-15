# Scripting
Scripting is used to automate tasks for software applications while using an existing program.

**Libraries**

A library is a collection of modules or packages.

**Modules**

A module is a code block or functions. 

#### Seven core modules used in DevOps
```python
# system module
import sys

# Get Python version
print(sys.version)

# operating system module
import os

# Get current working directory
print(os.getcwd())

# subprocess module
import subprocess

# Runs an external file when executed
subprocess.run(["python", "hello_world.py"])

# math module
import math

pi = math.pi
pi_string = str(pi)
print("The value of pi is " + pi_string)

# random module
import random

randnum = random.randrange(1, 10)
print(randnum)

# datetime module
import datetime

today = datetime.datetime.now()
print(today)

# JSON module
import json

# JSON used for transporting data

x = {"name": "John",
     "age": 30,
     "city": "Liverpool"}

y = json.dumps(x)
print(type(x)) # -- dict
print(type(y)) # -- str
```

**os module**

os module used for interacting with the operating system.
```python
import os

os.system('echo Hello world!')

"""
make and change directories
create a directory
"""

# directory name
directory = "test_dir"

# parent directory name
parent_dir = "d:/python project/"

# Path
path = os.path.join(parent_dir, directory)

# create directory
os.mkdir(path)
```
```python
import os

# Put a new file in the new dir
filename = "testfile.txt"

# directory name
directory = "test_dir"

# parent directory name
parent_dir = "d:/python project/"

# Path
path = os.path.join(parent_dir, directory)

filepath = os.path.join(path, filename)

with open(os.path.join(path, filename), "w") as file1:
    toFile = "Contents of the file is written here"
    file1.write(toFile)

print("file " + filename + " created in " + directory + " folder")
```

**Example** 

Using **_os_** and **_subprocess_** to run a script in shell 
```python
import os
import subprocess

# Stores the file path to the current path
script_dir = os.path.dirname(__file__)
# print(script_dir)

# Stores the filepath to the script to run
script_absolute_path = os.path.join(script_dir + '/shell_script.sh')

# calls the shell file and runs it
subprocess.call(['sh', script_absolute_path])
```
```shell
#!/bin/bash

 echo "This is a shell script!"

 ls
```
