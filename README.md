# vueComponent
## création de composants vuejs
vue est un framwork component  
il faut comprendre :  
interaction avec le dom, comment est composée une instance vue avec l'objet qui nous permetait  
d'initialiser un instance vue  
un component c'est quoi : 
une petite brique qui va composer votre application vuejs  
chaqu'une de ces briques aura une partie visuelle qui correspont à un template HTML
et une partie logique qui va intéragire avec ce template HTML
ces components sont defini par un selector qui vas vous permettre de les utilisers dans vos page HTML  
on va pouvoir reutiliser les comonents a plusieurs endroit sans à voir à les recoder  
quel type de component on peut creer ?  
comment les creers  
et toute les possibilitées offertes par se produit  
**un composant est une instance Vue**  
# creer un composant 
utiliser un key dans l'instance vue 
template : '  '  
ce qu'il y aa l'interieur de template vas remplacer ce qu'il y aa l'interieur <div id="app"> dans le html. 
el : va identifier dans le dom ou il faut installer ou positionner l'insatnce et remplacer par la Key Template.  
template : ' ' doit etre une chaine de caractère.  ` ` template litérale pour plusieur ligne.  
## le nom des tags :
pour ne pas avoir de problème avec l'api native HTML 
donc les noms des Tags natif  
toujours bien préfixer les Noms des composants exemples :
my-test, app-test, 

## différence entre le component et l'instance vue principal  
1. dans le component quand on ecrit notre template il faut avoir un route element  
ce qui veut dire qu'il me faut qu'une seule, une div parent <div></div> par component.  
 <div>
    <h3>My first component</h3>
    <h3>My first component</h3>
 </div>
 ca ce situe au niveau de l'alghoritme de diff de différence qui est un algoritme de vue 
 et notament sur la mise en place du virtual Dom car dans le virtual dom il y a une hiérarchie  
 qui va ce mettre en place sur les différents components en route principal notre instance vue  
 et pour pouvoir comparer cette hiérarchie de composant dans le virtual Dom il ne faut q'une seul  
 <div><div> 
 une div d'arret ou de stop
2. ## data doit etre une fonction  
pourquoi?, quand on va utiliser les components le but du jeu ca va être du coté de vue d'etre optimiser au maximum  
et de réutiliser au maximum les différentes key de notre component sans avoir a chaque fois réinstancier la totalité  
de notre objet pour tout vos component ce ne serai pas performant sauf que dans le cadre de DATA: on veut  
neccessairement avoir un DATA : par éléments  
donc typiquement quand je vais instancier mon premier <my-test><my-test>
je vais avoir mon template mon set de data sauf que quand je vais implémenter mon 2eme  
je veux que les data sois différents, pas qu' elle soit liées. sinon peut intéret d'avoir la   
possibilité de mettre plusieurs fois le component.
et pour isoler le data on va simplement le transformer en fonction et cette fonction va retourner  
un objet et cette objet sera le DATA de l'instance.  
## def fonction sur data.
le fait d'utiliser DATA comme fonction qui retourne un nouvelle objet fait que a chaque fois  
que l'on va utiliser le component <my-test> on va a chaque fois réinvoqué la methode DATA qui va   
retourner un nouvelle objet et donc la reference de notre objet DATA cera différente a chaque instanciation  
de mon component <my-test> . et que chaque component ai son propre set de DATA .  
 ## component global et local  
 le **component global** c'est comme dans l'exemple précédent  
 le **composant local** 

