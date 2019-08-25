# Horse Bank

  - Category: **web**
  - author: @kumfc

> Did you know, that the best friends of bees are horses. And, suddenly, we have no horses on our apiary. Can you bring us some?

> task.pase.ca:24065

**Hint:**
> What would be better, than a multi-task banker? Or not...

### Write-up

Открываем сервис, регистрируемся, видим что мы можем покупать алмазные блоки, но нам немного не хватает до флага.
Смотрим ещё раз на название таска, понимает что это race condition, авторизуемся с одного аккаунта в нескольких сессиях и одновременно со всех отправляем множество запросов на покупку алмазных блоков.
Как результат получаем -10rub и 10DB на балансе, покупаем флаг.
