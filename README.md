# FRANCE CREATOR V4.2 — France Cut Optimizer

V4.2 è il successore della V3.3 “ibridato” con il magazzino parametrico della V4.1.
Mantiene la lettura operativa per pacco della V3.3, ma sostituisce la scelta greedy della V4.1 con un'ottimizzazione globale dei fabbisogni compatibili.

## Cosa cambia nell'ottimizzatore

- Il fabbisogno produttivo è **esatto**: non vengono creati pezzi non richiesti per riempire una tavola.
- Il motore genera gli schemi compatibili con i pacchi realmente attivi in magazzino e costruisce un problema globale di taglio.
- La fase principale usa una **rilassata lineare globale** sugli schemi di taglio; la parte intera residua viene chiusa con una ricerca esatta/beam sulla coda. Se il problema diventa troppo grande, resta disponibile un fallback euristico con rifinitura locale.
- Uno stesso componente può essere distribuito fra pacchi di lunghezza diversa quando questo migliora l'incastro complessivo.
- Il numero minimo assoluto di tavole/travetti non è un vincolo: una o più unità grezze aggiuntive sono ammesse se riducono sensibilmente lo scarto morto.
- Lo **scarto morto** ha una penalità crescente: pochi centimetri sono tollerati, gli sfridi più importanti diventano rapidamente costosi per l'ottimizzatore.
- Le misure di **recupero utile** restano paracadute: salvano materiale quando conviene, ma ogni pezzo archiviato ha un costo di gestione per evitare il comportamento eccessivamente “salva tutto” della V3.3.
- A parità pratica il motore tende a contenere recuperi utili, pezzi grezzi usati e numero di schemi.
- Kerf prudenziale: **0,5 cm per taglio**.

## Tracciabilità visiva V4.2

- **Bordo verde** = famiglia TAVOLE.
- **Bordo arancio** = famiglia TRAVETTI.
- La **tonalità cambia** quando cambia lo spessore/sezione rilevante: ad esempio tavole 2,2 e 1,8 hanno due verdi diversi; travetti 9,5×4,1 e 7,5×4,1 hanno due aranci diversi.
- Ogni elemento/gabbione riceve automaticamente un **simbolo neutro** nella propria distinta (◆ ▲ ★ ● ...).
- Nell'ottimizzazione lo stesso simbolo ricompare **colorato in base al componente** e accompagnato dal nome corto: `◆ Testate`, `◆ Fondo`, `◆ Coperchio`, `◆ Piantoni`, ecc.
- La combinazione **simbolo + componente** resta coerente anche se il fabbisogno viene distribuito fra pacchi diversi.
- `Testate finali esterne` è stato semplificato in **Testate**.

## Magazzino e compatibilità

- Tavole: lunghezza + spessore; larghezza opzionale con checkbox.
- Se tutte le tavole attive dello spessore richiesto hanno larghezza dichiarata, il conteggio è esatto.
- Se almeno una larghezza è ignota, il piano rimane a pannelli senza inventare il numero di tavole.
- Travetti: lunghezza + due lati della sezione obbligatori.
- Sezioni e spessori vengono confrontati normalizzando al decimo di centimetro, senza tolleranze “fuzzy”.
- Materiale mancante o troppo corto blocca il piano con errore esplicito.

## Gabbione

Per quote interne, la ricetta corrente mantiene le formule V4.1. La voce `Testate finali esterne` è rinominata `Testate` senza modificarne la geometria.
Tavolette e rinforzi restano esclusi dall'ottimizzatore/volume finché la loro sezione di magazzino non viene formalizzata.

## Compatibilità dati

La V4.2 continua a usare la chiave `franceCreatorV4` di localStorage, così i dati della V4.1 restano leggibili.
