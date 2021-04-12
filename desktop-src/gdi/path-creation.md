---
description: 若要建立路徑並將其選取到 DC，首先必須定義描述它的點。
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: 路徑建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191928"
---
# <a name="path-creation"></a>路徑建立

若要建立路徑並將其選取到 DC，首先必須定義描述它的點。 這是藉由呼叫 [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) 函式來完成，指定適當的繪圖函式，然後再呼叫 [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) 函數。 這種函式組合 (**BeginPath**、繪製函式和 **EndPath**) 構成 *路徑括弧*。 以下是可以使用的繪圖函數清單。

-   [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [**和絃**](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [**橢圓形**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [**圓形圖**](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [**PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [**PolyDraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [**多邊形**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [**聚合線條**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [**PolyPolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [**矩形**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

當應用程式呼叫 [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)時，系統會在指定的 DC 中選取相關聯的路徑。  (如果先前已在 DC 中選取另一個路徑，系統就會刪除該路徑，而不會儲存該路徑 ) 。當系統選取 DC 中的路徑之後，應用程式就可以使用下列其中一種方式在路徑上操作：

-   使用目前的畫筆) 繪製路徑 (的大綱。
-   使用目前的筆刷) ，繪製路徑 (的內部。
-   繪製外框並填滿路徑的內部。
-   修改路徑 (將曲線轉換成線段) 。
-   將路徑轉換成剪輯路徑。
-   將路徑轉換成區域。
-   將路徑中的每個曲線轉換成一連串的線段，以壓平合併路徑。
-   抓取組成路徑之線條和曲線的座標。

 

 



