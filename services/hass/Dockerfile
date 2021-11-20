FROM homeassistant/home-assistant:2021.11

COPY ./bin /maison/bin
RUN chmod ug+rx /maison/bin/* && \
    mkdir -p /tmp/maison && \
    # Install DMX
    mkdir -p /maison/hass/config/custom_components/dmx && \
    wget 'https://github.com/bartfeenstra/hass-dmx/archive/rgbd.zip' -O /tmp/maison/dmx.zip && \
    mkdir -p /tmp/maison/dmx && \
    unzip /tmp/maison/dmx.zip -d /tmp/maison/dmx && \
    mv /tmp/maison/dmx/hass-dmx-rgbd/custom_components/dmx/* /maison/hass/config/custom_components/dmx && \
    # Clean up.
    rm -r /tmp/maison

CMD /maison/bin/entry-point
