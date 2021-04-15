---
title: 'ID 屬性 (VML) '
description: 'ID 屬性 (VML) '
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463325"
---
# <a name="id-attribute-vml"></a>ID 屬性 (VML) 

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

提供元素的唯一識別碼。 讀取/寫入 **字串**。

**適用於**

所有的 VML 元素。

**標記語法**

<v： *elementname* id = " *idname* " >

**指令碼語法**

*elementname* . id = " *idname* "

*運算式* =*elementname*。識別碼

**備註**

使用 **ID** 來參考特定的元素。 一旦您建立了圖形並為其指定識別碼之後，就可以在想要操作專案時使用識別碼名稱。

需要 **識別碼**，才能使用 [ShapeType](msdn-online-vml-shapetype-element.md)元素。

當 Microsoft Office 產生 VML 時，如果將物件模型名稱指派給圖形，則 **識別碼** 會設定為此名稱。 如果未設定物件模型名稱，則會使用 *Spid* (內部圖形識別碼產生名稱) 再加上前置詞 (S （適用于主要圖形的 M）、T 代表 shapetype) 。

*VML 標準屬性*。

**範例**

若要變更圖形的屬性，您必須先為圖形指定識別碼;例如，"myrect"。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



[ID 屬性範例](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example)。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 