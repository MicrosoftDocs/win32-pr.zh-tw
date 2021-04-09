---
title: 影片影像轉換
description: 影片影像轉換
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format SDK、影片影像轉換
- Advanced Systems Format (ASF) 、影片影像轉換
- ASF (Advanced 系統格式) 、影片影像轉換
- 影片影像轉換
- Windows Media 視訊9映射 v2 編解碼器
- 編解碼器，Windows Media 視訊9映射 v2 編解碼器
- 影片串流，Windows Media 視訊9映射 v2 編解碼器
- 影片串流，影像轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021256"
---
# <a name="video-image-transitions"></a><span data-ttu-id="7b75c-111">影片影像轉換</span><span class="sxs-lookup"><span data-stu-id="7b75c-111">Video Image Transitions</span></span>

<span data-ttu-id="7b75c-112">Windows Media 視訊9映射 v2 編解碼器會將一系列的影像動畫，並產生影片串流。</span><span class="sxs-lookup"><span data-stu-id="7b75c-112">The Windows Media Video 9 Image v2 codec animates a series of images, resulting in a video stream.</span></span> <span data-ttu-id="7b75c-113">編解碼器可以一次管理兩個影像，並將它們結合在一起，並根據您所提供的設定，建立從另一個影像轉換。</span><span class="sxs-lookup"><span data-stu-id="7b75c-113">The codec can manipulate two images at once, blending them together and creating a transition from one to the other according to the configuration you supply.</span></span> <span data-ttu-id="7b75c-114">本節說明支援的轉換和它們所需的參數。</span><span class="sxs-lookup"><span data-stu-id="7b75c-114">This section describes the supported transitions and the parameters they require.</span></span>

<span data-ttu-id="7b75c-115">轉換依其全域識別碼列于下表中。</span><span class="sxs-lookup"><span data-stu-id="7b75c-115">The transitions are listed in the following table by their global identifiers.</span></span>



