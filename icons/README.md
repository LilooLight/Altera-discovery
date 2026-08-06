# МИС Альтера — Пакет иконок бренд-бука

**31 иконка** в стиле **Material Symbols Outlined**, 24px, формат SVG.

## Содержание

| Файл | Описание |
|---|---|
| `svg/` | Папка с 31 отдельным SVG-файлом (по одной иконке на файл) |
| `sprite.svg` | Единый SVG-спрайт со всеми иконками внутри `<symbol>` |
| `preview.html` | HTML-страница с визуальным превью всех иконок (откройте в браузере) |
| `README.md` | Этот файл |

## Цвет и использование

Все SVG используют `currentColor` — цвет наследуется из CSS `color` родителя. Чтобы получить фирменный Тиффани:

```css
.icon { color: #5ECEC1; }
```

```html
<svg width="24" height="24" viewBox="0 0 24 24"><use href="sprite.svg#icon-autorenew"/></svg>
```

Или вставьте SVG-код прямо в HTML — `<path fill="#5ECEC1" d="..."/>`.

## Полный список иконок (31 шт.)

### Логотип и знак
- **`autorenew`** — фирменный знак МИС Альтера (3 диагональные изогнутые линии). Используется на слайдах 1, 3, 4, 9, 10, 14, 15.

### Характер бренда (Слайд 2 — Философия)
- `sentiment_satisfied` — Дружелюбный, но без панибратства
- `verified` — Экспертный
- `auto_awesome` — Современный и технологичный
- `self_improvement` — Спокойный

### Логотип — правила (Слайд 3)
- `palette` — Цветная версия
- `contrast` — Монохром
- `straighten` — Минимальные размеры

### Охранное поле (Слайд 4)
- `arrow_outward` — Выноски на схеме
- `block` — Запрещённые действия

### Цвета и палитра (Слайд 5)
- `touch_app` — Акцент / точечное действие

### Статусные цвета (Слайд 6)
- `check_circle` — Успех (#27AE60)
- `warning` — Предупреждение (#F2B84B)
- `error` — Ошибка (#F35E62)
- `info` — Информация (#386BF6)
- `workspace_premium` — Премиум-акцент (#C9A96E)
- `auto_awesome` — Выделение (#8C56FF, переиспользована)

### Биофильный стиль (Слайд 8)
- `gradient` — Мягкие 3D-абстракции / стекло

### Полиграфия и материалы (Слайд 9)
- `layers` — Матовая офсетная печать
- `flare` — Выборочный УФ-лак
- `texture` — Блинтовое тиснение

### UI-кит данных (Слайд 12 — тёмная тема)
- `favorite_border` — Здоровье (используется filled heart из нового Material Symbols, т.к. `favorite_border` удалён из репо)
- `medication` — Медикаменты
- `monitor_heart` — Мониторинг пациента
- `calendar_today` — Календарь приёмов
- `analytics` — Аналитика
- `health_and_safety` — Безопасность пациента

### Tone of Voice (Слайд 13)
- `handshake` — На Вы
- `groups` — На равных
- `visibility` — Простота
- `shield` — Без паники

### Компоновка логотипа (Слайд 15)
- `align_horizontal_left` — Левофланговое расположение в UI
- `straighten` — Минимальный размер (переиспользована)

## Источник

Официальный репозиторий Google Material Symbols:
https://github.com/google/material-design-icons/tree/master/symbols/web

Лицензия: Apache License 2.0 — свободное коммерческое использование.

## Примечание о `favorite_border`

В новом репо Material Symbols нет отдельной outlined-версии `favorite_border` — там только filled `favorite`. В этом пакете `favorite_border.svg` содержит filled heart. Если нужен именно контурный вариант — можно:
1. Открыть `favorite_border.svg` в Figma/Illustrator и вручную перевести в stroke
2. Использовать `health_and_safety` (тоже про здоровье, есть в наборе)
3. Или использовать иконку `favorite` с CSS `fill: none; stroke: currentColor; stroke-width: 2`
