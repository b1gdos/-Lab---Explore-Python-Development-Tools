# Lab - Explore Python Development Tools

This lab explores various Python development tools and practices, including Python installation, PIP, Python virtual environments, and sharing virtual environments.

## Objectives

- Launch the DEVASC VM
- Review the Python Installation
- PIP and Python Virtual Environments
- Sharing Your Virtual Environment

## Background / Scenario

This lab is designed to familiarize students with maintaining a Python development environment. It covers essential topics such as Python installation, PIP usage, Python virtual environments, and sharing virtual environments with other developers.

## Required Resources

- 1 PC with an operating system of your choice
- Virtual Box or VMWare
- DEVASC Virtual Machine

## Instructions

### Part 1: Launch the DEVASC VM

Ensure you have completed the Lab - Install the Virtual Machine Lab Environment. Launch the DEVASC VM.

### Part 2: Review the Python Installation

- Check the version of Python installed:
  ```
  devasc@labvm:~$ python3 -V
  Python 3.8.2
  ```

- View the directory for the local Python environment:
  ```
  devasc@labvm:~$ which python3
  /usr/bin/python3
  ```

### Part 3: PIP and Python Virtual Environments

- Create a Python 3 virtual environment named "devfun":
  ```
  devasc@labvm:~$ cd labs/devnet-src/python/
  devasc@labvm:~/labs/devnet-src/python$ python3 -m venv devfun
  ```

- Activate the virtual environment:
  ```
  devasc@labvm:~/labs/devnet-src/python$ source devfun/bin/activate
  (devfun) devasc@labvm:~/labs/devnet-src/python$
  ```

- Install the Python requests package:
  ```
  (devfun) devasc@labvm:~/labs/devnet-src/python$ pip3 install requests
  ```

- Deactivate the virtual environment:
  ```
  (devfun) devasc@labvm:~/labs/devnet-src/python$ deactivate
  devasc@labvm:~/labs/devnet-src/python$
  ```

### Part 4: Sharing Your Virtual Environment

- Create a requirements file:
  ```
  (devfun) devasc@labvm:~/labs/devnet-src/python$ pip3 freeze > requirements.txt
  ```

- Create and activate a new Python virtual environment named "devnew":
  ```
  devasc@labvm:~/labs/devnet-src/python$ python3 -m venv devnew
  devasc@labvm:~/labs/devnet-src/python$ source devnew/bin/activate
  ```

- Install packages from the requirements file:
  ```
  (devnew) devasc@labvm:~/labs/devnet-src/python$ pip3 install -r requirements.txt
  ```

- Deactivate the virtual environment:
  ```
  (devnew) devasc@labvm:~/labs/devnet-src/python$ deactivate
  devasc@labvm:~/labs/devnet-src/python$
  ```

This lab provides hands-on experience with Python development tools and practices, enabling students to create and manage Python virtual environments effectively.
