---
title: VML BWMode 屬性
description: VML BWMode 屬性
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682606"
---
# <a name="vml-bwmode-attribute"></a>VML BWMode 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定如何針對黑白輸出裝置呈現圖形。 讀取/寫入 [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* o:bwmode = " *expression* " >

**備註**

當圖形列印在黑色和白色印表機上，或是在應用程式中以黑白視圖顯示時，可能會有數個選項。 如需此屬性值的詳細資訊，請參閱 [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) 主題。 預設值是 **auto**。

如果指定 **auto** ，則會使用 [BWNormal](msdn-online-vml-bwnormal-attribute.md) 來判斷一般黑白輸出的行為，並使用 [BWPure](msdn-online-vml-bwpure-attribute.md) 來判斷純黑色和白色輸出的行為。

*Microsoft Office Extensions 屬性*

**範例**

圖形的黑色和白色模式是 [ **自動**]。


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 