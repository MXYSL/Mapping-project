# Mapping Project — Ficha de idea

**Proyecto:** Mapping Project  
**Tipo:** Aplicación de creación y edición de *projection mapping* (videomapping).  
**Fecha de elaboración:** 9 de octubre de 2026.  
**Estado:** Propuesta inicial; hipótesis de necesidad pendiente de validar.

## 1. Ruta elegida y motivo

**Ruta elegida:** desarrollo de una aplicación original multiplataforma, no un videojuego ni la reproducción de un proyecto base.

Se propone crear una herramienta que permita preparar proyecciones visuales ajustadas a objetos y superficies físicas, mediante la definición manual de regiones, vértices y cuadrículas, y la asignación de imágenes o videos. Se elige esta ruta porque atiende una tarea creativa concreta y permite entregar una primera versión verificable sin depender de reconocimiento automático de espacios ni de modelado tridimensional avanzado.

La solución contempla **tres formas de acceso**: aplicación Android, aplicación web desde un navegador y aplicación de escritorio para Windows 11. Las tres compartirán el concepto de proyecto y sus datos, pero no tendrán necesariamente las mismas herramientas. La infraestructura de servicios se ejecutará mediante Docker; esto no implica que las aplicaciones Android o Windows se ejecuten dentro de contenedores.

## 2. Usuario y contexto

**Usuario principal:** estudiante o creador audiovisual principiante que necesita preparar una proyección sobre un objeto o una superficie real y no domina software especializado.

**Contexto concreto:** en un aula, taller, estudio o espacio para un evento, durante la preparación y las pruebas de una instalación visual. Por ejemplo, una estudiante dispone de una computadora con Windows 11, un proyector y varias cajas que desea iluminar con contenido coordinado. Utiliza el celular para fotografiar la escena y hacer ajustes iniciales; después abre el proyecto en la computadora para calibrarlo y proyectarlo. También puede consultar y editar proyectos desde el navegador.

## 3. Problema observable

**Frase del problema:** Crear una proyección visual que se ajuste correctamente a objetos o superficies reales resulta difícil para quienes no conocen las herramientas técnicas de videomapping.

El problema puede observarse cuando una persona intenta adaptar imágenes o videos a la forma de un objeto: debe delimitar las superficies, corregir la perspectiva y comprobar físicamente si el contenido coincide con los bordes. La necesidad y su frecuencia **todavía no se han comprobado mediante pruebas con usuarios**.

## 4. Alternativa actual

Actualmente, el usuario puede recurrir a software especializado de videomapping, a herramientas generales de edición audiovisual o a la preparación manual de videos ya deformados para un escenario específico. Estas alternativas permiten realizar el trabajo, pero pueden exigir aprendizaje técnico, pasos manuales adicionales o un flujo menos cómodo entre celular y computadora. No se afirma que todas sean costosas ni que carezcan de funciones móviles; esas comparaciones requieren investigación posterior.

## 5. Tarea principal

**Crear, ajustar y guardar un proyecto de videomapping** a partir de una imagen de referencia de la escena: delimitar una o más superficies con puntos editables, seleccionar una geometría prediseñada cuando corresponda, asignar una imagen o video, revisar una vista previa y enviar el resultado a un proyector conectado a Windows 11.

**Recorrido básico:** abrir la aplicación → crear proyecto → capturar o cargar fotografía → definir superficie y ajustar vértices/cuadrícula → elegir geometría o contenido del catálogo → previsualizar → guardar → abrir en Windows y proyectar.

## 6. Criterio de éxito

La primera versión se considerará funcional si, en una prueba guiada, una persona puede:

