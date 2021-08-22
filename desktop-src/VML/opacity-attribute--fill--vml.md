---
title: '不透明度屬性 (填滿)  (的 VML) '
description: '不透明度屬性 (填滿)  (的 VML) '
ms.assetid: abd2fe4d-6391-4413-80f0-549bcc74f42e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ea4f539eb2386dae7b8e863c95556cf70400c320ee515897cf7f96a85fe3ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057596"
---
# <a name="opacity-attribute-fillvml"></a>不透明度屬性 (填滿)  (的 VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義填滿的透明度。 讀取/寫入 [VgFraction](msdn-online-vml-vgfraction-data-type.md)。

**適用於**

[填滿](msdn-online-vml-fill-element.md)

**標記語法**

<v： *element* opacity = " *expression* " >

**指令碼語法**

*元素* 。不透明度 = "*expression*"

*運算式* =*元素*。不透明度

**備註**

預設值為 1.0。

*VML 標準屬性*

**範例**

圖形填滿會是50% 的透明。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill opacity="50%" color="red"/>
   </v:shape>
```



 

 