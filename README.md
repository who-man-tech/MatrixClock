# MatrixClock
Clock based on the matrix max 7219

# Часы основанные на матрице с чипами max7219

- Одна матрица имеет размеры 8x8, таких матриц - 4.

**Основные функции**
- Вывод времени на матрицу.
- Вывод температуры и давления.
- Режим пониженного потребления энергии.
- Сохранение времени, даже если часы разрядились.

____

- Управление происходит при помощи трех сенсорных кнопок.
- Имеется батарея, следовательно пользоваться данными часами
    можно, как от разетки, так и без нее.


# Режимы использования часов
За управление дисплеем и получением данных отвечает булевая. Если она активна, то получаем данные и дисплей работает. Управление данной булевой происходит в режимах потребления, приведенных ниже. 

**Power mode**
Данный режим предназначен для использования часов от розетки. 
В этом режиме экран всегда включен. Выключение происходит только, когда время больше 00:00 и датчик освещения показывает, что свет в комнате выключен. Если экран выключен, но датчик света показывает, что есть свет, то включаем дисплей. Затем, если свет выключится часы опять уйдут спать. Если центральная кнопка была нажата, то экран включится и если в течении 15 минут мы не будем ничего нажимать, часы уйдуть спать. 
Данный режим является самым потребляемым. 

**Normal mode**
В голове у автора не нашлось классной идеи для этого режима, но данный режим нужен(интуиция подсказывает).

**Eco mode**
Данный режим максимально экономит энергию, предназначен для использования часов от батареи. Наследуется от Power mode, но имеется несколько отличий. Дисплей включен, если инфракрасный датчик зафиксировал движение. Часы включаться на 15 мин и если движений не будет, то они выключаться. 
 

Все режимы работают сами по себе, пока любая из кнопок не будет нажата. Если кнопка была нажата, то мы переходим в активный режим. Если ни каких  действий не происходит, то через 15 минут, выходим из активного режима 
