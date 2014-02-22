pacchetto_installazione_win32
=============================
Questo è il nuovo sistema sperimentale per Qgis 2 Dufour All in One Installer Per Windows 7 SOLO A 32bit

I files presenti sono presi da
http://www.lfd.uci.edu/~gohlke/pythonlibs/
http://qgis.org/it/site/

Nel pacchetto sono inclusi tutti i file di installazione e cartelle.

Installazione per Windows 7
ATTENZIONE: installare ogni pacchetto con spuntata l'opzione Tutti gli utenti quando presente.

Scaricate il pacchetto (240 mb) dal Dropbox di pyArchInit da questo link: https://www.dropbox.com/sh/3eqrb5vstee56rl/JTH0BTAr4z


##############   Step 1   
AL momento è  necessario avere la seguente installazione
Qgis Dufour da All in one Installer 32 bit (x86) (File 1)


##############   Step 2   
Una volta istallato QGis sarà necessario installare Python27 dall'installer a 32bit (File 2)

##############   Step 3   
Verificare prima se dentro alla cartella "C:\Program Files (x86)\QGIS Dufour\apps\Python27\Lib\site-packages"  della vostra installazione Qgis sia gi  presente networkx (al 100% si!!!)

Se fosse già presente, non sarà necessario installare Networkx e potete passare allo step 5 altrimenti lanciate  l'installer di networkx (File 3)

##############   Step 4   
Andate nell'installazione di python nella cartella "C:\Python27\Lib\site-packages" e copiate sia la cartella networkx che il file networkx.x.x.EGG.

Spostatevi nell'installazione python del vostro QGis "C:\Program Files (x86)\QGIS Dufour\apps\Python27\Lib\site-packages" e incollate dentro i files di networkx appena copiati

##############   Step 5   
Installate Graphviz (Versione raccomandata  2.30) (File 4)


##############   Step 6   
Installate pygraphviz (Versione raccomandata 1.2) (File 5)

Andate nell'installazione di python nella cartella "C:\Python27\Lib\site-packages\" e copiate sia la cartella  pygraphviz che il file pygraphviz.x.x.EGG o EGG-INFO

Spostatevi nell'installazione python del vostro QGis "C:\Program Files (x86)\QGIS Dufour\apps\Python27\Lib\site-packages\pygraphviz\" e incollate dentro i files di pygraphviz appena copiati

APPLICAZIONE DELLA PATCH PER IL SISTEMA DI MATRIX INTERATTIVO (al 100% non più necessaria!!!)

E' necessario aggiungere questa patch nel codice seguendo le istruzioni:

andate sotto
 "C:\Program Files (x86)\QGIS Dufour\apps\Python27\Lib\site-packages\pygraphviz\" e individuate il file agraph.py. Apritelo con un editor di testo (wordpad) e cercate la stringa: runprog=self._get_prog(prog) se non è presente chiudete tutto e proseguite.
 
ATTENZIONE: E' possibile che il vostro installer di pygraphviz abbia già la patch applicata.
In questo caso saltate allo step 7

cercate esattamente questo pezzo di codice:

runprog=self._get_prog(prog) 

sostituendolo con

runprog=r'"%s"'%self._get_prog(prog)

ATTENZIONE A NON CAMBIARE NIENT'ALTRO, SPAZI COMPRESI!!!!!

##############   Step 7   
Installate reportlab (File 6)

Andate nell'installazione di python nella cartella "C:\Python27\Lib\site-packages" e copiate sia la cartella 
repotlab che il file reportlab.x.x.EGG.

Spostatevi nell'installazione python del vostro QGis "C:\Program Files (x86)\QGIS Dufour\apps\Python27\Lib\site-packages" e incollate dentro i files di reportlab appena copiati

##############   Step 8   
Installate sqlalchemy (File 7)

Andate nell'installazione di python nella cartella "C:\Python27\Lib\site-packages" e copiate sia la cartella sqlalchemy che l eventuale cartella sqlalchemy_nose che il file sqlalchemy.x.x.EGG-INFO
Spostatevi nell'installazione python del vostro QGis "C:\Program Files (x86)\QGIS Dufour\apps\Python27\Lib\site-packages" e incollate dentro i files di sqlalcehmy appena copiati

##############   Step 9   
Aprite Qgis 2.0

Andate a Impostazioni-> Opzioni->Sistema:
in questo modo:

Spuntate la prima Flag Usa variabili utente
e dopo aver cliccato su aggiungi
Inserite nella riga i seguenti valori
Prima colonna  |Seconda colonna  |Terza Colonna
Accoda         |Path             |;C:\Program Files (x86)\Graphviz2.30\bin

ATTENZIONE IL PERCORSO PUO' VARIARE IN BASE ALLA VOSTRA MACCHINA E AL SISTEMA OPERATIVO INSTALLATO. Qui siamo sotto Windows 7.

##############   Step 10  
Se avete già  installato altri plugin potete passare allo Step 11

Per la seguente procedura dovete avere una rete con collegamento Internet attivo!
Se siete alla prima installazione di Qgis, aprite Qgis 2.0, andate sotto Plugins->Gestisci e installa plugin...
Selezionate dal menu di sinistra "Altro" scegliete un plugin che vi aggrada e installatelo selezionandolo e dal pulsante in basso a dx 
cliccate su installa.
Questo creerà  la cartella C:\users\vostro_utente\.qgis2\python\plugins dove inserirete pyarchinit
Chiudete QGis



##############   Step 11   
Andate su https://github.com/pyarchinit/pyarchinit_beta_test_dev e dal pulsante download scaricate il plugin, scompattate lo zip, estraete il plugin pyarchinit_devxxxxxx e rinominate la cartella in pyarchinit.
Copiate la cartella appena rinominata in pyarchinit nella cartella C:\users\vostro_utente\.qgis2\python\plugins 



##############   Step 12   
Avviate QGis e il plugin dovrebbe essere pronto all'uso. Fate riferimento alla documentazione in rete sul sito ufficiale di pyarchinit:
https://sites.google.com/site/pyarchinit/documentazione (Al momento in revisione)

Per versioni aggiornate potete scaricare da qua: https://github.com/pyarchinit/pyarchinit_beta_test_dev e seguire lo step 11
Per segnalare bug o altro: https://github.com/pyarchinit/pyarchinit_beta_test_dev/issues?direction=desc&labels=&milestone=&page=1&sort=created&state=open
Per chiedere info: https://groups.google.com/forum/#!forum/pyarchinit-users
