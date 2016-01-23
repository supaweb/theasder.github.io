---
layout: post
title: "Что полезно знать о дате, времени и часовых поясах в процессе разработки"
date: 2016-01-23 22:00:00
category: development
tags: [time, development, programming, unix, високосные секунды, летнее время, часовые пояса, время, системные часы, unix-время в программировании, високосные секунды в программировании, летнее время в программировании, часовые пояса в программировании, системные часы в программировании, время в программировании, часовые пояса в программировании]
author: "Софья Лепёхина"
published: true
---

<img src="https://theasder.github.io/monitor.jpg" class="img-responsive" /><br />

Основные сведения, которые полезно знать каждому программисту.

<!-- more -->

##Часовые пояса: основные понятия

* **UTC** (Universal Coordinated Time): Время на нулевом градусе долготы (нулевой меридиан) называется Всемирное координированное время. UTC &mdash; это нейтральный вариант между французским TUC и английским CUT.

* **GMT** (Greenwich Mean Time): вместо UTC раньше использовалось Среднее время по Гринвичу (GMT), поскольку нулевой меридиан проходил через Гринвичскую королевскую обсерваторию.

* Другие часовые пояса могут быть выражены как смещение от UTC. Например, Австралийское восточное стандартное время (EST) выражается как UTC+1000, т.е. 10:00 по UTC &mdash; это 20:00 по EST одного и того же дня.

* **Летнее время** не влияет на UTC. Это просто политическое решение об изменении времени (смещение от UTC). Например, GMT до сих пор используется: это британское национальное время в зимний период. Летом оно становится BST.

* **Високосные секунды**: По международному соглашению, UTC (который является произвольным человеческим изобретением) держится в 0,9 секундах от физической реальности (UT1, который измеряется по солнечному времени) с помощью введения «високосной секунды» в последнюю минуту года по UTC или в последнюю минуту июня.

* Високосные секунды не обязаны быть объявлены более, чем за 6 месяцев до их введения. Это может стать проблемой, если вам нужно спланировать все до секунды на срок более 6 месяцев.

* **Unix-время**: измеряется количеством секунд с эпохи (начало 1970 года по UTC). На Unix-время не влияют часовые пояса или летнее время.

* В соответствии с POSIX.1, для Unix-времени предполагается  обрабатывать високосную секунду повторением предыдущей секунды, например:

59.00

59.25

59.50

59.75

59.00 ← повторение

59.25

59.50

59.75

00.00 ← инкремент

00.25

Это компромисс: вы не можете выразить високосную секунду, и ваше время точно пойдет в обратную сторону. С другой стороны, каждый день равен точно 86,400 секундам, и вам не нужна таблица всех прошлых и будущих високосных секунд для того, чтобы форматировать Unix-время в удобное для человека часы-минуты-секунды.

##Что важно знать разработчику о времени

* Часовые пояса относятся к уровню презентации.
Большинство кода не относится к часовым поясам или к местному времени, оно должно передавать Unix-время.

* При записи момента времени, измеряйте Unix-время. Это UTC. Так легче, потому что оно не имеет часовых поясов или летнего времени (или високосных секунд).

* При хранении времени, храните Unix-время. Это одно число.

* Если вы хотите сохранить читаемое время (например, в логах), то рекомендуется сохранять его вместе с Unix-временем, а не вместо него.

* При отображении времени, всегда добавляйте смещение времени. Формат времени без этого бесполезен.

* Системные часы неточны.

* Вы в сети? Любые другие системные часы по-своему неточны.

* Системные часы могут и будут прыгать вперед и назад во времени из-за вещей вне вашего контроля. Ваша программа должна быть разработана так, чтобы пережить это.

* Количество секунд часов к количеству настоящих секунд неточно и может изменяться. Это зависит, в основном, от температуры.

* ntpd может изменять системное время двумя способами:

  * Шаг: часы перепрыгивают назад или вперед на нужное время мгновенно.

  * Подкручивание: изменение частоты часов так, что они медленно сдвигаются в сторону нужного времени.

Способ подкручивания является более предпочтительным, потому что он менее разрушителен. Но подкручивание полезно только при коррекции небольших отклонений.

##Специальные замечания

* Високосные секунды случаются чаще, чем високосные годы.

* Время проходит со скоростью в одну секунду за секунду для каждого наблюдателя. Частота удаленных часов по отношению к наблюдателю зависит от скорости и гравитации. Часы внутри спутников GPS регулируются для преодоления [релятивистских эффектов](https://ru.wikipedia.org/wiki/Релятивистское_замедление_времени).

* MySQL хранит DATETIME в виде "YYYY-MM-DD HH:MM:SS"

* Также существует тип TIMESTAMP, который хранится как Unix-время, но имеет свои особенности.

<b>В заключение:</b> если вы задумываетесь о хранении отметок времени в MySQL, храните их как целые числа и используйте функции UNIX_TIMESTAMP() и FROM_UNIXTIME().

Перевод: Софья Лепёхина

[Источник](https://unix4lyfe.org/time/?v=1)