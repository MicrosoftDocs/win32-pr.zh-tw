---
description: 下列函式會搭配區域使用。
ms.assetid: 3a42fc7a-4c07-4540-99a7-520f99532f33
title: '區域函式 (Windows GDI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0f55549f978dd2868f231b9ff042f6f825459d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972545"
---
# <a name="region-functions-windows-gdi"></a>區域函式 (Windows GDI) 

下列函式會搭配區域使用。



| 函式                                                       | 描述                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)                               | 結合兩個區域，並將結果儲存在第三個區域。                                |
| [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)                 | 建立橢圓形區域。                                                                |
| [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect) | 建立橢圓形區域。                                                                |
| [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)                   | 建立多邊形區域。                                                                  |
| [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)           | 建立由一系列多邊形組成的區域。                                         |
| [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)                         | 建立矩形區域。                                                                |
| [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)         | 建立矩形區域。                                                                |
| [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)               | 建立具有圓角的矩形區域。                                           |
| [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn)                                   | 檢查兩個指定的區域，以判斷它們是否相同。                    |
| [**ExtCreateRegion**](/windows/desktop/api/Wingdi/nf-wingdi-extcreateregion)                     | 從指定的區域和轉換資料建立區域。                          |
| [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn)                                     | 使用指定的筆刷來填滿區域。                                                 |
| [**FrameRgn**](/windows/desktop/api/Wingdi/nf-wingdi-framergn)                                   | 使用指定的筆刷，在指定的區域周圍繪製框線。                     |
| [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)                     | 抓取目前的多邊形填滿模式。                                                     |
| [**GetRegionData**](/windows/desktop/api/Wingdi/nf-wingdi-getregiondata)                         | 使用描述區域的資料來填滿指定的緩衝區。                                    |
| [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox)                                 | 抓取指定區域的周框。                                    |
| [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn)                                 | 反轉指定區域中的色彩。                                                  |
| [**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)                                 | 依據指定的位移移動區域。                                                     |
| [**PaintRgn**](/windows/desktop/api/Wingdi/nf-wingdi-paintrgn)                                   | 使用目前選取的筆刷至裝置內容，繪製指定的區域。   |
| [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion)                               | 判斷指定的點是否在指定的區域內。                       |
| [**RectInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-rectinregion)                           | 判斷指定之矩形的任何部分是否在區域界限內。 |
| [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)                     | 為填滿多邊形的函式設定多邊形填滿模式。                                 |
| [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)                               | 將區域轉換成具有指定座標的矩形區域。                  |



 

 

 



