# Use
## Extension
In your VS Code install the `Remote - Containers` extension.
## Env vars
Make a copy of the `.env.EXAMPLE` file:
```
cp .env.EXAMPLE .env
```
and configure your preferences.

## SHELL
To select the shell you want to use, open Command Palete (Ctrl + Shift + P) and type:
```
Terminal: Select Default Profile
```
and select the one you prefer.

## Sample app
You can test this dev environment with this repo: https://github.com/juanlb/vscode-medium-sample-app

Clone it wherever you want in your computer, and then put the path in the `MAIN_APP_PATH` variable in the `.env` file
# First run

## Install dependencies:
```
bundle install
rake db:create db:migrate db:seed
```
## Run the app:
```
rails s -b 0.0.0.0
```

Then access to `http://localhost:3000`

The default binding is `localhost`, and as the app runs inside a docker, it needs a 0.0.0.0 binding, or access from your browser to the internal docker IP.


