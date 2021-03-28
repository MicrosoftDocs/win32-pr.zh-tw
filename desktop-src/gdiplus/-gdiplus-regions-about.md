---
description: 區域是顯示介面的一部分。
ms.assetid: eb78d7a0-6293-487f-88c5-88ba455b965f
title: 區域 (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d6a7f0a5a6d3df4b11a491111dbedf9e155c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558910"
---
# <a name="regions-gdi"></a><span data-ttu-id="531ea-103">區域 (GDI+)</span><span class="sxs-lookup"><span data-stu-id="531ea-103">Regions (GDI+)</span></span>

<span data-ttu-id="531ea-104">區域是顯示介面的一部分。</span><span class="sxs-lookup"><span data-stu-id="531ea-104">A region is a portion of the display surface.</span></span> <span data-ttu-id="531ea-105">區域可以是簡單 (單一矩形) 或複雜 (多邊形和封閉曲線) 的組合。</span><span class="sxs-lookup"><span data-stu-id="531ea-105">Regions can be simple (a single rectangle) or complex (a combination of polygons and closed curves).</span></span> <span data-ttu-id="531ea-106">下圖顯示兩個區域：一個是從矩形建立的，另一個則是從路徑所建立。</span><span class="sxs-lookup"><span data-stu-id="531ea-106">The following illustration shows two regions: one constructed from a rectangle, and the other constructed from a path.</span></span>

![顯示與不透明曲線圖形重迭的透明矩形區域圖例](images/aboutgdip02-art27.png)

<span data-ttu-id="531ea-108">區域通常用於裁剪和點擊測試。</span><span class="sxs-lookup"><span data-stu-id="531ea-108">Regions are often used for clipping and hit testing.</span></span> <span data-ttu-id="531ea-109">裁剪牽涉到將繪圖限制為螢幕的特定區域，通常是需要更新的螢幕部分。</span><span class="sxs-lookup"><span data-stu-id="531ea-109">Clipping involves restricting drawing to a certain region of the screen, usually the portion of the screen that needs to be updated.</span></span> <span data-ttu-id="531ea-110">點擊測試牽涉到在按下滑鼠按鍵時，檢查游標是否在畫面的特定區域中。</span><span class="sxs-lookup"><span data-stu-id="531ea-110">Hit testing involves checking to see whether the cursor is in a certain region of the screen when a mouse button is pressed.</span></span>

<span data-ttu-id="531ea-111">您可以從矩形或從路徑來建立區域。</span><span class="sxs-lookup"><span data-stu-id="531ea-111">You can construct a region from a rectangle or from a path.</span></span> <span data-ttu-id="531ea-112">您也可以藉由合併現有區域來建立複雜的區域。</span><span class="sxs-lookup"><span data-stu-id="531ea-112">You can also create complex regions by combining existing regions.</span></span> <span data-ttu-id="531ea-113">[**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region)類別提供下列方法來結合區域： [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion))、 [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion))、 [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_))、 [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion))和 [**Region：：補數**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath))。</span><span class="sxs-lookup"><span data-stu-id="531ea-113">The [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) class provides the following methods for combining regions: [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstregion)), [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstregion)), [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)), [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)), and [**Region::Complement**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-complement(inconstgraphicspath)).</span></span>

<span data-ttu-id="531ea-114">兩個區域的交集是屬於這兩個區域的所有點的集合。</span><span class="sxs-lookup"><span data-stu-id="531ea-114">The intersection of two regions is the set of all points belonging to both regions.</span></span> <span data-ttu-id="531ea-115">聯集是所有屬於一或多個區域的所有點的集合。</span><span class="sxs-lookup"><span data-stu-id="531ea-115">The union is the set of all points belonging to one or the other or both regions.</span></span> <span data-ttu-id="531ea-116">區域的補數是不在區域中的所有點的集合。</span><span class="sxs-lookup"><span data-stu-id="531ea-116">The complement of a region is the set of all points that are not in the region.</span></span> <span data-ttu-id="531ea-117">下圖顯示上圖中兩個區域的交集和聯集。</span><span class="sxs-lookup"><span data-stu-id="531ea-117">The following illustration shows the intersection and union of the two regions in the previous figure.</span></span>

![顯示上圖中區域交集及其交集的圖例](images/aboutgdip02-art28.png)

<span data-ttu-id="531ea-119">套用至一組區域的 [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) 方法會產生一個區域，其中包含屬於一個區域或另一個區域的所有點，但不能同時包含兩者。</span><span class="sxs-lookup"><span data-stu-id="531ea-119">The [Xor](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-xor(inconstrect_)) method, applied to a pair of regions, produces a region that contains all points that belong to one region or the other, but not both.</span></span> <span data-ttu-id="531ea-120">適用于一組區域的 [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) 方法會產生一個區域，其中包含第一個區域中不在第二個區域的所有點。</span><span class="sxs-lookup"><span data-stu-id="531ea-120">The [Exclude](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-exclude(inconstregion)) method, applied to a pair of regions, produces a region that contains all points in the first region that are not in the second region.</span></span> <span data-ttu-id="531ea-121">下圖顯示將 Xor 和 Exclude 方法套用至本主題開頭所顯示的兩個區域所產生的區域。</span><span class="sxs-lookup"><span data-stu-id="531ea-121">The following illustration shows the regions that result from applying the Xor and Exclude methods to the two regions shown at the beginning of this topic.</span></span>

![顯示兩個區域中的元件，而不是兩者都有的圖例，以及未與曲線區域重迭的矩形部分](images/aboutgdip02-art29.png)

<span data-ttu-id="531ea-123">若要填滿區域，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、 [**筆刷**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件和 [**區域**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) 物件。</span><span class="sxs-lookup"><span data-stu-id="531ea-123">To fill a region, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object, and a [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) object.</span></span> <span data-ttu-id="531ea-124">**Graphics** 物件提供 [**Graphics：： FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion)方法，而 **筆刷** 物件會儲存填滿的屬性，例如色彩或模式。</span><span class="sxs-lookup"><span data-stu-id="531ea-124">The **Graphics** object provides the [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion) method, and the **Brush** object stores attributes of the fill, such as color or pattern.</span></span> <span data-ttu-id="531ea-125">下列範例會以純色填滿區域。</span><span class="sxs-lookup"><span data-stu-id="531ea-125">The following example fills a region with a solid color.</span></span>


```
myGraphics.FillRegion(&mySolidBrush, &myRegion);
```



 

 
