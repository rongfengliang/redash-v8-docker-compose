# redash:8.0.0.b30340 docker-compose running

## how to runing


* create env

```code
mkdir -p  opt/redash
cd  opt/redash
touch env
content:
PYTHONUNBUFFERED=0
REDASH_LOG_LEVEL=INFO
REDASH_REDIS_URL=redis://redis:6379/0
REDASH_MAIL_SERVER=xxxxxx
REDASH_MAIL_USERNAME=xxxxx
REDASH_MAIL_PASSWORD=xxxxx
REDASH_HOST=xxxxxxx
REDASH_ADDITIONAL_QUERY_RUNNERS=redash.query_runner.oracle
REDASH_MAIL_DEFAULT_SENDER=xxxxxxxx
POSTGRES_PASSWORD=INbnpou9MixIE036z6cI6pxOkbouNoUx
REDASH_COOKIE_SECRET=SfF3UIXzk4A92AjAp7U2ptRxLV8oBOFN
REDASH_SECRET_KEY=aeFiLXzB7QBVCakpFddK9YmEOh1necat
REDASH_DATABASE_URL=postgresql://postgres:INbnpou9MixIE036z6cI6pxOkbouNoUx@postgres/postgres
```

* start docker-compose service

```code
docker-compose up -d
```

* init db

```code
docker-compose run --rm server create_db
```

* config redash sys

```code
open http://localhost
```

