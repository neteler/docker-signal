# docker-signal-desktop

Whisper Systems Signal Desktop in a container

To run this image, share the X11 socket or use any
of the other methods to run X11 Apps in Docker.

For example, you can run the image like this on Linux. With this snippet
in your `~/.bahsrc`:

```
alias x_in_docker="sudo docker run -d -u 1000:1000 --rm -e HOME \
  -e DISPLAY=unix:0 -e XAUTHORITY=/tmp/xauth \
  -v $XAUTHORITY:/tmp/xauth -v $HOME:$HOME \
  -v /etc/passwd:/etc/passwd:ro -v /etc/group:/etc/group:ro \
  -v /tmp/.X11-unix:/tmp/.X11-unix -w $HOME"
alias signal='x_in_docker neteler/signal'
```

Launch the app by simply typing `signal` on your command line.

## MacOS: Using this image

For MacOS, see https://github.com/ksylvan/docker-signal

Now, `signal` should launch the application.

# Reference

- https://signal.org/download/
