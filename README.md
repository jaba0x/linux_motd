# Ansible Role: jaba0x Motd [![Build Status](https://travis-ci.org/lucasmaurice/ansible-role-linux-motd.svg?branch=master)]

Install a standardized welcome message on a **Debian** or a **RedHat** host.

## Role Variables

Available variables are listed below, along with default values (see defaults/main.yml):

```yaml
---
MOTD_CONTACT: admin@jaba.ge

# Name of the interfaces to read the Ip address.
MOTD_PRIVATE_INTERFACE: x
MOTD_PUBLIC_INTERFACE: x

# Welcome message accent color. Select a color here: https://misc.flogisoft.com/bash/tip_colors_and_formatting (Dont forget the `\e[38;5;` and the `m`)
MOTD_COLOR_ACCENT: \e[38;5;202m
# Welcome message and font. Select a font here: http://www.figlet.org/fontdb.cgi
MOTD_WELCOME_FONT: nancyj
MOTD_WELCOME: TELMIKO

# Users to disable default motd
users: []
```

- `MOTD_CONTACT`: The contact email address to show.

- `MOTD_PRIVATE_INTERFACE`: Network interface you want to read the private Ip address to show.

- `MOTD_PUBLIC_INTERFACE`: Network interface you want to read the public Ip address to show.

> Set the network interface to *x* or do not set it for no interface.

- `MOTD_COLOR_ACCENT`: The colors of the welcome message accents. (Select a color on the [Bash Colors List](https://misc.flogisoft.com/bash/tip_colors_and_formatting) ; **Dont forget the `\e[38;5;` and the `m`**)

- `MOTD_WELCOME_FONT`: The font of the welcome word. (Select a font on the [Figlet Website](http://www.figlet.org/fontdb.cgi))

- `MOTD_WELCOME`: The welcome word.

- `users`: Global variable containing all the users. Will disable the default motd on all listed users.


## License

[![WTFPL](http://www.wtfpl.net/wp-content/uploads/2012/12/wtfpl-badge-1.png)](https://http://www.wtfpl.net)
