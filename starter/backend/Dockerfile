FROM python:3.10-alpine

RUN apk add --no-cache \
    gcc \
    musl-dev \
    linux-headers \
    python3-dev \
    libffi-dev

ENV CFLAGS="-Wno-error=incompatible-pointer-types"

WORKDIR /app

RUN pip install --no-cache-dir pipenv

COPY Pipfile Pipfile.lock ./

RUN pipenv install --system --ignore-pipfile

COPY . .

EXPOSE 5000

CMD ["python", "app.py"]
