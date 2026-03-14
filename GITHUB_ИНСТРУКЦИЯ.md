# Как выложить сайт КОФЕРУМ на GitHub

## 1. Установите Git

- Скачайте установщик: **https://git-scm.com/download/win**
- Установите с настройками по умолчанию (галочка «Add Git to PATH» обязательна).

## 2. Создайте репозиторий на GitHub

1. Зайдите на **https://github.com** и войдите в аккаунт.
2. Нажмите **«+»** → **«New repository»**.
3. Укажите:
   - **Repository name:** например `koferum` или `koferum-site`
   - **Description:** по желанию, например «Сайт кофейни КОФЕРУМ, Кострома»
   - Выберите **Public**.
   - **НЕ** ставьте галочки «Add a README» / «Add .gitignore» — репозиторий создайте пустым.
4. Нажмите **«Create repository»**.

## 3. Загрузите сайт через командную строку

Откройте **PowerShell** или **Командную строку** и выполните по порядку (подставьте вместо `ВАШ_ЛОГИН` свой логин GitHub):

```bash
cd "C:\Users\User\сайт"

git init
git add .
git commit -m "Первый коммит: сайт КОФЕРУМ"
git branch -M main
git remote add origin https://github.com/ВАШ_ЛОГИН/koferum.git
git push -u origin main
```

Если репозиторий вы назвали не `koferum`, в строке с `git remote add origin` укажите свой URL (он будет показан на странице нового репозитория на GitHub).

При первом `git push` может потребоваться войти в GitHub (логин и пароль или токен).

## 4. Включить GitHub Pages (опционально)

Чтобы сайт открывался по адресу вида `https://ВАШ_ЛОГИН.github.io/koferum/`:

1. В репозитории на GitHub: **Settings** → **Pages**.
2. В блоке **Source** выберите ветку **main** и папку **/ (root)**.
3. Сохраните. Через 1–2 минуты сайт будет доступен по указанной ссылке.

**Важно:** в `index.html` все пути к файлам уже относительные (`about.png`, `gallery/`, `menu/`), поэтому на GitHub Pages всё будет отображаться корректно.
