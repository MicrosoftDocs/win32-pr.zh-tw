---
description: 本主題說明兩個相關的概念、圖片外觀比例和圖元外觀比例。
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: 圖片外觀比例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191764"
---
# <a name="picture-aspect-ratio"></a><span data-ttu-id="98ec3-103">圖片外觀比例</span><span class="sxs-lookup"><span data-stu-id="98ec3-103">Picture Aspect Ratio</span></span>

<span data-ttu-id="98ec3-104">本主題說明兩個相關的概念、圖片外觀比例和圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="98ec3-104">This topic describes two related concepts, picture aspect ratio and pixel aspect ratio.</span></span> <span data-ttu-id="98ec3-105">接著，它會說明如何使用媒體類型在 Microsoft 媒體基礎中表示這些概念。</span><span class="sxs-lookup"><span data-stu-id="98ec3-105">It then describes how these concepts are expressed in Microsoft Media Foundation using media types.</span></span>

-   [<span data-ttu-id="98ec3-106">圖片外觀比例</span><span class="sxs-lookup"><span data-stu-id="98ec3-106">Picture Aspect Ratio</span></span>](#picture-aspect-ratio)
    -   [<span data-ttu-id="98ec3-107">上下黑邊縮</span><span class="sxs-lookup"><span data-stu-id="98ec3-107">Letterboxing</span></span>](#letterboxing)
    -   [<span data-ttu-id="98ec3-108">平移和掃描</span><span class="sxs-lookup"><span data-stu-id="98ec3-108">Pan-and-Scan</span></span>](#pan-and-scan)
-   [<span data-ttu-id="98ec3-109">圖元外觀比例</span><span class="sxs-lookup"><span data-stu-id="98ec3-109">Pixel Aspect Ratio</span></span>](#pixel-aspect-ratio)
-   [<span data-ttu-id="98ec3-110">使用外觀比例</span><span class="sxs-lookup"><span data-stu-id="98ec3-110">Working with Aspect Ratios</span></span>](#working-with-aspect-ratios)
-   [<span data-ttu-id="98ec3-111">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="98ec3-111">Code Examples</span></span>](#code-examples)
    -   [<span data-ttu-id="98ec3-112">尋找顯示區域</span><span class="sxs-lookup"><span data-stu-id="98ec3-112">Finding the Display Area</span></span>](#finding-the-display-area)
    -   [<span data-ttu-id="98ec3-113">圖元外觀比例之間的轉換</span><span class="sxs-lookup"><span data-stu-id="98ec3-113">Converting Between Pixel Aspect Ratios</span></span>](#converting-between-pixel-aspect-ratios)
    -   [<span data-ttu-id="98ec3-114">計算黑邊區域</span><span class="sxs-lookup"><span data-stu-id="98ec3-114">Calculating the Letterbox Area</span></span>](#calculating-the-letterbox-area)
-   [<span data-ttu-id="98ec3-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="98ec3-115">Related topics</span></span>](#related-topics)

## <a name="picture-aspect-ratio"></a><span data-ttu-id="98ec3-116">圖片外觀比例</span><span class="sxs-lookup"><span data-stu-id="98ec3-116">Picture Aspect Ratio</span></span>

<span data-ttu-id="98ec3-117">*圖片外觀比例* 會定義所顯示影片影像的形狀。</span><span class="sxs-lookup"><span data-stu-id="98ec3-117">*Picture aspect ratio* defines the shape of the displayed video image.</span></span> <span data-ttu-id="98ec3-118">圖片外觀比例為 X:Y，其中 X:Y 是圖片寬度與圖片高度的比例。</span><span class="sxs-lookup"><span data-stu-id="98ec3-118">Picture aspect ratio is notated X:Y, where X:Y is the ratio of picture width to picture height.</span></span> <span data-ttu-id="98ec3-119">大部分的影片標準都使用4:3 或16:9 圖片外觀比例。</span><span class="sxs-lookup"><span data-stu-id="98ec3-119">Most video standards use either 4:3 or 16:9 picture aspect ratio.</span></span> <span data-ttu-id="98ec3-120">16:9 外觀比例通常稱為 *寬螢幕*。</span><span class="sxs-lookup"><span data-stu-id="98ec3-120">The 16:9 aspect ratio is commonly called *widescreen*.</span></span> <span data-ttu-id="98ec3-121">電影院電影通常會使用1:85:1 或1:66:1 外觀比例。</span><span class="sxs-lookup"><span data-stu-id="98ec3-121">Cinema film often uses a 1:85:1 or 1:66:1 aspect ratio.</span></span> <span data-ttu-id="98ec3-122">圖片外觀比例也稱為 *顯示外觀比例* (DAR) 。</span><span class="sxs-lookup"><span data-stu-id="98ec3-122">Picture aspect ratio is also called *display aspect ratio* (DAR).</span></span>

![顯示4:3 和16:9 外觀比例的圖表](images/aspect-ratio01.png)

<span data-ttu-id="98ec3-124">影片影像有時與顯示區域沒有相同的圖形。</span><span class="sxs-lookup"><span data-stu-id="98ec3-124">Sometimes the video image does not have the same shape as the display area.</span></span> <span data-ttu-id="98ec3-125">例如，4:3 的影片可能會顯示在寬屏 (16 × 9) 電視上。</span><span class="sxs-lookup"><span data-stu-id="98ec3-125">For example, a 4:3 video might be shown on a widescreen (16×9) television.</span></span> <span data-ttu-id="98ec3-126">在「電腦影片」中，影片可能會顯示在具有任意大小的視窗內。</span><span class="sxs-lookup"><span data-stu-id="98ec3-126">In computer video, the video might be shown inside a window that has an arbitrary size.</span></span> <span data-ttu-id="98ec3-127">在這種情況下，您可以透過三種方式來使影像符合顯示區域：</span><span class="sxs-lookup"><span data-stu-id="98ec3-127">In that case, there are three ways the image can be made to fit within the display area:</span></span>

-   <span data-ttu-id="98ec3-128">沿著一個軸伸展影像以符合顯示區域。</span><span class="sxs-lookup"><span data-stu-id="98ec3-128">Stretch the image along one axis to fit the display area.</span></span>
-   <span data-ttu-id="98ec3-129">調整影像以符合顯示區域，同時維持原始圖片的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="98ec3-129">Scale the image to fit the display area, while maintaining the original picture aspect ratio.</span></span>
-   <span data-ttu-id="98ec3-130">裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="98ec3-130">Crop the image.</span></span>

<span data-ttu-id="98ec3-131">將影像延展成適合顯示區域幾乎都是錯誤的，因為它不會保留正確的圖片外觀比例。</span><span class="sxs-lookup"><span data-stu-id="98ec3-131">Stretching the image to fit the display area is almost always wrong, because it does not preserve the correct picture aspect ratio.</span></span>

### <a name="letterboxing"></a><span data-ttu-id="98ec3-132">上下黑邊縮</span><span class="sxs-lookup"><span data-stu-id="98ec3-132">Letterboxing</span></span>

<span data-ttu-id="98ec3-133">調整寬螢幕影像以符合4:3 顯示器的程式稱為 *上下黑邊縮*，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="98ec3-133">The process of scaling a widescreen image to fit a 4:3 display is called *letterboxing*, shown in the next diagram.</span></span> <span data-ttu-id="98ec3-134">影像頂端和底部的結果 rectanglular 區域通常會填滿黑色，雖然可以使用其他色彩。</span><span class="sxs-lookup"><span data-stu-id="98ec3-134">The resulting rectanglular areas at the top and bottom of the image are typically filled with black, although other colors can be used.</span></span>

![顯示正確黑邊方式的圖表](images/aspect-ratio02.png)

<span data-ttu-id="98ec3-136">相反地，調整4:3 影像以符合寬螢幕顯示器的情況，有時也稱為 *pillarboxing*。</span><span class="sxs-lookup"><span data-stu-id="98ec3-136">The reverse case, scaling a 4:3 image to fit a widescreen display, is sometimes called *pillarboxing*.</span></span> <span data-ttu-id="98ec3-137">不過， *黑邊* 一詞也會用來表示調整影片影像以符合任何指定的顯示區域。</span><span class="sxs-lookup"><span data-stu-id="98ec3-137">However, the term *letterbox* is also used in a general sense, to mean scaling a video image to fit any given display area.</span></span>

![顯示 pillarboxing 的圖表](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a><span data-ttu-id="98ec3-139">平移和掃描</span><span class="sxs-lookup"><span data-stu-id="98ec3-139">Pan-and-Scan</span></span>

<span data-ttu-id="98ec3-140">移動流覽和掃描是一種技術，可將寬螢幕影像裁剪成4×3矩形區域，以顯示于4:3 顯示裝置上。</span><span class="sxs-lookup"><span data-stu-id="98ec3-140">Pan-and-scan is a technique whereby a widescreen image is cropped to a 4×3 rectangular area, for display on a 4:3 display device.</span></span> <span data-ttu-id="98ec3-141">產生的影像會填滿整個顯示器，而不需要黑色黑邊的區域，而原始影像的部分則會裁剪掉。</span><span class="sxs-lookup"><span data-stu-id="98ec3-141">The resulting image fills the entire display, without requiring black letterbox areas, but portions of the original image are cropped out of the picture.</span></span> <span data-ttu-id="98ec3-142">裁剪的區域可以從畫面格移至框架，如同感興趣的區域。</span><span class="sxs-lookup"><span data-stu-id="98ec3-142">The area that is cropped can move from frame to frame, as the area of interest shifts.</span></span> <span data-ttu-id="98ec3-143">*平移和掃描* 中的「移動流覽」一詞是指移動移動流覽和掃描區域所造成的移動流覽效果。</span><span class="sxs-lookup"><span data-stu-id="98ec3-143">The term "pan" in *pan-and-scan* refers to the panning effect that is caused by moving the pan-and-scan area.</span></span>

![顯示平移和掃描的圖表](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a><span data-ttu-id="98ec3-145">圖元外觀比例</span><span class="sxs-lookup"><span data-stu-id="98ec3-145">Pixel Aspect Ratio</span></span>

<span data-ttu-id="98ec3-146">*圖元外觀比例* (PAR) 測量圖元的形狀。</span><span class="sxs-lookup"><span data-stu-id="98ec3-146">*Pixel aspect ratio* (PAR) measures the shape of a pixel.</span></span>

<span data-ttu-id="98ec3-147">當您捕獲數位映射時，會以垂直和水準方式取樣影像，產生量化範例的矩形陣列，稱為 *圖元* 或 *pels*。</span><span class="sxs-lookup"><span data-stu-id="98ec3-147">When a digital image is captured, the image is sampled both vertically and horizontally, resulting in a rectangular array of quantized samples, called *pixels* or *pels*.</span></span> <span data-ttu-id="98ec3-148">取樣方格的形狀決定了數位化影像中圖元的形狀。</span><span class="sxs-lookup"><span data-stu-id="98ec3-148">The shape of the sampling grid determines the shape of the pixels in the digitized image.</span></span>

<span data-ttu-id="98ec3-149">以下範例會使用較小的數位來簡化數學運算。</span><span class="sxs-lookup"><span data-stu-id="98ec3-149">Here is an example that uses small numbers to keep the math simple.</span></span> <span data-ttu-id="98ec3-150">假設原始影像是正方形 (也就是說，圖片的外觀比例為 1:1) ;並假設取樣方格包含12個元素，並以4×3方格排列。</span><span class="sxs-lookup"><span data-stu-id="98ec3-150">Suppose that the original image is square (that is, the picture aspect ratio is 1:1); and suppose the sampling grid contains 12 elements, arranged in a 4×3 grid.</span></span> <span data-ttu-id="98ec3-151">每個產生圖元的形狀將會高於寬度。</span><span class="sxs-lookup"><span data-stu-id="98ec3-151">The shape of each resulting pixel will be taller than it is wide.</span></span> <span data-ttu-id="98ec3-152">具體而言，每個圖元的形狀將會是3×4。</span><span class="sxs-lookup"><span data-stu-id="98ec3-152">Specifically, the shape of each pixel will be 3×4.</span></span> <span data-ttu-id="98ec3-153">非正方形的圖元稱為 *非正方形圖元*。</span><span class="sxs-lookup"><span data-stu-id="98ec3-153">Pixels that are not square are called *non-square pixels*.</span></span>

![顯示非方形取樣方格的圖表](images/aspect-ratio05.png)

<span data-ttu-id="98ec3-155">圖元外觀比例也適用于顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="98ec3-155">Pixel aspect ratio also applies to the display device.</span></span> <span data-ttu-id="98ec3-156">顯示裝置和實體圖元解析度 (的實體圖形，) 判斷顯示裝置的範圍。</span><span class="sxs-lookup"><span data-stu-id="98ec3-156">The physical shape of the display device and the physical pixel resolution (across and down) determine the PAR of the display device.</span></span> <span data-ttu-id="98ec3-157">電腦監視器通常使用正方形圖元。</span><span class="sxs-lookup"><span data-stu-id="98ec3-157">Computer monitors generally use square pixels.</span></span> <span data-ttu-id="98ec3-158">如果影像相等且顯示的不相符，則必須以垂直或水準方式調整影像的大小，才能正確顯示。</span><span class="sxs-lookup"><span data-stu-id="98ec3-158">If the image PAR and the display PAR do not match, the image must be scaled in one dimension, either vertically or horizontally, in order to display correctly.</span></span> <span data-ttu-id="98ec3-159">下列公式的關聯等同、顯示外觀比例 (DAR) 和影像大小（以圖元為單位）：</span><span class="sxs-lookup"><span data-stu-id="98ec3-159">The following formula relates PAR, display aspect ratio (DAR), and image size in pixels:</span></span>

<span data-ttu-id="98ec3-160">*DAR* = (*影像寬度（以* 圖元為單位）  /  *影像高度（圖元）*) × *PAR*</span><span class="sxs-lookup"><span data-stu-id="98ec3-160">*DAR* = (*image width in pixels* / *image height in pixels*) × *PAR*</span></span>

<span data-ttu-id="98ec3-161">請注意，此公式中的影像寬度和影像高度會參考記憶體中的影像，而不是所顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="98ec3-161">Note that image width and image height in this formula refer to the image in memory, not the displayed image.</span></span>

<span data-ttu-id="98ec3-162">以下是真實世界的範例： NTSC-M 類比影片包含使用中影像區域的480掃描行。</span><span class="sxs-lookup"><span data-stu-id="98ec3-162">Here is a real-world example: NTSC-M analog video contains 480 scan lines in the active image area.</span></span> <span data-ttu-id="98ec3-163">ITU-R Rec 指定水準取樣率為每行704個可見的圖元，並產生具有 704 x 480 圖元的數位影像。</span><span class="sxs-lookup"><span data-stu-id="98ec3-163">ITU-R Rec. BT.601 specifies a horizontal sampling rate of 704 visible pixels per line, yielding a digital image with 704 x 480 pixels.</span></span> <span data-ttu-id="98ec3-164">預期的圖片外觀比例為4:3，而產生的是10:11。</span><span class="sxs-lookup"><span data-stu-id="98ec3-164">The intended picture aspect ratio is 4:3, yielding a PAR of 10:11.</span></span>

-   <span data-ttu-id="98ec3-165">DAR：4:3</span><span class="sxs-lookup"><span data-stu-id="98ec3-165">DAR: 4:3</span></span>
-   <span data-ttu-id="98ec3-166">寬度（以圖元為單位）：704</span><span class="sxs-lookup"><span data-stu-id="98ec3-166">Width in pixels: 704</span></span>
-   <span data-ttu-id="98ec3-167">高度（以圖元為單位）：480</span><span class="sxs-lookup"><span data-stu-id="98ec3-167">Height in pixels: 480</span></span>
-   <span data-ttu-id="98ec3-168">PAR：10/11</span><span class="sxs-lookup"><span data-stu-id="98ec3-168">PAR: 10/11</span></span>

<span data-ttu-id="98ec3-169">4/3 = (704/420) x (10/11) </span><span class="sxs-lookup"><span data-stu-id="98ec3-169">4/3 = (704/420) x (10/11)</span></span>

<span data-ttu-id="98ec3-170">若要在具有正方形圖元的顯示裝置上正確地顯示此影像，您必須將寬度調整為10/11 或依11/10 的高度。</span><span class="sxs-lookup"><span data-stu-id="98ec3-170">To display this image correctly on a display device with square pixels, you must scale either the width by 10/11 or the height by 11/10.</span></span>

## <a name="working-with-aspect-ratios"></a><span data-ttu-id="98ec3-171">使用外觀比例</span><span class="sxs-lookup"><span data-stu-id="98ec3-171">Working with Aspect Ratios</span></span>

<span data-ttu-id="98ec3-172">影片框架的正確圖形是以 *圖元外觀比例* 定義 (PAR) 和 *顯示區域*。</span><span class="sxs-lookup"><span data-stu-id="98ec3-172">The correct shape of a video frame is defined by the *pixel aspect ratio* (PAR) and the *display area*.</span></span>

-   <span data-ttu-id="98ec3-173">等同定義影像中圖元的形狀。</span><span class="sxs-lookup"><span data-stu-id="98ec3-173">The PAR defines the shape of the pixels in an image.</span></span> <span data-ttu-id="98ec3-174">正方形圖元的外觀比例為1:1。</span><span class="sxs-lookup"><span data-stu-id="98ec3-174">Square pixels have an aspect ratio of 1:1.</span></span> <span data-ttu-id="98ec3-175">任何其他外觀比例都會描述非正方形圖元。</span><span class="sxs-lookup"><span data-stu-id="98ec3-175">Any other aspect ratio describes a non-square pixel.</span></span> <span data-ttu-id="98ec3-176">例如，NTSC 電視使用10:11。</span><span class="sxs-lookup"><span data-stu-id="98ec3-176">For example, NTSC television uses a 10:11 PAR.</span></span> <span data-ttu-id="98ec3-177">假設您要在電腦監視器上呈現影片，顯示器的 (1:1 PAR) 的正方形圖元。</span><span class="sxs-lookup"><span data-stu-id="98ec3-177">Assuming that you are presenting the video on a computer monitor, the display will have square pixels (1:1 PAR).</span></span> <span data-ttu-id="98ec3-178">在媒體類型上的 [ [**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**](mf-mt-pixel-aspect-ratio-attribute.md) ] 屬性中，會提供來源內容的等同部分。</span><span class="sxs-lookup"><span data-stu-id="98ec3-178">The PAR of the source content is given in the [**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute on the media type.</span></span>
-   <span data-ttu-id="98ec3-179">顯示區域是要顯示之影片影像的區域。</span><span class="sxs-lookup"><span data-stu-id="98ec3-179">The display area is the region of the video image that is intended to be shown.</span></span> <span data-ttu-id="98ec3-180">媒體類型中可能會指定兩個相關的顯示區域：</span><span class="sxs-lookup"><span data-stu-id="98ec3-180">There are two relevant display areas that might be specified in the media type:</span></span>
    -   <span data-ttu-id="98ec3-181">平移和掃描光圈。</span><span class="sxs-lookup"><span data-stu-id="98ec3-181">Pan-and-scan aperture.</span></span> <span data-ttu-id="98ec3-182">移動流覽和掃描光圈是一部影片的4×3區域，應以平移/掃描模式顯示。</span><span class="sxs-lookup"><span data-stu-id="98ec3-182">The pan-and-scan aperture is a 4×3 region of video that should be displayed in pan/scan mode.</span></span> <span data-ttu-id="98ec3-183">它是用來在沒有上下黑邊縮的情況下，顯示4×3顯示器上的寬螢幕內容。</span><span class="sxs-lookup"><span data-stu-id="98ec3-183">It is used to show wide-screen content on a 4×3 display without letterboxing.</span></span> <span data-ttu-id="98ec3-184">[移動流覽] 和 [掃描] 光圈是在 [ [**mf \_ mt \_ 平移 \_ 掃描 \_**](mf-mt-pan-scan-aperture-attribute.md) ] 屬性中提供，只有在 [ [**mf \_ Mt \_ 平移 \_ 掃描 \_ 已啟用**](mf-mt-pan-scan-enabled-attribute.md) ] 屬性為 **TRUE** 時才會使用。</span><span class="sxs-lookup"><span data-stu-id="98ec3-184">The pan-and-scan aperture is given in the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute and should be used only when the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute is **TRUE**.</span></span>
    -   <span data-ttu-id="98ec3-185">顯示光圈。</span><span class="sxs-lookup"><span data-stu-id="98ec3-185">Display aperture.</span></span> <span data-ttu-id="98ec3-186">這個光圈是以部分影片標準定義。</span><span class="sxs-lookup"><span data-stu-id="98ec3-186">This aperture is defined in some video standards.</span></span> <span data-ttu-id="98ec3-187">顯示光圈以外的任何地方都是 overscan 區域，不應該顯示。</span><span class="sxs-lookup"><span data-stu-id="98ec3-187">Anything outside of the display aperture is the overscan region and should not be displayed.</span></span> <span data-ttu-id="98ec3-188">例如，NTSC 電視為720×480圖元，顯示口徑為704×480。</span><span class="sxs-lookup"><span data-stu-id="98ec3-188">For example, NTSC television is 720×480 pixels with a display aperture of 704×480.</span></span> <span data-ttu-id="98ec3-189">您可以在 [**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**](mf-mt-minimum-display-aperture-attribute.md) 屬性中指定顯示光圈。</span><span class="sxs-lookup"><span data-stu-id="98ec3-189">The display aperture is given in the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span> <span data-ttu-id="98ec3-190">如果有的話，則應該在平移和掃描模式為 **FALSE** 時使用。</span><span class="sxs-lookup"><span data-stu-id="98ec3-190">If present, it should be used when pan-and-scan mode is **FALSE**.</span></span>

<span data-ttu-id="98ec3-191">如果平移和可以模式為 **FALSE** ，且未定義顯示光圈，則應該會顯示整個影片畫面。</span><span class="sxs-lookup"><span data-stu-id="98ec3-191">If pan-and-can mode is **FALSE** and no display aperture is defined, the entire video frame should be displayed.</span></span> <span data-ttu-id="98ec3-192">事實上，除了電視和 DVD 影片之外，大部分的影片內容都是如此。</span><span class="sxs-lookup"><span data-stu-id="98ec3-192">In fact, this is the case for most video content other than television and DVD video.</span></span> <span data-ttu-id="98ec3-193">整個圖片的外觀比例會計算為 (*顯示區域寬度*  /  *顯示區域高度*) ×等於。 </span><span class="sxs-lookup"><span data-stu-id="98ec3-193">The aspect ratio of the entire picture is calculated as (*display area width* / *display area height*) × *PAR*.</span></span>

## <a name="code-examples"></a><span data-ttu-id="98ec3-194">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="98ec3-194">Code Examples</span></span>

### <a name="finding-the-display-area"></a><span data-ttu-id="98ec3-195">尋找顯示區域</span><span class="sxs-lookup"><span data-stu-id="98ec3-195">Finding the Display Area</span></span>

<span data-ttu-id="98ec3-196">下列程式碼顯示如何從媒體類型取得顯示區域。</span><span class="sxs-lookup"><span data-stu-id="98ec3-196">The following code shows how to get the display area from the media type.</span></span>


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a><span data-ttu-id="98ec3-197">圖元外觀比例之間的轉換</span><span class="sxs-lookup"><span data-stu-id="98ec3-197">Converting Between Pixel Aspect Ratios</span></span>

<span data-ttu-id="98ec3-198">下列程式碼示範如何將矩形從一個圖元的外觀比例轉換成另一個圖元的外觀比例 (相等的) ，同時保留圖片的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="98ec3-198">The following code shows how to convert a rectangle from one pixel aspect ratio (PAR) to another, while preserving the picture aspect ratio.</span></span>


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a><span data-ttu-id="98ec3-199">計算黑邊區域</span><span class="sxs-lookup"><span data-stu-id="98ec3-199">Calculating the Letterbox Area</span></span>

<span data-ttu-id="98ec3-200">下列程式碼會在給定來源和目的地矩形的情況下，計算黑邊區域。</span><span class="sxs-lookup"><span data-stu-id="98ec3-200">The following code calculates the letterbox area, given a source and destination rectangle.</span></span> <span data-ttu-id="98ec3-201">假設兩個矩形都有相同的 PAR。</span><span class="sxs-lookup"><span data-stu-id="98ec3-201">It is assumed that both rectangles have the same PAR.</span></span>


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a><span data-ttu-id="98ec3-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="98ec3-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98ec3-203">媒體類型</span><span class="sxs-lookup"><span data-stu-id="98ec3-203">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="98ec3-204">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="98ec3-204">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="98ec3-205">**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="98ec3-205">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="98ec3-206">**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="98ec3-206">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="98ec3-207">**\_已啟用 MF MT \_ PAN \_ 掃描 \_**</span><span class="sxs-lookup"><span data-stu-id="98ec3-207">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[<span data-ttu-id="98ec3-208">**MF \_ MT \_ 圖元 \_ 外觀 \_ 比例**</span><span class="sxs-lookup"><span data-stu-id="98ec3-208">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



