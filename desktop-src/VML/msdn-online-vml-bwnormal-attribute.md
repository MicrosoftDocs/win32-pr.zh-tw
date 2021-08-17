---
title: VML BWNormal 屬性
description: VML BWNormal 屬性
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2811a9cd734e0f2ca6ca2f707b6313d7434ac756a1f9cd8982d7179c75748bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754953"
---
# <a name="vml-bwnormal-attribute"></a>VML BWNormal 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義一般黑色和白色輸出裝置的黑色和白色模式。 讀取/寫入 [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* o:bwnormal = " *expression* " >

**備註**

當 [BWMode](msdn-online-vml-bwmode-attribute.md) 設定為 **auto** 時，這個屬性會用來決定如何以一般黑色和白色呈現圖形。

如需此屬性值的詳細資訊，請參閱 [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) 主題。 預設值是 **auto**。

*Microsoft OfficeExtensions 屬性*

**範例**

圖形會處理為一般黑色和白色輸出的灰階影像。


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 