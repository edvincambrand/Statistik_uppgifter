
**Stokastisk variabel**

>[!quote] STOKASTISK VARIABEL $X$
>En stokastisk variabel är en variabel som mäter egenskaper hos utfallen i utfallsrummet $\Omega$. 
>$X:\Omega\to \Omega_{x}$
>Exempelvis; $X=$ *antal krona vid myntkast*

**Sannolikhetsfunktion**

>[!quote] Sannolikhetsfunktion $p_{X}(k)$
>Eng: *Probability mass function*
>Mäter sannolikheten att en **diskret** s.v. $X$ antar ett visst värde:
>$p_{X}(k)=P(X=k)$, där $k\in \Omega_{x}$

**räkneregler** $p_{x}(k):$
* $0\leq p_{X}(k) \leq 1$
* $\sum_{k\in \Omega_{x}}p_{X}(k)=1$

>Låt $S\subset \Omega_{x}$. Då gäller:
>$P(S)=\sum_{k\in S}p_{X}(k)$

>[!warning] OLIKHET
>$P(X>0)$ är inte samma sak som $P(X\geq 0)$, och kan i **diskreta** fall vara exceptionellt annorlunda. För **kontinuerliga** variablar är det däremot ingen skillnad på olikheterna. 


------------------------------------------------------


**Fördelningsfunktion**

>[!quote] Fördelningsfunktion $F_{X}(\tilde{x})$
>Ger sannolikheten att s.v. $X$ är **mindre** än ett givet antal.
>$F_{X}(\tilde{x}):=P(X\leq \tilde{x})$
>-----------------------------------------------------
>$F_{X}(\tilde{x})\to 0$ då $\tilde{x}\to-\infty$
>$F_{X}(\tilde{x})\to 1$ då $\tilde{x}\to \infty$

Vi definierar $\alpha-$**kvantilen** som lösningen $\tilde{x}=x_{\alpha}$ till $F_{X}(\tilde{x})=1-\alpha$   
Exempel: kvantilen till $F_{X}(\tilde{x})=0.7$ är ett $\tilde{x}$ sådant att $P(X\leq \tilde{x})=0.7$

**Regler**
* $P(X=\tilde{x})=F_{X}(\tilde{x})-F_X(\tilde{x}-1)$
* $F_{X}(\tilde{x})$ är en *icke-avtagande* funktion.


------------------------------------------------------


**Binomialfördelning**

Givet en sekvens av $n$ **oberoende**, **slumpmässiga försök** var och en med exakt två möjliga utfall *succe* eller *misslyckande*, 
$\Omega_{x}=\{0,1,2\dots n\}$
Låt $X$ mäta antalet succeer i sekvensen. $X$ säges då vara en **binomialfördelad** stokastisk variabel med sannolikhetsfunktion:
$$
p_{X}(k)={n\choose k}p^{k}(1-p)^{n-k}
$$
där $k\in \Omega_{x}$. Skrivs även att $X\in Bin(n,p)$

>[!example] 20 myntkast
>Vi kastar ett mynt 20 gånger och låter $X=$ *antal 6-or* för varje given sekvens $\omega$. Varje kast är oberoende, och varje succe har sannolikhet $p=1/6$. Sannolikheten att få $k$ sexor ges alltså av:
$$
p_{X}(k)={20\choose k}\left( \frac{1}{6} \right)^{k}\left( \frac{5}{6} \right)^{n-k}$$

------------------------------------------------------


**För-första-gången fördelning**

Givet en sekvens av $n$ **oberoende**, **slumpmässiga försök** var och en med exakt två utfall *succe* eller *misslyckande*,
$\Omega_{x}=\{1,2,3,\dots\}$
Låt $X$ mäta *antalet försök upp till och inklusive* **första succe**. $X$ säges då vara för-första-gången fördelad med sannolikhetsfunktion:$$
\begin{gather}
p_{X}(k)=(1-p)^{k-1}p
\end{gather}
$$
Notera att vi ovan tar hänsyn till ordningen, eftersom det annars skulle finnas en succe före den "första"

>[!example] Myntkast till första krona
>$p_{x}(1)=(1-0.5)^{1-1}\cdot 0.5=0.5$
>$p_{x}(2)=0.25$
>$p_{x}(3)=0.125$
>...

>[!example] Inspekterade kretskort
>$X=$ *antal inspekterade kretskort* ***tills*** *en är defekt*
>Då är $X$ en $ffg$-variabel: $X\in ffg(p)$, med sannolikhet för defekt $p$. Låt då $p=0.005$. Vad är sannolikheten att $X=10$?
>$P(X=10)=p_{x}(10)=(1-0.005)^{9}\cdot(0.005)=$ **0.00478**


---


**Poissonfördelning**

Givet en tidsperiod i vilken det förekommer en viss oberoende händelse genomsnittligen $\mu$ gånger per denna period.
$\Omega_{x}=\{0,1,2,\dots\}$
Låt $X$ mäta antalet av denna händelse i tidsenheten. Då är $X$ *Poissonfördelad*, $X\in Po(\mu)$ och sannolikhetsfunktionen ges av:
$$
p_{X}(k)=\frac{\mu^{k}}{k!}e^{-k}
$$


|             | *Binomial*                                                                                                        | *För-första-gången*                                                                                                      | *Poisson*                                                  |
| ----------- | ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------- |
| *Villkor*   | Oberoende händelser, slumpmässiga försök, två utfall, mäter antalet succeer givet $n$ sekvenser, med återläggning | Oberoende händelser, slumpmässiga försök, två utfall, mäter antal misslyckanden inklusive första succe, med återläggning | oberoende händelsefrekvens, tidsberoende, genomsnitt $\mu$ |
| $p_{X}(k):$ | ${n\choose k}p^{k}(1-p)^{n-k}$                                                                                    | $(1-p)^{k-1}p$                                                                                                           | ${\mu^{k}} e^{-\mu} /k!$                                   |


