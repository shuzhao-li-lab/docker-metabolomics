FROM python:3.8.6-slim-buster
LABEL maintainer=shuzhao

RUN pip install mummichog==2.4.4; \
    rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["bin/bash"]
