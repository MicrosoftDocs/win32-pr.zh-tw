---
title: 轉譯意圖
description: 國際色彩協會 (ICC) 已定義四個不同的值，稱為轉譯意圖。
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Windows Color System (WCS) ，轉譯意圖
- WCS (Windows 色彩系統) ，轉譯意圖
- 影像色彩管理、轉譯意圖
- 色彩管理、轉譯意圖
- 色彩，轉譯意圖
- 轉譯意圖
- 國際色彩聯盟 (ICC)
- 'IIC (國際色彩協會) '
- 圖片意圖
- 圖形意圖
- 證明意圖
- 符合意圖
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106974780"
---
# <a name="rendering-intents"></a><span data-ttu-id="52028-115">轉譯意圖</span><span class="sxs-lookup"><span data-stu-id="52028-115">Rendering Intents</span></span>

<span data-ttu-id="52028-116">國際色彩協會 (ICC) 已定義四個不同的值，稱為轉譯 *意圖*。</span><span class="sxs-lookup"><span data-stu-id="52028-116">The International Color Consortium (ICC) has defined four different values called *rendering intents*.</span></span> <span data-ttu-id="52028-117">這些代表四種不同的方法來建立色彩轉譯。</span><span class="sxs-lookup"><span data-stu-id="52028-117">These represent four different approaches to creating a color rendering.</span></span> <span data-ttu-id="52028-118">這四個意圖和在程式碼中用來參考這些意圖的常數如下所示。</span><span class="sxs-lookup"><span data-stu-id="52028-118">These four intents, and the constants used to refer to them in code are as follows.</span></span>



| <span data-ttu-id="52028-119">Intent</span><span class="sxs-lookup"><span data-stu-id="52028-119">Intent</span></span>                            | <span data-ttu-id="52028-120">ICC 名稱</span><span class="sxs-lookup"><span data-stu-id="52028-120">ICC Name</span></span>              | <span data-ttu-id="52028-121">Description</span><span class="sxs-lookup"><span data-stu-id="52028-121">Description</span></span>                    |
|-----------------------------------|-----------------------|--------------------------------|
| <span data-ttu-id="52028-122">Picture</span><span class="sxs-lookup"><span data-stu-id="52028-122">Picture</span></span> | <span data-ttu-id="52028-123">感性</span><span class="sxs-lookup"><span data-stu-id="52028-123">Perceptual</span></span>            | <span data-ttu-id="52028-124">意圖 \_ 感知</span><span class="sxs-lookup"><span data-stu-id="52028-124">INTENT\_PERCEPTUAL</span></span>             |
| <span data-ttu-id="52028-125">Graphic</span><span class="sxs-lookup"><span data-stu-id="52028-125">Graphic</span></span> | <span data-ttu-id="52028-126">飽和度</span><span class="sxs-lookup"><span data-stu-id="52028-126">Saturation</span></span>            | <span data-ttu-id="52028-127">意圖 \_ 飽和度</span><span class="sxs-lookup"><span data-stu-id="52028-127">INTENT\_SATURATION</span></span>             |
| <span data-ttu-id="52028-128">證明</span><span class="sxs-lookup"><span data-stu-id="52028-128">Proof</span></span>     | <span data-ttu-id="52028-129">相對色度</span><span class="sxs-lookup"><span data-stu-id="52028-129">Relative Colorimetric</span></span> | <span data-ttu-id="52028-130">意圖 \_ 相對 \_ 色度</span><span class="sxs-lookup"><span data-stu-id="52028-130">INTENT\_RELATIVE\_COLORIMETRIC</span></span> |
| <span data-ttu-id="52028-131">比對</span><span class="sxs-lookup"><span data-stu-id="52028-131">Match</span></span>     | <span data-ttu-id="52028-132">絕對色度</span><span class="sxs-lookup"><span data-stu-id="52028-132">Absolute Colorimetric</span></span> | <span data-ttu-id="52028-133">意圖 \_ 絕對 \_ 色度</span><span class="sxs-lookup"><span data-stu-id="52028-133">INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> |




 

