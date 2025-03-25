**2.1**
$\Omega_{1}$ - antal träningskast för att ett utfall skall ske toalt två gånger
$\implies \Omega_{1}=\{2,3,4,5,6,7\}$ 
*det är omöjligt att få ett nytt tal efter sjätte kastet*
$\Omega_{2}$ - antal tärningskast för att ett utfall skall ske två gånger i rad
$\implies \Omega_{2}=\{2,3,4,\dots\}$ *Det finns ingen begränsning, exempel* $\omega=1,2,1,2,1,2,1,2,\dots$

**2.2**
Vi sågar upp meterlånga brädor och slänger resten i en hög. Varje längd på restbitarna i högen utgör ett utfall i utfallsrummet.
$\implies \Omega=(0,1)$ *om restbiten är exakt 1 meter så slängs den inte, om den har längd 0 så finns den inte i högen. Alltså har vi olikheterna < och >*.

**2.3**
a) Vi skapar 3 enheter i ordning, dessa kan vara korrekta (K) eller defekta (D). Ange utfallsrum och händelsen när exakt två är defekta.
$\Omega=\{(K,K,K),(K,K,D),(K,D,K),\dots,(D,D,D)\}$
$A=\{(K,D,D),(D,K,D),(D,D,K)\}$
b) Ange utfallsrummet när ordningen inte tas hänsyn till och man räknar antalet defekta enheter, samt ange händelsen när exakt två är defekta och 
$\Omega=\{0,1,2,3\}$
$B=\{2\}$
c) Vi mäter hållfastheten hos ett armeringsjärn. Ange utfallsrummet och händelsen *hållfastheten är större än a men mindre än b*
$\Omega=(0,\infty)=\mathbb{R}_{+}$
$A=(a,b)$
d) Vi mäter hållfastheten hos **två** armeringsjärn. Ange utfallsrum och händelsen *båda har hållfasthet större än a*
$\Omega=\{(0,\infty),(0,\infty)\}=(0,\infty)^{2}=\mathbb{R}^{2}_{+}$
$A=\{(a,\infty),(a,\infty)\}=(a,\infty)\times (a,\infty)$
e) Vi mäter **n** armeringsjärn. Ange utfallsrum.
$\Omega=\{(0,\infty),(0,\infty),\dots,(0,\infty)\}=(0,\infty)^{n}=\mathbb{R}_{+}^{n}$

**2.4**
A och B är två händelser.
$A\cap B$ - *A och B inträffar*
$A\cup B$ - *A eller B inträffar*
$A\cap B^{*}$ - *A inträffar och B inträffar inte*
$A^{*}\cap B^{*}$ - *Varken A eller B inträffar*

**2.5**

**2.6**
$A$ och $B$ är oförenliga. Beräkna $P(B)$ om:
$P(A)=0.25$, $P(A\cup B)=0.75$
$P(A\cup B)=P(A)+P(B)+P(A\cap B)=P(A)+P(B)$
$\implies P(B)=P(A\cup B)-P(A)=0.75-0.25=$ **0.5**

**2.7**
Givet att:
$P(A)=0.6,P(B)=0.7,P(A\cup B)=0.8$, bestäm $P(A\cap B)$
$P(A\cup B)=P(A)+P(B)-P(A\cap B)$
$\implies P(A\cap B)=P(A)+P(B)-P(A\cup B)=0.6+0.7-0.8=$ **0.5**

**2.8**

**2.9**
Givet $P(A)=0.6,P(B)=0.7$ kan A,B ej vara disjunkta, ty $P(A)+P(B)>1$

**2.10**
Givet att $P(A\cap B)=0.4,P(A)=0.5,P(A^{*}\cap B)=0.1$, bestäm $P(A\cup B)$
Lösning:
$P(A^{*}\cap B)+P(A\cap B)=P(B)\implies P(B)=0.1+0.4=0.5$
$P(A\cup B)=P(A)+P(B)-P(A\cap B)=0.5+0.5-0.4=0.6$

**2.11**
Visa att sannolikheten att exakt en av händelserna $A,B$ inträffar är $P(A)+P(B)-2P(A\cap B)$.
Lösning:
Att exakt en av händelserna inträffar är ekvivalent med:
$A\cap B^{*}+A^{*}\cap B$
$$
\begin{gather}
\implies P=P(A\cap B^{*})+P(A^{*}\cap B) \\
=P(A\cap B^{*})+P((A\cup B^{*})^{*}) \\
=P(A\cap B^{*})+(1-P(A\cup B^{*})) \\
=P(A\cap B^{*})+1-P(A)-P(B^{*})+P(A\cap B^{*}) \\
=P(B)-P(A)+2P(A\cap B^{*})
\end{gather}
$$
Okej vi provar något annat. Det är också ekvivalent med:
$A\cup B-A\cap B$.
$$
\begin{gather}
\implies P=P(A\cup B)-P(A\cap B) \\
=P(A)+P(B)-2P(A\cap B)
\end{gather}
$$
ez lol.

