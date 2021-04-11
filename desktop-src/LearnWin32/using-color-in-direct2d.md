---
title: 在 Direct2D 中使用色彩
description: 在 Direct2D 中使用色彩
ms.assetid: 74b1f12c-b1de-4df1-85ba-0cf7a0009499
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb195a4ad0bdd9ff32f1123a8a57ff2ce0aadbde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314824"
---
# <a name="using-color-in-direct2d"></a><span data-ttu-id="e6164-103">在 Direct2D 中使用色彩</span><span class="sxs-lookup"><span data-stu-id="e6164-103">Using Color in Direct2D</span></span>

<span data-ttu-id="e6164-104">Direct2D 使用 RGB 色彩模型，其中的色彩是藉由結合紅色、綠色和藍色的不同值形成。</span><span class="sxs-lookup"><span data-stu-id="e6164-104">Direct2D uses the RGB color model, in which colors are formed by combining different values of red, green, and blue.</span></span> <span data-ttu-id="e6164-105">第四個元件（Alpha）測量圖元的透明度。</span><span class="sxs-lookup"><span data-stu-id="e6164-105">A fourth component, alpha, measures the transparency of a pixel.</span></span> <span data-ttu-id="e6164-106">在 Direct2D 中，每個元件都是一個範圍為 0.0 1.0 的浮點值 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="e6164-106">In Direct2D, each of these components is a floating-point value with a range of \[0.0 1.0\].</span></span> <span data-ttu-id="e6164-107">針對三個色彩元件，此值會測量色彩的濃度。</span><span class="sxs-lookup"><span data-stu-id="e6164-107">For the three color components, the value measures the intensity of the color.</span></span> <span data-ttu-id="e6164-108">針對 Alpha 元件，0.0 表示完全透明，1.0 表示完全不透明。</span><span class="sxs-lookup"><span data-stu-id="e6164-108">For the alpha component, 0.0 means completely transparent, and 1.0 means completely opaque.</span></span> <span data-ttu-id="e6164-109">下表顯示各種100% 濃度的組合所產生的色彩。</span><span class="sxs-lookup"><span data-stu-id="e6164-109">The following table shows the colors that result from various combinations of 100% intensity.</span></span>



| <span data-ttu-id="e6164-110">紅色</span><span class="sxs-lookup"><span data-stu-id="e6164-110">Red</span></span> | <span data-ttu-id="e6164-111">綠色</span><span class="sxs-lookup"><span data-stu-id="e6164-111">Green</span></span> | <span data-ttu-id="e6164-112">藍色</span><span class="sxs-lookup"><span data-stu-id="e6164-112">Blue</span></span> | <span data-ttu-id="e6164-113">色彩</span><span class="sxs-lookup"><span data-stu-id="e6164-113">Color</span></span>   |
|-----|-------|------|---------|
| <span data-ttu-id="e6164-114">0</span><span class="sxs-lookup"><span data-stu-id="e6164-114">0</span></span>   | <span data-ttu-id="e6164-115">0</span><span class="sxs-lookup"><span data-stu-id="e6164-115">0</span></span>     | <span data-ttu-id="e6164-116">0</span><span class="sxs-lookup"><span data-stu-id="e6164-116">0</span></span>    | <span data-ttu-id="e6164-117">黑色</span><span class="sxs-lookup"><span data-stu-id="e6164-117">Black</span></span>   |
| <span data-ttu-id="e6164-118">1</span><span class="sxs-lookup"><span data-stu-id="e6164-118">1</span></span>   | <span data-ttu-id="e6164-119">0</span><span class="sxs-lookup"><span data-stu-id="e6164-119">0</span></span>     | <span data-ttu-id="e6164-120">0</span><span class="sxs-lookup"><span data-stu-id="e6164-120">0</span></span>    | <span data-ttu-id="e6164-121">紅色</span><span class="sxs-lookup"><span data-stu-id="e6164-121">Red</span></span>     |
| <span data-ttu-id="e6164-122">0</span><span class="sxs-lookup"><span data-stu-id="e6164-122">0</span></span>   | <span data-ttu-id="e6164-123">1</span><span class="sxs-lookup"><span data-stu-id="e6164-123">1</span></span>     | <span data-ttu-id="e6164-124">0</span><span class="sxs-lookup"><span data-stu-id="e6164-124">0</span></span>    | <span data-ttu-id="e6164-125">綠色</span><span class="sxs-lookup"><span data-stu-id="e6164-125">Green</span></span>   |
| <span data-ttu-id="e6164-126">0</span><span class="sxs-lookup"><span data-stu-id="e6164-126">0</span></span>   | <span data-ttu-id="e6164-127">0</span><span class="sxs-lookup"><span data-stu-id="e6164-127">0</span></span>     | <span data-ttu-id="e6164-128">1</span><span class="sxs-lookup"><span data-stu-id="e6164-128">1</span></span>    | <span data-ttu-id="e6164-129">藍色</span><span class="sxs-lookup"><span data-stu-id="e6164-129">Blue</span></span>    |
| <span data-ttu-id="e6164-130">0</span><span class="sxs-lookup"><span data-stu-id="e6164-130">0</span></span>   | <span data-ttu-id="e6164-131">1</span><span class="sxs-lookup"><span data-stu-id="e6164-131">1</span></span>     | <span data-ttu-id="e6164-132">1</span><span class="sxs-lookup"><span data-stu-id="e6164-132">1</span></span>    | <span data-ttu-id="e6164-133">11：青色</span><span class="sxs-lookup"><span data-stu-id="e6164-133">Cyan</span></span>    |
| <span data-ttu-id="e6164-134">1</span><span class="sxs-lookup"><span data-stu-id="e6164-134">1</span></span>   | <span data-ttu-id="e6164-135">0</span><span class="sxs-lookup"><span data-stu-id="e6164-135">0</span></span>     | <span data-ttu-id="e6164-136">1</span><span class="sxs-lookup"><span data-stu-id="e6164-136">1</span></span>    | <span data-ttu-id="e6164-137">桃紅色</span><span class="sxs-lookup"><span data-stu-id="e6164-137">Magenta</span></span> |
| <span data-ttu-id="e6164-138">1</span><span class="sxs-lookup"><span data-stu-id="e6164-138">1</span></span>   | <span data-ttu-id="e6164-139">1</span><span class="sxs-lookup"><span data-stu-id="e6164-139">1</span></span>     | <span data-ttu-id="e6164-140">0</span><span class="sxs-lookup"><span data-stu-id="e6164-140">0</span></span>    | <span data-ttu-id="e6164-141">黃色</span><span class="sxs-lookup"><span data-stu-id="e6164-141">Yellow</span></span>  |
| <span data-ttu-id="e6164-142">1</span><span class="sxs-lookup"><span data-stu-id="e6164-142">1</span></span>   | <span data-ttu-id="e6164-143">1</span><span class="sxs-lookup"><span data-stu-id="e6164-143">1</span></span>     | <span data-ttu-id="e6164-144">1</span><span class="sxs-lookup"><span data-stu-id="e6164-144">1</span></span>    | <span data-ttu-id="e6164-145">白色</span><span class="sxs-lookup"><span data-stu-id="e6164-145">White</span></span>   |



 

![顯示 rgb 色彩的影像。](images/graphics13.png)

<span data-ttu-id="e6164-147">0和1之間的色彩值會導致這些純量的不同陰影。</span><span class="sxs-lookup"><span data-stu-id="e6164-147">Color values between 0 and 1 result in different shades of these pure colors.</span></span> <span data-ttu-id="e6164-148">Direct2D 使用 [**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f) 結構來表示色彩。</span><span class="sxs-lookup"><span data-stu-id="e6164-148">Direct2D uses the [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure to represent colors.</span></span> <span data-ttu-id="e6164-149">例如，下列程式碼會指定洋紅。</span><span class="sxs-lookup"><span data-stu-id="e6164-149">For example, the following code specifies magenta.</span></span>


```C++
    // Initialize a magenta color.

    D2D1_COLOR_F clr;
    clr.r = 1;
    clr.g = 0;
    clr.b = 1;
    clr.a = 1;  // Opaque.
```



<span data-ttu-id="e6164-150">您也可以使用衍生自 [**D2D1 \_ color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)結構的 [**D2D1：： ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)類別來指定色彩。</span><span class="sxs-lookup"><span data-stu-id="e6164-150">You can also specify a color using the [**D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class, which derives from the [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure.</span></span>


```C++
    // Equivalent to the previous example.

    D2D1::ColorF clr(1, 0, 1, 1);
```



## <a name="alpha-blending"></a><span data-ttu-id="e6164-151">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="e6164-151">Alpha Blending</span></span>

<span data-ttu-id="e6164-152">Alpha 混色藉由使用下列公式，將前景色彩與背景色彩混合來建立半透明區域。</span><span class="sxs-lookup"><span data-stu-id="e6164-152">Alpha blending creates translucent areas by blending the foreground color with the background color, using the following formula.</span></span>

<dl> <span data-ttu-id="e6164-153">color = af \* Cf + (1-af) \* Cb</span><span class="sxs-lookup"><span data-stu-id="e6164-153">color = af \* Cf + (1 - af) \* Cb</span></span>  
</dl>

<span data-ttu-id="e6164-154">其中 *Cb* 是背景色彩、 *Cf* 是前景色彩，而 *af* 是前景色彩的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="e6164-154">where *Cb* is the background color, *Cf* is the foreground color, and *af* is the alpha value of the foreground color.</span></span> <span data-ttu-id="e6164-155">此公式會成對套用至每個色彩元件。</span><span class="sxs-lookup"><span data-stu-id="e6164-155">This formula is applied pairwise to each color component.</span></span> <span data-ttu-id="e6164-156">例如，假設前景色彩是 **(r = 1.0、G = 0.4、B = 0.0)**（ **Alpha = 0.6**），背景色彩為 **(R = 0.0、G = 0.5、B = 1.0)**。</span><span class="sxs-lookup"><span data-stu-id="e6164-156">For example, suppose the foreground color is **(R = 1.0, G = 0.4, B = 0.0)**, with **alpha = 0.6**, and the background color is **(R = 0.0, G = 0.5, B = 1.0)**.</span></span> <span data-ttu-id="e6164-157">產生的 Alpha 混合色彩為：</span><span class="sxs-lookup"><span data-stu-id="e6164-157">The resulting alpha-blended color is:</span></span>

<span data-ttu-id="e6164-158">R = (1.0 \* 0.6 + 0 \* 0.4) = 6</span><span class="sxs-lookup"><span data-stu-id="e6164-158">R = (1.0 \* 0.6 + 0 \* 0.4) = .6</span></span>   
<span data-ttu-id="e6164-159">G = (0.4 \* 0.6 + 0.5 \* 0.4) =. 44</span><span class="sxs-lookup"><span data-stu-id="e6164-159">G = (0.4 \* 0.6 + 0.5 \* 0.4) = .44</span></span>  
<span data-ttu-id="e6164-160">B = (0 \* 0.6 + 1.0 \* 0.4) =. 40</span><span class="sxs-lookup"><span data-stu-id="e6164-160">B = (0 \* 0.6 + 1.0 \* 0.4) = .40</span></span>  

<span data-ttu-id="e6164-161">下圖顯示此混合作業的結果。</span><span class="sxs-lookup"><span data-stu-id="e6164-161">The following image shows the result of this blending operation.</span></span>

![顯示 Alpha 混色的影像。](images/graphics15.png)

## <a name="pixel-formats"></a><span data-ttu-id="e6164-163">像素格式</span><span class="sxs-lookup"><span data-stu-id="e6164-163">Pixel Formats</span></span>

<span data-ttu-id="e6164-164">[**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)結構不會描述圖元在記憶體中的表示方式。</span><span class="sxs-lookup"><span data-stu-id="e6164-164">The [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure does not describe how a pixel is represented in memory.</span></span> <span data-ttu-id="e6164-165">在大多數情況下，這並不重要。</span><span class="sxs-lookup"><span data-stu-id="e6164-165">In most cases, that doesn't matter.</span></span> <span data-ttu-id="e6164-166">Direct2D 會處理將色彩資訊翻譯成圖元的所有內部詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e6164-166">Direct2D handles all of the internal details of translating color information into pixels.</span></span> <span data-ttu-id="e6164-167">但是，如果您直接使用記憶體中的點陣圖，或結合 Direct2D 與 Direct3D 或 GDI，您可能必須知道像素格式。</span><span class="sxs-lookup"><span data-stu-id="e6164-167">But you might need to know the pixel format if you are working directly with a bitmap in memory, or if you combine Direct2D with Direct3D or GDI.</span></span>

<span data-ttu-id="e6164-168">[**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)列舉定義了像素格式的清單。</span><span class="sxs-lookup"><span data-stu-id="e6164-168">The [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration defines a list of pixel formats.</span></span> <span data-ttu-id="e6164-169">這份清單相當長，但只有少數幾個與 Direct2D 相關。</span><span class="sxs-lookup"><span data-stu-id="e6164-169">The list is fairly long, but only a few of them are relevant to Direct2D.</span></span> <span data-ttu-id="e6164-170"> (其他專案則是由 Direct3D) 使用。</span><span class="sxs-lookup"><span data-stu-id="e6164-170">(The others are used by Direct3D).</span></span>



| <span data-ttu-id="e6164-171">像素格式</span><span class="sxs-lookup"><span data-stu-id="e6164-171">Pixel format</span></span>                                                                                                                           | <span data-ttu-id="e6164-172">Description</span><span class="sxs-lookup"><span data-stu-id="e6164-172">Description</span></span>                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6164-173"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="e6164-173"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>**DXGI\_FORMAT\_B8G8R8A8\_UNORM**</span></span><br/> | <span data-ttu-id="e6164-174">這是最常見的像素格式。</span><span class="sxs-lookup"><span data-stu-id="e6164-174">This is the most common pixel format.</span></span> <span data-ttu-id="e6164-175">所有圖元元件 (紅色、綠色、藍色和 Alpha) 為8位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="e6164-175">All pixel components (red, green, blue, and alpha) are 8-bit unsigned integers.</span></span> <span data-ttu-id="e6164-176">元件會以 *BGRA* 順序排列在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="e6164-176">The components are arranged in *BGRA* order in memory.</span></span> <span data-ttu-id="e6164-177"> (請參閱下面的圖例。 ) </span><span class="sxs-lookup"><span data-stu-id="e6164-177">(See illustration that follows.)</span></span><br/>                                          |
| <span data-ttu-id="e6164-178"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="e6164-178"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>**DXGI\_FORMAT\_R8G8B8A8\_UNORM**</span></span><br/> | <span data-ttu-id="e6164-179">圖元元件是以 *RGBA* 順序為8位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="e6164-179">Pixel components are 8-bit unsigned integers, in *RGBA* order.</span></span> <span data-ttu-id="e6164-180">換句話說，會交換紅色和藍色的元件，相對於 **DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**。</span><span class="sxs-lookup"><span data-stu-id="e6164-180">In other words, the red and blue components are swapped, relative to **DXGI\_FORMAT\_B8G8R8A8\_UNORM**.</span></span> <span data-ttu-id="e6164-181">只有硬體裝置才支援此格式。</span><span class="sxs-lookup"><span data-stu-id="e6164-181">This format is supported only for hardware devices.</span></span><br/>                             |
| <span data-ttu-id="e6164-182"><span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**DXGI \_ 格式 \_ A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="e6164-182"><span id="DXGI_FORMAT_A8_UNORM"></span><span id="dxgi_format_a8_unorm"></span>**DXGI\_FORMAT\_A8\_UNORM**</span></span><br/>                   | <span data-ttu-id="e6164-183">此格式包含8位 Alpha 元件，不含 RGB 元件。</span><span class="sxs-lookup"><span data-stu-id="e6164-183">This format contains an 8-bit alpha component, with no RGB components.</span></span> <span data-ttu-id="e6164-184">它很適合用來建立不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="e6164-184">It is useful for creating opacity masks.</span></span> <span data-ttu-id="e6164-185">若要閱讀有關在 Direct2D 中使用不透明度遮罩的詳細資訊，請參閱 [相容的 A8 轉譯目標總覽](/windows/desktop/Direct2D/compatible-a8-rendertargets)。</span><span class="sxs-lookup"><span data-stu-id="e6164-185">To read more about using opacity masks in Direct2D, see [Compatible A8 Render Targets Overview](/windows/desktop/Direct2D/compatible-a8-rendertargets).</span></span><br/> |



 

<span data-ttu-id="e6164-186">下圖顯示 BGRA 圖元版面配置。</span><span class="sxs-lookup"><span data-stu-id="e6164-186">The following illustration shows BGRA pixel layout.</span></span>

![顯示 bgra 圖元版面配置的圖表。](images/graphics14.png)

<span data-ttu-id="e6164-188">若要取得轉譯目標的像素格式，請呼叫 [**ID2D1RenderTarget：： GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat)。</span><span class="sxs-lookup"><span data-stu-id="e6164-188">To get the pixel format of a render target, call [**ID2D1RenderTarget::GetPixelFormat**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelformat).</span></span> <span data-ttu-id="e6164-189">像素格式可能不符合顯示器解析度。</span><span class="sxs-lookup"><span data-stu-id="e6164-189">The pixel format might not match the display resolution.</span></span> <span data-ttu-id="e6164-190">例如，顯示可能會設定為16位色彩，即使轉譯目標使用32位色彩也一樣。</span><span class="sxs-lookup"><span data-stu-id="e6164-190">For example, the display might be set to 16-bit color, even though the render target uses 32-bit color.</span></span>

### <a name="alpha-mode"></a><span data-ttu-id="e6164-191">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="e6164-191">Alpha Mode</span></span>

<span data-ttu-id="e6164-192">轉譯目標也有 Alpha 模式，它會定義如何處理 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="e6164-192">A render target also has an alpha mode, which defines how the alpha values are treated.</span></span>



| <span data-ttu-id="e6164-193">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="e6164-193">Alpha mode</span></span>                           | <span data-ttu-id="e6164-194">說明</span><span class="sxs-lookup"><span data-stu-id="e6164-194">Desciption</span></span>                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6164-195">**D2D1 \_ ALPHA \_ 模式 \_ 忽略**</span><span class="sxs-lookup"><span data-stu-id="e6164-195">**D2D1\_ALPHA\_MODE\_IGNORE**</span></span>        | <span data-ttu-id="e6164-196">不會執行任何 Alpha 混色。</span><span class="sxs-lookup"><span data-stu-id="e6164-196">No alpha blending is performed.</span></span> <span data-ttu-id="e6164-197">系統會忽略 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="e6164-197">Alpha values are ignored.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="e6164-198">**\_直接 D2D1 ALPHA \_ 模式 \_**</span><span class="sxs-lookup"><span data-stu-id="e6164-198">**D2D1\_ALPHA\_MODE\_STRAIGHT**</span></span>      | <span data-ttu-id="e6164-199">直線。</span><span class="sxs-lookup"><span data-stu-id="e6164-199">Straight alpha.</span></span> <span data-ttu-id="e6164-200">圖元的色彩元件代表 Alpha 混色之前的色彩濃度。</span><span class="sxs-lookup"><span data-stu-id="e6164-200">The color components of the pixel represent the color intensity prior to alpha blending.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="e6164-201">**預 \_ 乘的 D2D1 ALPHA \_ 模式 \_**</span><span class="sxs-lookup"><span data-stu-id="e6164-201">**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**</span></span> | <span data-ttu-id="e6164-202">預乘 Alpha。</span><span class="sxs-lookup"><span data-stu-id="e6164-202">Premultiplied alpha.</span></span> <span data-ttu-id="e6164-203">圖元的色彩元件表示色彩濃度乘以 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="e6164-203">The color components of the pixel represent the color intensity multiplied by the alpha value.</span></span> <span data-ttu-id="e6164-204">這種格式比直接 Alpha 更有效率，因為 Alpha 混色公式的 (af Cf) 的詞彙是預先計算的。</span><span class="sxs-lookup"><span data-stu-id="e6164-204">This format is more efficient to render than straight alpha, because the term (af   Cf) from the alpha-blending formula is pre-computed.</span></span> <span data-ttu-id="e6164-205">不過，這種格式不適合儲存在影像檔案中。</span><span class="sxs-lookup"><span data-stu-id="e6164-205">However, this format is not appropriate for storing in an image file.</span></span> |



 

<span data-ttu-id="e6164-206">以下是直接 Alpha 和預乘 Alpha 之間差異的範例。</span><span class="sxs-lookup"><span data-stu-id="e6164-206">Here is an example of the difference between straight alpha and premultiplied alpha.</span></span> <span data-ttu-id="e6164-207">假設想要的色彩是純紅色 (100% 濃度) 50% Alpha。</span><span class="sxs-lookup"><span data-stu-id="e6164-207">Suppose the desired color is pure red (100% intensity) with 50% alpha.</span></span> <span data-ttu-id="e6164-208">作為 Direct2D 類型，此色彩會以 (1，0，0，0.5) 表示。</span><span class="sxs-lookup"><span data-stu-id="e6164-208">As a Direct2D type, this color would be represented as (1, 0, 0, 0.5).</span></span> <span data-ttu-id="e6164-209">使用直接 Alpha 和假設為8位的色彩元件，圖元的紅色元件為0xFF。</span><span class="sxs-lookup"><span data-stu-id="e6164-209">Using straight alpha, and assuming 8-bit color components, the red component of the pixel is 0xFF.</span></span> <span data-ttu-id="e6164-210">使用預乘 Alpha，紅色的元件會以50% 為相等的0x80 來調整。</span><span class="sxs-lookup"><span data-stu-id="e6164-210">Using premultiplied alpha, the red component is scaled by 50% to equal 0x80.</span></span>

<span data-ttu-id="e6164-211">[**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)資料類型一律會使用直接 Alpha 表示色彩。</span><span class="sxs-lookup"><span data-stu-id="e6164-211">The [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) data type always represents colors using straight alpha.</span></span> <span data-ttu-id="e6164-212">如有需要，Direct2D 會將圖元轉換成預乘的 Alpha 格式。</span><span class="sxs-lookup"><span data-stu-id="e6164-212">Direct2D converts pixels to premultiplied alpha format if needed.</span></span>

<span data-ttu-id="e6164-213">如果您知道您的程式不會執行任何 Alpha 混色，請使用 **D2D1 \_ Alpha \_ 模式來 \_ 略** 過 Alpha 模式來建立呈現目標。</span><span class="sxs-lookup"><span data-stu-id="e6164-213">If you know that your program will not perform any alpha blending, create the render target with the **D2D1\_ALPHA\_MODE\_IGNORE** alpha mode.</span></span> <span data-ttu-id="e6164-214">此模式可以改善效能，因為 Direct2D 可以略過 Alpha 計算。</span><span class="sxs-lookup"><span data-stu-id="e6164-214">This mode can improve performance, because Direct2D can skip the alpha calculations.</span></span> <span data-ttu-id="e6164-215">如需詳細資訊，請參閱 [改善 Direct2D 應用程式的效能](/windows/desktop/Direct2D/improving-direct2d-performance)。</span><span class="sxs-lookup"><span data-stu-id="e6164-215">For more information, see [Improving the Performance of Direct2D Applications](/windows/desktop/Direct2D/improving-direct2d-performance).</span></span>

## <a name="next"></a><span data-ttu-id="e6164-216">下一個</span><span class="sxs-lookup"><span data-stu-id="e6164-216">Next</span></span>

[<span data-ttu-id="e6164-217">在 Direct2D 中套用轉換</span><span class="sxs-lookup"><span data-stu-id="e6164-217">Applying Transforms in Direct2D</span></span>](applying-transforms-in-direct2d.md)

 

