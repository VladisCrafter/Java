---
share: true
---
# Типы данных
```java
// комментарий

/* 
* Длинный комментарий
*/

int variable; // объявление
variable = 1; // придача значения
int variable = 1; // всё сразу

int name = 1; // целое число
float name = 3.14f; // десятичные...
double name = 6.4 // ...дроби
boolean name = True // либо False
char name = 'X' // одинарные кавычки
String name = "x x x" // двойные кавычки
```
# Синтаксис
```java
int x = 10;
int y = x; // => y = 10
```
# Ввод и вывод
```java
System.out.println("Hello Java!"); // [консоль] Hello Java!
int x = 10;
System.out.println(x); // [консоль] 10
System.out.println("Число x равно " + x); // [консоль] Число x равно 10

Scanner scannerX = new Scanner(System.in); // не забыть import java.util.scanner!
String x = scannerX.next(); // значение СТРОКИ x будет равно введённому в консоль
int x = scannerX.nextInt(); // значение ЧИСЛА x будет равно введённому в консоль
System.out.println("Введено " + x); // [консоль] Введено {введённое значение}
```
# Математика
```java
int x = 1;
int y = 2;

int xy = x + y; // xy - сумма x и y
int xy = x - y; // xy - разность x и y
int xy = x * y; // xy - произведение x и y
int xy = x / y; // xy - частное x и y
int xy = x % y; // xy - остаток от деления x и y

int z = -3
double w = 1.21

int x = Math.abs(z); // x - модуль z (3)
int x = Math.ceil(w); // x - округлённый вверх w (2.0)
int x = Math.round(w); // x - округлённый w (1)
int x = Math.floor(w); // x - округлённый вниз w (1.0)
int x = Math.max(y, z); // x - максимальное значение из выбранных (y)
int x = Math.min(y, z); // x - минимальное значение из выбранных (z)
```
# Булевы и логика
```java
int x = 5;
int y = 10;
int z = -20;

boolean comparison = y > x; // True, т.к. y больше x
boolean comparison = z <= x; // True, т.к. z меньше или равен x
boolean comparison = y != z; // True, т.к. y не равен z
boolean comparison = y == x; // False, т.к. y НЕ равен x

boolean trueboolean = True;
boolean falseboolean = False;

boolean anytrue = trueboolean || falseboolean; // True, т.к. одного с True достаточно
boolean alltrue = trueboolean && falseboolean; // False, т.к. одного с True недостаточно
```
# Операторы присваивания
```java
int x = 10; // объявление и присвоение
x = x + 90; // увеличение значения
x += 90; // краткий вариант
x ++; // ещё более краткий для увеличения на 1
// работает со остальными операторами (- * / %)
```
# Ветвление
```java
int x = scannerX.next();
boolean comparison = x >= 10 && x <= 100; // True, если x не меньше 10 и не больше 100

if(comparison) { // исполняется, если True
	System.out.println("x в пределах границ");
} else { // исполняется, если любой другой результат кроме True (здесь - False)
	System.out.println("x за пределами границ");
}

int y = scannerX.next();

if(y > 0) {
	System.out.println("y больше 0");
} else if(y < 0) {
	System.out.println("y меньше 0");
} else {
	System.out.println("y равно 0");
}

int z = 4;
switch (z) { // прописывать действие нужно ДЛЯ КАЖДОГО исхода
	case 0: System.out.println("z равен нулю"); break; // не
	case 1: System.out.println("z равен единице"); break; // забыть
	case 2: System.out.println("z равен двум"); break; // break;
	case 3: System.out.println("z равен трём"); break; // в конце
	case 4: System.out.println("z равен четырём"); break; // это важно
	default: System.out.println("z равен неизвестному значению"); // работает как else
}
```
# Циклы
```java
for(int x = 0; x <= 10; x++) { // (новая переменная; желаемое конечное значение; размер шага)
	System.out.println(i); // [консоль] {0...10}
}

y = 10
while(y <= 20) {
	y++;
	if(y == 16) {
		continue; // всё последующее проигнорируется и цикл повторится
	}
	if(y == 20) {
		break; // всё последующее также проигнорируется, но цикл перестанет повторяться
	}
}
```
# * Первое упражнение
```java
package vladiscrafter;  
  
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        while (true) {  
            System.out.println("Добро пожаловать в легкий кулькалятор! Для начала выберите тип операции:"); // welcome + selecting the operation type  
            Scanner scanner = new Scanner(System.in);  
            String operation = scanner.next();  
            System.out.println("Теперь первое число:"); // first int  
            int first = scanner.nextInt();  
            System.out.println("И второе число:"); // second int  
            int second = scanner.nextInt();  
  
            switch (operation) {  
                case "+" -> {  
                    int result = first + second;  
                    System.out.println("Результат: " + result);  
                }  
                case "-" -> {  
                    int result = first - second;  
                    System.out.println("Результат: " + result);  
                }  
                case "*" -> {  
                    int result = first * second;  
                    System.out.println("Результат: " + result);  
                }  
                case "/" -> {  
                    int result = first / second;  
                    System.out.println("Результат: " + result);  
                }  
                case "%" -> {  
                    int result = first % second;  
                    System.out.println("Результат: " + result);  
                }  
                default -> System.out.println("Некорректный тип операции"); // incorrect operation type  
            }  
            System.out.println("Продолжить: 1 | Закончить: 0"); // continue: 1 | end: 0  
            int continueorno = scanner.nextInt();  
            if(continueorno == 1) {  
                continue;  
            } else break;  
        }  
    }    
}
```
# Тернарный оператор
```java
int x = 1;
String isOne = " ";  
if(x > 0) {
    isOne = "больше нуля.";
} else {
    isOne = "ноль.";
}
System.out.println("Состояние x: " + isOne);

isOne = x > 0 ? "больше нуля." : "ноль."; // пер = условие ? {если True} : {иначе}
System.out.println("Состояние x: " + isOne); // по сути, компактный вариант if-else
```
# Приведение переменных
```java
int x = 10;
float y = 20.5f;
float xy = x + y; // x без проблем переводится в float, т.к. не теряет информацию
int xy = (int)y - x; // перевод надо огласить, и у пер. y обрезается инфа после точки

String strZ = "64";
int z = Integer.parseInt(strZ) + 6; // перевод строки в число и выполнение простого действия
```
# Строки и методы с ними
```java
String nick = "VladisCrafter";
String hobby = "YouTube";
System.out.println("Hi! I'm " + nick + ", a Minecraft " + hobby); // не хватает "r!" в конце
hobby += "r!";
System.out.println("Hi! I'm " + nick + ", a Minecraft " + hobby); // "r!" присоединён к hobby

String strangecase = "HELLO there";
System.out.println(strangecase.toLowerCase()); // всё строчными буквами
System.out.println(strangecase.toUpperCase()); // всё ЗАГЛАВНЫМИ буквами
System.out.println("Имеет ли \"there\"? " + strangecase.contains("there")); // True
System.out.println("Имеет ли \"here\"? " + strangecase.contains("here")); // False
strangecase = strangecase.replace("there", "then");
System.out.println("Имеет ли теперь \"then\"? " + strangecase.contains("then"));
int charpos = 4;  
System.out.println("Сиволом №" + charpos + " является: " + strangecase.charAt(charpos));
```
# Массивы
```java
String[] keys = new String[3]; // новый список, указание кол-ва элементов
keys[0] = "key_zero"; // указание
keys[1] = "key_one"; // этих самых
keys[2] = "key_two"; // элементов
String[] values = new String[3];
values[0] = "value_zero";
values[1] = "value_one";
values[2] = "value_two";
for(int i = 0; i < keys.length; i++) {
    System.out.println(keys[i] + " | " + values[i]);
}

for(String key : keys) { // каждый цикл переменная key соответствует элементу массива  
    System.out.println(key);  
}
```
# Методы
```java
public static int newClass(int x, int y) { // название не должно начинаться с заглавной  
    return x + y;  
}

public static void outputKeys_n_Values(String[] keys, String[] values) {
    for(int i = 0; i < keys.length; i++) {
        System.out.println(keys[i] + " | " + values[i]);
    }
} // вывод ключей-значений из прошлой темы как отдельный класс

for(int i = 0; i < 2; i++) {
    outputKeys_n_Values(keys, values);
} // 2-кратный вызов данного класса

/*
* ПКМ -> Refactor -> Extract method (ctrl+alt+M)
*/
private static void outputKeys_n_ValuesTwice(String[] keys, String[] values) {  
    for(int i = 0; i < 2; i++) {  
        outputKeys_n_Values(keys, values);  
    }  
} // автоматически создаётся и динамически меняет название
```
# Коллекции
```java
List<String> keys = new ArrayList(); // коллекция строк
keys.add("key_zero"); // добавление элемента
keys.clear(); // очистка коллекции
Set<String> set = new HashSet(); // то же, только дупликаты элементов не будут учитываться
List<Integer> ints = new ArrayList<>(); // коллекция чисел (важен Integer, а не int)
Map<String, Integer> keys_values = new HashMap<>();
keys_values.put("key0", 0); // key - ключ, а 0 - значение
keys_values.put("key1", 1);
keys_values.put("key2", 2);
System.out.println("Значение ключа key0: " + keys_values.get("key0")); // значение по ключу
for(Map.Entry<String, Integer> entry : keys_values.entrySet()) {
    System.out.println("Ключ: " + entry.getKey() + " | Значение: " + entry.getValue()) 
}
```
# * Второе упражнение
```java
package vladiscrafter;  
  
import java.util.*;  
  
public class Main {  
    public static void main(String[] args) {  
        Scanner scanner = new Scanner(System.in);  
        while (true) {  
            calculating();  
            System.out.println("Продолжить: y | Закончить: n");  
            String continuing = scanner.next();  
            if(continuing.equals("y")) {  
                continue;  
            } else {  
                break;  
            }  
        }  
    }  
  
    public static void calculating() {  
        System.out.println("Добро пожаловать в легкий, но улучшенный кулькалятор! Для начала выберите тип операции:"); // welcome + selecting the operation type  
        Scanner scanner = new Scanner(System.in);  
        String operation = scanner.next();  
        System.out.println("Теперь первое число:"); // first int  
        int first = scanner.nextInt();  
        System.out.println("И второе число:"); // second int  
        int second = scanner.nextInt();  
        int result = 0;  
  
        switch (operation) {  
            case "+" -> {  
                result = first + second;  
                System.out.println("Результат: " + result);  
            }  
            case "-" -> {  
                result = first - second;  
                System.out.println("Результат: " + result);  
            }  
            case "*" -> {  
                result = first * second;  
                System.out.println("Результат: " + result);  
            }  
            case "/" -> {  
                if(second != 0) {  
                    result = first / second;  
                } else {  
                    System.out.println("Ошибка: деление на 0.");  
                }  
                System.out.println("Результат: " + result);  
            }  
            case "%" -> {  
                result = first % second;  
                System.out.println("Результат: " + result);  
            }  
            default -> System.out.println("Некорректный тип операции"); // incorrect operation type  
        }  
    }  
}
```
# Классы и объекты
### NewClass.java
```java
package vladiscrafter;
public class NewClass {
    public String data1; // определение параметров,
    public String data2; // с которыми задаётся
    public int data3; // объект типа NewClass
//    public NewClass() {
//        // конструктор по умолчанию
//    }
    public NewClass(String data1, String data2, int data3) { // конструктор с параметрами
        this.data1 = data1; // назначение
        this.data2 = data2; // параметров
        this.data3 = data3; // объекта
    }
    public void intIncrease() {
        data3++; // простенькое действие для примера
    }
}
```
### Main.java
```java
package vladiscrafter;
import java.util.*;
public class Main {
    public static void main(String[] args) {
        NewClass example1 = new NewClass("String1_1", "String1_2", 0);
        NewClass example2 = new NewClass("String2_1", "String2_2", 1);
        // создание объектов с заданием соответствующих параметров
        System.out.println("int второго объекта: " + example2.data3);
        example2.intIncrease();
        System.out.println("Он же, прошедший increase: " + example2.data3);
        example2.data3 += 20;
        System.out.println("Он же, изменённый вручную: " + example2.data3);
    }
}
```
# Регуляторы доступа
```java

```