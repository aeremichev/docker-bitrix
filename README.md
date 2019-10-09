# docker-bitrix

Copy .env.template to .env

docker-compose exec node  bash
cd sites/site.ru/local/templates/.default/markup/src/
tars build -m
tars dev -l --custom-flags '--backend'
tars dev -t --custom-flags '--backend'

docker-compose exec php php -f /var/www/sites/site.ru/bitrix/modules/main/tools/cron_events.php
docker-compose exec php php -f /var/www/sites/pramana2.a-kulibin.ru/bitrix/modules/main/tools/cron_events.php