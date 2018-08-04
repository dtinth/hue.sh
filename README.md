# hue.sh

Shell scripts to control my Philips Hue (using local HTTP API).

## Prerequisites

- [HTTPie](https://httpie.org/)

- Obtain a Hue IP address and username, see this guide on how to obtain a
  username:
  [Commanding your Philips Hue lights with PowerShell](https://blog.kloud.com.au/2018/03/19/commanding-your-philips-hue-lights-with-powershell/)

## Set up

1.  Clone repo

    ```sh-session
    $ git clone git@github.com:dtinth/hue.sh.git ~/Projects/hue.sh
    ```

2.  Create file `~/.huerc`

    ```
    HUE_API=http://192.168.1.3
    HUE_USERNAME=u9lJqgXjhOktRGNOlvujEKXFImE9CZTKybrvfW52
    ```

3.  Set up PATH to include `~/Projects/hue.sh/bin`

## Raw CLI (`hue`)

```sh-session
$ hue get lights
HTTP/1.1 200 OK
(JSON output)

$ hue put lights/1/state hue:=6510 sat:=48 bri:=254
HTTP/1.1 200 OK
(JSON output)
```

## Light presets (`lights`)

```sh-session
$ lights status
$ lights on
$ lights off
$ lights normal
$ lights dimmed
$ lights white
$ lights colorloop
$ lights nocolorloop
```
