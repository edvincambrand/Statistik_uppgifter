>[!abstract] Modeller
>    **Stokastisk** - En slumpmässig modell utan exakt förutsägelse
>    **Deterministisk** - En matematisk funktion

Alla slumpmässiga försök måste genomföras med samma villkor för att en stokastisk modell skall vara giltig.

**Viktiga definitioner:**

>[!quote] **SLUMPMÄSSIGT FÖRSÖK**
>Ett försök vars resultat inte kan förutsägas

>[!quote] **UTFALL - $\omega_{1},\omega_{2}$**
>Def: *Resultatet av ett slumpmässigt försök*

>[!quote] **UTFALLSRUM - $\Omega$**
>Def: *Mängden av alla möjliga utfall*

>[!quote] **HÄNDELSE - A,B,C**
>Def: *En samling av utfall, delmängd av utfallsrummet*
>Om ett utfall **tillhörande** $A$ inträffar, säger vi att $A$ inträffar.

>[!quote] **ÄNDLIG, DISKRET, KONTINUERLIG**
>Ett utfallsrum $\Omega$ kallas *diskret* om mängden är **ändlig**$^{(1)}$ *eller* **uppräkneligt oändlig**$^{(2)}$. Om $\Omega$ enbart är ändligt, kallas det rimligt nog bara *ändligt*.
>Ett utfallsrum $\Omega$ kallas *kontinuerligt* om antalet utfall är **oräkneligt oändligt**$^{(1)}$.

>[!example] Exempel
> *Kast tärning* - $\Omega=\{1,2,3,4,5,6\}$ **Ändlig**
> *Radioaktivt avfall* - $\Omega=\{1,2,3,\dots\}$ **Diskret**
> *Fysikalisk mätning* - $\Omega=\{602.24,655.99\dots\dots\}$ **Kontinuerlig**

>[!abstract]  Händelser
>* $\bigcup_{i=1}^{n} A_{i}=$ **Minst en** av händelserna $A_{1},\dots ,A_{n}$ sker
>* $\bigcap_{i=1}^{n}=$ **Alla** händelserna $A_{1},\dots,A_{n}$ sker

>[!abstract] De Morgans Lagar
(1)    $A \cap (B \cup C)=(A \cap B)\cup (A \cap C)$
(2)    $A\cup(B\cap C)=(A\cup B)\cap(A\cup C)$
(3)    $(\bigcup_{i=1}^{n}A_{i})^{*}=(\bigcap_{i=1}^{n}A_{i}^{*})$
(4)    $(\bigcap_{i=1}^{n}A_{i})^{*}=(\bigcup_{i=1}^{n}A_{i}^{*})$

$A_{i}^{*}$ *inträffar* $=A_{i}$ *inträffar inte*
**(1)**
*A och minst en av B, C = minst en av (AB), (AC)*
**(2)**
Minst en av A, (B och C) = (minst en av A, B) och (minst en av A,C)
**(3)** 
*Komplementet till att minst en av händelserna $A_{i}$ inträffar = alla komplement till $A_{i}$ inträffar = Ingen av händelserna $A_{i}$ inträffar*
**(4)**
*Komplementet till att alla händelser $A_{i}$ inträffar = Minst en av komplementen till $A_{i}$ inträffar = Minst en av $A_{i}$ inträffar inte*


------------------------------------------------------


***Avsnitt 2.3***



>[!quote] **SANNOLIKHET $P(A)$**
>Ett tal som tilldelas en händelse. Oberoende av frekvenser vid mätningar. Sannolikheten av en händelse är summan av dess utfall:
>$P(A)=\sum P(\omega),\hspace{5pt} \omega\in A$

>[!quote] **SANNOLIKHETSRUM**
>Sammanlagd mängd med $\Omega$ och alla $A_{i},P(A_{i})$.



>[!abstract] **AXIOM $(1-3)$ SATS $(4-6)$**
>    $(1)$    $P(A_{})\in[0,1]$
>    $(2)$    $P(\Omega)=1$
>    $(3)$    $P\left( \bigcup_{i=1}^{n} A_{i} \right)=\sum_{i=1}^{n} P(A_{i})$
>    $(4)$    $P(A^{*})=1-P(A)$
>    $(5)$    $P(A\cup B)=P(A)+P(B)-P(A\cap B)$
>    $(6)$    $P(A\cup B)\leq P(A)+P(B)$


