---
description: 當您建立 Pen 物件時，可以提供畫筆寬度做為該函式的其中一個引數。 您也可以使用 Pen：： SetWidth 方法來變更畫筆寬度。
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: 設定畫筆寬度和對齊方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553752"
---
# <a name="setting-pen-width-and-alignment"></a><span data-ttu-id="dc15c-104">設定畫筆寬度和對齊方式</span><span class="sxs-lookup"><span data-stu-id="dc15c-104">Setting Pen Width and Alignment</span></span>

<span data-ttu-id="dc15c-105">當您建立 [**pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 物件時，可以提供畫筆寬度做為該函式的其中一個引數。</span><span class="sxs-lookup"><span data-stu-id="dc15c-105">When you create a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object, you can supply the pen width as one of the arguments to the constructor.</span></span> <span data-ttu-id="dc15c-106">您也可以使用 [**pen：： SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) 方法來變更畫筆寬度。</span><span class="sxs-lookup"><span data-stu-id="dc15c-106">You can also change the pen width by using the [**Pen::SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) method.</span></span>

<span data-ttu-id="dc15c-107">理論線的寬度為零。</span><span class="sxs-lookup"><span data-stu-id="dc15c-107">A theoretical line has a width of zero.</span></span> <span data-ttu-id="dc15c-108">當您繪製線條時，圖元會置於理論線的中央。</span><span class="sxs-lookup"><span data-stu-id="dc15c-108">When you draw a line, the pixels are centered on the theoretical line.</span></span> <span data-ttu-id="dc15c-109">下列範例會繪製指定的行兩次：一次使用黑色的寬度1，一次具有寬度為10的綠色畫筆。</span><span class="sxs-lookup"><span data-stu-id="dc15c-109">The following example draws a specified line twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



<span data-ttu-id="dc15c-110">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="dc15c-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="dc15c-111">綠色圖元和黑色圖元會以理論線為中心。</span><span class="sxs-lookup"><span data-stu-id="dc15c-111">The green pixels and the black pixels are centered on the theoretical line.</span></span>

![<span data-ttu-id="dc15c-112">圖例顯示以寬綠線括住的細線、對角線、黑色線</span><span class="sxs-lookup"><span data-stu-id="dc15c-112">illustration showing a thin, diagonal, black line surrounded by a wide, green line</span></span> ](images/pens1a.png)

<span data-ttu-id="dc15c-113">下列範例會繪製一個指定的矩形兩次：一次是黑色畫筆的寬度1，一次具有寬度10的綠色畫筆。</span><span class="sxs-lookup"><span data-stu-id="dc15c-113">The following example draws a specified rectangle twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span> <span data-ttu-id="dc15c-114">此程式碼會將 **PenAlignmentCenter** [**) 列舉值**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) 的 (值傳遞給 [**Pen：： SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) 方法，以指定以綠色畫筆繪製的圖元會以矩形的界限為中心。</span><span class="sxs-lookup"><span data-stu-id="dc15c-114">The code passes the value **PenAlignmentCenter** (an element of the [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) enumeration) to the [**Pen::SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) method to specify that the pixels drawn with the green pen are centered on the boundary of the rectangle.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



<span data-ttu-id="dc15c-115">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="dc15c-115">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="dc15c-116">綠色圖元以黑色圖元表示的理論矩形為中心。</span><span class="sxs-lookup"><span data-stu-id="dc15c-116">The green pixels are centered on the theoretical rectangle, which is represented by the black pixels.</span></span>

![圖例：以較大的綠線括住矩形圖形中的黑色細線](images/pens2.png)

<span data-ttu-id="dc15c-118">您可以修改上述範例中的第三個語句來變更綠色畫筆的對齊方式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="dc15c-118">You can change the green pen's alignment by modifying the third statement in the preceding example as follows:</span></span>


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



<span data-ttu-id="dc15c-119">寬綠線的圖元現在會顯示在矩形內，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="dc15c-119">Now the pixels in the wide green line appear on the inside of the rectangle as shown in the following illustration.</span></span>

![圖例顯示矩形圖形中的黑色黑色線條，將相同圖形的寬綠線封閉](images/pens3.png)

 

 



