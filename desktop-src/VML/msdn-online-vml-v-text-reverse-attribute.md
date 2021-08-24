---
title: VML V-Text-Reverse 屬性
description: VML V-Text-Reverse 屬性
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f1535620c1fefe98ac23e2f842ef9a97e13b9cb39c65ec6b97f6f7d12b1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654618"
---
# <a name="vml-v-text-reverse-attribute"></a>VML V-Text-Reverse 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否反轉資料列的版面配置順序。 讀取/寫入 **VgTriState**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "v-text-reverse： *expression* " >

**指令碼語法**

*element* 。 v-text-reverse = "*expression*"

*運算式* =*元素*。 v-text-reverse

**備註**

若 **為 True**，則會反轉資料列的版面配置順序。 這個屬性是用於垂直文字版面配置。 預設值為 **[False]** 。

*VML 標準屬性*

**範例**

版面配置順序相反。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 