**NOTERA!**
(3) gäller bara enbart **OFÖRENLIGA** händelser

**Bevis av (4):**
$$
\begin{gather}
1=P(\Omega)=P(A\cup A^{*})=P(A)+P(A^{*}) \\
\Longleftrightarrow \\
P(A)=1-P(A^{*})
\end{gather}
$$
**Bevis av (5)**
$$
\begin{gather}
(A\cup B)=\Omega\cap (A\cup B)=(A\cup A^{*})\cap(A\cup B) \\
=A\cup(A^{*}\cap B) \\
\implies P(A\cup B)=P(A)+P(A^{*}\cap B)\\
 \\
B=B\cap \Omega=B\cap(A\cup A^{*})=(B\cap A)\cup(B\cap A^{*}) \\
\implies P(B)=P(B\cap A)+P(B\cap A^{*})
\end{gather}
$$
Subtraktion ger oss:
$$
\begin{gather}
P(A\cup B)-P(B)=P(A)-P(B\cap A) \\
\Longleftrightarrow P(A\cup B)=P(A)+P(B)-P(B\cap A) \\
 \\
=P(A)+P(B)-P(A\cap B)
\end{gather}
$$

**Bevis av ABC (induktion)**
Låt oss lägga till en händelse $C$ och använda ekvationen ovan:
$$
\begin{gather}
P((A\cup B)\cup C)=P(A\cup B)+P(C)-P((A\cup B)\cap C) \\ \\

=P(A)+P(B)-P(A\cap B)+P(C)-P((A\cap C)\cup(B\cap C)) \\ \\

=P(A)+P(B)+P(C)-P(A\cap B) \\
-\left(P(A\cap C)+P(B\cap C)-P(A\cap B\cap C)\right) \\
 \\
=P(A)+P(B)+P(C) \\
-P(A\cap B) -P(A\cap C)-P(B\cap C) \\
+P(A\cap B\cap C)
\end{gather}
$$

>[!abstract] **SATS OM FÖRENLIGA SANNOLIKHETER**
>$P(A\cup B\cup C)=P(A)+P(B)+P(B)$
>$- P(A\cap B)-P(A\cap C)-P(B\cap C)+P(A\cap B\cap C)$



------------------------------------------------------


**Avsnitt 2.4**


>[!quote] **LIKFORMIGT SANNOLIKHETSMÅTT**
>Def: Sannolikheten av varje **enskilt** utfall är lika stort. Låt utfallrsummet $\Omega$ innehålla $m$ möjliga enskilda utfall:
> $\implies P(\omega_{i})=\frac{1}{m}$, $i=1,2,\dots,m$
>Låt nu händelsen $A$ innehålla $g$ gynnsamma fall:
>$\implies P(A)=P(\omega_{i})\cdot g=\frac{g}{m}$
>Kallas även *Klassisk sannolikhetsdefinition*




>[!example] **EXEMPEL: FELPRODUKTION**
>$2\%$ av enheterna har fel vikt
>$5\%$ av enheterna har fel färg
>$1\%$ av enheterna har både fel vikt och fel färg.
>$\implies P(A\cup B)=P(A)+P(B)-P(A\cap B)=2\%+5\%-1\%=6\%$
>*svar*: $6\%$ av enheterna har minst ett fel, vikt eller färg.

>[!example] **KAMERA OCH MINNE**
>Efter fem års användning har 30% anmärkt fel på kameran, 20% anmärkt fel på minnet, 10% anmärkt fel på båda. Hur många saknar problem efter fem år?
>**alternativ 1**
>$P(A\cup B)=P(A)+P(B)-P(A\cap B)$
>$\implies P((A\cup B)^{*})=1-(P(A)+P(B)-P(A\cap B))=$
>$=100-(30+20-10)=100-40=60\%$
>**alternativ 2**
>Vi använder de morgans lagar:





