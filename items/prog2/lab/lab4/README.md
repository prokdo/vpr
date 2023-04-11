# Лабораторная работа #4

## Вступление

Все классы, созданные по нижеприведенным заданиям, должны
размещаться в пакетах (например, `lab4.car`, `lab4.complex`).

Так как много больших математических формул в описании заданий, то я их сократил до минимального вида. Полное задание в методичке

## Работа

### Задание 1
Создайте класс Car, представляющий понятие
"автомобиль". Каждый автомобиль должен иметь, как минимум,
следующие характеристики: регистрационный знак, марка, вид, цвет,
мощность двигателя, количество колес. Для вновь созданного,
конкретного автомобиля такие характеристики как марка, вид, цвет,
мощность двигателя, количество колес должны быть заданы
непременно, но регистрационного номера у него до поры до времени
может и не быть (а может и быть). Все характеристики автомобиля,
кроме марки, вида и количества колес можно изменять в процессе его
эксплуатации. Вид автомобиля - легковой, грузовой, автобус. Создайте
и используйте для задания вида автомобиля перечислимый тип. Для
легковых, грузовых автомобилей и автобусов с нормальным
креплением знака (тип 1) согласно ГОСТ Р 50577-2018 [6] знак имеет
следующий формат: X 000 XX 00 RUS или X 000 XX 000 RUS. Здесь 0 в
реальном знаке заменяется какой-то арабской цифрой, а X - одной из
12 букв кириллицы (в верхнем регистре), написание которой совпадает
с написанием латинской буквы: А, В, Е, К, М, Н, О, Р, С, Т, У, Х. Попытка
задания неправильного знака должна пресекаться соответствующим
методом класса. Для проверки используйте регулярное выражение.
Создайте код для тестирования класса Car с заданием начальных
характеристик, запросом новых значений для тех характеристик,
которые можно изменять и выводом на экран текущих значений всех
характеристик.

```java
```


##### Вывод
```bash

```


### Задание 2
В Java отсутствует стандартный класс для представления
комплексных чисел. Создайте такой класс (Complex), поддерживающий
операции получения действительной, мнимой частей числа, сложения,
вычитания, умножения, деления, комплексного сопряжения, проверки
двух чисел на равенство, вывода значения комплексного числа в
алгебраической и тригонометрической формах. Так как действительное
число, это комплексное число с нулевой мнимой частью, должны
поддерживаться также арифметические операции, в которых один из
аргументов действительное число (тип double).


```java
```


##### Вывод
```bash

```

### Задание 3
Реализуйте методы для вычисления элементарных
функций комплексного переменного z = ..., 
sin(z) = ..., cos(z) = ..., tan(z) = ..., arctan(z) = ...
sh(z) = ..., ch(z) = ..., , th(z) = ..., cth(z) = ...
Формула Эйлера: `e^(i*x) = cos(x)+i*sin(x)`, `x` - действительное число.
Организуйте методы так, чтобы их можно было вызывать, не создавая
объекты класса, которому принадлежат эти методы. Прежде чем писать
код, ответьте себе на вопрос, должны ли эти методы быть методами
класса Complex, созданного в предыдущем задании?

```java
```


##### Вывод
```bash

```

### Задание 4
В Задании 1 двигатель автомобиля представлен только
одной своей характеристикой - мощностью. А самом деле каждый
двигатель имеет серийный (заводской) номер, и, помимо мощности,
рабочий объем, расход топлива, вид топлива, число цилиндров и т.д.
Поэтому для такого важного понятия удобно ввести отдельный класс.
Создайте класс Engine, включив в него несколько важных характеристик
двигателя и методы доступа к этим характеристикам. Определите и
реализуйте нужный конструктор (или конструкторы) класса Engine.
Замените в классе Car поле "мощность" на поле "двигатель" (engine).
Измените код тестирования для проверки работоспособности новой
версии класса Car и класса Engine.

```java
```


##### Вывод
```bash

```

### Задание 5
В Заданиях 1, 4 вид автомобиля задается как
предопределенное значение. Появление новых видов будет приводить
к необходимости модифицировать класс Car. Кроме того, для новых
видов автомобилей правила формирования регистрационного знака
могут быть другими. Более гибкое решение - каждый вид автомобиля
представлять собственным классом. С другой стороны, все автомобили 
будут обладать одинаковым набором некоторых базовых
характеристик. Не разумно при возникновении нового вида автомобиля
всякий раз повторять в нем объявления этих базовых характеристик и
определять методы доступа к ним. Нужно использовать семейство
родственных классов, в котором один (Car) будет содержать все общие
характеристики, а другие - классы для конкретных видов автомобилей
дополнительные характеристики и/или конкретные значения для
базовых характеристик. Измените нужным образом класс Car, создайте
классы для следующих видов автомобилей: легковой, грузовой,
автобус, специальный (например, пожарная машина, или автомобиль
для дипломатических миссий). Для специальных автомобилей
придумайте свою схему формирования регистрационного знака (или
возьмите из ГОСТ Р 50577-2018 [6]).

