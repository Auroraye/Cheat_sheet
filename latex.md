# Basic Usage
Math Symbol: https://oeis.org/wiki/List_of_LaTeX_mathematical_symbols

### Bold
`\textbf{}`
### Empty space 
`\`
### { with multi-lines
```
$$\begin{cases}
	A &= B\\
        B &= C
\end{cases}$$
```
### Center
```
\begin{center}
	......
\end{center}
```
OR 
```
\centering
```
### New page
`\newpage`
### NFA / DFA
``` 
\begin{tikzpicture}[auto, node distance=3cm, every loop/.style={},
		ultra thick,main node/.style={circle,draw,font=\sffamily\Large\bfseries}]
    
		\node[initial text =, initial, state] (1) {$q_0$};
		\node[state] (2) [right of =1] { $q_1$};
		\node[state, accepting, double distance=2pt] (3) [below of =1] {$q_2$};
    
    
		\path[->]
		(1) edge[bend left] node  {1} (2)
		edge [loop above] node {0} (1)
		(2) edge[bend left = 30] node  {0} (3)
		edge [bend left]node {0, 1} (1)
		(3) edge node  {0, 1} (1)
		edge [loop left] node {0} (3);
\end{tikzpicture}
```
`edge[bend left = 30]`: bending degree

### Text on the arrow 
```
$$ q_0 \xrightarrow{1} q_1 $$
```

### Table 
NOTE: ADD `[h]` to avoid table at top of the page
```
\begin{tabular}{|l|l|l|}
	\hline
	state & 0 & 1   \\ \hline
	A & B & C
\end{tabular}
```
```
\begin{table}[h]
  \caption{Timeline}
  \label{sample-table}
  \centering
  \begin{tabular}{lll}
    \toprule
    Date     & Goal     & Note \\
    \midrule
    Oct 5  - Oct 14 & Establish a collection of papers &   \\
    Oct 15 - Oct 21 & Describe in-depth background information &   \\
    Oct 22 - Oct 28 & Finish individual assigned work &   \\
    Oct 29 - Nov 4 & Finish the draft and review &   \\
    Nov 5  - Nov 11 & Ready for submission &   \\
    \bottomrule
  \end{tabular}
\end{table}
```
