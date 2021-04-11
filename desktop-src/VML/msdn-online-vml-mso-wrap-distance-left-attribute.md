---
title: VML MSO-換行距離-左方屬性
description: VML MSO-換行距離-左方屬性
ms.assetid: 25dcb5d0-a839-4a4b-8969-8e5dcf1baa47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d1e47fff0f9dceff5fd98ad526208bf487d851
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315430"
---
# <a name="vml-mso-wrap-distance-left-attribute"></a>VML MSO-換行距離-左方屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義從圖形左邊到換行文字的距離。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* style = "mso-wrap-left： *expression* " >

**備註**

請注意，這個屬性與 CSS **Margin** 屬性不同。 **邊界** 會變更圖形的原點以包含邊界區域，但 Microsoft Office 中的換行距離不會變更圖形的原點。

*Microsoft Office Extensions 屬性*

**範例**

圖形的左邊緣為10點。


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-left:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 