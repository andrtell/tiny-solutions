# Firefox ugly fonts

Try this to fix font rendering.

```
$ sudo ln -s /usr/share/fontconfig/conf.avail/70-no-bitmaps.conf /etc/fonts/conf.d/
$ pack install google-fonts-ttf
$ pack install freefont-ttf
```
