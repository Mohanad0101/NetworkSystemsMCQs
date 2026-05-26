# Как загрузить тесты на GitHub Pages

1. Создайте новый публичный репозиторий на GitHub или откройте уже существующий репозиторий курса.
2. Загрузите в корень репозитория все файлы из этой папки: `README.md`, `index.html`, `_sidebar.md`, `.nojekyll`, папку `quizzes/` и `PACKAGE_VALIDATION.json`.
3. Откройте `Settings` → `Pages`.
4. В разделе `Build and deployment` выберите `Deploy from a branch`.
5. Укажите ветку `main` и папку `/root`, затем нажмите `Save`.
6. После сборки отправьте студентам ссылку вида `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.

Важно: студентам лучше открывать именно GitHub Pages-сайт, а не отдельные `.md` файлы в интерфейсе github.com, потому что цветовая проверка ответов использует JavaScript.