| <span data-ttu-id="7b75c-116">轉換識別碼</span><span class="sxs-lookup"><span data-stu-id="7b75c-116">Transition identifier</span></span>                                                                           | <span data-ttu-id="7b75c-117">Description</span><span class="sxs-lookup"><span data-stu-id="7b75c-117">Description</span></span>                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b75c-118">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 凸起 \_ 系結**</span><span class="sxs-lookup"><span data-stu-id="7b75c-118">**WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE**</span></span>](wmt-videoimage-transition-bow-tie.md)              | <span data-ttu-id="7b75c-119">新的影像會顯示在框架相反邊的一組三角形中。</span><span class="sxs-lookup"><span data-stu-id="7b75c-119">New image is revealed in a set of triangles on opposite sides of the frame.</span></span>                                                                  |
| [<span data-ttu-id="7b75c-120">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 圓形**</span><span class="sxs-lookup"><span data-stu-id="7b75c-120">**WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE**</span></span>](wmt-videoimage-transition-circle.md)                 | <span data-ttu-id="7b75c-121">新的影像會顯示在圓形中。</span><span class="sxs-lookup"><span data-stu-id="7b75c-121">New image is revealed in a circle.</span></span>                                                                                                           |
| [<span data-ttu-id="7b75c-122">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 交叉 \_ 淡化**</span><span class="sxs-lookup"><span data-stu-id="7b75c-122">**WMT\_VIDEOIMAGE\_TRANSITION\_CROSS\_FADE**</span></span>](wmt-videoimage-transition-cross-fade.md)        | <span data-ttu-id="7b75c-123">沒有特殊轉換，這兩個影像的 blend 係數會決定交叉淡化 (溶解) 。</span><span class="sxs-lookup"><span data-stu-id="7b75c-123">No special transition, the blend coefficients of the two images determine the cross-fade (dissolve).</span></span>                                         |
| [<span data-ttu-id="7b75c-124">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 對角線**</span><span class="sxs-lookup"><span data-stu-id="7b75c-124">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL**</span></span>](wmt-videoimage-transition-diagonal.md)             | <span data-ttu-id="7b75c-125">新的影像會沿著框架的一個角落以對角線線顯示。</span><span class="sxs-lookup"><span data-stu-id="7b75c-125">New image is revealed along a diagonal line originating in one corner of the frame.</span></span>                                                          |
| [<span data-ttu-id="7b75c-126">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 鑽石**</span><span class="sxs-lookup"><span data-stu-id="7b75c-126">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND**</span></span>](wmt-videoimage-transition-diamond.md)               | <span data-ttu-id="7b75c-127">新的影像會顯示在菱形中。</span><span class="sxs-lookup"><span data-stu-id="7b75c-127">New image is revealed in a diamond.</span></span>                                                                                                          |
| [<span data-ttu-id="7b75c-128">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 淡化 \_ 成 \_ 色彩**</span><span class="sxs-lookup"><span data-stu-id="7b75c-128">**WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR**</span></span>](wmt-videoimage-transition-fade-to-color.md) | <span data-ttu-id="7b75c-129">從影像到純色框架的溶解。</span><span class="sxs-lookup"><span data-stu-id="7b75c-129">Dissolves from the image to a frame of solid color.</span></span>                                                                                          |
| [<span data-ttu-id="7b75c-130">**WMT \_ VIDEOIMAGE \_ 轉換已 \_ 填滿 \_ V**</span><span class="sxs-lookup"><span data-stu-id="7b75c-130">**WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V**</span></span>](wmt-videoimage-transition-filled-v.md)            | <span data-ttu-id="7b75c-131">新的影像會顯示在來自框架某一端的三角形中。</span><span class="sxs-lookup"><span data-stu-id="7b75c-131">New image is revealed in a triangle originating from one side of the frame.</span></span>                                                                  |
| [<span data-ttu-id="7b75c-132">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 翻轉**</span><span class="sxs-lookup"><span data-stu-id="7b75c-132">**WMT\_VIDEOIMAGE\_TRANSITION\_FLIP**</span></span>](wmt-videoimage-transition-flip.md)                     | <span data-ttu-id="7b75c-133">舊影像會在 y 軸上透過框架的中心旋轉。</span><span class="sxs-lookup"><span data-stu-id="7b75c-133">Old image is rotated on a y-axis through the center of the frame.</span></span> <span data-ttu-id="7b75c-134">新映射會顯示為舊影像的背面。</span><span class="sxs-lookup"><span data-stu-id="7b75c-134">The new image is revealed as the back of the old image.</span></span>                    |
| [<span data-ttu-id="7b75c-135">**WMT \_ VIDEOIMAGE \_ 轉換內 \_ 凹**</span><span class="sxs-lookup"><span data-stu-id="7b75c-135">**WMT\_VIDEOIMAGE\_TRANSITION\_INSET**</span></span>](wmt-videoimage-transition-inset.md)                   | <span data-ttu-id="7b75c-136">新的影像是由框架的一個角落的矩形所顯示。</span><span class="sxs-lookup"><span data-stu-id="7b75c-136">New image is revealed by a rectangle originating from one corner of the frame.</span></span>                                                               |
| [<span data-ttu-id="7b75c-137">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 鳶尾花**</span><span class="sxs-lookup"><span data-stu-id="7b75c-137">**WMT\_VIDEOIMAGE\_TRANSITION\_IRIS**</span></span>](wmt-videoimage-transition-iris.md)                     | <span data-ttu-id="7b75c-138">沿著 X 軸和 y 軸顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="7b75c-138">New image is revealed along an x-axis and a y-axis.</span></span>                                                                                          |
| [<span data-ttu-id="7b75c-139">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 頁面 \_ 滾動**</span><span class="sxs-lookup"><span data-stu-id="7b75c-139">**WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL**</span></span>](wmt-videoimage-transition-page-roll.md)          | <span data-ttu-id="7b75c-140">舊影像會在頁面翻轉效果中轉換，並在下方顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="7b75c-140">Old image is transformed in a page-flipping effect, revealing the new image underneath.</span></span>                                                      |
| [<span data-ttu-id="7b75c-141">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 矩形**</span><span class="sxs-lookup"><span data-stu-id="7b75c-141">**WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE**</span></span>](wmt-videoimage-transition-rectangle.md)           | <span data-ttu-id="7b75c-142">框架內的矩形會顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="7b75c-142">New image is revealed by a rectangle within the frame.</span></span>                                                                                       |
| [<span data-ttu-id="7b75c-143">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="7b75c-143">**WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL**</span></span>](wmt-videoimage-transition-reveal.md)                 | <span data-ttu-id="7b75c-144">新的影像會沿著來自框架一端的直線來顯示。</span><span class="sxs-lookup"><span data-stu-id="7b75c-144">New image is revealed along a straight line originating from one side of the frame.</span></span>                                                          |
| [<span data-ttu-id="7b75c-145">**WMT \_ VIDEOIMAGE \_ 轉換投影 \_ 片**</span><span class="sxs-lookup"><span data-stu-id="7b75c-145">**WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE**</span></span>](wmt-videoimage-transition-slide.md)                   | <span data-ttu-id="7b75c-146">舊的影像會滑出畫面格，並在下方顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="7b75c-146">Old image slides out of the frame, revealing the new image underneath.</span></span>                                                                       |
| [<span data-ttu-id="7b75c-147">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 分割**</span><span class="sxs-lookup"><span data-stu-id="7b75c-147">**WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT**</span></span>](wmt-videoimage-transition-split.md)                   | <span data-ttu-id="7b75c-148">新的影像會顯示在舊影像中的水準或垂直分割。</span><span class="sxs-lookup"><span data-stu-id="7b75c-148">New image is revealed by a horizontal or vertical split in the old image.</span></span> <span data-ttu-id="7b75c-149">分割會沿著框架內的直條顯示。</span><span class="sxs-lookup"><span data-stu-id="7b75c-149">The split appears along a straight line starting inside the frame.</span></span> |
| [<span data-ttu-id="7b75c-150">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 星星**</span><span class="sxs-lookup"><span data-stu-id="7b75c-150">**WMT\_VIDEOIMAGE\_TRANSITION\_STAR**</span></span>](wmt-videoimage-transition-star.md)                     | <span data-ttu-id="7b75c-151">新的影像會顯示在框架內由五個指向的星星。</span><span class="sxs-lookup"><span data-stu-id="7b75c-151">New image is revealed by a five-pointed star inside the frame.</span></span>                                                                               |
| [<span data-ttu-id="7b75c-152">**WMT \_ VIDEOIMAGE \_ 轉換 \_ 輪子**</span><span class="sxs-lookup"><span data-stu-id="7b75c-152">**WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL**</span></span>](wmt-videoimage-transition-wheel.md)                   | <span data-ttu-id="7b75c-153">有四個具有一般軸的旋轉輪輻可顯示新的影像。</span><span class="sxs-lookup"><span data-stu-id="7b75c-153">New image is revealed by four rotating spokes with a common pivot point.</span></span>                                                                     |



 

<span data-ttu-id="7b75c-154">每個轉換都是在它自己的主題中完整說明。</span><span class="sxs-lookup"><span data-stu-id="7b75c-154">Each transition is fully described in its own topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b75c-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b75c-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b75c-156">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="7b75c-156">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="7b75c-157">**WMT \_ VIDEOIMAGE \_ sample2.xml**</span><span class="sxs-lookup"><span data-stu-id="7b75c-157">**WMT\_VIDEOIMAGE\_SAMPLE2**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




