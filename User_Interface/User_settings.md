# Налаштування користувача #
Деякі значення та налаштування в CoppeliaSim не залежать від [сцени](https://www.coppeliarobotics.com/helpFiles/en/scenes.htm) чи [моделі](https://www.coppeliarobotics.com/helpFiles/en/models.htm), а радше від користувача. Діалогове вікно налаштувань користувача (яке частково відображає вміст файлу *system/usrset.txt*) можна відкрити за допомогою [Панель меню --> Інструменти --> Налаштування] або натиснувши наступну кнопку на панелі інструментів:
 
 ![settings1](settings1.jpg)
 
[Кнопка панелі інструментів налаштувань]

 ![settings2](settings2.jpg)
 
 [Діалогове вікно налаштувань користувача]

+ **Розмір кроку переведення:** лінійний розмір кроку, який використовується під час переведення [об’єктів](https://www.coppeliarobotics.com/helpFiles/en/objects.htm) у [режимі маніпулювання об’єктами](https://www.coppeliarobotics.com/helpFiles/en/objectMovement.htm). Рекомендується зберігати значення 5 см. Об’єктам можна призначити певні розміри кроку [в діалоговому вікні координат і трансформації](https://www.coppeliarobotics.com/helpFiles/en/coordinateDialog.htm).
+ **Розмір кроку обертання:** розмір кутового кроку, який використовується під час обертання [об’єктів](https://www.coppeliarobotics.com/helpFiles/en/objects.htm) у [режимі маніпулювання об’єктами](https://www.coppeliarobotics.com/helpFiles/en/objectMovement.htm). Об’єктам можна призначити певні розміри кроку [в діалоговому вікні координат і трансформації](https://www.coppeliarobotics.com/helpFiles/en/coordinateDialog.htm).
+ **Видалити ідентичні вершини, допуск:** якщо вибрано, вершини, які лежать поруч з іншими вершинами, будуть згруповані, щоб утворити одну вершину (яка потім буде спільною для навколишніх трикутників). Це зменшує обсяг необхідних ресурсів пам'яті. Цей параметр впливає на сітки, коли вони [імпортуються](https://www.coppeliarobotics.com/helpFiles/en/importExport.htm), або на [форми](https://www.coppeliarobotics.com/helpFiles/en/shapes.htm), коли виходять із [режиму редагування форми](https://www.coppeliarobotics.com/helpFiles/en/shapeEditModes.htm). Допуск визначає поріг відстані, який слід враховувати при групуванні вершин. Загалом, зберігайте низьке значення, але відмінне від нуля: деякі формати даних сіті (наприклад, STL) призначають окремі вершини кожному трикутнику, незалежно від того, чи вершина ідентична іншій вершині в іншому трикутнику; це може значно збільшити необхідний обсяг пам'яті.
+ **Видалити ідентичні трикутники:** якщо вибрано, ідентичні трикутники в ресурсі сітки буде видалено під час операції імпорту або коли фігура виходить із режиму редагування фігури.
+ **Ігноруйте звивання трикутника:** трикутник може мати дві різні орієнтації (оскільки він має дві різні грані). Якщо вибрано цей пункт, орієнтація трикутника ігнорується під час визначення однакових трикутників.
+ **Undo/redo вмикач:** вмикає або вимикає функцію скасування/повторення. Ця функція працює шляхом серіалізації (збереження) усієї сцени в пам’яті кожного разу, коли реєструється зміна. Запам’ятовуються лише відмінності від попередніх пунктів скасування, щоб використовувати мало пам’яті. Це дуже ефективне та безпечне скасування/повторення, яке також підтримується [плагінами](https://www.coppeliarobotics.com/helpFiles/en/plugins.htm) або [основним клієнтським додатком](https://www.coppeliarobotics.com/helpFiles/en/mainClientApplication.htm), і це дозволено лише тому, що процедури серіалізації CoppeliaSim дуже швидкі. Однак бувають випадки, коли або комп’ютер дуже старий, або вміст сцени надзвичайно великий (наприклад, дуже детальні дані cad), коли цей метод уповільнює роботу всієї програми. У такому випадку просто вимкніть функцію скасування/повторення.
+ **Відображати еталонний світ:** відображає невелику еталонну рамку світу в нижній лівій частині екрана [камери](https://www.coppeliarobotics.com/helpFiles/en/cameras.htm). Як і скрізь у CoppeliaSim, червона, зелена та синя стрілки відповідають осям x, y та z відповідно.
+ **Відображати обмежувальні рамки вибраних об’єктів:** відображає білу/жовту обмежувальну рамку навколо вибраних об’єктів
+ **Автоматичне збереження ввімкнено:** коли автозбереження ввімкнено, кожна відкрита сцена буде зберігатися на регулярній основі. У разі збою автоматично збережені сцени можна відновити. Затримку автозбереження можна налаштувати у файлі system/usrset.txt.
+ **Приховати вікно консолі:** дозволяє приховати або показати [вікно консолі](https://www.coppeliarobotics.com/helpFiles/en/userInterface.htm#ConsoleWindow). За замовчуванням вікно консолі приховане. На Mac цей пункт недоступний (стандартний вивід можна переглянути в системній консолі (Програми/Утиліти/Консоль)).
+ **Приховати ієрархію під час симуляції:** автоматично приховує ієрархію сцени під час симуляції.
+ **Параметри OpenGL:** відкриває діалогове вікно, яке дозволяє налаштувати більшість параметрів, пов’язаних з OpenGL:

Налаштування OpenGL

![openGlSettings](openGlSettings.jpg)

[Діалогове вікно налаштувань OpenGL]

+ **Тип позакадрового контексту:** тип позакадрових контекстів візуалізації. За замовчуванням невидимі вікна.
+ **Тип FBO:** тип об’єктів буфера кадру. За замовчуванням FBO на основі Qt на Mac і FBO не на основі Qt у Windows і Linux.
+ **Операція VBO:** чи використовуються об’єкти буфера вершин. Параметр **за замовчуванням** використовує VBO.
+ **Idle fps:** кількість кадрів за секунду в режимі очікування.