# Jocker Gallery

  - Category: **web**
  - kphp, author: @kumfc

> Department of stooped dogs tried to make a new gallery module for bee social network.
> But seems like they made a grave mistake. Again.

> task.pase.ca:24041

### Write-up

Открываем сайт, видим галерею из множество миниатюр картинок в base64, при нажатии с адреса http://task.pase.ca:24041/al_photos.php подгружается ссылка на полную версию.
Замечаем что id картинок идут по порядку, но пропущен 16776, пробуем отправить запрос с этим айди, на что получаем 

> {"error": 20, "error_text": "Access Denied"}

Учитывая что id 16775 загружается нормально, пробуем отправить запрос с нецелым числом:

> al=1&id=16776.1

Получаем в ответ ссылку на флаг.
