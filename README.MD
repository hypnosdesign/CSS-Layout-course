#### Margini verticali che collassano.
- Si può risolvere in due modi. O si mette al tag figlio un margine 0, o si aggiunge del padding al padre.
es. ho un wrapper che contiene un H1. Sull'H1 posso dare margine 0, oppure posso aggiungere del padding al wrapper.


#### Note

If there is no content, padding, or border area to interrupt two touching margins, the margins collapse to the largest of the two margin values.
You may experience margins collapsing in adjacent elements like paragraphs and divs.
If a div's bottom margin is larger than the top margin of the div below it, the margin area between the divs collapses to the largest of the two margin values.

- Risorse:
https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing