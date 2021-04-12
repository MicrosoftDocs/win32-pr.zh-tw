---
description: 真實世界中的燈光包含一個非常高的動態範圍 (HDR) 的亮度值。
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: " (Direct3D 9) 的 HDR 照明"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187370"
---
# <a name="hdr-lighting-direct3d-9"></a><span data-ttu-id="41767-103"> (Direct3D 9) 的 HDR 照明</span><span class="sxs-lookup"><span data-stu-id="41767-103">HDR Lighting (Direct3D 9)</span></span>

<span data-ttu-id="41767-104">真實世界中的燈光包含一個非常高的動態範圍 (HDR) 的亮度值。</span><span class="sxs-lookup"><span data-stu-id="41767-104">Lighting in the real world contains a very high dynamic range (HDR) of luminance values.</span></span> <span data-ttu-id="41767-105">真實世界有大約10個動態範圍 (DR) 的亮度值分散到亮度的範圍之間。</span><span class="sxs-lookup"><span data-stu-id="41767-105">The real world has about 10 orders of dynamic range (DR) for luminance values spread across the spectrum of darkness to brightness.</span></span> <span data-ttu-id="41767-106">另一方面，電腦螢幕的顯示範圍 (或亮度值範圍) ：大約兩個動態範圍的順序。</span><span class="sxs-lookup"><span data-stu-id="41767-106">On the other hand, a computer screen has a very limited display gamut (or range of luminance values): approximately two orders of dynamic range.</span></span> <span data-ttu-id="41767-107">產生 HDR 轉譯影像的挑戰，是要將真實世界的 HDR 值對應到電腦螢幕的有限範圍內。</span><span class="sxs-lookup"><span data-stu-id="41767-107">The challenge to producing HDR rendered images is to map the real world HDR values into the limited gamut of a computer screen.</span></span>

<span data-ttu-id="41767-108">色調對應是 DirectX 用來將 HDR 資訊對應到更有限範圍的技術。</span><span class="sxs-lookup"><span data-stu-id="41767-108">Tone mapping is the technique used by DirectX for mapping HDR information into a more limited range.</span></span> <span data-ttu-id="41767-109">套用至 CGI 轉譯的色調對應可大幅改善所呈現的光源詳細資料量，讓您可以在最深的區域中看到詳細資料，以及在外觀較亮的區域中提供對比。</span><span class="sxs-lookup"><span data-stu-id="41767-109">Tone mapping applied to CGI rendering can dramatically improve the amount of lighting detail rendered, allowing details in the darkest areas to be seen, and providing contrast in areas that are so bright, they appear burned.</span></span> <span data-ttu-id="41767-110">產生的場景會呈現更多可見的光源詳細資料。</span><span class="sxs-lookup"><span data-stu-id="41767-110">The resulting scenes render with far more visible lighting detail.</span></span>

<span data-ttu-id="41767-111">[HDRLighting 範例](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) 是示範 HDR 照明的 SDK 範例。</span><span class="sxs-lookup"><span data-stu-id="41767-111">[HDRLighting Sample](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) is a SDK sample that demonstrates HDR lighting.</span></span>

## <a name="tone-mapping"></a><span data-ttu-id="41767-112">語氣對應</span><span class="sxs-lookup"><span data-stu-id="41767-112">Tone Mapping</span></span>

<span data-ttu-id="41767-113">色調對應通常會模擬監視的 DR 無法造成的光學現象。</span><span class="sxs-lookup"><span data-stu-id="41767-113">Tone mapping generally simulates optical phenomena that cannot be caused by the DR of the monitor.</span></span> <span data-ttu-id="41767-114">這種情況的範例包括光暈或綻放 (，這些屬性大多是鏡頭) 的屬性，也就是在一般情況下，人類眼中發生的藍色變換，以及生物化學眼睛結果的其他採用原音。</span><span class="sxs-lookup"><span data-stu-id="41767-114">Examples of this are flares or blooming (which are mostly properties of lenses), the blue shift that happens in the human eye in low light conditions, and other adaptations that are a result of the biochemistry of the eye.</span></span> <span data-ttu-id="41767-115">如果顯示器的 DR 夠大，則不需要語氣對應，除了提供美術效果或某些相機鏡頭或收費裝置的屬性 (CCD) 。</span><span class="sxs-lookup"><span data-stu-id="41767-115">If the DR of the display were large enough, tone mapping would not be as neccessary, except for providing artistic effects or some of the properties of a camera lens or a charge coupled device (CCD).</span></span>

<span data-ttu-id="41767-116">色調對應會將場景中的亮度值範圍分割成一組區域。</span><span class="sxs-lookup"><span data-stu-id="41767-116">Tone mapping divides the range of luminance values in a scene into a set of zones.</span></span> <span data-ttu-id="41767-117">每個區域都包含一個範圍的亮度值。</span><span class="sxs-lookup"><span data-stu-id="41767-117">Each zone encompasses a range of luminance values.</span></span>

<span data-ttu-id="41767-118">HDR 使用下列詞彙：</span><span class="sxs-lookup"><span data-stu-id="41767-118">HDR uses the following terms:</span></span>

-   <span data-ttu-id="41767-119">區域範圍的亮度值</span><span class="sxs-lookup"><span data-stu-id="41767-119">Zone - range of luminance values</span></span>
-   <span data-ttu-id="41767-120">場景的中間灰色-中間亮度區域</span><span class="sxs-lookup"><span data-stu-id="41767-120">Middle gray - middle brightness region of the scene</span></span>
-   <span data-ttu-id="41767-121">動態範圍-最高場景亮度至最低場景亮度的比率</span><span class="sxs-lookup"><span data-stu-id="41767-121">Dynamic range - ratio of the highest scene luminance to the lowest scene luminance</span></span>
-   <span data-ttu-id="41767-122">場景光源的按鍵-主觀測量：這會因淺色而異至深色</span><span class="sxs-lookup"><span data-stu-id="41767-122">Key - subjective measurement of scene lighting: this varies from light to moderate to dark</span></span>

<span data-ttu-id="41767-123">若要從 RGB 值計算亮度，請使用：</span><span class="sxs-lookup"><span data-stu-id="41767-123">To calculate luminance from RGB values, use this:</span></span>


```
L = 0.27R + 0.67G + 0.06B;
```



<span data-ttu-id="41767-124">記錄平均的亮度是場景索引鍵的有用近似值。</span><span class="sxs-lookup"><span data-stu-id="41767-124">The log-average luminance is a useful approximation for the key of a scene.</span></span> <span data-ttu-id="41767-125">一般方程式如下所示：</span><span class="sxs-lookup"><span data-stu-id="41767-125">A general equation looks like this:</span></span>

<span data-ttu-id="41767-126">L<sub>w</sub> = exp \[ 1/N ( sum \[ Log ( delta + L<sub>w</sub> ( x，y ) ) \] ) \]</span><span class="sxs-lookup"><span data-stu-id="41767-126">L<sub>w</sub> = exp\[ 1 / N( sum\[ log( delta + L<sub>w</sub>( x, y ) ) \] ) \]</span></span>

<span data-ttu-id="41767-127">其中：</span><span class="sxs-lookup"><span data-stu-id="41767-127">Where:</span></span>

-   <span data-ttu-id="41767-128">L<sub>w</sub> -記錄-平均亮度</span><span class="sxs-lookup"><span data-stu-id="41767-128">L<sub>w</sub> - log-average luminance</span></span>
-   <span data-ttu-id="41767-129">N-影像中的圖元數目</span><span class="sxs-lookup"><span data-stu-id="41767-129">N - number of pixels in the image</span></span>
-   <span data-ttu-id="41767-130">delta-避免黑色圖元問題的小型因素</span><span class="sxs-lookup"><span data-stu-id="41767-130">delta - a small factor to avoid problems with black pixels</span></span>
-   <span data-ttu-id="41767-131">L<sub>w</sub> ( x，y ) -圖元 ( x，y ) 的世界空間亮度</span><span class="sxs-lookup"><span data-stu-id="41767-131">L<sub>w</sub>( x, y ) - the world space luminance for pixel ( x, y )</span></span>

