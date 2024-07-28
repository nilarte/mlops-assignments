FROM python:3.11.7-slim

WORKDIR /app
COPY [ "model.bin", "model.bin" ]

#RUN pip install -U pip & pip install pipenv
RUN pip install pipenv

COPY [ "Pipfile", "Pipfile.lock", "./" ]

RUN pipenv install --system --deploy

COPY [ "batch.py", "batch.py" ]

ENTRYPOINT [ "python", "batch.py" ]
