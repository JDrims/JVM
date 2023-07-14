```java

public class JvmComprehension {

    public static void main(String[] args) {
        int i = 1;                      // 1. в стэке присваивает переменной i значение 1
        Object o = new Object();        // 2. выделяет память в куче для объекта Object 
        // и присваивает ссылку в стэке переменной о
        Integer ii = 2;                 // 3. выделяет память в куче для объекта Integer 
        // со значением int и присваивает переменной ii значение 2
        printAll(o, i, ii);             // 4. выделяет память в стэке под метод printAll 
        // в параметрах: выделяет память в куче для объекта Object и передает ссылку переменной о,
        // передает переменной i значение 1, выделяет память в куче для объекта Integer со значением
        // int и передает ссылку переменной ii значение 2
        System.out.println("finished"); // 5. выделяет память в стэке под метод println выделяет память
        // в куче для объекта String и передает ссылку в переменную в методе
    }

    private static void printAll(Object o, int i, Integer ii) {
        Integer uselessVar = 700;                   // 6. выделяет память в куче для объекта Integer
        // со значением int и при присваивает переменной uselessVar значение 700
        System.out.println(o.toString() + i + ii);  // 7. выделяет память в стэке под метод println, выделяет
        // память в куче для объекта String, выполняется действия сложений в строку и передает ссылку в параметр метода
    }
}

```