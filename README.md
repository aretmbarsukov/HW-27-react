# КАДР — пошук фільмів

React-застосунок для перегляду популярних фільмів, пошуку за назвою та перегляду
детальної інформації, акторського складу й відгуків за допомогою TMDB API.

## Локальний запуск

1. Створи API-ключ у своєму акаунті [TMDB](https://www.themoviedb.org/).
2. Створи в корені проєкту `.env`:

   ```env
   REACT_APP_TMDB_API_KEY=твій_api_ключ
   ```

3. Виконай `npm install`, потім `npm start`.

`.env` виключений із Git. Ключ у клієнтському застосунку доступний користувачам
браузера; обмеж його доменом у налаштуваннях TMDB.

## Маршрути

- `/` — популярні фільми дня.
- `/movies` — пошук фільмів за назвою; запит зберігається в URL.
- `/movies/:movieId` — деталі фільму.
- `/movies/:movieId/cast` — акторський склад.
- `/movies/:movieId/reviews` — відгуки.

Сторінки маршрутів завантажуються асинхронно через `React.lazy` і `Suspense`.

## Перевірка

```bash
npm run lint:js
npm run build
```

## GitHub Pages

Збірка налаштована для [HW-27-react](https://github.com/aretmbarsukov/HW-27-react).
Щоб TMDB API-запити працювали на сайті, додай ключ як GitHub Actions secret
`REACT_APP_TMDB_API_KEY` у налаштуваннях репозиторію. Workflow передає його у
збірку; значення не зберігається у файлах проєкту.

Сайт: <https://aretmbarsukov.github.io/HW-27-react/>.
