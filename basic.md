# Basic Usage
Math Symbol: https://oeis.org/wiki/List_of_LaTeX_mathematical_symbols

### Bold
`\textbf{}`
### Center
```
\begin{center}
	......
\end{center}
```
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
```
\begin{tabular}{|l|l|l|}
	\hline
	state & 0 & 1   \\ \hline
	A & B & C
\end{tabular}
```
