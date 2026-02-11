---
title: Prueba oculta
description: Esta es una prueba oculta
hide: true
hidefromtoc: true
landing-page-breadcrumb-title: Test AEM 6.5
landing-page-name: experience-manager-65
feature: Annotations
hold: true
exl-id: e6e5ba1c-98a5-4d7d-9913-426df31bc7a3
source-git-commit: f3cf599787da4d3d1b9b77bd6207fea46c732dd7
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 6%

---

# Prueba oculta

4 de febrero de 2026 - `hold: true` es el.
Probando clave nueva

11 de febrero: Prueba en espera.

Esta es una prueba oculta. Estoy agregando este(a) `[` para asegurarme de que funcione correctamente en el procesamiento v2.

## Abrir en una pestaña nueva {#section_92882928}

`[See What's new](auditor.md){target="_blank"} `

[Abrir en la misma pestaña](auditor.md)

[Nueva ficha con espacio entre comillas](auditor.md){target="_blank"} 

[Nueva pestaña con delimitador](auditor.md){target=_blank}

[Nueva ficha sin espacio con comillas](auditor.md){target="_blank"}

[Nueva ficha con espacio sin comillas](auditor.md){target=_blank} 

[Nueva ficha sin espacio sin comillas](auditor.md){target=_blank}

[Nueva pestaña con vínculo profundo](commerce-channels.md#channel-manager-extension){target="_blank"}

[Anclar nueva ficha con vínculo profundo](https://experienceleague.adobe.com/es/docs/analytics/analyze/home#key-analytics-resources){target="_blank"}

[Nueva pestaña con vínculo externo](https://www.adobe.com){target="_blank"}

[Nuevo vínculo raíz de ficha](/help/guide-1/auditor.md){target="_blank"}


<table>
  <tr>
    <th>Con comillas</a></th>
    <th>Sin comillas</th>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com" target="_blank">Nueva pestaña de Adobe</a></td>
    <td><a href="https://www.adobe.com" target="_blank">Nueva pestaña de Adobe</td>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com">Adobe en ficha nueva</a></td>
    <td><a href="https://www.adobe.com">Adobe en ficha nueva</td>
  </tr>
</table>

## Prueba de comentario

18 de noviembre de 2025

<!-- ## Comment with basic text

This is a new line.

Second new line. -->


Comentario a continuación. Si esto es lo último que ve en este artículo, se debe a la sintaxis del comentario.

1. Haga clic en **[!UICONTROL Crear]**.

<!-- ## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. -->

Esta línea va después del comentario.

## Prueba de vídeo

### Vídeo sin formato sin transcripción: debe mostrar la transcripción porque metadata.md se filtran hacia abajo

>[!VIDEO](https://video.tv.adobe.com/v/3409657?captions=spa&hidetitle=true)

### Con la transcripción establecida en verdadera

>[!VIDEO](https://video.tv.adobe.com/v/3409657?captions=spa&hidetitle=true){transcript=true}

### Con la transcripción configurada como falsa: la transcripción de vídeo no debe mostrarse

>[!VIDEO](https://video.tv.adobe.com/v/3409657?captions=spa&hidetitle=true){transcript=false}

## Vínculos relativos

* [Información general](overview.md)
* [Buscar y promocionar](search-promote.md)
* [Social](social.md)

## Vínculo profundo explícito

[información general adicional (raíz)](/help/guide-1/overview.md#additional-products)

[información general adicional](overview.md#additional-products)

## Prueba de texto de desplazamiento {#this-is-a-heading-anchor}

Sin texto de desplazamiento

```
![alt text](assets/maui-flip.jpg)
```

![texto alternativo](assets/maui-flip.jpg)


Sí, pasar el texto

```
![alt text](assets/maui-flip.jpg "Hover text")
```

![texto alternativo](assets/maui-flip.jpg "Texto de desplazamiento")

## Diapositiva

Sintaxis:

```
>[!SLIDE](analyze-project)
https://experienceleague-stage.adobe.com/en/slides/analyze-project
```

Procesado:

<!--
>[!SLIDE](analyze-project)
-->

Bob: elimine el comentario de la diapositiva una vez que pruebe el tema loc.
