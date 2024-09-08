Hai să rezolvăm exercițiul 1 din acest nou model de examen. Vom descrie execuția programului folosind semantica operațională big-step.

### Exercițiul 1

Avem următorul program:

``` 
while I * I ≤ N do (if I * I = N then P := 1 else skip); I := I + 1 
```

**(a) Să se descrie formal execuția lui Pgm, dintr-o stare inițială σ cu σ(N) = 30, σ(I) = 5, σ(P) = 0, folosind semantica operațională big-step sau small-step.**

### Rezolvare:

1. **Stare inițială:**
   - σ(N) = 30
   - σ(I) = 5
   - σ(P) = 0

2. **Programul:** `while I * I ≤ N do (if I * I = N then P := 1 else skip); I := I + 1`

3. **Aplica regula `while` și începe evaluarea buclei:**

   Începem să evaluăm bucla `while` pentru condiția `I * I ≤ N`.

   Starea curentă:
   - I = 5, N = 30, P = 0
   - Condiție: `5 * 5 ≤ 30` (adică `25 ≤ 30`) -> Adevărat

4. **Aplica `if-then-else`:**
   - `I * I = N` (adică `5 * 5 = 30`) -> Fals
   - Deci, se aplică ramura `else`: `skip`
   
   Starea rămâne aceeași: I = 5, N = 30, P = 0

5. **Aplica `I := I + 1`:**
   - I devine `I + 1` (adică `5 + 1 = 6`).

   Noua stare: 
   - I = 6, N = 30, P = 0

6. **Bucla continuă cu noua valoare a lui I:**
   - Condiția `6 * 6 ≤ 30` devine `36 ≤ 30`, care este falsă.

7. **Ieșirea din bucla `while`:**  
   Deoarece condiția este falsă, bucla se încheie și execuția programului se oprește.

### Starea finală:
- I = 6
- N = 30
- P = 0

**Rezultatul final:** `σ'(I) = 6`, `σ'(N) = 30`, `σ'(P) = 0`

---

**(b) Să se arate că enunțul Hoare**:

\[
\{I = 0 \land \exists K (N = K * K)\} \text{Pgm}\{P = 1\}
\]

**este demonstrabil.**

### Demonstrație:

Enunțul Hoare afirmă că, dacă inițial \(I = 0\) și există un \(K\) astfel încât \(N = K * K\), atunci, după execuția lui Pgm, \(P = 1\).

1. Condiția de intrare spune că există un \(K\) astfel încât \(N = K * K\).
2. În timpul execuției buclei, dacă \(I * I = N\), atunci \(P := 1\) și \(P = 1\) rămâne valabil.
3. Din moment ce bucla parcurge toate valorile de la 0 în sus și condiția \(I * I \leq N\) este adevărată, în final, dacă \(I * I = N\) pentru un anumit \(I\), se va seta \(P = 1\).

Astfel, enunțul Hoare este demonstrabil.

Dacă mai ai nevoie de detalii sau clarificări, spune-mi!
