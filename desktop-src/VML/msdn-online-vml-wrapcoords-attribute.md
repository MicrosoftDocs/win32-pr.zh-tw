---
title: VML WrapCoords 屬性
description: VML WrapCoords 屬性
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682523"
---
# <a name="vml-wrapcoords-attribute"></a>VML WrapCoords 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圍繞形狀的周框多邊形。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* o:wrapcoords = " *expression* " >

**備註**

描述以逗號分隔的 x 和 ycoordinates 清單;也就是「x1、y1、x2、y2、x3、y3,...」這是在文字與圖形緊密環繞時使用。 預設值為 **Null** (空) 字串，直到 **MSO 自動換行模式** 屬性設定為 [ **緊密型** ] 或 [ **到**] 為止。

*Microsoft Office Extensions 屬性*

**範例**

圖形具有文字環繞周框方塊，其為大於路徑的5個單位。


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 