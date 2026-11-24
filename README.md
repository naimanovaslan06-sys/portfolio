# ГИС-портфолио Аслана Найманова

Сайт из одного файла: `index.html`. Все карты и графики встроены прямо в него, отдельная папка с картинками не нужна.

## Как опубликовать на GitHub Pages

1. Зарегистрируйтесь или войдите на https://github.com.
2. Нажмите **New repository** (плюс в правом верхнем углу → New repository).
   - Repository name: `portfolio` — сайт будет по адресу `https://ЛОГИН.github.io/portfolio/`.
     Если назвать репозиторий `ЛОГИН.github.io`, сайт откроется прямо по `https://ЛОГИН.github.io/`.
   - Выберите **Public** и нажмите **Create repository**.
3. На странице нового репозитория нажмите ссылку **uploading an existing file**.
4. Распакуйте архив и перетащите в окно браузера файлы `index.html` и `README.md`
   (только файлы, не саму папку `portfolio`, иначе сайт окажется по адресу `.../portfolio/portfolio/`).
   Важно: открывайте `index.html` только после распаковки архива.
5. Внизу нажмите **Commit changes**.
6. Откройте **Settings → Pages**. В блоке *Build and deployment*:
   Source — **Deploy from a branch**, Branch — **main**, папка — **/ (root)**. Нажмите **Save**.
7. Через 1–2 минуты сайт появится по адресу `https://ЛОГИН.github.io/portfolio/`
   (ссылка также будет показана вверху страницы Settings → Pages).

## Как обновлять

В репозитории: **Add file → Upload files**, перетащите изменённые файлы с теми же именами → **Commit changes**.
Через минуту изменения появятся на сайте (если нет — обновите страницу с Ctrl+F5).

## Как подключить форму обратной связи (по желанию)

1. Зарегистрируйтесь на https://formspree.io и создайте форму — вы получите адрес вида `https://formspree.io/f/xxxxabcd`.
2. В `index.html` найдите строку `<form id="form">` и замените её на
   `<form id="form" action="https://formspree.io/f/xxxxabcd" method="POST">`.
3. В конце файла найдите блок, который начинается с `document.getElementById('form').addEventListener` (3 строки),
   и удалите его — тогда форма будет отправлять письма вам на почту.

## Как добавить новый проект

Скопируйте в `index.html` блок `<section class="band" id="projects"> … </section>`,
поменяйте тексты, а новые картинки загрузите в репозиторий в папку `img/` и укажите путь вида `img/my-map.webp`
(лучше формат .webp или .jpg шириной 1000–1400 px).
