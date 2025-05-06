```markdown
# 🌾 Meadows

**Meadows** este un joc 2D de tip adventure/sandbox dezvoltat în C# folosind framework-ul [MonoGame](https://www.monogame.net/). Jucătorul explorează o lume naturală unde poate colecta, folosi și planta resurse. Jocul combină mecanici simple de explorare, inventar și interacțiune cu mediul, într-o lume pixelată cu atmosferă relaxantă.

---

## 📁 Structura proiectului

Meadows/  
├── Meadows.Content/ # Conținut multimedia (sprites, sunete, fonturi, hărți)  
├── Meadows.Entities/ # Entități din joc (jucător, plante, iteme)  
├── Meadows.Items/ # Sisteme pentru iteme, unelte, resurse  
├── Meadows.Levels/ # Clasele ce definesc nivelul/harta  
├── Meadows.Scenes/ # Scenele jocului (meniu, joc, splash screen)  
├── Meadows.Tiles/ # Tile-uri și foi de sprite-uri  
├── Meadows.Utility/ # Sisteme auxiliare (sunet, input)  
├── Program.cs # Punctul de intrare în aplicație  
├── Main.cs # Inițializarea și logica de bază  
├── README.md # Documentația proiectului

---

## 🛠️ Tehnologii și librării utilizate

- **C#** – Limbajul principal al proiectului
- **MonoGame** – Framework pentru dezvoltarea jocurilor 2D
- **.mgcb** – MonoGame Content Builder (pentru gestionarea fișierelor media)
- **CSV** – Folosit pentru definirea nivelelor

---

## 🎮 Despre joc

În **Meadows**, jucătorul controlează un personaj care:

- **Explorează o lume naturală** formată din plaje, iarbă, apă și stânci.
- **Colectează iteme** de pe jos, fiecare cu un damage diferit.
- **Folosește aceste iteme** pentru a ataca și distruge plante.
- **Primește drop-uri** de la plantele distruse (de exemplu: morcovi).
- **Poate planta** aceste plante înapoi pe terenuri de iarbă.
- **Navighează prin apă și pământ** fără restricții de mișcare.
- **Folosește o bară de iteme (hotbar)** similară cu cea din Minecraft (fără inventar mare momentan).

---

## ✨ Funcționalități implementate

✅ Mișcare liberă pe hartă  
✅ Navigație prin apă și pământ  
✅ Sistem de iteme cu damage  
✅ Două tipuri de plante distrugibile  
✅ Drop de iteme și sistem de plantare  
✅ Hotbar funcțional  
✅ Coliziuni și logică de interacțiune cu mediu

---

## 📸 Imagini din joc

> 📷 Adaugă aici capturi de ecran din joc (de exemplu în `assets/screenshots/`)

![screenshot1](assets/screenshots/gameplay1.png)
![screenshot2](assets/screenshots/gameplay2.png)
![screenshot3](assets/screenshots/planting.png)

---

## 🎥 Video de prezentare

> 🎞️ Adaugă aici un video de gameplay încărcat pe YouTube sau local

[![Watch the video](https://img.youtube.com/vi/VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=VIDEO_ID_HERE)

---

## 🧩 Următoarele obiective

- 🔲 Adăugarea unui inventar mare (ca în Minecraft)
- 🔲 Sistem de crafting
- 🔲 Inamicii și AI de bază
- 🔲 Misiuni și progresie
- 🔲 Salvarea jocului

---

## 👨‍💻 Autor

**Avramescu Isaac Sebastian**  
Facultatea de Matematică și Informatică – Grupa 344  
Lucrare de licență – 2025

---

## 📄 Licență

Acest proiect este public și poate fi folosit în scop educativ.  
Include asset-uri grafice originale și sunete pentru uz non-comercial.

```