<span data-ttu-id="52028-134">您可以從 color.org 下載 ICC 配置檔案格式規格版本3.4 （描述這些意圖）。</span><span class="sxs-lookup"><span data-stu-id="52028-134">The ICC Profile Format Specification Version 3.4, which describes these intents, can be downloaded from color.org.</span></span>

## <a name="picture-intent"></a><span data-ttu-id="52028-135">圖片意圖</span><span class="sxs-lookup"><span data-stu-id="52028-135">Picture Intent</span></span>

<span data-ttu-id="52028-136">在 ICC 規格子句4.9 中稱為 [感知意圖]，圖片意圖會將影像的整個範圍壓縮或展開以 [填滿目的地](./g.md) 裝置的範圍，因此會保留灰色平衡，但不會保留色階的精確度。</span><span class="sxs-lookup"><span data-stu-id="52028-136">Called perceptual intent in the ICC specification clause 4.9, a Picture intent causes the full [gamut](./g.md) of the image to be compressed or expanded to fill the gamut of the destination device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span>

<span data-ttu-id="52028-137">換句話說，如果影像中的某些色彩落在輸出裝置可轉譯的色彩範圍之外，圖片意圖將會調整影像中的所有色彩，以便影像中的每個色彩都落在可轉譯的範圍內，如此一來，色彩之間的關聯性就會盡可能地保留。</span><span class="sxs-lookup"><span data-stu-id="52028-137">In other words, if certain colors in an image fall outside of the range of colors that the output device can render, the picture intent will cause all the colors in the image to be adjusted so that the every color in the image falls within the range that can be rendered and so that the relationship between colors is preserved as much as possible.</span></span>

<span data-ttu-id="52028-138">此意圖最適合顯示相片和影像，而且通常是預設意圖。</span><span class="sxs-lookup"><span data-stu-id="52028-138">This intent is most suitable for display of photographs and images, and is generally the default intent.</span></span>

## <a name="graphic-intent"></a><span data-ttu-id="52028-139">圖形意圖</span><span class="sxs-lookup"><span data-stu-id="52028-139">Graphic Intent</span></span>

<span data-ttu-id="52028-140">ICC 規格子句4.12 會以 [飽和度](s.md) 意圖呼叫圖形意圖。</span><span class="sxs-lookup"><span data-stu-id="52028-140">The ICC specification clause 4.12 calls the Graphic intent a [saturation](s.md) intent.</span></span> <span data-ttu-id="52028-141">它會將色彩的色度保留在影像中，可能會有 [色調](h.md) 和 [亮度](l.md)的費用。</span><span class="sxs-lookup"><span data-stu-id="52028-141">It preserves the chroma of colors in the image at the possible expense of [hue](h.md) and [lightness](l.md).</span></span>

<span data-ttu-id="52028-142">這種意圖的實現仍有一些問題，而且 ICC 仍在使用方法來達成所需的效果。</span><span class="sxs-lookup"><span data-stu-id="52028-142">Implementation of this intent remains somewhat problematic, and the ICC is still working on methods to achieve the desired effects.</span></span>

<span data-ttu-id="52028-143">這種意圖最適合用來做為圖表等商務圖形，在這種情況下更重要的是，色彩更重要，且彼此對比，而不是特定的色彩。</span><span class="sxs-lookup"><span data-stu-id="52028-143">This intent is most suitable for business graphics such as charts, where it is more important that the colors be vivid and contrast well with each other rather than a specific color.</span></span>

## <a name="proof-intent"></a><span data-ttu-id="52028-144">證明意圖</span><span class="sxs-lookup"><span data-stu-id="52028-144">Proof Intent</span></span>

<span data-ttu-id="52028-145">證明意圖（即 ICC 規格中的色度意圖）的定義，是在輸出裝置可轉譯的範圍之外的任何色彩都調整為可轉譯的最接近色彩，而其他所有色彩則會保持不變。</span><span class="sxs-lookup"><span data-stu-id="52028-145">The Proof intent, called the colorimetric intent in the ICC specification, is defined such that any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span>

