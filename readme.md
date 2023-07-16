Задание: 

🧩Сделайте веб-страницу на которой необходимо отобразить оптимальный способ расположения коробок на стеллаже (чтобы коробки занимали наименьшее количество полок). 

Дано: 
Стеллаж, длиной 1310 мм. На каждой горизонтали одна полка во всю длину. 
8 коробок с соответствующей длиной (мм): 774, 214, 694, 321, 674, 527, 120, 567. 
Глубина и высота не учитываются. Количество полок не регламентировано. 

Отобразите на поверхности коробки её порядковый номер и длину, либо визуализируйте результат иным способом. 

Подробнее: 

Напишите алгоритм, который расставит коробки идеальным образом(с минимальным колличеством полок). 
Набор исходных данных не статичен. 
Желательно сделать в интерфейсе поля для пользовательского ввода кол-ва коробок, их длины и длины полки.
Чтобы можно было протестировать алгоритм на разных входящих данных.

-----------------------------------------------------------------------------------------------------

Реализация (этапы):

1. Создание/продумывание алгоритма;
2. Создание интерактивной панели для ввода данных пользователем (с кнопками добавить, удалить, подтвердить);
3. Получение данных пользователя через input value. Работа с статичным полем input и нестатичным n-кол-вом;
4. Создание дизайна (шкаф, полки) на основе данных пользователя. 
5. Доработка дизайна / создание проверок / описание задач и собственной реализации ТЗ

---------------------------------------------------------
1. Алгоритм.
Создание алгоритма на основе сортировки входящих данных от большего к меньшему. -> Пробежка по массиву данных в поиске подходящих значений, чтобы конечная сумма всех значений не превышала знечение длины полки. -> Все выбранные значения попадают в другой массив (полка), из массива заданных пользователем значений убираются. -> Как итог, работаем с оставшимися данными, распределяем по полкам. Работаем до момента, когда массив данных пользователя станет пустым. 

2. Надписи.
Title - при наведении на коробку показывает ее длину. 

3. Шкаф / полки. (Максимальная ширина шкафа - 2500мм или 2.5м), специально поставила ограничения!
Подобран шкаф, который был подставлен, как background-image и задан размер, чтобы коробки попадали ровно на полки шкафа. Картинка шкафа обработана в редакторе для максимально подходящего размера и чтобы коробки попадали на полки при большом количестве коробок. Шкаф расширяется и растет в высоту. Видно, когда на полке еще остается свободное место. Ширина шкафа подобрана под длину полки. Между полками создано расстояние, чтобы коробки попадали на полки.

4. Интерактивная таблица.
Создана и.таблица, позволяющая вводить 4х-значные данные.
Важно, чтобы длина полки не была меньше длины самой большой коробки. Кнопка "подтвердить" создает шкаф с полками и коробками. Есть кнопки удалить. Кнопка Reset - перезагружает страницу, дает возможность вводить данные снова.

5. Проверки:
- Размер полки дб больше, чем размер бОльшей коробки;
- Если полки не добавлены, добавляем;
- Вводимые данные должны быть числовыми.


UPDATES:

1. Добавлено поле для ввода параметров коробки. Присутствует изначально вместе с длиной полки. 
2. Проверка на негативные числа.