#### Margini verticali che collassano.
- Si può risolvere in due modi. O si mette al tag figlio un margine 0, o si aggiunge del padding al padre.
es. ho un wrapper che contiene un H1. Sull'H1 posso dare margine 0, oppure posso aggiungere del padding al wrapper.


#### Note

If there is no content, padding, or border area to interrupt two touching margins, the margins collapse to the largest of the two margin values.
You may experience margins collapsing in adjacent elements like paragraphs and divs.
If a div's bottom margin is larger than the top margin of the div below it, the margin area between the divs collapses to the largest of the two margin values.

- Risorse:
https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing

## Container
- Solitamente per centrare il contenuto, e solo quello, si applicano dei div con classe "container". Quindi si lascia invariato l'header e il footer e si centra il conuto dando alla classe container gli stessi valori dati precedentemente al wrapper. In questo caso il wrapper va eliminato. Il footer, se non contiene elementi complessi, come altri div, può non avere il suo container, basta solo dare un allineamente del testo centrale.

## Mobile first Approach

- Si scrive prima lo stile css per il mobile con le media queries si va ad modificare il layout per il desktop. In questa lezione abbiamo sotituito i valori del container con del padding per la versione mobile, e messo quei valori in una media queries di 769px. Alla fine abiamo utilizzato il selettore universale (*) per dare a tutti gli elementi la proprietà box-sizing con valore border-box, questo per evitare che il padding aggoiunto precedentemente andasse a vanificare il break di 769px della media quesries. Infatti senza questa proprietà il padding viene aggiunto alla larghezza del container.

## Creating a Sticky Footer

- Questa lezione è incentrata su una tecnica per realizzare uno sticky footer basata sulla funzione calc() di css e sul valore vh (Viewport Height). In sostanza si mette tutto il contenuto in un wrap a cui si da il valore .wrap { min-height: calc(100vh - 89px);} 89px è l'altezza del footer, non è un valore fisso, dipende dall'altezza del vostro footer. 100vh è il 100% della vostra visualizzazione a schermo. 1vh equivale a 1% della vostra viewport.