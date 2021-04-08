---
title: VML V 相同的字母高度屬性
description: VML V 相同的字母高度屬性
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682473"
---
# <a name="vml-v-same-letter-heights-attribute"></a>VML V 相同的字母高度屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷是否所有字母都會具有相同的高度，而不論初始案例為何。 讀取/寫入 **VgTriState**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "v-相同的字母高度： *expression* " >

**指令碼語法**

 node.js-相同的字母-高度 = "*expression*"

*運算式* =** node.js-相同的字母高度

**備註**

若 **為 True**，則小寫字母會延伸至大寫字母的高度。 預設值為 **[False]** 。

*VML 標準屬性*

**範例**

所有字母都會是相同的高度，而不會有任何大小寫。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 