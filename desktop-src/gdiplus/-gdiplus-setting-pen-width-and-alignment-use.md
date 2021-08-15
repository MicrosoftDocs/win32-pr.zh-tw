---
description: 當您建立 Pen 物件時，可以提供畫筆寬度做為該函式的其中一個引數。 您也可以使用 Pen：： SetWidth 方法來變更畫筆寬度。
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: 設定畫筆寬度和對齊方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2a6bd5be00fde0f27657cef558365d857775a5b55f9f108074884906916b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885011"
---
# <a name="setting-pen-width-and-alignment"></a>設定畫筆寬度和對齊方式

當您建立 [**pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 物件時，可以提供畫筆寬度做為該函式的其中一個引數。 您也可以使用 [**pen：： SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) 方法來變更畫筆寬度。

理論線的寬度為零。 當您繪製線條時，圖元會置於理論線的中央。 下列範例會繪製指定的行兩次：一次使用黑色的寬度1，一次具有寬度為10的綠色畫筆。


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



下圖顯示上述程式碼的輸出。 綠色圖元和黑色圖元會以理論線為中心。

![圖例顯示以寬綠線括住的細線、對角線、黑色線 ](images/pens1a.png)

下列範例會繪製一個指定的矩形兩次：一次是黑色畫筆的寬度1，一次具有寬度10的綠色畫筆。 此程式碼會將 **PenAlignmentCenter** [**) 列舉值**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) 的 (值傳遞給 [**Pen：： SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) 方法，以指定以綠色畫筆繪製的圖元會以矩形的界限為中心。


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



下圖顯示上述程式碼的輸出。 綠色圖元以黑色圖元表示的理論矩形為中心。

![圖例：以較大的綠線括住矩形圖形中的黑色細線](images/pens2.png)

您可以修改上述範例中的第三個語句來變更綠色畫筆的對齊方式，如下所示：


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



寬綠線的圖元現在會顯示在矩形內，如下圖所示。

![圖例顯示矩形圖形中的黑色黑色線條，將相同圖形的寬綠線封閉](images/pens3.png)

 

 



