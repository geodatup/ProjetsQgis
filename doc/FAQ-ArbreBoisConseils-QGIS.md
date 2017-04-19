###Comment garder la bordure extérieure d’un polygone noire si je mets un remplissage transparent à 50% ?

Il faut `dupliquer` et faire un second style de couche. Les données ne seront pas dupliquées.

###Comment renommer un champ ? (Table Manager refuse)

Table manager n'est plus maintenue. Il faut utiliser `refactor field` ou en français `factoriser les champs` . Ce traitement est disponible dans `Boite à outils de traitement`>`Géotraitement QGIS` > `Outils de table vecteur`

Pour afficher la `boite à outil`, aller dans `Vue`> `Panneaux`

Pour afficher l'interface avancée, en bas du panneaux boite à outil, séléctionner dans la liste déroulante `Advanced interface`



###Comment déplacer des étiquettes avec la souris ? (souvent mal placées)

Définir emplacement `libre (lent)` dans `style de couche` > `zone de texte` > l'onglet `placement`


###Comment récupérer la légende créée pour un autre projet ?

Faire un `clic droit` sur la couche et `enregistrer en tant que fichier de définition de couche`

Pour charger le style, aller dans les `propriétés de couche` > `Style` >  `bouton Style` (en bas) > `charger`.



###Peut-on fabriquer puis importer un menu déroulant importable pour remplir un champ de table attributaire ?

Oui, avec des tables en relation, puis des formulaires de saisie. 
C'est expliqué [ici](http://docs.qgis.org/2.14/fr/docs/user_manual/working_with_vector/attribute_table.html?highlight=formulaire#definition-relation-manager).


###Comment avoir le(s) WMS dans l’image ou le pdf exporté du composeur ??
Normalement, c'est standard. J'ai vu dans ton projet que ça ne fonctionne pas en effet. 
La projection du WMS SCANEXPRESS est WGS84 et il y a une reprojection à la volée lambert. Le soucis vient de là. 
En supprimant le  WMS SCANEXPRESS puis en l'ajoutant en lambert93 (2154), l'impression fonctionnera bien.
J'ai remarqué qu'il faut ajouter le wms via l'outil `Ajouter une couche WMS` ![](http://docs.qgis.org/2.14/fr/_images/mActionAddWmsLayer.png).

Si tu passes par l'explorateur le WMS est chargé en WGS84...


###Comment déplacer une carte dans le composeur d’image ? ou du moins centrer ma forêt !
oui, soit tu fais un centrage sur la carte et dans composeur tu fais `rafraichir la vue`.
Sinon, il y a un outil dans la barre de gauche pour déplacer le contenu de la carte ![](http://docs.qgis.org/2.14/fr/_images/mActionMoveItemContent.png).

Attention à vérifier que l'objet carte est bien modifiable ![](http://docs.qgis.org/2.14/fr/_images/locked.png)

###Peut-on grouper Points et Lignes dans une couche (Equipements) ?
Non, mais tu peux créer un groupe de couche.


###Comment importer et utiliser des symboles ? (liste cfr ci-dessous « Equipements »).

La réponse est [ici](http://docs.qgis.org/2.14/fr/docs/user_manual/working_with_vector/style_library.html?highlight=symbol#the-symbol-selector).
