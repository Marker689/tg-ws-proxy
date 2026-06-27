# tg-ws-proxy

Telegram MTProto WebSocket Bridge Proxy — Docker-билд-сервер.

Этот репозиторий автоматически собирает Docker-образ tg-ws-proxy из upstream-репозитория [Flowseal/tg-ws-proxy](https://github.com/Flowseal/tg-ws-proxy) и пушит его в [GHCR](https://github.com/marker689/tg-ws-proxy/pkgs/container/tg-ws-proxy).

## Образы

- `ghcr.io/marker689/tg-ws-proxy:latest` — последняя версия из main
- `ghcr.io/marker689/tg-ws-proxy:sha-<commit>` — образ конкретного коммита
- `ghcr.io/marker689/tg-ws-proxy:<branch>` — образ ветки

## Триггеры

- Push в main этого репозитория
- Завершение воркфлоу `Build & Release` в upstream-репозитории
- Ручной запуск через GitHub Actions → Actions → Docker Build → Run workflow

## Использование

```bash
docker run -d \
  --name tg-ws-proxy \
  --restart=always \
  -e TG_WS_PROXY_SECRET=*** \
  -p 1443:1443 \
  ghcr.io/marker689/tg-ws-proxy:latest
```

## Лицензия

MIT — см. [LICENSE](LICENSE)
