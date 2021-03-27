---
description: Windows GDI + 提供數個在 DashStyle 列舉中列出的虛線樣式。 如果這些標準虛線樣式不符合您的需求，您可以建立自訂虛線模式。
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: 繪製自訂虛線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988116"
---
# <a name="drawing-a-custom-dashed-line"></a><span data-ttu-id="f0432-104">繪製自訂虛線</span><span class="sxs-lookup"><span data-stu-id="f0432-104">Drawing a Custom Dashed Line</span></span>

<span data-ttu-id="f0432-105">Windows GDI + 提供數個在 [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) 列舉中列出的虛線樣式。</span><span class="sxs-lookup"><span data-stu-id="f0432-105">Windows GDI+ provides several dash styles that are listed in the [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) enumeration.</span></span> <span data-ttu-id="f0432-106">如果這些標準虛線樣式不符合您的需求，您可以建立自訂虛線模式。</span><span class="sxs-lookup"><span data-stu-id="f0432-106">If those standard dash styles don't suit your needs, you can create a custom dash pattern.</span></span>

<span data-ttu-id="f0432-107">若要繪製自訂虛線，請將連字號和空格的長度放在陣列中，並將陣列的位址當作引數傳遞至 [**pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen)物件的 [**Pen：： SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern)方法。</span><span class="sxs-lookup"><span data-stu-id="f0432-107">To draw a custom dashed line, put the lengths of the dashes and spaces in an array and pass the address of the array as an argument to the [**Pen::SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) method of a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="f0432-108">下列範例會根據陣列 {5，2，15，4} 繪製自訂虛線。</span><span class="sxs-lookup"><span data-stu-id="f0432-108">The following example draws a custom dashed line based on the array {5, 2, 15, 4}.</span></span> <span data-ttu-id="f0432-109">如果您將陣列的元素乘以畫筆寬度5的元素，則會得到 {25，10，75，20}。</span><span class="sxs-lookup"><span data-stu-id="f0432-109">If you multiply the elements of the array by the pen width of 5, you get {25, 10, 75, 20}.</span></span> <span data-ttu-id="f0432-110">顯示的連字號在25和75之間的長度，以及介於10和20之間的空格替代。</span><span class="sxs-lookup"><span data-stu-id="f0432-110">The displayed dashes alternate in length between 25 and 75, and the spaces alternate in length between 10 and 20.</span></span>


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



<span data-ttu-id="f0432-111">下圖顯示產生的虛線。</span><span class="sxs-lookup"><span data-stu-id="f0432-111">The following illustration shows the resulting dashed line.</span></span> <span data-ttu-id="f0432-112">請注意，最後一個破折號必須少於25個單位，如此一行才能以 (405，5) 結尾。</span><span class="sxs-lookup"><span data-stu-id="f0432-112">Note that the final dash has to be shorter than 25 units so that the line can end at (405, 5).</span></span>

![圖例顯示虛線;每個區段都是一個短行，後面接著一個長條](images/pens6.png)

 

 



