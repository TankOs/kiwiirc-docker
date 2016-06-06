# KiwiIRC Docker

This project contains a Dockerfile and startup script for building and running
a KiwiIRC instance.

## Running

Grab the KiwiIRC configuration example from
[here](https://github.com/prawnsalad/KiwiIRC/blob/master/config.example.js) and
adjust it to your needs. Save it as _config.js_.

Now run:

```
docker run -d -p 7778:7778 -v $(pwd)/config.js:/app/config.js boxbox/kiwiirc
```

**Important:** Don't leave out the `$(pwd)` part, otherwise Docker won't mount
the file, but tries to mount a directory.

The instance is now running on port 7778,
[ready to be used!](http://localhost:7778/)

## Building

Clone KiwiIRC's source code:

```
git submodule update --init
```

Build image:

```
docker build -t kiwiirc .
```

## Bugs

If you encounter bugs related to the whole Docker process, report them at the
[project's issue tracker](https://github.com/TankOs/kiwiirc-docker/issues).

Problems related to KiwiIRC have to be reported at the
[original project page](https://github.com/prawnsalad/KiwiIRC).

## Contact

Stefan "TankBo" Schindler, _docker-kiwiirc@boxbox.org_
