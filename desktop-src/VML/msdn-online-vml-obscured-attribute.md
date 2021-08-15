---
title: VML 遮蔽屬性
description: VML 遮蔽屬性
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9122b3a9828fde816684cb20035949628ef25e38d06fb188d8271f0d5384f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308278"
---
# <a name="vml-obscured-attribute"></a>VML 遮蔽屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

判斷陰影是否透明。 讀取/寫入 **VgTriState**。

**適用於**

[Shadow](msdn-online-vml-shadow-element.md)

**標記語法**

<v： *element* 遮蔽 = " *expression* " >

**指令碼語法**

*元素* 。遮蔽 = "*expression*"

*運算式* =*元素*。遮蔽

**備註**

若 **為 True**，可讓您在圖形沒有填滿時，透過陰影查看。 預設值為 **False**。

*VML 標準屬性*

**範例**

背景會透過陰影顯示。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 