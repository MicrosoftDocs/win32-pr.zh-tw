---
title: VML 專案符號屬性
description: VML 專案符號屬性
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f35fda917931567dcd2dc4cf823ed74e3b449e05fba6046f1390e3d6454fd45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755017"
---
# <a name="vml-bullet-attribute"></a>VML 專案符號屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定圖形是否為圖形化專案符號。 讀取/寫入 **VgTriState**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* o:bullet = " *expression* " >

**備註**

預設值為 **False**。 若 **為 True**，則圖形為圖形化專案符號。

*Microsoft OfficeExtensions 屬性*

**範例**

圖形是一個專案符號。


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 