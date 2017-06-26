FROM node:latest

RUN apt-get update && \
    apt-get install -yq --no-install-recommends libzmq-dev ipython-notebook && \
    apt-get clean

RUN git clone https://github.com/xwang2713/ijsecl.git && \
    cd ijsecl && \
    npm i

WORKDIR ijsecl

CMD git pull && npm run test:4 && npm run test:5
