# ESTUDIOS ESPECÍFICOS DE CORRELACIONES, VOLATILIDAD Y PERFORMANCE DE ACTIVOS DE RENTA VARIABLE

# CORRELACIONES

Permite llevar un registro de activos correlacionados (más y menos). Útil para ayudar a armar portafolios de inversión y administrar el riesgo.

## CORRELACIONES - INDICE DE FUNCIONES:

- getCorr(activos, años): Esta función devuelve un dataframe con las correlaciones de los activos pasados como lista y un gráfico de calor para una mejor visualización.
- getCorrRank(activos, activo, años): Esta función devuelve una serie ordenada de los activos más correlacionados a menos correlacionados del activo en cuestión.
- clusterizar_dend(tickers, años): Es una función para graficar mapas de correlación a través de dendogramas, clusterizando tickers, agrupando los más correlacionados primero.
- getPeers(symbol): Función útil para encontrar acciones similares a una acción (correlacionadas), para mercados que no conocemos bien, etc.

# ESTACIONALIDAD

Estudio de estacionalidad por períodos para determinar patrones en los rendimientos de activos de renta variable o índices y operarlos en forma razonable.

## ESTACIONALIDAD - INDICE DE FUNCIONES:

- rends_mensuales(ticker, tipo, tipoacum, interval, period = None, data_from = None, data_to = None): retorna un dataframe y un gráfico con los rendimientos acumulados o promedio (según parámetro) mensuales para visualizar estacionalidad.

- rends_anuales(ticker, tipo, interval, period = None, data_from = None, data_to = None): retorna un dataframe y un gráfico con los rendimientos acumulados anuales para visualizar estacionalidad.

- meses_favorables(ticker, tipo, tipoacum, interval, period = None, data_from = None, data_to = None): retorna los meses de mejor rendimiento acumulado o de promedio diario. Análogo a rends_mensuales, pero ordenado en forma descendente y tabulado.

- heatmap_estacional(ticker, tipo, interval, period = None, data_from = None, data_to = None): es un heatmap de rendimientos mensuales para varios años (todo parametrizable) en colores de modo de visualizar estacionalidades.

# PERFORMANCE

Estudios de performance superpuesta y comparativos. Implementar estudios de performance de activos superpuestos en gráficos. O distintas variables del mismo activo (necesitan distinto eje Y). O bien mismo activo en distintos períodos de tiempo. Para buscar patrones, entender movimientos, buscar estacionalidades, etc. Para más detalle observar la descripción de las funciones debajo.

## PERFORMANCE - INDICE DE FUNCIONES:

- plotPriceVolat(symbol, desde, hasta, n = 20, log = False): Esta función grafica precio y volatilidad de un ticker en particular entre dos fechas especificadas.
- plotPricePrice(symbols, desde, hasta, log = False): Esta función grafica la evolución de precios de dos tickers superpuestos.
- plotPerformance(ticker, years, log = False): Gráfico de evolución de precio de cierre para varios años (parametrizable) del mismo ticker. Permite visualizar estacionalidades, ver cómo se suele comportar en distintas épocas del año, etc.
- plotPerformanceIndex(ticker, years): Gráfico de evolución rendimiento acumulado base 100 del mismo ticker. Permite visualizar estacionalidades, ver cómo se suele comportar en distintas épocas del año, etc.

AGRADECIMIENTOS: con apoyo de código de la serie de libros "Python para Finanzas Quant" de Juan Pablo Pisano.