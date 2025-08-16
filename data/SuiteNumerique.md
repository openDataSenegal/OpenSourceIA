# **Cours sur les Suites Numériques**

---

## **1. Introduction**

En mathématiques, une **suite numérique** est une liste ordonnée de nombres réels (ou parfois entiers, rationnels, etc.) définie selon une règle ou une formule. Elle est utilisée pour modéliser des phénomènes évolutifs dans le temps (croissance, intérêts composés, populations, etc.).

---

## **2. Définition d'une suite numérique**

Une **suite numérique** est une fonction définie sur l’ensemble des entiers naturels (ou une partie de cet ensemble) à valeurs dans l’ensemble des nombres réels.

On note généralement une suite par :  
\[
(u_n)_{n \in \mathbb{N}} \quad \text{ou} \quad (u_n)_{n \geq 0}
\]

- \( u_n \) est le **terme de rang** \( n \) (ou **terme général** de la suite).
- L'entier \( n \) est appelé **indice** ou **rang**.

> **Exemple** :  
La suite définie par \( u_n = 2n + 1 \) donne :  
\( u_0 = 1, \, u_1 = 3, \, u_2 = 5, \, u_3 = 7, \, \dots \)

---

## **3. Modes de génération d'une suite**

### **3.1. Suite définie par une formule explicite**

Le terme \( u_n \) est exprimé directement en fonction de \( n \).

\[
u_n = f(n)
\]

> **Exemple** :  
\( u_n = n^2 - 1 \) → \( u_0 = -1, \, u_1 = 0, \, u_2 = 3, \, u_3 = 8 \)

---

### **3.2. Suite définie par récurrence**

Le terme \( u_{n+1} \) est défini à partir du terme précédent \( u_n \), souvent avec une **formule de récurrence** et une **valeur initiale**.

\[
\begin{cases}
u_0 = a \\
u_{n+1} = f(u_n)
\end{cases}
\]

> **Exemple** :  
\( u_0 = 2 \), \( u_{n+1} = 3u_n - 1 \)  
Alors :  
\( u_1 = 3 \times 2 - 1 = 5 \)  
\( u_2 = 3 \times 5 - 1 = 14 \), etc.

---

## **4. Représentation graphique d'une suite**

On peut représenter une suite dans un repère en plaçant les points de coordonnées \( (n, u_n) \).

> **Remarque** :  
Contrairement à une fonction continue, une suite est **discrète** : elle n’est définie que pour des valeurs entières de \( n \).

---

## **5. Sens de variation d'une suite**

On dit qu'une suite \( (u_n) \) est :

- **Croissante** si pour tout \( n \), \( u_{n+1} \geq u_n \)
- **Décroissante** si pour tout \( n \), \( u_{n+1} \leq u_n \)
- **Strictement croissante** si \( u_{n+1} > u_n \)
- **Strictement décroissante** si \( u_{n+1} < u_n \)
- **Stationnaire** (ou constante) si \( u_{n+1} = u_n \) pour tout \( n \)
- **Monotone** si elle est croissante ou décroissante

### **Méthodes pour étudier le sens de variation**

1. **Étudier le signe de \( u_{n+1} - u_n \)**  
   - Si \( u_{n+1} - u_n \geq 0 \), la suite est croissante.
   - Si \( u_{n+1} - u_n \leq 0 \), elle est décroissante.

2. **Si \( u_n > 0 \) pour tout \( n \), étudier \( \frac{u_{n+1}}{u_n} \)**  
   - Si \( \frac{u_{n+1}}{u_n} \geq 1 \), la suite est croissante.

