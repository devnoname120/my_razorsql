# My_RazorSQL (unlicensed version)

![workflow](https://github.com/henkez73/my_razorsql/actions/workflows/publish-docker-image.yaml/badge.svg)

RazorSQL is copyrighted and title to Software and all associated intellectual property rights are retained by Richardson Software, LLC.

To run RazorSQL use the runme.sh script which sets up all the required bits and copies the profiles and preferences into the container.

On macOS you will need to set up an Xorg graphical server first and then run `export DISPLAY=docker.for.mac.host.internal:0`. You can find the instructions here: https://gist.github.com/devnoname120/ce02ef43da968e15340427c2f1c286a7

## Saving your profiles between container runs

1. Run `docker cp my_razorsql:home/developer/.razorsql/data/profiles.txt .` when your my_razorsql container is running so it can copy the profiles.txt file from the running container to the directory you are currently in (you can also do this for preferences.txt if required).

2. Copy or move the profiles.txt file into the data folder so that when you start the container with the runme.sh script it copies the local data/profiles.txt back into the running container.
