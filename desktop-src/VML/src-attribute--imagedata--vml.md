---
title: 'Src 屬性 (ImageData)  (VML) '
description: 'Src 屬性 (ImageData)  (VML) '
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023539"
---
# <a name="src-attribute-imagedatavml"></a>Src 屬性 (ImageData)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義影像的來源。 讀取/寫入 **字串**。

**適用於**

[ImageData](msdn-online-vml-imagedata-element.md)

**標記語法**

<v： *element* src = " *expression* " >

**指令碼語法**

 src = "*expression*"

*運算式* =*元素* src

**備註**

此屬性一律必須與 [ImageData](msdn-online-vml-imagedata-element.md) 專案搭配使用，並指向有效的影像資料，才能顯示圖片。 如果出現沒有 [HRef](https://www.bing.com/search?q=HRef) 或 [Title](title-attribute--imagedata--vml.md)的屬性，則會連結影像。

*VML 標準屬性*

**範例**

影像的來源是名為 "kids.jpg" 的檔案。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 