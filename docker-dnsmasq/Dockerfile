

FROM ubuntu:14.04

RUN apt-get update && \
	apt-get install -y --no-install-recommends \
		dnsmasq \
	&& apt-get clean

VOLUME /etc/dnsmasq/dnsmasq.d

CMD /bin/bash
