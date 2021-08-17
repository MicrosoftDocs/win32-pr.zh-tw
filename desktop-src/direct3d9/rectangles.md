---
description: 在 Direct3D 和視窗程式設計中，畫面上的物件是以周框矩形為參考。
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: " (Direct3D 9) 的矩形"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02dda6e8a4f10128ab11ffeb8b390e79be7cc0f698ed1625ca3f2c5df995d67e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119368870"
---
# <a name="rectangles-direct3d-9"></a> (Direct3D 9) 的矩形

在 Direct3D 和視窗程式設計中，畫面上的物件是以周框矩形為參考。 週框的側邊永遠和螢幕的側邊平行，以讓矩形可由兩個點描述，這兩點為左上角和右下角。 大部分的應用程式會使用 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構，來攜帶在 blitting 至螢幕或執行點擊偵測時，所要使用的周框的相關資訊。

在 c + + 中， [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構具有下列定義。


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



在先前的範例中，左上成員是繫結矩形的左上角的 x 座標和 y 座標。 同樣地，右下成員組成右下角的座標。 下圖顯示您可以視覺化這些值的方式。

![左、上、右和下方值所繫結矩形的圖例](images/rect.png)

右緣的像素資料行和下緣的像素資料列不包含在 RECT 中。 例如，鎖定成員 {10, 10, 138, 138} 的 RECT 產生矩形寬度與高度為 128 像素的物件。

在效率、一致性和易用性方面，所有的 Direct3D 展示函式都可搭配矩形使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[座標系統和幾何](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
