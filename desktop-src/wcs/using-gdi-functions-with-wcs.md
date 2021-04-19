---
title: 使用 GDI 函數搭配 WCS
description: 圖形裝置介面中有各種不同的函式 (使用或操作色彩資料的 GDI) 。
ms.assetid: a19ec8b9-11c9-4fde-a99a-7f4a112b49e7
keywords:
- 'Windows Color System (WCS) 、圖形裝置介面 (GDI) '
- 'WCS (Windows 色彩系統) 、圖形裝置介面 (GDI) '
- '影像色彩管理、圖形裝置介面 (GDI) '
- '色彩管理、圖形裝置介面 (GDI) '
- '色彩、圖形裝置介面 (GDI) '
- " (GDI) 的圖形裝置介面"
- 'GDI (圖形裝置介面) '
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f411d5d91c36bf5d2f2fa82f332c9b15519d800d
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106993762"
---
# <a name="using-gdi-functions-with-wcs"></a><span data-ttu-id="91ea1-110">使用 GDI 函數搭配 WCS</span><span class="sxs-lookup"><span data-stu-id="91ea1-110">Using GDI Functions With WCS</span></span>

<span data-ttu-id="91ea1-111">圖形裝置介面中有各種不同的函式 (使用或操作色彩資料的 GDI) 。</span><span class="sxs-lookup"><span data-stu-id="91ea1-111">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="91ea1-112">有些會啟用以搭配 WCS 使用，有些則否。</span><span class="sxs-lookup"><span data-stu-id="91ea1-112">Some are enabled for use with WCS and some are not.</span></span> <span data-ttu-id="91ea1-113">下列 GDI 函數與 ICM 相關：</span><span class="sxs-lookup"><span data-stu-id="91ea1-113">The following GDI functions are relevant to ICM:</span></span>

