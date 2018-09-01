FROM derekmerck/diana:arm32v7
VOLUME /etc/orthanc
COPY services.yml /config/diana/services.yml
CMD bash -c 'git pull  \
    && pip install -r requirements.txt \
    && pip install -e packages/diana \
    && python3 apps/cli/diana-mock.py -s /config/diana/services.yml scanner -d mock -r 30'