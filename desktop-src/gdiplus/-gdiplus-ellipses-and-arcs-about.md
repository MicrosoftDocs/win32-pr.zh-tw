---
description: 橢圓形是由其周框所指定。 下圖顯示一個橢圓形以及它的周框。
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: 橢圓形和弧形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115229"
---
# <a name="ellipses-and-arcs"></a><span data-ttu-id="45ceb-104">橢圓形和弧形</span><span class="sxs-lookup"><span data-stu-id="45ceb-104">Ellipses and Arcs</span></span>

<span data-ttu-id="45ceb-105">橢圓形是由其周框所指定。</span><span class="sxs-lookup"><span data-stu-id="45ceb-105">An ellipse is specified by its bounding rectangle.</span></span> <span data-ttu-id="45ceb-106">下圖顯示一個橢圓形以及它的周框。</span><span class="sxs-lookup"><span data-stu-id="45ceb-106">The following illustration shows an ellipse along with its bounding rectangle.</span></span>

![包含周框矩形內的橢圓形圖例](images/aboutgdip02-art05.png)

<span data-ttu-id="45ceb-108">若要繪製橢圓形，您需要 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件和 [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) 物件。</span><span class="sxs-lookup"><span data-stu-id="45ceb-108">To draw an ellipse, you need a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="45ceb-109">**Graphics** 物件提供 [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_))方法，而 **Pen** 物件會儲存橢圓形的屬性，例如線條寬度和色彩。</span><span class="sxs-lookup"><span data-stu-id="45ceb-109">The **Graphics** object provides the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, and the **Pen** object stores attributes of the ellipse, such as line width and color.</span></span> <span data-ttu-id="45ceb-110">**畫筆** 物件的位址會做為 DrawEllipse 方法的其中一個引數傳遞。</span><span class="sxs-lookup"><span data-stu-id="45ceb-110">The address of the **Pen** object is passed as one of the arguments to the DrawEllipse method.</span></span> <span data-ttu-id="45ceb-111">傳遞至 DrawEllipse 方法的其餘引數會指定橢圓形的周框。</span><span class="sxs-lookup"><span data-stu-id="45ceb-111">The remaining arguments passed to the DrawEllipse method specify the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="45ceb-112">下列範例會繪製一個橢圓形;周框的寬度為160、高度80，以及 (100，50) 的左上角。</span><span class="sxs-lookup"><span data-stu-id="45ceb-112">The following example draws an ellipse; the bounding rectangle has a width of 160, a height of 80, and an upper-left corner of (100, 50).</span></span>


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



<span data-ttu-id="45ceb-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) 是 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的多載方法，因此您可以透過數種方式提供引數給它。</span><span class="sxs-lookup"><span data-stu-id="45ceb-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) is an overloaded method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="45ceb-114">例如，您可以建立 [**rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) 物件，並將 **rect** 物件的參考傳遞為 DrawEllipse 方法的引數。</span><span class="sxs-lookup"><span data-stu-id="45ceb-114">For example, you can construct a [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawEllipse method.</span></span>


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



<span data-ttu-id="45ceb-115">弧形是橢圓形的一部分。</span><span class="sxs-lookup"><span data-stu-id="45ceb-115">An arc is a portion of an ellipse.</span></span> <span data-ttu-id="45ceb-116">若要繪製弧線，請呼叫 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal))方法。</span><span class="sxs-lookup"><span data-stu-id="45ceb-116">To draw an arc, you call the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="45ceb-117">DrawArc 方法的參數與 [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) 方法的參數相同，不同之處在于 DrawArc 需要起始角度和掃除角度。</span><span class="sxs-lookup"><span data-stu-id="45ceb-117">The parameters of the DrawArc method are the same as the parameters of the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, except that DrawArc requires a starting angle and sweep angle.</span></span> <span data-ttu-id="45ceb-118">下列範例會繪製一條弧線，其開始角度為30度，而將角度為180度。</span><span class="sxs-lookup"><span data-stu-id="45ceb-118">The following example draws an arc with a starting angle of 30 degrees and a sweep angle of 180 degrees.</span></span>


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



<span data-ttu-id="45ceb-119">下圖顯示弧線、橢圓形和周框。</span><span class="sxs-lookup"><span data-stu-id="45ceb-119">The following illustration shows the arc, the ellipse, and the bounding rectangle.</span></span>

![周框矩形內的橢圓形圖例;橢圓形的左下半部以紅色繪製](images/aboutgdip02-art06.png)

 

 



