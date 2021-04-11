---
title: 關於 DrawDib 函式
description: 關於 DrawDib 函式
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- Windows (VFW) 的影片，DrawDib
- 適用于 Windows) 的 VFW (影片，DrawDib
- DrawDib，關於
- DrawDib，色彩表
- DrawDib，傳輸模式
- DrawDib，顯示介面卡
- DrawDib，影像延展
- DrawDib，壓縮的影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f3e9ba822e16a7568775378b24f69bbca12de
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682109"
---
# <a name="about-the-drawdib-functions"></a><span data-ttu-id="5f901-111">關於 DrawDib 函式</span><span class="sxs-lookup"><span data-stu-id="5f901-111">About the DrawDib Functions</span></span>

<span data-ttu-id="5f901-112">DrawDib 函式統稱為 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 函式，其提供影像延展和遞色功能。</span><span class="sxs-lookup"><span data-stu-id="5f901-112">Collectively, the DrawDib functions are similar to the [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) function in that they provide image-stretching and dithering capabilities.</span></span> <span data-ttu-id="5f901-113">不過，DrawDib 函式支援影像解壓縮、資料串流，以及更多的顯示器介面卡數目。</span><span class="sxs-lookup"><span data-stu-id="5f901-113">However, the DrawDib functions support image decompression, data-streaming, and a greater number of display adapters.</span></span>

<span data-ttu-id="5f901-114">在某些情況下，您會發現使用 DrawDib 函式很有説明。</span><span class="sxs-lookup"><span data-stu-id="5f901-114">You will find it beneficial to use the DrawDib functions in some circumstances.</span></span> <span data-ttu-id="5f901-115">但是， [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 的多樣性比 DrawDib 函式更多樣化，當 DrawDib 函式無法提供所需的功能時，就應該使用這些功能。</span><span class="sxs-lookup"><span data-stu-id="5f901-115">Still, [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) is more diverse than the DrawDib functions and should be used when the DrawDib functions cannot provide the desired functionality.</span></span> <span data-ttu-id="5f901-116">下列清單描述在決定是否要使用 DrawDib 函式或 **StretchDIBits** 時要考慮的因素。</span><span class="sxs-lookup"><span data-stu-id="5f901-116">The following list describes factors to consider when deciding whether to use the DrawDib functions or **StretchDIBits**.</span></span>

-   <span data-ttu-id="5f901-117">色彩資料表資訊格式。</span><span class="sxs-lookup"><span data-stu-id="5f901-117">Color table information format.</span></span> <span data-ttu-id="5f901-118">DrawDib 函式會顯示在色彩表中使用 **DIB \_ RGB \_ 色彩** 格式的影像。</span><span class="sxs-lookup"><span data-stu-id="5f901-118">DrawDib functions display images that use the **DIB\_RGB\_COLORS** format for their color table.</span></span> <span data-ttu-id="5f901-119">如果您應用程式中的影像儲存具有 **DIB \_ pal \_ 色彩** 或 **dib \_ pal \_ 索引** 格式的色彩表資訊，您就必須使用 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 來顯示它們。</span><span class="sxs-lookup"><span data-stu-id="5f901-119">If images in your application store color table information with the **DIB\_PAL\_COLORS** or **DIB\_PAL\_INDICES** format, you must use [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) to display them.</span></span>
-   <span data-ttu-id="5f901-120">傳輸模式。</span><span class="sxs-lookup"><span data-stu-id="5f901-120">Transfer mode.</span></span> <span data-ttu-id="5f901-121">DrawDib 函式要求您的應用程式必須使用 **SRCCOPY** 傳輸模式。</span><span class="sxs-lookup"><span data-stu-id="5f901-121">DrawDib functions require that your application use the **SRCCOPY** transfer mode.</span></span> <span data-ttu-id="5f901-122">如果您的應用程式使用 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 搭配 **SRCCOPY** 以外的傳輸模式，您應該繼續使用 **StretchDIBits**。</span><span class="sxs-lookup"><span data-stu-id="5f901-122">If your application uses [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) with a transfer mode other than **SRCCOPY**, you should continue to use **StretchDIBits**.</span></span> <span data-ttu-id="5f901-123">同樣地，如果您需要在應用程式中使用其他的點陣作業（例如 XOR），請使用 **StretchDIBits**。</span><span class="sxs-lookup"><span data-stu-id="5f901-123">Similarly, if you need to use other raster operations in your application, such as an XOR, use **StretchDIBits**.</span></span>
-   <span data-ttu-id="5f901-124">影片和動畫播放的品質。</span><span class="sxs-lookup"><span data-stu-id="5f901-124">Quality of video and animation playback.</span></span> <span data-ttu-id="5f901-125">您可以針對資料串流應用程式使用 DrawDib 函式，例如播放影片剪輯和動畫順序的函式。</span><span class="sxs-lookup"><span data-stu-id="5f901-125">You can use the DrawDib functions for data-streaming applications, such as those that play video clips and animated sequences.</span></span> <span data-ttu-id="5f901-126">DrawDib 函式優於 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) ，因為它們提供了較高品質的影像，並改善播放期間的動作。</span><span class="sxs-lookup"><span data-stu-id="5f901-126">The DrawDib functions outperform [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) in that they provide higher-quality images and improve motion during playback.</span></span>
-   <span data-ttu-id="5f901-127">顯示介面卡。</span><span class="sxs-lookup"><span data-stu-id="5f901-127">Display adapters.</span></span> <span data-ttu-id="5f901-128">DrawDib 函式支援的顯示器介面卡數目超過 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) 支援的數目。</span><span class="sxs-lookup"><span data-stu-id="5f901-128">DrawDib functions support a greater number of display adapters than [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) supports.</span></span> <span data-ttu-id="5f901-129">DrawDib 函式支援使用4位影像深度提供16色調色板的 VGA 色器、使用8位影像深度提供256色調色板的 SVGA 介面卡，以及使用16位、24位和32位影像深度提供數千種色彩的純色顯示器介面卡。</span><span class="sxs-lookup"><span data-stu-id="5f901-129">The DrawDib functions support VGA color adapters that provide 16-color palettes using 4-bit image depth, SVGA adapters that provide 256-color palettes using 8-bit image depth, and true-color display adapters that provide thousands of colors using 16-bit, 24-bit, and 32-bit image depths.</span></span>

    <span data-ttu-id="5f901-130">DrawDib 函式也可改善在具有更多功能的顯示器介面卡上顯示影像的速度和品質。</span><span class="sxs-lookup"><span data-stu-id="5f901-130">The DrawDib functions also improve the speed and quality of displaying images on display adapters with more limited capabilities.</span></span> <span data-ttu-id="5f901-131">例如，在使用8位的顯示器介面卡時，DrawDib 函式會有效率地將真色彩影像遞色至256色彩。</span><span class="sxs-lookup"><span data-stu-id="5f901-131">For example, when using an 8-bit display adapter, the DrawDib functions efficiently dither true-color images to 256 colors.</span></span> <span data-ttu-id="5f901-132">它們也會在使用4位顯示介面卡時，將8位影像遞色。</span><span class="sxs-lookup"><span data-stu-id="5f901-132">They also dither 8-bit images when using 4-bit display adapters.</span></span>