<span data-ttu-id="41767-132">若要將此對應至中間的值，以下是明亮比例調整運算子：</span><span class="sxs-lookup"><span data-stu-id="41767-132">To map this to a middle-gray value, here is a luminance scaling operator:</span></span>

<span data-ttu-id="41767-133">L ( x，y ) = a \* L<sub>w</sub> ( x，y ) /l<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="41767-133">L( x, y ) = a \* L<sub>w</sub>( x, y ) / L<sub>w</sub></span></span>

<span data-ttu-id="41767-134">其中：</span><span class="sxs-lookup"><span data-stu-id="41767-134">Where:</span></span>

-   <span data-ttu-id="41767-135">L ( x，y ) 縮放亮度（圖元） ( x，y ) </span><span class="sxs-lookup"><span data-stu-id="41767-135">L( x, y ) - scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="41767-136">套用調整之後的影像索引鍵值</span><span class="sxs-lookup"><span data-stu-id="41767-136">a - image key value after applying the scaling</span></span>

<span data-ttu-id="41767-137">最後，以下是可壓縮高 luminances 的簡單音調對應運算子：</span><span class="sxs-lookup"><span data-stu-id="41767-137">And finally, here is a simple tone mapping operator for compressing the high luminances:</span></span>

<span data-ttu-id="41767-138">L<sub>d</sub> ( x、y ) = L ( x、y ) / ( 1 + L ( x、y ) ) </span><span class="sxs-lookup"><span data-stu-id="41767-138">L<sub>d</sub>( x, y ) = L( x, y ) / ( 1 + L( x, y ) )</span></span>

<span data-ttu-id="41767-139">其中：</span><span class="sxs-lookup"><span data-stu-id="41767-139">Where:</span></span>

-   <span data-ttu-id="41767-140">L<sub>d</sub> ( x、y ) 壓縮和縮放亮度（圖元） ( x，y ) </span><span class="sxs-lookup"><span data-stu-id="41767-140">L<sub>d</sub>( x, y ) - compressed and scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="41767-141">套用調整之後的影像索引鍵值</span><span class="sxs-lookup"><span data-stu-id="41767-141">a - image key value after applying the scaling</span></span>

<span data-ttu-id="41767-142">此運算子會將高 luminances 的級別調整為 1/L，並將低 luminances 比例調整為1。</span><span class="sxs-lookup"><span data-stu-id="41767-142">This operator scales high luminances by 1/L and low luminances by 1.</span></span> <span data-ttu-id="41767-143">如需詳細資訊，請參閱下列文章。</span><span class="sxs-lookup"><span data-stu-id="41767-143">For more details, see the following paper.</span></span>

<span data-ttu-id="41767-144">Reinhard、Erik、Mike Stark、Peter Shirley 和 James Ferwerda。</span><span class="sxs-lookup"><span data-stu-id="41767-144">Reinhard, Erik, Mike Stark, Peter Shirley, and James Ferwerda.</span></span> <span data-ttu-id="41767-145">「[數位影像的攝影語氣複製品](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf)」。</span><span class="sxs-lookup"><span data-stu-id="41767-145">["Photographic Tone Reproduction for Digital Images"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span></span> <span data-ttu-id="41767-146">關於圖形 (TOG) 、電腦圖形和互動式技術的29年會議記錄， (SIGGRAPH) ，267-276。</span><span class="sxs-lookup"><span data-stu-id="41767-146">ACM Transactions on Graphics (TOG), Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques (SIGGRAPH), pp. 267-276.</span></span> <span data-ttu-id="41767-147">紐約，紐約州：按下，2002。</span><span class="sxs-lookup"><span data-stu-id="41767-147">New York, NY: ACM Press, 2002.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41767-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="41767-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41767-149">Advanced 主題</span><span class="sxs-lookup"><span data-stu-id="41767-149">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 



