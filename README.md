# docker-asterisk-armhf

asterisk version: 13

# usage

1. sudo docker build --rm=True -t USER/asterisk .
1. sudo ./run.sh
1. cp docker-container.service /etc/systemd/system/docker-container@asterisk.service
1. systemctl enable docker-container@asterisk.service

If you use OpenVPN on docker, you need to run OpenVPN container with --net=host option.

# Tested On

* Cubox (not cubox-i)
    * kernel is 4.0.2-1

# Known issue

* No data valumes for the configuration (Overwrite all settings).
* CA for WebRTC does not be included.
* Need to rebuild to update configurations.
