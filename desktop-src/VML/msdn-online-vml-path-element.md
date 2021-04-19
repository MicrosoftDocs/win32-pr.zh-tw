---
title: VML Path 元素
description: VML Path 元素
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1de9440761479d6b3dc6cb10c96b00ea48626247
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967898"
---
# <a name="vml-path-element"></a>VML Path 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的路徑。

下列屬性會修改陰影。



| 屬性                                                        | 描述                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Arrowok](msdn-online-vml-arrowok-attribute.md)                 | 決定是否會顯示箭頭。                                |
| [ConnectAngles](msdn-online-vml-connectangles-attribute.md)     | 指定曲線將如何連接到連接點。                       |
| [ConnectLocs](msdn-online-vml-connectlocs-attribute.md)         | 定義路徑上連接點的位置。                            |
| [ConnectType](msdn-online-vml-connecttype-attribute.md)         | 定義用來將圖形附加至其他圖形的連接點類型。 |
| [ExtrusionOK](msdn-online-vml-extrusionok-attribute.md)         | 決定是否會顯示延伸。                              |
| [FillOK](msdn-online-vml-fillok-attribute.md)                   | 決定是否會顯示填滿。                                    |
| [GradientShapeOK](msdn-online-vml-gradientshapeok-attribute.md) | 決定是否會顯示漸層圖形。                          |
| [識別碼](id-attribute--path--vml.md)                                | 定義路徑的唯一識別碼。                                         |
| [豪華 轎車](msdn-online-vml-limo-attribute.md)                       | 定義路徑上的延展點。                                            |
| [ShadowOK](msdn-online-vml-shadowok-attribute.md)               | 決定是否會顯示陰影。                                  |
| [StrokeOK](msdn-online-vml-strokeok-attribute.md)               | 決定是否會顯示筆觸。                                  |
| [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)         | 定義圖形內的一或多個文字方塊。                                   |
| [TextPathOK](msdn-online-vml-textpathok-attribute.md)           | 決定是否會顯示 textpath。                                |
| [V](msdn-online-vml-v-attribute.md)                             | 定義組成路徑的命令。                                       |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

下列程式碼示範如何使用路徑定義圖形。


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



請注意， **path** 的 [V](msdn-online-vml-v-attribute.md)屬性會取代 [Shape](shape-element--vml.md)的 [path](msdn-online-vml-path-attribute.md)屬性。

**範例**

-   [簡單路徑子項目範例](/previous-versions/bb229545(v=vs.85))
-   [動態路徑子項目範例](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 