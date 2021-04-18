---
title: VML CoordSize 屬性
description: VML CoordSize 屬性
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965649"
---
# <a name="vml-coordsize-attribute"></a><span data-ttu-id="84070-103">VML CoordSize 屬性</span><span class="sxs-lookup"><span data-stu-id="84070-103">VML CoordSize Attribute</span></span>

<span data-ttu-id="84070-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="84070-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="84070-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="84070-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="84070-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="84070-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="84070-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="84070-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="84070-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="84070-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="84070-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="84070-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="84070-110">指定圍繞圖形之矩形的水準和垂直單位。</span><span class="sxs-lookup"><span data-stu-id="84070-110">Specifies the horizontal and vertical units of the rectangle that bounds a shape.</span></span> <span data-ttu-id="84070-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="84070-111">Read/write.</span></span> <span data-ttu-id="84070-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="84070-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="84070-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="84070-113">**Applies To**</span></span>

[<span data-ttu-id="84070-114">形狀</span><span class="sxs-lookup"><span data-stu-id="84070-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="84070-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="84070-115">**Tag Syntax**</span></span>

<span data-ttu-id="84070-116"><v： *element* coordsize = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="84070-116"><v: *element* coordsize=" *expression* "></span></span>

<span data-ttu-id="84070-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="84070-117">**Script Syntax**</span></span>

<span data-ttu-id="84070-118"> coordsize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="84070-118">*element* .coordsize="*expression*"</span></span>

<span data-ttu-id="84070-119">*運算式* =\*\* coordsize</span><span class="sxs-lookup"><span data-stu-id="84070-119">*expression*=*element*.coordsize</span></span>

<span data-ttu-id="84070-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="84070-120">**Remarks**</span></span>

<span data-ttu-id="84070-121">如果未指定，座標大小與圖形的周框方塊相同。</span><span class="sxs-lookup"><span data-stu-id="84070-121">If not specified, the coordinate size is the same as the bounding box of the shape.</span></span>

<span data-ttu-id="84070-122">請注意，此屬性是向量，而且單位是相對於周框矩形的長度和寬度。</span><span class="sxs-lookup"><span data-stu-id="84070-122">Note that this attribute is a vector and that the units are relative to the length and width of the bounding rectangle.</span></span>

<span data-ttu-id="84070-123">另請注意， **coordsize** 和周框方塊之間的對應可設為非等的。</span><span class="sxs-lookup"><span data-stu-id="84070-123">Also note that mapping between **coordsize** and the bounding box can be made anisotropic.</span></span> <span data-ttu-id="84070-124">如果您不想要扭曲圖形，請確定 **coordsize 寬度** 和 **coordsize 高度** 與 **樣式寬度** 和 **高度** 相同。</span><span class="sxs-lookup"><span data-stu-id="84070-124">Make sure that the **coordsize width** and **coordsize height** is the same as the **style width** and **height** if you don't want to distort the shape.</span></span>

<span data-ttu-id="84070-125">在腳本中，因為這是2D 向量，所以您可以分別存取 x 和 y 值，也可以決定預期的單位類型。</span><span class="sxs-lookup"><span data-stu-id="84070-125">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="84070-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="84070-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="84070-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="84070-127">**Example**</span></span>

<span data-ttu-id="84070-128">圖形是100點高和100點寬，但座標空間中的每個水準和垂直單位都是點的1/10。</span><span class="sxs-lookup"><span data-stu-id="84070-128">The shape is 100 points high and 100 points wide, but each horizontal and vertical unit in the coordinate space is 1/10 of a point.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="84070-129">[CoordSize 屬性範例](/previous-versions/bb229665(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84070-129">[CoordSize Attribute Example](/previous-versions/bb229665(v=vs.85)).</span></span> <span data-ttu-id="84070-130"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="84070-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 