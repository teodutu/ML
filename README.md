# ML
Machine Learning - UPB 2021



## Laboratoare
### Laborator 1 - K-means
Se implementeaza algoritmul *K-means* pentru clusterizare, cu centroizii alesi
in 3 moduri:
- aleator
- prin metoda *K-means++*
- prin algoritmul *Kaufman*

Se compara scorurile *Rand Index* ale algoritmului pentru primele 2 situatii de
mai sus, iar rezultatele sunt in general similare. Pentru anumite (cateva)
numere de clustere si anumite dataseturi, *K-means++* da rezultate **putin** mai
bune.


### Laborator 2 - Arbori de decizie
Se implementeaza clasificarea unor seturi de date prin 3 algoritmi:
- `randomTree` - atributul fiecarui nod e ales aleator
- `id3` - atributul fiecarui nod este cel ce maximizeaza `gain`-ul
- `randomForest` - o colectie de arbori aleatori, fiecare fiind antrenat pe un
subset din exemplele de antrenament

Apoi, se compara acuratetile, preciziile si regasirilor acestor modele,
observandu-se cand apare fenomenul de *overfitting* la `randomForest` si ca
pe masura ce adancimea unui arbore aleator creste, forma si felul in care acesta
ia decizia se aseamana tot mai mult cu cele ale unui model antrenat cu
algoritmul `id3`.


### Laborator 3 - Regresie liniara
Se implementeaza un model clasic de regresie liniara: unul fara si altul cu
regularizare si se observa ca primul are *overfitting* cand setul de antrenare e
mic, pe cand cel de-al doilea se comporta mai bine chiar si pe seturi mici de
antrenare.


### Laborator 4 - Boosting
Se compara `AdaBoost` si `GradientBoost` cu arbori de decizie chiori +
`RandomForest`. Cam la fel de vrajeala ca si pana acum :(.


### Laborator 5 - SVM
O basina copiata probabil de
[aici](https://xavierbourretsicotte.github.io/SVM_implementation.html).
Ecuatiile nu-s explicate deloc, iar codul n-are sens mai deloc. Era mai misto la
IA. Macar acolo parea ca-i pasase cuiva de laburi.


### Laborator 6 - Reinforcement Learning
Se gaseste o planificare pentru a ajunge dintr-o pozitie in alta intr-un
labirint 2D, folosind atat *Policy Iteration*, cat si *Value Iteration*.


### Laborator 7 - Q Learning
Se implementeaza algoritmul *Q Learning* to pentru a rezolva un labirint 2D.
Ca de obicei, trebui bulaniti hiperparametri pana da bine. O mizerie. Era mai
misto la IA.



## Teme
### Tema 1 - Clasificare
Se compara mai multi algoritmi de clasificare: *Random Forest*, *XGBoost*,
*SVM*, *Naive Bayes* si *K-means*. O mizerie de tema in care doar luam modelele
din `sklearn` si tunam hiperparametrii. Un fel de `from keras import ...` :(.
