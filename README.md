# A sample Python project template

![Python Logo](https://www.python.org/static/community_logos/python-logo.png "Sample inline image")

A sample project that exists as an aid to the [Python Packaging User
Guide][packaging guide]'s [Tutorial on Packaging and Distributing
Projects][distribution tutorial].

This is the updated clone of original [sampleproject](https://github.com/pypa/sampleproject) template

### Clone the Course Repository
To clone the repository, follow this  [guide](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository).

**Important**: Please do not fork the repository.

The course repository is [here](https://github.com/Mexmath-Foundation/python-project-template).
You can either use Intellij IDE or do it manually.
For manually cloning create a new folder called `python-project-template`, move to the folder and run
````shell
git clone https://github.com/Mexmath-Foundation/python-project-template.git
````
in the commandline

### Verify the cloned repository
#### Check the remote
To check the remote repositories run the following command
```shell
git remote -v
```
in the commandline, the output should be
```shell
origin https://github.com/Mexmath-Foundation/python-project-template.git (fetch)
origin https://github.com/Mexmath-Foundation/python-project-template.git (push)
```
#### Check the branches
To check the branches run the following command
```shell
git branch
```
in the commandline, the output should be
```shell
* main
```

### Secure the original repository
Students **not allowed** to push the changes to the original course repository.
To prevent accidental pushes, it is necessary to detach the original repository from your private repository.
To do this, rename the `origin` and disable `push` to the original course repository.

#### Rename origin
To rename the origin run the following command
```shell
git remote rename origin course
```
in the commandline.

Run `git remote -v` in the commandline, the output should be
```shell
course https://github.com/Mexmath-Foundation/python-project-template.git (fetch)
course https://github.com/Mexmath-Foundation/python-project-template.git (push)
```
#### Disable pushes
To prevent pushing to the course repository replace push url by any non-existent url, i.e. DISABLED run the following command
```shell
git remote set-url --push course DISABLED
```
in the commandline.

Run `git remote -v` in the commandline, the output should be
```shell
course https://github.com/Mexmath-Foundation/python-project-template.git (fetch)
course DISABLED (push)
```

### Link the local repository to your private repository
To link the local repository to your private GitHub repository add new `origin`.

#### Open the newly created repository
Open your new GitHub repository web page and follow the instructions in `…or push an existing repository from the command line` section.
There should be a list of commands:
```shell
git remote add origin <your private repository>
git branch -M main
git push -u origin main
```
Run each command one-by-one in the commandline.

Execute `git remote -v` in the commandline, the output should be
```shell
course https://github.com/Mexmath-Foundation/python-project-template.git (fetch)
course DISABLED (push)
origin https://github.com/<your github account>/python-project-template.git  (fetch)
origin https://github.com/<your github account>/python-project-template.git (push)
```

### Create virtual environment

#### Create a new virtual environment

**Unix/macOS**
```shell
python -m venv .venv
```

**Windows**
```shell
py -m venv .venv
```

#### Activate a virtual environment

**Unix/macOS**
```shell
source .venv/bin/activate
```

**Windows**
```shell
.venv\Scripts\activate
```

* [venv — Creation of virtual environments](https://docs.python.org/3/library/venv.html)
* [Install packages in a virtual environment using pip and venv](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/)

### Pip installation

#### Installation

**Unix/macOS**
```shell
python -m ensurepip --upgrade
```

**Windows**
```shell
py -m ensurepip --upgrade
```

#### Upgrading

**Unix/macOS**
```shell
python3 -m pip install --upgrade pip
```

**Windows**
```shell
py -m pip install --upgrade pip
```

* [Pip Installation](https://pip.pypa.io/en/stable/installation/)

### check-manifest

```shell
pip install check-manifest

check-manifest -u -v
```

* [check-manifest](https://pypi.org/project/check-manifest/)

## Nox

### Install Nox
```shell
python3 -m pip install --upgrade nox
```

### Run tests
```shell
python3 -m nox -s tests-3.11
```

### Run lint

In case of failed execution check if `.venv,.idea,.github` etc. added to `noxfile.py` lint section

* [Nox](https://nox.thea.codes/en/stable/)


### Description

This project does not aim to cover best practices for Python project
development as a whole. For example, it does not provide guidance or tool
recommendations for version control, documentation, or testing.

[The source for this project is available here][src].

The metadata for a Python project is defined in the `pyproject.toml` file,
an example of which is included in this project. You should edit this file
accordingly to adapt this sample project to your needs.

----

This is the README file for the project.

The file should use UTF-8 encoding and can be written using
[reStructuredText][rst] or [markdown][md use] with the appropriate [key set][md
use]. It will be used to generate the project webpage on PyPI and will be
displayed as the project homepage on common code-hosting services, and should be
written for that purpose.

Typical contents for this file would include an overview of the project, basic
usage examples, etc. Generally, including the project changelog in here is not a
good idea, although a simple “What's New” section for the most recent version
may be appropriate.

[packaging guide]: https://packaging.python.org
[distribution tutorial]: https://packaging.python.org/tutorials/packaging-projects/
[src]: https://github.com/pypa/sampleproject
[rst]: http://docutils.sourceforge.net/rst.html
[md]: https://tools.ietf.org/html/rfc7764#section-3.5 "CommonMark variant"
[md use]: https://packaging.python.org/specifications/core-metadata/#description-content-type-optional
