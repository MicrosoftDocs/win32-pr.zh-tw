---
description: 通常，為頂點指定的點不完全符合螢幕上的像素。 當發生此狀況，Direct3D 會套用點陣化規則來判斷哪些像素適用於指定三角形。
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: " (Direct3D 9) 的點陣化規則"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104195654"
---
# <a name="rasterization-rules-direct3d-9"></a><span data-ttu-id="17ca6-104"> (Direct3D 9) 的點陣化規則</span><span class="sxs-lookup"><span data-stu-id="17ca6-104">Rasterization Rules (Direct3D 9)</span></span>

<span data-ttu-id="17ca6-105">通常，為頂點指定的點不完全符合螢幕上的像素。</span><span class="sxs-lookup"><span data-stu-id="17ca6-105">Often, the points specified for vertices do not precisely match the pixels on the screen.</span></span> <span data-ttu-id="17ca6-106">當發生此狀況，Direct3D 會套用點陣化規則來判斷哪些像素適用於指定三角形。</span><span class="sxs-lookup"><span data-stu-id="17ca6-106">When this happens, Direct3D applies triangle rasterization rules to decide which pixels apply to a given triangle.</span></span>

-   [<span data-ttu-id="17ca6-107">三角形的點陣化規則</span><span class="sxs-lookup"><span data-stu-id="17ca6-107">Triangle Rasterization Rules</span></span>](#triangle-rasterization-rules)
-   [<span data-ttu-id="17ca6-108">點與行規則</span><span class="sxs-lookup"><span data-stu-id="17ca6-108">Point and Line Rules</span></span>](#point-and-line-rules)
-   [<span data-ttu-id="17ca6-109">點 Sprite 規則</span><span class="sxs-lookup"><span data-stu-id="17ca6-109">Point Sprite Rules</span></span>](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a><span data-ttu-id="17ca6-110">三角形點陣化規則</span><span class="sxs-lookup"><span data-stu-id="17ca6-110">Triangle Rasterization Rules</span></span>

<span data-ttu-id="17ca6-111">Direct3D 針對填充幾何使用左上角填充慣例。</span><span class="sxs-lookup"><span data-stu-id="17ca6-111">Direct3D uses a top-left filling convention for filling geometry.</span></span> <span data-ttu-id="17ca6-112">這是針對 GDI 和 OpenGL 矩形中使用的相同慣例。</span><span class="sxs-lookup"><span data-stu-id="17ca6-112">This is the same convention that is used for rectangles in GDI and OpenGL.</span></span> <span data-ttu-id="17ca6-113">在 Direct3D 中，像素的中心是決定點。</span><span class="sxs-lookup"><span data-stu-id="17ca6-113">In Direct3D, the center of the pixel is the decisive point.</span></span> <span data-ttu-id="17ca6-114">如果中心在三角形內部，像素是三角形的一部分。</span><span class="sxs-lookup"><span data-stu-id="17ca6-114">If the center is inside a triangle, the pixel is part of the triangle.</span></span> <span data-ttu-id="17ca6-115">像素中心位於整數座標。</span><span class="sxs-lookup"><span data-stu-id="17ca6-115">Pixel centers are at integer coordinates.</span></span>

<span data-ttu-id="17ca6-116">這個 Direct3D 使用的三角形點陣化規則描述，不一定適用於所有可用的硬體。</span><span class="sxs-lookup"><span data-stu-id="17ca6-116">This description of triangle-rasterization rules used by Direct3D does not necessarily apply to all available hardware.</span></span> <span data-ttu-id="17ca6-117">您的測試可能會發現這些規則實作的次要變化。</span><span class="sxs-lookup"><span data-stu-id="17ca6-117">Your testing may uncover minor variations in the implementation of these rules.</span></span>

<span data-ttu-id="17ca6-118">下圖顯示左上角位於 (0, 0) ，右下角位於 (5, 5) 的矩形。</span><span class="sxs-lookup"><span data-stu-id="17ca6-118">The following illustration shows a rectangle whose upper-left corner is at (0, 0) and whose lower-right corner is at (5, 5).</span></span> <span data-ttu-id="17ca6-119">如您所預期，這個矩形填滿 25 個像素。</span><span class="sxs-lookup"><span data-stu-id="17ca6-119">This rectangle fills 25 pixels, just as you would expect.</span></span> <span data-ttu-id="17ca6-120">矩形的寬度定義為右減左。</span><span class="sxs-lookup"><span data-stu-id="17ca6-120">The width of the rectangle is defined as right minus left.</span></span> <span data-ttu-id="17ca6-121">高度被定義為上減下。</span><span class="sxs-lookup"><span data-stu-id="17ca6-121">The height is defined as bottom minus top.</span></span>

![編號正方形分為六個數據列和資料行的圖例](images/pixmap.png)

<span data-ttu-id="17ca6-123">在左上填充慣例，*上* 是指水平跨距的垂直位置，*左* 是指跨距內像素的水平位置。</span><span class="sxs-lookup"><span data-stu-id="17ca6-123">In the top-left filling convention, *top* refers to the vertical location of horizontal spans, and *left* refers to the horizontal location of pixels within a span.</span></span> <span data-ttu-id="17ca6-124">邊不可為頂邊，除是是水平方向。</span><span class="sxs-lookup"><span data-stu-id="17ca6-124">An edge cannot be a top edge unless it is horizontal.</span></span> <span data-ttu-id="17ca6-125">一般而言，大部分三角形只有左右邊。</span><span class="sxs-lookup"><span data-stu-id="17ca6-125">In general, most triangles have only left and right edges.</span></span> <span data-ttu-id="17ca6-126">下圖顯示頂邊和右邊。</span><span class="sxs-lookup"><span data-stu-id="17ca6-126">The following illustration shows a top edge and a right edge.</span></span>

![包含兩個三角形的編號正方形圖例](images/triedge.png)

<span data-ttu-id="17ca6-128">左上角填充慣例判斷當三角形通過像素的中心時 Direct3D 會採取的動作。</span><span class="sxs-lookup"><span data-stu-id="17ca6-128">The top-left filling convention determines the action taken by Direct3D when a triangle passes through the center of a pixel.</span></span> <span data-ttu-id="17ca6-129">下圖顯示兩個三角形，一個在 (0, 0)、(5, 0) 和 (5, 5)，另一個在 (0, 5)、(0, 0) 和 (5, 5)。</span><span class="sxs-lookup"><span data-stu-id="17ca6-129">The following illustration shows two triangles, one at (0, 0), (5, 0), and (5, 5), and the other at (0, 5), (0, 0), and (5, 5).</span></span> <span data-ttu-id="17ca6-130">在本案例中第一個三角形取得 15 像素 (顯示黑色)，第二個僅取得 10 像素 (顯示灰色)，因為的共用邊是第一個三角形的左邊。</span><span class="sxs-lookup"><span data-stu-id="17ca6-130">The first triangle in this case gets 15 pixels (shown in black), whereas the second gets only 10 pixels (shown in gray) because the shared edge is the left edge of the first triangle.</span></span>

![顯示兩個三角形的編號方塊圖例](images/twotris.png)

<span data-ttu-id="17ca6-132">如果您定義在 (0.5, 0.5) 左上角的矩形，而其右下角在 (2.5, 4.5)，此矩形中心點則在 (1.5, 2.5)。</span><span class="sxs-lookup"><span data-stu-id="17ca6-132">If you define a rectangle with its upper-left corner at (0.5, 0.5) and its lower-right corner at (2.5, 4.5), the center point of this rectangle is at (1.5, 2.5).</span></span> <span data-ttu-id="17ca6-133">當 Direct3D 點陣化將這個矩形切成方格時，每個像素中心均明確地位於四個三角形的每個三角形內，不需要左上角填充慣例。</span><span class="sxs-lookup"><span data-stu-id="17ca6-133">When the Direct3D rasterizer tessellates this rectangle, the center of each pixel is unambiguously inside each of the four triangles, and the top-left filling convention is not needed.</span></span> <span data-ttu-id="17ca6-134">下圖顯示此項。</span><span class="sxs-lookup"><span data-stu-id="17ca6-134">The following illustration shows this.</span></span> <span data-ttu-id="17ca6-135">矩形中的像素依據 Direct3D 包含像素的三角形中標示。</span><span class="sxs-lookup"><span data-stu-id="17ca6-135">The pixels in the rectangle are labeled according to the triangle in which Direct3D includes them.</span></span>

![顯示編號的方形，其中包含的矩形會分成四個三角形。](images/noambig.png)

<span data-ttu-id="17ca6-137">如果您移動前述圖中的矩形，其左上角便會在 (1.0, 1.0)，其右下角在 (3.0, 5.0)，而其中心點在 (2.0, 3.0)，Direct3D 會套用左上角填充慣例。</span><span class="sxs-lookup"><span data-stu-id="17ca6-137">If you move the rectangle in the preceding illustration so that its upper-left corner is at (1.0, 1.0), its lower-right corner at (3.0, 5.0), and its center point at (2.0, 3.0), Direct3D applies the top-left filling convention.</span></span> <span data-ttu-id="17ca6-138">此矩形中的大多數像素跨兩個或更多三角形間的邊界，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="17ca6-138">Most pixels in this rectangle straddle the border between two or more triangles, as the following illustration shows.</span></span>

![編號方塊的圖例，其中包含分成四個三角形的矩形](images/fillrule.png)

<span data-ttu-id="17ca6-140">針對這兩個矩形，同一個像素會受到影響，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="17ca6-140">For both rectangles, the same pixels are affected, as shown in the following illustration.</span></span>

![由前面兩個編號方塊影響的圖元圖例](images/samepix.png)

## <a name="point-and-line-rules"></a><span data-ttu-id="17ca6-142">點和行規則</span><span class="sxs-lookup"><span data-stu-id="17ca6-142">Point and Line Rules</span></span>

<span data-ttu-id="17ca6-143">點的呈現與點精靈相同，兩者均呈現為對齊螢幕的四邊形，因此遵守和多邊形著色演算相同的規則。</span><span class="sxs-lookup"><span data-stu-id="17ca6-143">Points are rendered the same as point sprites, which are both rendered as screen-aligned quadrilaterals and thus adhere to the same rules as polygon rendering.</span></span>

<span data-ttu-id="17ca6-144">非平滑化行轉譯規則確實和是[GDI 行](../gdi/lines.md)一樣。</span><span class="sxs-lookup"><span data-stu-id="17ca6-144">Non-antialiased line rendering rules are exactly the same as those for [GDI lines](../gdi/lines.md).</span></span>

<span data-ttu-id="17ca6-145">如需反鋸齒線轉譯的詳細資訊，請參閱 [**ID3DXLine**](id3dxline.md)。</span><span class="sxs-lookup"><span data-stu-id="17ca6-145">For information about antialiased line rendering, see [**ID3DXLine**](id3dxline.md).</span></span>

## <a name="point-sprite-rules"></a><span data-ttu-id="17ca6-146">點精靈規則</span><span class="sxs-lookup"><span data-stu-id="17ca6-146">Point Sprite Rules</span></span>

<span data-ttu-id="17ca6-147">點精靈和修補程式的基本類型，就好像基本類型第一次鑲嵌至三角形，而結果三角形點陣被點陣化。</span><span class="sxs-lookup"><span data-stu-id="17ca6-147">Point sprites and patch primitives are rasterized as if the primitives were first tessellated into triangles and the resulting triangles rasterized.</span></span> <span data-ttu-id="17ca6-148">如需詳細資訊，請參閱 [點 sprite (Direct3D 9) ](point-sprites.md)。</span><span class="sxs-lookup"><span data-stu-id="17ca6-148">For more information, see [Point Sprites (Direct3D 9)](point-sprites.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="17ca6-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="17ca6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17ca6-150">座標系統和幾何</span><span class="sxs-lookup"><span data-stu-id="17ca6-150">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
