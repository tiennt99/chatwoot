## Build chatwoot bằng docker
- Sửa lại file env posgre
```text
POSTGRES_DATABASE=chatwoot_production
POSTGRES_HOST=10.6.30.98
POSTGRES_USERNAME=odoo
POSTGRES_PASSWORD=odoo
RAILS_ENV=production
RAILS_MAX_THREADS=5
- ```

```shell
docker-compose -f docker-compose.production.yaml up -build -d
```

```shell
docker compose run --rm rails bundle exec rails db:chatwoot_prepare
```
