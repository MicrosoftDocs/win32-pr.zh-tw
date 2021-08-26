---
title: VML FitShape 屬性
description: VML FitShape 屬性
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0adbb6fd92f296156cf2f95cf2b714cfacd2f193f8e1e1b912e6637b9e8d5cd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099248"
---
# <a name="vml-fitshape-attribute"></a>VML FitShape 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義文字是否適合圖形的周框方塊。 讀取/寫入 **VgTriState**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* fitshape = " *expression* " >

**指令碼語法**

 fitshape = "*expression*"

*運算式* =** fitshape

**備註**

若 **為 True**，則會將文字向外延伸至定義整個圖形的方塊邊緣。 預設值為 **False**。

*VML 標準屬性*

**範例**

文字會伸展以符合圖形。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 