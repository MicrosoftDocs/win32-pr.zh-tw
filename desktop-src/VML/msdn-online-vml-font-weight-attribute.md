---
title: VML Font-Weight 屬性
description: VML Font-Weight 屬性
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14dd5edb3fed869390edeff514471359162ee39fd1d78796af3d2a260c96bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754639"
---
# <a name="vml-font-weight-attribute"></a>VML Font-Weight 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義字型之字母的粗細。 讀取/寫入 **字串**。

**適用於**

[TextPath](msdn-online-vml-textpath-element.md)

**標記語法**

<v： *element* style = "font-size： *expression* " >

**指令碼語法**

 fontweight = "*expression*"

*運算式* =** fontweight

**備註**

這些值與標準 HTML 樣式屬性相同。 數值包括：



| 值   | 描述                                                                 |
|---------|-----------------------------------------------------------------------------|
| 正常  | 一般。 預設值。                                                            |
| 粗體    | 大膽。                                                                       |
| bolder  | 比一般一般。                                                        |
| lighter | 比平常更淺。                                                        |
| 100     | 至少以最亮的200權數。                                        |
| 200     | 至少以粗體顯示100權數，以及至少與300權數相同。 |
| 300     | 至少以粗體顯示200權數，以及至少與400權數相同。 |
| 400     | 一般。                                                                     |
| 500     | 至少以粗體顯示400權數，以及至少與600權數相同。 |
| 600     | 至少以粗體顯示500權數，以及至少與700權數相同。 |
| 700     | 大膽。                                                                       |
| 800     | 至少以粗體顯示700權數，以及至少與900權數相同。 |
| 900     | 至少以粗體顯示800權數。                                         |



 

*VML 標準屬性*

**範例**

字型粗細為粗體。


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 