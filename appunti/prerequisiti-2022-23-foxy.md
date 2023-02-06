# Prerequisiti per seguire "Metodi logici per la filosofia"

Appunti di **[Foxy](https://foxyseta.github.io)** (Stefano Volpe) per l'a.a.
2022-23: se trovi qualcosa di sbagliato, non esitare a **[caricare la
correzione](https://github.com/csunibo/metodi-logici-per-la-filosofia)**. Questi
appunti coprono solo le prime lezioni del prof., pensate per chi non ha mai
seguito un corso di logica di base.

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
$\Diamond P \leftrightarrow \neg \Box \neg P$ o, equivalentemente,
$\Box P \leftrightarrow \neg \Diamond \neg P$. In generale, il loro ruolo è
rappresentare operazioni logiche non vero-funzionali. Possono avere diverse
interpretazioni:

- i. aletica: "è necessario che" vs "è possibile che";
- i. epistemica: "si sa che" vs "???" (nessuna interpretazione immediata in
  linguaggio naturale);
- i. doxastica: "si crede che" vs "???" (nessuna interpretazione immediata in
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

## 02-01. Ripasso di logica classica proposizionale (1)

### Cos'è la logica?

Si dice che una proposizione è conseguenza logica di (o "segue logicamente da")
altre quando, se le ultime sono vere, allora lo deve essere anche la prima.

In particolare, un argomento o ragionamento si dice corretto o valido se la sua
conclusione è conseguenza logica delle sue premesse.

La logica è la discliplina che studia la conseguenza logica.

### Cos'è la logica proposizionale classica?

Una proposizione (semplicisticamente) è una parte del discorso che potrebbe
essere vera o falsa.

Una logica si dice proposizionale quando tratta solo proposizioni.

Noi ripasseremo la logica proposizionale classica (e cioè quella comunemente
usata) prima di vedere quelle modali.

Essa è formata da un insieme infinito di atomi logici (fungono da variabili
vere o false che rappresentano le proposizioni semplici del linguaggio
naturale),

$$\Phi := \\{ p_0, p_1, p_2, \dots \\}$$

alcuni connettivi logici primitivi (fungono da vero-funzioni, ovvero funzioni
che prendono in ingresso 0, 1 o più proposizioni per formarne una nuova),

$$\bot, \neg, \wedge, \lor, \rightarrow$$

e le parentesi tonde $($ e $)$ come simboli ausiliari per disambiguare il nostro
linguaggio.

Andiamo ora a definire per induzione l'insieme $Fm^\Phi$ delle formule ammesse
dal linguaggio della logica classica proposizionale:

1. se $p_i \in \Phi$, allora $p_i \in Fm^\Phi$;
1. $\bot \in Fm^\Phi$;
1. se $A \in Fm^\Phi$, allora $\neg A \in Fm^\Phi$;
1. se $A, B \in Fm^\Phi$, allora $(A \wedge B), (A \lor B), (A \rightarrow) B \in Fm^\Phi$;
1. nessun altra formula appartiene al linguaggio.

Ci saranno utili alcune definizioni "di comodo", ovvero abbreviazioni
sintattiche:

$$ \top \equiv \bot \rightarrow \bot $$

$$ (A \leftrightarrow B) \equiv ((A \rightarrow B) \wedge (B \rightarrow A)) $$

Siccome dover sempre usare le parentesi tonde per disambiguare la nostra
grammatica stanca, adottiamo alcune utili convenzioni per non doverle usare
quando il significato della formula si capisce anche senza:

1. se una coppia di parentesi si trova ai margini sinistro e destro della
formula, lo possiamo sottointendere;
1. priorità: la negazione lega più forte di congiunzione e disgiunzione, che a
loro volta legano più forte del condizionale materiale;
1. associatività: la congiunzione e la disgiunzione associano a sinistra (ma
non fra di loro).

Le definizioni per induzione sono utili: si sposano bene con la struttura con
cui abbiamo definito le nostre formule, e forniscono un modo algoritmico per
calcolare gli oggetti di cui parlano. Per esempio, possiamo definire la
lunghezza $lg$ (o "peso") di una formula o come il numero di occorrenze di connettivi
logici unari o binari che ne fanno parte o, equivalentemente, per induzione:

$$lg(p_i) = lg(\bot) = 0$$

$$lg(\neg A) = lg(A) + 1$$

$$lg(A \wedge B) = lg(A \lor B) = lg(A \rightarrow B) = lg(A) + lg(B) + 1$$

Se siamo familiari con il concetto di dimostrazione per induzione sui numeri
naturali in teoria dei numeri, possiamo ora effettuare dimostrazioni per
induzione sulla lunghezza delle formula della logica proposizionale classica.

Principio di induzione (versione "classica"):

- se $P(0)$ (passo base);
- se $\forall m \in \mathbb{N} (P(m) \rightarrow P(m + 1))$ (passo di induzione);
- allora $\forall n \in \mathbb{N} : P(n)$ (tesi).

Talvolta ci conviene usare invece una sua variante, detta "principio di
induzione forte" (l'ipotesi induttiva viene fortificata):

- se $P(0)$;
- se $\forall m \in \mathbb{N} : ((\forall n \in \mathbb{N} : (n \leq m \rightarrow P(n))) \rightarrow P(m + 1))$;
- allora $\forall n \in \mathbb{N} : P(n)$.

Siccome dover risalire dalla lunghezza della formula alle "tipologie" (schemi,
costruttori) che potrebbero avere tale lunghezza, tedia, spesso dimostriamo per
induzione direttamente elencando le vaire "tipologie" di formula con le quali
potremmo avere a che fare.

### Esercizio per casa

$\char"0023_((A) = \char"0023_)(A)$

dove $\char"0023_a(A)$ significa "il numero di occorrenze di $a$ in $A$".

## 02-02. Esercizi sulla sintassi della logica classica proposizionale

### Esercizio svolto in aula

$\char"0023_{p_i, \bot}(A) \geq \char"0023_{\wedge, \lor, \rightarrow}(A)$

L'esercizio, volendo, si semplifica dimostrando la disuguaglianza stretta al
posto di quella lasca.

## 02-06. Semantica della logica classica proposizionale (1)

### Cos'è la semantica?
La semantica di un linguaggio formale è il significato che associamo ai suoi
elementi. Senza semantica, potremmo costruire formule ben formate secondo le
regole della sintassi, ma senza poterci accordare su cosa rappresentino.

### La semantica della logica proposizionale

La semantica della logica proposizionale si basa sul concetto di
*interpetazione*. Una possibile interpretazione $I$ relativa al nostro
linguaggio è un qualsiasi sottoinsieme dell'insieme $\Phi$ degli atomi logici:

$$I \subseteq \Phi$$

Intuitivamente, l'interpretazione rappresenta l'insieme di tutte e sole le
proposizioni atomiche che essa rende vere: le proposizioni atomiche lasciate
fuori dall'interpretazione saranno quindi false secondo essa. Siccome una
interpretazione è un sottoinsieme di $\Phi$, possiamo sempre definirla anche
come la funzione caratteristica del suddetto sottoinsieme, e cioè la funzione $I
: \Phi \rightarrow \\{0, 1\\}$ che associa a ogni proposizione atomica che
vorremmo fosse resa vera 1, e 0 alle proposizioni atomiche che vorremmo fossero
rese false.

Questi due modi di concepire le interpretazioni fanno uso di oggetti matematici
diversi, ma sono entrambi funzionali. Di volta in volta, capiremo quale stiamo
usando dal contesto. In logica modale, però, spesso è più comoda la prima.

In entrambi i casi, siccome partiamo da un insieme $\Phi$ infinito, avremo un
numero infinito di possibili interpretazioni. Per dire che una formula A vale
rispetto a una certa interpretazione I (o che "I rende vera A"), scriviamo $I
\models A$. Siamo ora pronti a definire la semantica della logica proposizionale
classica:

- $I \models p_i \quad sse \quad p_i \in I (oppure, usando la funzione
  caratteristica i(p_i) = 1)$
- $I \not\models \bot$
- $I \models \neg A \quad sse \quad I \not\models A$
- $I \models A \wedge B \quad sse \quad I \models A e I \models B$
- $I \models A \lor B \quad sse \quad I \models A o I \models B$ (disgiunzione
  inclusiva)
- $I \models A \rightarrow B \quad sse \quad I \not\models A o I \models B$
  (disgiunzione inclusiva)

### Applicabilità del metodo delle tavole di verità

Un metodo meccanico e concettualmente semplice (anche se potenzialmente lungo)
per verificare quali interpretazioni soddisfino una data formula A è quello
delle cosiddette "tavole di verità". Per mostrarne l'applicabilità, però,
abbiamo prima bisogno di un risultato preliminare. Per sommi capi, questo
"lemma" ci assicura che, per capire se una formula sia vera o meno rispetto a
una data interpetazione, è sufficiente sapere come questa interpetazione si
collochi rispetto agli atomi logici che effettivamente compaiono nella formula.
In altre parole, se un atomo logico non compare nella formula, non ci interessa
se sia vero o falso in una data interpretazione per capire se questa renda vera
la formula o meno.

> Sia A una formula e siano I e I' due interpretazioni. Se, per ogni atomo logico
> $p_i$ che occorre almeno una volta in A, $I(p_i) = I'(p_i)$, allora vale che
>
> I \models A \quad sse \quad I' \models A

### Esercizio per casa

Si dimostri, per induzione strutturale sul numero naturale $k$:

$$I \models A \quad sse \quad I \models \neg{}^{2k}A$$

### Utili definizioni per la semantica

Siano A una formula, I un'interpretazione e $\Gamma$ un insieme di formule.
Allora:

- "A è soddisfatta da I" significa $I \models A$ (siccome siamo ancora in logica
  proposizionale)
- "A è soddisfacibile" significa $\exists I : I \models A$
- $\models A$ (si legge "A è valida", "A è una verità logica" o, finché restiamo
  nella logica classica proposizionale, "A è una tautologia") significa $\forall
  I : I \models A$
- $\Gamma \models A$ (si legge "A è conseguenza logica di \Gamma") significa
  $\forall I : ((\forall B \in \Gamma : I \models B) \rightarrow I \models A)$

### Il teorema di deduzione

Il teorema di deduzione è un risultato di semantica molto importante, perché ci
permette di capire che, in virtù della semantica che abbiamo associato ad esso,
il condizionale materiale $\rightarrow$ all'interno del nostro linguaggio la
nozione di conseguenza logica:

$$\Gamma, A \models B \quad sse \quad \Gamme \models A \rightarrow B$$

### Altri esercizi per casa

Scegliere alcune tautologie a piacere e dimostrare (senza tavole di verità) che
esse siano effettivamente tautologie.
