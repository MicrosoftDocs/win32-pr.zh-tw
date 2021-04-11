---
description: VMR 中的座標組應
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: VMR 中的座標組應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c18b38249471e6e68e36f1b9051f51e920f62b31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846008"
---
# <a name="coordinate-mapping-in-the-vmr"></a><span data-ttu-id="dca94-103">VMR 中的座標組應</span><span class="sxs-lookup"><span data-stu-id="dca94-103">Coordinate Mapping in the VMR</span></span>

<span data-ttu-id="dca94-104">本節說明在 VMR 將其對應至最終輸出影像之前，套用至來源映射的五個轉換。</span><span class="sxs-lookup"><span data-stu-id="dca94-104">This section describes the five transformations that are applied to a source image before it is mapped by the VMR onto the final output image.</span></span>

1.  <span data-ttu-id="dca94-105">轉換 *T (Src)* 將來源矩形對應至目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="dca94-105">The transformation *T(Src)* maps the source rectangle to the destination rectangle.</span></span> <span data-ttu-id="dca94-106">這些是由媒體類型中 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)或 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)結構的 **rcSource** 和 **rcTarget** 成員所指定。</span><span class="sxs-lookup"><span data-stu-id="dca94-106">These are specified by the **rcSource** and **rcTarget** members of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure in the media type.</span></span> <span data-ttu-id="dca94-107">此對應會在傳遞至 VMR 時，將來源影像進行前置處理。</span><span class="sxs-lookup"><span data-stu-id="dca94-107">This mapping preprocesses the source image as it passes to the VMR.</span></span>
2.  <span data-ttu-id="dca94-108">轉換 *T (旗標)* 執行媒體範例中的旗標所指定的任何影像操作。</span><span class="sxs-lookup"><span data-stu-id="dca94-108">The transformation *T(Flag)* performs any image manipulations specified by flags in the media sample.</span></span> <span data-ttu-id="dca94-109">這些包含的轉換（例如垂直轉譯和尺規）可容納 bob 交錯旗標。</span><span class="sxs-lookup"><span data-stu-id="dca94-109">These included transformations such as the vertical translation and scale to accommodate the bob interlace flags.</span></span> <span data-ttu-id="dca94-110">交錯轉換會將影像高度加倍，而且可能會將影像轉譯成非奇數位段中的一半的影片線。</span><span class="sxs-lookup"><span data-stu-id="dca94-110">The interlace transformation doubles the image height and possibly translates the image by half of a video line if it is in the odd field.</span></span>
3.  <span data-ttu-id="dca94-111">轉換 *T (AR)* 會根據影像外觀比例，將影像調整為正方形圖元。</span><span class="sxs-lookup"><span data-stu-id="dca94-111">The transformation *T(AR)* adjusts the image to square pixels, based on the image aspect ratio.</span></span> <span data-ttu-id="dca94-112">針對 **VIDEOINFOHEADER** 媒體類型，外觀比例取決於影像大小。</span><span class="sxs-lookup"><span data-stu-id="dca94-112">For **VIDEOINFOHEADER** media types, the aspect ratio is determined by the image size.</span></span> <span data-ttu-id="dca94-113">針對 **VIDEOINFOHEADER2** 類型，外觀比例取決於 **dwPictAspectRatioX** 和 **dwPictAspectRatioY** 欄位，除非 \_ \_ 已設定 AMCONTROL PAD to \_ 16x9 或 AMCONTROL \_ PAD \_ to \_ 4x3 旗標。</span><span class="sxs-lookup"><span data-stu-id="dca94-113">For **VIDEOINFOHEADER2** types, the aspect ratio is determined by the **dwPictAspectRatioX** and **dwPictAspectRatioY** fields, unless the AMCONTROL\_PAD\_TO\_16x9 or AMCONTROL\_PAD\_TO\_4x3 flags are set.</span></span> <span data-ttu-id="dca94-114">這項轉換假設監視器顯示設定符合監視的實體外觀比例。</span><span class="sxs-lookup"><span data-stu-id="dca94-114">This transformation assumes that the monitor display setting matches the physical aspect ratio of the monitor.</span></span> <span data-ttu-id="dca94-115">例如，如果使用者具有具有 4 x 3 外觀比例的監視器，但將顯示器設定為 1280 x 768 圖元 (5 x 3) ，則影像將沒有正確的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="dca94-115">For example, if the user has a monitor with 4 x 3 aspect ratio, but sets the display to 1280 x 768 pixels (5 x 3), the image will not have the correct aspect ratio.</span></span>
4.  <span data-ttu-id="dca94-116">轉換 *T (混合)* 轉換會使用 [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) 方法中指定的正規化矩形，在目的影像內放置影像。</span><span class="sxs-lookup"><span data-stu-id="dca94-116">The transformation *T(Mix)* transforms positions the image within the destination image, using the normalized rectangles specified in the [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) methods.</span></span> <span data-ttu-id="dca94-117">正規化的矩形可讓應用程式組織來來源資料流的放置和縮放方式（相對於彼此）。</span><span class="sxs-lookup"><span data-stu-id="dca94-117">The normalized rectangles enable the application to organize how the source streams are positioned and scaled relative to each other.</span></span> <span data-ttu-id="dca94-118">VMR 藉由計算所有來源影像的最大尺寸，並將每個影像集中在整體周框內，來計算目的影像。</span><span class="sxs-lookup"><span data-stu-id="dca94-118">The VMR computes the destination image by computing the maximum dimensions of all the source images and centering each inside an overall bounding rectangle.</span></span> <span data-ttu-id="dca94-119">周框的邊角會被指派範圍 (0，0) 至 (1，1) 。</span><span class="sxs-lookup"><span data-stu-id="dca94-119">The corners of the bounding rectangle are assigned the range (0,0) to (1,1).</span></span> <span data-ttu-id="dca94-120">在圖形執行之前，周框是固定的，而且即使已新增或刪除資料流程，也會維持不變。</span><span class="sxs-lookup"><span data-stu-id="dca94-120">The bounding rectangle is fixed before the graph runs and remains constant even if streams are added or deleted.</span></span> <span data-ttu-id="dca94-121">每個資料流程的目的地矩形可以位於範圍 (0、0) 至 (1、1) ，而且仍然有效。</span><span class="sxs-lookup"><span data-stu-id="dca94-121">Destination rectangles for each stream can lie outside of the range (0,0) to (1,1) and still be valid.</span></span>
5.  <span data-ttu-id="dca94-122">最後，混合影像的一部分可以由對應 *T (Dst)*（由 VMR 的 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面中的來源和目的地矩形所指定）進行轉換。</span><span class="sxs-lookup"><span data-stu-id="dca94-122">Finally, a portion of the mixed image can be transformed by the mapping *T(Dst)*, specified by the source and destination rectangles in the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface on the VMR.</span></span> <span data-ttu-id="dca94-123">如果 Allocator-Presenter 已被取代，而且未使用 **IBasicVideo** 介面，應用程式必須執行 [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) 介面，並將座標組應回2d 線性空間。</span><span class="sxs-lookup"><span data-stu-id="dca94-123">If the Allocator-Presenter is replaced and the **IBasicVideo** interface is not used, the application must implement the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface and map the coordinates back into a 2D linear space.</span></span> <span data-ttu-id="dca94-124">傳回至 DVD 導覽器的滑鼠座標也必須在此空間中。</span><span class="sxs-lookup"><span data-stu-id="dca94-124">The mouse coordinates returned to the DVD navigator must also be in this space.</span></span> <span data-ttu-id="dca94-125">例如，如果應用程式將影片轉譯為旋轉立方體，則會回報無視窗控制項的整個顯示，並傳回相對於顯示器的滑鼠座標。</span><span class="sxs-lookup"><span data-stu-id="dca94-125">For example, if an application renders video onto a spinning cube, they would report back the entire display for the windowless control and return mouse coordinates relative to the display.</span></span>

