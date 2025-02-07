# Роботу виконав студент ***Шроль Софія Григорівна***
> ***Київський політехнічний інституту, ІТС, группа ТЗ-22***

## Lab4
> *Варіант 25:*
- [x] Завдання 1(№25)
- [x] Завдання 2(№55)
- [x] Завдання 3(№64)
### Опис
Кожне з трьох завдань розташовується в класі 'Task + номер завдання'. В кожному завданні виконані вправи з масивами.
Завдання знаходиться за *[посиланням](https://docs.google.com/document/d/1oyh_Fen-c0Z6R15DjGKeDtLA_xLmADzhX3BB1LfqZoM/edit?tab=t.0)*.

Кожен клас має метод printResult, з параметром масивом відповідно завданню, що виводить результат розрахунків в термінал редактору кода. В завданні 25 - функція повертає значення min2, яке є іншим мінімальним за модуль елементом. В 55 - повертається значення змінної count, яке показує кількість додаткових елементів. 64 - повертається новий елемент result, у якому кожен перетворений відповідно до заданих умов.

> ***Контрольні питання:***

### 1. Чим змінна відрізняється від масиву

- Змінна : це одинична комірка пам'яті, яка зберігає одне значення певного типу (наприклад, int, double, charтощо). наприклад, int x = 5;.
- Масив : це структура даних, яка дозволяє зберегти множину значень одного типу в наступних комірках пам'яті. наприклад, int[] arr = {1, 2, 3};. Масив має зафіксовану довжину та дозволяє доступ до кожного елемента через індекс.

### 2. Що таке стек? Що таке купа? Яка між ними різниця?

### - Стек (стек):
- Ця структура пам'яті, де дані зберігаються за принципом LIFO (Last In, First Out).
- Стек використовує для зберігання локальних змінних і викликів функцій.
- Керується автоматично: при виклику функції змінні додаються в стек, а при завершенні функції звільняються.
### - Купа (купа):
- Це область пам'яті для динамічного розподілу даних.
- Використовується для об'єктів, масивів або інших структур, які повинні існувати незалежно від поточного завдання функції.
- Пам'ять у купі потрібно явно звільняти (або вона очищається зібраним сміттям у мовах на кшталт Java).
### - Різниця :
- Стек швидкий, але обмежений за розміром і використання для тимчасових даних.
- Купа більша, але виділення пам’яті в ній повільніше, і вона використовується для даних, що потребують тривалого зберігання.

### 3. Чи може змінна бути розташована у стеку? Безпосередньо у купі? В об’єкті у купі? Чи може масив бути розташований у стеку? Безпосередньо у купі? В об’єкті у купі?

- Чи може бути змінена у стеку?
Так, локальні змінні зберігаються у стеку.
- Безпосередньо у купі?
Ні, якщо це не об'єкт. Однак змінні класи, що належать до об'єкта, зберігаються в купі разом з об'єктом.
- В об'єкті у купі?
Так, якщо змінена є членом класу, вона буде в купі разом із об'єктом.
- Чи може бути масив у стеку?
У стеку зберігається лише посилання на масив. Сам масив розташовується у купі.
- Безпосередньо у купі?
Так, масив завжди зберігається у купі.
- В об'єкті у купі?
Ні, але посилання на масив може бути полем об'єкта.

### 4. Чим посилання на масив відрізняється від масиву? Чи може посилання на масив бути розташовано у стеку? Безпосередньо у купі? В об’єкті у купі?

- Посилання на масив : це змінно, що зберігає адресу початку масиву в пам'яті.
- Масив : це структура даних, що містить елементи.
- Розташування посилання :

У стеку: якщо це локально змінено.

У купі: якщо це поле об'єкта.

В об'єкті в купі: якщо це поле класу, розташованого в купі.

### 5. Якщо масив складається з 10 комірок, які індекси мають перша та остання комірки?

- Перша комірка має індекс 0.
- Остання комірка має індекс 9(завжди довжина - 1).

### 6. Що буде, якщо звернутися до неіснуючої комірки у масиві?

- У мовах на кшталт Java виникне виняток ArrayIndexOutOfBoundsException.

- У мовах на кшталт C++ це можна призвести до доступу до вільної пам'яті, що може спричинити помилку.

### 7. При створенні нового масиву без явної ініціалізації усі його комірки будуть проініціалізовані:
### - спеціальними значеннями за замовчуванням?
### - довільними значеннями, що знаходяться в цей час у пам’яті, яку виділено під масив?

- У деяких мовах (наприклад, Java):

При створенні масиву його елементи ініціалізуються значеннями за замовчуванням ( 0, false, null).

- У мовах на кшталт C++:

Масив може надрукувати випадкові значення, якщо його явно не ініціалізувати.

### 8. Як дізнатися номер першої та останньої комірки масиву, якщо відомо лише посилання на нього?

- Перша комірка завжди має індекс 0.

- Остання комірка: array.length - 1(в Java та інших мовах).

### 9. Як змінити розмір масиву?

У деяких мовах (Java, C++) розмір масиву зафіксований. Щоб змінити розмір:

- Створюється новий масив більшого розміру.

- Старі значення копі знаходяться у новому масиві.

### 10. Що відбувається з масивом при копіюванні посилання на нього?

Створюється ще одна змінна, яка вказує на той самий масив у пам'яті. Зміни через одне посилання будуть видимі через інше.

### 11. Що відбувається з масивом при втрачанні посилання на нього?

- У Java: об'єкт (масив) стає недоступним і згодом очищається зібраним вмістом.

- У C++: пам'ять, виділена під масив, залишитися зайнятою, що може призвести до витоку пам'яті.


### 12. Чим відрізняються конструкції «for» та «for-each» при роботі з масивами? Які переваги та недоліки кожного з варіантів?

- for:

Універсальний.

Дозволяє доступ до індексів та контроль над порядком виконання.

- for-each:

Простий синтаксис для роботи з кожним елементом.
Не дає доступу до індексів.

Перевагиfor-each : менше коду, безпечніше.

Недоліки : обмежений доступ до індексів.

### 13. Чи можна у масив «double[]» записати значення «int»? Чи можна у масив «int[]» записати значення «double»?

У Java:

- Можна записати intу double[](через автоматичне приведення типів).

- Не можна записати doubleу int[](виникне помилка компіляції).
