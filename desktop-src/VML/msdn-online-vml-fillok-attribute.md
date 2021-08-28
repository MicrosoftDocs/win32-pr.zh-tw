---
title: VML FillOK 屬性
description: VML FillOK 屬性
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c346e4499e8c9a0ba390936a61e8c1cd1b4f36c5b115904cfdaee24f4c29ffa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124818"
---
# <a name="vml-fillok-attribute"></a>VML FillOK 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否會顯示填滿。 讀取/寫入 **VgTriState**。

**適用於**

[路徑](msdn-online-vml-path-element.md)

**標記語法**

<v： *element* fillok = " *expression* " >

**指令碼語法**

 fillok = "*expression*"

*運算式* =** fillok

**備註**

如果 **為 False**，則表示路徑無法填入。 預設值為 **True**。 這個屬性會覆寫 parent 或 **fill** 元素中的所有其他填滿屬性。

*VML 標準屬性*

**範例**

將不會填入路徑。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 