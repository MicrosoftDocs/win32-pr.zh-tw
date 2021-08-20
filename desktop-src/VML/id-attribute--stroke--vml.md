---
title: 'ID 屬性 (筆觸)  (VML) '
description: 'ID 屬性 (筆觸)  (VML) '
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02fa8ad958315af58e2abfa6d374a6545cc1e3e171080ec29ac6a30600160184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125301"
---
# <a name="id-attribute-strokevml"></a>ID 屬性 (筆觸)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

為筆觸提供唯一識別碼的名稱。 讀取/寫入 **字串**。

**適用於**

[中風](msdn-online-vml-stroke-element.md)

**標記語法**

<v： *element* id = " *expression* " >

**指令碼語法**

*元素* 。 id = "*expression*"

*運算式* =*元素*。識別碼

**備註**

使用 **ID** 來參考特定筆劃。 當您建立筆劃並將其指定為識別碼之後，您可以在想要操作筆劃時使用識別碼名稱。

*VML 標準屬性*

**範例**

圖形具有稱為 "mystroke" 的筆觸識別碼。


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 