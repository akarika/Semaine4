#RUBY#
--------


####Aperçu et avant-goût
Le Ruby est un langage de programmation puissant et flexible, vous pouvez l'utiliser pour vos développements web, pour traiter du texte, créer des jeux ou au sein du célèbre framework web Ruby on Rails. Le Ruby est un langage :

####Interprété
 c'est à dire que vous n'avez pas besoin de compilateur pour écrire et exécuter du Ruby. 
Orienté en fonction des objets, c'est à dire qu'il permet de manipuler des structures de données appelées objets pour construire des programmes.

####types de données en Ruby

1.**les nombres** `25`

2.**les booleans** `true``false`

3.**strings** `chaînes de caractères`


####Les varibles


Vous pouvez considérer une variable comme un mot ou un nom qui contient une valeur unique

Déclarer des variables en Ruby est facile : il suffit d'écrire un nom, comme `mon_nombre`, utiliser `=` pour lui assigner une valeur, et c'est tout.
	`mon_nombre=100`
	
	
####Les maths avec Ruby

L'addition (`+`)
La soustraction (`-`)
La multiplication (`*`)
La division (`/`)
L'exponentiation (`**`)
Le modulo (`%`)

-----------
###RUBY II###
----------

`print` ficher un texte à l'écran
`gets` méthode Ruby qui récupère "l'entrée utilisateur" 
`chomp`supprime le retour à la ligne
`puts` affiche la sortie

####Afficher la sortie

Si vous définissez une variable `singe` qui est égale à la string `King Kong`, et que vous avez une autre string qui dit` "J'ai emmené #{singe} au zoo"`. Ruby va faire quelque chose appelé *l'interpolation de chaînes de caractères* (qui n'est autre que du remplacement de mots) et remplace la partie `#{singe}` par la valeur de `singe` - c'est à dire qu'il affichera au final `"J'ai emmené King Kong au zoo.".` 

####Formater grâce aux méthodes de strings

`.upcase` majuscule
`.downcase` minuscule
`.capitalize` la 1er lettre en majuscule

 ajoutez un `!` à la fin du nom de la méthode. .`capitalize!` **modifie** donc la **string appelée** plutôt que d'en faire **une copie**. La string originale, non modifiée, est perdue pour toujours, mais vous en avez maintenant une toute nouvelle et bien mise en forme à la place.
 
-------- 
###RUBY III ###
-----------

####Les structures de contrôle###
**If (si)**

En Ruby, l'instruction `if` est suivie d'une **expression**, c'est à dire quelque chose qui a une valeur (comme `4`, `true` ou `pantalon`). Si cette expression est `true`(vraie), Ruby exécute le bloc de code qui suit le `if`. Si elle est `false` (fausse), le code qui la suit n'est pas exécuté, l'interpréteur passe directement à la suite.

Voici un exemple d'instruction if en action :
`if 1 < 2
print "Je m'affiche car un est inférieur à deux !"
end`

**Else / sinon**
La partenaire du `if` c'est l'instruction `else`. L'instruction `if`/`else` revient à écrire : "Si (if) cette expression est vraie, exécuter ce bloc de code, sinon (else) exécuter le code après le else. En voici un exemple :


`
f 1 > 2
  print "Je ne m'afficherai pas car un n'est pas supérieur à deux."
else
  print "Par contre moi je m'affiche !"`
  
  **Elsif / sinon si**
  
  Que faire si nous avons besoin de plus de deux options ? Nous avons besoin d'un `elsif` ! L'instruction `elsif` permet d'ajouter autant de conditions que vous voulez, comme ça :
  
  `
  if x < y  # En supposant que les variables x et y sont définies
  puts "x est plus petit que y !"
elsif x > y
  puts "x est plus grand que y !"
else`

**Unless / à moins que**

 vérifie si quelque chose est faux, plutôt que vrai
 
 `
 faim = false
unless faim
  puts "Je programme en Ruby !"
else
  puts "A table !"
end`

####Les comparaisons####

`==`est égal à 
`!=`différent de 
`<`plus petit que
`<=`plus petit ou égal à 
`>`plus grand que
`>=`plus grand ou égal à 


####Les valeurs booléens####

**&&** , opérateur **et**
`
true && true => true
true && false => false
false && true => false
false && false => false
`

Par exemple, `1 < 2 && 2 < 3` vaut `true` car il est vrai que 1 est plus petit que 2 et 2 est plus petit que 3.

**||**, oéprateur **ou**

Vous pouvez aussi utiliser l'opérateur **ou** (`|`|). Le `||` est appelé ou inclusif car il donne `true` si l'une ou les deux expressions sont `true`. Voici comment il fonctionne :
`true || true => true
true || false => true
false || true => true
false || false => false `


**!** , opératuer **Non**

il existe l'opérateur booléen non (`!`). Le ! transforme la valeur `true` en `false` et vice-versa :

`!true => false
!false => true`


**Combiner des opérateurs booléens**

`boolean_1 = (3 < 4 || false) && (false || true)
boolean_1 = true
boolean_2 = !true && (!true || 100 != 5**2)
boolean_2 = false
boolean_3 = true || !(true || false)
boolean_3 = true`


---------
###Boucle & itérateurs###
----------

**While**

