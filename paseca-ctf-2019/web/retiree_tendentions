# Retiree Tendentions

  - Category: **web**
  - pozhiloy, author: @lbezvershenko

> Retiree people are slightly coming to the business these times, so Lil Granny opened her own honey shop. 
> She is also selling an old flag, which I really want to get for my collection. Can you buy it for me? 

> task.pase.ca:24068

### Write-up

Заходим на сайт, видим что мы можем покупать товары за баланс.
Также можно скачивать картинки по адресу

> http://task.pase.ca:24068/download?image=1.jpg

Пробуем lfi, скачиваем файл /proc/self/environ

> http://task.pase.ca:24068/download?image=/../../../../../../proc/self/environ

Видим в нём строчку SECRET_KEY=T6D_?Bhh]Dt_}*3uK)!4UkJObT}T-7ztv]Wg_vlPF9aUa!Pj#r.
Замечаем что информация о балансе и покупках пользователя хранится в куке с названием session в виде jwt токена.
Пробуем расшифровать, получаем

> {"balance": 1336,"purchases": []}

Создаём новый токен, подписанный уже известным нам секретным ключём с header равным

> {"balance": 1337,"purchases": []}

Заменяем куку, получаем 1337 баланса и покупаем флаг.
