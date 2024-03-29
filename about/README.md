# Описание Игры

Принцип игры точно такой же как в игре State IO. Игровое поле представляет собой квадрат и состоит из 1000x1000 элементарных единиц (квадратов). Квадрат может как временно, так и постоянно содержать города.

Отсчет начинается с левого верхнего угла (x - 0, y - 0). Вы управляете городами которые принадлежат вам. Города могут нарасчивать силу, так и воздействовать на другие города.

# Механика игры

- Игра управляется внутреигровыми часами, за элементарную секунду берется одна итерация игры - **tick**. За **1 tick** игрок может сделать 1 движение.
- Вы управляете в какой момент времени взаимодействовать на другие города. По умолочанию города создают 1 единицу за **tick** и имеют максимальное количество вмещающихся единиц. Цель игры всегда одна - иметь под контролем все города (для песочницы) или иметь большее влияние на всей территории чем соперник (для арены).

# Технические правила

- Основой бота является бесконечный цикл, на каждой итерации которого ваш бот должен обработать входную информацию с параметрами игры и принять решение о дальнейшем действии.
- Программа должна сначала прочитать все параметры игры (передаются через **stdin**).
- После этого необходимо отдать движение бота в **stdout** ("запринтить" текст с командой)
- На каждую итерацию дается **200 мс**
- Если ваша программа не успевает принять решение за это время или не выдает никаких результатов совсем, ход считается за бездействие.

# Порядок хода

1. Обновление состояния городов
2. Игроки получают состояние карты
3. Ход игрока
