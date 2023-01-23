SKETCH TO IMAGE PROJECT AVEC PYTORCH
-------------------------
<p class = "justify">
Notre projet consiste à utiliser les auto encodeurs pour obtenir des images à partir de dessins (des formes tracées à l'aide d'un crayon). La force des auto-encodeurs, s'il sont bien régularisés, est qu'ils sont capables de procurer des images en sortie cohérentes avec des images fournies en entrée. Pour ce faire les auto-encodeurs utilisent deux outils principaux:


- L'encodeur: Qui permet de transformer les images en variables latentes (exemple: des logits),
- Le décodeur: Qui permet de transformer les variables latentes en images.
<p class = "justify">

Ainsi notre but sera de faire en sorte que les variables latentes soit entièrement régularisées, autrement dit que chaque variable puissent décrire correctement les images fournies en entrées, pour qu'on puisse ensuite comparer les images fournies en sortie aux vraies images grâce à une fonction de perte (voire deux pour obtenir plus de précision). 
</p>

```html
<div class = "background: white;">
![autoencoder]("https://miro.medium.com/max/828/1*qFzKC1GqOR17XaiQBex83w.webp")
</div>
```
#### Contexte

Dans ce projet, nous allons traiter deux types d'images:

- En entrée: Les 'rendered sketch' (données en format svg ou png) qui sont les dessins des objets (**Grayscale**). Lien pour télécharger -> [sketch_link](https://drive.google.com/file/d/1_AIxKnZXQms5Ezb-cEeVIDIoVG-eliHc/view)
- En sortie: Les 'sketch' (données en format png) qui sont les images originaux en **RGB**. 

![rgb_to_sketch](https://mtli.github.io/sketch/img/Wild-half.jpg)

