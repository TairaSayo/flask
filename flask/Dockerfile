FROM python:alpine3.11

RUN pip install Flask

WORKDIR /app

COPY flask_app.py /app

HEALTHCHECK --interval=1s --timeout=1s --start-period=5s --retries=3 CMD curl -f localhost:5000 || exit 1

ENTRYPOINT [ "python" ]

CMD [ "flask_app.py" ]