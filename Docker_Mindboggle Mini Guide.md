___
# Docker Mini-Guide

_see docker images_
`docker image ls`

_see docker container_
`docker container ls`

_run a docker image (call the image)_
`docker run -it ubuntu`
_=> "-it" stands for interactive shell. ubuntu is the image to be run_

_call it and mount a real folder to the docker image of ubuntu_
`docker run -it -v /home/user/hd:/home ubuntu`
_=> the content of the hd folder is in the home folder. OBS! THIS IS IMPORTANT because you can not get the data out of the docker!!!_

_call a function not interactively from outside the image (here "mindboggle" is the docker image and "antsn4" is the function run)_
`docker run mindboggle antsn4 -d 3 ...`

_instead of exit to create a detached call_
`docker run -itd -name competent_nobel ubuntu`

_get the list of running containers_
`docker container ls`

_choose the call (run a saved container, here is "MB2") by copying the NAMES or ID_
`docker attach MB2`
_OBS! if you exit it is closed and detached_

_exit docker without removing it_
`on MAC: ctrl +Q`
`on PC: ctrl + P`

_stop the container_
`docker stop [name container]`

_doublecheck if it is still there_
`docker container ls -a`

_remove container_
`docker rm [name container]`

_delete the ubuntu image_
`docker image rm -f ubuntu`

___
# Mindboggle Mini-Guide

_run the mindboggle docker image_
`docker run -it nipy/mindboggle bash`
_see eg mindboggle_
`mindboggle -h`
