---
title: VML DoubleClickNotify 屬性
description: VML DoubleClickNotify 屬性
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315235"
---
# <a name="vml-doubleclicknotify-attribute"></a>VML DoubleClickNotify 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

按兩下圖形時傳送事件訊息。 讀取/寫入 **VgTriState**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* o:doubleclicknotify = " *expression* " >

**備註**

預設值為 **False**，表示不會引發事件。

*Microsoft Office Extensions 屬性*

**範例**

按兩下時，圖形將會觸發按兩下事件。


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 