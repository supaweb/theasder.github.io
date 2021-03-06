---
layout: post
title: "Как понять, что пишешь читабельный и легко поддерживаемый код?"
date: 2015-04-09 12:03:28
category: development
tags: [code, keep-it-simple-stupid, coding]
description: "Советы и принципы, которые помогут определить уровень читабельности кода."
published: true
---
<img src="https://theasder.github.io/img/wtfm.jpg" class="img-responsive" /><br />

Скорее всего, когда вы пишите код, вам он понятен на данный момент, но мы должны быть честными по отношению к себе. Так как понять, что мы пишем грязный и неподдерживаемый код? Существуют ли конструкции или руководящие принципы для ответа на данный вопрос?

* Вы можете попросить посмотреть то, что вы написали кого-то еще, чтобы узнать мнение другого человека по поводу вашего кода.
* Посмотреть на свой код через шесть месяцев и попытаться понять, что вы написали. Если поняли быстро, то код читабелен.
* Ваш код поддерживаемый, если вы можете поддержать(см. предыдущий пункт); легко поддерживаемый, если кто-то еще может его поддерживать, не спрашивая у вас помощи; читабельный, если кто-то, прочев ваш код, правильно понял дизайн, макет и идею.
* Если код соответствует принципам [SOLID](https://ru.wikipedia.org/wiki/SOLID_(%D0%BE%D0%B1%D1%8A%D0%B5%D0%BA%D1%82%D0%BD%D0%BE-%D0%BE%D1%80%D0%B8%D0%B5%D0%BD%D1%82%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D0%BE%D0%B5_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5)) и [DRY](https://ru.wikipedia.org/wiki/Don%E2%80%99t_repeat_yourself), а также имеет хороший ряд юнит-тестов, то вероятнее всего, код поддерживаем.
* В книгах Р. Мартина «Чистый код», А. Александреску «Стандарты программирования на С++», М. Фаулера «Рефакторинг. Улучшение существующего кода», С. Макконелла «Совершенный код» имеется большой список критериев, чтобы оценить ваш код, такие как разумные названия, размер кода функции, связность и сплоченность, дизайн объектов, юнит-тестирование и т.д. Вам достаточно просмотреть книги и найти несколько ключевых моментов, на которых сосредоточить свое внимание.
* Воспользоваться существующими мерами сложности кода, ведь между сложностью кода и читабельностью/поддерживаюмостью корреляция довольно высока. Существует несколько способов вычислить сложность кода, один из них это [цикломатическая сложность программы](https://ru.wikipedia.org/wiki/%D0%A6%D0%B8%D0%BA%D0%BB%D0%BE%D0%BC%D0%B0%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F_%D1%81%D0%BB%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D1%8C): вам следует посчитать количество все возможных «маршрутов» (это могут быть разветвления в виде if-ов) через вашу программу. Так вот значением меры будет количество строк кода, поделенного на количество этих «маршрутов». Однако, эта мера не лишена уязвимости: мы можем написать 300 строчек кода и в коде нет ни одного условия, то наверняка нарушен принцип «Не повторяйся», что не очень хорошо. Таким образом, в дополнение к цикломатической сложности программы следует проверять код на наличие дупликатов в нем.
* Опыт в развитии каких-либо проектов, в том числе open-source проекты поможет вам не допускать ошибок.
* Ответьте на эти вопросы:

    * Выйдите из IDE. Можете ли вы прочесть свой код? Легко ли найти ошибку в коде и поставить брейкпоинт в нужном месте, чтобы понять, где проблема?
    * Превратится ли отладка программы в игру, где исправление каждого бага приведет к появлению еще нескольких?
    * Сколько файлов вам приходится открывать, чтобы добавить обычный новый метод к классу?
    * Подумайте над шаблонами и практиками разработки, которые вы использовали. Использовали ли вы их, потому что прекрасно понимали зачем или потому что вы задавались вопросами «это единственный способ реализовать это?» или вы хотели добавить в свое резюме или потому что какой-то крутой разработчик вам так посоветовал.
    * Сможете ли вы этот код или часть его использовать еще раз в дальнейшем в каком-либо еще проекте?
