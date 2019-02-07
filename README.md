Dockerized Old Tools
--

One of the more useful possible uses of Docker is to allow older vulnerable and unsupported tools to be run in isolated environments.  this is just a repo. with some tools that could be useful to have older versions of.

The images should be available on Docker hub via automated builds.


Firefox
--
To run you'll just need to specify some environment variables and volumes (this is assuming you're runnning from Linux)

For example below this should run Firefox version 30. Just change the number at the end to one of the versions in the repo (10,15,20,25,30,35,40).

You need to give access to your X Server first before runnig GUI programs in Docker.  The YOLO approach is `xhost +local:root` 

Then you can run something like the below to get your firefox running

`docker run -it -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix raesene/firefox-v30`

N.B. Don't have another version of Firefox running on the host at the same time or it'll just start another instance of that :)
