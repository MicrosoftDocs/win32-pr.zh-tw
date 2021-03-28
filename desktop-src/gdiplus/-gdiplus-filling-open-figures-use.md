---
description: 您可以將 GraphicsPath 物件的位址傳遞至 Graphics：： FillPath 方法，以填滿路徑。
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: 填滿開放圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f4a4608b787d8b0af8b9e9c7100a43c0c76dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556720"
---
# <a name="filling-open-figures"></a>填滿開放圖形

您可以將 [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) 物件的位址傳遞至 [**Graphics：： FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) 方法，以填滿路徑。 **Graphics：： FillPath** 方法會根據目前為路徑設定的填滿模式 (替代或繞組) 來填滿路徑。 如果路徑具有任何開放的圖形，則會將路徑填滿，就像這些資料已關閉一樣。 GDI + 會將一條直線從其結束點繪製到起點，以關閉圖表。

下列範例會建立一個路徑，其中有一個開啟的圖 (弧形) 和一個封閉的圖形 (橢圓形) 。 [**Graphics：： FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)方法會根據預設填滿模式來填滿路徑，也就是 FillModeAlternate。


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



下圖顯示上述程式碼的輸出。 請注意，路徑是根據 FillModeAlternate) 填滿 (，如同開啟的圖形是從其結束點到起點的直線封閉。

![圖例顯示重迭寬橢圓形下半部的高橢圓形;union 已填滿，但交集是空的](images/fillopenpath.png)

 

 



