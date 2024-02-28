# Optimizacion del Filtro de Hodrick-Prescott mediante el metodo de Gradiente Descendente
Mediante los conociminetos adquiridos y entendiendo los metodos de optimizacion y sus aplicaciones se presenta el siguiente proyecto. Donde inicialmente se describe el problema que queremos optimizar o encontrar su punto optimo, la funcion del filtro de Hodrick-Prescott. Luego, resolvemos el problema de optimizacion $x^*= \text{arg}\min_{\alpha > 0 } f(x)$ implementando el algoritmo del Gradiente Descendente en el lenguaje de programacion de Python. Por ultimo, se muestran los experimentos y resultados obtenidos.

De forma general, el algoritmo que implementamos para el Gradiente Descendente es el siguiente: 

$$\begin{algorithm}
    \SetAlgoLined
    \KwIn {$x_0$, $f$, $\nabla f$, $H_f$}
    \KwOut {$x^*$ (punto óptimo)}
    
    $k \leftarrow 0$\;
    $g_0 \leftarrow -\nabla f(x_0)$\;
    
    \While {criterio de alto sea falso}{
        $\alpha_k \leftarrow$ arg min$_{\alpha > 0}$ $f(x_k + \alpha d_k)$\;
        $x_{k+1} \leftarrow x_k + \alpha_k g_k$\;
        $g_{k+1} \leftarrow -\nabla f(x_{k+1})$\;
        $k \leftarrow k + 1$\;
    }
    
    \Return{$x^* = x_k$}\;
    
    \caption{Algoritmo de Gradiente Descendente }
\end{algorithm}$$
