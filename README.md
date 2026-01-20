## Comparativa de tecnologías para entrenamiento de modelos y despliegue como API

| Criterio                                   | Peso (1–5) | Python (1–5) | R (1–5) | Java (1–5) | Node (1–5) |
|--------------------------------------------|------------|--------------|---------|------------|------------|
| Ecosistema IA/ML (librerías, comunidad)    | 5          | 5            | 4       | 3          | 2          |
| Productividad / prototipado                | 5          | 5            | 4       | 3          | 4          |
| Rendimiento / latencia                     | 3          | 3            | 2       | 5          | 4          |
| Concurrencia / I-O / servicios (API)       | 4          | 3            | 2       | 5          | 5          |
| Integración Big Data / pipelines           | 3          | 5            | 3       | 5          | 3          |
| Despliegue y portabilidad                  | 4          | 4            | 3       | 5          | 4          |
| Mantenibilidad / tipado / tooling          | 3          | 3            | 2       | 5          | 3          |
| Talento disponible                         | 4          | 5            | 3       | 5          | 4          |
| **TOTAL ponderado**                        |            | **153**      | **103** | **146**    | **131**    |


##Conclusion

Para el caso de uso planteaado (entrenar un modelo y desplegarlo como API de predicciones), el mejor lenguaje es Python.
Su amplio ecosistema de Machine Learning y Deep Learning, con librerias como scikit-learn, permite entrenar modelos de forma rápida, 
eficiente y con abundante soporte de la comunidad. 
Además, frameworks como FastAPI facilitan la creaciónde APIs REST de manera sencilla y mantenible.

El principal riesgo técnico de esta elección es el rendimiento y la escalabilidad en entornos de alta concurrencia, ya que Python
no ofrece el mismo nivel de eficiencia que otros lenguajes en escenarios de latencia muy baja o gran volumen de peticiones.
Para mitigar este riesgo, se puede adoptar una arquitectura híbrida: Python para el entrenamiento y validación del modelo, y
Java para servir el modelo en producción, comunicándose mediante servicios REST o contenedores Docker.
