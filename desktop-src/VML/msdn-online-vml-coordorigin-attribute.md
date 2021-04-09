---
title: VML CoordOrigin 屬性
description: VML CoordOrigin 屬性
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842344"
---
# <a name="vml-coordorigin-attribute"></a><span data-ttu-id="d1342-103">VML CoordOrigin 屬性</span><span class="sxs-lookup"><span data-stu-id="d1342-103">VML CoordOrigin Attribute</span></span>

<span data-ttu-id="d1342-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="d1342-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d1342-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="d1342-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d1342-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="d1342-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d1342-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="d1342-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d1342-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="d1342-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d1342-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="d1342-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d1342-110">指定將圖形系結之矩形的座標單位原點。</span><span class="sxs-lookup"><span data-stu-id="d1342-110">Specifies the coordinate unit origin of the rectangle that bounds a shape.</span></span> <span data-ttu-id="d1342-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1342-111">Read/write.</span></span> <span data-ttu-id="d1342-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="d1342-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="d1342-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="d1342-113">**Applies To**</span></span>

[<span data-ttu-id="d1342-114">形狀</span><span class="sxs-lookup"><span data-stu-id="d1342-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d1342-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="d1342-115">**Tag Syntax**</span></span>

<span data-ttu-id="d1342-116"><v： *element* coordorigin = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d1342-116"><v: *element* coordorigin=" *expression* "></span></span>

<span data-ttu-id="d1342-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="d1342-117">**Script Syntax**</span></span>

<span data-ttu-id="d1342-118"> coordorigin = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d1342-118">*element* .coordorigin="*expression*"</span></span>

<span data-ttu-id="d1342-119">*運算式* =\*\* coordorigin</span><span class="sxs-lookup"><span data-stu-id="d1342-119">*expression*=*element*.coordorigin</span></span>

<span data-ttu-id="d1342-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="d1342-120">**Remarks**</span></span>

<span data-ttu-id="d1342-121">如果未指定，則原始座標為圖形周框方塊左上角的 (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="d1342-121">If not specified, the origin coordinates are (0,0) at the top left corner of the shape bounding box.</span></span>

<span data-ttu-id="d1342-122">**CoordSize** 的 x 值會加入至 **CoordOrigin** 的 x 值，以判斷水準值的範圍。</span><span class="sxs-lookup"><span data-stu-id="d1342-122">The x value of **CoordSize** is added to the x value of **CoordOrigin** to determine the range of the horizontal values.</span></span> <span data-ttu-id="d1342-123">例如，如果 **CoordOrigin** 的 x 值為-100，而 **CoordSize** 的 x 值為200，則水準單位的範圍將從-100 到 + 100。</span><span class="sxs-lookup"><span data-stu-id="d1342-123">For example,if the x value of **CoordOrigin** is -100 and the x value of **CoordSize** is 200, the horizontal units will range from -100 to +100.</span></span> <span data-ttu-id="d1342-124">如果 **CoordOrigin** 的 x 值為100，而 **CoordSize** 的 x 值為200，則水準單位的範圍將從100到300，全都在周框方塊內。</span><span class="sxs-lookup"><span data-stu-id="d1342-124">If the x value of **CoordOrigin** is 100 and the x value of **CoordSize** is 200, the horizontal units will range from 100 to 300, all within the bounding box.</span></span> <span data-ttu-id="d1342-125">Y 值也是如此。</span><span class="sxs-lookup"><span data-stu-id="d1342-125">The same is true for the y values.</span></span>

<span data-ttu-id="d1342-126">請注意，此屬性是向量，而且單位與 [CoordSize](msdn-online-vml-coordsize-attribute.md) 的單位類型相同。</span><span class="sxs-lookup"><span data-stu-id="d1342-126">Note that this attribute is a vector and that the units are the same type of unit as [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span></span>

<span data-ttu-id="d1342-127">在腳本中，因為這是2D 向量，所以您可以分別存取 x 和 y 值，也可以決定預期的單位類型。</span><span class="sxs-lookup"><span data-stu-id="d1342-127">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="d1342-128">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="d1342-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="d1342-129">**範例**</span><span class="sxs-lookup"><span data-stu-id="d1342-129">**Example**</span></span>

<span data-ttu-id="d1342-130">周框方塊的中心將會是圖形路徑的原點 (0、0) 。</span><span class="sxs-lookup"><span data-stu-id="d1342-130">The center of the bounding box will be the origin (0,0) of the path for the shape.</span></span> <span data-ttu-id="d1342-131">因為 **CoordOrigin** 是 "-500-500" 且 **CoordSize** 為 "1000 1000"，所以水準和垂直單位的範圍將從-500 到 + 500。</span><span class="sxs-lookup"><span data-stu-id="d1342-131">Because **CoordOrigin** is "-500 -500" and **CoordSize** is "1000 1000", the horizontal and vertical units will range from -500 to +500.</span></span> <span data-ttu-id="d1342-132">路徑的左邊和左上角將位於左邊和頂端點所定義的周框方塊中央，如 **樣式** 所定義。</span><span class="sxs-lookup"><span data-stu-id="d1342-132">The left and top corner of the path will be at the center of the bounding box defined by the left and top points as defined by **Style**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="d1342-133">[CoordOrigin 屬性範例](/previous-versions/bb229664(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d1342-133">[CoordOrigin Attribute Example](/previous-versions/bb229664(v=vs.85)).</span></span> <span data-ttu-id="d1342-134"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="d1342-134">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 