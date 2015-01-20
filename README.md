# BIMserver Docker Image

A [Docker][docker] image for [BIMserver][bimserver] on [Tomcat][tomcat].

* [BIMserver image on DockerHub][dockerhub]


## Installation

To run BIMserver in a container on your server, Docker needs to be [installed][docker-install]. On
Debian/Ubuntu Linux, this is as simple as `sudo apt-get install docker.io`.

With Docker installed, running BIMserver is as simple as
`sudo docker run -p 8080:8080 urbanetic/bimserver`. This will run BIMserver on port 8080.

You can easily forward this to port 80 using [iptables][iptables] with the command
`sudo iptables -t nat -A PREROUTING -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 8080`.


[bimserver]: http://bimserver.org/
[docker]: https://www.docker.com/
[dockerhub]: https://registry.hub.docker.com/u/urbanetic/bimserver/
[docker-install]: https://docs.docker.com/installation/
[iptables]: https://help.ubuntu.com/community/IptablesHowTo
[tomcat]: https://tomcat.apache.org/
