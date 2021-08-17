---
title: VML MiterLimit 屬性
description: VML MiterLimit 屬性
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef82ce7e8e0d3bf99fc532a9e746a94006a6bb9deba282ce8edd6ab91d41902
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308368"
---
# <a name="vml-miterlimit-attribute"></a>VML MiterLimit 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義斜接接點的平滑。 讀取/寫入 **VgNumber**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* miterlimit = " *expression* " >

**指令碼語法**

 miterlimit = "*expression*"

*運算式* =** miterlimit

**備註**

聯合的內部點和外部點之間的最大距離。 此數位是線條粗細的倍數。

預設值為 8。

*VML 標準屬性*

**範例**

聚合線條上的接點是一個限制為10的接點，也就是5倍的2點。


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 