<span data-ttu-id="dca94-126">從來源資料到最終轉譯器的整體影像轉換如下：</span><span class="sxs-lookup"><span data-stu-id="dca94-126">The overall image transformation from the source data to the final renderer is:</span></span>

<span data-ttu-id="dca94-127">T = T (Src) \* t (旗標) T (Ar) t (混合) \* t (Dst) \*</span><span class="sxs-lookup"><span data-stu-id="dca94-127">T = T(Src)\* T(Flag)T(Ar)T(Mix)\* T(Dst)\*</span></span>

<span data-ttu-id="dca94-128">其中 \* 指出映射可以裁剪至該階段的目的地影像。</span><span class="sxs-lookup"><span data-stu-id="dca94-128">where \* indicates that the image could be clipped to the destination image at that stage.</span></span> <span data-ttu-id="dca94-129">請注意，這些都是仿射轉換，所以 VMR 可以將它們合併成單一轉換。</span><span class="sxs-lookup"><span data-stu-id="dca94-129">Note that these are all affine transformations, so the VMR can combine them into a single transformation.</span></span>

<span data-ttu-id="dca94-130">轉換的反向為：</span><span class="sxs-lookup"><span data-stu-id="dca94-130">The inverse of the transformation is:</span></span>

![反向轉換](images/vmrmapping-t-1.png)

<span data-ttu-id="dca94-132"> (Src 的因數 T) T (旗標) T (Ar) 相對於來源解析。</span><span class="sxs-lookup"><span data-stu-id="dca94-132">The factor T(Src) T(Flag) T(Ar) is relative to the source resolution.</span></span> <span data-ttu-id="dca94-133">在因數 T (混合) 中，正規化來源矩形相對於外觀更正影像。</span><span class="sxs-lookup"><span data-stu-id="dca94-133">In the factor T(Mix), the normalized source rectangle is relative to the aspect-corrected image.</span></span> <span data-ttu-id="dca94-134">正規化的目的地矩形相對於輸出解析度。</span><span class="sxs-lookup"><span data-stu-id="dca94-134">The normalized destination rectangle is relative to the output resolution.</span></span> <span data-ttu-id="dca94-135">下圖顯示這些關聯性。</span><span class="sxs-lookup"><span data-stu-id="dca94-135">The following diagram shows these relationships.</span></span>

![映射轉換步驟](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a><span data-ttu-id="dca94-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="dca94-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dca94-138">使用 VMR 來進行 DirectShow 篩選器開發人員</span><span class="sxs-lookup"><span data-stu-id="dca94-138">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



