

**3.1**
Vi har ett lyckohjul som kan anta alla värden mellan 1 och 20. Låt $X$ mäta talet som dyker upp vid varje snurr.
a) Vilka värden kan $X$ anta?
**a)** $X$ kan anta alla värden mellan 1 och 20

b) Bestäm sannolikhetsfunktionen $p_{X}(k)$
**b)** Sannolikheten är likformigt fördelat om lyckohjulet är väl konstruerat. $p_{X}(k)$ ges av: $p_{X}(k)=\frac{1}{20}$

c) Verifiera att $\sum_{k=0}^{\infty} p_{X}(k)=1$
**c)** Vi vet att $k\in\{1,2,3,\dots,19,20\}$. Så summan ges av $\sum_{k=1}^{20} \frac{1}{20}=1$

d) Beräkna $P(2<X\leq 5)$
**d)** $P(2<X\leq5)=\sum_{k=3}^{5} \frac{1}{20}=\frac{3}{20}$


**3.2**
$X$ kan anta alla värden inom $\Omega_{X}=\{5,20,100\}$
$P(X=100)=\frac{1}{1000}=0.1\%$
$P(X=20)=\frac{5}{1000}=0.5\%$
$P(X=5)=\frac{30}{1000}=3\%$


**3.3**
$\Omega_{X}=\{3,4,7,8,9\}$
$p_{X}(3)=\frac{1}{3}$, $p_{X}(4)=\frac{1}{4}$, $p_{X}(7)=\frac{1}{6}$, $p_{X}(8)=\frac{1}{6}$
$\implies p_{X}(9)=1-\frac{1}{3}-\frac{1}{4}-\frac{2}{6}=1-\frac{2}{3}-\frac{1}{4}=\frac{12}{12}-\frac{8}{12}-\frac{3}{12}=\frac{1}{12}$
$\implies F_{X}(5)=p_{X}(3)+p_{X}(4)=\frac{4}{12}+\frac{3}{12}=\frac{7}{12}$
$\implies P(4\leq X\leq8)=p_{X}(4)+p_{X}(7)+p_{X}(8)=\frac{7}{12}$
$\implies P(X\geq 8)=p_{X}(8)+p_{X}(9)=\frac{1}{6}+\frac{1}{12}=\frac{3}{12}=\frac{1}{4}$


**3.4**
I en ask ligger **en** femkrona och **två** enkronor. Ta **två** av dessa på måfå.
$X=$ *summan av myntens värden*
Vilka värden kan $X$ anta? - $\Omega_{X}=\{2,6\}$
$p_{X}(2)={2\choose 2}{1 \choose 0}/{3 \choose 2}=\frac{1}{3}$
$p_{X}(6)={2\choose 1}{1\choose 1}/{3\choose 2}=\frac{2}{3}$

___
**3.5**
En urna innehåller **4 vita** och **6 svarta** kulor. Dra **med återläggning** kulor tills du **för första gången** drar en vit kula. Bestäm $p_{X}(k)$ och $P(X\geq3)$.

För-första-gången sannolikhet **exklusivt succen** ges av:
$$
p_{X}(k)=(1-p)^{k}p=0.6^{k}\cdot 0.4
$$
$P(X\geq 3)=\sum_{k=3}^{\infty}p_{X}(k)=0.4\cdot(1+0.6+0.6^{2}+\dots)-p_{X}(0)-p_{X}(1)-p_{X}(2)$

$x+x^{2}+\dots+x^{n+1}=S_{n+1}-1=S_{n}\cdot x=S_{n}-1+x^{n+1}$
$\implies S_{n}=({x^{n+1}-1})/(x-1)$
$\implies P(X\geq3)=1-0.4-0.6\cdot 0.4-0.6^{2}\cdot 0.4=0.216$

___
**3.6**
Under samma förutsättningar som i förra uppgiften, ange sannolikhetsfunktionen för **antalet drag** $Y$ och bestäm $P(Y\geq2)$

Detta blir en **för-första-gången** fördelning **inklusive succe**, vars sannolikhetsfunktion ges av:
$$
p_{X}(k)=(1-p)^{k-1}p=0.6^{k-1}\cdot 0.4
$$
$\implies P(Y\geq2)=1-P(Y=1)=1-0.4=0.6$

___
**3.7**
Vi drar tre kulor från urnan. låt $X$ mäta antalet vita kulor. Bestäm $p_{X}(k)$ med och utan återläggning. Bestäm sedan sannolikheten att få fler vita kulor än svarta, med eller utan återläggning.

**Utan återläggning (hypergeometrisk)**:
$p_{X}(k)={4\choose k}{6\choose 3-k}/{10\choose 3}$
**Med återläggning (binomialfördelning)**: $p_{X}(k)={3\choose k}4^{k}6^{3-k}/10^{3}={3\choose k}0.4^{k}0.6^{3-k}$

