# pi-ffplay
Simple app to allow playback of videos using v4l2 m2m codecs on the RPi3

Prompts the user to choose a video, then tries to play it back using
a V4L2 M2M codec. Designed to allow straightforward leverage of
the RPi3's hardware-assisted video decoding from a 64-bit userland.

If a video path is given as the (only) argument, this will be used as the
playback target, and no file chooser will be shown.

Basically, this is a trivial wrapper around `ffplay`, that tries to
select the correct codec (since, atm, `ffmpeg` will not do this
automatically).

Will become redundant once apps like `vlc` etc. start exploiting
v4l2 m2m properly.
