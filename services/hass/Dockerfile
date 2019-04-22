FROM homeassistant/home-assistant:0.91.3

COPY ./conf /maison/conf
COPY ./bin /maison/bin
RUN chmod ug+rx /maison/bin/*

CMD /maison/bin/entry-point
