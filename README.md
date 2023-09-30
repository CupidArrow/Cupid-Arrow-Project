# Cupid-Arrow-Project

## Descripción del problema
La tasa de divorcios a nivel mundial ha alcanzado un nivel alarmante, pues en Perú hubo un aumento de más de 25% en divorcios durante los últimos 9 años y con una tendencia creciente (INE). Esta preocupante tendencia refleja cambios significativos en la dinámica de las relaciones y el matrimonio en la sociedad peruana. Factores como la evolución de las expectativas en las parejas, la independencia económica de ambos cónyuges y la creciente aceptación social del divorcio como una opción legítima para poner fin a relaciones insatisfactorias contribuyen a este incremento (Ricou, 2016). El proceso de divorcio puede ser emocionalmente agotador y traumático, ya que las parejas se enfrentan a una serie de desafíos emocionales y psicológicos. La sensación de fracaso y pérdida puede generar sentimientos de tristeza, culpa, enojo y ansiedad. Los cónyuges a menudo deben lidiar con la separación de un compañero de vida, la reestructuración de las relaciones familiares y la adaptación a una nueva realidad. Sin embargo, Los hijos también pueden verse afectados, experimentando confusión, tristeza, culpabilidad y estrés debido a la ruptura de la unidad familiar (Pérez et al., 2009).

## Descripción del conjunto de datos (dataset)

El conjunto de datos que usaremos será un json que fue creado por un script hecho en python donde almacenamos datos de nombres masculinos, femeninos, intereses (Cine, Música, etc...) y las ciudades donde residen. El script se encuentra en la carpeta `data` con el nombre de `scripts.py` y el json generado se encuentra en la carpeta `data` con el nombre de `data.json`.
el json tiene los siguientes parámetros:
* `id`: Identificador único del usuario
* `name`: Nombre del usuario
* `sex`: Género del usuario
* `city`: Ciudad donde reside el usuario
* `interests`: Intereses del usuario

El número de usuarios en el conjuto de datos es de 10 mil usuarios. en los cuales encontramos tanto hombres como mujeres, con intereses variados y de diferentes ciudades del Perú.

<div>
    <img src="https://media.discordapp.net/attachments/1145753804864749568/1157718405311369257/image.png?ex=6519a0c9&is=65184f49&hm=cd39acf64aceada5c9d1cb01f4c5132442723f340563834f942b0bd094f0ef01&=" alt="Imagen de Grafo"/>
</div>

La imagen representa a un conjunto de grafos donde las conexiones de cada nodo representa un usuario y cada arista representa una conexión entre dos usuarios.
Estas conexiones se dan cuando dos usuarios tienen intereses en común, viven en la misma ciudad y son del género seleccionado.


## Propuesta
**Objetivo:**
El objetivo de esta propuesta es abordar el problema del alto índice de divorcio en la sociedad actual mediante la implementación de un sistema de búsqueda y recomendación de parejas en una aplicación de citas en línea. Nuestra meta principal es proporcionar a los usuarios una herramienta que les permita encontrar relaciones más sólidas y compatibles desde el inicio, reduciendo así la tasa de divorcio y promoviendo relaciones amorosas más saludables y duraderas.

**Técnica Utilizada: Union-Find Disjoint Sets (UFDS)**
Hemos decidido emplear la técnica de Union-Find Disjoint Sets (UFDS) como la piedra angular de nuestra solución debido a sus ventajas en la agrupación de usuarios en conjuntos o clústeres en función de criterios de similitud. Esta elección se respalda tanto por su versatilidad como por su capacidad para adaptarse a las necesidades específicas de los usuarios en la búsqueda de parejas compatibles.

La UFDS nos permitirá crear grupos de usuarios que comparten intereses, características o preferencias similares. Al agrupar a los usuarios de esta manera, podremos ofrecer recomendaciones más precisas y relevantes al sugerir a los usuarios que interactúen dentro de su grupo de afinidad. Esta estrategia se basa en la idea de que las relaciones sólidas a menudo se desarrollan entre personas con intereses y valores comunes (McPherson et al., 2001).

**Metodología:**
- <b>Recopilación de datos:</b> Inicialmente, obtendremos información de diversas fuentes, incluyendo encuestas, perfiles de usuarios, datos públicos disponibles en línea y registros de citas previas dentro de nuestra aplicación. Estos datos serán fundamentales para identificar similitudes y patrones entre los usuarios, permitiéndonos realizar recomendaciones más precisas y personalizadas.

- <b>Preprocesamiento de datos:</b> Realizaremos una limpieza exhaustiva y un preprocesamiento de los datos para eliminar duplicados, valores atípicos y garantizar la calidad de los datos.

- <b>Aplicación de UFDS:</b> Utilizaremos UFDS para agrupar a los usuarios en clústeres basados en criterios de similitud, como intereses, ubicación geográfica, edad y otros atributos relevantes.

- <b>Desarrollo de algoritmos de recomendación:</b> Para cada clúster, desarrollaremos algoritmos de recomendación personalizados que sugieran parejas compatibles dentro del mismo grupo.

