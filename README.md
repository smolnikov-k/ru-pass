# ru-pass

Кастомный `geosite.dat` на базе [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) с доп. RU-доменами для direct-роутинга (обход VPN).

## Скачать

- `geosite.dat`: https://github.com/nobi-k/ru-pass/releases/latest/download/geosite.dat
- `geoip.dat`: https://github.com/nobi-k/ru-pass/releases/latest/download/geoip.dat

Обновляется автоматически каждую ночь (22:00 UTC) + при пуше в `main`.

## Добавить свой домен в RU bypass

1. Открой `custom-ru-direct.txt`
2. Добавь домен новой строкой
3. Коммит в `main` — workflow пересоберёт через ~3-5 минут

Workflow снимает ограничивающие атрибуты (`@ads`, `@!cn`) с указанных доменов в `community/data/category-ru` и дописывает их, если их там нет. Клиенты, использующие тег `geosite:category-ru`, начнут роутить их как direct.

## Клиентское применение

Happ Plus → RU Bypass → geosite URL:
```
https://github.com/nobi-k/ru-pass/releases/latest/download/geosite.dat
```

## Лицензия

GPLv3 (upstream: Loyalsoldier).
