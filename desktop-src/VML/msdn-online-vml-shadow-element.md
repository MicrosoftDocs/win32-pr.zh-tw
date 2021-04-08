---
title: VML 影子項目
description: VML 影子項目
ms.assetid: 3e7d3e8c-45f8-4db3-95f3-7d993b7c2ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd73bb7087c2736ba5bec75102ffcb4337407650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933278"
---
# <a name="vml-shadow-element"></a>VML 影子項目

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的陰影。

下列屬性會修改陰影。



| 屬性                                          | 描述                                        |
|----------------------------------------------------|----------------------------------------------------|
| [色彩](color-attribute--shadow--vml.md)          | 定義陰影的色彩。                     |
| [Color2](color2-attribute--shadow--vml.md)        | 定義陰影的第二個色彩。              |
| [識別碼](id-attribute--shadow--vml.md)                | 指定陰影的唯一識別碼。       |
| [矩陣](matrix-attribute--shadow--vml.md)        | 定義陰影的觀點轉換。     |
| [遮蔽](msdn-online-vml-obscured-attribute.md) | 判斷陰影是否透明。      |
| [Offset](offset-attribute--shadow--vml.md)        | 定義陰影延伸超過圖形的距離。 |
| [Offset2](msdn-online-vml-offset2-attribute.md)   | 定義第二個位移。                           |
| [開啟](on-attribute--shadow--vml.md)                | 決定是否要顯示陰影。          |
| [不透明度](opacity-attribute--shadow--vml.md)      | 決定陰影的透明度。           |
| [起源](origin-attribute--shadow--vml.md)        | 定義陰影的中心。                  |
| [型別](type-attribute--shadow--vml.md)            | 指定陰影的類型。                      |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

此外， [On](on-attribute--shadow--vml.md) 屬性必須設定為 **True**。

以下是產生陰影所需的最少程式碼。


```HTML
   <v:rect
   fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True"/>
   </v:rect>
```



除非您增加 [位移](offset-attribute--shadow--vml.md) 值，否則您可能不會注意到陰影，因為預設位移是2pt，2pt。

**範例**

-   [簡單陰影範例](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/t_shadow.md)
-   [動態陰影範例](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/x_shadow.md)

 

 