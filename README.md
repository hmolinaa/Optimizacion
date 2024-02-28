# Optimizacion del Filtro de Hodrick-Prescott mediante el metodo de Gradiente Descendente
\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage{algorithm}
\usepackage{algorithmic}

\title{Algoritmo de Gradiente Descendente}
\author{Tú Nombre}
\date{\today}

\begin{document}

\maketitle

\section{Descripción}

Este repositorio contiene una implementación en pseudocódigo del algoritmo de Gradiente Descendente, utilizado comúnmente en optimización numérica para encontrar el mínimo de una función.

\section{Pseudocódigo}

El pseudocódigo del algoritmo es el siguiente:

\begin{algorithm}
    \caption{Algoritmo de Gradiente Descendente}
    \begin{algorithmic}[1]
        \REQUIRE $x_0$, $f$, $\nabla f$, $H_f$
        \ENSURE $x^*$ (punto óptimo)
        
        \STATE $k \leftarrow 0$
        \STATE $g_0 \leftarrow -\nabla f(x_0)$
        
        \WHILE {criterio de alto sea falso}
            \STATE $\alpha_k \leftarrow$ arg min$_{\alpha > 0}$ $f(x_k + \alpha d_k)$
            \STATE $x_{k+1} \leftarrow x_k + \alpha_k g_k$
            \STATE $g_{k+1} \leftarrow -\nabla f(x_{k+1})$
            \STATE $k \leftarrow k + 1$
        \ENDWHILE
        
        \RETURN{$x^* = x_k$}
    \end{algorithmic}
\end{algorithm}

\section{Uso}

El pseudocódigo proporcionado puede ser traducido a cualquier lenguaje de programación para su implementación. Se necesitan los siguientes elementos para utilizar el algoritmo:

\begin{itemize}
    \item Un punto inicial $x_0$.
    \item La función objetivo $f$.
    \item El gradiente de la función $\nabla f$.
    \item Opcionalmente, la Hessiana de la función $H_f$.
\end{itemize}

\section{Contribuciones}

Las contribuciones a este repositorio son bienvenidas. Siéntase libre de enviar una solicitud de extracción para proponer mejoras o correcciones.

\section{Licencia}

Este proyecto está bajo la Licencia MIT.

\end{document}


