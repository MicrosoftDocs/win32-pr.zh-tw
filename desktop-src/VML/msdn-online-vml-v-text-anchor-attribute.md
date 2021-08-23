---
title: VML V 文字錨點屬性
description: VML V 文字錨點屬性
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c4b355aa4e56e3b0320200a092a66aa1f504b16be02f697e1335cd295627c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057696"
---
# <a name="vml-v-text-anchor-attribute"></a>VML V 文字錨點屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義文字方塊中文字的垂直錨定。 讀取/寫入 **字串**。

**適用於**

[TextBox](msdn-online-vml-textbox-element.md)

**標記語法**

<v： *element* v-text-錨點 = " *expression* " >

**備註**

數值包括：

-   **top** (預設) 
-   **中間**
-   **底部**
-   **上至中央**
-   **中間中心**
-   **下中心**
-   **最上層基準**
-   **下-基準**
-   **最上層-基準**
-   **下中心-基準**

文字會錨定到文字方塊中的垂直位置，如屬性值所示。 只有當 [MSO 符合文字到圖形](msdn-online-vml-mso-fit-text-to-shape-attribute.md) 為 **False** 時，文字錨點的對齊才會變得很明顯。 這個屬性與 **垂直對齊** 樣式屬性不同，它是用於表意文字的語言。

Microsoft Office 會使用這個屬性將資料儲存在 Web 檔中，但不會在 Microsoft Internet Explorer 5 或更新版本中轉譯。

*VML 標準屬性*

**範例**

文字對齊文字方塊的底部。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 