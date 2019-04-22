FROM homeassistant/home-assistant:0.85.1

RUN cd /bin \
    && wget https://raw.githubusercontent.com/jirutka/esh/v0.1.1/esh \
    && echo '2a992f8b74cb47f8b0e36dfb4c16061d3042bfaa  esh' | sha1sum -c \
    && chmod ug+rx ./esh \
    || exit 1

COPY ./conf /maison-hab/config
COPY ./run /maison-hab/run
RUN chmod ug+rx /maison-hab/run

CMD /maison-hab/run