**2.12**
Om $A_{1},A_{2},\dots,A_{n}$ är parvis oförenliga, gäller att $P(A_{i}\cup A_{j})=P(A_{i})+P(A_{j})$
Induktion ger:$P(A_{1}\cup(A_{2}\cup A_{3}))=P(A_{1})+P(A_{2}\cup A_{3})=P(A_{1})+P(A_{2})+P(A_{3})$ $\implies P\left( \bigcup_{i=1}^{n}A_{i} \right)=\sum_{i=1}^{n}P(A_{i})$
Orkar inte göra b)

**2.13**
Ur en ask innehållandes bokstäverna $V,G,K,N,A,C,K,A$
tar vi på måfå ut två av dem. Vad är sannolikheten att vi tar ut $V$ och $G$? Antag likformig sannolikhet.
Vi tar inte hänsyn till ordningen. Vi kan få $V$ och $G$ på 1 sätt:
$A=\{V,G\}$
Totala antalet sätt att välja två bokstäver är $8\choose 2$.
Sannolikheten blir $g/m=\frac{|A|}{|\Omega|}=1/{8\choose 2}=\frac{1}{28}$
Om vi tar hänsyn till ordningen blir $g=2$.
Totala antelet sätt är:
* Åtgärd 1. Vi kan välja första bokstaven på 8 sätt.
* Åtgärd 2. Vi kan välja andra bokstaven på 7 sätt.
$\frac{g}{m}=\frac{2}{8\cdot 7}=\frac{1}{28}$

**2.14**
Ta på måfå tre kort från en kortlek. Vad är sannolikheten att du får
a) Tre hjärter
b) Inget hjärter
c) Tre ess
Lösning:
**a)** Det finns 13 kort som har färg hjärter. Vi kan välja tre av dessa utan hänsyn till ordning på $13\choose 3$ sätt.
Totalt kan vi välja 3 kort från en kotrlek på $52 \choose 3$ sätt.
Sannolikheten ges därför av:
$P(a)={13\choose 3}/{52 \choose 3}$
**b)** Det finns 52-13=39 kort som INTE är hjärter. Vi kan välja tre av dessa på $39\choose 3$ sätt. Alltså får vi:
$P(b)={39\choose 3}/{52\choose 3}$
**c)** Det finns fyra ess i en kortlek. Vi kan välja tre av dessa på 4 sätt
$\implies P(c)={4\choose 3}/{52\choose 3}$

**2.15**
i en urna finns $v=3$ vita kulor, $s=4$ svarta kulor. Tag på måfå 2.
a) Sannolikheten att dra 1 vit, 1 svart (utan återläggning)
b) Sannolikheten att dra 1 vit, 1 svart (med återläggning)
**a)** Totalt kan vi göra $7\choose 2$ drag. Vi kan välja 1 vit kula på $3\choose 1$ sätt, samt 1 svart kula på $4\choose 1$ sätt, oberoende av vita drag. Alltså har vi enligt multiplikationsprincipen:
$P(a)={3\choose 1}\cdot{4\choose 1}/{7\choose 2}\approx 0.57$
**b)** Totalt kan vi med återläggning och med hänsyn till ordningen göra $7^{2}$ drag. Vi kan välja 1 vit kula på 3 sätt, 1 svart kula på 4 sätt. Eftersom vi tar hänsyn till ordningen behöver vi ta hänsyn till att det blir dubbelt så många gynnsamma fall, eftersom vi kan börja med svart istället. Alltså får vi:
$\implies P(b)={2\choose 1}\cdot{3^{1}}\cdot{4^{1}}/7^{2}\approx 0.49$

**2.16**
Tipsrad: 13 rader, 3 alternativ i varje. Vad är sannolikheten (antag likformig sannolikhet) att:
a) en person som får 13 rätt
b) en person får de 12 första rätt men den sista fel
c) en person får exakt 12 rätt.
Vi kan skapa $3^{13}$ olika tipsrader. Vi kan välja rätt på alla rader på 1 sätt. $\implies P(a)=1/3^{13}$
Vi kan välja de första 12 rätt och den sista fel på 2 sätt. $\implies P(b)=2/3^{13}$
Vi kan välja exakt 12 rätt på: ${13\choose 1}\cdot2$ sätt
$\implies P(c)=13\cdot2/3^{13}$

