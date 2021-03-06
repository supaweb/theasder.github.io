---
layout: post
title: "Список идей для начинающих программистов по созданию игр-клонов. Часть 1."
date: 2015-04-17 17:54:25
category: projects
tags: [games, novice, ideas, gamedev]
description: "Список идей, с помощью которых можно получить практические навыки программирования."
published: true
---
<img src="https://theasder.github.io/img/pacman.png" class="img-responsive" /><br />

Для тех, кто решил заняться программированием и стремится освоить эту премудрость самостоятельно, существует много источников знаний. Среди них «Invent Your Own Computer Games with Python», а также множество бесплатных книг по программированию для начинающих. Но что такое теоретические знания без практики? Половина дела. Чтобы улучшить навыки в написании кода, нужны проекты с открытым исходным кодом, желательно на соответствующем уровне или просто «для чайников», которые позволят испытать себя в деле и вживую увидеть результаты своего труда.

Предлагаем вашему вниманию список идей для игр-клонов, с помощью которых можно получить практические навыки программирования. Каждая из них сопровождается кратким описанием игры, ссылками на видео геймплея и описанием тех алгоритмов, которые необходимы для работы с ней. Эти игры были отобраны за их простоту, так что с ними вполне сможет справиться и новичок. Кроме того, для освоения каждой из них потребуется совсем немного времени, примерно один уик-энд для каждой. Конечно, создать клон Mario или Zelda будет сложно, но клоны Tetris или Asteroids как раз то, что нужно.

