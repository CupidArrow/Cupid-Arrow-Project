#### Universidad Peruana de Ciencias Aplicadas
#### Ingeniería de Software
#### Complejidad Algorítmica - WS6B
<hr>

# <div align="center">Informe TF</div>

<p align="center">
    <strong>Universidad Peruana de Ciencias Aplicadas</strong><br>
    <img src="https://upload.wikimedia.org/wikipedia/commons/f/fc/UPC_logo_transparente.png"></img><br>
    <strong>Ingeniería de Software - 5to Ciclo</strong><br>
    <strong>Complejidad Algorítmica - WS6B</strong><br>
    <strong>Profesor: Luis Martín Canaval Sánchez</strong><br>
</p>


## Team Members:

<div align="center">
    <table>
        <tr>
            <th>Member</th>
            <th>Code</th>
        </tr>
        <tr>
            <td>Castillo Robles, Steve</td>
            <td>U202121679</td>
        </tr>
        <tr>
            <td>Quito Igreda, Cristian Andrés</td>
            <td>U202121882</td>
        </tr>
        <tr>
            <td>Esquivel Aguayo, Diego Martín</td>
            <td>U202116749</td>
        </tr>
    </table>
</div>
<br>

### <div align="center">Ciclo 2023-02</div>
<br><br>

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
El diseño de nuestra aplicación de citas ha sido meticulosamente elaborado para brindar a los usuarios una experiencia intuitiva y atractiva. Con una interfaz limpia y moderna, la aplicación presenta colores cálidos y vibrantes que crean un ambiente acogedor y agradable. La inclusión de imágenes de alta resolución y perfiles detallados permite a los usuarios conocer mejor a sus posibles coincidencias. Además, la aplicación ha sido diseñada con un enfoque en la privacidad y la seguridad, garantizando que los usuarios se sientan cómodos al explorar conexiones significativas en un entorno digital.
* Diseño en Figma: [Cupid Arrow Design](https://www.figma.com/file/gdCB2vb2MLBAO4eaTEosga/Untitled?type=design&node-id=0%3A1&mode=design&t=DCJNDd5DPVKsSYui-1)
<div>
    <img src="https://cdn.discordapp.com/attachments/1150821498878185663/1172783188129628281/Part1.png?ex=65619275&is=654f1d75&hm=4a905385a5284cf7b33692490db656708811875341b98e0aea57310dead95570&" alt="Diseño Cupid Arrow 1"/>
</div>
<div>
    <img src="https://cdn.discordapp.com/attachments/1150821498878185663/1172783188427415557/Part2.png?ex=65619275&is=654f1d75&hm=39bd61209072c1a309df69cf4c11125869ec5a4bcbdb4916984c217ccb95217a&" alt="Diseño Cupid Arrow 2"/>
</div>
Como se puede apreciar en las imagenes anteriores, nuestra aplicación de citas se distingue por su enfoque "First Desktop", lo que significa que se ha priorizado la experiencia del usuario en plataformas de escritorio para asegurar una interacción fluida y cómoda desde computadoras. La interfaz se adapta de manera elegante a pantallas más grandes, aprovechando al máximo el espacio visual disponible y ofreciendo una disposición de elementos que facilita la exploración de perfiles y la gestión de preferencias.

## Validación de resultados y pruebas.
Este proyecto tiene como objetivo detectar patrones y relaciones significativas en los datos relacionados con el alto índice de divorcios en Perú, con la finalidad de abordar este problema mediante el uso de  Union-Find Disjoint Sets (UFDS). De esta manera, el usuario podrá encontrar quienes son las personas con las que mejor se puede relacionar en función de su ciuidad, sexo e intereses.

### Resultados del backend:
<div>
    <img src="https://cdn.discordapp.com/attachments/1150821498878185663/1177250840000602182/image.png?ex=6571d348&is=655f5e48&hm=12b8086d2e81db802fceb0be9c56f7a005dd7fd69ec6c6ea9994114b118c9f08&" alt="Backend test 1"/>
</div>
<div>
    <img src="https://media.discordapp.net/attachments/1150821498878185663/1177250586056474706/image.png?ex=6571d30b&is=655f5e0b&hm=61b5f1a185d5dca07dd411249e3b8b8f31ab27439b1fec486796083be9ddfcb4&=&format=webp&width=1148&height=646" alt="Backend test 2"/>
</div>

### Resultados del frontend conectado al backend:
<div>
    <img src="https://media.discordapp.net/attachments/1145753804864749568/1177241855881138207/image.png?ex=6571caea&is=655f55ea&hm=ad95e36872ec3e569fdfae792423637f6649dc2b7fc5062df3823bf1decdb453&=&format=webp&width=1210&height=646" alt="Frontend test 1"/>
</div>
<div>
    <img src="https://cdn.discordapp.com/attachments/1145753804864749568/1177243098301071410/image.png?ex=6571cc12&is=655f5712&hm=160187f150d51055a8e140498965cf3432071104f0c9b693734ba54c52626091&" alt="Frontend test 2"/>
</div>
<div>
    <img src="https://cdn.discordapp.com/attachments/1145753804864749568/1177243886758940722/image.png?ex=6571ccce&is=655f57ce&hm=55414f2f3ccb618d7a7595421f9d56f6bc7f7e4dc76878e2095e5f857c2fdb7e&" alt="Frontend test 2">
</div>

## Conclusiones
* La elección de UFDS se basó en su eficacia para formar grupos de similitud en conjuntos de datos complejos, respaldada por investigaciones previas y mejores prácticas.
* La interfaz de usuario de la aplicación de citas refleja una atención meticulosa hacia la experiencia del usuario, la eficiencia en la interacción y la alineación con los objetivos centrales de la aplicación para mejorar la calidad de las relaciones y reducir la tasa de divorcio.
* La mejora continua de nuestro trabajo fue esencial para asegurar el éxito y la efectividad de la aplicación de citas.De esta manera, optimizamos constantemente la experiencia del usuario, incorporando la retroalimentación de los usuarios y adaptándonos a las tendencias emergentes.
* Las reuniones constantes y las sesiones colaborativas permitieron un proceso de desarrollo más ágil y efectivo, optimizando la calidad y funcionalidad de la aplicación.

## Referencias Bibliográficas
* Aggarwal, C. C. (2015). Data Clustering: Algorithms and Applications. CRC Press. Recuperado de https://www.taylorfrancis.com/books/data-clustering-charu-aggarwal/e/10.1201/b18438
* Instituto Nacional de Estadística. (2013). _Divorcios según estado civil de los cónyuges al contraer el matrimonio_ [Conjunto de datos]. Instituto Nacional de Estadística (INE). [https://www.ine.es/](https://www.ine.es/)
* McPherson, M., Smith-Lovin, L., & Cook, J. M. (2001). Birds of a feather: Homophily in social networks. Annual Review of Sociology, 27(1), 415-444. Recuperado de https://www.annualreviews.org/doi/abs/10.1146/annurev.soc.27.1.415
* Pérez et al. (2009). El divorcio: una aproximación psicológica. _La Revue du REDIF_, _2_, 39-46. [https://d1wqtxts1xzle7.cloudfront.net/39320485/univ._ramon_llull-libre.pdf?1445359097=&response-content-disposition=inline%3B+filename%3DEl_divorcio_una_aproximacion_psicologica.pdf&Expires=1695916106&Signature=cxEayaE2IUzagCtmrWDgsKsNrGYmw9Y~kSLKJhYigMExK6w4IwFFYhfS~o-0QcBnPjXZMBphRme2bD6gPboMJ~DBW-si4-zngp08LGSvZrhjKvG~tuX2KpoNeoiQagrTuZpcCVYWXgRzeyl5YoX4iEbFAfXfBQUkb2NdfmhlwXWE7DWEdl7fzayhmaKg5ywEorgjU36WmUxPZkJaKAMR4FlTGqZoEr4OON2eIfcQReRb3vUXxYmSKvNiDyB~14APyIjQySQ7TBgUSrW7vQyHQTQq~EWnXUKGKXe5hLX84taMaGKjY3WXYXfUo0YH0RArrQKtLeHdOO-YyqczTdlyjg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA](https://d1wqtxts1xzle7.cloudfront.net/39320485/univ._ramon_llull-libre.pdf?1445359097=&response-content-disposition=inline%3B+filename%3DEl_divorcio_una_aproximacion_psicologica.pdf&Expires=1695916106&Signature=cxEayaE2IUzagCtmrWDgsKsNrGYmw9Y~kSLKJhYigMExK6w4IwFFYhfS~o-0QcBnPjXZMBphRme2bD6gPboMJ~DBW-si4-zngp08LGSvZrhjKvG~tuX2KpoNeoiQagrTuZpcCVYWXgRzeyl5YoX4iEbFAfXfBQUkb2NdfmhlwXWE7DWEdl7fzayhmaKg5ywEorgjU36WmUxPZkJaKAMR4FlTGqZoEr4OON2eIfcQReRb3vUXxYmSKvNiDyB~14APyIjQySQ7TBgUSrW7vQyHQTQq~EWnXUKGKXe5hLX84taMaGKjY3WXYXfUo0YH0RArrQKtLeHdOO-YyqczTdlyjg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)
* Ricou, J. (2016, 2 de octubre). _Divorcios: cada cinco minutos se rompe una pareja_. La Vanguardia. Recuperado el 28 de setiembre de 2023, de [https://www.lavanguardia.com/vida/20161002/41720816201/cada-cinco-minutos-se-rompe-una-pareja.html](https://www.lavanguardia.com/vida/20161002/41720816201/cada-cinco-minutos-se-rompe-una-pareja.html)

## Anexos
* Gráfico estadístico de divorcios totales
<p>
    <img src="https://cdn.discordapp.com/attachments/1037343952694685706/1156975561630027826/image.png?ex=6516ecf5&is=65159b75&hm=708e9c04a5d982ade1f6f3815abe4762e3f5f2745e65036fe7e01cede057e879&" alt="Gráfico estadistico de divorcios totales">
</p>