-   <span data-ttu-id="5f901-133">影像延展。</span><span class="sxs-lookup"><span data-stu-id="5f901-133">Image-stretching.</span></span> <span data-ttu-id="5f901-134">如同 [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)，DrawDib 函式會使用來源和目的地矩形來控制顯示之影像的部分。</span><span class="sxs-lookup"><span data-stu-id="5f901-134">Like [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits), the DrawDib functions use source and destination rectangles to control the portion of an image that is displayed.</span></span> <span data-ttu-id="5f901-135">您可以藉由改變來源和目的地矩形的位置和大小，來裁剪影像的不必要部分或延展影像。</span><span class="sxs-lookup"><span data-stu-id="5f901-135">You can crop unwanted portions of an image or stretch an image by varying the position and size of the source and destination rectangles.</span></span> <span data-ttu-id="5f901-136">如果顯示驅動程式不支援影像延展，DrawDib 函式會提供比 **StretchDIBits** 更有效率的延展功能。</span><span class="sxs-lookup"><span data-stu-id="5f901-136">If a display driver does not support image-stretching, the DrawDib functions provide more efficient stretching capabilities than **StretchDIBits**.</span></span>
-   <span data-ttu-id="5f901-137">壓縮的影像。</span><span class="sxs-lookup"><span data-stu-id="5f901-137">Compressed images.</span></span> <span data-ttu-id="5f901-138">DrawDib 函式會繪製您有解壓縮程式的任何格式，包括執行長度的編碼 (RLE) 、Cinepak 和 411 YUV。</span><span class="sxs-lookup"><span data-stu-id="5f901-138">The DrawDib functions will draw any format for which you have a decompressor, including run-length encoding (RLE), Cinepak, and 411 YUV.</span></span> <span data-ttu-id="5f901-139">Windows 包含可選擇性安裝的 RLE 和 Cinepak decompressors。</span><span class="sxs-lookup"><span data-stu-id="5f901-139">Windows includes RLE and Cinepak decompressors that can be optionally installed.</span></span>
-   <span data-ttu-id="5f901-140">Windows 不再支援 Indeo 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="5f901-140">The Indeo codec is no longer supported in Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f901-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f901-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f901-142">DrawDib</span><span class="sxs-lookup"><span data-stu-id="5f901-142">DrawDib</span></span>](drawdib.md)
</dt> </dl>

 

 