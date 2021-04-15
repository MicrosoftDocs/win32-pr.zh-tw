---
title: 'Src 屬性 (填滿)  (的 VML) '
description: 'Src 屬性 (填滿)  (的 VML) '
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463185"
---
# <a name="src-attribute-fillvml"></a>Src 屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義要載入填滿的影像。 讀取/寫入 **字串**。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* src = " *expression* " >

**指令碼語法**

*element* 。 src = "*expression * * *"**

*運算式* =*元素* src

**備註**

影像的 URL，以載入影像和模式填滿。 這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。 如果這個屬性單獨出現 (也就是沒有 **HRef** 或 **Title** 屬性) ，則會連結影像。

*VML 標準屬性*

**範例**

使用檔案 myimage.gif 作為來源的磚影像隨即顯示。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 