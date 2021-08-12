---
title: 'Title 屬性 (Shape)  (VML) '
description: 'Title 屬性 (Shape)  (VML) '
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ec2a16df6740bca64357dae039f4222de956300604198b2d199977970c526d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596506"
---
# <a name="title-attribute-shapevml"></a>Title 屬性 (Shape)  (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義滑鼠指標移至圖形上方時所顯示的文字。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* title = " *expression* " >

**指令碼語法**

*element* 。 title = "*expression*"

*運算式* =*元素*。標題

**備註**

**標題** 屬性類似于標準 HTML **標題** 屬性。 標題的行為類似于 Microsoft Windows 工具提示。

**VML 標準屬性**

**範例**

圖形的標題是「工具提示顯示」，並會在滑鼠指標移至圖形上方時顯示。


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Title 屬性範例](/previous-versions/bb264097(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 