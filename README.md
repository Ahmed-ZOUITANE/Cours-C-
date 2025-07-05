Bien sûr Ahmed ! Voici un **cours C++ complet et progressif**, **parfait pour les débutants jusqu’aux intermédiaires**, avec des explications claires, exemples commentés et sections bien structurées.

---

# 🎓 **Cours Complet en C++**

---

## 📦 Partie 1 : Introduction au langage C++

### ✅ Qu’est-ce que le C++ ?

* Langage compilé, rapide, multi-paradigmes.
* Hérité de C, mais avec la programmation orientée objet.
* Utilisé dans : systèmes embarqués, jeux, logiciels lourds, finance...

### ✅ Premier programme

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Bonjour le monde !" << endl;
    return 0;
}
```

---

## 🧱 Partie 2 : Les bases du langage

### 🔢 Types de données

| Type     | Description             | Exemple               |
| -------- | ----------------------- | --------------------- |
| `int`    | entier                  | `int age = 25;`       |
| `float`  | nombre à virgule simple | `float pi = 3.14f;`   |
| `double` | nombre à virgule double | `double x = 5.67;`    |
| `char`   | caractère               | `char lettre = 'A';`  |
| `bool`   | booléen                 | `bool actif = true;`  |
| `string` | chaîne de caractères    | `string nom = "Ali";` |

📌 Pour `string`, inclure : `#include <string>`

---

### ⚙️ Opérateurs arithmétiques

```cpp
int a = 10, b = 3;
cout << a + b << endl;  // Addition
cout << a - b << endl;  // Soustraction
cout << a * b << endl;  // Multiplication
cout << a / b << endl;  // Division entière
cout << a % b << endl;  // Modulo
```

---

### 📥 Entrée utilisateur

```cpp
#include <iostream>
using namespace std;

int main() {
    string nom;
    int age;

    cout << "Entrez votre nom : ";
    cin >> nom;

    cout << "Entrez votre âge : ";
    cin >> age;

    cout << "Bonjour " << nom << ", vous avez " << age << " ans." << endl;
    return 0;
}
```

---

## 🔄 Partie 3 : Contrôle de flux

### ✅ Conditions (if / else)

```cpp
if (age >= 18) {
    cout << "Majeur";
} else {
    cout << "Mineur";
}
```

### ✅ Switch

```cpp
switch (choix) {
    case 1: cout << "Un"; break;
    case 2: cout << "Deux"; break;
    default: cout << "Inconnu"; break;
}
```

### ✅ Opérateur ternaire

```cpp
string statut = (age >= 18) ? "Majeur" : "Mineur";
```

---

## 🔁 Partie 4 : Boucles

```cpp
// Boucle for
for (int i = 0; i < 5; i++) {
    cout << i << " ";
}

// Boucle while
int i = 0;
while (i < 5) {
    cout << i << " ";
    i++;
}

// Boucle do while
int x;
do {
    cout << "Tapez un nombre positif : ";
    cin >> x;
} while (x < 0);
```

---

## 📚 Partie 5 : Fonctions

```cpp
// Déclaration
int carre(int x) {
    return x * x;
}

int main() {
    cout << carre(4);  // Affiche 16
    return 0;
}
```

✅ Passage par référence

```cpp
void doubler(int& x) {
    x *= 2;
}
```

---

## 📌 Partie 6 : Tableaux et boucles

```cpp
int notes[3] = {15, 18, 12};

// Boucle for
for (int i = 0; i < 3; i++) {
    cout << notes[i] << endl;
}

// Boucle foreach (C++11+)
for (int note : notes) {
    cout << note << endl;
}
```

---

## 🧠 Partie 7 : Pointeurs

```cpp
int x = 10;
int* ptr = &x;

cout << *ptr << endl;  // Affiche 10 (déréférencement)
```

---

## 🧱 Partie 8 : Structures (struct)

```cpp
struct Personne {
    string nom;
    int age;
};

Personne p1 = {"Ali", 20};
cout << p1.nom;
```

---

## 🧍 Partie 9 : Programmation Orientée Objet (POO)

```cpp
class Animal {
public:
    string nom;
    void parler() {
        cout << nom << " fait un bruit." << endl;
    }
};

int main() {
    Animal a;
    a.nom = "Chien";
    a.parler();
}
```

### 🔁 Héritage

```cpp
class Chien : public Animal {
public:
    void parler() {
        cout << nom << " aboie." << endl;
    }
};
```

---