**2.17**
Vad är sannolikheten att minst två personer i en grupp med 23 personer har samma födelsedag?
Vi betraktar motsatsen: Vad är sannolikheten att INGEN har samma födelsedag?
Den första födelsedagen kan väljas på 365 sätt. Den andra på 364 sätt. osv. Totalt har vi $\frac{365!}{(365-23)!}$
När vi dividerar på totala antalet möjliga födelsedagskombinationer hos alla individerna får vi:
$\frac{365!}{(365-23)!}/365^{23}\approx 0.493$
Alltså är komplementsannolikheten $1-0.493=0.507$

**2.18**

**2.19**
Dra på måfå 13 kort ur en kortlek, utan återläggning. Vad är sannolikheten att du får:
a) 5 spader, 3 hjärter, 3 ruter, 2 klöver
b) fördelningen 5, 3, 3, 2 på godtyckliga färger.
Lösning:
**a)** Vi kan välja 5 spader på $13\choose 5$ sätt. Vi kan välja 3 hjärter på $13 \choose 3$ sätt. Samma för 3 ruter. Vi kan välja 2 klöver på $13 \choose 2$ sätt. Totalt kan vi välja $52 \choose 13$ kombinationer. Sannolikheten givet klassisk sannolikhetsdefinition är alltså:
$\implies P(a)={13\choose 5}{13\choose 3}^{2}{13\choose 2}/{52\choose 13} \approx 0.0129=1.29\%$
**b)** Vi kan organisera fyra färger på $4!$ sätt. Men notera att: $H,K,S,R=H,S,K,R$ ty de har samma antal. Vi kan alltså kombinera färgerna på $\frac{4!}{2}=12$ sätt.
$\implies P(b)=12\cdot {13\choose 5}{13\choose 3}^{2}{13\choose 2}/{52\choose 13} \approx 0.155=15.5\%$

**2.20**
En välblandad kortlek delas i två högar sådant att det ligger två kungar i vardera hög. Vad är sannolikheten att det ligger en röd kung i vardera hög?
Lösning:
Antag att det är lika sannolikt för alla kungarna att finnas i varsin hög. (klassisk sannolikhetsdefinition).
Våra kombinationer är:
H,R-S-K
H,S-K,R
H,K-S,R
I de senare två av dessa har vi en röd i varsin hög. Sannolikheten är alltså $\frac{2}{3}$

**2.21**
En köpare tar på måfå 5 enheter från ett parti med 100, i vilken det finns 6 defekta enheter. 
a) Vad är sannolikheten att exakt 2 av de 5 som valts är defekta?
b) Vad är sannolikheten att högst 1 enhet är defekt?
**Lösning:**
**a)** $v=94,s=6$. Vi kan välja 3 korrekta enheter på $94\choose 3$ sätt. Vi kan välja 2 defekta enheter på $6\choose 2$ sätt. Totalt kan vi välja fem enheter på $100 \choose 5$ sätt. Sannolikheten blir:
$\implies P(a)={94\choose 3}{6\choose 2}/{100 \choose 5}=2.67\%$
**b)** Högst 1 enhet defekt = Ingen enhet defekt + 1 enhet defekt
Vi kan välja 5 korrekta enheter på ${94\choose 5}$ sätt.
Vi kan välja 4 korrekta och 1 defekt på ${94 \choose 4}{6 \choose 1}$ sätt
$\implies P(b)=({94\choose 5}+{94\choose 4}{6\choose 1})/{100\choose 5} \approx97.2\%$

**2.22**
Vi drar **4** kort ur en kortlek **utan återläggning**, men **med** hänsyn till **ordning**.
a) Givet att de första tre korten är hjärter, vad är den betingade sannolikheten att det fjärde kortet **inte** är ett hjärter?
b) Hur stor är sannolikheten att de tre första är hjärter och det fjärde spader?
**Lösning:**
**a)** Vi skall välja 1 kort (fjärde) från en kortlek med 49 kort, var vi tagit bort 3 hjärter. Det finns $(49-10)=39$ kort som inte är hjärter. Den betingade sannolikheten är alltså $\frac{39}{49} \approx 80\%$
**b)** Vi kan organisera de tre första på: $13\cdot 12\cdot 11=1716$ sätt. Vi kan välja det fjärde kortet på $13$ sätt. Totalt finns det $1716\cdot 13=22308$ gynsamma fall. Antalet möjliga fall är $\frac{52!}{(52-4)!}=6497400$. 
$\implies P(b)=22308/6497400\approx 0.34\%$

