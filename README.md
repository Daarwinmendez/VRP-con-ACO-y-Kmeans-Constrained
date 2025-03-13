# Proyecto VRP con ACO y Clustering

## Descripción

Este proyecto tiene como objetivo implementar una solución al problema de enrutamiento de vehículos (VRP) utilizando el algoritmo de optimización de colonias de hormigas (ACO) en conjunto con un algoritmo de clustering.

El problemset está disponible gracias al Ingeniero y maestro **Carlos Ogando**.

## Estructura del Proyecto

- **Clustering:** Se utiliza K-Means con restricción de capacidad para agrupar los puntos de entrega en clusters, teniendo en cuenta la demanda de cada punto y la capacidad de los vehículos.
- **ACO:** El algoritmo ACO se ejecuta en cada cluster para encontrar la ruta óptima dentro del mismo. Se considera el depósito como punto de inicio y fin de cada ruta.
- **Flujo General:** Se crea un flujo para integrar el clustering y el ACO, que procesa los datos, aplica los algoritmos y almacena los resultados en un dataframe.
- **Validación:** Se realiza una comparación con soluciones previamente calculadas utilizando Clarke-Wright (CW) y fuerza bruta (BF), y se calculan métricas de error como MAE y MSE.

## Instalación

Para ejecutar el proyecto en tu máquina local, instala las dependencias con:

```bash
pip install -r requirements.txt
```

## Uso

1. **Importar datos:** Asegúrate de tener los datos de entrada en los formatos correspondientes (Parquet, Excel) y ubicados en las rutas indicadas en el código.
2. **Ejecutar el flujo general:** Ejecuta las celdas de código en secuencia, comenzando por la importación de librerías y la carga de datos, hasta llegar a la validación de resultados.
3. **Análisis de resultados:** Interpreta los resultados obtenidos, como el costo total de las rutas, el número de vehículos utilizados y las métricas de error.

## Contribuyentes

- **Darwin Mendez:** [GitHub](https://github.com/Daarwinmendez), [LinkedIn](https://www.linkedin.com/in/darwin-mendez-061881185)
- **Roither Sanchez:** [GitHub](https://github.com/XTrollaX), [LinkedIn](https://www.linkedin.com/in/roither-s%C3%A0nchez-sosa-b77b37244/)
- **Michael García:** [GitHub](https://github.com/MichaGF0305), [LinkedIn](https://www.linkedin.com/in/michael-david-garc%C3%ADa-feliz-37446b296/)
- **Camily García:** [GitHub](https://github.com/CamyG18), [LinkedIn](https://www.linkedin.com/in/camily-garc%C3%ADa-7b4632319/)

## Sugerencias para mejorar

- Explorar distintos parámetros del ACO y del clustering para optimizar aún más la solución.
- Comparar el rendimiento con otros algoritmos de enrutamiento.
- Considerar la visualización de las rutas en un mapa.
