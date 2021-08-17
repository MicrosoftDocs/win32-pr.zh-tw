---
title: VML V 文字對齊屬性
description: VML V 文字對齊屬性
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bf8ec2e781b04e7ababc0b30ea3996e569e5cf9066a4bac072806fd7329eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117939127"
---
# <a name="vml-v-text-align-attribute"></a>VML V 文字對齊屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義文字的對齊方式。 讀取/寫入 **字串**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "v-text align： *expression* " >

**指令碼語法**

*element* 。 v-text-align = "*expression*"

*運算式* =*元素*。 v-文字對齊

**備註**

數值包括：

-   **左方** (預設) 
-   **對**
-   **中心**
-   **證明**
-   **字母-調整**
-   **延展-調整**

*VML 標準屬性*

**範例**

系統會將文字縮小以符合路徑，但是會在每個字母之間放置額外的空間。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 