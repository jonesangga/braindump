# Get and Change Default Browser

02-04-25

When I run `mdbook serve --open` it always open in brave browser.
I want to change to firefox. I found [this](https://thelinuxcode.com/open-default-browser-command-line-linux/) tutorial.

Get the default browser.

```
$ xdg-settings get default-web-browser
brave-browser.desktop
```

Change to firefox.

```
$ xdg-settings set default-web-browser firefox.desktop
```
