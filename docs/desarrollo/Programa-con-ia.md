---
sidebar_position: 1
---

# Creación de proyectos con IA de manera estructurada

Para poder crear proyectos de manera estructurada y que puedas hacer que la IA siga tu camino y no te lleve por el suyo, es neceario tener un proceso de creación, si inviertes un poco de tiempo al establecer ésto te ahorrás mucho mas tiempo en repasar y repasar módulos o funcionalidades que quedaron mal desde el principio.

Sigue estos 5 pasos que te ayudarán a establecer la ruta a seguir.

## 1. Define la idea en Lenguaje Natural (Alto Nivel)

Lo primero es plasmar la idea central del proyecto o del _hito_ en el lenguaje más sencillo posible. No necesitamos especificaciones técnicas complejas, solo la **idea de alto nivel**.

Es crucial enfocarse en el primer hito, no en todo el tiempo de vida de la aplicación.

## 2. Solicita Features y Escenarios en Gherkin

Pasa la idea a tu LLM preferido y pidele que te proponga una serie de _features_ y escenarios en formato **Gherkin**

¿Por qué Gherkin? Es ideal si practicas [BDD/TDD](https://katalon.com/resources-center/blog/tdd-vs-bdd), ya que establece una relación directa entre funcionalidad y los tests.

## 3. Persiste los Features en archivos `.feature`

Crea una carpeta `docs/features` y pide a la IA que cree los ficheros `.feature` y sus escenarios ahí.

ESTA ES LA CLAVE PARA LIBERAR EL CONTEXTO: La conversación con la IA es efímera, pero la planificación completa queda persistida en tus archivos. Retomas la conversación sin perder el progreso.

## 4. Implementa un fichero `PROGRESS.md`

Crea un fichero `PROGRESS.md` que actúe como un _tracker_ de desarrollo, identificando en que punto del proyecto estamos.

Que lo gestione la IA, pidele que mantenga esta _checklist_ actualizada cada vez que completemos un paso.

Así, los _prompts_ posteriores solo serían: "Desarrolla el próximo escenario", y la IA sabe desde donde seguir.

## 5. Desarrolla escenario por escenario (metódico)

Finalmente, pidele a la IA que desarrolle el código paso a paso, según tu flujo de escenarios. Cada escenario se revisa, se prueba y se hace _commit_ de forma independiente.
