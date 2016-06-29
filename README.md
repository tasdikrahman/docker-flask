## docker-flask

Simple example of integrating [docker](https://www.docker.com/) with web apps, [flask](http://flask.pocoo.org/) in this case

## Running it

Make sure you have docker up and running on your system. To check, you can do a

    $ sudo systemctl status docker
    [sudo] password for tasdik:
    ● docker.service - Docker Application Container Engine
       Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
       Active: active (running) since Tue 2016-06-28 12:55:03 IST; 20h ago
         Docs: https://docs.docker.com
     Main PID: 3447 (docker)
        Tasks: 27
       Memory: 562.1M
          CPU: 10min 39.671s
       CGroup: /system.slice/docker.service
               ├─3447 /usr/bin/docker daemon -H fd://
               └─3454 docker-containerd -l /var/run/docker/libcontainerd/docker-containerd.sock --runtime docker-runc --start-timeout 2m


**NOTE**: Command can vary depending on the OS you are on

Pull my docker image

```sh
$ docker pull prodicus/flask-example
```

Run the flask app

```sh
$ docker run -p 8888:5000 prodicus/flask-example
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
```

You will find the running app instance at [http://localhost:8888/](http://localhost:8888/)

![app on localhost](http://i.imgur.com/5pJ41n1.png)

## Building the `Dockerfile` locally

If you are feeling pumped for the day, you can build the `Dockerfile` locally.

```sh
$ git clone https://github.com/prodicus/docker-flask.git && cd docker-flask
$ docker build -t flask_docker .
$ docker run -p 8888:5000 flask_docker
# open the app on http://localhost:8888/
```

## Links

- [Docker hub image](https://hub.docker.com/r/prodicus/flask-example/)
- [Docker documentation](https://docs.docker.com/)

## License

GPLv3

    docker-flask
    Copyright (C) 2016 Tasdik Rahman

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

