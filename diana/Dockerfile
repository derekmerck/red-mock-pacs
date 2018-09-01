FROM derekmerck/diana:arm32v7
COPY services.yml /config/diana/services.yml
WORKDIR /opt/diana
CMD bash -c 'git pull  \
    && pip install -r requirements.txt \
    && pip install -e packages/guidmint packages/diana \
    && python3 apps/cli/diana-mock.py -s /config/diana/services.yml -d mock -r 30'