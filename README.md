# md-ebook-template
Template per la creazione di progetti con documentazione in formato markdown e la generazione di ebook in PDF, ePub, HTML ... con pandoc



Struttura repository:

 

docs/*

 qui dentor ci sono tutti file *.md

 

media/*

Qui dentro ci sono tutte le immagini bitmap e vettoriali e altre risorse esterne linkate nei file md

 

metadata.txt

File dei metadati per il documento finale

Cover.tex

File tex con layout della copertina

 

dist/*

Cartella con gli artefatti. Potrebbe anche non essere inclusa nel repository

 

 per fare la build di documenti:

 

```shell
Git clone …

Git pull …

Cd <project>

 

pandoc -o dist/manuale.pdf metadata.txt docs/*.md --table-of-contents --resource-path=.:media

 

pandoc -o dist/manuale.pdf metadata.yaml docs/*.md --table-of-contents --resource-path=.:media --include-before-body cover.tex
```

 

 