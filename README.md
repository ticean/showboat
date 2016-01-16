Dockerized media setup, including:

* [couchpotato](https://couchpota.to/)
* [plex](https://plex.tv/)
* [sabnzbd](http://sabnzbd.org/)
* [sickrage](https://github.com/SiCKRAGETV/SickRage)


## Dependencies

* [Docker Toolbox](https://www.docker.com/docker-toolbox) - All the Docker tools
    you'll need.


## Installation

* Install dependencies listed above.
* If you are are on Mac or PC, then you'll need to create a Docker compatible
  host. This can be done with the docker tools. The following command creates a
  new virtual machine called "media":
  `docker-machine create --provider virtualbox media`
* Run the project with `docker-compose up -d` to run in the background.


## Port Forwarding

You'll most likely want to access the services from other computers and will
need to configure port fowarding if you're running the Docker containers in a
virtual machine. For example, this is true if you are using `docker-machine`
and VirtualBox in the instructions above.

For VirtualBox, configure the port forwarding manually with the VirtualBox GUI.

1. Open VirtualBox
2. Select the virtual machine
3. Open "Settings"
4. Open "Network"
5. Choose the network adapter, most likely "Adapter 1"
6. Open "Advanced"
7. Click "Port Forwarding"
8. Add entries for the service ports.


## Using the Services

The projects are available on the IP of your Docker host. This may vary with
your setup, but you can find the IP with this command:

```sh
docker-machine ip media
```

Then you can access the services on that IP and service port. For example, if
the IP is `192.168.99.100`, then you could access on the following URL's. (You
will need to replace the IP with your own if it is different.)

| Service     | Port  | URL |
| ----------- | ----- | --- |
| couchpotato | 5050  | http://192.168.99.100:5050  |
| plex        | 32400 | http://192.168.99.100:32400 |
| sabnzbd     | 8080  | http://192.168.99.100:8080  |
| sickbeard   | 8081  | http://192.168.99.100:8081  |


## Links and Info

* [Usenet Provider Info](https://www.reddit.com/r/usenet/wiki/providers#wiki_usenet_services_map)


## License

Copyright (c) 2016 Ticean Bennett

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
