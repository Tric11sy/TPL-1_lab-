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


**S** →  (**T** - **S**) → (**T** - **T** + **S**) → (**T** - **T** + **T**) → (**T** - **T** + **F**) → (**T** - **T** + b) → (**T** - **F** * **T** + b) → (**T** - **F** * **F** + b) → (**T** - **F** * a + b) → (**T** - b * a + b) → (**F** - b * a + b) → (a - b * a + b) 

- b.
    ```
    S : 'a' S B C | 'ab' C;
    C B : B C;
    'b' B : 'bb';
    'b' C : 'bc' ;
    'c' C : 'cc';
    ```
    Цепочка: ```aaabbbccc```.



**S** → (a**SBC**) → (aa**SBCBC**) → (aaab**CBCBC**) → (aaab**BCCBC**) → (aaabb**CCBC**) → (aaabb**CBCC**) → (aaabb**BCCC**) → (aaabbb**CCC**) → (aaabbbc**CC**) → (aaabbbcc**C**) → (aaabbbccc)

#
