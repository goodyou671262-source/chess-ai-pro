# ♟ Chess AI Pro — Halloween Edition

**Offline chess in a single HTML file: play against a built-in engine, study tactics, review games, edit positions, and switch to a Halloween-themed mode.**

[Русский](#русский) · [English](#english)

---

<a id="русский"></a>
## 🇷🇺 О проекте

**Chess AI Pro — Halloween Edition** — браузерное шахматное приложение с классической партией, встроенным движком, учебными инструментами и необязательными хэллоуинскими игровыми механиками. Приложение упаковано в один файл `index.html`: сборка, установка пакетов и подключение CDN не требуются.

### Возможности

- **Игра против компьютера.** Встроенный движок выбирает ходы с настраиваемой глубиной поиска и временем расчёта.
- **Партия ИИ против ИИ.** Можно запустить матч двух экземпляров движка, изменять параметры расчёта, ставить матч на паузу и делать отдельный ход.
- **Разбор партии.** Приблизительная оценка ходов, категории качества, график динамики преимущества и просмотр позиции из списка анализа.
- **История и запись партии.** Отмена хода, список ходов, копирование и скачивание PGN.
- **FEN и редактор позиции.** Создание нестандартных расстановок, установка или удаление фигур, импорт и экспорт FEN.
- **Тактическая академия.** Справочник мотивов и матовых идей, поиск и фильтрация тем, а также интерактивные задачи на доске.
- **Ввод хода текстом.** Можно указывать шахматные координаты или описывать ход по-русски; приложение проверяет допустимость хода.
- **Подсказки движка.** Получение рекомендации для текущей позиции.
- **Хэллоуинский режим.** Дополнительные игровые механики, эффекты, достижения и встроенные 3D-модели на WebGL.
- **Настройки и восстановление партии.** Параметры, состояние игры и учебный прогресс сохраняются в локальном хранилище браузера.
- **Адаптивный интерфейс.** Интерфейс рассчитан на настольные браузеры и мобильные экраны.

### Технологии

- HTML5 и CSS — структура интерфейса, оформление и адаптивная компоновка.
- Vanilla JavaScript — правила/состояние игры, интерфейс, тактические инструменты и поиск ходов.
- WebGL — встроенная отрисовка хэллоуинских 3D-моделей.
- `localStorage` — локальное сохранение настроек и состояния.

Встроенный шахматный ИИ использует классический поиск по дереву ходов с альфа-бета-отсечением, итеративным углублением, quiescence search, позиционными таблицами и таблицей транспозиций. Несмотря на отдельные подписи в интерфейсе, это **не нейросетевая модель**.

### Как запустить

1. Скачайте `index.html` или клонируйте репозиторий.
2. Откройте `index.html` в современном браузере.
3. Нажмите **«Новая партия»** и выберите фигуру, чтобы начать игру.

Сборщик, Node.js, сервер и дополнительные зависимости для обычного локального запуска не нужны. Для публикации на GitHub Pages достаточно разместить `index.html` в корне репозитория и включить Pages в настройках репозитория.

### Данные и ограничения

- Игра и 3D-модели реализованы без внешних библиотек и CDN; основная игра может работать без подключения к интернету.
- Настройки, сохранённая партия и учебный прогресс остаются в том браузере/профиле, где их создали. Очистка данных браузера может удалить их.
- «Локальный аккаунт» не является облачной учётной записью: профиль хранится в браузере, не синхронизируется между устройствами и не предоставляет серверной аутентификации.
- Анализ партии использует ограниченную глубину и является приблизительным. Его оценки не следует считать турнирным рейтингом, гарантией оптимального хода или заменой полноценному анализу сильным шахматным движком.
- Сила игры зависит от глубины поиска, времени расчёта и устройства; заявленный рейтинг Elo не гарантируется.
- В репозиторий не включена лицензия. До добавления лицензии не следует считать, что сторонним пользователям автоматически предоставлено право копировать, распространять или изменять код.

### Публикация через GitHub Pages

1. Создайте репозиторий на GitHub и загрузите `index.html` вместе с этим `README.md`.
2. Откройте **Settings → Pages**.
3. В разделе публикации выберите **Deploy from a branch**, ветку `main` и папку `/(root)`, затем сохраните настройки.
4. После публикации GitHub покажет адрес сайта в разделе Pages.

### Предлагаемые метаданные GitHub

- **Имя репозитория:** `chess-ai-pro-halloween`
- **Краткое описание:** `Offline browser chess with a built-in search engine, tactical puzzles, position analysis, FEN/PGN tools, and a Halloween mode.`
- **Topics:** `chess`, `chess-ai`, `chess-engine`, `javascript`, `html`, `offline`, `webgl`, `chess-puzzles`, `github-pages`

---

<a id="english"></a>
## 🇬🇧 About

**Chess AI Pro — Halloween Edition** is a single-file browser chess application combining classic chess, a built-in search engine, tactical training tools, position editing, game review, and an optional Halloween-themed mode. It runs from `index.html` without a build step, package installation, external libraries, or CDN assets.

### Features

- **Play against the built-in engine** with configurable search depth and thinking time.
- **AI vs. AI matches** with separate engine settings, pause/resume controls, and single-move stepping.
- **Game analysis** with approximate move evaluations, quality labels, an advantage graph, and position review.
- **Move history and PGN export** with undo, copy, and download actions.
- **FEN and position editor** to place or remove pieces and load/export custom positions.
- **Tactics academy** with searchable themes, checkmate ideas, and interactive board puzzles.
- **Text-based move input** using algebraic coordinates or Russian descriptions, validated against legal moves.
- **Engine hints** for the current position.
- **Halloween mode** featuring custom mechanics, visual effects, achievements, and embedded WebGL 3D models.
- **Local persistence** for game state, preferences, and learning progress.
- **Responsive interface** for desktop and mobile browsers.

### Implementation

The app uses HTML5, CSS, vanilla JavaScript, WebGL, and browser `localStorage`. Its chess engine is a traditional search-based engine using alpha-beta pruning, iterative deepening, quiescence search, positional tables, and a transposition table. Despite some UI labels, it is **not a neural-network engine**.

### Run locally

1. Download `index.html` or clone this repository.
2. Open `index.html` in a modern browser.
3. Select **New Game** to start playing.

No build tools, Node.js runtime, server, or third-party dependencies are required for local use. For GitHub Pages, place `index.html` in the repository root and enable Pages in the repository settings.

### Data and limitations

- The app has no required external libraries or CDN dependencies and its core gameplay can run offline.
- Settings, game state, and learning progress are stored in the current browser profile. Clearing browser site data may erase them.
- The local account feature is not a cloud account system, does not sync across devices, and does not provide server-side authentication.
- Game analysis is depth-limited and approximate; it is not a tournament rating or a guarantee of the objectively best move.
- Playing strength depends on search depth, available thinking time, and hardware; no Elo rating is guaranteed.
- No software license is included yet. Until a license is added, do not assume third parties have permission to reuse, modify, or redistribute the code.

### Suggested GitHub metadata

- **Repository name:** `chess-ai-pro-halloween`
- **Description:** `Offline browser chess with a built-in search engine, tactical puzzles, position analysis, FEN/PGN tools, and a Halloween mode.`
- **Topics:** `chess`, `chess-ai`, `chess-engine`, `javascript`, `html`, `offline`, `webgl`, `chess-puzzles`, `github-pages`
