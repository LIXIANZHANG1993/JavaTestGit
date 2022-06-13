- ## 1. 以下對於Java Language的敘述，何者為非
  - 1.Java是一種向後兼容的語言
  - 2.Java是一種物件導向的語言
  - 3.Java是一種半開源的語言，另一半由Oracle掌握並管理
  - 4.Java是一種跨平台性的語言

Ans: 3



- ## 2. 下列何種順序是Java程式在Windows平台的執行流程

  - 1.撰寫 Java 程式 -> 利用Windows平台內建的 Javac 編譯器，編譯產生Windows的machine code -> 交由Windows執行
  - 2.撰寫 Java 程式 -> 利用JDK裡面的Javac編譯器，編譯產生 JVM 可執行的Java byte code ->利用 JVM 的 JIT / Java Interprter，編譯產生Windows可執行的machine code ->  交由Windows執行
  - 3.撰寫 Java 程式 -> 利用Windows平台內建的 Javac編譯器，編譯產生 JVM 可執行的Java byte code ->利用 JVM 的 JIT / Java Interprter，編譯產生Windows可執行的machine code ->  交由Windows執行
  - 4.撰寫 Java 程式 -> 利用JDK裡面的Javac編譯器，編譯產生 JVM 可執行的machine code ->利用 JVM 的 JIT / Java Interprter，編譯產生Windows可執行的Java byte code ->  交由Windows執行

Ans: 2 ![](assets/java_execution_flow.png)

- ## 3. 下列程式碼中，何者為錯
  - 1.char a = '中';
  - 2.char b = 'b';
  - 3.char c = '\t';
  - 4.char d = '-98';

Ans: 4 char變量不能爲負值。字符數據類型的範圍爲0到65535

- ## 4. 下列程式碼中，何者正確
  - 1.Object $event = new Object();
  - 2.Object name = new Object();
  - 3.Object false = new Object();
  - 4.Object _name = new Object();
  
Ans: 2 Java命名方式不能以 底線,$,數字 開頭，且不能使用保留字

- ## 5.將一個int 變數 a = 5， 與另一個 short 變數 b = 120 相加，不能使用下列何種類型的變數儲存其值
  - 1.int
  - 2.short
  - 3.float
  - 4.Interger

Ans: 2 Java中數值類型的變數相加，會自動提升為容量大的變數類型，另外此容量並不是依據占用記憶體的空間去比較，而是用表示「數字」的範圍去比較
       例如:float占用4個位元組，而long占用8個位元組，但兩者相加如果使用long類型的變數儲存，會報錯

- ## 6. 下列何者關於 record 紀錄類別的敘述為非
  - 1.record class 會幫我們自動生成了 toString(), hashCode() 和equals()方法
  - 2.record class 會幫我們自動生成了 toString(), getter() 和 setter()方法
  - 3.record class 的狀態是 immutable 的，也不能在類別本體去定義非 static 的 fiel 並且不能被繼承等限制
  - 4.Java 16以後，紀錄類別才成為正式特性

Ans: 2, record class並不會生成 setter()方法，紀錄類別在語義上，就是作為不可變動的資料載體，在JEP 395一開頭的摘要，就明確地寫到「記錄類別就是不可變資料的透明載體（transparent carriers ）」，透明指的是，無論是在名稱、結構、狀態上，記錄類別都明確地曝露、表現出來，沒有任何隱藏。(<https://www.ithome.com.tw/voice/147531>)

- ## 7. 以下程式碼中，變數 a , b , sum 的結果分別為何? 
  ```
     public static void main(String[] args) {
        int a = 10;
        int b = 10;
        int sum = a++ + b;
        System.out.println("a:" + a);
        System.out.println("b:" + b);
        System.out.println("sum:" + sum);
    }
  ```
  - 1.a = 11, b = 10, sum = 21
  - 2.a = 11, b = 10, sum = 21
  - 3.a = 10, b = 10, sum = 20
  - 4.a = 10, b = 10, sum = 20

Ans: 1 , 此程式碼中，a 會先用後加，故結果為20 ，而 a 為 11


- ## 8. 以下程式碼中，會輸出何種結果

  ``` 
  public static void main(String[] args) {
     int[] arr = new int[5];
        System.out.println(arr[5]);
    }
  ```
  - 1.零
  - 2.一
  - 3.五
  - 4.Index 5 out of bounds for length 5

Ans: 4 

- ## 9. 以下程式碼中，會輸出何種結果

  ```
  public static void main(String[] args) {
     int[] arr = new int[5];
        System.out.println(arr[0]);
    }
  ```

  - 1.零
  - 2.一
  - 3.五
  - 4.Index 5 out of bounds for length 5

Ans: 1 ， 若未初始化陣列元素，Java 會根據陣列型別給予預設值，而 int 型別的預設值為 0

