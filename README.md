This is an excerpt from gst-rtsp-server/example:
https://gitlab.freedesktop.org/gstreamer/gstreamer/-/tree/main/subprojects/gst-rtsp-server/examples

This is a test-onvif-client.c and test-onvif-server.c only project running in VS Code.
I have slightly modified the source code to run on Windows. (see git history)

Both Linux and Windows build with Meson.

~~The Windows gstreamer installer did not include rtponviftimestamp, so I used gstreamer version 1.22.0 built with cerbero.~~

The Windows gstreamer installer ver.1.22.4 contains rtponviftimestamp.
We can reproduce using this, too.

On Linux run in VS Code in this order:

・(Linux) test-onvif-server

・(Linux) test-onvif-client

On Windows run in VS Code in this order:

・(Windows) test-onvif-server

・(Windows) test-onvif-client
