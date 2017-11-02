# Provisioning Browser Live CD

This is a debian based Live image which directly boots into a full screen browser that will visit the site specified with the provisioning_url kernel parameter.

The kernel, initrd and squashfs filesystem is booted using iPXE through HTTP (also makes use of the webbooting support included in debian live images).

In order to build this image you need the latest live build scripts at:
http://anonscm.debian.org/git/debian-live/live-build.git

The Complete Live Systems manual is available here:
https://debian-live.alioth.debian.org/live-manual/stable/manual/html/live-manual.en.html

# Build steps

```
lb clean --all
lb config
lb build
```

If all goes well you should have the necessary files under binary/live/{vmlinuz,initrd.img,filesystem.squashfs}. Ubuntu 16.04.3 LTS is known to work.

