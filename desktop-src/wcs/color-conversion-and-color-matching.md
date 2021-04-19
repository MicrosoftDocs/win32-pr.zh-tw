---
title: 色彩轉換和色彩比對
description: 將色彩從某個色彩空間轉換成另一個色彩的程式稱為色彩轉換。
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Color System (WCS) ，色彩轉換
- WCS (Windows 色彩系統) ，色彩轉換
- 影像色彩管理、色彩轉換
- 色彩管理、色彩轉換
- 色彩，色彩轉換
- 色彩轉換
- Windows Color System (WCS) ，色彩比對
- WCS (Windows 色彩系統) ，色彩比對
- 影像色彩管理、色彩比對
- 色彩管理、色彩比對
- 色彩、色彩比對
- 配色
- Windows Color System (WCS) 、色彩對應
- WCS (Windows 色彩系統) ，色彩對應
- 影像色彩管理、色彩對應
- 色彩管理、色彩對應
- 色彩、色彩對應
- 色彩對應
- 白色點
- 著色 劑
- Gamma 修正
- 域
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106985510"
---
# <a name="color-conversion-and-color-matching"></a><span data-ttu-id="94d89-125">色彩轉換和色彩比對</span><span class="sxs-lookup"><span data-stu-id="94d89-125">Color Conversion and Color Matching</span></span>

<span data-ttu-id="94d89-126">將色彩從某個 [色彩空間](c.md) 轉換成另一個色彩的程式稱為 *色彩轉換*。</span><span class="sxs-lookup"><span data-stu-id="94d89-126">The process of converting colors from one [color space](c.md) to another is called *color conversion*.</span></span> <span data-ttu-id="94d89-127">色彩空間中的所有色彩都是相對於色彩空間的 [白色點](w.md)固定的。</span><span class="sxs-lookup"><span data-stu-id="94d89-127">All colors in a color space are fixed relative to the color space's [white point](w.md).</span></span> <span data-ttu-id="94d89-128">由於色彩空間的白色點會因裝置而異，因此轉換後的色彩必須符合目的色彩空間中其視覺效果最接近的色彩。</span><span class="sxs-lookup"><span data-stu-id="94d89-128">Since the white point of a color space varies from device to device, a converted color must then be matched to its visually closest color in the destination color space.</span></span> <span data-ttu-id="94d89-129">此進程稱為 *色彩對應*。</span><span class="sxs-lookup"><span data-stu-id="94d89-129">This process is called *color mapping*.</span></span>

<span data-ttu-id="94d89-130">例如，如果您有在顯示器上建立的數位影像，它可能會在與裝置相關的 RGB 色彩空間中。</span><span class="sxs-lookup"><span data-stu-id="94d89-130">For example, if you have a digital image that you created on your display, it may be in a device-dependent RGB color space.</span></span> <span data-ttu-id="94d89-131">如果您想要在印表機上列印，則必須將它轉換成印表機的色彩空間。</span><span class="sxs-lookup"><span data-stu-id="94d89-131">If you want to print it on a printer, it must be converted to the printer's color space.</span></span> <span data-ttu-id="94d89-132">因為印表機可能會使用裝置相關的 CMYK 色彩空間，所以所有的 RGB 值都必須轉換成 CYMK。</span><span class="sxs-lookup"><span data-stu-id="94d89-132">Since the printer probably uses a device-dependent CMYK color space, all RGB values must be converted to CYMK.</span></span> <span data-ttu-id="94d89-133">這是 [色彩轉換](c.md)。</span><span class="sxs-lookup"><span data-stu-id="94d89-133">This is [color conversion](c.md).</span></span> <span data-ttu-id="94d89-134">一旦根據 CYMK 空間指定值，就必須與印表機所能產生的最接近色彩相符。</span><span class="sxs-lookup"><span data-stu-id="94d89-134">Once the values are specified in terms of the CYMK space, they need to be matched to the closest color that the printer can produce.</span></span> <span data-ttu-id="94d89-135">這稱為色彩對應或 [色彩](c.md)比對。</span><span class="sxs-lookup"><span data-stu-id="94d89-135">This is called color mapping or [color matching](c.md).</span></span>

<span data-ttu-id="94d89-136">色彩轉換和色彩對應都必須考慮許多裝置特定的因素。</span><span class="sxs-lookup"><span data-stu-id="94d89-136">Both color conversion and color mapping must take into account a number of device-specific factors.</span></span> <span data-ttu-id="94d89-137">例如，螢幕影像的建立區塊是圖元。</span><span class="sxs-lookup"><span data-stu-id="94d89-137">For instance, the building blocks of screen images are pixels.</span></span> <span data-ttu-id="94d89-138">每個圖元都有一組要儲存其色彩或色彩索引值的位數。</span><span class="sxs-lookup"><span data-stu-id="94d89-138">Each pixel has a set number of bits to store its color or color index value.</span></span> <span data-ttu-id="94d89-139">每圖元的位數取決於所使用的顯示和顯示介面卡類型，以及該介面卡的設定模式。</span><span class="sxs-lookup"><span data-stu-id="94d89-139">The number of bits per pixel depends on the type of display and display adapter being used, and the mode to which that the adapter is set.</span></span> <span data-ttu-id="94d89-140">大部分的印表機類型都會使用不同的 [colorants](c.md) ，並在特定的解析度列印。</span><span class="sxs-lookup"><span data-stu-id="94d89-140">Most every printer type uses different [colorants](c.md) and prints at particular resolutions.</span></span>

<span data-ttu-id="94d89-141">此外，裝置的實體色調特性通常會在不同的裝置上有所不同。</span><span class="sxs-lookup"><span data-stu-id="94d89-141">In addition, the physical tone characteristics of a device are often different on different devices.</span></span> <span data-ttu-id="94d89-142">比方說，當色彩是由電腦監視器產生時，它們的顯示方式可能會與按下列印時所產生的色彩不同。</span><span class="sxs-lookup"><span data-stu-id="94d89-142">For instance, when colors are produced by computer monitors, they can appear different than they would if they were produced on a printing press.</span></span> <span data-ttu-id="94d89-143">更正因數（稱為 *gamma 更正*）經常用來彌補這類差異。</span><span class="sxs-lookup"><span data-stu-id="94d89-143">A correction factor, called *gamma correction*, is frequently used to compensate for such differences.</span></span>

<span data-ttu-id="94d89-144">這些裝置相關因素的結果是每個色彩裝置都有一組特定的色彩可產生。</span><span class="sxs-lookup"><span data-stu-id="94d89-144">The result of these device-dependent factors is that each color device has a particular set of colors that it can produce.</span></span> <span data-ttu-id="94d89-145">此色彩集 *稱為其範圍*。</span><span class="sxs-lookup"><span data-stu-id="94d89-145">This color set is known as its *gamut*.</span></span> <span data-ttu-id="94d89-146">若要執行色彩轉換和色彩對應，影像中的色彩必須從來源裝置的色彩空間和範圍轉換成目的地裝置的色彩空間。</span><span class="sxs-lookup"><span data-stu-id="94d89-146">To perform color conversion and color mapping, the colors in an image must be converted from the color space and gamut of the source device into the color space of the destination device.</span></span> <span data-ttu-id="94d89-147">然後，它們會符合目的地裝置的範圍。</span><span class="sxs-lookup"><span data-stu-id="94d89-147">They are then matched into the gamut of the destination device.</span></span>

 

 




