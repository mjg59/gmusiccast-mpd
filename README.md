Simple MPD client for playing Google Music on Chromecasts
=========================================================

This app does one thing: it exposes an MPD compatible interface for searching Google Music and plays songs back over Chromecasts. That's it. It is not well-written. It will not gain additional features, with the possible exception of adding support for stations. It certainly will not gain support for playing back other streaming services or playing to local speakers.

Requirements
------------

* [My fork of python-mpd-server](https://github.com/mjg59/python-mpd-server)
* [pychromecast](https://github.com/balloob/pychromecast)
* [gmusicapi](https://github.com/simon-weber/gmusicapi)

Use
---
Create a file called .gmusiccast.cfg in your home directory that looks like the following:

```
[gmusic]
device_id=1234567890abcdef
username=fakename@google.invalid
password=password

[server]
port=9999
```

device_id must be a 16 character string. If you use one that corresponds to a real Android device that you use the same account on, you will be periodically logged out of that device. username should be your Google username. If you use 2FA, password should be an app password generated [here](https://security.google.com/settings/security/apppasswords)

Connect an MPD-compatible client to the configured port and away you go.

License
-------
This app uses python-mpd-server, and as such is released under version 3 of the GNU General Public License, or (at your option) any later version.