---
title: 'Size 屬性 (VMLFrame) '
description: 'Size 屬性 (VMLFrame) '
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32d496bc40b5b84b7a8a16bf6b84a2926010d56dcc311659dd63300363a7067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754123"
---
# <a name="size-attribute-vmlframe"></a>Size 屬性 (VMLFrame) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義框架裁剪區域的大小。 讀取/寫入 **VgVector2D**。

**適用於**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**標記語法**

<v： *element* size = " *expression* " >

**指令碼語法**

*元素* 。 size = "*expression*"

*運算式* =*元素*。大小

**備註**

預設值為 0,0。 請注意，只有當 [剪輯](msdn-online-vml-clip-attribute.md)為 **True** 時，**大小** 才會運作。 在這個屬性中，大小會定義為框架的寬度和高度。

*VML 標準屬性*

**範例**

裁剪區域的大小將會是50pt，50pt。


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 