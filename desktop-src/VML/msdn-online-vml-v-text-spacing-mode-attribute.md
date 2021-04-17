---
title: VML V-文字間距模式屬性
description: VML V-文字間距模式屬性
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463672"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>VML V-文字間距模式屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義字母間距的模式。 讀取/寫入 **字串**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "v-text-間距-mode： *expression* " >

**指令碼語法**

 node.js-文字間距-模式 = "*expression*"

*運算式* =*元素*. 樣式。 v-文字間距-模式

**備註**

值包括

-   **(預設**) 
-   **跟蹤**

這個屬性會決定是否要在每個字母之間移除空間 (將) ，或在每個字母 (追蹤) 之間新增空間。 字母間距變更的數量是由 [V 文字間距](msdn-online-vml-v-text-spacing-attribute.md) 屬性所定義。

*VML 標準屬性*

**範例**

每個字母的字母間距會增加200單位。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 