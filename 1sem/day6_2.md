# 6 день. Системы программирования

- [d10. Нотация Дейкстры](https://mai-806.github.io/fund-wiki/1sem/day10.html) <--> [d11. Типы данных](https://mai-806.github.io/fund-wiki/1sem/day11.html) <--> [d12. Файлы, блоки](https://mai-806.github.io/fund-wiki/1sem/day12.html) <--> [d13. Критика фон Неймана, рекурсия](https://mai-806.github.io/fund-wiki/1sem/day13.html)

- [d1. Раскладки клавиатур, кодировки](https://mai-806.github.io/fund-wiki/1sem/day1.html) <--> [d6. Системы программирования](https://mai-806.github.io/fund-wiki/1sem/day6_2.html) <--> [d9. Железки (1-12)](https://mai-806.github.io/fund-wiki/1sem/day9.html) <--> [d14. Железки (13-35)](https://mai-806.github.io/fund-wiki/1sem/day14.html) <--> [d15. Железки (36-74)](https://mai-806.github.io/fund-wiki/1sem/day15.html) 

***

## Словарик программиста:

**Термины с лекции:**

- [Сборка программ на C](https://acm.bsu.by/wiki/C2017/Сборка_программ_на_C)
- [Библиотеки](https://blog.skillfactory.ru/glossary/biblioteka/)
- [Система программирования](https://github.com/mai-806/fund-wiki/blob/main/1sem/Система%20программирования.md)
- [Оператор](https://github.com/mai-806/fund-wiki/blob/main/1sem/Оператор.md)
- ***Верификаторы*** могут выяснять корректность работы программы.
- ***Профилёры*** выявляют корректность и выводят данные о потреблении.
- ***Языковая среда*** — это интерпретативные компоненты ЯП (!).

***

- [Компилятор](https://github.com/mai-806/fund-wiki/blob/main/1sem/Компилятор.md) — то же, что и ***транслятор***!
- ***Компиляция*** — перевод текста программы с исходного формального языка на более простой язык. 
- ***Компоновщик*** (линкер) связывает все объектные файлы и статические библиотеки в единый исполняемый файл, который мы и сможем запустить в дальнейшем.
- [Линкер](https://ru.bmstu.wiki/Linker_(Link_Editor))
- [Докер](https://cloud.yandex.ru/blog/posts/2022/03/docker-containers)

***

- [Интерпретатор](https://github.com/mai-806/fund-wiki/blob/main/1sem/Интерпретатор.md) — или ***отладчик***
- [Отладка и её методы](https://github.com/mai-806/fund-wiki/blob/main/1sem/Отладка.md)
- [Тестирование и отладка](https://github.com/mai-806/fund-wiki/blob/main/1sem/Тестирование%20и%20отладка.md)

***

## Система программирования


[Система программирования](https://github.com/mai-806/fund-wiki/blob/main/1sem/Система%20программирования.md) — организованная совокупность компонентов для обеспечения программирования.
- Главным в СП является сам язык программирования, а не компилятор.


- В состав СП входит языковый процессор (либо в виде интерпретатора, либо в виде компилятора)


> Синус, логарифм, экспонента — не компилируются в Pascal.
> Это хороший пример, где компилятор работает не до конца.

- Если в языке есть интерпретатор, то туда входит и языковая среда (т.е. библиотеки).
- Интерпретативная система является удобной для отладки.

_Если язык чисто компилируемый (а таких нет), то в нём и нет среды.
А сама среда нужна, чтобы можно было взаимодействовать с Unix (с ОС)._

- `Верификаторы` могут выяснять корректность работы программы.
- `Профилёры` выявляют корректность и выводят данные о потреблении.

## Текстовые терминалы

**Текстовый терминал** — это последовательный компьютерный интерфейс для ввода и отображения текста. Информация в нём представлена в виде массива предварительно выбранных сформированных символов. В таких устройствах используется электронно-лучевая трубка, выдающая одноцветное изображение.

В дни универсальных ЭВМ с середины 1970-х до середины 1980-х люди использовали терминалы для дистанционной связи с компьютерами. В отличие от монитора, который обычно размещен рядом с компьютером, терминал может быть расположен очень далеко от главного компьютера. 

Терминал получил своё название, так как был размещен на `терминальном конце` кабеля.

Терминал состоит из **экрана** и **клавиатуры**. Программы выполняются на главном компьютере, но результаты отображаются на экране терминала. 

[Подробнее про терминал](https://studfile.net/preview/5208985/)

## Языковые процессоры

> © Assembler — это почти не нужно. Во всём мире нужно человек 100, программирующих на Assembler.

Человеку удобно работать на языке высокого уровня.
Но программа и высокоуровневый язык имеют между собой большую пропасть, которую как-то надо устранять.

[***Компилятор***](https://github.com/mai-806/fund-wiki/blob/main/1sem/Компилятор.md) (*или транслятор*) — принимает на вход текст высокого уровня и транслирует его в текст низкого уровня (в машинные тексты).

Раньше компиляторы было дорого и тяжело разрабатывать (да и сейчас, в принципе). 
Изначальным целевым языком компилятора был Assembler.

- © Unix: "Компилировать в Assembler не зазорно!"

Таким подходом оправдывалась экономия расходов на разработку новых компиляторов.

***Компилятор*** воспринимает всю программу целиком, анализирует её правильность и переводит в машинные коды.
Подобно переводчику, он берёт и выполняет письменный перевод текста.

`© Все стоят к Assembler спиной!`
 
Недостатки письменного перевода (компилирования): дороговизна, скорость работы. Одновременно они являются и продолжением его достоинств. Письменный перевод всегда получается качественным.
- Но при отладке нам важна скорость!

Интерпретатор же берёт и выполняет (бубнит текст).

`© Каждый отладчик - это интерпретатор!`

- Интерпретатор хорош для отладки, потому что запускает работу программы сразу (отладка — это и есть интерпретация).

[***Интерпретатор***](https://github.com/mai-806/fund-wiki/blob/main/1sem/Интерпретатор.md) — устный переводчик (ему говорят, и машина выполняет).

Итак, ***письменный перевод*** выполняется `компилятором`, ***устный перевод*** - `интерпретатором`.

- Си — транслятор (но в нём развита интерпретативная часть).
- Паскаль — транслятор.
- С++ — компилятор.

> © Лучший пример интерпретатора — `железный язык`.
> - Он есть ещё со времён Адама и Евы...
> - Т.е. это непосредственно сам язык выполнения кода машиной.

На компиляторе пишут **многоразовые программы**

> Assembler не является интерпретатором. По методу реализации он является компилятором, хоть и очень примитивным.
> - А примитивным, потому что компилирует в формате 1 к 1.

- Unix, basic — интерпретаторы.

На интерпретаторах пишут ***одноразовые программы/лабы***.

- Lisp — интерпретатор, Марков — интерпретатор, Тьюринг — тоже.

> © Питон не предназначен для систем...
> © Windows по уровню сложности сравним с Boeing...

***Отладчик*** — компилятивный суррогат.

`Языковая среда` — интерпретативные компоненты ЯП.

- Интерпретируемые языки — lisp, prolog.
> © Чистых компиляторов и интерпретаторов нет.


`Профессор Вирт` предложил ***Pascal*** - улучшение Algol.

```yaml
© Язык Си мощнее Pascal в 5.5 раз!
- `(joke)`
.....Почему?
- Описание страницы языка Си занимает
- 550 страниц, а языка Pascal - 99! 
```

- Pascal разрабатывали в университетах Швейцарии (при этом в то время все вузы были бедные).
- Pascal компилирует не в машинном коде и не в Assembler, а в ***p-code***.

`P-code` — это двоичный массив, маленькая абстрактная стековая машина.
Технология компилирования называлась `bootstrapping` (см. [бутстрепинг](https://github.com/mai-806/fund-wiki/blob/main/1sem/Бутстреппинг.md)) (в переводе - развязывание шнурка, потянув за него).

## GNU compiler collection

- `GCC` — это многоплатформенная и многоязычная система программирования (создана с инструментальными средствами).

- Lex, flex, yacc (yet another compiler compiler), Bison -



- [***Cтатья***](http://rus-linux.net/lib.php?name=/MyLDP/algol/lex-yacc-howto.html) об их применении.

## Компиляция программ

- ***Первый компилятор*** на Cи писал ***Брайан Керниган***.
- Сам ***язык Си*** писал ***Деннис Ричи***.
> Условие компиляции — программа должна соблюдать стандарт.

- [***Линкер***](https://ru.bmstu.wiki/Linker_(Link_Editor)) — программа, производящая ***компоновку*** - связывание объектных файлов и статических библиотек в единый исполняемый файл.
Он настраивает программу на готовую работу.

a.out — assembler.out (вывод ассемблера - результат линкера)

Команда *a.out* предназначена для выполнения без затрат на компиляцию (в некомпилируемых системах).

(?) библиотеки (.dll)
(?) ключи компилятора - флаги
Компиляция + ключ, Linkage

## Программирование

- [Тестирование и отладка](https://github.com/mai-806/fund-wiki/blob/main/1sem/Тестирование%20и%20отладка.md)

Создание программ включает в себя ещё тестирование и отладку.
- Тесты — это данные.
- А тестирование — деятельность по доказательству отсутствия ошибок в программе.
Тестирование **доказывает** отстутствие ошибок.
А отладка **ищет** ошибки.

Тесты должны прощупывать **все** ветки программы.

> © Программист должен быть злым и ненавидеть свою программу, чтобы она работала!
- Т.е. он должен тщательно тестировать свою программу!

- [Оператор](https://github.com/mai-806/fund-wiki/blob/main/1sem/Оператор.md) в программировании.

### Методы отладки:

1) ***Ручная отладка***. Иначе говоря, ручная прокрутка программы — это интерпретация. Она полезна! Это совершенно другой подход к программированию!
2) ***Отладка средствами стандарта языка***. Проверки вставляем после того, как программа отказалась работать.
3) ***С помощью отладчика***. Если тесты не работают, надо искать семантические ошибки в коде программы. Когда сами пишете программу, часто глаз замыливается, и тогда возникают ошибки. Для этого производите отладку через некоторое время, когда вы полны сил!

```yaml
© Машина Тьюринга 
— это рулон туалетной бумаги
```
## Дополнительная информация

- Лауреаты [премии Тьюринга](https://ru.zahn-info-portal.de/wiki/Turing_Award).
- Здесь я спросил о [колмогоровской сложности](https://github.com/mai-806/fund-wiki/blob/main/1sem/combinatorical_logic.md).

***

- [d10. Нотация Дейкстры](https://mai-806.github.io/fund-wiki/1sem/day10.html) <--> [d11. Типы данных](https://mai-806.github.io/fund-wiki/1sem/day11.html) <--> [d12. Файлы, блоки](https://mai-806.github.io/fund-wiki/1sem/day12.html) <--> [d13. Критика фон Неймана, рекурсия](https://mai-806.github.io/fund-wiki/1sem/day13.html)

- [d1. Раскладки клавиатур, кодировки](https://mai-806.github.io/fund-wiki/1sem/day1.html) <--> [d6. Системы программирования](https://mai-806.github.io/fund-wiki/1sem/day6_2.html) <--> [d9. Железки (1-12)](https://mai-806.github.io/fund-wiki/1sem/day9.html) <--> [d14. Железки (13-35)](https://mai-806.github.io/fund-wiki/1sem/day14.html) <--> [d15. Железки (36-74)](https://mai-806.github.io/fund-wiki/1sem/day15.html) 
