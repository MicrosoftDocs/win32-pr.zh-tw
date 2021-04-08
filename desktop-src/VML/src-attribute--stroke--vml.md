---
title: 'Src 屬性 (筆觸)  (VML) '
description: 'Src 屬性 (筆觸)  (VML) '
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682418"
---
# <a name="src-attribute-strokevml"></a>Src 屬性 (筆觸)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義要為筆觸填滿載入的來源影像。 讀取/寫入 **字串**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* src = " *expression* " >

**指令碼語法**

 src = "*expression*"

*運算式* =*元素* src

**備註**

影像的 URL，以載入影像和模式填滿。 這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。 如果這個屬性單獨出現，亦即沒有 **HRef** 或 **標題**，則會連結影像。

*VML 標準屬性*

**範例**

使用 cylinder.gif 檔案所指定的影像來建立筆觸。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 