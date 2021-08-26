---
title: VML 灰階屬性
description: VML 灰階屬性
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683371e2441ffa93f96dc8f727e4eed293954b1897267db8848aa39ffa497af8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099208"
---
# <a name="vml-grayscale-attribute"></a>VML 灰階屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷圖片是否會以灰階模式顯示。 讀取/寫入 **VgTriState**。

**適用於**

[ImageData](msdn-online-vml-imagedata-element.md)

**標記語法**

<v： *element* 灰階 = " *expression* " >

**指令碼語法**

*元素* 。灰階 = "*expression*"

*運算式* =*元素*. 灰階

**備註**

若 **為 True**，則圖片會以灰階顯示，而不是以色彩顯示。 預設值為 **False**。

此值是根據 CCIR 建議709，其偏好較高的綠色權數，並為自然色彩產生更滿意的結果。

*VML 標準屬性*

**範例**

影像會以灰階顯示，而不是以色彩顯示。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 