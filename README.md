#
## Задание 1
Дана грамматика. Постройте вывод заданной цепочки.
#
- a.
    ```
     S : T | T '+' S | T '-' S;
     T : F | F '*' T;
     F : 'a' | 'b';
     ```
    Цепочка:  ```a - b * a + b```.

**S** -> T - **S** -> T - T + **S** -> **T** - T + T -> F - **T** + T -> F - F * **T** + T -> F - F * F + **T** -> **F** - F * F + F -> a - **F** * F + F -> a - b * **F** + F -> a - b * a + **F** -> a - b * a + b

S →  (T-S )→  (T-T+S) →   (T-T+T )→  (T-T+F )→  (T-T+b) →  (T-F*T+b) → (T-F*F+b) → (T-F*a+b) → (T-b*a+b) → (F-b*a+b) → (a- b*a+b) 

- b.
    ```
    S : 'a' S B C | 'ab' C;
    C B : B C;
    'b' B : 'bb';
    'b' C : 'bc' ;
    'c' C : 'cc';
    ```
    Цепочка: ```aaabbbccc```.

**S** -> a **S** B C -> a a **S** B C B C -> a a a b **C B** C B C -> a a a b B C **C B** C -> a a a b B **C B** C C -> a a a **b B** B C C C -> a a a b **b B** C C C -> a a a b b **b C** C C ->  a a a b b b **c C** C -> a a a b b b c **c C** -> a a a b b b c c 

S → (aSBC) → (aaSBCBC) → (aaabCBCBC) → (aaabBCCBC) → (aaabbCCBC) → (aaabbCBCC) → (aaabbBCCC) → (aaabbbCCC) → (aaabbbcCC) → (aaabbbccC) → (aaabbbccc)

#
