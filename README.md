# Flatpak ZAP

## Issues
Please open issues under: https://github.com/zaproxy/zaproxy/issues

## Usage

ZAP's Flatpak sandbox provides host filesystem access and network access by default. Most functionalities work out of the box, including proxied browser launching via Firefox.

### Launching a browser

Firefox is supported out of the box using Selenium WebDriver (geckodriver bundled). The wrapper at `/app/bin/firefox` searches for Firefox at:

- `/usr/bin/firefox` (Fedora, Debian, standard installs)
- `/snap/firefox/*/usr/lib/firefox/firefox` (Ubuntu snap)
- `/usr/lib/firefox/firefox`
- `/usr/lib64/firefox/firefox`

To open URLs in your system browser from ZAP's context menus, xdg-desktop-portal is used.

### Use host shell in the integrated terminal.

ZAP integrates with the host system. To execute commands on the host from within the sandbox:

```shell
$ flatpak-spawn --host <COMMAND>
```

or

```shell
$ host-spawn <COMMAND>
```

### Run ZAP from host terminal

```shell
$ alias zap="flatpak run org.zaproxy.ZAP"
```

Then:

```shell
$ zap
```

## Related Documentation

- https://www.zaproxy.org/docs/
- https://www.zaproxy.org/faq/
