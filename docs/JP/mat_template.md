## Packages
```tex
\usepackage{amsthm, amssymb, amsfonts, array, mathtools} % for mathematics
\usepackage{bm} % for vectors
\usepackage{algorithmic, algorithm} % for psuedo code
\usepackage{cite} % for citation
\usepackage{color} % draft writig and revise
\usepackage{comment} % draft writig and revise
\usepackage[dvipdfmx]{graphicx}
\usepackage[hang,small,bf]{caption}
\usepackage[subrefformat=parens]{subcaption}

%% ----- Create MathOperator Command ----- %%
\DeclareMathOperator{\diag}{diag}
\DeclareMathOperator{\DIAG}{DIAG}
\DeclareMathOperator{\minimize}{minimize}
\DeclareMathOperator{\prox}{prox}
\DeclareMathOperator{\Tr}{Tr}
\DeclareMathOperator{\sub}{subject\;to}

\newcommand{\argmin}{\mathop{\rm arg~min~}\limits}

%% ----- Create Theorems Command ----- %%
\newtheorem{lemma}{Lemma}
\newtheorem{thm}{Theorem}
\newtheorem{remark}{Remark}
\newtheorem{problem}{Problem}
\newtheorem{prop}{Proposition}
```