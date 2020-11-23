## Getting started
* You can either install mkdocs from pip or from a virtual environment.
* It's highly recommended to use a virtual environment and not pip, so that the dependencies of this project won't mess with your system-wide python packages / modules.
* Personnally I am using pipenv, which you install on openSUSE distributions with: `pip3 install --user pipenv`. Then you'll need to add `~/.local/bin` to your PATH. The best method for that depends on your shell.
* Then clone this repos where you want in your home folder, `cd` to it and run `pipenv install` to build and then `pipenv shell` to run the environment. Then `cd` to `project` and run you `mkdocs` commands from there, i.e. `mkdocs build` to generate the web content and `mkdocs serve` to serve it (normally at http://127.0.0.1:8000/).
* Available commands & documentation on mkdocs: https://www.mkdocs.org/
