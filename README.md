Laptop
======
[![Build Status](https://travis-ci.org/monfresh/laptop.svg)](https://travis-ci.org/monfresh/laptop)

Laptop is a script to set up a macOS computer for web development, and to keep
it up to date.

It can be run multiple times on the same machine safely. It installs,
upgrades, or skips packages based on what is already installed on the machine.

This was formerly for a Ruby environment, but now configured for a Go and Javascript environment.

More advanced users can easily [customize](#customize-in-laptoplocal-and-brewfilelocal)
the script to install additional tools. To see an example of a more advanced
script, check out [18F/laptop](https://github.com/18F/laptop).


Install
-------

In your Terminal window, copy and paste the command below, then press `return`.

```sh
bash <(curl -s https://raw.githubusercontent.com/transcarent/laptop/master/laptop)
```

Debugging
---------

Your last Laptop run will be saved to a file called `laptop.log` in your home
folder. Read through it to see if you can debug the issue yourself. If not,
copy the entire contents of `laptop.log` into a

What it sets up
---------------
* [Go] for API development bliss
* [Homebrew] for managing operating system libraries
* [Homebrew Cask] for quickly installing Mac apps from the command line
* [Homebrew Services] so you can easily stop, start, and restart services
* [Postgres] for storing relational data
* [Zsh] as your shell (if you opt in)

It should take less than 15 minutes to install (depends on your machine and
internet connection).


Customize in `~/.laptop.local` and `~/Brewfile.local`
-----------------------------------------------------
```sh
# Go to your macOS user's root directory
cd ~

# Download the sample files to your computer
curl --remote-name https://raw.githubusercontent.com/monfresh/laptop/master/.laptop.local
curl --remote-name https://raw.githubusercontent.com/monfresh/laptop/master/Brewfile.local

# open the files in Sublime Text
subl .laptop.local
subl Brewfile.local
```

Your `~/.laptop.local` is run at the end of the `mac` script.
Put your customizations there. If you want to install additional
tools or Mac apps with Homebrew, add them to your `~/Brewfile.local`.
You can use the `.laptop.local` and `Brewfile.local` you downloaded
above to get started. It lets you install the following tools and Mac apps:


Credits
-------

This laptop script is inspired by
[thoughbot's laptop](https://github.com/thoughtbot/laptop) script.

### Public domain

thoughtbot's original work remains covered under an [MIT License](https://github.com/thoughtbot/laptop/blob/c997c4fb5a986b22d6c53214d8f219600a4561ee/LICENSE).

My work on this project is in the worldwide [public domain](LICENSE.md), as are contributions to my project. As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
