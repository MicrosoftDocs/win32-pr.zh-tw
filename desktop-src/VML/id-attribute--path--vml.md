---
title: 'ID 屬性 (路徑)  (VML) '
description: 'ID 屬性 (路徑)  (VML) '
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29fe87845616b0e93e47458cd5c96f25733edd3aea7b09af6088b057d8ce0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118845916"
---
# <a name="id-attribute-pathvml"></a>ID 屬性 (路徑)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

為路徑提供唯一識別碼的名稱。 讀取/寫入 **字串**。

**適用於**

[路徑](msdn-online-vml-path-element.md)

**標記語法**

<v： *element* id = " *expression* " >

**指令碼語法**

*元素* 。 id = "*expression*"

*運算式* =*元素*。識別碼

**備註**

使用 **ID** 來參考特定路徑。 當您建立路徑並指定識別碼之後，您可以在想要操作路徑時使用識別碼名稱。

*VML 標準屬性*

**範例**

圖形具有名為 "myPath" 的路徑識別碼。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 