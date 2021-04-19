---
title: VML 可見度屬性
description: VML 可見度屬性
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967674"
---
# <a name="vml-visibility-attribute"></a>VML 可見度屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否要顯示圖形。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* style = "可見度： *expression* " >

**指令碼語法**

style *. visibility* = "*expression*"

*運算式* =*element*。 visibility

**備註**

**可見度** 屬性類似于樣式的標準 HTML **可見度** 屬性。

數值包括：



| 值    | 描述                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 可見  | 圖形是可見的。                                                                                                                                                                   |
| 隱藏   | 圖形是不可見的，但仍是瀏覽器中物件流程的一部分。 系統不會處理滑鼠事件。                                                                  |
| inherit  | 預設值。 可見度狀態是繼承自圖形的父系。 Microsoft Office 的應用程式只會使用 **繼承** 和 **隱藏**;任何其他值都會對應到 **inherit**。 |
| 摺疊 | 用於可折迭圖形群組的圖形編輯應用程式;例如，outliners。                                                                                     |



 

*VML 標準屬性*

**範例**

下列程式碼會建立一個圖形，但讓它隱藏起來。 檔中的其他物件會在其周圍流動，讓空間的大小與圖形相同。


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



[可見度屬性範例](/previous-versions/bb264100(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 