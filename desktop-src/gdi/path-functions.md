---
description: 下列函數用來建立、改變或繪製路徑。
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: '路徑函式 (Windows GDI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700298056ac595b0e9208c0b8535d7a3d2e822e048e4c656d0b4501947764533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759424"
---
# <a name="path-functions-windows-gdi"></a>路徑函式 (Windows GDI) 

下列函數用來建立、改變或繪製路徑。



| 函式                                       | 描述                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | 關閉並捨棄指定之裝置內容中的任何路徑。                                                                                                   |
| [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | 在指定的裝置內容中開啟路徑括弧。                                                                                                            |
| [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | 在路徑中關閉已開啟的圖表。                                                                                                                                 |
| [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | 關閉路徑括弧，並在指定的裝置內容中選取由括弧定義的路徑。                                                             |
| [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | 關閉目前路徑中的所有開啟的圖表，並使用目前的筆刷和多邊形填滿模式來填滿路徑的內部。                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | 將選取的路徑中的任何曲線轉換為目前的裝置內容 (DC) ，將每個曲線轉換成一連串的線條。                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | 抓取指定之裝置內容的斜接限制。                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | 抓取定義線條端點的座標，以及在指定的裝置內容中選取的路徑中找到的曲線控制點。 |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | 從選取到指定之裝置內容的路徑建立區域。                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | 設定指定之裝置內容的斜接聯結長度限制。                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | 關閉路徑中的所有開啟的圖表，使用目前的畫筆來筆劃路徑的外框，並使用目前的筆刷來填滿其內部。                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | 使用目前的畫筆呈現指定的路徑。                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | 將目前的路徑重新定義為如果路徑是使用目前選取的畫筆，在指定的裝置內容中繪製的區域。            |



 

 

 



