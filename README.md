# FRANCE CREATOR V4.2.2

## Patch leggibilità sequenze di taglio

Questa versione mantiene **invariato il motore France Cut Optimizer V4.2.1** e modifica soltanto la presentazione operativa degli schemi esatti.

### Nuova lettura macchina

Una riga del tipo:

`3 travetti → 120,4 ★Piantoni + 99,0 ◆Travetti fondo + 79,0 ▲Travetti fondo + 2 × 74,0 ★Travetti fondo`

viene ora presentata così:

`3 travetti`  
`→ 1 × 120,4 ★Piantoni`  
`→ 1 × 99,0 ◆Travetti fondo`  
`→ 1 × 79,0 ▲Travetti fondo`  
`→ 2 × 74,0 ★Travetti fondo`

Nessuna etichetta “Schema 1 / Schema 2”: la quantità di tavole o travetti è già l’intestazione operativa sufficiente.

- Quantità + misura sono allineate verticalmente per parlare direttamente con la macchina.
- Simbolo, colore e nome componente restano identici alla V4.2.1 e servono come informazione secondaria di destinazione.
- Recuperi utili, scarto morto, bordi materiale, stampa chiara e logica di ottimizzazione restano invariati.
- Cache PWA aggiornata a `france-creator-v4-2-2`.
- Dati salvati ancora sulla chiave `franceCreatorV4`: nessuna migrazione necessaria.
