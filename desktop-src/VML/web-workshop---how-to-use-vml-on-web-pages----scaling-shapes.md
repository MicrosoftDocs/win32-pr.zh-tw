---
title: 調整形狀
description: 調整形狀
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- 網路研討會，調整圖形
- 設計網頁、調整圖形
- Vector Markup Language (VML) 、縮放圖形
- VML (Vector Markup Language) 、縮放形狀
- 向量圖形，縮放形狀
- VML 圖形，縮放比例
- 調整形狀
- Vector Markup Language (VML) ，調整大小圖形
- VML (Vector Markup Language) ，調整大小圖形
- 向量圖形，調整大小圖形
- VML 圖形，調整大小
- 調整大小圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc7f62d802548ef1bc19aabf33c886c5b826098ae1280a9dd0b69413c9a61aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057005"
---
# <a name="scaling-shapes"></a>調整形狀

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

您已瞭解如何使用 VML 在網頁上繪製和上色圖形。 在本主題中，我們將說明如何將圖形調整為任何您想要的大小。

VML 使用在[CSS2 規格](https://www.w3.org/TR/PR-CSS2/)的 [[視覺效果轉譯模型詳細資料](https://www.w3.org/TR/PR-CSS2/visudet.mdl)] 區段中定義的相同語法來指定包含方塊的大小，以便將圖形內容轉譯 (在包含的方塊中繪製) 。 您可以使用 [ **寬度** ] 和 [ **高度** ] 樣式屬性來定義包含方塊的大小。

例如，如果您繪製 oval 並指定 **style**= ' width： 75pt; height： 100pt '，則會在包含大小為75點的方塊內繪製橢圓， (寬度) 100 點 (高度) ，如下列圖片所示：

![oval1.gif (660 個位元組) ](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





如果您將大小變更為 **style**= ' width： 120pt; height： 140pt '，則 oval 會變大，因為它會在新的包含方塊中調整120點大小， (寬度) 140 點 (高度) ，如下圖所示：

![oval2.gif (966 個位元組) ](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





如果您將大小變更為 **style**= ' width： 60pt; height： 40pt '，則 oval 會變得較小，因為它會在新的內含方塊中調整60點大小， (寬度) 40 點 (高度) ，如下圖所示：

![oval3.gif (394 個位元組) ](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 