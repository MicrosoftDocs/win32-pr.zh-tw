---
title: VML PreferRelative 屬性
description: VML PreferRelative 屬性
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154297a528f18a3ac53f788ebbfe80ff59196f2872dd3dcb3789db16d5c91cb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654978"
---
# <a name="vml-preferrelative-attribute"></a>VML PreferRelative 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷在重新格式化之後是否儲存物件的原始大小。 讀取/寫入 **VgTriState**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* o:preferrelative = " *expression* " >

**備註**

預設值為 **False**。 若 **為 True**，將會儲存物件的原始大小，而且所有調整大小都會以該原始大小的百分比為基礎。 否則，每個調整大小都會將比例重設為100%。

*Microsoft OfficeExtensions 屬性*

**範例**

如果調整圖形的大小，則不會儲存原始的大小。


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 