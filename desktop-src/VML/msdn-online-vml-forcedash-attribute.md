---
title: VML ForceDash 屬性
description: VML ForceDash 屬性
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e162f95c4760c8a499f690c600fd651259694bae5c7fcc81ed2b2ee0d65bcb09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119396060"
---
# <a name="vml-forcedash-attribute"></a>VML ForceDash 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定當圖形沒有線條或填滿時，是否使用虛線輪廓繪製圖形。 讀取/寫入 **VgTriState**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* o:forcedash = " *expression* " >

**備註**

當圖形沒有線條且沒有填滿時，Microsoft PowerPoint 預留位置用來繪製虛線外框。 預設值為 **False**。 若 **為 True**，則會使用虛線外框來表示預留位置。

*Microsoft OfficeExtensions 屬性*

**範例**

如果沒有線條或填滿，則會使用虛線來呈現圖形。


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 