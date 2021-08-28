---
title: VML 轉譯屬性
description: VML 轉譯屬性
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17063d1e742a5b014e18d61d2d4290eb2511843ef24f1513bd3564ee83c5e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513338"
---
# <a name="vml-render-attribute"></a>VML 轉譯屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義延伸的呈現模式。 讀取/寫入 **字串**。

**適用於**

[擠壓](msdn-online-vml-extrusion-element.md)

**標記語法**

<o： *element* render = " *expression* " >

**指令碼語法**

*element* = "*expression*"

*運算式* =*element*。 render

**備註**

數值包括：



| 值        | 描述                                                   |
|--------------|---------------------------------------------------------------|
| 固體        | 轉譯會顯示穩固的形狀。 預設值。                    |
| 著色    | 轉譯會顯示線框圖形。                         |
| boundingcube | 轉譯會顯示包含圖形的周框 cube。 |



 

*Microsoft OfficeExtensions 屬性*

 

 