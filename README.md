# Spotify-Now
A bash script that gives you information on the current Spotify song.

## Usage

Valid keywords:

* %album
* %artist
* %track

If you want a custom message when Spotify isn't running:
`-m "your custom message"`

##### Example:

```
$ spotify-now %artist - %title
Kendrick Lamar - Alright
```

```
$ spotify-now -m "your custom message" Album: %album
Album: To Pimp A Butterfly
```

And if Spotify is closed:

```
$ spotify-now -m "stopped" %title
stopped
```

![scrot](https://raw.githubusercontent.com/getmicah/spotify-now/master/scrot.png)

## How?
This works by send a dbus message to the Spotify player which then returns information on the song currently playing. This data is then parsed and echoed.
