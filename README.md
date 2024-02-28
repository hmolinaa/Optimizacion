# Optimizacion del Filtro de Hodrick-Prescott mediante el metodo de Gradiente Descendente
Mediante los conociminetos adquiridos y entendiendo los metodos de optimizacion y sus aplicaciones se presenta el siguiente proyecto. Donde inicialmente se describe el problema que queremos optimizar o encontrar su punto optimo, la funcion del filtro de Hodrick-Prescott. Luego, resolvemos el problema de optimizacion $x^*= \text{arg}\min_{\alpha > 0 } f(x)$ implementando el algoritmo del Gradiente Descendente en el lenguaje de programacion de Python. Por ultimo, se muestran los experimentos y resultados obtenidos.

De forma general, el algoritmo que implementamos para el Gradiente Descendente es el siguiente: 

Entradas:
    - x_0: punto inicial
    - f: función objetivo
    - ∇f: gradiente de la función
    - H_f: Hessiana de la función (opcional)

Salida:
    - x^*: punto óptimo

Inicializar k = 0
Calcular g_0 = -∇f(x_0)

Mientras el criterio de alto sea falso:
    Calcular α_k = arg min_{α > 0} f(x_k + α d_k)
    Actualizar x_{k+1} = x_k + α_k g_k
    Calcular g_{k+1} = -∇f(x_{k+1})
    Incrementar k en 1

Devolver x^* = x_k

