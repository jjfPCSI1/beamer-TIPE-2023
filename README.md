# Présentation beamer à destination de l'épreuve orale de TIPE

Le présent dépôt contient un template de présentation [LaTeX beamer](https://latex-beamer.com/)
spécialement préparé en vue de l'épreuve de TIPE.

## Organisation

Le fichier `fichier_principal.tex` contient les inclusions de structures qui
sont réparties comme suit:
* `preambule/special_beamer.tex` contient les déclarations spécifiques à beamer
* `preambule/autres_packages.tex` contient les import d'autres packages qui peuvent être utile
* `preambule/macros.tex` contient quelques définitions de commandes: c'est là
que vous devriez mettre vos définitions personnelles et il y en a quelques-unes de prédéfinies pour vous, en particulier
	* `\U` permet de composer facilement les unités en respectant un minimum de convention (caractères en romains, espace automatique entre nombre et unité). On l'utilise de la sorte: `$g = 9{,}81 \U{m.s^{-2}}$`
	* `\ofg` permet de mettre son argument entre guillemets: `entre \ofg{guillemets}`
	* `\dd` est un raccourci pour `\mathrm{d}` qui fait un d en caractères droits, ce qui devrait être utilisé dans les dérivées: `$\frac{\dd r}{\dd t}$` pour la dérivée de r par rapport à t
	* `\pa` met des parenthèses dont la taille s'adapte à son argument: `$\pa{\int_0^\infty\mathrm{e}^{-t/\tau}\,\dd t$`
	* `\pac` fait pareil avec des crochets
	* `\paa` itou avec des accolades
	* `\Cte` introduit une constante (en caractères droits)
	* `\e` permet de mettre en indice des lettres en caractères droit, comme pour une énergie potentielle: `$E\e{p}$` qui est un raccourci pour `$E_{\text{p}$`
	* `\vectoriel` est un raccourci pour le symbole du produit vectoriel qui a un nom bizarre (`\wedge`) en LaTeX
* puis vient la définition du titre du TIPE, de l'auteur et de la session avant le début de la présentation proprement dite.
* `00_titre_et_tdm.tex` ne devrait pas être touché, il se contente d'appeler à afficher les informations définies juste avant.
* `01_premiere_partie.tex` correspond aux premières diapos pour la première partie de l'exposé
* `02_deuxieme_partie.tex` pareil pour la deuxième partie
* `03_troisieme_partie.tex` pour la troisième (mais on pourrait en rajouter une quatrième si on veut ou supprimer celle-ci, as you wish)
* `04_conclusion.tex`, comme, souvent, trois parties suffisent, ce fichier a vocation à contenir les frame de conclusion
* `05_annexes.tex`, enfin, contient toutes les diapos annexes qui ne font pas à proprement parler partie de la présentation mais pourraient être utilies lors des questions du jury
* `exemples.tex` pour sa part a vocation a être supprimé de la présentation et se contente de présenter quelques exemples d'utilisation de syntaxe beamer ou LaTeX
* le dossier `figures/` vise à contenir les images que vous voulez inclure dans votre présentation, histoire que cela ne traîne pas un peu partout dans le dossier principal. N'oubliez pas de réduire leur taille au maximum sans empiéter sur la qualité: nul besoin d'avoir une photo à 5Mo pour juste voir un bécher sur une table.
