# Metodi logici per la filosofia

Appunti di **[Foxy](https://foxyseta.github.io)** (Stefano Volpe) per l'a.a.
2022-23: se trovi qualcosa di sbagliato, non esitare a **[caricare la
correzione](https://github.com/csunibo/metodi-logici-per-la-filosofia)**.

## 01-30. Presentazione del corso

### Organizzazione

- Libro: il primo titolo in bibliografia funge da manuale del corso. Non serve
  acquistarlo: il prof invia copie gratuite in PDF a chi lo richiede. Puoi
  trovarlo fra i **[libri](https://csunibo.github.io/metodi-logici-per-la-filosofia/libri)**.
- Notazioni: capita che il prof. le usi in modo inconsistente, ma noi dobbiamo
  consistentemente usare lo stile del manuale.
- Orari: si comincia ai 15, si finisce ai 45.
- Capienza aule: se le aule raggiungono la piena capienza e alcune persone
  devono rimanere fuori, il prof. pensa a soluzioni alternative (come le
  registrazioni, che in casi normali non vengono mai fatte).
- Lezioni: frontali, con "mini-interrogazioni" e compitini a casa (entrambi non
  valutati) per aiutarci a seguire.
- Registrazioni: ci sono quelle degli anni scorsi, ma quest'anno no.
- Ricevimenti: previo appuntamento via email.
- Seminario: chi vuole, in solitaria o in piccoli gruppi, tiene brevi seminari
  durante il corso su argomenti collegati a quelli trattati dal prof. (ma non
  gli stessi). Il tempo di esposizione varia in base all'argomento. Chi tiene
  un seminario ha un orale di molto semplificato.
- Consigli: se ci si perde una lezione, non si capisce molto di quelle dopo. Si
  studia volta per volta! Storicamente, va meglio all'esame chi lo sostiene
  appena terminate le lezioni (il prof. non fa preferenze ma avere gli argomenti
  freschi aiuta).
- Orale: si parte da una domanda a scelta, e poi il prof. prosegue con domande
  decise da lui. Siccome vengono chiesti enunciati e dimostrazioni, all'orale si
  usano carta e penna o lavagna e gesso.

### Le dimostrazioni del corso

Le nostre dimostrazioni formali non useranno la deduzione naturale, ma il
calcolo dei sequenti (anch'esso introdotto da Gentzen). Il metateorema
principale (*Hauptsatz*) di Gentzen che riguarga questo sistema ci permette di
fare a meno della regola del taglio, ottenendo un sistema deduttivo analitico
e non sintetico. Questo ci garantisce l'esistenza di prove concise e meccaniche.
Molto meglio della deduzione naturale!

### I contenuti del corso

Questo insegnamento parla di logiche modali. Esse aggiungono due nuovi operatori
proposizionali prefissi unari: $\Box$ e $\Diamond$. Sono duali:
$\Box P \leftrightarrow \neg \Diamond \neg P$. In generale, il loro ruolo è
rappresentare operazioni logiche non vero-funzionali. Possono avere diverse
intepretazioni:

- i. aletica: "è necessario che" vs "è possibile che";
- i. epistemica: "si sa che" vs "???" (nessuna intepretazione immediata in
  linguaggio naturale);
- i. doxastica: "si crede che" vs "???" (nessuna intepretazione immediata in
  linguaggio naturale);
- i. deontica: "è obbligatorio che" vs "è possibile che".

Tutte queste interpretazioni sono non vero-funzionali. Infatti, se tentassimo di
esprimere i concetti di cui sopra tramite tabelle di verità, non riusciremmo a
decidere come riempire alcune celle. Se una semantica delle tabelle di verità,
quindi, non basta, ricorriamo a quella di Kripke dei mondi possibili. La
semantica di questi operatori quantificherà su un certo sottoinsieme dei mondi
possibili, asserendo che la proposizione modale sia vera sulla base dello stato
di cose nei suddetti mondi. A seconda di quale interpretazione scegliamo,
opteremo per una diversa relazione insiemistica che, dato un mondo attuale, ci
permetta di risalire ai mondi da esso "visibili" (e cioè da considerare nella
nostra semantica degli operatori modali).

Dopo aver definito in modo rigoroso sintassi e semantica di diversi sistemi
modali sulla base di queste considerazioni, passeremo a risultati metalogici di
teoria delle dimostrazioni che ci rivelano proprietà particolari di questi
sistemi.
