# ghRepo

> A script to init a repository on Github from the command line.

![][license]


## Install

Install it to `/usr/local/bin`, or in another location. Just make sure it's added to PATH.

	sudo install -v -m755 -o0 -g0 ghRepo /usr/local/bin


## Preparations
To be able to use the script you'll need to set up an “access token”. You can go and create one at Github [here][token_url]:

![''][ghToken]

_Check the **repo** or **puplic_repo**._


## Usage

	$ ghRepo

Or copy the 2 functions and put in your `~/.bash_git` _(or `~/.bashrc` etc)_.

**Example output**

```bash
$ cd /path/to/fooBar
$ git init && git add . && git commit -m "Initial commit"
```
```bash
$ ghRepo
»» Repo name (leave empty for 'fooBar'):
»» Add a short description: This is my new fooBar script.

:: Your Github username is missing in your config file(s)
»» Add this to global config (Y/n)?
»» Enter your Github username: YOUR_USER_NAME

:: Your Github token is missing in your config file(s)

    # To generate an access token, visit: <https://github.com/settings/tokens>
    # Token description: ghRepo

»» Add this to global config (Y/n)?
»» Enter your Github token: ACCESS_TOKEN

»» Creating Github repository: MyScript
origin	git@github.com:YOUR_USER_NAME/fooBar.git (fetch)
origin	git@github.com:YOUR_USER_NAME/fooBar.git (push)
:: Done

»» Pushing code to Github
:: Done

-----

    [!] You should branch off to 'devel', and work from there...

    $ git checkout -b devel

```


The script adds your username and token on first run, but you can set them manually of course:

```bash
git config --global github.username YOUR_USER_NAME
git config --global github.token ACCESS_TOKEN
```

When your Github _username_ and _token_ are already in `.gitconfig`:

```bash
$ ghRepo
»» Repo name (leave empty for 'fooBar'):
»» Add a short description: This is my new fooBar script

»» Creating Github repository: MyScript
origin	git@github.com:YOUR_USER_NAME/fooBar.git (fetch)
origin	git@github.com:YOUR_USER_NAME/fooBar.git (push)
:: Done

»» Pushing code to Github
:: Done

-----

    [!] You should branch off to 'devel', and work from there...

    $ git checkout -b devel

```


## Misc

The script was made and inspired from these pages/posts...

-	https://www.viget.com/articles/create-a-github-repo-from-the-command-line
-	http://stackoverflow.com/questions/2423777/is-it-possible-to-create-a-remote-repo-on-github-from-the-cli-without-opening-br#7563830
-	https://developer.github.com/v3/repos/#create


## Contributing

1. Fork it (<https://github.com/iEFdev/ghRepo/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

<!-- Markdown link & img dfn's -->
[license]: https://img.shields.io/badge/License-0BSD-789.svg?style=plastic "BSD Zero Clause License (SPDX: 0BSD)"
[token_url]: https://github.com/settings/tokens
[ghToken]: https://raw.githubusercontent.com/iEFdev/ghRepo/master/gh_access_token.png