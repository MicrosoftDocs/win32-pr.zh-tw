---
description: 行聯結是由兩行所組成的一般區域，其結尾會符合或重迭。
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: 聯結線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2ab0bc53239b9a0d9327a26e25eed1c93c685b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569149"
---
# <a name="joining-lines"></a><span data-ttu-id="302d9-103">聯結線</span><span class="sxs-lookup"><span data-stu-id="302d9-103">Joining Lines</span></span>

<span data-ttu-id="302d9-104">行聯結是由兩行所組成的一般區域，其結尾會符合或重迭。</span><span class="sxs-lookup"><span data-stu-id="302d9-104">A line join is the common area that is formed by two lines whose ends meet or overlap.</span></span> <span data-ttu-id="302d9-105">Windows GDI + 提供四條線聯結樣式：已裁剪的斜接、斜面、圓形和斜接。</span><span class="sxs-lookup"><span data-stu-id="302d9-105">Windows GDI+ provides four line join styles: miter, bevel, round, and miter clipped.</span></span> <span data-ttu-id="302d9-106">線條聯結樣式是 [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="302d9-106">Line join style is a property of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="302d9-107">當您為畫筆指定線條聯結樣式，然後使用該畫筆繪製路徑時，會將指定的聯結樣式套用至路徑中的所有連接行。</span><span class="sxs-lookup"><span data-stu-id="302d9-107">When you specify a line join style for a pen and then use that pen to draw a path, the specified join style is applied to all the connected lines in the path.</span></span>

<span data-ttu-id="302d9-108">您可以使用 [**pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen)類別的 [**Pen：： SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin)方法來指定線條聯結樣式。</span><span class="sxs-lookup"><span data-stu-id="302d9-108">You can specify the line join style by using the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="302d9-109">下列範例示範水平線條和垂直線之間的斜面線聯結：</span><span class="sxs-lookup"><span data-stu-id="302d9-109">The following example demonstrates a beveled line join between a horizontal line and a vertical line:</span></span>


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



<span data-ttu-id="302d9-110">下圖顯示產生的斜面線聯結。</span><span class="sxs-lookup"><span data-stu-id="302d9-110">The following illustration shows the resulting beveled line join.</span></span>

![顯示兩行以右角進行經過斜面化聯結的圖例](images/pens5.png)

<span data-ttu-id="302d9-112">在上述範例中，傳遞至 [**Pen：： SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin)方法 (**LineJoinBevel**) 值是 [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin)列舉的元素。</span><span class="sxs-lookup"><span data-stu-id="302d9-112">In the preceding example, the value (**LineJoinBevel**) passed to the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method is an element of the [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) enumeration.</span></span>

 

 



