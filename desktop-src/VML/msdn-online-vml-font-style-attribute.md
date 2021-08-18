---
title: VML Font-Style 屬性
description: VML Font-Style 屬性
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4571f9805b3a12f1c3c7b340780d0f3d9f6ce8644c2ec501e8c93aa58d378de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057856"
---
# <a name="vml-font-style-attribute"></a>VML Font-Style 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義字型的斜線量。 讀取/寫入 **字串**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "字型樣式： *運算式* " >

**指令碼語法**

 fontstyle = "*expression*"

*運算式* =** fontstyle

**備註**

值如下：

-   一般 (預設) 
-   斜
-   斜體

大部分的瀏覽器會以斜體呈現傾斜。 這些值與標準 HTML 樣式屬性相同。

*VML 標準屬性*

**範例**

字型為斜體 (傾斜) 。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 