---
title: 設定影像串流
description: 設定影像串流
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- 串流，設定影像資料流程
- 編解碼器，設定影像串流
- 影像串流，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b05a21474143e227257dad240ff4d4464732ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372117"
---
# <a name="configuring-image-streams"></a><span data-ttu-id="c0140-106">設定影像串流</span><span class="sxs-lookup"><span data-stu-id="c0140-106">Configuring Image Streams</span></span>

<span data-ttu-id="c0140-107">影像資料流程包含靜止的影像（JPEG 格式）。</span><span class="sxs-lookup"><span data-stu-id="c0140-107">Image streams contain still images in JPEG format.</span></span> <span data-ttu-id="c0140-108">雖然影像串流像是影片串流，但它們會將未壓縮的影像作為輸入，因此需要的設定稍有不同。</span><span class="sxs-lookup"><span data-stu-id="c0140-108">Even though image streams are like video streams in that they take uncompressed images as inputs, they require a slightly different configuration.</span></span> <span data-ttu-id="c0140-109">若要設定影像資料流程，您必須設定影片設定結構成員的值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="c0140-109">To configure an image stream, you must set the values for the members of the video configuration structures as shown in the following table.</span></span>



| <span data-ttu-id="c0140-110">設定</span><span class="sxs-lookup"><span data-stu-id="c0140-110">Setting</span></span>                                                           | <span data-ttu-id="c0140-111">Description</span><span class="sxs-lookup"><span data-stu-id="c0140-111">Description</span></span>                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0140-112">**WM \_ 媒體 \_ 類型。 majortype**</span><span class="sxs-lookup"><span data-stu-id="c0140-112">**WM\_MEDIA\_TYPE.majortype**</span></span>                                     | <span data-ttu-id="c0140-113">設定為 WMMEDIATYPE \_ 影像。</span><span class="sxs-lookup"><span data-stu-id="c0140-113">Set to WMMEDIATYPE\_Image.</span></span>                                                                                                                                                       |
| <span data-ttu-id="c0140-114">**WM \_ 媒體 \_ 類型。子類型**</span><span class="sxs-lookup"><span data-stu-id="c0140-114">**WM\_MEDIA\_TYPE.subtype**</span></span>                                       | <span data-ttu-id="c0140-115">設定為 WMMEDIASUBTYPE \_ RGB24。</span><span class="sxs-lookup"><span data-stu-id="c0140-115">Set to WMMEDIASUBTYPE\_RGB24.</span></span>                                                                                                                                                    |
| <span data-ttu-id="c0140-116">**WM \_ 媒體 \_ 類型。 bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="c0140-116">**WM\_MEDIA\_TYPE.bFixedSizeSamples**</span></span>                             | <span data-ttu-id="c0140-117">設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c0140-117">Set to **FALSE**.</span></span>                                                                                                                                                                |
| <span data-ttu-id="c0140-118">**WM \_ 媒體 \_ 類型。 bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="c0140-118">**WM\_MEDIA\_TYPE.bTemporalCompression**</span></span>                          | <span data-ttu-id="c0140-119">設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c0140-119">Set to **FALSE**.</span></span>                                                                                                                                                                |
| <span data-ttu-id="c0140-120">**WM \_ 媒體 \_ 類型。 lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="c0140-120">**WM\_MEDIA\_TYPE.lSampleSize**</span></span>                                   | <span data-ttu-id="c0140-121">設定為0。</span><span class="sxs-lookup"><span data-stu-id="c0140-121">Set to 0.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c0140-122">**WM \_ 媒體 \_ 類型。 formattype**</span><span class="sxs-lookup"><span data-stu-id="c0140-122">**WM\_MEDIA\_TYPE.formattype**</span></span>                                    | <span data-ttu-id="c0140-123">設定為 WMFORMAT \_ VideoInfo。</span><span class="sxs-lookup"><span data-stu-id="c0140-123">Set to WMFORMAT\_VideoInfo.</span></span>                                                                                                                                                      |
| <span data-ttu-id="c0140-124">**WM \_ 媒體 \_ 類型。 pUnk**</span><span class="sxs-lookup"><span data-stu-id="c0140-124">**WM\_MEDIA\_TYPE.pUnk**</span></span>                                          | <span data-ttu-id="c0140-125">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c0140-125">Set to **NULL**.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="c0140-126">**WM \_ 媒體 \_ 類型。 cbFormat**</span><span class="sxs-lookup"><span data-stu-id="c0140-126">**WM\_MEDIA\_TYPE.cbFormat**</span></span>                                      | <span data-ttu-id="c0140-127">設定為 `sizeof(WMVIDEOINFOHEADER)`。</span><span class="sxs-lookup"><span data-stu-id="c0140-127">Set to `sizeof(WMVIDEOINFOHEADER)`.</span></span>                                                                                                                                              |
| <span data-ttu-id="c0140-128">**WM \_ 媒體 \_ 類型。 pbFormat**</span><span class="sxs-lookup"><span data-stu-id="c0140-128">**WM\_MEDIA\_TYPE.pbFormat**</span></span>                                      | <span data-ttu-id="c0140-129">設定為正確設定的 **WMVIDEOINFOHEADER** 結構位址。</span><span class="sxs-lookup"><span data-stu-id="c0140-129">Set to the address of a properly configured **WMVIDEOINFOHEADER** structure.</span></span>                                                                                                     |
| <span data-ttu-id="c0140-130">**WMVIDEOINFOHEADER. rcSource** 和 **WMVIDEOINFOHEADER. rcTarget**</span><span class="sxs-lookup"><span data-stu-id="c0140-130">**WMVIDEOINFOHEADER.rcSource** and **WMVIDEOINFOHEADER.rcTarget**</span></span> | <span data-ttu-id="c0140-131">設定這兩個矩形，讓左上角成為座標 (0、0) 和右下角的座標 (x，y) 其中 x 是影像寬度，y 是影像高度。</span><span class="sxs-lookup"><span data-stu-id="c0140-131">Set both rectangles so that the top left corners are coordinates (0, 0) and the bottom right corners are coordinates(x, y) where x is the image width and y is the image height.</span></span> |
| <span data-ttu-id="c0140-132">**WMVIDEOINFOHEADER.dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="c0140-132">**WMVIDEOINFOHEADER.dwBitRate**</span></span>                                   | <span data-ttu-id="c0140-133">設定為數據流的位元速率。</span><span class="sxs-lookup"><span data-stu-id="c0140-133">Set to the bit rate of the stream.</span></span>                                                                                                                                               |
| <span data-ttu-id="c0140-134">**WMVIDEOINFOHEADER.dwErrorRate**</span><span class="sxs-lookup"><span data-stu-id="c0140-134">**WMVIDEOINFOHEADER.dwErrorRate**</span></span>                                 | <span data-ttu-id="c0140-135">設定為0。</span><span class="sxs-lookup"><span data-stu-id="c0140-135">Set to 0.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c0140-136">**WMVIDEOINFOHEADER.dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="c0140-136">**WMVIDEOINFOHEADER.dwBitErrorRate**</span></span>                              | <span data-ttu-id="c0140-137">設定為0。</span><span class="sxs-lookup"><span data-stu-id="c0140-137">Set to 0.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c0140-138">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="c0140-138">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span></span>                             | <span data-ttu-id="c0140-139">設定為0。</span><span class="sxs-lookup"><span data-stu-id="c0140-139">Set to 0.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c0140-140">**BITMAPINFOHEADER.biWidth**</span><span class="sxs-lookup"><span data-stu-id="c0140-140">**BITMAPINFOHEADER.biWidth**</span></span>                                      | <span data-ttu-id="c0140-141">設定為影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="c0140-141">Set to the width of the image.</span></span>                                                                                                                                                   |
| <span data-ttu-id="c0140-142">**BITMAPINFOHEADER.biHeight**</span><span class="sxs-lookup"><span data-stu-id="c0140-142">**BITMAPINFOHEADER.biHeight**</span></span>                                     | <span data-ttu-id="c0140-143">設定為影像的高度。</span><span class="sxs-lookup"><span data-stu-id="c0140-143">Set to the height of the image.</span></span>                                                                                                                                                  |
| <span data-ttu-id="c0140-144">**BITMAPINFOHEADER.biPlanes**</span><span class="sxs-lookup"><span data-stu-id="c0140-144">**BITMAPINFOHEADER.biPlanes**</span></span>                                     | <span data-ttu-id="c0140-145">設定為 1。</span><span class="sxs-lookup"><span data-stu-id="c0140-145">Set to 1.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c0140-146">**BITMAPINFOHEADER.biBitCount**</span><span class="sxs-lookup"><span data-stu-id="c0140-146">**BITMAPINFOHEADER.biBitCount**</span></span>                                   | <span data-ttu-id="c0140-147">設定為24。</span><span class="sxs-lookup"><span data-stu-id="c0140-147">Set to 24.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="c0140-148">**BITMAPINFOHEADER.biCompression**</span><span class="sxs-lookup"><span data-stu-id="c0140-148">**BITMAPINFOHEADER.biCompression**</span></span>                                | <span data-ttu-id="c0140-149">設定為 [BI \_ RGB]。</span><span class="sxs-lookup"><span data-stu-id="c0140-149">Set to BI\_RGB.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="c0140-150">**BITMAPINFOHEADER.biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="c0140-150">**BITMAPINFOHEADER.biSizeImage**</span></span>                                  | <span data-ttu-id="c0140-151">設定為 ( (x \* y \* c) /8) ，其中 x 是影像的寬度，y 是影像的高度，而 c 是影像的色彩深度 (在此案例中一律為 24) 。</span><span class="sxs-lookup"><span data-stu-id="c0140-151">Set to ((x \* y \* c) / 8), where x is the width of the image, y is the height of the image, and c is the color depth of the image (in this case always 24).</span></span>                     |
| <span data-ttu-id="c0140-152">**BITMAPINFOHEADER.biXPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="c0140-152">**BITMAPINFOHEADER.biXPelsPerMeter**</span></span>                              | <span data-ttu-id="c0140-153">設定為0。</span><span class="sxs-lookup"><span data-stu-id="c0140-153">Set to 0.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c0140-154">**BITMAPINFOHEADER.biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="c0140-154">**BITMAPINFOHEADER.biYPelsPerMeter**</span></span>                              | <span data-ttu-id="c0140-155">設定為0。</span><span class="sxs-lookup"><span data-stu-id="c0140-155">Set to 0.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c0140-156">**BITMAPINFOHEADER.biClrUsed**</span><span class="sxs-lookup"><span data-stu-id="c0140-156">**BITMAPINFOHEADER.biClrUsed**</span></span>                                    | <span data-ttu-id="c0140-157">設定為0。</span><span class="sxs-lookup"><span data-stu-id="c0140-157">Set to 0.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="c0140-158">**BITMAPINFOHEADER.biClrImportant**</span><span class="sxs-lookup"><span data-stu-id="c0140-158">**BITMAPINFOHEADER.biClrImportant**</span></span>                               | <span data-ttu-id="c0140-159">設定為0。</span><span class="sxs-lookup"><span data-stu-id="c0140-159">Set to 0.</span></span>                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="c0140-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0140-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0140-161">**所有資料流程通用的設定**</span><span class="sxs-lookup"><span data-stu-id="c0140-161">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="c0140-162">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="c0140-162">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="c0140-163">**使用 Windows Media 視訊9螢幕編解碼器取得良好的結果**</span><span class="sxs-lookup"><span data-stu-id="c0140-163">**Getting Good Results with the Windows Media Video 9 Screen Codec**</span></span>](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[<span data-ttu-id="c0140-164">**影像串流**</span><span class="sxs-lookup"><span data-stu-id="c0140-164">**Image Streams**</span></span>](image-streams.md)
</dt> </dl>

 

 




