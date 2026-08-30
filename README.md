# Facebook products finding

Public catalog of Facebook-advertised products. Each item compares Amazon.fr, a legitimate French shop, and a worldwide shop.

## Filters

The page loads `site/catalog.json` in the browser. Pills at the top combine:

- **Catégorie** — salle de bain, cuisine, nettoyage, électronique, mode, enfants, autre, or all.
- **Dédié à** — a named person, all, or untagged (*sans nom*).

Both filters apply together.

## Deploy

The Hostinger VPS serves this site with docker-compose (nginx:alpine, host port 8080):

```bash
docker compose up -d --build
```

`Dockerfile` copies `site/` into nginx html. `restart: unless-stopped` keeps the container up.