- <b>Evaluación y Ajuste Continuo:</b> Realizaremos pruebas exhaustivas y evaluaciones de las recomendaciones proporcionadas por el sistema. Ajustaremos los algoritmos según la retroalimentación de los usuarios para mejorar la precisión y la satisfacción del usuario.

- <b>Lanzamiento y Monitoreo:</b> Lanzaremos la aplicación y continuaremos monitoreándola para realizar mejoras y ajustes adicionales.

La elección de UFDS como técnica central de agrupación se basa en su eficacia probada en la formación de grupos de similitud en conjuntos de datos complejos. Además, al ser una técnica bien establecida, podemos aprovechar la investigación previa y las mejores prácticas en la aplicación de UFDS para mejorar nuestras recomendaciones (Aggarwal, 2015).

En resumen, esta propuesta tiene como objetivo abordar el problema del alto índice de divorcio mediante la aplicación de la técnica UFDS para agrupar usuarios y proporcionar recomendaciones de parejas más efectivas en una aplicación de citas en línea.

## Diseño del aplicativo

## Validación de resultados y pruebas.

## Conclusiones

## Referencias Bibliográficas
* Ricou, J. (2016, 2 de octubre). _Divorcios: cada cinco minutos se rompe una pareja_. La Vanguardia. Recuperado el 28 de setiembre de 2023, de [https://www.lavanguardia.com/vida/20161002/41720816201/cada-cinco-minutos-se-rompe-una-pareja.html](https://www.lavanguardia.com/vida/20161002/41720816201/cada-cinco-minutos-se-rompe-una-pareja.html)
* Pérez et al. (2009). El divorcio: una aproximación psicológica. _La Revue du REDIF_, _2_, 39-46. [https://d1wqtxts1xzle7.cloudfront.net/39320485/univ._ramon_llull-libre.pdf?1445359097=&response-content-disposition=inline%3B+filename%3DEl_divorcio_una_aproximacion_psicologica.pdf&Expires=1695916106&Signature=cxEayaE2IUzagCtmrWDgsKsNrGYmw9Y~kSLKJhYigMExK6w4IwFFYhfS~o-0QcBnPjXZMBphRme2bD6gPboMJ~DBW-si4-zngp08LGSvZrhjKvG~tuX2KpoNeoiQagrTuZpcCVYWXgRzeyl5YoX4iEbFAfXfBQUkb2NdfmhlwXWE7DWEdl7fzayhmaKg5ywEorgjU36WmUxPZkJaKAMR4FlTGqZoEr4OON2eIfcQReRb3vUXxYmSKvNiDyB~14APyIjQySQ7TBgUSrW7vQyHQTQq~EWnXUKGKXe5hLX84taMaGKjY3WXYXfUo0YH0RArrQKtLeHdOO-YyqczTdlyjg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA](https://d1wqtxts1xzle7.cloudfront.net/39320485/univ._ramon_llull-libre.pdf?1445359097=&response-content-disposition=inline%3B+filename%3DEl_divorcio_una_aproximacion_psicologica.pdf&Expires=1695916106&Signature=cxEayaE2IUzagCtmrWDgsKsNrGYmw9Y~kSLKJhYigMExK6w4IwFFYhfS~o-0QcBnPjXZMBphRme2bD6gPboMJ~DBW-si4-zngp08LGSvZrhjKvG~tuX2KpoNeoiQagrTuZpcCVYWXgRzeyl5YoX4iEbFAfXfBQUkb2NdfmhlwXWE7DWEdl7fzayhmaKg5ywEorgjU36WmUxPZkJaKAMR4FlTGqZoEr4OON2eIfcQReRb3vUXxYmSKvNiDyB~14APyIjQySQ7TBgUSrW7vQyHQTQq~EWnXUKGKXe5hLX84taMaGKjY3WXYXfUo0YH0RArrQKtLeHdOO-YyqczTdlyjg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)
* Instituto Nacional de Estadística. (2013). _Divorcios según estado civil de los cónyuges al contraer el matrimonio_ [Conjunto de datos]. Instituto Nacional de Estadística (INE). [https://www.ine.es/](https://www.ine.es/)
* McPherson, M., Smith-Lovin, L., & Cook, J. M. (2001). Birds of a feather: Homophily in social networks. Annual Review of Sociology, 27(1), 415-444. Recuperado de https://www.annualreviews.org/doi/abs/10.1146/annurev.soc.27.1.415
* Aggarwal, C. C. (2015). Data Clustering: Algorithms and Applications. CRC Press. Recuperado de https://www.taylorfrancis.com/books/data-clustering-charu-aggarwal/e/10.1201/b18438

## Anexos
* Gráfico estadístico de divorcios totales
<p>
    <img src="https://cdn.discordapp.com/attachments/1037343952694685706/1156975561630027826/image.png?ex=6516ecf5&is=65159b75&hm=708e9c04a5d982ade1f6f3815abe4762e3f5f2745e65036fe7e01cede057e879&" alt="Gráfico estadistico de divorcios totales">
</p>
