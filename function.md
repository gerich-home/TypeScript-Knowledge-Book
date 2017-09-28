### **Название фичи: Функции**

**Описание:      
**Работа функций и особенности аналогичныJS.**  
Аналог в c\# / js: **аналогично JS  
**Отличия:**

* Типизация для параметров и функции

* Типизация возвращаемого значения функции, на него указывает стрелка “=&gt;” между параметрами и типом возвращаемого значения. Часть необходимая, в случае если функция не возвращает значения пишем void.

* TS считает, что число передаваемых параметров должно совпадать с числом параметров, которые ожидает функция, то есть каждый параметр функции обязателен.

* Возможность сделать параметры функции необязательными с помощью «**?**»  
  `function buildName (lastName?:string) {…}`  
  Необязательные параметры должны идти после обязательных.

* Параметры со значением по умолчанию \(`lastName= “Hello!”`\)

**Решаемая проблема:**

**Пример возникновения:**

**Пример кода:  
**_**упрощенная контекстная типизация**_

`function add (x: number, y: number): number {`

`return x + y;`

`}`

`let myAdd = function (x: number, y: number): number {`

`return x+y;`

`};`

_**полноценный пример**_

`let myAdd: (baseValue: number, increment: number) =>`

`number = function (x: number, y: number): number {`

```
   return x + y;
```

`};`

**  
Перекомпилированный в JS код:**

![](/assets/daimport.png)

`var myAdd = function (x, y) {`

```
 return x + y; 
```

`};`

**  
Как решилась проблема:**
