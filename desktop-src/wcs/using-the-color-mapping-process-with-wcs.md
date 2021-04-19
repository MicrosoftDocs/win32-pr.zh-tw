---
title: 使用具有 WCS 的色彩對應進程
description: WCS 色彩對應以裝置設定檔為基礎。
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Windows Color System (WCS) 、色彩對應
- WCS (Windows 色彩系統) ，色彩對應
- 影像色彩管理、色彩對應
- 色彩管理、色彩對應
- 色彩、色彩對應
- 色彩對應
- Windows Color System (WCS) 、裝置設定檔
- WCS (Windows 色彩系統) 、裝置設定檔
- 影像色彩管理、裝置設定檔
- 色彩管理，裝置設定檔
- 色彩、裝置設定檔
- Windows Color System (WCS) ，設定檔
- WCS (Windows 色彩系統) ，設定檔
- 影像色彩管理，設定檔
- 色彩管理，設定檔
- 色彩，設定檔
- 裝置設定檔
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106997591"
---
# <a name="using-the-color-mapping-process-with-wcs"></a><span data-ttu-id="ea47e-120">使用具有 WCS 的色彩對應進程</span><span class="sxs-lookup"><span data-stu-id="ea47e-120">Using The Color Mapping Process with WCS</span></span>

<span data-ttu-id="ea47e-121">WCS 色彩對應以 [裝置設定檔](d.md)為基礎。</span><span class="sxs-lookup"><span data-stu-id="ea47e-121">WCS color mapping is based on [device profiles](d.md).</span></span> <span data-ttu-id="ea47e-122">這些是由彩色硬體裝置的廠商提供，並會在安裝裝置時安裝。</span><span class="sxs-lookup"><span data-stu-id="ea47e-122">These are supplied by vendors of color hardware devices and installed when a device is installed.</span></span> <span data-ttu-id="ea47e-123">當應用程式使用色彩對應時，WCS 會存取影像的裝置設定檔，以取得將映射轉換成電腦所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="ea47e-123">When color mapping is used by an application program, WCS accesses the device profile of the image to get the information needed to convert the image to the PCS.</span></span> <span data-ttu-id="ea47e-124">轉換是由 CMM 進行。</span><span class="sxs-lookup"><span data-stu-id="ea47e-124">The conversion is done by the CMM.</span></span>

<span data-ttu-id="ea47e-125">裝置設定檔可以內嵌至映射本身。</span><span class="sxs-lookup"><span data-stu-id="ea47e-125">A device profile can be embedded into the image itself.</span></span> <span data-ttu-id="ea47e-126">因此，即使是透過網際網路，裝置設定檔也會與影像一起移動。</span><span class="sxs-lookup"><span data-stu-id="ea47e-126">So the device profile travels with the image, even across the Internet.</span></span> <span data-ttu-id="ea47e-127">使用者不需要來源裝置來取得正確的色彩對應。</span><span class="sxs-lookup"><span data-stu-id="ea47e-127">A user does not need the source device to get an accurate color mapping.</span></span> <span data-ttu-id="ea47e-128">如果映射沒有裝置設定檔，則會使用 sRGB 空間作為預設值。</span><span class="sxs-lookup"><span data-stu-id="ea47e-128">If an image does not have a device profile, the sRGB space is used as a default.</span></span> <span data-ttu-id="ea47e-129">如需詳細資訊，請參閱 [使用網際網路上的色彩管理](using-color-management-on-the-internet.md)。</span><span class="sxs-lookup"><span data-stu-id="ea47e-129">For more details, see [Using Color Management on the Internet](using-color-management-on-the-internet.md).</span></span>

<span data-ttu-id="ea47e-130">請注意，使用 WCS 的應用程式絕對不應該將 sRGB 設定檔內嵌至映射。</span><span class="sxs-lookup"><span data-stu-id="ea47e-130">Note that applications which use WCS should never embed the sRGB profile into an image.</span></span> <span data-ttu-id="ea47e-131">SRGB 色彩空間提供可在所有裝置上移植的標準化色彩空間。</span><span class="sxs-lookup"><span data-stu-id="ea47e-131">The sRGB color space provides a standardized color space that is portable across all devices.</span></span> <span data-ttu-id="ea47e-132">Windows 98 和更新版本以及 Windows 2000 和更新版本的使用者會自動使用此功能。</span><span class="sxs-lookup"><span data-stu-id="ea47e-132">It is automatically available to users of Windows 98 and later as well as Windows 2000 and later.</span></span> <span data-ttu-id="ea47e-133">因此，它不需要隨影像移動。</span><span class="sxs-lookup"><span data-stu-id="ea47e-133">Therefore, it does not need to travel with the image.</span></span>

