**Objetivo**

Adaptar un modelo base de simulación de eventos discretos (DES) para evaluar la latencia y la gestión de recursos de una API de Machine Learning en producción, utilizando Teoría de Colas y políticas de inventario de recursos computacionales.

**Indicaciones:**

1. Tomar como referencia el código del archivo [(ver archivo)](https://colab.research.google.com/drive/1KlfxGnaELS0lumqNC4cnUL9rhyH7VIcJ?usp=sharing) visto en clase.
2. Modificar el código para simular la infraestructura de la API utilizando estrictamente los siguientes parámetros operativos:
    - Tasa de llegadas (lambda): 30 peticiones de usuarios por minuto.
    - Tasa de servicio (mu): 10 imágenes procesadas por minuto.
    - Servidores (c): 4 Nodos GPU.
    - Stock inicial: 500 créditos de nube (Tokens).
    - Punto de reorden (s): 50 créditos.
    - Cant. de recarga (Q): 400 créditos.
    - Lead Time (retraso): Media de 2 minutos.
3. Renombrar las variables y entidades del código original para que estén alineadas al nuevo problema.
4. Configurar el tiempo de simulación para evaluar un escenario de 60 minutos continuos.
5. Ejecutar 30 réplicas del escenario y mostrar en la consola de resultados:
    - El Intervalo de Confianza al 95% del tiempo de espera en cola (W_q).
    - El promedio de predicciones fallidas por falta de créditos.
    - La utilización teórica ($\rho$) de los nodos GPU.
6. Analizar por qué el sistema arroja predicciones fallidas a pesar de tener una utilización de hardware estable.
7. Modificar el código encontrando y configurando el valor exacto del Punto de Reorden (s) necesario para asegurar que las predicciones fallidas lleguen a cero absoluto.

**Entregables:**
- Link del repositorio de GitHub donde se encuentre alojado el archivo con el código modificado y 100% funcional.
- Dentro del mismo código, incluir varias celdas de texto que responda al análisis del paso 6 y justifique el nuevo valor asignado en el paso 7.
- Nota: Si el link de GitHub está roto, el repositorio es privado o no se puede acceder al código por cualquier motivo, la calificación será automáticamente de cero (0).
