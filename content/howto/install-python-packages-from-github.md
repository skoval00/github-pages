Title: Install Python packages from Github
Date: 2016-06-25 07:24

Taken from [pip documentation](https://pip.pypa.io/en/latest/reference/pip_install/#vcs-support).

pip supports installing from Git, Mercurial, Subversion and Bazaar, and detects the type of VCS using url prefixes: "git+", "hg+", "bzr+", "svn+".

## Git

Here are the supported forms:

    [-e] git+https://github.com/MyAccount/MyProject#egg=MyProject
    [-e] git+git://git.myproject.org/MyProject#egg=MyProject
    [-e] git+ssh://git.myproject.org/MyProject#egg=MyProject
    -e git+git@git.myproject.org:MyProject#egg=MyProject

Passing branch names, a commit hash or a tag name is possible like so:

    [-e] git://git.myproject.org/MyProject.git@master#egg=MyProject
    [-e] git://git.myproject.org/MyProject.git@v1.0#egg=MyProject
    [-e] git://git.myproject.org/MyProject.git@da39a3ee5e6b4b0d3255bfef95601890afd80709#egg=MyProject

The "project name" component of the url suffix "egg=<project name>-<version>" is used by pip in its dependency logic to identify the project prior to pip downloading and analyzing the metadata. The optional "version" component of the egg name is not functionally important. It merely provides a human-readable clue as to what version is in use.


### Subdirectory install

For projects where setup.py is not in the root of project, "subdirectory" component is used. Value of "subdirectory" component should be a path starting from root of the project to where setup.py is located.

`pip install -e vcs+protocol://repo_url/#egg=pkg&subdirectory=pkg_dir`


### Editable and non-editable installs

VCS projects can be installed in editable mode (using the --editable option) or not.

* For editable installs, the clone location by default is "<venv path>/src/SomeProject" in virtual environments, and "<cwd>/src/SomeProject" for global installs. The --src option can be used to modify this location.

* For non-editable installs, the project is built locally in a temp dir and then installed normally.
