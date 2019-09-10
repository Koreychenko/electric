# electric
Игра электрик на Symfony и vue.js

Изначальное техническое задание:
https://docs.google.com/document/d/1gKO4MFdgjixwY0tKn2Qsnr12WcOfgi8-XqxCLSDLG14/edit#heading=h.sei4c8b2jw0k


## Задание
Разработать игру “Электрик”.

Игра визуально похожа на известную игру “Выключите свет”, например из состава GNOME Games. Однако, эта игра обладает другими правилами переключения света и дополнена случайными переключениями.

## Описание игры
Игра проходит на поле 5х5 ячеек, где каждая ячейка представляет собой “лампочку”. “Лампочка” может иметь два состояния: “Горит” и “Не горит”. “Электрик” (т.е. игрок) кликом на любую ячейку-”лампочку” переводит ее в состояние “Горит”, при этом, все близлежащие “лампочки” (включая диагональные) меняют свое текущее состояние на противоположное. Для дополнительной сложности после каждого хода с шансом 1 к 25 может погаснуть одна любая лампочка. После каждого хода, увеличивается счетчик ходов.
Цель игры
Сделать так, чтобы все лампочки горели одновременно за минимальное число ходов. (Конечно, это очень условно. Игра очень простая, а случайные переключения делают игру не спортивной)
Выигрыш
Если “электрик” справился с заданием, то появляется диалоговое окно, где ему показывают его количество ходов и предлагают ввести имя. По нажатию на “ОК”, его имя и результат сохраняется в БД.
Лучшие результаты
Сделать кнопку, по нажатию на которую, появляется диалоговое окно со списком 10 лучших “электриков”, которые справились за минимальное число ходов. С сортировкой по местам, конечно же.
Требования к реализации
Графический интерфейс приведен для примера. Сама игра должна точно соответствовать описанию. Обработка выигрыша и лучшие результаты опциональны (ниже есть пункт). Ниже представлен список технических требований, из которого нужно выбрать те, которые Вы выполните. Выбирайте требования, которые считаете наиболее значимыми, чтобы продемонстрировать свои навыки. 

Важно! Вам нужно выбрать те требования, которые Вы точно выполните и прислать их список до того как возьметесь выполнять задание. Те требования, которые Вы не пришлете не будут учитываться при проверке. Но те требования, которые Вы пришлете, нужно будет выполнить обязательно.

Список требований:
* Интерфейс сделать на react или vue. Ячейки должны быть блоками (div-ами, а не canvas-ом или таблицей).
* Должна быть анимация включения и выключения “лампочки”. Анимация должна быть на CSS.
* Должно быть приятно глазу, но без заморочек.
* Счетчик ходов сделать “электронными” цифрами (как на картинке).
* Расчет какая лампочка загорается и гаснет должен происходить на backend.
* Для backend использовать Symfony 4.
* Не использовать Angular :-)
* Блокировать мошенничество: подмену количества ходов, выигрыш, состояние лампочек.
* Сохранять текущий прогресс игры и сделать кнопку начала новой игры. (Без этого пункта, нужно чтобы новая игра запускалась по обновлению страницы.)
* Обновление состояния лампочек и счетчика ходов должно происходить без перезагрузки страницы.
* Реализовать сохранение лучших результатов.
* Для хранения в БД использовать Doctrine ORM.
* Если “Электрик” побеждает второй раз, подставлять его имя в форму победителя автоматически.
* Покрыть тестами код backend.
* Покрыть тестами код frontend.
* Сделать функциональные тесты на Selenium.
* Код должен быть в git репозитории одного из: GitHub, GitLab, Bitbucket.
* Должна быть история коммитов, где видно как игра разрабатывалась. Это очень, очень желательный пункт.
* Сделать Vagrantfile или Dockerfile или Docker Compose, чтобы с одной команды запустилось все нужное.
