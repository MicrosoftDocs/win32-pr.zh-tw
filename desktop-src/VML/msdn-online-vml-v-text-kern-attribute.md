---
title: VML V 文字間距屬性
description: VML V 文字間距屬性
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933448"
---
# <a name="vml-v-text-kern-attribute"></a>VML V 文字間距屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否開啟字偶間距調整。 讀取/寫入 **VgTriState**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "v-text-字偶間距： *expression* " >

**指令碼語法**

 node.js-text-字偶間距 = "*expression*"

*運算式* =*元素*. 樣式。 v 文字間距

**備註**

若 **為 True**，則會開啟字偶間距。 預設值為 **False**。 字偶間距會移除特定字母組之間的空格，以彌補不平均的 letterforms。 例如，如果開啟字偶間距調整，則會移除大寫 "T" 和小寫 "i" 之間的額外空間。

*VML 標準屬性*

**範例**

已開啟字偶間距。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 