Une boucle `while` permet de répéter une instruction tant qu'une condition est vraie.

Pour illustrer cela, nous allons faire un programme qui récite une table de multiplication. La boucle se répètera tant que l'on n'aura pas atteint 10 :

`n = 0
while n < 10 #tant que n est inférieur à 10 exécuter le code
    print n * 8 #ici la table de 8
    n = n + 1 #rajouter 1 à n pour que la boucle ne tourne pas en rond et atteigne 10
    print " "
end`

**Until**

Le complémentaire de la boucle `while` est la boucle `until`. `Until` signifie `jusqu'à ce que`, en Anglais. Elle fonctionne en quelque sorte comme une boucle while à l'envers : elle exécutera son code `tant que la condition` qu'elle contrôle est fausse. Dès que la condition devient vraie, on sort de la boucle.

`compteur = 1
until compteur > 10
  puts compteur
  compteur+=1
end`

**opérateurs d'assignation**

opérateurs d'assignation, comme par exemple `+=`, `-=`, `*=`, et `/=`. Par exemple, quand vous écrivez :

`compteur += 1`

La boucle `for` exécute des instructions pour chaque élément d'un intervalle.
Dans cet exemple, le code exécute l'instruction `print n` et permet d'afficher tous les nombres de l'intervalle :
`for n in 0...5
    print n #instruction(s)
end`
`0 1 2 3 4`

En utilisant cette syntaxe, avec `3 points`, la borne haute de est **exclue** de l’**intervalle**. Si vous voulez l'**inclure**, utilisez la même syntaxe avec seulement **deux points**.

**Boucle 'For'**

La boucle `for` exécute des instructions données pour chaque élément d'un ensemble.

`for n in (0..7)
puts n
end
=> 0 1 2 3 4 5 6 7`

`..`intervalle inclusifs `...`intervalle exclusif 
`puts n` est exécutée pour chaque élément de [0; 7], `n` prend successivement les valeurs de cet ensemble.

Une boucle `for` se termine par un end.
--------------------
**Les itétateurs**
--------------------

Les **itérateurs** permettent d'accéder, tout comme la boucle `for`, à tous les éléments d'un ensemble un à un.

* `loop`l'itérateur le plus simple est la méthode . Vous pouvez créer une boucle `loop` simple (mais infinie !) en tapant simplement :

`loop { print "Hello, world!" }`
En Ruby, en général, il est possible de remplacer les accolades` {` et `} `respectivement par `do` et `end`. Sachant cela, on peut écrire une boucle un peu plus intelligente que celle du dessus :

`i = 0
loop do
  i += 1
  print "#{i}"
  break if i > 5
end`

L'instruction break c'est notre carte "Sortie de prison" : elle arrête la boucle dès lors que la condition est remplie.

 * `next` peut être utilisé pour sauter certaines étapes de la boucle. Par exemple, si on veut afficher les nombres pairs, on peut écrire :

`i = 20
loop do
i -= 1
next if i % 2 == 0
print "#{i}
break if i <= 0
end`

* `times` est équivalente à une boucle `for` très compacte. Elle peut effectuer une tâche sur chaque élément d'un objet, un nombre spécifié de fois.

Par exemple, si nous voulions afficher `"Comment est votre blanquette ?" dix fois, nous pourrions écrire :

`10.times { print "Comment est votre blanquette ?" }`


**Tableaux**


Un *tableau* est une structure pouvant stocker des données. Des données de types différents peuvent cohabiter dans un même tableau (par exemple, un nombre et une chaîne de caractères). Un tableau est délimité par des crochets et ses éléments sont séparés par des virgules.

`tab = [] # tableau vide
prix = [30, 400, 25, 73] # tableau contenant des entiers
puts prix # affichage de toutes les valeurs du tableau
langues = ["fr", "en"] # tableau de chaînes de caractères
puts langues
mix = 4, "quatre" # tableau mixte
puts mix`

Les crochets ne sont pas obligatoires, quel que soit le type des éléments contenus dans le tableau.

Chaque élément du tableau est associé à un nombre (un entier naturel) qui représente la case du tableau qu'il occupe ; la première case correspond à l'indice 0. Un exemple pour vous éclairer :

`prix = [30, 400, 25, 73]
puts prix[3] # => 73`

Ajouter un élément à un tableau[modifier
Pour ajouter un élément à la fin de votre tableau, vous pouvez utiliser l'opérateur `<<` que vous avez déjà vu pour les chaînes de caractères (dans le chapitre consacré aux opérateurs).

Vous pouvez également vous en servir pour concaténer deux tableaux (les mettre bout à bout) :

`t = [4, 7, 3] ; s = [6, 8]
t << s
=> [4, 7, 3, [6, 8]]
Pour ajouter réellement les valeurs de s à t =
t += s
=> [1, 7, 3, 6, 8]`

**Les hachages**

Les *hachages* sont des tableaux particuliers : au lieu d'associer une valeur à son indice (la place qu'elle occupe dans le tableau), elle sera associée à une clé (un mot).

La seconde différence essentielle avec les tableaux ordinaires est l'utilisation d'accolades dans la déclaration des éléments à la place de crochets. Les **accolades** ne sont pas **facultatives**.


[badges codeacademy](https://www.codecademy.com/fr/users/akarika/achievements)
