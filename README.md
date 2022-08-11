## Парсинг онлайн-библиотеки [tululu.org](https://tululu.org)
С помощью срипта можно скачать книги от и до указанных id, а также изображения их обложек и такую информацию как имя автора, жанр, комментарии.

Ссылка на [Github Pages](https://iterekhov98.github.io).

### Быстрый запуск без установки и web-сервера
Скачайте репозиторий с кодом, перейдите в директорию `pages` и откройте в браузере любую из страниц.  

### Установка
Скачайте репозиторий с кодом, установите необходимые зависимости:
```
pip install -r requirements.txt
```
### Запуск сайта
В консоли выполните команду:
```
python server.py
```
Сайт будет доступен по адресу [http://127.0.0.1:5500](http://127.0.0.1:5500).

### Запуск парсера
Основная команда для запуска скрипта:
```
python main.py 
```
Обратите внимание, что вызов этой команды без аргументов приведёт к скачиванию ВСЕХ страниц из коллекции, что, вероятно, не является вашей целью. Ограничить диапазон скачиваемых страниц можно с помощью дополнительных аргументов:
```
python main.py --start_page=1 --end_page=3
```

Такая команда скачает книги с первых двух страниц.

Также доступны некоторые кастомные настройки:
- `--dest_folder` - указать каталог для сохранения результатов (по умолчанию рабочая директория кода)
- `skip_imgs` - отменить скачивание картинок (по умолчанию false)
- `skip_txt` - отменить скачивание текста книг (по умолчанию false)
- `json_path` - указать каталог для сохранения json-файла с описанием книг (по умолчанию рабочая директория кода)
