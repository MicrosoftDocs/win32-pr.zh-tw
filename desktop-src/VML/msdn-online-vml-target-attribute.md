---
title: VML 目標屬性
description: VML 目標屬性
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106990890"
---
# <a name="vml-target-attribute"></a>VML 目標屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義顯示 URL 的框架或視窗。 讀取/寫入 **字串**。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* target = " *expression* " >

**備註**

**目標** 屬性類似于錨點的標準 HTML **目標** 屬性。

數值包括：



| 值      | 描述                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TargetName | 字串，包含要在其中載入檔的框架或視窗的名稱。                                                                                                                                                                                 |
| \_空白    | 指定將連結的檔載入至新的空白視窗。 此視窗未命名。                                                                                                                                                                  |
| \_媒體    | 從適用于 Windows XP Service Pack 2 的 Internet Explorer 6， \_ 媒體屬性已淘汰且不再受到支援。 第一次在 Internet Explorer 6 中提供，這個值指定連結的檔應該載入到 Media Bar 中。                |
| \_父母   | 指定將連結的檔載入包含連結之檔的直屬父代。                                                                                                                                                      |
| \_搜索   | 從適用于 Windows XP Service Pack 2 的 Internet Explorer 7，： \_ 搜尋屬性已過時，不再受到支援。 第一次在 Internet Explorer 6 中提供，這個值指定連結的檔要載入瀏覽器的 [搜尋] 窗格中。 |
| \_自我     | 指定將連結的檔載入至已按一下連結的視窗中， (使用中視窗) 。                                                                                                                                                  |
| \_top      | 指定將連結的檔載入最上層視窗。                                                                                                                                                                                            |



 

*VML 標準屬性*

**範例**

當您按下矩形時，瀏覽器會在同一個視窗中載入 Microsoft Corporation 首頁。


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[目標屬性範例](/previous-versions/bb264096(v=vs.85))。  (需要 Microsoft Internet Explorer 5 或更高版本。 ) 

 

 