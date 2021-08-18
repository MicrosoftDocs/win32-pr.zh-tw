---
description: 若要以純色填滿圖形，請建立 SolidBrush 物件，然後將該 SolidBrush 物件的位址當作引數傳遞至 Graphics 類別的其中一個 fill 方法。
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: 以純色填滿形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ad3ecb5efb3bde32f696db8b97319d89834886eb63a70cd45289e49db03863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036716"
---
# <a name="filling-a-shape-with-a-solid-color"></a>以純色填滿形狀

若要以純色填滿圖形，請建立 [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) 物件，然後將該 **SolidBrush** 物件的位址當作引數傳遞至 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的其中一個 fill 方法。 下列範例顯示如何使用紅色的紅色填滿橢圓形：


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



在上述範例中， [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) 的函式會採用 [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) 物件參考做為其唯一的引數。 **色彩** 的函式所使用的值代表色彩的 Alpha、紅色、綠色和藍色元件。 這些值的每一個都必須在0到255的範圍內。 第一個255表示色彩完全不透明，而第二個255表示紅色元件的強度已滿。 這兩個零表示綠色和藍色元件的強度都是0。

傳遞至 [**Graphics：： FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) 方法的四個數字 (0、0、100、60) 指定橢圓形的周框矩形位置和大小。 矩形左上角的 (0、0) 、寬度為100、高度為60。

 

 
