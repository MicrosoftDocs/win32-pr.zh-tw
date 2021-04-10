---
title: 'ID 屬性 (VMLFrame)  (VML) '
description: 'ID 屬性 (VMLFrame)  (VML) '
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023690"
---
# <a name="id-attribute-vmlframevml"></a>ID 屬性 (VMLFrame)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義框架的唯一識別碼。 讀取/寫入 **字串**。

**適用於**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**標記語法**

<v： *element* ID = " *expression* " >

**指令碼語法**

*元素* 。 ID = "*expression*"

*運算式* =*元素*。識別碼

**備註**

使用 **ID** 參考框架。 例如，您可以藉由變更 **識別碼** 所參考的框架位置，在頁面上移動框架。

*VML 標準屬性*

**範例**

框架的 **識別碼** 是 "frame01"。


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 