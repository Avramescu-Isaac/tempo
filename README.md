### 1. **Crearea Materialului Nou**
1. Creează un material nou:
   - În **Content Browser**, clic dreapta → **Material** → Denumește-l `M_GlitterStars`.
2. Deschide materialul pentru editare.

---

### 2. **Crearea Sclipiciului cu "Stele"**
1. **Zgomot pentru Randomizare:**
   - Adaugă un nod **Noise**:
     - Setează:
       - **Scale**: între 50 și 200 (ajustabil pentru densitatea punctelor sclipitoare).
       - **Quality**: 2 sau 3 pentru mai multe detalii.
       - Conectează un nod **Time** la intrarea **Position** a nodului `Noise` pentru a anima sclipiciul (steluțele vor apărea și dispărea).
   - **Rezultat**: Acesta creează o distribuție de puncte "aleatoare".

2. **Controlul Sclipirii:**
   - Creează un nod **Sine**:
     - Adaugă un nod `Time` și conectează-l la nodul `Sine`.
     - Conectează ieșirea nodului `Sine` la un nod **Multiply** împreună cu nodul `Noise`.
     - Acest pas face ca punctele să lumineze intermitent.

3. **Threshold pentru Stele:**
   - Adaugă un nod **If**:
     - Conectează ieșirea din `Multiply` la pinul **A** al nodului `If`.
     - Creează un nod `Constant` cu valoarea `0.7` (sau ajustează) și conectează-l la pinul **B**.
     - Configurează:
       - **A >= B**: Setează la `1` (zonele stelare luminoase).
       - **A < B**: Setează la `0` (zonele întunecate).

---

### 3. **Adăugarea Culorii la Stele**
1. Creează un nod **Constant3Vector** pentru culoarea stelelor (alb, galben, sau orice culoare preferată) și conectează-l la un nod **Multiply** împreună cu ieșirea din `If`.
2. Conectează rezultatul acestui nod la **Emissive Color** pentru a face stelele să strălucească.

---

### 4. **Culoarea Fundalului**
1. Creează o culoare de fundal:
   - Adaugă un nod `Constant3Vector` pentru culoarea materialului de bază.
   - Conectează-l direct la **Base Color**.

---
