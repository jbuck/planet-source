FROM centos:6

RUN groupadd -g 10001 app && \
    useradd -d /app -g 10001 -m -u 10001 app
WORKDIR /app

COPY . /app
RUN chown -R app:app /app

USER app

RUN mkdir cache output

CMD ["python", "spider.py", "local.ini"]