1. Crear un proyecto nuevo y asignarle un nombre válido.
2. Cargar una fotografía de referencia.
3. Crear al menos una superficie de cuatro vértices y modificar la posición de sus puntos.
4. Elegir un elemento prediseñado del catálogo básico y asignar una imagen o video compatible a la superficie.
5. Observar la transformación del contenido en una vista previa.
6. Guardar, cerrar y volver a abrir el proyecto sin perder las coordenadas ni las referencias al contenido.
7. Desde la aplicación de Windows 11, presentar la salida de proyección a pantalla completa en un proyector reconocido como segunda pantalla.

**Verificación:** cada punto debe producir un resultado observable por otra persona. La alineación física fina dependerá de una calibración manual; no se exige precisión automática ni reconstrucción tridimensional exacta.

## 7. Alcance de la primera versión (MVP)

**Funciones comunes:** creación y apertura de proyectos; importación de fotografía; editor básico de superficies con cuadrícula y vértices; catálogo inicial de geometrías simples (por ejemplo, plano, cubo y prisma rectangular); asignación de imágenes y videos compatibles; vista previa; guardado y recuperación de proyectos.

**Android:** captura de fotografías, consulta de proyectos, creación y ajustes básicos de superficies, elección de contenido y vista previa. No requiere ofrecer todas las herramientas de escritorio.

**Web:** acceso a proyectos, carga de fotografías y edición básica desde un navegador moderno. No se garantiza control directo de un proyector desde el navegador en esta versión.

**Windows 11:** editor de mapping con herramientas más completas de ajuste manual, vista previa y salida a pantalla completa en una segunda pantalla conectada a un proyector.

**Infraestructura:** backend/API y base de datos configurables con Docker Compose; repositorio GitHub con documentación y código fuente. Se priorizará que los proyectos puedan conservarse y abrirse de nuevo; la sincronización instantánea entre dispositivos no es obligatoria para el MVP.

## 8. Funciones aplazadas deliberadamente

- Reconstrucción automática de la geometría de una habitación a partir de una fotografía.
- Detección de superficies y calibración automática mediante inteligencia artificial.
- Edición y modelado 3D libre de objetos complejos.
- Mallas de deformación avanzadas, *edge blending* y soporte para múltiples proyectores sincronizados.
- Control colaborativo simultáneo y sincronización en tiempo real entre varios usuarios.
- Efectos audiovisuales reactivos, seguimiento de objetos en movimiento y realidad aumentada.
- Publicación de una biblioteca comunitaria extensa de modelos o efectos.

Estas funciones se aplazan para concentrar el desarrollo en un flujo sencillo y comprobable de principio a fin.

## 9. Hipótesis pendiente de validar

**Hipótesis:** las personas sin experiencia en videomapping podrán preparar una primera escena con menos dificultades si disponen de cuadrículas editables, figuras prediseñadas, vista previa y una interfaz accesible desde el celular y la computadora.

**Estado:** hipótesis sin validar. Todavía no se cuenta con entrevistas, encuestas, observaciones de uso ni pruebas de prototipo con participantes que permitan sostenerla como un hallazgo.

**Plan de validación propuesto (no realizado):** solicitar a entre tres y cinco estudiantes o creadores principiantes que intenten construir una escena de una superficie con un prototipo; registrar tiempo de realización, errores, puntos de confusión y si completan la tarea sin ayuda. Comparar esos resultados con la hipótesis antes de ampliar el alcance.

## 10. Registro de evidencia

| Fecha | Método | Resultado real | Interpretación |
|---|---|---|---|
| 9 de octubre de 2026 | Definición conceptual del proyecto y revisión de ejemplos audiovisuales aportados como referencia | Se concretó la propuesta de una herramienta multiplataforma de videomapping con editor por superficies y catálogo. No se realizaron pruebas con usuarios. | Los ejemplos inspiran la funcionalidad, pero **no demuestran una necesidad de mercado ni validan la facilidad de uso**. |

**Declaración:** a la fecha de esta ficha, la idea permanece como **hipótesis pendiente de validación**. No se presentan cifras de adopción, entrevistas ni pruebas que no hayan ocurrido.
