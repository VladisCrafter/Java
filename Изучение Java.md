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
### NewClass.java
```java
package vladiscrafter;
public class NewClass {
    public String data1; // доступен везде (и изменяется)
    protected String data2; // доступен в подклассах того же package
    private int data3; // доступен ТОЛЬКО в этом классе
    public static int numberOfExamples = 0; // статичный - равен для любого случая вызова
	
    public NewClass(String data1, String data2, int data3) {
        this.data1 = data1;
        this.data2 = data2;
        this.data3 = data3;
        numberOfExamples++;
    }
    public void intIncrease() {
        data3++;
    }
    public int getData3() { // "получатель"
        return data3;
    }
    public void setData3(int data3) { // "установщик"
        this.data3 = data3;
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
        System.out.println("int второго объекта: " + example2.getData3());
        example2.intIncrease(); // data3 -> getData3
        System.out.println("Он же, прошедший increase: " + example2.getData3());
        System.out.println("Объектов для примера: " + NewClass.numberOfExamples); // 2
        NewClass example3 = new NewClass("String3_1", "String3_2", 2);
        System.out.println("А теперь: " + NewClass.numberOfExamples); // 3
    }
}
```
# Наследование и полиморфизм
### SuperClass.java
```java
package vladiscrafter;

public class SuperClass {
    public String data1;
    protected String data2;
    private int data3;
	
    public SuperClass(String data1, String data2, int data3) {
        this.data1 = data1;
        this.data2 = data2;
        this.data3 = data3;
    }
    
    public void action() {
        System.out.println("\nТестовое действие для любого класса подтверждено!");
    } // action в данном случае исполняется одинаково любым классом, но это можно изменить... 
		
    public void display() {
        System.out.println(data1 + "\n" + data2 + "\n" + data3);
    }
	
    public int getData3() {
        return data3;
    }
	
    public void intIncrease() {  
        data3++;
        System.out.println("intIncrease для " + data1 + " пройдён! Результат: " + data3);
    }
}
// ВСЁ ЭТО БУДЕТ РАБОТАТЬ С ЛЮБЫМ ПОДКЛАССОМ!
```
### NewClass.java
```java
package vladiscrafter;

public class NewClass extends SuperClass { // NewClass является пеодклассом SuperClass
	
    public NewClass(String data1, String data2, int data3) {
        super(data1, data2, data3);
    }
	
    @Override // действие action переписывается специально под этот класс
    public void action() {
        System.out.println("\nТестовое действие для первого класса подтверждено!");
    }
}
```
### NewClass2.java
```java
package vladiscrafter;

public class NewClass2 extends SuperClass { // NewClass2 является пеодклассом SuperClass
	
    public NewClass2(String data1, String data2, int data3) {
        super(data1, data2, data3);
    }
	
    @Override // действие action переписывается специально под этот класс
    public void action() {
        System.out.println("\nТестовое действие для второго класса подтверждено!");
    }
}
```
### Main.Java
```java
package vladiscrafter;
import java.util.*;

public class Main {
    public static void main(String[] args) {
        SuperClass example1 = new NewClass("1_String1_1", "1_String1_2", 10);
        SuperClass example2 = new NewClass("1_String2_1", "1_String2_2", 20);  
        // необязательно определять выбор класса в начале, можно просто исп. SuperClass!
        SuperClass example3 = new NewClass2("2_String_3_1", "2_String3_2",30);
        SuperClass example4 = new NewClass2("2_String_4_1", "2_String4_2",40);
        System.out.println("int второго объекта: " + example2.getData3());
        System.out.println("int четвёртого объекта: " + example4.getData3());
        example2.intIncrease();
        example4.intIncrease();
        System.out.println("\nОтображение инфы о третьем объекте: ");
        example3.display();
        example2.action();
        example3.action();
    }
}
```
# Абстрактные классы и интерфейсы
### NewClass3.java
```java
package vladiscrafter;

public class NewClass3 extends SuperClass implements Itestable {
    public NewClass3(String data1, String data2, int data3) {
        super(data1, data2, data3);
    }
    
    @Override
    public void undefAction() {
        test();
    }
    
    @Override
    public void test() {
        System.out.println("Третий класс протестирован.");
    }
}
```
### SuperClass.java
```java
package vladiscrafter;

public abstract class SuperClass { // класс назначен абстрактным
    public String data1;
    protected String data2;
    private int data3;
	
    public SuperClass(String data1, String data2, int data3) {
        this.data1 = data1;
        this.data2 = data2;
        this.data3 = data3;
    }
	
    public abstract void undefAction(); // никаких условий для метода здесь не прописывается! 
	
    public int getData3() {
        return data3;
    }
	
    public void intIncrease() {
        data3++;
        System.out.println("intIncrease для " + data1 + " пройдён! Результат: " + data3);
    }
}
```
### Itestable.java
```java
package vladiscrafter;

public interface Itestable { // "I" в начале и "able" в конце названия интерфейса
    void test();
}
```
### Main.java
```java
package vladiscrafter;
import java.util.*;

public class Main {
    public static void main(String[] args) {
        SuperClass example1 = new NewClass("1_String1_1", "1_String1_2", 10);
        SuperClass example2 = new NewClass("1_String2_1", "1_String2_2", 20);
        
        SuperClass example3 = new NewClass2("2_String_3_1", "2_String3_2",30);
        SuperClass example4 = new NewClass2("2_String_4_1", "2_String4_2",40);
        
        NewClass3 example5 = new NewClass3("3_String5_1", "3_String5_2", 50);
        
        example2.undefAction(); // выполнение метода
        example3.undefAction(); // по своему
        example5.undefAction(); // выполнение test через undefAction  
        ((NewClass3) example5).test(); // example5.cast + tab позволяет выполнить напрямую
        example5.test(); // сработает, только если выше сменить SuperClass на NewClass3
        
        List<SuperClass> classes = new ArrayList<>();
        classes.add(example1);
        classes.add(example2);
        classes.add(example3);
        classes.add(example4);
        classes.add(example5);
        
        List<Itestable> testables = new ArrayList<>();
        testables.add(example5); // только если выше сменить SuperClass на NewClass3
    }
}
```
# Анонимные классы
### Main.java
```java
SuperClass example6wrong = new SuperClass("4_string6_1", "4_string6_2", 60);
// Это не сработает, т.к. SuperClass абстрактный

SuperClass example6 = new SuperClass("4_string6_1", "4_string6_2", 60) {
    @Override // создание анонимного класса прямо здесь
    public void undefAction() {
    }
    @Override // свободное переписывание действия
    public void intIncrease() {
        super.intIncrease();
    }
};
```
# * Третье упражнение
### Main.java
```java
package vladiscrafter;  
  
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        while(true) {  
            System.out.println("Бобро пожаловать в третий, заключительный калькулятор! Этот раз был непрост...");  
            System.out.println("Итак, введите тип операции:");  
            Scanner scanner = new Scanner(System.in);  
            String opType = scanner.next();  
            System.out.println("Теперь первое число:");  
            int f = scanner.nextInt();  
            System.out.println("И второе число:");  
            int s = scanner.nextInt();  
            int result = 0;  
            switch (opType) {  
                case "+" -> {  
                    Add add = new Add(f, s, result);  
                    add.calculate();  
                } case "-" -> {  
                    Sub sub = new Sub(f, s, result);  
                    sub.calculate();  
                } case "*" -> {  
                    Mul mul = new Mul(f, s, result);  
                    mul.calculate();  
                } case "/" -> {  
                    Div div = new Div(f, s, result);  
                    div.calculate();  
                } case "%" -> {  
                    Per per = new Per(f, s, result);  
                    per.calculate();  
                } default -> throw new IllegalStateException("Неверный тип операции: " + opType);  
            }  
            System.out.println("Для продолжения введите: +");  
            String continuing = scanner.next();  
            if (continuing.equals("+")) {  
                System.out.println("Перезапуск...");  
                continue;  
            } else {  
                System.out.println("Прерывание...");  
                break;  
            }  
        }  
    }  
}
```
### Add.java (+ остальные операции)
```java
package vladiscrafter;  
  
public class Add implements ICalculable { // сложение
// public class Sub implements ICalculable // вычитание
// public class Mul implements ICalculable // умножение
// public class Div implements ICalculable // деление
// public class Per implements ICalculable // остаток
    public int f;  
    public int s;  
    public int result;  
    public Add(int f, int s, int result) { // сложение
    // public Sub(int f, int s, int result) { // вычитание
    // public Mul(int f, int s, int result) { // умножение
    // public Div(int f, int s, int result) { // деление
    // public Per(int f, int s, int result) { // остаток
        this.f = f;  
        this.s = s;  
        this.result = result;  
    }  
    @Override  
    public void calculate() {  
        result = f + s; // сложение
        // result = f - s; // вычитание
        // result = f * s; // умножение
        // result = f / s; // деление
        // result = f % s; // остаток
        System.out.println("Результат операции: \n" + result);  
    }  
}
```
### ICalculable.java
```java
package vladiscrafter;  
  
public interface ICalculable {  
    void calculate();  
}
```
# Перечисления
### Main.java
```java
package vladiscrafter;  
  
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        Options option = Options.OPTION2;  
        System.out.println("Выбранная опция: " + option + "\n");  
		
        Tiers chosenTier_one = Tiers.TIER3;  
        Tiers chosenTier_two = Tiers.TIER2;  
        Tiers chosenTier_three = Tiers.TIER1;  
		
        System.out.println("Имя третьего тира: " + chosenTier_one.getName());  
        System.out.println("Уровень второго тира: " + chosenTier_two.getLevel());  
        System.out.println("Эффективн. первого тира: " + chosenTier_three.getEfficiency());  
    }  
}
```
### Options.java
```java
package vladiscrafter;  
  
public enum Options { // создание перечисления  
    OPTION1, // запятые  
    OPTION2, // после элементов,  
    OPTION3; // но точка-с-запятой после последнего  
}
```
### Tiers.java
```java
package vladiscrafter;  
  
public enum Tiers { // сборка по конструктору
    TIER1("First tier", 1, 2.2f),  
    TIER2("Second tier", 2, 2.5f),  
    TIER3("Third tier", 3, 2.8f);  
	
    private String name;  
    private int level;  
    private float efficiency;  
	
    Tiers(String name, int level, float efficiency) {  
        this.name = name; // конструктор  
        this.level = level; // продвинутого  
        this.efficiency = efficiency; // перечисления  
    }  
	
    // ПКМ -> Generate -> Getter  
    public String getName() {  
        return name;  
    }  
    public int getLevel() {  
        return level;  
    }  
    public float getEfficiency() {  
        return efficiency;  
    }  
	
}
```
# Исключение - пробы и... улов?
```java
int i = 1;  
try {  
    i = 1 / 0;  
} catch (Exception e) {  
    System.out.println("Поймано исключение! " + e.getMessage());  
}  

System.out.println("Программа продолжает работать, несмотря на пойманное исключение!");  
  
if (i >= 0) {  
    throw new Exception("Почему исключение? Да потому что... потому!");  
} // кастомное исключение обычного типа
```
# Генеративы
### Main.java
```java
package vladiscrafter;  
  
import java.util.Scanner;  
  
public class Main {  
    public static void main(String[] args) {  
        ObjectStorage<Object> objectStorage = new ObjectStorage<>();  
        objectStorage.addObject(new ObjectT1());  
        objectStorage.addObject(new ObjectT2());  
        objectStorage.displayObjects();  
        ObjectStorage<ObjectT2> objectStorageT2 = new ObjectStorage<>();  
        objectStorageT2.addObject(new ObjectT2());  
        // objectStorageT2.addObject(new ObjectT1()); // ошибка из-за неподходящего типа  
		
    }  
}
```
### ObjectStorage.java
```java
package vladiscrafter;  
  
import java.util.ArrayList;  
import java.util.List;  
  
public class ObjectStorage<T extends Object> { // в список принимаются только объекты,  
    private List<T> objects; // исходящие из Object  
    public ObjectStorage() {  
        this.objects = new ArrayList<>();  
    }  
    public void addObject(T object) {  
        objects.add(object);  
        System.out.println(object + " добавлен в список.");  
    }  
    public void displayObjects() {  
        System.out.println("Список объектов:");  
        for(T object : objects) {  
            System.out.println("- " + object);  
        }  
    }  
}
```
### Object.java
```java
package vladiscrafter;  
  
public class Object {  
    public Object(String type) {  
    }  
}
```
### ObjectT1
```java
package vladiscrafter;  
  
public class ObjectT1 extends Object {   
    public ObjectT1() {  
        super("Object Type 1");  
    }  
}
```
### ObjectT2
```java
package vladiscrafter;  
  
public class ObjectT2 extends Object {    
    public ObjectT2() {  
        super("Object Type 2");  
    }  
}
```
# Лямбда-выражения и потоки
```java
package vladiscrafter;  
  
import java.util.List;  
import java.util.function.Consumer;  
import java.util.function.Supplier;  
  
public class Main {  
    public static void something(Runnable runnable) {  
        runnable.run();  
    }  
    public static void hi() {  
        System.out.println("Здрасте");  
    }  
    public static void main(String[] args) {  
        Runnable runnable = () -> System.out.println("Как метод, наверное?");  
        something(runnable);  
        something(Main::hi);  
        Supplier<Float> x = () -> 6.4f;  
        Consumer<Runnable> test = runnable1 -> runnable1.run();  
        test.accept(runnable);  
        Runnable method = Main::hi;  
		
        List<String> objects = List.of("One", "Two", "Three", "Four", "Five");  
		
        objects.stream() // конвертация в поток  
                .filter(object -> object.startsWith("T")) // отбор по критерию  
                .forEach(System.out::println); // вывод отобранных  
    }  
}
```
# Записи
### Record.java
```java
package vladiscrafter;  
  
public record Record(String name, int value) {  
  // и всё, ничего здесь более не нужно!
}
```
### Main.java
```java
Record record = new Record("generic_1", 10); // новая запись
System.out.println("Информация о record: " + record);  
// Record[name=generic_1, value=10]
```
# JSON
### resources -> VladisCrafter.json
```json
{  
  "playerName": "VladisCrafter",  
  "level": 66,  
  "inventory": {  
    "items": [  
      { "name": "Diamond Sword", "damage": 1562 },  
      { "name":  "Netherite chestplate", "protection":  2 },  
      { "name":  "Ender Pearl", "count":  16 }  
    ]  
  },  
  "location": {  
    "x": 2650,  
    "y": 144,  
    "z": 1440  
  },  
  "isCreativeMode": true  
}
```