# Cours C++
Tu as une liste très complète des concepts de base à avancés en C++. 

---

## ✅ **1. Variables and Basic Data Types ✗**

```cpp
#include <iostream>
using namespace std;

int main() {
    // Déclaration de variables
    int age = 25;               // entier
    float taille = 1.75f;       // réel simple précision
    double poids = 70.5;        // réel double précision
    char initiale = 'A';        // caractère
    bool estMajeur = true;      // booléen
    string nom = "Ahmed";       // chaîne de caractères (nécessite #include <string>)

    // Affichage
    cout << "Nom : " << nom << endl;
    cout << "Âge : " << age << " ans" << endl;
    cout << "Taille : " << taille << " m" << endl;
    cout << "Poids : " << poids << " kg" << endl;
    cout << "Initiale : " << initiale << endl;
    cout << "Est majeur ? " << estMajeur << endl;

    return 0;
}
```

---

## ✅ **2. Const 🚫**

```cpp
#include <iostream>
using namespace std;

int main() {
    const float PI = 3.14159f;  // constante : valeur qui ne change jamais

    // PI = 3.14; ❌ Erreur : on ne peut pas modifier une constante

    cout << "La valeur de PI est : " << PI << endl;

    return 0;
}
```

---

## ✅ **3. Namespaces 📛**

```cpp
#include <iostream>

// Exemple sans utiliser namespace std
int main() {
    std::cout << "Bonjour sans using namespace std;" << std::endl;

    return 0;
}
```

✅ Il est courant d'écrire en haut :

```cpp
using namespace std;
```


---

## ✅ **4. Typedef and Type Aliases 🙋‍♂️**

```cpp
#include <iostream>
using namespace std;

typedef unsigned int uint;  // ancien style (C style)
using uint2 = unsigned int; // moderne (C++11)

int main() {
    uint age = 30;
    uint2 annee = 2025;

    cout << "Âge : " << age << ", Année : " << annee << endl;

    return 0;
}
```

---

## ✅ **5. Arithmetic Operators 🧮**

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10, b = 3;

    cout << "Addition : " << a + b << endl;      // 13
    cout << "Soustraction : " << a - b << endl;  // 7
    cout << "Multiplication : " << a * b << endl;// 30
    cout << "Division : " << a / b << endl;      // 3 (division entière)
    cout << "Modulo : " << a % b << endl;        // 1 (reste)

    return 0;
}
```

---

## ✅ **6. Type Conversion ✨**

```cpp
#include <iostream>
using namespace std;

int main() {
    int entier = 10;
    float reel = 3.5;

    // conversion implicite
    float resultat = entier + reel;  // 13.5

    // conversion explicite (cast)
    int conv = (int)reel;  // 3

    cout << "Résultat : " << resultat << ", Reel converti : " << conv << endl;

    return 0;
}
```

---

## ✅ **7. User Input ⌨️**

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

    cout << "Bonjour " << nom << ", tu as " << age << " ans." << endl;

    return 0;
}
```

---

## ✅ **8. Useful Math Functions 🔢**

```cpp
#include <iostream>
#include <cmath>  // Bibliothèque mathématique
using namespace std;

int main() {
    cout << "Racine carrée de 16 : " << sqrt(16) << endl;
    cout << "Puissance 2^4 : " << pow(2, 4) << endl;
    cout << "Valeur absolue de -9 : " << abs(-9) << endl;
    cout << "Arrondi de 4.6 : " << round(4.6) << endl;
    cout << "Plafond de 4.2 : " << ceil(4.2) << endl;
    cout << "Plancher de 4.8 : " << floor(4.8) << endl;

    return 0;
}
```

---

## ✅ **9. Hypotenuse Calculator 📐**

```cpp
#include <iostream>
#include <cmath>
using namespace std;

int main() {
    float a, b;

    cout << "Entrer le côté a : ";
    cin >> a;
    cout << "Entrer le côté b : ";
    cin >> b;

    float hypotenuse = sqrt(pow(a, 2) + pow(b, 2));
    cout << "L'hypoténuse est : " << hypotenuse << endl;

    return 0;
}
```

---

## ✅ **10. If Statements 🤔**

```cpp
#include <iostream>
using namespace std;

int main() {
    int age;
    cout << "Entrez votre âge : ";
    cin >> age;

    if (age >= 18) {
        cout << "Vous êtes majeur." << endl;
    } else if (age > 12) {
        cout << "Vous êtes un adolescent." << endl;
    } else {
        cout << "Vous êtes un enfant." << endl;
    }

    return 0;
}
```

---

## ✅ **11. Switch Statement 🔀**

```cpp
#include <iostream>
using namespace std;

int main() {
    int choix;
    cout << "Entrez un nombre de 1 à 3 : ";
    cin >> choix;

    switch (choix) {
        case 1:
            cout << "Vous avez choisi UN." << endl;
            break;
        case 2:
            cout << "Vous avez choisi DEUX." << endl;
            break;
        case 3:
            cout << "Vous avez choisi TROIS." << endl;
            break;
        default:
            cout << "Choix invalide." << endl;
    }

    return 0;
}
```

---

## ✅ **12. Console Calculator Program 🖩**

