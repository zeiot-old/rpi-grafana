# RPI Grafana

* Master: [![pipeline status](https://gitlab.com/zeiot/rpi-grafana/badges/master/pipeline.svg)](https://gitlab.com/zeiot/rpi-grafana/commits/master)

Docker image of [Grafana][] to use on a [Raspberry PI][].

Configure binfmt-support on the Docker host (works locally or remotely, i.e: using boot2docker):

    $ docker run --rm --privileged multiarch/qemu-user-static:register --reset

Then you can run an armhf image from your x86_64 Docker host :

    $ make run version=3.1

Or build :

    $ make build version=3.1


# Supported tags

* [![](https://images.microbadger.com/badges/image/zeiot/rpi-grafana:4.0.2.svg)](https://microbadger.com/images/zeiot/rpi-grafana:4.0.2 "Get your own image badge on microbadger.com")
* [![](https://images.microbadger.com/badges/image/zeiot/rpi-grafana:3.1.1.svg)](https://microbadger.com/images/zeiot/rpi-grafana:3.1.1 "Get your own image badge on microbadger.com")
* [![](https://images.microbadger.com/badges/image/zeiot/rpi-grafana:3.0.4.svg)](https://microbadger.com/images/zeiot/rpi-grafana:3.0.4 "Get your own image badge on microbadger.com")

## License

See [LICENSE](LICENSE) for the complete license.


## Changelog

A [ChangeLog.md](ChangeLog.md) is available.


## Contact

Nicolas Lamirault <nicolas.lamirault@gmail.com>


[Raspberry PI]: https://www.raspberrypi.org/
[Grafana]: https://grafana.org/
