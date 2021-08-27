---
title: VML MSO-換行距離-底端屬性
description: VML MSO-換行距離-底端屬性
ms.assetid: b096fc67-dd99-4833-bb82-73de7b06f43c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e28ea0f2d84b9bf9f5981f9ebb22f15af75a2071f07dd9f3e006ac70b34256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007678"
---
# <a name="vml-mso-wrap-distance-bottom-attribute"></a>VML MSO-換行距離-底端屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義從圖形底部到換行文字的距離。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* style = "mso-wrap-下： *expression* " >

**備註**

請注意，這個屬性與 CSS **Margin** 屬性不同。 **邊界** 會變更圖形的原點以包含邊界區域，但 Microsoft Office 中的換行距離不會變更圖形的原點。

*Microsoft OfficeExtensions 屬性*

**範例**

圖形具有10點的底部換行距離。


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-bottom:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 