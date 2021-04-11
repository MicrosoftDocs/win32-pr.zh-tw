---
title: VML OnEd 屬性
description: VML OnEd 屬性
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316291"
---
# <a name="vml-oned-attribute"></a>VML OnEd 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷是否隱藏形狀的額外控點。 讀取/寫入 **VgTriState**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* o:oned = " *expression* " >

**備註**

隱藏左上角和右下角以外的所有圖形控點;亦即，用於直線線段的相同控制碼。 預設值為 **False**。

*Microsoft Office Extensions 屬性*

**範例**

圖形的左上角和下右控點都是隱藏的。


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 