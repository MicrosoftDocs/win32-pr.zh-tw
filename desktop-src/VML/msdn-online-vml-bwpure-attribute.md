---
title: VML BWPure 屬性
description: VML BWPure 屬性
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842444"
---
# <a name="vml-bwpure-attribute"></a>VML BWPure 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義純黑色和白色輸出裝置的黑色和白色模式。 讀取/寫入 [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md)。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* o:bwpure = " *expression* " >

**備註**

當 [BWMode](msdn-online-vml-bwmode-attribute.md) 設定為 **auto** 時，這個屬性會用來判斷如何以純黑色和白色呈現圖形。

如需此屬性值的詳細資訊，請參閱 [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) 主題。 預設值是 **auto**。

*Microsoft Office Extensions 屬性*

**範例**

圖形會作為純黑色和白色輸出的高對比影像來處理。


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 