
# Robots
Библиотека для начального обучения Python. Аналог исполнителя "Робот" в Pascal.
## Возможности

 1. Прохождение уровней из библиотеки
 2. Создание своих уровней в конструкторе
 3. Создание уровней с рандомной генерацией при помощи кода
## Установка
### Установка через pip
``pip install -i https://test.pypi.org/simple/ projectRobot``
### Установка вручную
 1. Клонируем репозиторий
 2. Импортируем файл robot.py
## Пример кода
```python
from robots.robot import *

level_name = 'a1'
field = Field(level_name)

red_robot = field.init_robot('red')
while red_robot.free_from_right():
    red_robot.right()
    if red_robot.wall_from_down():
        red_robot.paint()
red_robot.down()

blue_robot = field.init_robot('blue')
while blue_robot.free_from_right():
    blue_robot.right()
    if blue_robot.wall_from_up():
        blue_robot.paint()
blue_robot.up()

field.done()
```
## Презентация проекта
[Открыть в браузере](https://www.beautiful.ai/player/-MfcwzFT0X8b-WW3OkMS)
