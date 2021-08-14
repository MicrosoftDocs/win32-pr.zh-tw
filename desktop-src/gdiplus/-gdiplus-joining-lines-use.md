---
description: 行聯結是由兩行所組成的一般區域，其結尾會符合或重迭。
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: 聯結線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2aa93eac405bd77f6d87b2a8b86edc8a4043a57de3e4c4d5f31fb45acecc955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066972"
---
# <a name="joining-lines"></a>聯結線

行聯結是由兩行所組成的一般區域，其結尾會符合或重迭。 Windows GDI+ 提供四條線聯結樣式：已裁剪的斜接、斜面、圓形和斜接。 線條聯結樣式是 [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 類別的屬性。 當您為畫筆指定線條聯結樣式，然後使用該畫筆繪製路徑時，會將指定的聯結樣式套用至路徑中的所有連接行。

您可以使用 [**pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen)類別的 [**Pen：： SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin)方法來指定線條聯結樣式。 下列範例示範水平線條和垂直線之間的斜面線聯結：


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



下圖顯示產生的斜面線聯結。

![顯示兩行以右角進行經過斜面化聯結的圖例](images/pens5.png)

在上述範例中，傳遞至 [**Pen：： SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin)方法 (**LineJoinBevel**) 值是 [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin)列舉的元素。

 

 



