---
description: 基本曲線是一條聯結的個別曲線，形成較大的曲線。
ms.assetid: 4fc62f00-7006-4ade-bfcc-091a3a97d889
title: 基本曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d85c0163e405a6f9346f521b4057eb936108cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192353"
---
# <a name="cardinal-splines"></a><span data-ttu-id="8f892-103">基本曲線</span><span class="sxs-lookup"><span data-stu-id="8f892-103">Cardinal Splines</span></span>

<span data-ttu-id="8f892-104">基本曲線是一條聯結的個別曲線，形成較大的曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-104">A cardinal spline is a sequence of individual curves joined to form a larger curve.</span></span> <span data-ttu-id="8f892-105">曲線是由點陣列和張力參數所指定。</span><span class="sxs-lookup"><span data-stu-id="8f892-105">The spline is specified by an array of points and a tension parameter.</span></span> <span data-ttu-id="8f892-106">基線曲線會順暢地通過陣列中的每個點;曲線的 tightness 沒有尖角，而且沒有任何突然變化。</span><span class="sxs-lookup"><span data-stu-id="8f892-106">A cardinal spline passes smoothly through each point in the array; there are no sharp corners and no abrupt changes in the tightness of the curve.</span></span> <span data-ttu-id="8f892-107">下圖顯示一組點，以及通過集合中每個點的基本曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-107">The following illustration shows a set of points and a cardinal spline that passes through each point in the set.</span></span>

![圖例顯示通過六個定義點的基線曲線](images/aboutgdip02-art09.gif)

<span data-ttu-id="8f892-109">實體曲線是一種精簡的木頭或其他彈性的教材。</span><span class="sxs-lookup"><span data-stu-id="8f892-109">A physical spline is a thin piece of wood or other flexible material.</span></span> <span data-ttu-id="8f892-110">在數學曲線的出現之前，設計人員使用了實體曲線來繪製曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-110">Before the advent of mathematical splines, designers used physical splines to draw curves.</span></span> <span data-ttu-id="8f892-111">設計工具會將曲線放在一張紙上，並錨定到指定的點集合。</span><span class="sxs-lookup"><span data-stu-id="8f892-111">A designer would place the spline on a piece of paper and anchor it to a given set of points.</span></span> <span data-ttu-id="8f892-112">然後，設計工具可以使用鉛筆沿著曲線繪製來建立曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-112">The designer could then create a curve by drawing along the spline with a pencil.</span></span> <span data-ttu-id="8f892-113">根據實體曲線的屬性，指定的點集合可能會產生各種曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-113">A given set of points could yield a variety of curves, depending on the properties of the physical spline.</span></span> <span data-ttu-id="8f892-114">例如，具有高阻力來彎曲的曲線會產生與極具彈性曲線的不同曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-114">For example, a spline with a high resistance to bending would produce a different curve than an extremely flexible spline.</span></span>

<span data-ttu-id="8f892-115">數學曲線的公式是以彈性棒敲的屬性為基礎，因此數學曲線所產生的曲線類似于實體曲線所產生的曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-115">The formulas for mathematical splines are based on the properties of flexible rods, so the curves produced by mathematical splines are similar to the curves that were once produced by physical splines.</span></span> <span data-ttu-id="8f892-116">如同不同張力的實體曲線會透過一組指定的點來產生不同的曲線，具有張力參數不同值的數學曲線將會透過一組指定的點來產生不同的曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-116">Just as physical splines of different tension will produce different curves through a given set of points, mathematical splines with different values for the tension parameter will produce different curves through a given set of points.</span></span> <span data-ttu-id="8f892-117">下圖顯示四個透過相同點集合傳遞的基本曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-117">The following illustration shows four cardinal splines passing through the same set of points.</span></span> <span data-ttu-id="8f892-118">會顯示每個曲線的張力。</span><span class="sxs-lookup"><span data-stu-id="8f892-118">The tension is shown for each spline.</span></span> <span data-ttu-id="8f892-119">請注意，張力0會對應到無限的實體張力，強制曲線採用最短的方式 (直線之間) 的點。</span><span class="sxs-lookup"><span data-stu-id="8f892-119">Note that a tension of 0 corresponds to infinite physical tension, forcing the curve to take the shortest way (straight lines) between points.</span></span> <span data-ttu-id="8f892-120">一個張力1對應到無實體張力，讓曲線能夠採用最少的折彎軌跡。</span><span class="sxs-lookup"><span data-stu-id="8f892-120">A tension of 1 corresponds to no physical tension, allowing the spline to take the path of least total bend.</span></span> <span data-ttu-id="8f892-121">當張力值大於1時，曲線的行為就像是壓縮的彈簧，會被推送以取得較長的路徑。</span><span class="sxs-lookup"><span data-stu-id="8f892-121">With tension values greater than 1, the curve behaves like a compressed spring, pushed to take a longer path.</span></span>

![顯示四個基本曲線的圖，透過相同的三個點](images/aboutgdip02-art10.gif)

<span data-ttu-id="8f892-123">請注意，上圖中的四個曲線會在起始點共用相同的正切線條。</span><span class="sxs-lookup"><span data-stu-id="8f892-123">Note that the four splines in the preceding figure share the same tangent line at the starting point.</span></span> <span data-ttu-id="8f892-124">正切函數是沿著曲線從起點到下一個點繪製的線條。</span><span class="sxs-lookup"><span data-stu-id="8f892-124">The tangent is the line drawn from the starting point to the next point along the curve.</span></span> <span data-ttu-id="8f892-125">同樣地，結束點的共用正切函數是從結束點繪製到曲線上上一個點的線條。</span><span class="sxs-lookup"><span data-stu-id="8f892-125">Likewise, the shared tangent at the ending point is the line drawn from the ending point to the previous point on the curve.</span></span>

<span data-ttu-id="8f892-126">若要繪製基本曲線，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件和 [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) 物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="8f892-126">To draw a cardinal spline, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and an array of [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="8f892-127">**Graphics** 物件提供 [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inreal))方法，它會繪製曲線，而 **Pen** 物件會儲存曲線的屬性，例如線條寬度和色彩。</span><span class="sxs-lookup"><span data-stu-id="8f892-127">The **Graphics** object provides the [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inreal)) method, which draws the spline, and the **Pen** object stores attributes of the spline, such as line width and color.</span></span> <span data-ttu-id="8f892-128">**Point** 物件的陣列會儲存曲線將通過的點。</span><span class="sxs-lookup"><span data-stu-id="8f892-128">The array of **Point** objects stores the points that the curve will pass through.</span></span> <span data-ttu-id="8f892-129">下列範例會繪製在 *myPointArray* 中傳遞點的基本曲線。</span><span class="sxs-lookup"><span data-stu-id="8f892-129">The following example draws a cardinal spline that passes through the points in *myPointArray*.</span></span> <span data-ttu-id="8f892-130">第三個參數是張力。</span><span class="sxs-lookup"><span data-stu-id="8f892-130">The third parameter is the tension.</span></span>


```
myGraphics.DrawCurve(&myPen, myPointArray, 3, 1.5f);
```



 

 



