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
Migrate
```shell
docker compose run --rm rails bundle exec rails db:chatwoot_prepare
```
Note:
Ubuntu => volumes thêm ./data


Hưỡng dẫn http => https
./ngrok http 80
https://lekssays.wordpress.com/2017/01/18/how-to-make-your-localhost-online-on-ubuntu/

Connect fb vào cấu hình
https://developers.facebook.com/apps/101810679523238/fb-login/settings/
https://www.chatwoot.com/docs/self-hosted/configuration/features/integrations/facebook-channel-setup/

##https://developers.facebook.com/tools/accesstoken
FB_VERIFY_TOKEN=101810679523238|_SP67lbtI8KGkTIjeQKVM-qDYjU
# https://developers.facebook.com/apps/101810679523238/settings/basic/
FB_APP_SECRET=bbce119c798087c545607571f6655783
FB_APP_ID=101810679523238
Connect zalo qua api channel
https://developers.zalo.me/app/1161529783500880903/webhook
Tao webhook tren zalo
- Tao 1 api https don su kien webhook
Tao webhook nhan su kien call api
