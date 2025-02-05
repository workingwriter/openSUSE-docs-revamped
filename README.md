## Getting started
* You can either install mkdocs from pip or from a virtual environment.
* It's highly recommended to use a virtual environment and not pip, so that the dependencies of this project won't mess with your system-wide python packages / modules. You still need to use pip to install pipenv though ;).
* Personnally I am using pipenv, which you install on openSUSE distributions with: `pip3 install --user pipenv`. Then you'll need to add `~/.local/bin` to your PATH. The best method for that depends on your shell:
    * in Bash add "PATH=$PATH:/home/your-user-name/.local/bin" to `.bashrc`
    * in ZSH add "export PATH=$PATH/home/your-user-name/.local/bin" to `.zshrc`

* Then 
    1. clone this repo where you want in your home folder
    2. `cd` to it and run `pipenv install` to install the dependencies, and then `pipenv shell` to run the environment. 
    3. finally `cd` to `project` and run you `mkdocs` commands from there, i.e. `mkdocs build` to generate the web content and `mkdocs serve` to serve it (by default at http://127.0.0.1:8000/). The built-in dev-server allows you to preview your documentation as you're writing it. It will even auto-reload and refresh your browser whenever you save your changes.
* Available commands & documentation on mkdocs: https://www.mkdocs.org/

## Repo structure
```
...
Pipfile     # dependencies listed in pipenv format
requirements.txt    # dependencies listed in pip format (added for compatibility purposes)
project/
    docs/   # contents files that mkdocs injects when building the website
    site/   # the source files of the generated website after each 'mkdocs build' command.
    ...
...
```

## Branches & rules
* The default branch -- the working branch -- is not `main` or `master` but `dev`. That's the branch where day-to-day work should happen.
* `master` enforces the same basic rules, bear them in mind if something is not working as expected:
    * Require pull request reviews before merging
    * Require status checks to pass before merging
    * Require branches to be up to date before merging
