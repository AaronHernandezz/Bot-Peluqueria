Proyecto: Chatbot con IA para automatizar citas en negocios locales

He desarrollado un chatbot con inteligencia artificial enfocado a resolver un problema muy común en negocios locales como peluquerías: la gestión manual de citas.

Muchos negocios pierden tiempo respondiendo mensajes, organizando horarios y gestionando reservas de forma manual. Además, los clientes esperan respuestas rápidas, algo que no siempre es posible.

Para solucionar esto, he construido un sistema que automatiza completamente este proceso.

 ¿Cómo funciona el sistema?

El chatbot está desarrollado en Python y funciona a través de Telegram como canal de comunicación.

La arquitectura del sistema combina varias piezas clave:

Un bot que recibe los mensajes del usuario
Un modelo de IA (OpenAI) que interpreta lo que el cliente quiere
Un sistema de lógica propio que controla el flujo de la conversación
Integración con Google Calendar para gestionar citas reales

El flujo es sencillo desde el punto de vista del usuario:

El cliente escribe un mensaje
La IA interpreta su intención (consultar o reservar)
El sistema guía paso a paso la reserva
Se confirma la cita
Se guarda automáticamente en el calendario
 
 Parte técnica 
 
Uno de los aprendizajes más importantes del proyecto es que la IA no puede controlar todo.

Por eso, el sistema está diseñado con una arquitectura híbrida:

La IA se encarga de entender el lenguaje natural
El código controla la lógica, las validaciones y las decisiones críticas

Para conseguir esto, implementé un sistema de estado que guarda en todo momento en qué punto está el usuario:

nombre
servicio
fecha
hora
teléfono
si hay una reserva activa
si está pendiente de confirmación

Esto permite que la conversación no se rompa y que el bot guíe correctamente al usuario, incluso si escribe cosas sueltas.

 Problemas reales que tuve que resolver

Durante el desarrollo aparecieron varios problemas importantes:

La IA se salía del flujo de reserva
El bot inventaba precios o servicios
Fallaba la confirmación de citas 
Era posible reservar el mismo horario dos veces
Problemas técnicos con Google Calendar (formatos de fecha y zona horaria)

Todas estas situaciones se resolvieron añadiendo control desde el código:

Sistema de estado para mantener el flujo
Uso de un archivo services.json como única fuente de verdad
Validaciones estrictas de datos
Comprobación de disponibilidad antes de crear citas
Manejo correcto de zonas horarias

 Qué hace diferente a este bot

La clave no es solo usar IA, sino cómo está integrada.

Este sistema:

No depende completamente de la IA
No inventa información
Evita errores críticos
Funciona como una agenda real
Tiene un flujo guiado y robusto

 Enfoque como producto

Más allá de la parte técnica, este proyecto está pensado como producto real.

Se puede ofrecer como un SaaS para negocios locales con un modelo de suscripción:

Plan básico: chatbot + reservas
Plan avanzado: integración con WhatsApp

Costes bajos (IA + infraestructura) y alto margen, lo que lo hace escalable.

 Aprendizajes clave

Este proyecto me ha dejado varias conclusiones importantes:

La IA por sí sola no es suficiente
El control del sistema debe estar en la lógica, no en el modelo
Validar datos es fundamental
Pensar en producto desde el inicio cambia totalmente el enfoque
