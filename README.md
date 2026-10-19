https://cryzhovnic.github.io/electro-quiz/

# Электробезопасность — тестирование по билетам

PWA без сборки на стороне сервера: 10 билетов по 10 вопросов, работает офлайн.

## Структура

- `index.html`, `js/app.js` — интерфейс и логика
- `data/exam_data.json` — вопросы (источник для приложения); `data/exam_data.py` — те же данные в виде Python-словаря
- `css/tailwind.css` — **готовая** сборка стилей (в репозитории, пересобирать нужно только при смене классов)
- `sw.js` — service worker (офлайн-кэш; при изменении файлов из `ASSETS` увеличивайте `CACHE`)

## Пересборка стилей

После правок классов Tailwind в `index.html` или `js/app.js`:

```bash
npx tailwindcss@3 -c tailwind.config.js -i src/input.css -o css/tailwind.css --minify
```

## Локальный запуск

```bash
python3 -m http.server 8000   # затем http://localhost:8000
```
