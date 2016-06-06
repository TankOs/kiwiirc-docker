# KiwiIRC Docker

This project contains a Dockerfile and startup script for building an running a
KiwiIRC instance.

## Running

Grab the KiwiIRC configuration example from
[https://github.com/prawnsalad/KiwiIRC/blob/master/config.example.js](here) and
adjust it to your needs. Save it as _config.js_.

Now run:

```
docker run -d -p 7778:7778 -v $(pwd)/config.js:/app/config.js boxbox/kiwiirc
```

**Important:** Don't leave out the `$(pwd)` part, otherwise Docker won't mount
the file, but tries to mount a directory.

The instance is now running on port 7778, [http://localhost:7778/](ready to be
used!)

## Bugs

If you encounter bugs related to the whole Docker process, report them at the
[https://github.com/TankOs/kiwiirc-docker/issues](project's issue tracker).

Problems related to KiwiIRC have to be reported at the
[https://github.com/prawnsalad/KiwiIRC](original project page).

## Contact

Stefan "TankBo" Schindler, docker-kiwiirc@boxbox.org
