# cubeVenture - Presentazione
Ciao! Questo è il mio capolavoro per l'anno scolastico 2023-2024. 
Ho scelto, per creare questo progetto, Python, per la sua semplicità e soprattutto perché ne ho dimestichezza.
Mi sono ispirato ampiamente a Minecraft, un gioco con mondi infiniti dove è possibile esplorare e costruire.

Da tempo volevo creare un gioco, e per esercitarmi ho creato questa "prova", che serve più che altro da concetto per qualcosa che vorrei fare in futuro.
Ho iniziato cercando varie librerie che potessero aiutarmi nella sua realizzazione, e sono finito su ursina, un motore grafico completamente open-source basato su panda3d. Il progetto è iniziato semplicemente: un quadrato 5x5 dove si poteva costruire con dei blocchi per poi distruggerli. 
Ho aggiunto poi le mie texture (disegnate per il meglio che ho potuto), ma aggiungendole dovetti creare un nuovo modello di cubo, in quanto quello dato dal motore grafico non andava bene per la mappatura corretta della texture (il nuovo cubo è nella cartella assets). Continuai aggiungendo una musica in sottofondo, per poi aggiungere la feature che per più tempo mi ha tenuto bloccato: la generazione casuale del terreno.

L'idea era piuttosto semplice: rendere il mondo infinito come quello di Minecraft. Tuttavia, i problemi furono molteplici, primo tra quali le performance: le collisioni di ogni cubo nell'ambiente di gioco rendevano lentissimo il gioco, provocando lag, così rendendo limitato il mondo di gioco. Arrivai alla soluzione di implementare la generazione progressiva del mondo, tramite una render distance (distanza di rendering) di un quadrato di 15x15 per volta. E' la dimensione ideale, fermando il gioco a 30 FPS sul mio computer, rendendolo pressoché godibile. 
Il secondo problema era il mondo di per sé: data la presenza (in base al seme) di varie colline e montagne in gioco, queste lasciavano nel terreno alcuni buchi vuoti, attraverso i quali il giocatore poteva cadere. Ho sistemato tranquillamente la situazione aggiungendo uno strato inferiore di terreno identico all'originale, abbassando il suo asse y di una coordinata, dandogli la texture della pietra. Una soluzione provvisoria, che stranamente, non sembrava avere ripercussioni sulle prestazioni del gioco di per sé, dunque, decisi di tenerla.
Ulteriore problema si presentò nello scegliere il nome: il nome originale era "Ripoffcraft", nome scherzoso che indicava che questo fosse una "copia" di Minecraft, ma finii su cubeVenture in quanto non c'è molto da costruire, ma solo da esplorare. Il mondo di per sé appare vuoto, niente animali o alberi (o meglio, gli alberi presenti nel codice e attivabili manualmente, ma non sono molto funzionanti), in parte anche per conservare quel poco di prestazioni che rimanevano. Il gioco di per sé è leggero, non consuma molte risorse del computer, e funzionerebbe ancora meglio se fosse ben ottimizzato.

# cubeVenture - Come installarlo e provarlo

Su Windows, è necessario aprire il file "win_install.cmd", installerà tutti i requisiti fondamentali per eseguire il gioco (compreso Python);
Su Linux, in modo simile bisognerà soltanto aprire il file "install.sh";
Su Mac, dovrai installare i prerequisiti manualmente (scusa)

# cubeVenture - Pre-requisiti e installazione manuale

Ecco le librerie fondamentali per far funzionare il gioco, installabili tramite questo comando:

> pip install ursina numpy perlin-noise

Bisognerà installare anche Python, presente sul Microsoft Store o sul loro sito ufficiale. Su Linux, se non presente, bisognerà installarlo dal proprio package-manager, spesso Aptitude.

Buon divertimento!

# cubeVenture - Comandi
Stavo per dimenticare i comandi. In modo simile a Minecraft, ci si muove nel mondo utilizzando WASD sulla propria tastiera, saltando con la barra spaziatrice e si costruisce e si distrugge con il tasto destro e sinistro del mouse. 
Sommario:
> WASD - Movimento\n
> Tasto sinistro del mouse - Distruggere blocchi\n
> Tasto destro del mouse - Costruire blocchi\n
> ESC - Uscire dal gioco

