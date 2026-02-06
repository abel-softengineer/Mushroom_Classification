# Mushroom Classification Project

Ez a projekt egy gombák osztályozására szolgáló gépi tanulási modell, amely fizikai tulajdonságok (kalapátmérő, tönk magassága stb.) alapján jósolja meg, hogy egy gomba ehető (**e**) vagy mérgező (**p**).

## 🚀 Áttekintés
A szkript egy **K-Nearest Neighbors (KNN)** algoritmust használ az osztályozáshoz. A folyamat magában foglalja az adatok tisztítását, a hiányzó értékek pótlását (imputation) és a kategóriás adatok numerikussá alakítását (encoding).

## 📊 Adathalmaz jellemzői
A modell az alábbi oszlopokat használja a tanuláshoz:
* `stem-height`: Tönk magassága
* `stem-width`: Tönk vastagsága
* `cap-diameter`: Kalap átmérője
* `cap-shape`: Kalap formája (kódolt)
* `cap-color`: Kalap színe (kódolt)
* `ring-type`: Gyűrű típusa (kódolt)
* `has-ring`: Van-e gyűrűje (bináris: 0 vagy 1)

## 🛠️ Megvalósítás lépései
1.  **Adattisztítás**: 
    * A hiányzó `cap-diameter` értékeket a mediánnal pótoljuk.
    * A hiányzó `ring-type` értékeket a leggyakoribb elemmel (mode) helyettesítjük.
2.  **Preprocessing**:
    * `OrdinalEncoder` segítségével a szöveges kategóriákat számokká alakítjuk.
    * A `has-ring` oszlopot bináris (0/1) formátumra hozzuk.
3.  **Modellezés**:
    * **Algoritmus**: K-Nearest Neighbors (n=5).
    * **Tanítás**: Az `input.csv` fájl alapján (80-20% vonat-teszt felosztás mellett).
4.  **Predikció**:
    * A modell a `validation.csv` fájl adataira készít jóslatokat.
    * Az eredményeket egy `pred.txt` fájlba menti.

## 💻 Használat
A futtatáshoz szükséged lesz a következő könyvtárakra:
```bash
pip install pandas matplotlib numpy scikit-learn