------------------------------------------------------


***Avsnitt 2.5***


>[!quote] **MULTIPLIKATIONSPRINCIPEN**
>Antalet åtgärder kan multipliceras vid två händelser för att få totalen av antalet möjliga åtgärder. Även sannolikheter kan multipliceras om de är oberoende av varandra.
>$P(A\to B\to C)=P(A)\cdot P(B)\cdot P(C)$.


Vi skall välja $k$ element från en samling med $n$ element:

|                      | med återläggning | utan återläggning                   |
| -------------------- | ---------------- | ----------------------------------- |
| **med** **ordning**  | **$n^{k}$**          | **$\frac{n!}{k!}$**                     |
| **utan** **ordning** | **$n+k-1\choose k$** | **$n \choose k$$=\frac{n!}{k!(n-k)!}$** |

>[!asbtract] **PERMUTATIONER**
>$n$ element kan *ordnas* på $n!$ sätt.

>[!example] **EXEMPEL: MARYAMS GARDEROB**
>Maryam kan välja mellan 4 strumpor, 3 byxor, 2 tröjor och 1 bh (edvins favorit). Hur många ställ kan hon skapa?
>$4\cdot 3\cdot 2\cdot 1 = 24$ ställ.
>

>[!quote] **KOMBINATORIK, GRUNDER**
>Antag att vi, från en mängd $\{e_{1},e_{2},\dots,e_{n}\}$, vill välja ut $k$ element. 
>**Med återläggning och ordning** - $N=n^{k}$
>**Utan återläggning, med ordning** - $N=\frac{n!}{k!}$
>**Utan återläggning, utan ordning** - $N=\frac{n!}{k!(n-k)!}=$$n\choose k$

>[!example] EXEMPEL **Vita/svarta kulor**
>Antag att vi har en skål med $v$ vita och $s$ svarta kulor. Vi väljer från denna $n$ kulor. Vad är sannolikheten att vi får precis $k$ vita kulor? $(k\leq n)$.


**(1)    Utan återläggning, utan hänsyn till ordning**

Vi beräknar antalet gynnsamma och möjliga fall. Varje utfall är enskilt och varje utfall har lika sannolikhet.
Vi kan välja k vita kulor på $v\choose k$ sätt.
Vi kan välja resterande (n-k) svarta kulor på $s \choose n-k$ sätt.
Vi kan välja k kulor från hela påsen på $v+s \choose k$ sätt.
Resultat med multiplikationsprincipen:
$$\frac{{v\choose k}\cdot{s\choose n-k}}{v+s \choose k}$$
>[!abstract] **DRAGNING UTAN ÅTERLÄGGNING**
>Sannolikheten att välja $k_{1}$ element av $v_{1}$, $k_{2}$ element av $v_{2}$, $...$, $k_{r}$ av $v_r$, där $N=\sum_{i=1}^{r}v_{i}$ och $n=\sum_{i=1}^{r}k_{i}$ ges av:
>$P={{v_{1}\choose k_{1}}\cdot{v_{2}\choose k_{2}}\cdot\cdot\cdot{v_{r}\choose k_{r}}}/{N \choose n}$

**(2)      Med återläggning och med hänsyn till ordning**
Välj först $k$ drag som innehåller vita kulor:
    V-S-V-V-S = $5 \choose 3$
Detta kan göras på $n\choose k$ sätt.
I varje drag som får en vit, kan vi välja de vita på $v^{k}$ sätt:
$V_{1},V_{2},\dots,V_{k}$
och de svarta på $s ^{n-k}$ sätt:
$S_{1},S_{2},\dots,S_{n-k}$
$\implies g={n \choose k}v^{k}s ^{n-k}$
$\implies P={n \choose k} \frac{v^{k}s^{n-k}}{(v+s)^{n}}$
Sannolikheten att en vit kula väljs är alltid $P(v)=\frac{v}{v+s}$
Sannolikheten att en svart kula väljs är alltid $P(s)=\frac{s}{v+s}$
Så vi kan också uttrycka det som:
$P={n \choose k}\left( \frac{v}{v+s} \right)^{k}\left( \frac{s}{v+s} \right)^{n-k}$