**2.23**
Tre mätinstrument 1,2,3 har sannolikheter att fungera 90%, 80% respektive 40%. 
a) Om man väljer ett instrument på måfå, vad är sannolikheten att instrumentet fungerar?
b) antag att instrumentet fungerar. Vad är den betingade sannolikheten att det är vardera instrument?
**Lösning:**
**a)**
Det är lika stor sannolikhet att välja vardera mätinstrument $\frac{1}{3}\approx 33\%$
$P(du-väljer-1-och-fungerar)=\frac{1}{3}\cdot 0.9=0.300$
$P(du-väljer-2-och-fungerar)=\frac{1}{3}\cdot 0.8=0.267$
$P(du-väljer-3-och-fungerar)=\frac{1}{3}\cdot 0.4=0.133$
$P(fungerar)=\sum_{i}P(du-väljer-i-och-den-fungerar)=$
$=0.3+0.267+0.133=0.7$
**svar: 70%**
**b)** $A_{i}=$ *det är maskin i*     $B=$ *den fungerar*
Söker: $P(A|B)=P(A\cap B)/P(B)$
Vi har tagit reda på $P(B)$ ovan, och på varje rad har vi också beräknad $P(A_{i}\cap B)$.
$P(A_{1}|B)=\frac{0.300}{0.7}\approx 42.9\%$
$P(A_{2}|B)=\frac{0.267}{0.7}\approx 38.1\%$
$P(A_{3}|B)=\frac{0.133}{0.7}\approx 19.0\%$

**2.24**
Per och Pål har 11 frukter varav 3 är giftiga. Per äter 4 på måfå och Pål äter 6. Deras hund får den sista.
a) Vad är sannolikheten att hunden klarar sig?
b) Den betingade sannolikheten att både per och pål blir förgiftade, givet att hunden klarar sig
c) Sannolikheten att både per och pål blir förgiftade, samt att hunden klarar sig.
**Lösning**
**a)** Hunden kan klara sig på 8 sätt, kan få frukt på 11 sätt. Sannolikheten är därför likformigt $\frac{8}{11} \approx 0.727=72.7\%$.
**b)** $B=$ *hunden klarade sig*     $A=$ *Per och Pål båda förgiftade*
Om det är givet att hunden klarade sig, finns det 3 giftiga frukter mellan 10  frukter som idioterna åt. Per åt 4 och Pål åt 6. 
$P(Per-OCH-Pål)=1-P(Ingen)-P(bara-per)-P(bara-pål)$
$P(Ingen)=0$, eftersom alla frukter åts.
$P(bara-per)={3\choose 3}{7\choose 1}/{10\choose 4}=7/210 \approx 0.0333$
$P(bara-pål)={3\choose 3}{7\choose 3}/{10 \choose 6}=35/210 \approx 0.167$
$\implies P(per-OCH-pål)=1-7/210-35/210=0.8=80\%$
**c)** $P(A|B)\cdot P(B)=P(A\cap B)=0.8\cdot {8}/11 \approx 58\%$

**2.25**
En analfabetiker sätter upp två bokstäver som fallit ned från en skylt som det står "MALMÖ" på. Bestäm sannolikheten att skylten står rätt.
**Lösning:** 
Om bokstäverna som faller ned är OLIKA, är sannolikheten 50%.
Om bokstäverna som faller ned är LIKA, är sannolikheten 100%.
Vi inför lagen om total sannolikhet:
$$
P(A)=\sum_{i=1}^{2}{P(H_{i})\cdot P(A|H_{i})}
$$
Låt $A=$ *Rätt stavning*    $H_{1}=$ *Bokstäverna olika*   $H_{2}=$ *Bokstäverna lika*
Totalt kan skyltbokstäverna falla ned på 10 sätt:
${(m_{1},m_{2}),(m_{1},a),(m_{1},l),(m_{1},ö),(m_{2},a),(m_{2},l),(m_{2},ö)(a,l),(a,ö),(l,ö)}$
Lika bokstäver kan falla ned på 1 sätt.
Olika bokstäver kan falla ned på 9 sätt.
$P(lika)=1/10$
$P(olika)=9/10$
$\implies$
$$
\begin{gather}
P(A)=P(olika)\cdot(0.5)+P(lika)\cdot(1) \\
=\frac{9}{10}\cdot \frac{1}{2}+\frac{1}{10}\cdot \frac{2}{2} \\
=\frac{9+2}{20}=\frac{11}{20}
\end{gather}
$$

