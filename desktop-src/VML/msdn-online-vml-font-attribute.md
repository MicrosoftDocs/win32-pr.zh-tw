---
title: VML 字型屬性
description: VML 字型屬性
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074aa0672002dcbbac55d21ed27383d5a3fd6e3b9ccfe9125ad89c2c43ac71ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986658"
---
# <a name="vml-font-attribute"></a>VML 字型屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

指定字型屬性的複合值。 讀取/寫入 **字串**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "font-size： *expression* " >

**指令碼語法**

style *. font-family* = "*expression*"

*運算式* =*element*。字型

**備註**

定義字型的屬性，包括系列、樣式、粗細、大小和變異數。 字串中的定義順序為： **字型樣式**、 **字型變異**、 **字型粗細**、 **字型大小**、 **線條高度** 和 **字型系列**。 這些值與標準 HTML 樣式屬性相同。

*VML 標準屬性*

**範例**

Textpath 文字的字型為斜體、小型大寫字母、粗體、36點 Arial。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 