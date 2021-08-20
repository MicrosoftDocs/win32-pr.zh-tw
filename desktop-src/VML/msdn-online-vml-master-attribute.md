---
title: VML Master 屬性
description: VML Master 屬性
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d126b9d02144bbc8831d7be9e73a3e5896c2ceccca71cfcbc8161d5ccc8112f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999108"
---
# <a name="vml-master-attribute"></a>VML Master 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷 **ShapeType** 元素是否為主要元素。 讀取/寫入 **VgTriState**。

**適用於**

[ShapeType](msdn-online-vml-shapetype-element.md)

**標記語法**

<v： *element* o:master = " *expression* " >

**備註**

若 **為 True**，表示 **ShapeType** 圖形是由轉譯引擎轉譯。 預設值為 **[False]** 。

*Microsoft OfficeExtensions 屬性*

**範例**

**ShapeType** 元素是主要圖形。


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 