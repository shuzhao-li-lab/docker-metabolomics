ARG OPENMS_TAG=latest
FROM openms/contrib:${OPENMS_TAG}

RUN apt-get update && apt-get install -y --no-install-recommends wget unzip libqt5svg5 qtbase5-dev\
	&& rm -rf /var/lib/apt/lists/*
	
RUN wget https://github.com/OpenMS/OpenMS/releases/download/Release2.6.0/OpenMS-2.6.0-Debian-Linux-x86_64.deb && \
    dpkg -i OpenMS-2.6.0-Debian-Linux-x86_64.deb && \
    rm OpenMS-2.6.0-Debian-Linux-x86_64.deb

ENTRYPOINT ["bin/bash"]
