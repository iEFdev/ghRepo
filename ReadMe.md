# ghRepo

> A script to init a repository on Github from the command line.

![''][license]

## Install

Install it to `/usr/local/bin`, or in another location. Just make sure it's added to PATH.

	sudo install -bv -m755 -o0 -g0 <file> /usr/local/bin

## Usage

	$ ghRepo

Or copy the 2 functions and put in your `~/.bash_git` _(or `~/.bashrc` etc)_.

**Example output**

```bash
$ cd /path/to/MyScript
$ ghRepo
»» Repo name (leave empty for 'MyScript'):
»» Add a short description: This is my new fooBar script.

:: Your Github username is missing in your config file(s)
»» Add this to global config (Y/n)?
»» Enter your Github username: YOUR_USER_NAME

:: Your Github token is missing in your config file(s)

    # To generate an access token, visit: <https://github.com/settings/tokens>
    # Token description: ghRepo

»» Add this to global config (Y/n)?
»» Enter your Github token: *** TOKEN ***

»» Creating Github repository: current_folder
origin	git@github.com:YOUR_USER_NAME/MyScript.git (fetch)
origin	git@github.com:YOUR_USER_NAME/MyScript.git (push)
:: Done

»» Pushing code to Github
:: Done

-----

    [!] You should branch off to 'devel', and work from there...

    $ git checkout -b devel

```

If your Github _username_ and _token_ are already in `.gitconfig`:

```bash
$ cd /path/to/MyScript
$ ghRepo
»» Repo name (leave empty for 'MyScript'):
»» Add a short description: This is my new fooBar script

»» Creating Github repository: ghRepo
origin	git@github.com:YOUR_USER_NAME/MyScript.git (fetch)
origin	git@github.com:YOUR_USER_NAME/MyScript.git (push)
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
[license]: https://img.shields.io/badge/License-WTFPL-778899.svg?style=plastic
