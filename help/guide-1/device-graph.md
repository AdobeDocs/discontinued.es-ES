---
keywords: Device-graph;fin de vida útil
title: Gráfico del dispositivo
description: Obtenga información acerca de los planes de fin de vida útil para el gráfico de dispositivos.
source-git-commit: d014c200dd926ccf0116faa50c4bffb1d234e926
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 4%

---

# Fin de la vida útil del gráfico de dispositivos

>[!WARNING]
>
>El gráfico de dispositivos de Cross-Device Analytics ya no está disponible a partir del **31 de diciembre de 2025**. Cambie cualquier grupo de informes virtuales habilitado para gráficos de dispositivos actuales al [método basado en campos](https://experienceleague.adobe.com/en/docs/analytics/components/cda/field-based-stitching).

El análisis entre dispositivos utilizó el gráfico privado para unir datos. Private Graph es un repositorio de ID de dispositivos con hash específicos de su organización. CDA se comunica regularmente con el gráfico del dispositivo para vincular dispositivos.

## Requisitos previos específicos del gráfico del dispositivo

Si tenía intención de implementar el análisis entre dispositivos mediante el método del gráfico del dispositivo, era necesario lo siguiente.

>[!WARNING]
>
>Si no se cumplen todos los requisitos previos, es posible que no se pueda habilitar el análisis entre dispositivos o que se obtengan resultados deficientes al vincular datos.

* Su organización debe utilizar [Adobe Experience Platform Identity Service Private Graph](https://business.adobe.com/products/experience-platform/identity-service.html). Consulte también la [Página principal](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html) en la guía del usuario del servicio de identidad.
* La implementación debe utilizar la versión más reciente del servicio de ID (ECID). Consulte la [Página de inicio](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=es) en la guía del usuario del servicio de ID. Es probable que la mayoría de las implementaciones que usan [Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=es) en Adobe Experience Platform ya hayan implementado el servicio de ID.
* Su implementación debe llamar a la función `setCustomerIDs` (o SDK equivalente) cada vez que se pueda identificar a un individuo, como cuando un usuario inicia sesión o abre un correo electrónico. Este requisito se aplica a todas las plataformas, incluidas las aplicaciones móviles, si se utilizan. Consulte [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html) en la guía de usuario del servicio de ID.

## Limitaciones específicas del gráfico del dispositivo

* No se admiten los ID de Analytics heredados. Solo se vinculan los visitantes con ECID.
* Si su organización utiliza un gráfico privado, los nuevos dispositivos tardan hasta 24 horas en vincularse.
* Los gráficos de dispositivos de terceros no son compatibles.

