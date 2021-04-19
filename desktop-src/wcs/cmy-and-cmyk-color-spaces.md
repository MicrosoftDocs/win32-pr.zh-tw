---
title: CMY 和 CMYK 色彩空間
description: CMY 和 CMYK 色彩空間通常用於彩色列印。 CMY 色彩空間使用青色、洋紅和黃色 (CMY) 作為其主要色彩。 紅色、綠色和藍色是次要色彩。
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Color System (WCS) ，CMY 色彩空間
- WCS (Windows 色彩系統) ，CMY 色彩空間
- 影像色彩管理、CMY 色彩空間
- 色彩管理，CMY 色彩空間
- 色彩，CMY 色彩空間
- 色彩空間、CMY
- CMY 色彩空間
- Windows Color System (WCS) 、CMYK 色彩空間
- WCS (Windows 色彩系統) 、CMYK 色彩空間
- 影像色彩管理、CMYK 色彩空間
- 色彩管理，CMYKcolor 空間
- 色彩、CMYK 色彩空間
- 色彩空間、CMYK
- CMYK 色彩空間
- 青色
- 洋紅
- 黃色
- '青色洋紅黃色 (CMY) '
- 'CMY (青色洋紅黃色) '
- '青色洋紅色黃色黑色 (CMYK) '
- 'CMYK (青色洋黃色黑色) '
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/26/2021
ms.locfileid: "106982782"
---
# <a name="cmy-and-cmyk-color-spaces"></a><span data-ttu-id="4fdc8-126">CMY 和 CMYK 色彩空間</span><span class="sxs-lookup"><span data-stu-id="4fdc8-126">CMY and CMYK Color Spaces</span></span>

<span data-ttu-id="4fdc8-127">CMY 和 CMYK [色彩空間](c.md) 通常用於彩色列印。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-127">The CMY and CMYK [color spaces](c.md) are often used in color printing.</span></span> <span data-ttu-id="4fdc8-128">CMY 色彩空間使用青色、洋紅和黃色 (CMY) 作為其 [主要色彩](p.md)。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-128">A CMY color space uses cyan, magenta, and yellow (CMY) as its [primary colors](p.md).</span></span> <span data-ttu-id="4fdc8-129">紅色、綠色和藍色是次要色彩。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-129">Red, green, and blue are the secondary colors.</span></span>

<span data-ttu-id="4fdc8-130">下圖是 CMY 色彩空間的色彩標記法。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-130">The following figures are color representations of the CMY color space.</span></span> <span data-ttu-id="4fdc8-131">CMY 色彩空間已正規化。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-131">The CMY color space is normalized.</span></span>

![cmy 色彩空間 cube （最大值）](images/cmyclrs1.png)

![cmy 色彩空間 cube （最小值）](images/cmyclrs2.png)

<span data-ttu-id="4fdc8-134">CMY 色彩空間為 subtractive。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-134">The CMY color space is subtractive.</span></span> <span data-ttu-id="4fdc8-135">因此，白色是 (0.0、0.0、0.0) 和黑色 (1.0、1.0、1.0) 。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-135">Therefore, white is at (0.0, 0.0, 0.0) and black is at (1.0, 1.0, 1.0).</span></span> <span data-ttu-id="4fdc8-136">如果您以白色開頭且不能減去任何色彩，您會得到白色。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-136">If you start with white and subtract no colors, you get white.</span></span> <span data-ttu-id="4fdc8-137">如果您以白色開頭，並同樣地減去所有色彩，則會得到黑色。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-137">If you start with white and subtract all colors equally, you get black.</span></span>

<span data-ttu-id="4fdc8-138">CMYK 色彩空間是 CMY 模型的變化。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-138">The CMYK color space is a variation on the CMY model.</span></span> <span data-ttu-id="4fdc8-139">它會將黑色 (青色、洋紅、黃色和黑色) 。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-139">It adds black (Cyan, Magenta, Yellow, and blacK).</span></span> <span data-ttu-id="4fdc8-140">CMYK 色彩空間會關閉理論與實務之間的差距。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-140">The CMYK color space closes the gap between theory and practice.</span></span> <span data-ttu-id="4fdc8-141">理論上，不需要額外的黑色元件。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-141">In theory, the extra black component is not needed.</span></span> <span data-ttu-id="4fdc8-142">不過，使用各種類型的墨水和紙張的經驗，會顯示當混合青色、洋紅和黃色油墨的相等元件時，結果通常是深棕色，而不是黑色。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-142">However, experience with various types of inks and papers has shown that when equal components of cyan, magenta, and yellow inks are mixed, the result is usually a dark brown, not black.</span></span> <span data-ttu-id="4fdc8-143">將黑色筆墨新增至混合可解決此問題。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-143">Adding black ink to the mix solves this problem.</span></span>

<span data-ttu-id="4fdc8-144">CMY 和 CMYK 色彩空間可與裝置無關，但最常使用於特定裝置的參考中。</span><span class="sxs-lookup"><span data-stu-id="4fdc8-144">The CMY and CMYK colors spaces can be device independent, but most often they are used in reference to a specific device.</span></span>

 

 




