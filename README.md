# Generador de letras de The Beatles
Mediante Cadenas de Markov.

El modelo se construye en base a tres diccionarios en Python:

- Inicial: Para generar la primer palabra
- Primer Orden: Para generar la segunda palabra dada la primera
- Segundo Orden: Para generar todas las palabras siguientes en base a las dos anteriores

El final de cada renglón se determina por el token especial "FIN", que tiene una probabilidad asignada dadas las dos últimas palabras.

Las probabilidades de los diccionarios se calculan en base a las frecuencias observadas en las letras de The Beatles.

Por ejemplo, si después de las palabras "the dog" se observaron las palabras "is" y "has", 8 y 2 veces respectivamente,
entonces la probabilidad de "is" dado que las dos palabras anteriores son "the dog" será de 0.8 (8 / (8+2)). Esta idea, tan simple como suena, es todo 
lo que hay que entender sobre cómo funciona este modelo.
