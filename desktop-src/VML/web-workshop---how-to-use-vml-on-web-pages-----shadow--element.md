---
title: 使用 Shadow 元素
description: 使用 Shadow 元素
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- 網路研討會，影子項目
- 設計網頁，shadow 元素
- Vector Markup Language (VML) 、shadow 元素
- VML (Vector Markup Language) 、shadow 元素
- 向量圖形、陰影元素
- shadow 元素
- VML 元素，陰影
- VML 圖形，shadow 元素
- Vector Markup Language (VML) ，以陰影效果繪製
- VML (Vector Markup Language) ，以陰影效果繪製
- 向量圖形，具有陰影效果的繪圖
- VML 圖形，具有陰影效果的繪圖
- 具有陰影效果的繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83be3f59eacfb495a2c80d212bc99cfd3d43be10aa8144eb68d3defd8a029e41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512591"
---
# <a name="using-the-shadow-element"></a>使用 Shadow 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

在本主題中，我們將說明如何使用 `<shadow>` 子項目繪製具有各種陰影效果的圖形。

您可以將子專案放在 `<shadow>` `<shape>` 、 `<shapetype>` 或任何預先定義的 shape 元素內，以繪製具有陰影的圖形。 然後，您可以使用子項目的屬性屬性 `<shadow>` 來自訂陰影。

例如，若要建立具有陰影的圖形（如下圖所示），您可以在網頁的區域中輸入下列幾行 `<BODY>` ：

![shape1.gif (887 個位元組) ](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   `on="t"` 並 `type="perspective"` 指出使用透檢視類型來開啟陰影。
-   [ **來源** ] 和 [ **位移** ] 會指出要在哪裡繪製陰影。
-   `matrix="..."` 指定透視圖的轉換矩陣。

如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858396) 。

 

 