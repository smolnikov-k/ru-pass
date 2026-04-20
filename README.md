# ru-pass

Кастомный `geosite.dat` на базе [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) с доп. RU-доменами для direct-роутинга (обход VPN).

## Скачать

- `geosite.dat`: https://github.com/nobi-k/ru-pass/releases/latest/download/geosite.dat
- `geoip.dat`: https://github.com/nobi-k/ru-pass/releases/latest/download/geoip.dat

Обновляется автоматически каждую ночь (22:00 UTC) + при пуше в `main`.

## Добавить свой домен в RU bypass

Кастомные домены живут в файле [`custom-ru-direct.txt` на ветке `hidden`](https://github.com/nobi-k/ru-pass/blob/hidden/custom-ru-direct.txt).

1. Открой файл на ветке `hidden`
2. Добавь домен новой строкой (без `@ads`, без комментариев — просто `example.com`)
3. Коммит → workflow пересоберёт `geosite.dat` через ~3-5 минут и выложит новый релиз

Для каждого домена из `custom-ru-direct.txt` workflow делает три вещи перед сборкой:
- Прописывает домен в `community/data/category-ru` без атрибутов (`@ads`, `@!cn` и т.п.)
- Удаляет домен и все его поддомены из `community/data/category-ads-all` (чтобы ads-блокировщики не резали)
- Удаляет из `community/data/gfw` (чтобы GFW-правило не форсило прокси)

Клиенты, использующие тег `geosite:category-ru` для direct routing, начнут пропускать эти домены напрямую.

## Клиентское применение

Happ Plus → RU Bypass → geosite URL:
```
https://github.com/nobi-k/ru-pass/releases/latest/download/geosite.dat
```

## Лицензия

GPLv3 (upstream: Loyalsoldier).
