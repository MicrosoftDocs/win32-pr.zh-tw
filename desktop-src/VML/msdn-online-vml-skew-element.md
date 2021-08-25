---
title: VML 扭曲元素
description: VML 扭曲元素
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d659d16e6d10e9ec88875989a812de82403d2ac5b946580e7c7b7def956b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099038"
---
# <a name="vml-skew-element"></a>VML 扭曲元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的扭曲。

下列屬性會修改扭曲。



| 屬性                                 | 描述                                    |
|-------------------------------------------|------------------------------------------------|
| [內線](ext-attribute--skew--vml.md)       | 定義扭曲的顯示方式。           |
| [識別碼](id-attribute--skew--vml.md)         | 定義扭曲的唯一識別碼。        |
| [矩陣](matrix-attribute--skew--vml.md) | 定義扭曲的觀點轉換。    |
| [Offset](offset-attribute--skew--vml.md) | 定義扭曲的位移。                  |
| [開啟](on-attribute--skew--vml.md)         | 決定是否會顯示扭曲。 |
| [起源](origin-attribute--skew--vml.md) | 決定扭曲的原點。               |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

此外， [矩陣](matrix-attribute--skew--vml.md) 和 [On](on-attribute--skew--vml.md) 屬性必須設定為 **True**。

以下是產生扭曲所需的最少程式碼。


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



**扭曲** 元素是 VML 的 Microsoft Office 延伸模組。

**範例**

-   [簡單扭曲範例](/previous-versions/bb229482(v=vs.85))
-   [動態扭曲範例](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 