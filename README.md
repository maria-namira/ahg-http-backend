# ahg-http-backend
#### Frontend: <a href="https://github.com/maria-namira/ahg-http.git">repository</a>
#### Легенда

Настало время докрутить менеджер картинок, который вы делали на протяжении нескольких лекций. Теперь нужно, чтобы все картинки загружались и хранились на сервере. А при удалении удалялись с сервера.

#### Описание

Напишите серверную часть с использованием 'koa' (по аналогии с тем, как это было на лекции), но докрутите туда:
1. Хранение списка картинок - предложите, как отдавать его на клиент (возможно, JSON?)
1. Удаление картинок с сервера (при нажатии на кнопку удалить с клиента)

<details>
<summary>Подсказка</summary>
    
Делайте удаление методом POST: /?method=removeImage&id=`<id>`
</details>

Напоминаем, как он должен выглядеть:

![](./pic/image.png)

Обратите внимание на несколько важных моментов:
1. Ваш менеджер картинок должен по-прежнему поддерживать drag and drop и загрузку по клику
1. Сервер на Heroku в бесплатной редакции "засыпает", при этом удаляются ваши файлы и то, что хранится в памяти (в этом нет ничего страшного, но это не должно быть для вас сюрпризом)
1. Не загружайте больших картинок (более 1Мб): на всех серверах установлены ограничения, мы для упрощения этот момент опускаем

Вам придётся провести исследовательскую работу и выяснить, как удалять файлы с помощью API NodeJS. Надеемся, что вы справитесь с этим, но дадим небольшую подсказку: https://nodejs.org/api/fs.html

Вы можете реализовать развёртывание в удобном для вас формате: либо так, как это было описано на лекции (отдельно для frontend + GitHub Pages и backend + Heroku), либо собрать frontend и настроить backend так, чтобы он обрабатывал frontend так же, как картинки (см. koa-static с лекции) и развернуть единую сборку на Heroku.

Используйте `FormData` для отправки данных. Авто-тесты к данной задаче не нужны.

В качестве результата пришлите проверяющему ссылку на GitHub репозиторий.
