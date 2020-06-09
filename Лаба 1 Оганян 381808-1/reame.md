# «Обработка изображений» 
Выполнил: студент группы 381808-1
**Оганян Роберт Владимирович**
Преподаватель: профессор кафедры математического обеспечения и суперкомпьютерных технологий Турлапов Вадим Евгеньевич 

## Описание работы программы

Лабораторная работа выполнена в среде разработки VisualStudio. Лабораторная работа посвящена базовым принципам обработки изображений, рассматриваются алгоритмы подавление и устранение шума в черно-белых и цветных изображениях, выделение границ, краев, однородных зон, улучшение качества изображения, спецэффекты.

### Главный экран
Главный экран представляет из себя окно, содержащее:

+ «Открыть» - загрузить изображение для последующей обработки
+ Раздел «Фильтры» для непосредственной обработки изображений
+ «Сохранить» - сохранить измененное изображение
+ Прямоугольная шкала внизу в центре экрана, показывающая прогресса обработки изображения
+ Кнопка «отмена» для отката изображения в предыдущее состояние
 ![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image002.jpg)
### Фильтры
В программе реализованы следующие фильтры:

1.  **Инверсия**
2.  **Оттенок серого**
3.  **Сепия**
4.  **Увеличение яркости**
5.  **Размытие**
6.  **Фильтр Гаусса**
7.  **Фильтр Собеля**
8.  **Фильтр резкости**
9.  **Медианный фильтр**
10. **Выделение границ**
11. **Motion Blur**
12. **Горизонтальные волны**
13. **Вертикальные волны**
14. **Стекло**
15. **Линейное растяжение**
16. **Серый мир**
17. **Поворот ( на 45 градусов)**
18. **Расширение** **(матморфология)**
19. **Сужение (матморфология)**
20. **Открытие (матморфология)**
21. **Замыкание (матморфология)**
22. **Top hat** **(матморфология)**

### Дополнительные возможности
В программе также реализованы возможности:
1. Сохранять изображения [Смотреть в примерах использования]
2. Возможность изменения размера окна, при которой элементы будут перемещаться или растягиваться пропорционально изменению размера окна
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image004.jpg)

![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image006.jpg)

![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image008.jpg)

3. Отмена последнего изменения ( смотреть в примерах работы программы)
Что касается структуры программы, за основу берем родительский класс Filter, от которого наследуем классы точечных фильтров ( например фильтры 1-4). Матричные фильтры мы также наследуем от Filter, а потом каждый матричный фильтр наследуем от MatrixFilter ( например 5,6). Аналогично для фильтров с ядрами по разным осям ( DoubleMatrix) ( например 7).  Операции математической морфологии также сначала наследуются от Filter в свой класс MathMorphology, от которого наследуются классы для каждой операции (18-21).

### Работа программы в примерах:

1. Для начала загрузим изображение:
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image010.jpg)
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image012.jpg) 

2. Инверсия
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image014.jpg)

**Нажмем на «отмена изменений», чтобы вернуть изображение в предыдущее состояние :****![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image015.jpg)

3. Оттенок серого
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image017.jpg)

4. Сепия
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image019.jpg)

5. Увеличение яркости
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image021.jpg)

6. Размытие
**Наше первоначальное изображение:**
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image023.jpg) 

**После размытия:**![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image025.jpg)

7. Фильтр Гаусса
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image027.jpg)

8. Фильтр Собеля
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image029.jpg) 

9. Фильтр резкости
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image031.jpg)

10. Медианный фильтр
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image032.jpg)

11. Motion Blur
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image033.jpg)

12. Горизонтальные волны
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image034.jpg)

13. Вертикальные волны
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image035.jpg)

14. Стекло
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image036.jpg)

15.Линейное растяжение
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image037.jpg)![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image038.jpg)

16.Серый мир
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image039.jpg)![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image040.jpg) 

17. Расширение (матморфология)
**Программа предоставляет выбор маски. При выборе неправильной маски появляется сообщение с ошибкой** ![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image042.jpg)

#### Пример расширения
**Исходное изображение:**![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image044.jpg)

**Маска (в документе она увеличенная):** 
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image046.png)

**Результат:**
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image048.jpg) 

18. Сужение (матморфология)
#### Пример сужения
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image050.jpg)

19.Открытие (матморфология)
#### Пример открытия
**Исходное:**
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image051.jpg)

**Результат:**
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image053.jpg) 

20. Замыкание (матморфология)
#### Пример замыкания
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image055.jpg)

21. Top hat (матморфология)
#### Пример Tophat
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image057.jpg)
**Сохраним наше изображение.**
![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image059.jpg)![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image061.jpg) 

## Заключение
В программе реализованы фильтры из методички, а также:
1. «Серый мир»
2. Линейное растяжение гистограммы
3. Стекло и Волны
4. Операции математической морфологии dilation, erosion, opening, closing. 
5. top hat 
6. Медианный фильтр
7. Возможность задать и изменить структурный элемент для операций матморфологии.
8. Возможность сохранять изображения
9. Возможность изменения размера окна, при которой элементы будут перемещаться или растягиваться пропорционально изменению размера окна
10. Отмена последнего действия

## Приложение
**![img](file:///C:/Users/OgRob/AppData/Local/Temp/msohtmlclip1/01/clip_image062.jpg)**
Ссылка на гитхаб: https://github.com/OganyanRV/Csharp-Second_Year