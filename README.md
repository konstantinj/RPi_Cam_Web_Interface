Web based interface for controlling the Raspberry Pi Camera, includes motion detection, time lapse, and image and video recording.
Current version 6.6.13
All information on this project can be found here: http://www.raspberrypi.org/forums/viewtopic.php?f=43&t=63276

The wiki page can be found here:

http://elinux.org/RPi-Cam-Web-Interface

This includes the installation instructions at the top and full technical details.
For latest change details see:

https://github.com/silvanmelchior/RPi_Cam_Web_Interface/commits/master
  
This version has updates for php7.3 / Buster. May need further changes for nginx

## Build docker file

Using docker compse:

Edit docker-compose.yml:

```yml
version: '3'
services:
    rpicam:
        # image: konjak/rpicam
        build:
            context: .
            dockerfile: Dockerfile
        restart: always
        # ... etc
```

Run `sudo docker-compose up --force-recreate`