<span data-ttu-id="ea47e-134">在 [電腦](p.md)中的影像色彩之後，WCS 會存取目的地裝置的裝置設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea47e-134">After the image colors are in the [PCS](p.md), WCS accesses the device profile of the destination device.</span></span> <span data-ttu-id="ea47e-135">它會取得 CMM，以將影像色彩從電腦轉換成目的地裝置的範圍。</span><span class="sxs-lookup"><span data-stu-id="ea47e-135">It gets the CMM to convert the image colors from PCS to the gamut of the destination device.</span></span>

<span data-ttu-id="ea47e-136">使用 WCS 也可以完成更複雜的色彩對應。</span><span class="sxs-lookup"><span data-stu-id="ea47e-136">More complex color mapping can also be done with WCS.</span></span> <span data-ttu-id="ea47e-137">例如，它可以用來瞭解在視頻顯示器上所建立的影像在高解析度雷射印表機上列印時的外觀。</span><span class="sxs-lookup"><span data-stu-id="ea47e-137">For example, it can be used to get an idea of what an image created on a video display would look like when printed on a high resolution laser printer.</span></span> <span data-ttu-id="ea47e-138">如果只有標準的噴墨印表機可供預覽，此範例會變得更複雜。</span><span class="sxs-lookup"><span data-stu-id="ea47e-138">The example gets more complex if there is only a standard inkjet printer on which to preview it.</span></span> <span data-ttu-id="ea47e-139">影像可以從顯示範圍轉換成噴墨印表機的範圍。</span><span class="sxs-lookup"><span data-stu-id="ea47e-139">The image can be converted from the gamut of the display, into the gamut of the inkjet printer.</span></span> <span data-ttu-id="ea47e-140">從該處，它可以轉換成雷射印表機的範圍。</span><span class="sxs-lookup"><span data-stu-id="ea47e-140">From there it can converted into the gamut of the laser printer.</span></span> <span data-ttu-id="ea47e-141">產生的影像可以列印在噴墨印表機上。</span><span class="sxs-lookup"><span data-stu-id="ea47e-141">The resulting image can be printed on the inkjet printer.</span></span> <span data-ttu-id="ea47e-142">當然，在列印彩色雷射印表機時，影像會以較高的解析度顯示。</span><span class="sxs-lookup"><span data-stu-id="ea47e-142">Of course the image would be at a higher resolution when printed on the color laser printer.</span></span> <span data-ttu-id="ea47e-143">不過，列印在噴墨印表機上的校樣影像的色彩，會與雷射印表機列印的色彩接近。</span><span class="sxs-lookup"><span data-stu-id="ea47e-143">However, the colors of the proofing image printed on the inkjet printer would be a close match to the colors that the laser printer would print.</span></span>

<span data-ttu-id="ea47e-144">範例中轉換的完成方式是將影像色彩從顯示器的範圍轉換成電腦。</span><span class="sxs-lookup"><span data-stu-id="ea47e-144">The way the conversions in the example are accomplished is to convert the image colors from the display's gamut into the PCS.</span></span> <span data-ttu-id="ea47e-145">影像色彩轉換成電腦之後，就會使用噴墨印表機的裝置設定檔，將它們轉換成噴墨印表機的範圍。</span><span class="sxs-lookup"><span data-stu-id="ea47e-145">After the image colors are converted into the PCS, the device profile of the inkjet printer would be used to transform them into the gamut of the inkjet printer.</span></span> <span data-ttu-id="ea47e-146">接著，會使用「範圍到電腦」轉換來將色彩移回電腦上。</span><span class="sxs-lookup"><span data-stu-id="ea47e-146">Next, the gamut to PCS transform would be used to move the colors back to the PCS.</span></span> <span data-ttu-id="ea47e-147">從該處，雷射印表機的裝置設定檔是用來將電腦的色彩轉換成雷射印表機的範圍。</span><span class="sxs-lookup"><span data-stu-id="ea47e-147">From there, the laser printer's device profile is used to convert the colors from PCS into the gamut of the laser printer.</span></span>

<span data-ttu-id="ea47e-148">能夠輕鬆地從裝置範圍將色彩轉換成電腦，然後再次啟用影像色彩，讓某一種色彩輸出裝置可在幾乎任何其他裝置上校訂。</span><span class="sxs-lookup"><span data-stu-id="ea47e-148">The ability to easily transform colors from a device gamut to the PCS and back again enables image colors intended for one color output device to be proofed on almost any other.</span></span>

<span data-ttu-id="ea47e-149">在上述範例中，描述會因清楚起見而稍微不同于實際程式。</span><span class="sxs-lookup"><span data-stu-id="ea47e-149">In the preceding example, the description varies from the actual procedure somewhat for clarity.</span></span> <span data-ttu-id="ea47e-150">實際上，上述段落中所提及的所有轉換都將串連成單一轉換。</span><span class="sxs-lookup"><span data-stu-id="ea47e-150">In reality, all of the transformations mentioned in the preceding paragraph would be concatenated into a single transformation.</span></span>

 

 




