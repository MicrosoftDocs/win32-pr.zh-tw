---
title: '在屬性 (填滿)  (的 VML) '
description: '在屬性 (填滿)  (的 VML) '
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee692bf1beb8c9a7c79b50ef8be3c115deea615f18ee6702d0817d4f81439555
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680638"
---
# <a name="on-attribute-fillvml"></a>在屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否會顯示填滿。 讀取/寫入 **VgTriState**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* on = " *expression* " >

**指令碼語法**

*element* . on = "*expression*"

*運算式* =*元素*。開啟

**備註**

如果 **為 False**，則不會顯示填滿。 預設值為 **True**。

*VML 標準屬性*

**範例**

雖然填滿定義為紅色，但不會顯示。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 