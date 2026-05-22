---
title: Preguntas frecuentes sobre el fin de vida útil de Adobe Media SDK (versiones 1.x y 2.x)
description: Obtenga respuestas a preguntas más frecuentes sobre el fin de vida útil de las versiones 1.x y 2.x de Adobe Media SDK (anteriormente, Biblioteca de Video Heartbeat).
source-git-commit: d014c200dd926ccf0116faa50c4bffb1d234e926
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 1%

---


# Preguntas frecuentes sobre el fin de vida útil de Adobe Media SDK (versiones 1.x y 2.x)

Adobe Media SDK **2.x llegó al fin de la compatibilidad el 31 de agosto de 2021**. La biblioteca de Video Heartbeat (VHL) **1.x está obsoleta** y no se admite desde hace varios años.

## ¿Qué está sucediendo?

La biblioteca original de Video Heartbeat (VHL), cuyo nombre cambió posteriormente a Media SDK, proporcionaba seguimiento del lado del cliente para el análisis de audio y vídeo. Adobe ha trasladado las funcionalidades de seguimiento a implementaciones más nuevas y capaces:

* **Media SDK 3.x (solo Analytics):** Actualmente compatible. Rastrea medios mediante la API de recopilación de medios. Recomendado para usuarios de la versión 2.x que aún no pueden pasar a Edge Network.
* **Medios de transmisión para Edge Network (recomendado):** La implementación recomendada actualmente. Utiliza la API de Adobe Experience Platform Web SDK, Mobile SDK o Media Edge para enviar datos de medios a través de Edge Network, lo que permite su uso en Adobe Analytics, Customer Journey Analytics, Real-Time CDP y Adobe Journey Optimizer.

## ¿Qué se incluye al final de su vida útil y qué no?

**Fin de vida útil (ya no se admite):**

* Biblioteca de Video Heartbeat (VHL) 1.x: todas las plataformas (Android, iOS, JavaScript, Apple TV, Chromecast, Roku, TVML)
* Media SDK 2.x: Android, iOS, JavaScript

**No es el final de su vida útil (aún se admite):**

* Media SDK 3.x: JavaScript, Chromecast, Roku (solo Analytics)
* Streaming Media para Edge Network: todas las plataformas compatibles

## ¿Por qué se retiraron las versiones 1.x y 2.x?

A partir de la versión 3.0, Media SDK se rediseñó para utilizar directamente la API de recopilación de contenidos, lo que eliminaba la necesidad de un patrón delegado y simplificaba la creación del rastreador. Los SDK 1.x y 2.x antiguos dependían de una arquitectura de servidor de Heartbeat que se había sustituido.

Adobe también introdujo la implementación de Edge Network para proporcionar un único canal de recopilación de datos capaz de alimentar varias aplicaciones de Adobe descendentes, algo que los SDK de Heartbeat heredados no podían admitir.

## ¿Dónde puedo encontrar la documentación archivada?

La documentación heredada se ha archivado en GitHub y está disponible para consulta:

| Versión | Estado | Documentación archivada |
|---|---|---|
| 1.x (Biblioteca de Video Heartbeat) | Obsoleto | [`video-heartbeat` repositorio de GitHub](https://github.com/Adobe-Marketing-Cloud/video-heartbeat/tree/master/docs) |
| 2.x (Media SDK) | Fin del soporte: 31 de agosto de 2021 | [`media-sdks` repositorio de GitHub](https://github.com/Adobe-Marketing-Cloud/media-sdks/blob/master/docs/2.x/README.md) |

## ¿Cuáles son mis opciones de transición?

**Opción 1: migrar a Media SDK 3.x (solo Analytics)**

Si está en 2.x y utiliza Adobe Analytics exclusivamente, la migración a 3.x es la ruta más sencilla. Consulte la guía de migración de [2.x a 3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html) para obtener una comparación de API completa y ejemplos de código.

**Opción 2: migrar a medios de transmisión para Edge Network (recomendado)**

Para nuevas implementaciones o cuando desee utilizar datos en varias aplicaciones de Adobe, utilice Adobe Experience Platform Edge Network:

* [Media Edge Web SDK](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-web-sdk.html)
* [Media Edge Mobile SDK](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [API de Media Edge](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge-api.html)

## Preguntas frecuentes

+++**¿Se verá afectada la compatibilidad con los SDK de Roku y Chromecast?**

No. Los SDK de Roku y Chromecast siguen estando disponibles y son compatibles como parte de Media SDK 3.x (solo Analytics). Esta fecha de finalización de la vida útil solo abarca las versiones 1.x y 2.x.

+++

+++**¿Se verán afectadas las implementaciones de Media Analytics JavaScript SDK?**

No. Los clientes que utilicen JavaScript SDK para Media Analytics pueden seguir utilizando la extensión de SDK o la extensión de etiqueta independiente.

+++

+++**Todavía estoy en Media SDK 2.x. ¿Qué debo hacer?**

Adobe recomienda migrar a la implementación de Edge Network para todos los proyectos nuevos. Si necesita un paso intermedio, [Migre de JavaScript SDK 2.x a 3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html), y luego planifique su traslado a Edge Network.

+++

+++**¿Cuál es el nivel de esfuerzo para migrar a una implementación compatible?**

El esfuerzo de migración depende de la implementación de cada cliente y variará. Después de revisar la documentación de migración, póngase en contacto con el servicio de consultoría o atención al cliente para obtener soporte adicional:

* [Implementación de medios de streaming con Mobile Edge SDK, Android y iOS](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [Migración de JavaScript SDK 2.x a 3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html)

+++

+++**¿Debo usar Adobe Experience Platform Tags como sistema de administración de etiquetas?**

En implementaciones de aplicaciones móviles, Experience Platform Tags no se utiliza como sistema de administración de etiquetas como lo hace para la web. La interfaz de usuario de etiquetas es necesaria para configurar las extensiones de SDK. Esto es similar a cómo se utilizó la interfaz de usuario de Adobe Mobile Services para configurar la versión 4 de SDK móvil. Las etiquetas proporcionan instrucciones de instalación personalizadas en función de la extensión elegida.

+++

+++**¿Afecta este fin de soporte a SDK para tvOS?**

Sí. Para tvOS (versión 10 o posterior), la implementación recomendada es migrar a medios de streaming para Edge Network mediante Adobe Experience Platform Mobile SDK. Consulte [Implementar medios de transmisión mediante Edge SDK móvil](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html) para obtener más información.

+++

+++**¿Afecta este fin de soporte a SDK para Fire TV y Android TV?**

Sí. Para Fire TV y Android TV, la implementación recomendada es migrar a Streaming Media para Edge Network mediante Adobe Experience Platform Mobile SDK. Consulte [Implementar medios de transmisión mediante Edge SDK móvil](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html) para obtener más información.

+++

+++**¿Dónde puedo encontrar la información de fin de vida útil de Mobile v4 SDK?**

Consulte las [Preguntas frecuentes sobre la finalización de la vida útil de Mobile Services](mobile-services.md). La plataforma de Mobile Services y los SDK de Mobile v4 llegaron al final de su vida útil el 31 de diciembre de 2022.

+++

+++**¿Dónde puedo ir si tengo preguntas?**

Póngase en contacto con el equipo de su cuenta de Adobe o con el Servicio de atención al cliente de Adobe para obtener ayuda sobre la migración.

+++

>[!MORELIKETHIS]
>
>* [Descripción general de la implementación de medios de streaming](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/overview.html)
>* [Medios de streaming para Edge Network](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge.html)
>* [Configuración de Media SDK 3.x — JavaScript](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/web-implementation.html)