<span data-ttu-id="52028-146">證明意圖不會保留 [白色點](w.md)。</span><span class="sxs-lookup"><span data-stu-id="52028-146">Proof intent does not preserve the [white point](w.md).</span></span>

<span data-ttu-id="52028-147">例如，紙張的 whitest 白色會比電腦監視器的 whitest 白色更黃。</span><span class="sxs-lookup"><span data-stu-id="52028-147">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="52028-148">使用相對色度意圖將影像轉換成印表機的範圍，會導致所有色彩變得更黃色。</span><span class="sxs-lookup"><span data-stu-id="52028-148">An image converted into the gamut of the printer using relative colorimetric intent would result in all colors becoming more yellow.</span></span> <span data-ttu-id="52028-149">影像的白色點會移動以符合印表機的白色點。</span><span class="sxs-lookup"><span data-stu-id="52028-149">The white point of the image is moved to match the white point of the printer.</span></span> <span data-ttu-id="52028-150">影像中的所有其他色彩都會保持其相對於白色點的位置。</span><span class="sxs-lookup"><span data-stu-id="52028-150">All other colors in the image keep their position relative to the white point.</span></span> <span data-ttu-id="52028-151">這會產生一個影像，以更精確地反映出印刷影像的樣子。</span><span class="sxs-lookup"><span data-stu-id="52028-151">This produces an image that more accurately reflects what the printed image will look like.</span></span> <span data-ttu-id="52028-152">不過，使用者可能會發現它以視覺化的方式令人不安。</span><span class="sxs-lookup"><span data-stu-id="52028-152">However, the user may find it visually disconcerting.</span></span>

## <a name="match-intent"></a><span data-ttu-id="52028-153">符合意圖</span><span class="sxs-lookup"><span data-stu-id="52028-153">Match Intent</span></span>

<span data-ttu-id="52028-154">在比對意圖中，任何落在輸出裝置所能轉譯範圍之外的色彩，都會調整為最接近可以轉譯的色彩，而其他所有色彩則會保持不變。</span><span class="sxs-lookup"><span data-stu-id="52028-154">In a Match intent, any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span> <span data-ttu-id="52028-155">ICC 規格會呼叫 match 意圖的絕對色度意圖。</span><span class="sxs-lookup"><span data-stu-id="52028-155">The ICC specification calls the match intent absolute colorimetric intent.</span></span>

<span data-ttu-id="52028-156">比對意圖會保留白色點。</span><span class="sxs-lookup"><span data-stu-id="52028-156">Match intent preserves the white point.</span></span>

<span data-ttu-id="52028-157">例如，紙張的 whitest 白色會比電腦監視器的 whitest 白色更黃。</span><span class="sxs-lookup"><span data-stu-id="52028-157">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="52028-158">使用 match 意圖將影像轉換成 [印表機的範圍，會](./g.md) 導致所有色彩轉換並符合印表機的範圍。</span><span class="sxs-lookup"><span data-stu-id="52028-158">An image converted into the [gamut](./g.md) of the printer using match intent would result in all colors being converted and matched into the gamut of the printer.</span></span> <span data-ttu-id="52028-159">影像的白色點不會移動以符合印表機的白色點。</span><span class="sxs-lookup"><span data-stu-id="52028-159">The white point of the image is not moved to match the white point of the printer.</span></span> <span data-ttu-id="52028-160">因此，色彩與白色點之間的距離可能會變更。</span><span class="sxs-lookup"><span data-stu-id="52028-160">Therefore, the distance of the colors to the white point may change.</span></span> <span data-ttu-id="52028-161">這會產生較不會以視覺方式令人不安給使用者的影像，但也是較不精確的印表機輸出呈現方式。</span><span class="sxs-lookup"><span data-stu-id="52028-161">This produces an image that is less visually disconcerting to the user, but is also a less accurate rendition of printer output.</span></span>

 

 