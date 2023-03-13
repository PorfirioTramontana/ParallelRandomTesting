# RANDOM PARALLEL TESTING   
## USING RANDOOP AND EMMA

GitHub Actions per il testing parallelo randomico di classi java utilizzando randoop per la generazione dei test ed Emma per ottenere il report sulla coverage.

## Utilizzo

- Cancellare (se presente) la cartella "merge/coverage" dalla repository.
- Carica il file .jar nella repository all' interno della directory "jars".
- Modifica il file "lista.txt" inserendo il nome delle classi da testare.
- Runnare il workflow manualmente dalla sezione "Action"(se è la prima esecuzione assicurarsi di aver correttamente eliminato la cartella merge/coverage).
- Al momento dell'avvio del workflow inserire nelle apposite caselle il nome del jar da testare e la coverage limit da raggiungere.



## Output

L' action genera nella repository la cartella merge/coverage, in cui sono presenti i file di coverage, ottenuti dal merge delle sessioni parallele e il merge con il risultato della precedente esecuzione

Al termine di ogni esecuzione del workflow saranno creati 2 Artifacts( consultabili in basso nella sezione summary ).
- Emma Reports, che contiene le cartelle "coverage_?", in cui sono presenti i report parziali delle singole sessioni e i test generati che trovano un fallimento.
- Coverage, che contiene il report finale sulla copertura di tutti i test eseguiti fino alla data esecuzione.

Cliccando sugli Artifacts vengono scaricati i .zip.

## COVERAGE

![Coverage Badges](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/PorfirioTramontana/8574debc02c060441c03fef539c02d15/raw/ParallelRandomTesting__.json)

![Coverage Badges](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/PorfirioTramontana/8574debc02c060441c03fef539c02d15/raw/ParallelRandomTesting2__.json)

![Coverage Badges](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/PorfirioTramontana/8574debc02c060441c03fef539c02d15/raw/ParallelRandomTesting3__.json)

![Coverage Badges](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/PorfirioTramontana/8574debc02c060441c03fef539c02d15/raw/ParallelRandomTesting4__.json)


### Note

A causa di alcuni problemi di comunicazione della piattaforma GitHub con GitHubGist, su cui vengono memorizzati i badge, gli stessi potrebbero non risultare aggiornati subito dopo l' esecuzione del workflow. Per visualizzare correttamente i valori di coverage si consiglia di attendere qualche minuto e riaggiornare la pagina della repository.
