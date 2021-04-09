---
title: VML Layout-Flow 屬性
description: VML Layout-Flow 屬性
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933401"
---
# <a name="vml-layout-flow-attribute"></a>VML Layout-Flow 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定文字方塊中文字版面配置的流程。 讀取/寫入 **字串**。

**適用於**

[TextBox](msdn-online-vml-textbox-element.md)

**標記語法**

<v： *element* style = "layout-flow： *expression* " >

**備註**

數值包括：



| 值                  | 描述                                 |
|------------------------|---------------------------------------------|
| 水平             | 文字會以水準方式顯示。 預設值。    |
| 垂直               | 文字會垂直顯示。               |
| 垂直-表意文字   | 會垂直顯示表意字。   |
| 水準-表意文字 | 以水準方式顯示表意字。 |



 

*VML 標準屬性*

**範例**

文字方塊中的文字流程將會垂直流動。


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 