**2.26**
Sannolikheten för pojkfödsel är $P(pojke)=p$. Könen hos födda barn i en familj är oberoende. En familj har fyra barn.
a) Givet att den det **äldsta barnet är en pojke**, vad är sannolikheten att familjen har 2 pojkar, 2 flickor?
b) Givet att familjen har **minst en pojke**, bestäm sannolikheten att familjen har 2 barn av vardera kön.
**Lösning:**
**a)** Det är givet att det äldsta barnet är en pojke. Vi söker alltså sannolikheten att bland 3 barn är en av dem pojke, och resterande flickor. Situationen består av **slumpmässiga försök, oberoende** av varandra som mäter **succe** eller **misslyckande**. Alltså ges sannolikheten av en binomialfördelning!
$$
p_{X}(1-pojke)={3\choose 1}p^{1}(1-p)^{2}
$$
**b)** 
**Alternativ 1 (enklast)**
$P(2-pojkar|minst-1-pojke)=\frac{P(2-pojkar\cap minst-1-pojke)}{P(minst-1-pojke)}$
$=P(2-pojkar)/P(minst-1-pojke)$
$=P(2-pojkar)/[1-P(0-pojkar)]$
$={4\choose 2}p^{2}(1-p)^{2}/[1-(1-p)^{4}]$
**Alternativ 2**
$A=$ *familjen har två pojkar*
$H_{0}=$ *familjen har ingen pojke*
$H_{1}=$ *familjen har minst 1 pojke*
Lagen om total sannolikhet ger oss:
$$P(A)=P(H_{0})P(A|H_{0})+P(H_{1})P(A|H_{1})$$
men $P(A|H_{0})=0$, så vi får:
$$
\begin{gather}
P(2-pojk)=P(minst-1-pojk)\cdot P(2-pojk|minst-1-pojk) \\
\implies P(2p|minst-1)=\frac{P(2p)}{P(minst-1)} \\
=\frac{6p^{2}(1-p)^{2}}{1-(1-p)^{4}}
\end{gather}$$

**2.27**
Välj på måfå en av tre kort i en urna och titta bara på en sida av kortet:
* Dubbelsidigt **rött**
* Dubbelsidigt **vitt**
* Ena sidan **röd**, andra sidan **vit**.
a) vad är den betingade sannolikheten att den andra sidan är röd, givet att den ena sidan är det?
b) Finn det logiska felet: Om vi ser rött så har vi antingen (röd-röd) eller (röd-vit). Det är lika stor chans för båda, så sannolikheten är $1/2$.
**Lösning:**
**a)** Det finns **6** sidor vi kan ta upp, varav **3** är röda. **2** av dessa finns på det dubbelsidigt röda kortet. Den andra finns på det rödvita kortet. Den betingade sannolikheten är därför $\frac{2}{3}$ att vi valt det dubbelsidiga röda kortet. 
**b)** Det är sant att det är lika stor chans att välja båda korten, men det är en större chans att vi valt det röd-röda kortet om vi vet att den är röd på ena sidan. Alltså blir den betingade sannolikheten inte 50/50.

**2.28**






Från och med nu räknar vi nedifrån uppåt!

**2.44**
En bridgespelare har fått 13 kort. Hon meddelar:
a) Jag har **minst ett ess**
b) Jag har **hjärter ess**
Vad är den betingade sannolikheten, givet påståendet ovan, att hon har ytterligare ett ess i varsitt fall?
Lösning:
$P(A|B)=P(A\cap B)/P(B)$
**a)** 
$B=$ Hon har **minst ett ess**
$A=$ Hon har **minst två ess**
Vi söker alltså $P(A\cap B)$ och $P(B)$.
$P(minst-ett-ess)=1-P(inga-ess)=1-{48\choose 13}/{52\choose 13}=0.696$
$P(A\cap B)=P(A)=1-P(inga-ess)-P(ett-ess)$
$P(ett-ess)={4\choose 1}{48\choose 12}/{52 \choose 13}=0.4388$
$\implies P(A\cap B)=0.696-0.4388=0.257$
$\implies P(A|B)=0.370$
**svar 37.0%**
**b)**
$B=$ Hon har **hjärter ess**
$A=$ Hon har **minst två ess**
Det är givet för oss att hon har ett hjärter ess. På hur många sätt kan vi få ett till ess? Sannolikheten är $1-P(inga-fler-ess)$
$1-P(inga-fler-ess)=1-{48\choose 12}/{52\choose 12}=0.5612$
**svar 56.1%**
Det är större sannolikhet att hon har **fler ess** givet att hon har **hjärter ess**, jämfört med villkoret att hon har **minst ett ess**.


