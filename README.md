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


### Laborator 8 - MLP
Se clasifica cifrele din [MNIST](https://en.wikipedia.org/wiki/MNIST_database)
folosind o retea *MLP* cu 2 straturi si un *ReLU* intre ele. Acuratetea fara
inertie e 95.61%, iar cu inertie 97.81%.


### Laborator 9 - Retele convolutionale
Aceeasi problema ca labul trecut, dar cu o retea *LeNet*. Acuratetea nu creste
cand modelului i se adauga inertie, pentru ca modelul se satureaza.


### Laborator 10 - ResNet
Parca putin mai ok explicat decat labul trecut, se implementeaza *ResNet-50* si
se testeaza pe *CIFAR*. Dureaza mult antrenarea, drept care n-am rulat toate 200
de epocie. Csf? Ncsf.


### Laborator 11 - Algoritmi genetici
Se implementeaza un algoritm genetic are rezolva problema rucsacului. Adica se
porneste cu o populatie initiala de 1000 de alegeri random ale obiectelor, iar
la fiecare noua generatie sunt pastrati 100 de indivizi care se reproduc aleator
(se combina inceputul unui set de obiecte de la un individ cu sfarsitul de la
altul) rezultand alti 900 de indivizi s.a.m.d. timp de 100 de generatii.



## Teme
### Tema 1 - Clasificare
Se compara mai multi algoritmi de clasificare: *Random Forest*, *XGBoost*,
*SVM*, *Naive Bayes* si *K-means*. O mizerie de tema in care doar luam modelele
din `sklearn` si tunam hiperparametrii. Un fel de `from keras import ...` :(.


### Tema 2 - Q-Learning
Se implementeaza *Q-Learning* si *SARSA* si iar se cauta acul in carul cu fan
(hiperparametrii optimi). E interesant totusi ca pentru anumite recompense,
algoritmii nu converg. De exemplu, cand recompensa pentru o miscare simpla e 0
si nu -1, *SARSA* nu mai are de ce sa invete nimic si toate Q-urile sunt 0. Dar
tot o mizerie e in care cea mai mare parte din timp se pierde asteptand sa
ruleze `for in for in for ...`.


### Tema 3 - Clasificare de fete
Se folosesc un *MLP*, un *CNN* si o combinatie de *VGG* + *SVM* ca sa se
clasifice fete. Se foloseste setul de date
[Labeled Faces in the Wild](http://vis-www.cs.umass.edu/lfw/).

Pe scurt, orice model are acurateti mici pe intreg setul de date ca-s prea
multe fete si nu intelege nimic din ele. Cand se reduce setul de date la
cele mai numeroase 5 clase, *MLP*-ul si *CNN*-ul ajung pe la 80-90%, iar
combo-ul de *VGG* + *SVM* la 57%. Un cacat de tema...
