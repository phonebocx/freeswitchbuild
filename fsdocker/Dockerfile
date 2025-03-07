ARG VERSION
FROM basedocker:${VERSION}

ENV FS_FILES_DIR=/usr/local/build/SOURCES

ADD alldebs.tar.gz /usr/local/

RUN apt-get -y install libpcre3-dev libpython3-dev python3-dev python3-all-dev dh-python python-is-python3

RUN apt-get -y install /usr/local/*.deb


