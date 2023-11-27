# skills-guide_compose

Репозиторий хранит файлы для развертывания проекта skills-guide через docker compose

## 🛠️ Подготовка в запуску
1. Во-первых, убедитесь, что у вас установлены как Docker.
    - [Install Docker Engine](https://docs.docker.com/engine/install/debian/)
2. Клонируйте репозиторий GitHub:
```bash
git clone https://github.com/acronicsM/skills-guide_compose.git
```
3. Перейдите в директорию проекта:
```bash
cd skills-guide_compose
```
4. Установите переменные окружения:
```bash
nano .env
```

5. Если нужен ssl сертификат:
   1. Получите сертификаты (следуйте инструкции на экране):
   ```bash
   docker compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d [domain-name]
   ```
   2. Замените настройку в файле /nginx/conf/nginx.conf на /nginx/conf/nginx.443conf
    ```bash
   cp nginx/conf/nginx.443conf nginx/conf/nginx.conf
   ```
   
6. Укажите server_name в файле /nginx/conf/nginx.conf
 ```bash
   nano nginx/conf/nginx.conf
   ```

7. Запустите службу с помощью Docker Compose:
```bash
docker compose up
```

## 💡 Инструкции к настройке и использованию сервисов проекта

- [PostgreSQL](https://www.postgresql.org/docs/)
- [pgAdmin](https://www.pgadmin.org/docs/pgadmin4/7.8/getting_started.html)
- [GPT](https://github.com/acronicsM/skills-guide_gpt)
- [Parser](https://github.com/acronicsM/ParserHH)
- [Telegram](https://github.com/acronicsM/skills-guide_telegram)
- [Site](https://github.com/acronicsM/skills-guide_site)

