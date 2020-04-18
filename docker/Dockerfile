
#cd ..
#docker build --file=docker/Dockerfile --tag=zwave .

#docker run --rm --device=/dev/ttyUSB0 zwave $@

FROM alpine:latest

ADD zwave_s /zwave_s

RUN apk add --update-cache \
		perl \
		perl-device-serialport \
	&& rm -rf /var/cache/apk/*


ENTRYPOINT ["/zwave_s"]

