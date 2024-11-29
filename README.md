# Openstreetmap viewer

This is just some mucking about by me attempting to do something I find useful. The base is (largely) from [here](https://docs.gtk.org/gtk3/getting_started.html) .

So, nothing much.

To compile this "project" use the following:

	 gcc `pkg-config --cflags gtk+-3.0` `pkg-config --cflags webkit2gtk-4.0` o openstreetmapviewer openstreetmapviewer.c `pkg-config --libs gtk+-3.0` `pkg-config --libs webkit2gtk-4.0`

Possibly followed by:

	strip --strip-all openstreetmapviewer

I have included a icon (It is probably copyrighted by I have no idea where I got it, so [YMMV](https://www.jejik.nl/jargon/html/Y/YMMV.html) .

Also included is a .desktop file that I made and has no copyright because it holds no original ideas.

