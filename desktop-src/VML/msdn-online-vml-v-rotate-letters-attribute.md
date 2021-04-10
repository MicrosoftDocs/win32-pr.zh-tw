---
title: VML V-旋轉字母屬性
description: VML V-旋轉字母屬性
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092766"
---
# <a name="vml-v-rotate-letters-attribute"></a>VML V-旋轉字母屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否旋轉文字的字母。 讀取/寫入 **VgTriState**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "v-旋轉字母： *expression* " >

**指令碼語法**

*： v* -旋轉字母 = "*expression*"

*運算式* =*： v*-旋轉字母

**備註**

若 **為 True**，則文字的字母會旋轉90度。 預設值為 **[False]** 。

*VML 標準屬性*

**範例**

字母會旋轉90度。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 