-   [<span data-ttu-id="91ea1-114">使用 WCS 的裝置內容函式</span><span class="sxs-lookup"><span data-stu-id="91ea1-114">Device Context Functions with WCS</span></span>](#device-context-functions-with-wcs)
-   [<span data-ttu-id="91ea1-115">使用 WCS 的畫筆和筆刷函數</span><span class="sxs-lookup"><span data-stu-id="91ea1-115">Pen And Brush Functions with WCS</span></span>](#pen-and-brush-functions-with-wcs)
-   [<span data-ttu-id="91ea1-116">使用 WCS 的文字輸出函數</span><span class="sxs-lookup"><span data-stu-id="91ea1-116">Text Output Functions with WCS</span></span>](#text-output-functions-with-wcs)
-   [<span data-ttu-id="91ea1-117">具有 WCS 的 Bitmap 函數</span><span class="sxs-lookup"><span data-stu-id="91ea1-117">Bitmap Functions with WCS</span></span>](#bitmap-functions-with-wcs)

## <a name="device-context-functions-with-wcs"></a><span data-ttu-id="91ea1-118">使用 WCS 的裝置內容函式</span><span class="sxs-lookup"><span data-stu-id="91ea1-118">Device Context Functions with WCS</span></span>



|                    |                                                                                                                                                                                                                                 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ea1-119">CreateCompatibleDC</span><span class="sxs-lookup"><span data-stu-id="91ea1-119">CreateCompatibleDC</span></span> | <span data-ttu-id="91ea1-120">如果透過其 hdc 參數透過其 hdc 參數傳遞到此函式 (DC) 的裝置內容已啟用 ICM，則函式所建立的 DC 也會啟用 ICM。</span><span class="sxs-lookup"><span data-stu-id="91ea1-120">If the device context (DC) that is passed to this function through its hdc parameter is enabled for ICM, then the DC the function creates is also ICM-enabled.</span></span> <span data-ttu-id="91ea1-121">來源和目的色彩空間會在 DC 中指定。</span><span class="sxs-lookup"><span data-stu-id="91ea1-121">The source and destination color spaces are specified in the DC.</span></span> |
| <span data-ttu-id="91ea1-122">CreateDC</span><span class="sxs-lookup"><span data-stu-id="91ea1-122">CreateDC</span></span>           | <span data-ttu-id="91ea1-123">您可以藉由將 pInitData 參數所指向之 DEVMODE 結構的 dmICMMethod 成員設定為適當的值，來啟用 ICM。</span><span class="sxs-lookup"><span data-stu-id="91ea1-123">ICM can be enabled by setting the dmICMMethod member of the DEVMODE structure pointed to by the pInitData parameter to the appropriate value.</span></span> <span data-ttu-id="91ea1-124">如需詳細資訊，請參閱 DEVMODE 結構上 Platform SDK 中的檔。</span><span class="sxs-lookup"><span data-stu-id="91ea1-124">For details, see the documentation in the Platform SDK on the DEVMODE structure.</span></span>  |
| <span data-ttu-id="91ea1-125">ResetDC</span><span class="sxs-lookup"><span data-stu-id="91ea1-125">ResetDC</span></span>            | <span data-ttu-id="91ea1-126">根據 lpInitData 參數所指定的 DEVMODE 結構中的資訊，將會重設 hdc 參數所指定之裝置內容的色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="91ea1-126">The color profile of the device context specified by the hdc parameter will be reset based on the information in the DEVMODE structure specified by the lpInitData parameter.</span></span>                                                   |



 

## <a name="pen-and-brush-functions-with-wcs"></a><span data-ttu-id="91ea1-127">使用 WCS 的畫筆和筆刷函數</span><span class="sxs-lookup"><span data-stu-id="91ea1-127">Pen And Brush Functions with WCS</span></span>



|                 |                                                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ea1-128">筆刷函數</span><span class="sxs-lookup"><span data-stu-id="91ea1-128">Brush Functions</span></span> | <span data-ttu-id="91ea1-129">建立筆刷時，不會進行任何色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-129">No color management is done at brush creation.</span></span> <span data-ttu-id="91ea1-130">不過，在將筆刷選取到啟用 ICM 的 DC 時，將會執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-130">However, color management will be performed when the brush is selected into an ICM-enabled DC.</span></span> |
| <span data-ttu-id="91ea1-131">CreatePen</span><span class="sxs-lookup"><span data-stu-id="91ea1-131">CreatePen</span></span>       | <span data-ttu-id="91ea1-132">建立畫筆時，不會進行任何色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-132">No color management is done at pen creation.</span></span> <span data-ttu-id="91ea1-133">不過，在將筆刷選取到啟用 ICM 的 DC 時，將會執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-133">However, color management will be performed when the brush is selected into an ICM-enabled DC.</span></span>   |
| <span data-ttu-id="91ea1-134">ExtCreatePen</span><span class="sxs-lookup"><span data-stu-id="91ea1-134">ExtCreatePen</span></span>    | <span data-ttu-id="91ea1-135">建立畫筆時，不會進行任何色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-135">No color management is done at pen creation.</span></span> <span data-ttu-id="91ea1-136">不過，在將筆刷選取到啟用 ICM 的 DC 時，將會執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-136">However, color management will be performed when the brush is selected into an ICM-enabled DC.</span></span>   |
| <span data-ttu-id="91ea1-137">SelectObject</span><span class="sxs-lookup"><span data-stu-id="91ea1-137">SelectObject</span></span>    | <span data-ttu-id="91ea1-138">如果選取的物件是筆刷或畫筆，則會執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-138">If the object being selected is a brush or a pen, color management is performed.</span></span>                                                              |
| <span data-ttu-id="91ea1-139">SetDCBrushColor</span><span class="sxs-lookup"><span data-stu-id="91ea1-139">SetDCBrushColor</span></span> | <span data-ttu-id="91ea1-140">如果啟用 WCS，則會執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-140">Color management is performed if WCS is enabled.</span></span>                                                                                              |
| <span data-ttu-id="91ea1-141">SetDCPenColor</span><span class="sxs-lookup"><span data-stu-id="91ea1-141">SetDCPenColor</span></span>   | <span data-ttu-id="91ea1-142">如果啟用 WCS，則會執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-142">Color management is performed if WCS is enabled.</span></span>                                                                                              |



 

## <a name="text-output-functions-with-wcs"></a><span data-ttu-id="91ea1-143">使用 WCS 的文字輸出函數</span><span class="sxs-lookup"><span data-stu-id="91ea1-143">Text Output Functions with WCS</span></span>



|              |                                                  |
|--------------|--------------------------------------------------|
| <span data-ttu-id="91ea1-144">SetBkColor</span><span class="sxs-lookup"><span data-stu-id="91ea1-144">SetBkColor</span></span>   | <span data-ttu-id="91ea1-145">如果啟用 WCS，則會執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-145">Color management is performed if WCS is enabled.</span></span> |
| <span data-ttu-id="91ea1-146">SetTextColor</span><span class="sxs-lookup"><span data-stu-id="91ea1-146">SetTextColor</span></span> | <span data-ttu-id="91ea1-147">如果啟用 WCS，則會執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-147">Color management is performed if WCS is enabled.</span></span> |



 

## <a name="bitmap-functions-with-wcs"></a><span data-ttu-id="91ea1-148">具有 WCS 的 Bitmap 函數</span><span class="sxs-lookup"><span data-stu-id="91ea1-148">Bitmap Functions with WCS</span></span>



|                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ea1-149">BitBlt</span><span class="sxs-lookup"><span data-stu-id="91ea1-149">BitBlt</span></span>            | <span data-ttu-id="91ea1-150">發生 blits 時，不會執行任何色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-150">No color management is performed when blits occur.</span></span>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="91ea1-151">CreateDIBitmap</span><span class="sxs-lookup"><span data-stu-id="91ea1-151">CreateDIBitmap</span></span>    | <span data-ttu-id="91ea1-152">FuUsage 參數會指定 lpbmi 參數所指向之 BITMAPINFO 結構的 bmiColors 成員，或不包含色彩資訊。</span><span class="sxs-lookup"><span data-stu-id="91ea1-152">The fuUsage parameter specifies that the bmiColors member of the BITMAPINFO structure pointed at by the lpbmi parameter does or does not contain color information.</span></span> <span data-ttu-id="91ea1-153">如果沒有，則不會對此點陣圖執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-153">If it does not, no color management is performed for this bitmap.</span></span> <span data-ttu-id="91ea1-154">點陣圖必須使用第4版或第5版的 BITMAPINFO 結構，才能啟用色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-154">The bitmap must use version 4 or version 5 of the BITMAPINFO structure for color management to be enabled.</span></span> <span data-ttu-id="91ea1-155">建立點陣圖之後，所產生點陣圖的內容不符合色彩。</span><span class="sxs-lookup"><span data-stu-id="91ea1-155">The contents of the resulting bitmap are not color matched after the bitmap has been created.</span></span> |
| <span data-ttu-id="91ea1-156">CreateDIBSection</span><span class="sxs-lookup"><span data-stu-id="91ea1-156">CreateDIBSection</span></span>  | <span data-ttu-id="91ea1-157">如果透過 pbmi 參數傳遞的 BITMAPINFO 結構不是第4版或第5版，就不會進行任何色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-157">If the BITMAPINFO structure passed through the pbmi parameter is not version 4 or version 5, no color management is done.</span></span> <span data-ttu-id="91ea1-158">如果是第4版或第5版，則會啟用色彩管理，並將指定的色彩空間與點陣圖相關聯。</span><span class="sxs-lookup"><span data-stu-id="91ea1-158">If it is version 4 or 5, color management is enabled, and the specified color space is associated with the bitmap.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="91ea1-159">MaskBlt</span><span class="sxs-lookup"><span data-stu-id="91ea1-159">MaskBlt</span></span>           | <span data-ttu-id="91ea1-160">發生 blits 時，不會執行任何色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-160">No color management is performed when blits occur.</span></span>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="91ea1-161">SelectObject</span><span class="sxs-lookup"><span data-stu-id="91ea1-161">SelectObject</span></span>      | <span data-ttu-id="91ea1-162">如果物件是使用 CreateDIBSection 所建立的點陣圖，則會執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-162">If the object is a bitmap created with CreateDIBSection, color management is performed.</span></span> <span data-ttu-id="91ea1-163">點陣圖的色彩空間會用來做為目的色彩空間。</span><span class="sxs-lookup"><span data-stu-id="91ea1-163">The bitmap's color space is used as the destination color space.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="91ea1-164">SetDIBits</span><span class="sxs-lookup"><span data-stu-id="91ea1-164">SetDIBits</span></span>         | <span data-ttu-id="91ea1-165">色彩管理的執行。</span><span class="sxs-lookup"><span data-stu-id="91ea1-165">Color management is performed.</span></span> <span data-ttu-id="91ea1-166">如果指定的 BITMAPINFO 結構不是第4版或第5版，則會使用目前 DC 的色彩設定檔做為來源色彩空間設定檔。</span><span class="sxs-lookup"><span data-stu-id="91ea1-166">If the specified BITMAPINFO structure is not version 4 or version 5, the color profile of the current DC is used as the source color space profile.</span></span> <span data-ttu-id="91ea1-167">如果沒有，則會使用 sRGB 空間。</span><span class="sxs-lookup"><span data-stu-id="91ea1-167">If it does not have one, the sRGB space is used.</span></span> <span data-ttu-id="91ea1-168">如果指定的 BITMAPINFO 結構為第4版或第5版，則點陣圖標頭中指定的色彩空間設定檔會用來做為來源色彩空間設定檔。</span><span class="sxs-lookup"><span data-stu-id="91ea1-168">If the specified BITMAPINFO structure is version 4 or version 5, the color space profile specified in the bitmap header is used as the source color space profile.</span></span>                                         |
| <span data-ttu-id="91ea1-169">SetDIBitsToDevice</span><span class="sxs-lookup"><span data-stu-id="91ea1-169">SetDIBitsToDevice</span></span> | <span data-ttu-id="91ea1-170">色彩管理的執行。</span><span class="sxs-lookup"><span data-stu-id="91ea1-170">Color management is performed.</span></span> <span data-ttu-id="91ea1-171">如果指定的 BITMAPINFO 結構不是第4版或第5版，則會使用目前裝置內容的色彩設定檔做為來源色彩空間設定檔。</span><span class="sxs-lookup"><span data-stu-id="91ea1-171">If the specified BITMAPINFO structure is not version 4 or version 5, the color profile of the current device context is used as the source color space profile.</span></span> <span data-ttu-id="91ea1-172">如果沒有的話，則會使用 sRGB 色彩空間。</span><span class="sxs-lookup"><span data-stu-id="91ea1-172">If it doesn't have one, the sRGB color space is used.</span></span> <span data-ttu-id="91ea1-173">如果指定的 BITMAPINFO 結構為第4版或第5版，則會使用與點陣圖相關聯的色彩空間設定檔做為來源色彩空間。</span><span class="sxs-lookup"><span data-stu-id="91ea1-173">If the specified BITMAPINFO structure is version 4 or version 5, the color space profile associated with the bitmap is used as the source color space.</span></span>                                    |
| <span data-ttu-id="91ea1-174">SetDIBColorTable</span><span class="sxs-lookup"><span data-stu-id="91ea1-174">SetDIBColorTable</span></span>  | <span data-ttu-id="91ea1-175">未執行任何色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-175">No color management is performed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="91ea1-176">StretchBlt</span><span class="sxs-lookup"><span data-stu-id="91ea1-176">StretchBlt</span></span>        | <span data-ttu-id="91ea1-177">發生 blits 時，不會執行任何色彩管理。</span><span class="sxs-lookup"><span data-stu-id="91ea1-177">No color management is performed when blits occur.</span></span>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="91ea1-178">StretchDIBits</span><span class="sxs-lookup"><span data-stu-id="91ea1-178">StretchDIBits</span></span>     | <span data-ttu-id="91ea1-179">色彩管理的執行。</span><span class="sxs-lookup"><span data-stu-id="91ea1-179">Color management is performed.</span></span> <span data-ttu-id="91ea1-180">如果指定的 BITMAPINFO 結構不是第4版或第5版，則會使用目前 DC 的色彩設定檔做為來源色彩空間設定檔。</span><span class="sxs-lookup"><span data-stu-id="91ea1-180">If the specified BITMAPINFO structure is not version 4 or version 5, the color profile of the current DC is used as the source color space profile.</span></span> <span data-ttu-id="91ea1-181">如果沒有，則會使用 sRGB 空間。</span><span class="sxs-lookup"><span data-stu-id="91ea1-181">If it does not have one, the sRGB space is used.</span></span> <span data-ttu-id="91ea1-182">如果指定的 BITMAPINFO 結構為第4版或第5版，則點陣圖標頭中指定的色彩空間設定檔會用來做為來源色彩空間設定檔。</span><span class="sxs-lookup"><span data-stu-id="91ea1-182">If the specified BITMAPINFO structure is version 4 or version 5, the color space profile specified in the bitmap header is used as the source color space profile.</span></span>                                         |



 

 

 




