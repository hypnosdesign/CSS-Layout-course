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