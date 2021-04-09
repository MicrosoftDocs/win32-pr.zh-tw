---
title: 使用 Path 元素
description: 使用 Path 元素
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- 網路研討會，path 元素
- 設計網頁、path 元素
- Vector Markup Language (VML) 、path 元素
- VML (Vector Markup Language) ，path 元素
- 向量圖形，path 元素
- path 元素
- VML 元素，路徑
- VML 圖形，path 元素
- Vector Markup Language (VML) 、自訂圖形大綱
- VML (Vector Markup Language) 、自訂圖形大綱
- 向量圖形，自訂圖形大綱
- VML 圖形，自訂大綱
- 自訂圖形大綱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682970"
---
# <a name="using-the-path-element"></a><span data-ttu-id="63d08-116">使用 Path 元素</span><span class="sxs-lookup"><span data-stu-id="63d08-116">Using the Path Element</span></span>

<span data-ttu-id="63d08-117">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="63d08-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="63d08-118">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="63d08-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="63d08-119">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="63d08-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="63d08-120">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="63d08-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="63d08-121">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="63d08-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="63d08-122">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="63d08-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="63d08-123">您已瞭解您可以使用 VML 預先定義的圖形元素，例如、、 `<oval>` 、、、 `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` 和 `<arc>` --繪製圖形。</span><span class="sxs-lookup"><span data-stu-id="63d08-123">You've learned that you can use the VML predefined shape elements -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` -- to draw a shape.</span></span> <span data-ttu-id="63d08-124">在本主題中，我們將說明如何使用 `<path>` 子項目自訂圖形的外框。</span><span class="sxs-lookup"><span data-stu-id="63d08-124">In this topic, we will illustrate how to use the `<path>` sub-element to customize the outline of a shape.</span></span>

<span data-ttu-id="63d08-125">您可以將子專案放在 `<path>` `<shape>` 或元素內 `<shapetype>` 。</span><span class="sxs-lookup"><span data-stu-id="63d08-125">You can place the `<path>` sub-element inside the `<shape>` or `<shapetype>` element.</span></span> <span data-ttu-id="63d08-126">然後，您可以使用子項目的屬性屬性 `<path>` 來自訂圖形的外框。</span><span class="sxs-lookup"><span data-stu-id="63d08-126">You can then use the property attributes of the `<path>` sub-element to customize the outline of the shape.</span></span>

<span data-ttu-id="63d08-127">例如，若要繪製下圖中所示的自訂圖形，您可以使用 `<path>` 子項目來定義圖形的外框，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="63d08-127">For example, to draw the customized shape illustrated in the following picture, you can use the `<path>` sub-element to define the outline of the shape, as shown in the following VML representation:</span></span>

![shape1.gif (1301 個位元組) ](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   <span data-ttu-id="63d08-129">這些值 `m 8,65` 表示繪圖從 (8，65) 的點開始。</span><span class="sxs-lookup"><span data-stu-id="63d08-129">The values `m 8,65` indicate that the drawing starts at the point (8,65).</span></span>
-   <span data-ttu-id="63d08-130">這些值 `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` 表示直線從目前的點開始 (8，65) ，結束于指定的點 (72，65) ，這會成為新的目前點。</span><span class="sxs-lookup"><span data-stu-id="63d08-130">The values `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicate that a straight line begins at the current point (8, 65) and ends at the given point (72, 65), which becomes the new current point.</span></span> <span data-ttu-id="63d08-131">新的一行會從目前的點開始 (72、65) ，並在給定的點結束，後者會成為新的目前點，依此類推，最後一個點 (60，100) 。</span><span class="sxs-lookup"><span data-stu-id="63d08-131">A new line begins at the current point (72, 65) and ends at the given point, which becomes the new current point, and so on, to the final point (60, 100).</span></span>
-   <span data-ttu-id="63d08-132">`x` 指出路徑會以從目前點開始 (60、100) 的直線來關閉，並在原始點 (8 65) 結束。</span><span class="sxs-lookup"><span data-stu-id="63d08-132">`x` indicates that the path will close by a straight line that starts at the current point (60, 100) and ends at the original point (8, 65).</span></span>
-   <span data-ttu-id="63d08-133">`e` 表示停止繪圖。</span><span class="sxs-lookup"><span data-stu-id="63d08-133">`e` indicates stop drawing.</span></span>

<span data-ttu-id="63d08-134">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858391) 。</span><span class="sxs-lookup"><span data-stu-id="63d08-134">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span></span>

 

 