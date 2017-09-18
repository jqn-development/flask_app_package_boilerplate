# Flask package boilerplate

## Installation - Mac OSX

This README assumes you are using a Mac and that you are comfortable using the Terminal and vi. The `$` indicates the command should be run in a Terminal window.

### virtualenv

virtualev enables multiple side-by-side installations of Python so you can have other projects besides this Flask app.

`$ pip install virtualenv`

### virtualenvwrapper

virtualenvwrapper is a set of extensions for creating and deleting virtual environments to make it easier to manage your development workflow and prevent dependencies conflicts.

`$ pip install virtualenvwrapper`

`$ cd`

`$ mkdir .virtualenvs`

Add the virtualenvwrapper path to your bash profile. If you don't have a .bash_profile create one `$ touch ~/.bash_profile` and run `$ source ~/.bash_profile` to have the terminal find it.

`$ vi .bash_profile`

`$ source /usr/local/bin/virtualenvwrapper.sh`

Create your environment

`$ mkvirtualenv flask_app`

`$ mdkir flask_app`

`$ cd flask_app`

workon, initializes the environment

`$ workon flask_app`

deactivate, deativates the environment

`$ deactivate flask_app`

Clone the app from git

`$ git clone https://github.com/jqn/flask_app_package_boilerplate.git . `

Install dependencies

`$ pip install -r requirements.txt`

Run the application

`$ export FLASK_APP=flask_app`

To enable debug mode

`$ export FLASK_DEBUG=1`

`$ flask run`

### Quick Tips

The previous command launches a simple built in server for local development. Head over to `http://127.0.0.1:5000/` where the app is running.

To allow access from other networks run `$ flask run --host=0.0.0.0` this tells the OS to listen on all public IPs.

To add your dependencies to the requirements.txt file run

`$ touch requirements.txt`

`$ pip freeze -r requirements.txt`

To save you some typing when launching the server and to manage your db easier add the following to postactivate.

`$ vi /Users/your-user/.virtualenvs/flask_app/bin/postactivate`

```
export FLASK_APP=flask_app
export FLASK_ DEBUG=1
```
