Hai să rezolvăm exercițiul 3 din al doilea model de examen, care se bazează pe găsirea unei **SLD-respingere** pentru un program Prolog. 

### Exercițiul 3 din al doilea model:

Program Prolog:
```prolog
shuffle(lit(X), lit(X)).
shuffle(arb(X, Y, Z), arb(T, U, W)) :- shuffle(X, U), shuffle(Y, W), shuffle(Z, T).
```

**Ținta:**
```prolog
shuffle(X, arb(lit(t), lit(c), lit(u)), arb(lit(i), lit(a), lit(t), lit(i), lit(e), lit(r))).
```

Trebuie să găsim o **SLD-respingere** pentru programul de mai sus și să determinăm valoarea lui `X` în substituția calculată.

### Rezolvare:

1. **Pasul 1: Începem cu rezolvarea goal-ului.**

   ```prolog
   shuffle(X, arb(lit(t), lit(c), lit(u)), arb(lit(i), lit(a), lit(t), lit(i), lit(e), lit(r))).
   ```

2. **Pasul 2: Aplicăm prima regulă `shuffle/2` pentru a descompune termenii.**

   Observăm că regula de bază:
   ```prolog
   shuffle(lit(X), lit(X)).
   ```
   nu se poate aplica direct, deoarece termenii nu sunt de forma `lit(X)`.

3. **Pasul 3: Aplicăm a doua regulă `shuffle/2` pentru a descompune arborele.**

   A doua regulă are forma:
   ```prolog
   shuffle(arb(X, Y, Z), arb(T, U, W)) :- shuffle(X, U), shuffle(Y, W), shuffle(Z, T).
   ```

   Aplicând această regulă:
   - `X = arb(X1, Y1, Z1)` pentru unii termeni `X1`, `Y1`, `Z1`.
   - Goal-urile devin:
     ```prolog
     shuffle(X1, lit(i)), shuffle(Y1, lit(a)), shuffle(Z1, arb(lit(t), lit(i), lit(e), lit(r))).
     ```

4. **Pasul 4: Descompunem `shuffle(X1, lit(i))`.**

   Dacă `X1 = lit(i)`, goal-ul `shuffle(lit(i), lit(i))` se poate rezolva folosind prima regulă `shuffle/2`. 

   - Substituția devine: `{X1 = lit(i)}`.
   - Noua listă de goal-uri devine:
     ```prolog
     shuffle(Y1, lit(a)), shuffle(Z1, arb(lit(t), lit(i), lit(e), lit(r))).
     ```

5. **Pasul 5: Descompunem `shuffle(Y1, lit(a))`.**

   Similar, dacă `Y1 = lit(a)`, goal-ul `shuffle(lit(a), lit(a))` se poate rezolva folosind prima regulă `shuffle/2`.

   - Substituția devine: `{Y1 = lit(a)}`.
   - Noua listă de goal-uri devine:
     ```prolog
     shuffle(Z1, arb(lit(t), lit(i), lit(e), lit(r))).
     ```

6. **Pasul 6: Descompunem `shuffle(Z1, arb(lit(t), lit(i), lit(e), lit(r)))`.**

   Aplicăm din nou regula a doua de shuffle:
   - `Z1 = arb(Z11, Z12, Z13)`.
   - Goal-urile devin:
     ```prolog
     shuffle(Z11, lit(t)), shuffle(Z12, lit(i)), shuffle(Z13, arb(lit(e), lit(r))).
     ```

7. **Pasul 7: Continuăm decompoziția cu `shuffle(Z11, lit(t))`, `shuffle(Z12, lit(i))`, și `shuffle(Z13, arb(lit(e), lit(r)))`.**

   - `shuffle(Z11, lit(t))` se rezolvă dacă `Z11 = lit(t)`.
   - `shuffle(Z12, lit(i))` se rezolvă dacă `Z12 = lit(i)`.
   - `shuffle(Z13, arb(lit(e), lit(r)))` se rezolvă printr-o altă descompunere:
     - `Z13 = arb(Z131, Z132)`, și goal-urile devin:
       ```prolog
       shuffle(Z131, lit(e)), shuffle(Z132, lit(r)).
       ```
     - `shuffle(Z131, lit(e))` se rezolvă dacă `Z131 = lit(e)`.
     - `shuffle(Z132, lit(r))` se rezolvă dacă `Z132 = lit(r)`.

8. **Pasul 8: Finalizarea substituției.**

   Avem următoarele substituții:
   - `X1 = lit(i)`
   - `Y1 = lit(a)`
   - `Z11 = lit(t)`
   - `Z12 = lit(i)`
   - `Z131 = lit(e)`
   - `Z132 = lit(r)`

   Deci, substituția completă pentru `X` este:

   ```prolog
   X = arb(lit(i), lit(a), arb(lit(t), lit(i), arb(lit(e), lit(r)))).
   ```

9. **Concluzie:**

   Valoarea lui `X` în substituția calculată este:
   ```prolog
   arb(lit(i), lit(a), arb(lit(t), lit(i), arb(lit(e), lit(r)))).
   ```

Acesta este răspunsul pentru exercițiul 3 din al doilea model de examen. Dacă ai întrebări sau vrei mai multe detalii, spune-mi!
