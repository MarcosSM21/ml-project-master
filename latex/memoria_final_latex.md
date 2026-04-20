\documentclass[12pt,a4paper]{article}

% --------------------
% PAQUETES BÁSICOS
% --------------------
\usepackage[spanish]{babel}
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}

\usepackage{geometry}
\geometry{margin=2.5cm}

\usepackage{setspace}
\onehalfspacing

\usepackage{graphicx}
\usepackage{float}

\usepackage{amsmath, amssymb}

\usepackage{booktabs}

\usepackage{hyperref}
\hypersetup{
    colorlinks=true,
    linkcolor=black,
    urlcolor=blue,
    citecolor=black
}

\usepackage{caption}
\usepackage{subcaption}

\usepackage{listings}
\usepackage{xcolor}

\setlength{\parindent}{0pt}
\setlength{\parskip}{6pt}

% --------------------
% CONFIGURACIÓN DE CÓDIGO (PYTHON)
% --------------------
\definecolor{codebg}{rgb}{0.97,0.97,0.97}

\lstset{
    language=Python,
    basicstyle=\ttfamily\small,
    keywordstyle=\color{purple},
    stringstyle=\color{orange!70!black},
    commentstyle=\color{gray!60},
    backgroundcolor=\color{codebg},
    showstringspaces=false,
    breaklines=true,
    frame=single,
    rulecolor=\color{gray!50}
}




% --------------------
% DATOS DEL DOCUMENTO
% --------------------
\title{\textbf{Machine Learning (I)}\\
\vspace{0.3cm}
\large Trabajo práctico: Clasificación Binaria}
\author{
\textbf{Autor:} Marcos Sánchez Martín}


\begin{document}

\maketitle

\begin{figure}[H]
\centering
\includegraphics[width=0.85\textwidth]{escudo_ucm.png}
\end{figure}


\vspace{0.7cm}
\begin{center}
\textit{Máster en Big Data, Data Science e Inteligencia Artificial\\
Universidad Complutense de Madrid}
\end{center}

\hrule
\vspace{0.4cm}

\newpage


% --------------------
% ÍNDICE
% --------------------
\tableofcontents
\thispagestyle{empty}
\newpage

\end{document}