```java
```


##### Вывод
```bash

```

### Задание 6
. В Задании 5 класс Car содержит общую функциональность
семейства автомобилей разных видов, но не представляет какие-то
конкретные автомобили. Не логично разрешать пользователям
создавать в программе экземпляры класса Car. Кроме того, некоторые
методы доступа к базовым характеристикам автомобиля, заданные в
классе Car не должны переопределяться в классах-наследниках. Если
это будет сделано случайно или преднамеренно, изменится базовое
поведение некоторых автомобилей, а этого не должно происходить по
логике организации семейства классов автомобилей. Нужно запретить
наследникам переопределять такие методы базового класса. Наконец,
нужно задаться вопросом, насколько расширяемой должна быть наша
система родственных классов. Например, есть ли какие-то особые
формы автобусов, для которых нужно построить класс-наследник
имеющегося класса? А для других классов, представляющих
автомобили? Сделайте так, чтобы, по крайней мере, класс
представляющий автобусы нельзя было расширять.

```java
```


##### Вывод
```bash

```

### Задание 7
Создайте класс "Автобаза". На базе может размещаться
некоторое фиксированное количество автомобилей разных видов
(классы производные от Car). Для хранения объектов, представляющих
автомобили нужно использовать массив фиксированного размера.
Максимально возможный размер для конкретной автобазы (конкретного
объекта класса) задается при создании объекта. Каждый автомобиль
может находиться в одном из трех допустимых состояний: на базе, в
рейсе, в ремонте. Нужно обеспечить добавление нового автомобиля
(если еще есть место для размещения автомобиля). Удаление 
30
(списание) автомобиля. Отправку исправного автомобиля в рейс.
Отправку неисправного автомобиля в ремонт. Возврат автомобиля из
рейса или из ремонта. Отображение на экране списка находящихся на
базе исправных автомобилей, списка автомобилей, находящихся в
рейсе, списка неисправных автомобилей (отдельные методы). 

```java
```


##### Вывод
```bash

```

### Задание 8


 Средство построения графиков функций может
генерировать рисунки подобные следующему. Отвлекаясь пока от
графического изображения спроектируйте
систему классов для решения такой задачи
в объектно-ориентированном стиле (в виде
UML-диаграммы классов). Каждое важное
понятие задачи нужно представить
собственным классом. Например, на
рисунке есть собственно весь график, на
нем отдельные кривые, оси координат,
координатная сетка, пояснения. Это все
важные понятия в решаемой задаче.
Каждый класс отвечает за свой функционал. В частности, каждый класс
отвечает за прорисовку своих объектов. Определите, какие параметры
должны хранить соответствующие классы, какие у них должны быть
методы и изобразите на UML-диаграмме классов сами классы, их поля
и методы, отношения между классами.

```java
```


##### Вывод
```bash

```

### Задание 9
Создайте классы для построенной в Задании 7 UMLдиаграммы классов. Вместо реального рисования нужно обеспечить
вывод на экран текстовой информации со значениями параметров
объектов соответствующих классов.

*Библиотека графического пользовательского интерфейса AWT предлагает
использовать в качестве главного окна программы объект класса Frame. Frame
представляет окно с полосой заголовка на которой, помимо заголовка,
размещаются также элементы управления для сворачивания окна,
разворачивания его на весь экран и закрытия окна, рамкой, позволяющей
нужным образом изменять размеры окна и рабочей областью, которая является
контейнером, то есть может содержать другие элементы пользовательского
интерфейса. Для рисования в AWT есть класс Canvas ("полотно"). Этот класс
представляет подчиненное окно без заголовка и рамки. Можно разместить
объект Canvas в рабочей области Frame так, чтобы "полотно" занимало всю
рабочую область. Чтобы Canvas всегда занимал всю рабочую область Frame
нужно при изменении размера Frame соответствующим образом изменять и
размер Canvas. AWT предлагает стандартные менеджеры размещения
(компоновки) которые берут на себя задачу изменения размеров элементов
управления, размещенных в окне Frame. При этом возможны разные варианты
изменений размеров, только по горизонтали, только по вертикали и более
сложные. Например, менеджер компоновки BorderLayout позволяет так
разместить элемент управления в окне, чтобы "подстраивались" одновременно
и ширина, и высота Canvas.*

```java
```


##### Вывод
```bash

```


*Авторство: **Бояршинов Н.О***