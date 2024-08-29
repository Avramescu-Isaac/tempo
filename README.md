Da, pot să te ajut cu exercițiul din imagine. Hai să trecem prin fiecare punct pe rând și să vedem ce relație ar trebui să existe între ele.

### 1. \(\mathbb{E}[\log(X)]\) vs. \(\log(\mathbb{E}[X])\)

Aceasta este o aplicație a inegalității lui Jensen, care afirmă că pentru o funcție concavă \(f\) și o variabilă aleatoare \(X\):
\[
\mathbb{E}[f(X)] \leq f(\mathbb{E}[X])
\]
Funcția \(\log\) este concavă, deci:
\[
\mathbb{E}[\log(X)] \leq \log(\mathbb{E}[X])
\]
Deci răspunsul este **≤**.

### 2. \(\mathbb{E}[X]\) vs. \(\sqrt{\mathbb{E}[X^2]}\)

Folosing inegalitatea Cauchy-Schwarz:
\[
\mathbb{E}[X]^2 \leq \mathbb{E}[X^2]
\]
rezultă că:
\[
\mathbb{E}[X] \leq \sqrt{\mathbb{E}[X^2]}
\]
Deci răspunsul este **≤**.

### 3. \(\mathbb{E}[\sin^2(X)] + \mathbb{E}[\cos^2(X)]\) vs. 1

Folosind identitatea trigonometrică:
\[
\sin^2(X) + \cos^2(X) = 1
\]
și aplicând așteptarea, avem:
\[
\mathbb{E}[\sin^2(X)] + \mathbb{E}[\cos^2(X)] = \mathbb{E}[1] = 1
\]
Deci răspunsul este **=**.

### 4. \(P(X > c)\) vs. \(\frac{\mathbb{E}[X^3]}{c^3}\)

Aici putem folosi inegalitatea Markov:
\[
P(X > c) \leq \frac{\mathbb{E}[X^3]}{c^3}
\]
Deci răspunsul este **≤**.

### 5. \(P(X \leq Y)\) vs. \(P(X \geq Y)\)

Pentru două variabile aleatoare i.i.d. \(X\) și \(Y\), probabilitățile ca \(X \leq Y\) și \(X \geq Y\) sunt egale, deoarece distribuțiile lor sunt simetrice. Deci răspunsul este **=**.

### 6. \(P(X + Y > 10)\) vs. \(P(X > 5\) sau \(Y > 5)\)

Folosind inegalitatea Boole:
\[
P(X + Y > 10) \geq P(X > 5 \text{ sau } Y > 5)
\]
Deci răspunsul este **≥**.

### 7. \(\mathbb{E}[\min(X, Y)]\) vs. \(\min(\mathbb{E}[X], \mathbb{E}[Y])\)

Folosind din nou inegalitatea Jensen, de data aceasta pentru funcția convexă \(\min\), avem:
\[
\mathbb{E}[\min(X, Y)] \leq \min(\mathbb{E}[X], \mathbb{E}[Y])
\]
Deci răspunsul este **≤**.

### 8. \(\frac{\mathbb{E}[X]}{\mathbb{E}[Y]}\) vs. \(\mathbb{E}\left[\frac{X}{Y}\right]\)

Folosind inegalitatea Jensen pentru funcția convexă \(\frac{1}{Y}\) (sub presupunerea că \(Y > 0\)):
\[
\mathbb{E}\left[\frac{X}{Y}\right] \geq \frac{\mathbb{E}[X]}{\mathbb{E}[Y]}
\]
Deci răspunsul este **≤**.

### 9. \(\mathbb{E}[X^2(X^2 + 1)]\) vs. \(\mathbb{E}[X^2(Y^2 + 1)]\)

Deoarece \(X\) și \(Y\) sunt variabile i.i.d., avem:
\[
\mathbb{E}[X^2(X^2 + 1)] = \mathbb{E}[X^2]\mathbb{E}[X^2 + 1]
\]
și 
\[
\mathbb{E}[X^2(Y^2 + 1)] = \mathbb{E}[X^2]\mathbb{E}[Y^2 + 1]
\]
Deci răspunsul este **=**.

### 10. \(\mathbb{E}\left[\frac{1}{X}\right]\) vs. \(\frac{1}{\mathbb{E}[X]}\)

Folosind inegalitatea Jensen pentru funcția convexă \(\frac{1}{X}\) (presupunând \(X > 0\)):
\[
\mathbb{E}\left[\frac{1}{X}\right] \geq \frac{1}{\mathbb{E}[X]}
\]
Deci răspunsul este **≥**.

Sper că aceste explicații sunt utile! Dacă ai alte întrebări sau nelămuriri, nu ezita să întrebi!
