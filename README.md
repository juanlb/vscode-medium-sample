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
# First run
```
bundle install
rake db:create db:migrate db:seed
```