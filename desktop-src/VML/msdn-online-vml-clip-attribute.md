---
title: VML 剪輯屬性
description: VML 剪輯屬性
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cab4afdef2a10c9c6f6a0561dedf5b4df3538a97152cb53181452b8ac531bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999288"
---
# <a name="vml-clip-attribute"></a>VML 剪輯屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷裁剪是否開啟。 讀取/寫入 **VgTriState**。

**適用於**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**標記語法**

<v： *element* clip = " *expression* " >

**指令碼語法**

*元素* 。剪輯 = "*expression*"

*運算式* =*元素*. 剪輯

**備註**

如果 **剪輯** 為 **False**，圖形將會縮放以符合框架。 若 **為 True**，將不會顯示框架外之圖形的任何部分。

請注意，除非 **剪輯** 為 **True**，否則不會使用 [原始](origin-attribute--vmlframe--vml.md)和 [大小](size-attribute--vmlframe.md)。

*VML 標準屬性*

**範例**

外部檔案中定義的映射將會被裁剪。


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 