## Orisinal Games:
Сайт [Orisinal](http://www.ferryhalim.com/orisinal/) предлагает большую коллекцию флеш игр с очень простой механикой, которые могут быть скопированы. 

Особенно удачной являются игры Winter Bells, A Daily Cup of Tea, Bugs и Hold the Rope.

Также идеи для игр-клонов можно [найти в Википедии](http://en.wikipedia.org/wiki/Video_game_clone# Notable_cloned_games).
Подробнее об играх для начинающих программистов можно узнать из бесплатных книг по программированию на Python - «Invent Your Own Computer Games with Python» и «Making Games with Python & Pygame». Все они с открытым исходным кодом и являются отличным материалом для новичков.


## 1. Dodger

*Описание*: «Плохие парни» падают с верхней части экрана, и игрок должен избежать встречи с ними. Управление героем игры осуществляется с помощью клавиш со стрелками или при помощи мыши. Чем позже состоится встреча героя с хулиганом, тем выше балл, заработанный в ходе игры.

*Варианты*: можно задать, чтобы хулиганы падали с разной скоростью и были различных размеров. Можно также сделать, чтобы они появлялись не только с верхней, но и с боковых сторон экрана. Одним из вариантов может быть наделение героя неуязвимостью на некоторое время, например, за достижение определенного количества баллов, замедление скорости падения “плохих парней” и т.д.

Эта игра описана в главе 20 книги [«Invent with Python»](http://inventwithpython.com/chapter20.html)

## 2. Memory Puzzle

*Описание*: Экран заполнен картами, лежащими рубашкой вверх. Для каждой из карт существует пара. Игрок переворачивает карты попарно. Если они совпадают, они остаются перевернутыми (открытыми). В противном случае они возвращаются в исходное положение. Игрок должен перевернуть все карты за наименьшее количество ходов (за меньшее время), чтобы набрать больше баллов.

*Варианты*: Можно снабдить игрока «подсказками», указывая на четыре карты из которых одна является парой только что вскрытой. Или, например, в начале игры на короткое время открыть все поле, чтобы игрок попытался запомнить как можно больше соответствий за это время.

Эта игра описана в главе 1 книги [«Making Games with Python & Pygame»](http://inventwithpython.com/pygame/chapter1.html)

## 3. Sliding Puzzle

*Описание*: Эта игра является аналогом всем известной головоломки «Пятнашки» или 15-puzzle. На поле размером 4x4 клетки находятся пронумерованные плитки в количестве 15 штук и одно свободное пространство. Чтобы выиграть игру, игрок должен передвигая плитки, поставить их в порядке возрастания.

*Варианты*: Числа можно заменить фрагментами изображения, превратив игру в складывание паззла.

Эта игра описана в главе 4 книги [«Making Games with Python & Pygame»](http://inventwithpython.com/pygame/chapter4.html)

## 4. Simon

*Описание*: Четыре цветные кнопки загораются по определенной схеме. После показа картинки, игрок должен повторить рисунок, нажав на кнопки в соответствующем порядке. Рисунок становится больше каждый раз, когда игрок правильно завершает картину. Если игрок нажимает не ту кнопку, игра заканчивается.

*Варианты*: Можно использовать поле с девятью кнопками, однако, эта версия игры может быть утомительной (согласитесь, трудно запомнить порядок, состоящий из девяти элементов).

Эта игра описана в главе 5 книги [«Making Games with Python & Pygame»](http://inventwithpython.com/pygame/chapter5.html)

## 5. Nibbles

*Описание*: червь или змея постоянно движется по экрану, управляемая игроком при помощи кнопок со стрелками. По ходу движения «змея» должна попытаться съесть яблоки, которые случайно появляются на поле. Чем больше яблок, тем длиннее становится «змея». Игра заканчивается, когда «змея» достигает края игрового поля или «кусает сама себя».

*Варианты*: На поле можно добавить препятствия в виде участков стен, рисунок которых будет усложняться из уровня в уровень. Можно также использовать различные виды бонусов, при «поедании» которых будет прибавляться различное количество очков. Можно ввести в игру предмет, подобрав который «змея» может укоротиться в два раза. Можно добавить движущиеся предметы, встречи с которыми «змея» должна избегать. Можно использовать два червя, которыми игрок должен управлять одновременно. Ниже представленная игра Tron является вариантом Nibbles для двух игроков.

Эта игра описана в главе 6 книги [«Making Games with Python & Pygame»](http://inventwithpython.com/pygame/chapter6.html)

## 6. Tetris

*Описание*: Фигуры из четырех блоков падают с верхней части экрана. Игрок должен складывать из них заполненные линии, вращая и перемещая их. Когда игроку удается составить полный ряд, он исчезает, а вся конструкция опускается вниз. Игра заканчивается, когда игровое поле будет заполнено доверху.

*Варианты*: несколько вариантов Tetris описаны в [Википедии](http://en.wikipedia.org/wiki/List_of_Tetris_variants)

Эта игра описана в главе 7 книги [«Making Games with Python & Pygame»](http://inventwithpython.com/pygame/chapter7.html)

## 7. Katamari Damacy
*Описание*: Оригинальная игра Katamari Damacy разработана в 3D-варианте, но создать ее 2D-версию не представляет труда. Игрок управляет небольшим предметом в мире, где находятся объекты различных размеров. Прикосновение предмета, управляемого игроком, к более мелким объектам прибавляет очки и увеличивает его в размерах, касаясь же более крупных объектов, предмет игрока сжимается. Игрок выигрывает, или проигрывает, когда его предмет достигает определенного размера (большого или маленького).

Как происходит игра в 2D Katamari можно посмотреть в ее [флеш-версии](http://dagobah.net/flash/katamari.swf)

Эта игра описана в главе 8 книги [«Making Games with Python & Pygame»](http://inventwithpython.com/pygame/chapter8.html)

## 8. Sokoban

*Описание*: логическая игра-головоломка, в которой игрок передвигает ящики по лабиринту, показанному в виде плана, с целью поставить все ящики на заданные конечные позиции. Только один ящик может быть передвинут за раз, причём герой игры — «кладовщик» — может только толкать ящики, но не тянуть их. Эта игра требует некоторых усилий по разработке новых уровней, но  их примеры можно найти в интернете.

*Варианты*: В игру можно добавить различные виды трюков: телепортационные плитки, конвейерные ленты, кнопки, открывающие двери или наводящие мосты, кнопки, на которые нужно установить ящик, чтобы дверь оставалась открытой, пока в нее будут выталкиваться другие ящики и т.д.

Эта игра описана в главе 9 книги [«Making Games with Python & Pygame»](http://inventwithpython.com/pygame/chapter9.html)


## 9. Othello

*Описание*: В игре используется квадратная доска размером 8 × 8 клеток и фишки белого и черного цвета. Это игра для двух игроков, которая также известна как «Риверси», и осуществляется по ее [правилам](https://ru.wikipedia.org/wiki/%D0%A0%D0%B5%D0%B2%D0%B5%D1%80%D1%81%D0%B8).

*Варианты*: В игру можно добавить, например, третьего игрока со своим цветом фишек или изменить число квадратов игрового поля.
Эта игра описана в главе 10 книги [«Making Games with Python & Pygame»](http://inventwithpython.com/pygame/chapter10.html) 

