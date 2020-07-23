FROM ubuntu:focal

RUN apt-get update && \
    apt-get -y install bzflag-server && \
    rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "/usr/games/bzfs" ]

CMD [ "--help" ]