---


**Kontinuerlig stokastisk variabel**


Låt $\Omega_{x}$ vara **ouppräkneligt oändlig**, exempelvis ett intervall $[a,b]$. Då är $X$ en kontinuerlig stokastisk variabel.

>[!quote] Täthetsfunktionen
>Om det finns en funktion $f_{X}(t)$ sådan att:
>$\hspace{20pt}P(X\in S)=\int_{S}f_{X}(t)dt$
>Så säges $X$ vara en **kontinuerlig stokastisk variabel** med täthetsfunktion $f_{X}$ (Eng: Probability density)

**Regler**
* $f_{X}(t)\geq 0$
* $\int_{-\infty}^{\infty}f_{X}(t)=1$

* $P(a<X\leq b)=\int_{a}^{b}f_{X}(t)dt$ $\implies P(X=a)=0$
* $F_{X}(\tilde{x})=\int_{-\infty}^{\tilde{x}}f(t)dt$
* $P(a<X\leq b)=F_{X}(b)-F_{X}(a)=\int_{a}^{b}f_{X}(t)dt$
* $\implies f_{X}(\tilde{x})=\frac{d}{dt}F_{X}(\tilde{x})$

>[!warning] Notera!
 >$P(X=a)=0$, $\implies P(a<X\leq b)=P(a\leq X\leq b)$.

---

**Kontinuerliga fördelningar**


>[!quote] Likformig fördelning $X\in U(a,b)$
>Exempel; väntetid på bussen.
>Om $X$ är likformigt fördelad på ett intervall $(a,b)$, så ges täthetsfunktionen av:
$$
f_{X}(\tilde{x})=
\begin{cases}
\frac{1}{b-a},& \tilde{x}\in(a,b) \\
0,& \tilde{x} \notin (a,b)
\end{cases}$$

>[!example] Likformig fördelning
>Wille är uttråkad på en psykologilektion och tittar på sin klocka. Han säger till sig själv: Jag slår vad om att sekundvisaren är maximalt 3 sekunder från 12 (57-60 sekunder). Vad är sannolikheten att han har rätt?
>
>Det är likformig sannolikhet att sekundvisaren står var som på klockan. $\implies f_{X}(t)=\frac{1}{b-a}$. Låt $[a,b]=[0,60]$ och låt $S=[57,60]$. $\implies P(S)=\int_{S}f_{X}(t)dt=\int_{57}^{60}\left( \frac{1}{60} \right)dt=\frac{1}{60}[60-57]=\frac{3}{60}=\frac{1}{20}=5\%$


___


>[!quote] Exponentialfördelning $X\in Exp(\lambda)$
>Exempel; livstid för elektronik, tiden passerad mellan två oberoende händelser
>Om $X$ är exponentialfördelad med genomsnittlig händelsefrekvens $\lambda$ så ges täthetfunktionen av:
$$f_{X}(\tilde{x})=
\begin{cases}
\lambda e^{-\lambda \tilde{x}}, & \tilde{x}>0 \\
0,& \tilde{x}<0
\end{cases}$$

>[!example] SMS
>Edvin får i genomsnitt 3 oberoende sms varje dag. Vad är sannolikheten att han får ett SMS under 24 timmar?
>___
> Den genomsnittliga händelsefrekvensen är $\lambda=\frac{3}{24}$. Alltså ges sannolikheten av:
> $\int_{0}^{24}\left( \frac{3}{24}e^{-(3/24)t} \right)dt=\left( \frac{3}{24} \right)\left[ -\frac{24}{3}e^{-3t/24} \right]_{0}^{24}=-[e^{-3}-1]=1-\frac{1}{e^{3}}$
> **svar**: $\approx$ **95%**

>[!example] SMS Fortsättning
>Vad är sannolikheten att Edvin får dubbelt så många SMS under en dag?
>___
>Vi kan använda Poissonfördelning!
>$p_{X}(k)=\mu^{k}e^{-\mu}/k!$ med $\mu=3,k=6$
>$\implies p_{X}(6)=3^{6}e^{-3}/6!=0.0504$
>**Svar**: $\approx$ **5%**


___


>[!quote] Normalfördelning $X\in N(\mu,\sigma)$
>Exempel; när mätningar centreras runt ett väntevärde
>Om $X$ är normalfördelad med väntevärde $\mu$ och standardavvikelse $\sigma$, ges täthetsfunktionen av:
$$f_{X}(\tilde{x})= \frac{1}{\sqrt{ 2\pi }\sigma}e^{-(\tilde{x}-\mu)^{2}/2\sigma^{2}}$$

Det finns även **Gammafördelning** och **Betafördelning** som inte inkluderas ovan.


___

>[!quote] Gammafördelning
>En exponentialfördelad variabel kan vara **gammafördelad** om vi är intresserade av **flera** händelser.
>$\alpha$ - antalet händelser som måste ske innan mätningen avslutas.
>$\beta$ - genomsnittligt antal händelser per tidsenhet
>$\Gamma(\alpha)=\int_{0}^{\infty}t^{\alpha-1}e^{-t}dt=(\alpha-1)!$
$$f_{X}(x)=\frac{\beta^{\alpha}x^{\alpha-1}e^{-\beta x}}{\Gamma(\alpha)}$$





