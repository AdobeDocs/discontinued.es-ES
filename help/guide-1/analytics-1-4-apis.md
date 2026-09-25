---
title: Fin de vida útil de la API de Adobe Analytics 1.4
description: La API de Adobe Analytics 1.4 y la autenticación WSSE llegaron al final de su vida útil el 31 de agosto de 2026. Descubra qué se ve afectado y cómo migrar a las API de Analytics 2.0.
source-git-commit: 4056ba0953e81a279d25b15449c7b41a4a5eb7f9
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%
---
# Fin de vida útil de la API de Adobe Analytics 1.4

A partir del **31 de agosto de 2026**, Adobe ha retirado la API de Adobe Analytics 1.4 y la autenticación WSSE. Ya no se puede acceder a todos los extremos que utilizan esta versión de la API y las integraciones creadas en ella han dejado de funcionar.

Las API de Adobe Analytics 1.4 proporcionan una amplia gama de acciones, como la creación de informes, clasificaciones, fuentes de datos, segmentos, métricas calculadas, fuentes de datos y configuración de grupos de informes. Se han reemplazado por las [API de Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0), que le permiten realizar casi cualquier acción disponible en la interfaz de usuario de Adobe Analytics, incluidos informes y administración de componentes como segmentos y métricas calculadas. Si tiene una integración que aún debe actualizarse, siga la guía de [Migración a las API de Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration).

## Qué llegó al final de su vida útil

Esta finalización de la vida útil afecta directamente a las siguientes capacidades de la API 1.4. Migre cada flujo de trabajo afectado a las [API de Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0):

* Creación de informes (incluidos los informes de Data Warehouse, en tiempo real, de rutas y de resumen)
* Configuración y administración de grupos de informes
* Clasificaciones
* Segmentos
* Métricas calculadas
* Fuentes de datos
* Fuentes de datos
* Métodos de marcadores y compañía (extremo)

También retira la **autenticación WSSE de Adobe Analytics** (consulte la [autenticación WSSE](#wsse-authentication) a continuación).

>[!IMPORTANT]
>
>Esta fecha de finalización de la vida útil *no* afecta la recopilación de datos. Las soluciones de etiquetado como Etiquetas (anteriormente Adobe Launch), Web SDK y AppMeasurement no se ven afectadas. La [API de inserción de datos](#data-insertion-api) también está *no* retirada. Sin embargo, si utiliza las API de fuentes de datos o clasificaciones 1.4 para mejorar los datos, debe migrar esos flujos de trabajo a las API de Adobe Analytics 2.0.

## Autenticación WSSE

La autenticación WSSE es un protocolo de autenticación heredado compatible con las API de Analytics 1.4. Se ha reemplazado por las opciones de autenticación basadas en OAuth que se proporcionan en [Adobe Developer Console](https://developer.adobe.com/console/home). Los proyectos que utilizaron la autenticación WSSE deben actualizar sus credenciales a las proporcionadas en Adobe Developer Console.

Para migrar, inicia sesión en [Adobe Developer Console](https://developer.adobe.com/console/home) y crea un proyecto para tu integración de la API de Analytics 2.0. Seleccione el método de autenticación **OAuth User** o **OAuth Server-to-Server**.

## API de inserción de datos

La API de inserción de datos es **no** parte de este fin de vida útil. Su documentación se movió al sitio [API de recopilación de datos de Adobe Analytics](https://developer.adobe.com/analytics-collection-apis/), junto con otros métodos de recopilación del lado del servidor:

* [API de inserción de datos](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/): envíe datos de evento de una visita en una, como una cadena de consulta (solicitud de imagen) o un XML `POST`.
* [API de inserción de datos en lotes](https://developer.adobe.com/analytics-collection-apis/methods/bulk-data-insertion/): Cargue lotes de datos de llamadas al servidor como archivos. Adobe recomienda utilizar la API de inserción masiva de datos para las nuevas implementaciones del lado del servidor.

## Preguntas frecuentes

+++¿Afecta esto a mis proyectos existentes de Adobe Developer para las API de Analytics?

Cualquier proyecto existente que utilice las API de Analytics 1.4 se verá afectado. Estas integraciones deben migrarse a las [API de Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0/).

+++

+++He compartido mis credenciales de Adobe con otro producto o aplicación que usa las API de Analytics. ¿Se ven afectados?

Si ese producto o aplicación utiliza sus credenciales de WSSE o llama a las API de Analytics 1.4, se verá afectado y deberá migrar. Póngase en contacto con el proveedor de productos o aplicaciones para obtener más información sobre sus planes de migración y plazos.

+++

+++¿Cómo puedo determinar qué API utiliza mi proyecto?

La dirección URL base a la que llama el proyecto determina qué versión de API utiliza. Las API de Adobe Analytics 1.4 utilizaban las siguientes direcciones URL base:

* `https://api.omniture.com`
* `https://api3.omniture.com`
* `https://api4.omniture.com`
* `https://api5.omniture.com`

Las [API de Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0/) utilizan la siguiente URL base:

* `https://analytics.adobe.io`

Si alguno de sus proyectos de API llama a `api*.omniture.com`, utilizará las API retiradas de Adobe Analytics 1.4 y deberá migrar a las API 2.0.

+++

+++¿Afecta este fin de vida útil a la recopilación de datos?

No. Esta fecha de finalización de la vida útil **no** afecta la recopilación directa de datos, como las etiquetas, el SDK web, AppMeasurement o la API de inserción de datos. Sin embargo, si utiliza las API de fuentes de datos o clasificaciones 1.4 para mejorar los datos, debe migrar esos flujos de trabajo a las API de Adobe Analytics 2.0.

+++

Si tiene más preguntas acerca de esta fecha de finalización de la vida útil que no ha respondido en esta página, póngase en contacto con el equipo de cuenta de Adobe.
