---
title: VML ArrowOK 屬性
description: VML ArrowOK 屬性
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375772"
---
# <a name="vml-arrowok-attribute"></a>VML ArrowOK 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否會顯示箭頭。 讀取/寫入 **VgTriState**。

**適用於**

[路徑](msdn-online-vml-path-element.md)

**標記語法**

<v： *element* arrowok = " *expression* " >

**指令碼語法**

 arrowok = "*expression*"

*運算式* =** arrowok

**備註**

如果 **為 False**，則路徑不會有箭頭。 預設值為 **False**。 這個屬性會覆寫父元素或 **筆劃** 元素中的所有其他箭頭屬性。

*VML 標準屬性*

**範例**

路徑不會有箭頭。


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 