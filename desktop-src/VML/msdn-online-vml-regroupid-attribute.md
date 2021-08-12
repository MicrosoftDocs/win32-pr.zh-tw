---
title: VML ReGroupID 屬性
description: VML ReGroupID 屬性
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c304bb0ecbe19c62e6fa5a204749b61fad4a700fe4222b6e1ef993384d53abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597641"
---
# <a name="vml-regroupid-attribute"></a>VML ReGroupID 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的上一個群組。 讀取/寫入 **VgInteger**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* o:regroupid = " *expression* " >

**備註**

識別碼是用來識別已不再分組之圖形的群組。 允許以程式設計方式 regrouped 圖形。

*Microsoft OfficeExtensions 屬性*

**範例**

圖形是群組識別碼040754所表示之群組的一部分。


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 