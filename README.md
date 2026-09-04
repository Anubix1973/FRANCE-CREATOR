# FRANCE CREATOR V3.2 — Fincantieri + Cut Optimizer

Estende FRANCE CREATOR V3.1 con la nuova tipologia **Cassa tipo Fincantieri**.

## Ricetta Fincantieri
Le quote della ricetta sono interne nette. `t` è lo spessore delle tavole/pannelli (default 2,2 cm), `f` lo spessore dei legni fondo (default 5 cm).

- Fondo: TAGLIO = larghezza interna; SVILUPPO = lunghezza interna.
- Legni fondo: lunghezza interna + 2t; direzione lunghezza.
- Legni sotto fondo: larghezza interna + 2t; direzione larghezza.
- Testate: TAGLIO = altezza interna + t; SVILUPPO = larghezza interna.
- Listelli testate: larghezza interna + 2t.
- Altezze: TAGLIO = altezza interna + t + f; SVILUPPO = lunghezza interna + 2t.
- Coperchio: TAGLIO = larghezza interna + 2t; SVILUPPO = lunghezza interna + 2t.
- Listelli coperchio: lunghezza interna + 4t (con t=2,2 → +8,8 cm).

Le quantità di legni e listelli sono campi modificabili. Default iniziali: 3 legni fondo, 3 legni sotto fondo, 2 listelli per testata, 2 listelli coperchio.

## Cut Optimizer 2,2 cm
Rimane invariato rispetto alla V3.1:
- pacchi 401,5 / 450 / 504 cm;
- perdita lama prudenziale 0,5 cm per taglio;
- archivio scarti De Martini / Leani / Slate&Marble;
- combinazioni miste eseguite per lotti;
- i legni fondo/sotto Fincantieri sono esclusi dall’ottimizzatore 2,2 cm, mentre pannelli e listelli da 2,2 cm sono inclusi.
