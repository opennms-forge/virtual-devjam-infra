FROM debian:stretch-slim

RUN apt-get update && \
    apt-get -y install wget apt-transport-https gnupg2 && \
    echo "deb https://overviewer.org/debian ./" > /etc/apt/sources.list.d/mc-overviewer.list && \
    wget -O - https://overviewer.org/debian/overviewer.gpg.asc | apt-key add - && \
    apt-get update && \
    apt-get -y install minecraft-overviewer && \
    rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "/usr/bin/overviewer.py" ]

CMD ["-h"]
