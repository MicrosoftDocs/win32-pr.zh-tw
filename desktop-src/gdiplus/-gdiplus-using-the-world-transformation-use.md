---
description: 「世界」轉換是圖形類別的屬性。
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: 使用全局轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191310"
---
# <a name="using-the-world-transformation"></a>使用全局轉換

「世界」轉換是 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的屬性。 指定「世界」轉換的數位會儲存在 [**矩陣**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) 物件中，此物件代表3×3矩陣。 **矩陣** 和 **圖形** 類別有數個方法可以設定全球轉換矩陣中的數位。 本節中的範例會操作矩形，因為矩形很容易繪製，而且很容易就能看到轉換在矩形上的效果。

我們一開始會先建立 50 by 50 矩形，然後在原點 (0，0) 找出它。 原點位於工作區的左上角。


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



下列程式碼會套用縮放轉換，以 x 方向的1.75 因數來展開矩形，並以 y 方向的0.5 因數來縮小矩形：


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



結果是一個矩形，這個矩形的長度超過 x 方向，而且在 y 方向比原始的還短。

若要旋轉矩形而不是縮放，請使用下列程式碼，而不是上述程式碼：


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



若要轉譯矩形，請使用下列程式碼：


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