3. **Utiliser une fonction associée**  
   Si \( u_n = f(n) \), et si \( f \) est croissante/décroissante sur \( [a, +\infty[ \), alors \( (u_n) \) a le même sens de variation à partir du rang \( a \).

> **Exemple** :  
Soit \( u_n = n^2 - 4n \)  
\( u_{n+1} - u_n = (n+1)^2 - 4(n+1) - (n^2 - 4n) = 2n - 3 \)  
Donc :  
- Pour \( n < 1.5 \), \( u_{n+1} - u_n < 0 \) → suite décroissante  
- Pour \( n > 1.5 \), \( u_{n+1} - u_n > 0 \) → suite croissante

---

## **6. Suite majorée, minorée, bornée**

- **Majorée** : il existe un réel \( M \) tel que \( u_n \leq M \) pour tout \( n \)
- **Minorée** : il existe un réel \( m \) tel que \( u_n \geq m \) pour tout \( n \)
- **Bornée** : si elle est à la fois majorée et minorée

> **Exemple** :  
\( u_n = \frac{1}{n+1} \) pour \( n \geq 0 \)  
- Minorée par 0 (car \( u_n > 0 \))  
- Majorée par 1 (car \( u_0 = 1 \), puis décroît)  
→ Donc bornée.

---

## **7. Limite d'une suite**

On dit qu'une suite \( (u_n) \) **converge** vers un réel \( \ell \) si, lorsque \( n \) devient très grand, \( u_n \) se rapproche de \( \ell \). On note :

\[
\lim_{n \to +\infty} u_n = \ell
\]

Si une suite ne converge pas, elle est **divergente**. Elle peut tendre vers \( +\infty \), \( -\infty \), ou ne pas avoir de limite (ex : \( u_n = (-1)^n \)).

### **Propriétés des limites**

- Une suite croissante et majorée converge.
- Une suite décroissante et minorée converge.
- Toute suite convergente est bornée.

---

## **8. Suites arithmétiques**

### **Définition**
Une suite \( (u_n) \) est **arithmétique** s’il existe un réel \( r \) (la **raison**) tel que :

\[
u_{n+1} = u_n + r
\]

### **Terme général**
\[
u_n = u_0 + n r \quad \text{ou} \quad u_n = u_p + (n - p)r
\]

### **Somme des termes**
Somme des \( n+1 \) premiers termes (de \( u_0 \) à \( u_n \)) :

\[
S = u_0 + u_1 + \dots + u_n = (n+1) \times \frac{u_0 + u_n}{2}
\]

> **Exemple** :  
\( u_0 = 2 \), \( r = 3 \) → \( u_n = 2 + 3n \)  
\( u_5 = 2 + 15 = 17 \)  
Somme de \( u_0 \) à \( u_5 \) : \( S = 6 \times \frac{2 + 17}{2} = 6 \times 9.5 = 57 \)

---

## **9. Suites géométriques**

### **Définition**
Une suite \( (u_n) \) est **géométrique** s’il existe un réel \( q \) (la **raison**) tel que :

\[
u_{n+1} = q \times u_n
\]

### **Terme général**
\[
u_n = u_0 \times q^n \quad \text{ou} \quad u_n = u_p \times q^{n-p}
\]

### **Somme des termes**
Si \( q \neq 1 \), somme des \( n+1 \) premiers termes :

\[
S = u_0 + u_1 + \dots + u_n = u_0 \times \frac{1 - q^{n+1}}{1 - q}
\]

> **Exemple** :  
\( u_0 = 1 \), \( q = 2 \) → \( u_n = 2^n \)  
\( u_4 = 16 \)  
Somme de \( u_0 \) à \( u_4 \) : \( S = 1 \times \frac{1 - 2^5}{1 - 2} = \frac{1 - 32}{-1} = 31 \)

### **Limite d'une suite géométrique**

- Si \( |q| < 1 \), alors \( \lim u_n = 0 \)
- Si \( q = 1 \), \( u_n = u_0 \) (constante)
- Si \( q > 1 \) et \( u_0 > 0 \), \( \lim u_n = +\infty \)
- Si \( q < -1 \), la suite diverge (pas de limite)

---

## **10. Exemples d'applications**

### **Exemple 1 : Intérêts composés**
Un capital \( C_0 = 1000 \) € placé à 3 % par an avec intérêts composés suit une suite géométrique :

\[
C_n = 1000 \times (1{,}03)^n
\]

### **Exemple 2 : Population**
Une population augmente de 100 habitants par an : suite arithmétique de raison 100.

\[
P_n = P_0 + 100n
\]

---

## **11. Comportement asymptotique et croissances comparées**

Certaines suites croissent plus vite que d'autres :

\[
\text{Constante} < \log n < n^\alpha \, (\alpha > 0) < a^n \, (a > 1) < n!
\]

> **Exemple** :  
\( \lim_{n \to \infty} \frac{2^n}{n^2} = +\infty \) → l’exponentielle domine la puissance.

---

## **12. Raisonnement par récurrence**

Méthode puissante pour démontrer des propriétés sur les suites.

### **Principe**
Pour démontrer qu'une propriété \( P(n) \) est vraie pour tout \( n \geq n_0 \) :

1. **Initialisation** : Vérifier que \( P(n_0) \) est vraie.
2. **Hérédité** : Supposer \( P(k) \) vraie pour un \( k \geq n_0 \), et montrer que \( P(k+1) \) est vraie.
3. **Conclusion** : Par récurrence, \( P(n) \) est vraie pour tout \( n \geq n_0 \).

> **Exemple** :  
Montrer que \( u_n = 2^n \) pour la suite \( u_0 = 1 \), \( u_{n+1} = 2u_n \)

- Initialisation : \( u_0 = 1 = 2^0 \) → OK
- Hérédité : Supposons \( u_k = 2^k \), alors \( u_{k+1} = 2u_k = 2 \times 2^k = 2^{k+1} \)
- Conclusion : vrai pour tout \( n \)

---

## **13. Exercices types (à faire en autonomie)**

1. Étudier le sens de variation de \( u_n = \frac{n}{n+1} \)
2. Calculer \( u_5 \) pour la suite définie par \( u_0 = 1 \), \( u_{n+1} = u_n + 2n \)
3. Montrer par récurrence que \( 1 + 2 + \dots + n = \frac{n(n+1)}{2} \)
4. Trouver la limite de \( u_n = 5 \times (0{,}8)^n \)

---

## **Résumé**

| Type de suite        | Formule de récurrence     | Terme général           | Somme des \( n+1 \) premiers termes |
|----------------------|----------------------------|--------------------------|--------------------------------------|
| Arithmétique         | \( u_{n+1} = u_n + r \)   | \( u_n = u_0 + nr \)     | \( (n+1)\frac{u_0 + u_n}{2} \)       |
| Géométrique          | \( u_{n+1} = q u_n \)     | \( u_n = u_0 q^n \)      | \( u_0 \frac{1 - q^{n+1}}{1 - q} \)  |

---

## **Conclusion**

Les suites numériques sont un outil fondamental en mathématiques, en particulier pour modéliser des évolutions discrètes. Maîtriser leur définition, leur sens de variation, leurs types classiques (arithmétique, géométrique), et les méthodes comme la récurrence, est essentiel pour aborder l’analyse, les probabilités, et les sciences appliquées.

---

> **À retenir** :  
> - Une suite est une fonction sur \( \mathbb{N} \)  
> - On étudie sa variation, sa borne, sa limite  
> - Les suites arithmétiques et géométriques ont des formules simples  
> - Le raisonnement par récurrence est indispensable