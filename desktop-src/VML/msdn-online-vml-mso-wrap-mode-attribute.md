---
title: VML MSO-Wrap 模式屬性
description: VML MSO-Wrap 模式屬性
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e3743522b9286da8a7f30e9100e06205430b1b18fa3c62def60b57f54b65d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136981"
---
# <a name="vml-mso-wrap-mode-attribute"></a>VML MSO-Wrap 模式屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義文字的換行模式。 讀取/寫入 **字串**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* style = "mso-wrap 模式： *expression* " >

**備註**

數值包括：



| 值          | 描述                          |
|----------------|--------------------------------------|
| square         | 在正方形的形狀周圍環繞文字。 |
| 緊          | 文字會包裝在圖形附近。  |
| 頂端和底部 | 從上到下的文字跳躍。       |
| 至        | 文字會透過圖形顯示。     |
| 無           | 文字不會換行。                   |



 

Microsoft PowerPoint 用來儲存至 HTML，以指出在自選圖形內自動換行是 (**方形**) 或 off (**無**) 。

*Microsoft OfficeExtensions 屬性*

**範例**

下列程式碼表示在 PowerPoint 中開啟自選圖形內的 wordwrap。


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 