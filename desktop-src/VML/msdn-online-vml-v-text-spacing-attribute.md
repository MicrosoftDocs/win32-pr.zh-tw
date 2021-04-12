---
title: VML V 文字間距屬性
description: VML V 文字間距屬性
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376016"
---
# <a name="vml-v-text-spacing-attribute"></a>VML V 文字間距屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義文字的間距量。 讀取/寫入 **VgNumber**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "v-text-間距： *expression* " >

**指令碼語法**

*元素* . style。 v-text-間距 = "*expression*"

*運算式* =*元素*. style. v-文字間距

**備註**

預設值是 100。 如需文字間距的詳細資訊，請參閱 [V 文字間距模式](msdn-online-vml-v-text-spacing-mode-attribute.md) 屬性。

*VML 標準屬性*

**範例**

每個字母的字母間距會由200單位加強。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 