Fler vita än svarta = 2 vita 1 svart / 3 vita 0 svarta
**Utan återläggning**: $P(v>s)=p_{X}(2)+p_{X}(3)=[{4\choose 2}{6\choose 1}+{4\choose 3}{6\choose 0}]/{10\choose 3}=(36+4)/120=1/3$
**Med återläggning**:$P(v>s)=p_{X}(2)+p_{X}(3)={3\choose 2}0.4^{2}0.6+{3\choose 3}0.4^{3}0.6^{0}=352/1000=35.2\%$
___
**3.8**
$X$ antar alla heltalsvärden $0,1,2,\dots$ och har sannolikhetsfunktion $p_{X}(k)=p^{k}$ för alla $k=1,2,3\dots$
$\implies P(X=0)=1-\sum_{k=1}^{\infty}p^{k}=1-(p+p^{2}+\dots)=$
$=1-(-1+1+p+p^{2}+\dots)=2-\sum_{k=0}^{\infty}p^{k}=2-\lim_{ n \to \infty } \frac{{p^{n+1}-1}}{p-1}=$
$=2+\frac{1}{p-1}=\frac{{2p-2}}{p-1}+\frac{{1}}{p-1}=\frac{2p-1}{p-1}$
Vilka värden på $p$ är möjliga?
$P(X=0)<1\implies 2p-1>p-1 \implies 2p>p$
$\sum_{k=1}^{\infty}p_{X}(k)=\sum_{k=0}^{\infty}p_{X}(k)-1=\frac{1}{1-p}-1<1$
$\implies \frac{1}{1-p}<2 \implies \frac{1}{2}<1-p \implies{p< 1/2}$
men vi tillåter även $p=\frac{1}{2}$ eftersom $P(X=0)=0$ för detta värde, så allt stämmer då med. $p$ är en sannolikhet, så den är positiv.
$\implies p\in\left[ 0, \frac{1}{2} \right]$

___
**3.9**
Antalet kunder som besöker en affär under ett givet tidsintervall är **poisson-fördelat** med **genomsnitt** $\mu=4$. Bestäm sannolikheten att fler än 2 och färre än 5 kunder besöker affären under tidsintervallet.
$P(2<X<5)=P(X=3)+P(X=4)$
$p_X(k)=\mu^{k}e^{-\mu}/k!\implies P(2<X<5)=4^{3}e^{-4}/3!+4^{4}e^{-4}/4! =39\%$

___
**3.10**

$$
\begin{gather}
p_{X}(0)=\frac{1}{4} \frac{1}{3} \frac{1}{2} = \frac{1}{24} \\
p_{X}(1)=\frac{6}{24} \\
p_{X}(2)= \frac{1}{4}\left( \frac{2}{3} \frac{1}{2} \right)+\left( \frac{3}{4} \right) \frac{1}{3}\left( \frac{1}{2} \right)+\left( \frac{3}{4} \frac{2}{3} \right) \frac{1}{2}=\frac{11}{24}\\

p_{X}(3)= \frac{3}{4} \frac{2}{3} \frac{1}{2} =\frac{6}{24} \\

\end{gather}

$$

**3.11**
Givet att  $p_{X}(k)=\mu^{k}e^{-\mu}/k!$ och $p_{X}(0)=\frac{1}{2}$, bestäm $P(X\geq 2)$.
**Lösning**
$P(X=0)=\frac{1}{2}\implies \frac{1}{2}=e^{-\mu}\implies{\mu=\ln(2)}$.
$\implies p_{X}(k)=\ln(2)^{k}/2k!$$P(X\geq 2)=1-P(X=0)-P(X=1)=1-\frac{1}{2}-\ln(2)/2=\frac{1}{2}(1-\ln(2))$
___
**3.12**
En man anländer till en busshållsplats där det alltid är 10 minuters väntetid mellan varje buss. $X=$ *Mannens väntetid*. Han anländer slumpmässigt någonstans mellan ankomsterna av två bussar.
$\Omega_{X}=(0,10)$
Sannolikheten är likformigt fördelad:
$$f_{X}(x)=
\begin{cases}
\frac{1}{10} & 0<x<10 \\
0&annars
\end{cases}$$
$P(3.5<X\leq7)=\int_{3.5}^{7}0.1dt=0.35=35\%$
$$F_{X}(x)=\begin{cases}
0,&x\leq0 \\
\frac{x}{10},&0<x<10 \\
1, & 1\leq x
\end{cases}$$

___
**3.13**
Givet en täthetsfunktion $f_{X}(x)$, bestäm konstanten $c$.
$$f_{X}(x)=\begin{cases}
cx^{2}, & x\in[0,6] \\
0, & annars
\end{cases}$$
Om funktionen är en täthetsfunktion så måste:
$\int_{-\infty}^{\infty}f_{X}(t)dt=1$ $\implies \left[ \frac{c}{3}x^{3} \right]^{6}_{0}=\frac{6^{3}}{3}c=1\implies c=\frac{3}{6^{3}}=\frac{1}{72}$

___
**3.14**
