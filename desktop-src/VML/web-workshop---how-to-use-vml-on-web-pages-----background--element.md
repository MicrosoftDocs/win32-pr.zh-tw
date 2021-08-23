---
title: 使用 Background 元素
description: 使用 Background 元素
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- 網路研討會，背景元素
- 設計網頁、背景元素
- Vector Markup Language (VML) 、background 元素
- VML (Vector Markup Language) ，background 元素
- 向量圖形、背景元素
- background 元素
- VML 元素、背景
- VML 圖形、背景元素
- Vector Markup Language (VML) 自訂背景
- VML (Vector Markup Language) ，自訂背景
- 向量圖形，自訂背景
- VML 圖形，自訂背景
- 自訂背景
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb4a694aa5458a0eae01fcbf577f72da8b8f54b7efda506423565aee362ce2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512778"
---
# <a name="using-the-background-element"></a>使用 Background 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

在本主題中，我們將說明如何使用 VML 中提供的元素自訂網頁的背景 `<background>` 。

如您從[ `<fill>` 使用](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)主題中學到的，您可以將子專案放在 `<fill>` `<shape>` 、 `<shapetype>` 或任何預先定義的 shape 元素內，以描述如何填滿圖形。

同樣地，您可以將 `<fill>` 子項目放在元素內， `<background>` 以描述如何填滿網頁的背景。 然後，您可以使用子項目的屬性屬性 `<fill>` 來自訂填滿效果，例如漸層 [填滿](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)、 [圖樣填滿](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)或 [圖片填滿](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)。

例如，若要繪製漸層填滿的背景，您可以在網頁的區域中輸入下列幾行 `<BODY>` ：


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858389) 。

 

 