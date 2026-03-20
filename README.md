# PHL Code Club - CTF

This repo is the top-level repository for all PHL Code Club CTF code. A ton of stuff is TBD, but here's some notes in case anyone comes on here.

This repo uses git submodules to contain the other active repos for the CTF stack -- this is because CTFd is its own repo on GitHub that we've forked for the purposes of this CTF, and it felt cleaner to make it a submodule than to just copy/paste their whole codebase.

## Development Setup

* Ensure you've [installed Docker](https://docs.docker.com/engine/install/) on your device
* Clone this repo with `git clone --recursive <link>`
* You're ready to code!
    * Only oddity is that each submodule in this directory is its own Git repo, and this repo tracks specific commits of the submodules.
    * If you make a change within a submodule (e.g. CTFd), you'll need to also make a commit to update the submodule's tracked commit in this repo.


## VPS Configuration

The CTF host has:
* Ubuntu
* `docker.io` from the Ubuntu repos installed because I like clean package sources (as opposed to from Docker directly)
* A `ctf` user with Docker permissions
