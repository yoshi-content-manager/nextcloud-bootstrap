# nextcloud-bootstrap

## Setup

```bash
cp .env.template .env
```

Update values in `.env`.

```bash
docker compose up -d
```

## Config

- Access `http://localhost:8081` or the domain in .env
- Create admin user
- Skip app install
- `alias occ='docker compose exec app php occ'`

```bash
occ app:disable dashboard
occ app:disable photos
occ config:app:set core defaultTemplateDirectory --value="/var/www/custom_skeleton"
```

## Deleting everything and start from scratch

```bash
docker compose down -v
docker compose up -d
```