```cpp
#include <iostream>
using namespace std;

int main() {
    char op;
    double a, b;

    cout << "Entrez une opération (+ - * /) : ";
    cin >> op;
    cout << "Entrez deux nombres : ";
    cin >> a >> b;

    switch (op) {
        case '+': cout << a + b << endl; break;
        case '-': cout << a - b << endl; break;
        case '*': cout << a * b << endl; break;
        case '/': 
            if (b != 0) cout << a / b << endl;
            else cout << "Erreur : division par zéro !" << endl;
            break;
        default: cout << "Opérateur invalide." << endl;
    }

    return 0;
}
```

---

## ✅ **13. Ternary Operator ❓**

```cpp
#include <iostream>
using namespace std;

int main() {
    int age;
    cout << "Entrez votre âge : ";
    cin >> age;

    string message = (age >= 18) ? "Majeur" : "Mineur";
    cout << message << endl;

    return 0;
}
```

---

## ✅ **14. Logical Operators 🔣**

```cpp
#include <iostream>
using namespace std;

int main() {
    bool a = true;
    bool b = false;

    cout << "a && b : " << (a && b) << endl; // false
    cout << "a || b : " << (a || b) << endl; // true
    cout << "!a : " << (!a) << endl;         // false

    return 0;
}
```

---

## ✅ **15. Temperature Conversion Program 🌡️**

```cpp
#include <iostream>
using namespace std;

int main() {
    float celsius;
    cout << "Entrez la température en °C : ";
    cin >> celsius;

    float fahrenheit = (celsius * 9 / 5) + 32;
    cout << "La température en °F est : " << fahrenheit << endl;

    return 0;
}
```

---

## ✅ **16. Useful String Methods 〰️**

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string phrase = "Bonjour Ahmed";

    cout << "Longueur : " << phrase.length() << endl;
    cout << "Premier caractère : " << phrase[0] << endl;
    cout << "Trouver 'Ahmed' : " << phrase.find("Ahmed") << endl;

    string sub = phrase.substr(8, 5);  // extrait "Ahmed"
    cout << "Substring : " << sub << endl;

    return 0;
}
```
---
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0));
    int secret = rand() % 100 + 1;  // nombre entre 1 et 100
    int guess;
    int essais = 0;

    do {
        cout << "Devine le nombre (1-100) : ";
        cin >> guess;
        essais++;

        if (guess < secret) cout << "Trop petit !" << endl;
        else if (guess > secret) cout << "Trop grand !" << endl;
        else cout << "Bravo ! Trouvé en " << essais << " essais." << endl;

    } while (guess != secret);

    return 0;
}
---
Parfait Ahmed 🙌 ! On continue alors avec les **boucles en C++** (super importantes 🔁) et on arrive bientôt aux jeux (🎲 Devine le nombre, ✊ Pierre Feuille Ciseaux, etc.). Voici la suite bien claire et commentée :

---

## ✅ **17. While Loops ♾️**

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 1;

    while (i <= 5) {
        cout << "Compteur : " << i << endl;
        i++; // incrémentation
    }

    return 0;
}
```

🧠 *Utilise `while` quand tu ne sais pas encore combien de fois tu vas boucler.*

---

## ✅ **18. Do While Loops 🔃**

```cpp
#include <iostream>
using namespace std;

int main() {
    int nombre;

    do {
        cout << "Tapez un nombre positif : ";
        cin >> nombre;
    } while (nombre < 0);

    cout << "Merci, vous avez entré : " << nombre << endl;

    return 0;
}
```

📌 *`do-while` s'exécute au moins **une fois**, même si la condition est fausse au départ.*

---

## ✅ **19. For Loops 🔂**

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 5; i++) {
        cout << "i vaut : " << i << endl;
    }

    return 0;
}
```

🧮 *Boucle `for` : idéale pour répéter un bloc un nombre **connu** de fois.*

---

## ✅ **20. Break & Continue 💔**

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 10; i++) {
        if (i == 5) continue; // saute 5
        if (i == 8) break;    // sort à 8

        cout << i << " ";
    }

    return 0;
}
```

---

## ✅ **21. Nested Loops ➿**

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int ligne = 1; ligne <= 3; ligne++) {
        for (int col = 1; col <= 5; col++) {
            cout << "*";
        }
        cout << endl; // retour à la ligne
    }

    return 0;
}
```

🎨 *Affiche un petit rectangle d’étoiles (3 lignes × 5 colonnes)*

---

## ✅ **22. Random Number Generator 🎲**

```cpp
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0)); // initialise l'aléatoire

    int nombre = rand() % 10 + 1; // entre 1 et 10
    cout << "Nombre aléatoire : " << nombre << endl;

    return 0;
}
```

---

## ✅ **23. Random Event Generator 🎁**

```cpp
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0));

    int chance = rand() % 3;

    if (chance == 0) cout << "🎉 Gagné un iPhone !" << endl;
    else if (chance == 1) cout << "💸 Gagné 100€ !" << endl;
    else cout << "😢 Rien gagné..." << endl;

    return 0;
}
```

---

## ✅ **24. Number Guessing Game ↕️**

```cpp
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    srand(time(0));
    int secret = rand() % 100 + 1;  // nombre entre 1 et 100
    int guess;
    int essais = 0;

    do {
        cout << "Devine le nombre (1-100) : ";
        cin >> guess;
        essais++;

        if (guess < secret) cout << "Trop petit !" << endl;
        else if (guess > secret) cout << "Trop grand !" << endl;
        else cout << "Bravo ! Trouvé en " << essais << " essais." << endl;

    } while (guess != secret);

    return 0;
}
```
