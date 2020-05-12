# RT running on Docker

This repo is part of my own experiments to run BestPractical's [Request Tracker](https://bestpractical.com) ticketing system via [Docker](https://docker.com).

## RT-Docker-Base-Debian

Build a Docker container image based on Debian Linux Stretch-Slim that supports running Request Tracker.

This image

* Contains only the base operating system and required Perl packages
* Does not initialize a database for the RT application
* Does not configure the RT application itself
* Loads the `MySQL` client packages and perl libraries
* Includes modules required for development and testing purpose
* Contains all the required plumbing to make RT work under Debian Linux

### Image building notes

This image contains development modules and tools suitable for RT extension Perl developers,
e.g. the C compiler, Perl module installation libraries, etc.

To build this image, run

```bash
$# cd <this dir>
$# docker build --pull --rm --tag lrestifo/rt-base-debian:0.01 .
```

### Typical usage

This image serves 2 main purposes:

* Test Perl module development, such as RT Extension packages
* Be included into application-specific images

Once built, the image can be run interactively e.g. to install additional modules or to run commands from the shell.

You can run this image interactively from Visual Studio Code or from the command line with

```bash
$# docker run --rm -it lrestifo/rt-app-base-debian:0.01 .
```

A more useful way to use this image is to include as the `FROM` Dockerfile command of an RT application container.

### Credits

Thanks to Christian Loos (GitHub:@cloos) for publishing RT docker examples.
This image was heavily inspired by his work.