>[!abstract] DRAGNING MED ÅTERLÄGGNING
> Sannolikheten $P$ att välja $k_1$ element från $v_1$, $k_2$ element från $v_{2}$, $...$, $k_r$ element från $v_r$ ges av:
>$P={n \choose k_{1}}v_{1}^{k_{1}}{n-k_{1}\choose k_{2}}v_{2}^{k_{2}}\dots{n-k_{1}-\dots-k_{r-1}\choose k_{r}}v_{r}^{k_{r}}/\left( \sum_{i=1}^{r} v_{i} \right)^{n}$
>$=\frac{n!}{k_{1}!k_{2}!\dots k_{r}!}v_{1}^{k_{1}}v_{2}^{k_{2}}\dots v_{r}^{k_{r}}/\left( \sum_{i=1}^{r} v_{i} \right)^{n}$
>Att välja $k$ element från $v$ och $n-k$ element från $s$ ges alltså med återläggning av:
>$P={n\choose k}v^{k}{n-k\choose n-k}s ^{n-k}/(v+s)^{n}={n\choose k}v^{k}s ^{n-k}/(v+s)^{n}$




>[!warning] MED/UTAN ORDNING
>Se till attt både nämnare och täljare har samma hänsyn till ordningen (antingen eller inte). Sannolikheten är blir densamma för bägge fall, så länge nämnare och täljare har samma avseende!!!



------------------------------------------------------



**Betingad sannolikhet**

| Tabell 1    | Man | Kvinna |      |
| ----------- | --- | ------ | ---- |
| Rökare      | 20  | 50     | =70  |
| Inte rökare | 80  | 100    | =180 |
| **Totalt:** | 100 | 150    | =250 |
låt $A=$ man, $B=$ rökare $\implies A^{*}=$ kvinna, $B^{*}=$ inte rökare
Antag att vi väljer en person i studien. Varje person väljs lika sannolikt.
    $P(A)=\frac{100}{250}=40\%$ 
    $P(A^{*})=\frac{150}{250}=60\%$
    $P(B)=\frac{70}{250}=28\%$
    $P(B^{*})=\frac{180}{250}=72\%$
$P(A\cap B)=\frac{20}{250}=8\%$, men $20\%$ av män röker
$P(A^{*}\cap B)=\frac{50}{250}=20\%$, men $50\%$ av kvinnor röker
$P(A\cap B^{*})=\frac{80}{250}=32\%$, men $80\%$ av män röker inte
$P(A^{*}\cap B^{*})=\frac{100}{250}=40\%$, men $66.67\%$ av kvinnor röker inte.

*Givet att vi valt en man, vad är sannolikheten att han röker?*

$P(B|A)=\frac{20}{100}=20\%$

Men detta kan också skrivas: $\frac{20/250}{100/250}=\frac{P(A\cap B)}{P(A)}$

>[!abstract] **BETINGAD SANNOLIKHET**
>Givet $A$, ges sannolikheten att även $B$ enligt
>$P(B|A)=P(A\cap B)/P(A)$

$$
\begin{gather}
P(A\cap B)=P(A)\cdot P(B|A) \\
P((A\cap B)\cap C)=P(A\cap B)\cdot P(C|(A\cap B)) \\
=P(A)\cdot P(B|A)\cdot P(C|A\cap B) \\
\end{gather}
$$
Detta säger oss följande:
*Sannolikheten att A,B,C alla inträffar, är sannolikheten att A inträffar, multiplicerat med betingad sannolikheten av B givet A, multiplicerat med betingad sannolikheten av C givet A och B!*

EXEMPELTIME!

Betrakta en tredimensionell tabell, var $P(A)=20\%$. $P(B|A)=50\%$, $P(C|A\cap B)=33.33\% \implies P(A\cap B\cap C)=0.2\cdot 0.5 \cdot 0.3333=3.33\%$




------------------------------------------------------




Men vad blir sannolikheten att någon är en man, givet att denna röker?

$P(A|B)=\frac{P(A\cap B)}{P(B)}=\frac{20/250}{70/250}\approx28.57\%$

