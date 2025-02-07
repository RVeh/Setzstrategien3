# Eine Rekursionsformel für den Zwei-Würfel-Fall

Eine Rekursionsformel für Gewinnwahrscheinlichkeiten ergibt sich analog zum Ein-Würfel-Fall. Da jetzt in einer Spielsituation nach den Ergebnissen der beiden nächsten Würfe für A und B unterschieden wird, entstehen Doppelsummen und kompliziertere Abbruchbedingungen, sodass wir den Zwei-Würfel-Fall nicht weiter verfolgen. Hier sind Simulationen  deutlich vorteilhafter, und zwar für jede noch so große Chipanzahl. Wir betonen, dass sich im Zwei-Würfel-Fall die Gewinnwahrscheinlichkeiten bei fest gewählten Setzstrategien deutlich von denen im Ein-Würfel-Fall unterscheiden können.

Bezeichnen in einer Spielsituation $(V,W)$ 
$s_V$ und $s_W$ die Anzahlen der noch im Spiel befindlichen Chips von A bzw. von B, so gibt es im Fall $s_V \ge 2$ und $s_W \ge 1$  auf jeden Fall noch zwei  Würfe, und wir unterscheiden danach, was nach diesen beiden Würfen passiert. Trifft der Wurf von A das Feld $i$ und der von B das Feld $j$, was wegen der Unabhängigkeit der Würfe mit Wahrscheinlichkeit $p_ip_j$ passiert, entsteht wie im Ein-Würfel-Fall genau eine der Spielsituationen  $(V_i,W_j)$, $(V,W_j)$, $(V_i,W)$ oder $(V,W)$.

Analog zu der Rekursionsformel für den Ein-Würfel-Fall gilt jetzt mit der Abkürzung

$$ t:= 1- \sum_{i,j=1}^m p_ip_j {\bf 1}(v_i=0,w_j=0): $$

$$
\begin{eqnarray*}
  \text{P}_A(V,W)  &  =  &   \sum_{i,j=1}^m
  \frac{p_ip_j}{t} \cdot \text{P}_A(V_i,W_j) \mathbb{1}(v_i \ge 1, w_j \ge 1) \\
  &  &  +  \sum_{i,j=1}^m 
  \frac{p_ip_j}{t} \cdot \text{P}_A(V_i,W) \mathbb{1}(v_i \ge 1, w_j  =  0) \\ 
  &   &  +  \sum_{i,j=1}^m 
  \frac{p_ip_j}{t} \cdot \text{P}_A(V,W_j) \mathbb{1}(v_i = 0, w_j  \ge  1).
\end{eqnarray*} 
$$


Diese Formel kann angewandt werden, bis erstmals eine der Bedingungen $s_V \ge 2$ und $s_W \ge 1$ nicht erfüllt ist.  