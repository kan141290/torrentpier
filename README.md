TorrentPier II
======================

TorrentPier II - движок торрент-трекера, написанный на php.

## Установка

1. Распаковываем на сервер содержимое папки **upload**.

2. Создаем базу данных, в которую при помощи phpmyadmin (или любого другого удобного инструмента) импортируем дамп, расположенный в папке **install/sql/mysql.sql**
3. Правим файл конфигурации **config.php**, загруженный на сервер:
> $bb_cfg['db']['db1'] = array('localhost', 'dbase', 'user', 'pass', $charset, $pconnect);    
> В данной строке изменяем данные входа в базу данных, остальные правки в файле вносятся по усмотрению, исходя из необходимости из внесения (ориентируйтесь на описания, указанные у полей).

4. Редактируем указанные файлы:
>favicon.ico (меняем на свою иконку, если есть)  
    robots.txt (меняем адреса в строках Host: и Sitemap: на свои адреса)

## Права доступа на папки и файлы

Устанавливаем права доступа на данные папки 777, на файлы внутри этих папок (кроме .htaccess) 666:
- ajax/html
- cache
- cache/filecache
- files
- files/thumbs
- images
- images/avatars
- images/captcha
- images/ranks
- images/smiles
- log
- triggers

## Необходимые значения в php.ini

    mbstring.internal_encoding = UTF-8
    magic_quotes_gpc = Off

## Необходимые модули для php

    php5-tidy

## Необходимый запуск cron.php

Подробнее в теме http://torrentpier.me/threads/Отвязка-запуск-крона.52/

## Часто задаваемые вопросы

http://torrentpier.me/threads/faq-для-новичков.260/

## Где задать вопрос

http://torrentpier.me/forums/Основные-вопросы-по-torrentpier-ii.10/