Det är alltså en skillnad mellan följande påståenden:

$(1)$ *Givet att en person är man, vad är sannolikheten att han röker?*
$(2)$ *Givet att en person röker, vad är sannolikheten att hen är man?*

$P_{1}=20\%$, $P_{2}\approx28.57\%$. $\implies P_1\neq P_{2}!$

| Tabell 2        | Man | Kvinna |      |
| --------------- | --- | ------ | ---- |
| Vårdpersonal    | 2   | 3      | =5   |
| Ej vårdpersonal | 118 | 9      | =127 |
| **total**       | 120 | 12     | =132 |
I tabellen ovan blir detta nog mer tydligt. Låt oss bestämma $P(A|B)$ och $P(B|A):$
    $P(A|B)=\frac{P(A\cap B)}{P(B)}=\frac{2/132}{5/132}\approx 40\%$
    $P(B|A)=\frac{P(A\cap B)}{P(A)}=\frac{2/132}{120/132}\approx 1.67\%$

-*Givet att den vi valt är vårdpersonal, är sannolikheten att denne är en man **40%***
-*Givet att den vi valt är en man, är sannolikheten att denne är vårdpersonal **1.67%***
Det är alltså **FUNDAMENTALT** annorlunda sannolikheter beroende på det ursprungliga villkoret!



>[!abstract] AXIOM
>$P(B^{*}|A)=1-P(B|A)$
>$P(B\cup C|A)=P(B|A)+P(C|A)-P(B\cap C|A)$
>$P(A\cap B\cap C)=P(A)\cdot P(B|A)\cdot P(C|A\cap B)$


>[!abstract] LAGEN OM TOTAL SANNOLIKHET
>Låt $H_{1},H_{2},\dots,H_{n}$ vara parvis disjunkta händelser sådana att $\bigcup_{i}H_{i}=\Omega$. Då gäller att:
>$P(A)=\sum_{i}P(H_{i})\cdot P(A|H_{i})$

**Bevis** *lagen om total sannolikhet*
$$
\begin{gather}
P(A)=P(A\cap \Omega)=P\left(A\cap \left(\bigcup_{i=1}^{n} H_{i}\right)\right) \\
=P\left(\bigcup_{i=1}^{n}(A\cap H_{i})\right)=\sum_{i=1}^{n}P(A\cap H_{i}) \\
=\sum_{i=1}^{n}P(A)\cdot P(A|H_{i})
\end{gather}
$$
Vi har använt att $P(A\cup B)=P(A)+P(B)$ vilket enbart gäller **disjunkta händelser**. Men eftersom varje $H_{i}$ är parvis disjunkt, måste $A\cap H_{i}$ vara parvis disjunkt.
Vi har också använd att $P(A\cap(B\cup C))=P(A\cap B)\cup(A\cap C)$ **(de morgan)** och att $P(A\cap B)=P(A)\cdot P(A|B)$ **(Betingad sannolikhet)**


------------------------------------------------------


$$
\begin{gather}
P(A\cap B)=P(A)P(B|A)=P(B)P(A|B) \\
\implies P(B|A)=\frac{P(B)P(A|B)}{P(A)}
\end{gather}
$$
Om vi delar upp utfallsrummet med total sannolikhet blir resultatet **bayes sats**:
$$
P(H_{i}|A)=\frac{P(H_{i})P(A|H_{i})}{\sum_{i=1}^{n}P(H_{i})P(A|H_{i}) }
$$
$i=1,2,\dots,n$



------------------------------------------------------

>[!quote] OBEROENDE HÄNDELSER
>Om $P(A|B)=P(A)$, så ser vi att händelsen $B$ inte påverkar sannolikheten om $A$ inträffar eller inte. Vi säger att $A,B$ är **oberoende** om och endast om:
>$\hspace{10pt} P(A\cap B)=P(B)P(A|B)=P(B)P(A)$

>[!abstract] OBEROENDE 
>Om $A$ och $B$ är oberoende, så är följande också oberoende:
>$\implies (A^{*},B)$
>$\implies (A,B^{*})$
>$\implies(A^{*},B^{*})$














