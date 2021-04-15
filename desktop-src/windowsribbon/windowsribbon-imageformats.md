---
title: 指定功能區影像資源
description: Windows 功能區架構是一種豐富的命令呈現系統，其設計目的是要在功能區使用者介面上廣泛地支援影像資源， (UI) 。 所有影像資源都是在功能區標記中宣告，或從功能區主機應用程式進行查詢。
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Windows 功能區，影像資源
- 功能區、影像資源
- Windows 功能區，透明度
- 功能區、透明度
- Windows 功能區，色彩深度
- 功能區、色彩深度
- Windows 功能區，對比
- 功能區，對比
- Windows 功能區中的影像資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463548"
---
# <a name="specifying-ribbon-image-resources"></a><span data-ttu-id="92b6c-113">指定功能區影像資源</span><span class="sxs-lookup"><span data-stu-id="92b6c-113">Specifying Ribbon Image Resources</span></span>

<span data-ttu-id="92b6c-114">Windows 功能區架構是一種豐富的命令呈現系統，其設計目的是要在功能區使用者介面上廣泛地支援影像資源， (UI) 。</span><span class="sxs-lookup"><span data-stu-id="92b6c-114">As a rich command presentation system, the Windows Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="92b6c-115">所有影像資源都是在 [功能區標記](windowsribbon-schema.md) 中宣告，或從功能區主機應用程式進行查詢。</span><span class="sxs-lookup"><span data-stu-id="92b6c-115">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="92b6c-116">針對 Windows 8 和更新版本，功能區架構支援下列圖形格式：32位 ARGB 點陣圖 (BMP) 檔和可移植網狀圖形 (PNG) 具有透明度的檔。</span><span class="sxs-lookup"><span data-stu-id="92b6c-116">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="92b6c-117">針對 Windows 7 及更早版本，映射資源必須符合 Windows 中所使用的標準 BMP 圖形格式。</span><span class="sxs-lookup"><span data-stu-id="92b6c-117">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="92b6c-118">如果提供不支援的影像格式給架構，則可能會發生編譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="92b6c-118">A compilation error may occur if an unsupported image format is supplied to the framework.</span></span>

 

## <a name="image-sizes"></a><span data-ttu-id="92b6c-119">映射大小</span><span class="sxs-lookup"><span data-stu-id="92b6c-119">Image Sizes</span></span>

<span data-ttu-id="92b6c-120">若要在調整應用程式視窗大小時提供功能區控制項配置的更大彈性，功能區架構會以下列兩種大小的其中一種來接受和轉譯影像：大型或小型。</span><span class="sxs-lookup"><span data-stu-id="92b6c-120">To provide greater flexibility for Ribbon control layouts when resizing an application window, the Ribbon framework accepts and renders images in one of two sizes: large or small.</span></span>

<span data-ttu-id="92b6c-121">下圖說明透過彈性控制項配置支援多個功能區大小的功能區應用程式，以及使用可用的小型影像來取代大型影像。</span><span class="sxs-lookup"><span data-stu-id="92b6c-121">The following images illustrate a Ribbon application that supports multiple Ribbon sizes through flexible control layouts and the replacement of large images with small images where available.</span></span>

<span data-ttu-id="92b6c-122">下列螢幕擷取畫面顯示具有縮放控制項大型影像的功能區。</span><span class="sxs-lookup"><span data-stu-id="92b6c-122">The following screen shot shows the Ribbon with large images for the Zoom controls.</span></span>

![螢幕擷取畫面，顯示使用縮放控制項之大型影像的功能區。](images/overviews/imageresources-largeimage.png)

<span data-ttu-id="92b6c-124">下列螢幕擷取畫面顯示相同的功能區，以縮放控制項的小型影像調整大小</span><span class="sxs-lookup"><span data-stu-id="92b6c-124">The following screen shot shows the same Ribbon resized with small images for the Zoom controls</span></span>

![螢幕擷取畫面，顯示針對縮放控制項使用小型影像的功能區。](images/overviews/imageresources-smallimage.png)

<span data-ttu-id="92b6c-126">下列螢幕擷取畫面顯示功能區處於隱藏狀態。</span><span class="sxs-lookup"><span data-stu-id="92b6c-126">The following screen shot shows the ribbon in hidden state.</span></span> <span data-ttu-id="92b6c-127">當所有可能的控制項版面配置都已用盡，而且無法使用可用的應用程式工作區來轉譯功能區時，就會隱藏功能區。</span><span class="sxs-lookup"><span data-stu-id="92b6c-127">The ribbon is hidden when all potential control layouts have been exhausted and the ribbon cannot be rendered with a usable application workspace.</span></span>

![顯示折迭功能區的螢幕擷取畫面。](images/overviews/imageresources-noimage.png)

<span data-ttu-id="92b6c-129">若為任何影像，確切的圖元大小取決於所使用監視器的顯示解析度或每英寸 (DPI) 的點。</span><span class="sxs-lookup"><span data-stu-id="92b6c-129">For any image, the exact pixel size is dependent on the display resolution, or dots per inch (dpi), of the monitor being used.</span></span> <span data-ttu-id="92b6c-130">在 96 DPI 時，大型影像的大小為32x32 圖元，而小型影像的大小為16x16 圖元。</span><span class="sxs-lookup"><span data-stu-id="92b6c-130">At 96 dpi, large images are 32x32 pixels in size and small images are 16x16 pixels in size.</span></span> <span data-ttu-id="92b6c-131">影像大小會以線性方式增加，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="92b6c-131">The image sizes increase in a linear fashion relative to dpi as illustrated in the following table.</span></span>



| <span data-ttu-id="92b6c-132">DPI</span><span class="sxs-lookup"><span data-stu-id="92b6c-132">DPI</span></span>     | <span data-ttu-id="92b6c-133">小型影像</span><span class="sxs-lookup"><span data-stu-id="92b6c-133">Small Image</span></span>  | <span data-ttu-id="92b6c-134">大型影像</span><span class="sxs-lookup"><span data-stu-id="92b6c-134">Large Image</span></span>  |
|---------|--------------|--------------|
| <span data-ttu-id="92b6c-135">96 DPI</span><span class="sxs-lookup"><span data-stu-id="92b6c-135">96 dpi</span></span>  | <span data-ttu-id="92b6c-136">16x16 圖元</span><span class="sxs-lookup"><span data-stu-id="92b6c-136">16x16 pixels</span></span> | <span data-ttu-id="92b6c-137">32x32 圖元</span><span class="sxs-lookup"><span data-stu-id="92b6c-137">32x32 pixels</span></span> |
| <span data-ttu-id="92b6c-138">120 DPI</span><span class="sxs-lookup"><span data-stu-id="92b6c-138">120 dpi</span></span> | <span data-ttu-id="92b6c-139">20x20 圖元</span><span class="sxs-lookup"><span data-stu-id="92b6c-139">20x20 pixels</span></span> | <span data-ttu-id="92b6c-140">40x40 圖元</span><span class="sxs-lookup"><span data-stu-id="92b6c-140">40x40 pixels</span></span> |
| <span data-ttu-id="92b6c-141">144 DPI</span><span class="sxs-lookup"><span data-stu-id="92b6c-141">144 dpi</span></span> | <span data-ttu-id="92b6c-142">24x24 圖元</span><span class="sxs-lookup"><span data-stu-id="92b6c-142">24x24 pixels</span></span> | <span data-ttu-id="92b6c-143">48x48 圖元</span><span class="sxs-lookup"><span data-stu-id="92b6c-143">48x48 pixels</span></span> |
| <span data-ttu-id="92b6c-144">192 DPI</span><span class="sxs-lookup"><span data-stu-id="92b6c-144">192 dpi</span></span> | <span data-ttu-id="92b6c-145">32x32 圖元</span><span class="sxs-lookup"><span data-stu-id="92b6c-145">32x32 pixels</span></span> | <span data-ttu-id="92b6c-146">64x64 圖元</span><span class="sxs-lookup"><span data-stu-id="92b6c-146">64x64 pixels</span></span> |



 

<span data-ttu-id="92b6c-147">功能區架構會視需要調整影像資源。</span><span class="sxs-lookup"><span data-stu-id="92b6c-147">The Ribbon framework scales image resources as required.</span></span> <span data-ttu-id="92b6c-148">不過，由於調整大小可能會產生不必要的成品和影像效能，因此強烈建議應用程式提供一組小型的影像資源，以跨越各種常用的 DPI 設定。</span><span class="sxs-lookup"><span data-stu-id="92b6c-148">However, because resizing may yield undesirable artifacts and image degradation, it is highly recommended that the application provide a small set of image resources that span various commonly used dpi settings.</span></span> <span data-ttu-id="92b6c-149">如果找不到完全相符的，則最接近的影像會向上或向下擴充。</span><span class="sxs-lookup"><span data-stu-id="92b6c-149">If an exact match is not found, the nearest image will be scaled up or down.</span></span>

<span data-ttu-id="92b6c-150">為了方便這項工作，您可以使用每個 [**命令**](windowsribbon-element-command.md)專案的一組 [**影像**](windowsribbon-element-image.md)元素，在功能區標記中宣告影像資源。</span><span class="sxs-lookup"><span data-stu-id="92b6c-150">To facilitate this, image resources can be declared in Ribbon markup by using a set of [**Image**](windowsribbon-element-image.md) elements for each [**Command**](windowsribbon-element-command.md) element.</span></span> <span data-ttu-id="92b6c-151">在執行時間，架構會根據每個 **影像** 元素的 *MinDPI* 屬性，選取要顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="92b6c-151">At run time, the framework selects the image to display based on the *MinDPI* attribute of each **Image** element.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="92b6c-152">當設計用來支援特定螢幕 DPI 設定的影像資源集合透過一組 [**影像**](windowsribbon-element-image.md)元素提供給功能區架構時，架構會使用 *MinDPI* 屬性值符合目前螢幕 DPI 設定的 **影像**。</span><span class="sxs-lookup"><span data-stu-id="92b6c-152">When a collection of image resources that are designed to support specific screen dpi settings is supplied to the Ribbon framework through a set of [**Image**](windowsribbon-element-image.md) elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>
>
> <span data-ttu-id="92b6c-153">如果未使用符合目前螢幕 DPI 設定的 *MinDPI* 值來宣告 [**影像**](windowsribbon-element-image.md)元素，則架構會挑選最接近目前螢幕 DPI 設定的最接近 *MinDPI* 值的 **影像**，並向上調整影像資源。</span><span class="sxs-lookup"><span data-stu-id="92b6c-153">If no [**Image**](windowsribbon-element-image.md) element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="92b6c-154">否則，如果未使用 *MinDPI* 屬性值（小於目前的螢幕 DPI 設定）來宣告 **影像** 元素，則架構會挑選大於目前螢幕 DPI 設定的最接近 *MinDPI* 值，並將影像資源向下調整。</span><span class="sxs-lookup"><span data-stu-id="92b6c-154">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

 

<span data-ttu-id="92b6c-155">下列範例說明如何宣告一組影像來容納各種功能區大小和系統設定。</span><span class="sxs-lookup"><span data-stu-id="92b6c-155">The following example illustrates how to declare a set of images to accommodate various Ribbon sizes and system settings.</span></span>


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



<span data-ttu-id="92b6c-156">如果在執行時間的標記中宣告的影像因為任何原因而失效，則會查詢主機應用程式是否有新的影像。</span><span class="sxs-lookup"><span data-stu-id="92b6c-156">If images declared in markup are invalidated at run time for any reason, the host application is queried for new images.</span></span> <span data-ttu-id="92b6c-157">當這些映射以程式設計方式產生和載入時，應用程式應該會嘗試傳回根據 [SM \_ CXICON 系統](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)計量所決定的預設系統圖示大小來調整大小的影像。</span><span class="sxs-lookup"><span data-stu-id="92b6c-157">When these images are generated and loaded programmatically, the application should attempt to return images that are sized according to the default system icon sizes determined by the [SM\_CXICON system metric](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span></span>

> [!Note]  
> <span data-ttu-id="92b6c-158">大型影像的 sm CXICON 大小為 sm \_ \_ CXICON，而小型影像的大小為 sm \_ CXICON/2，sm \_ CXICON/2。</span><span class="sxs-lookup"><span data-stu-id="92b6c-158">Large images have a size of SM\_CXICON by SM\_CXICON and small images have a size of SM\_CXICON/2 by SM\_CXICON/2.</span></span>

 

## <a name="color-depth-transparency-and-contrast"></a><span data-ttu-id="92b6c-159">色彩深度、透明度和對比</span><span class="sxs-lookup"><span data-stu-id="92b6c-159">Color Depth, Transparency, and Contrast</span></span>

<span data-ttu-id="92b6c-160">一般影像預期會在每圖元32位 (BPP) ARGB 像素格式，並調整為預設系統圖示大小。</span><span class="sxs-lookup"><span data-stu-id="92b6c-160">Regular images are expected to be in 32 bits per pixel (BPP) ARGB pixel format and scaled to the default system icon size.</span></span> <span data-ttu-id="92b6c-161">此格式支援透明和消除鋸齒 (使用每個通道) 的8位。</span><span class="sxs-lookup"><span data-stu-id="92b6c-161">This format supports both transparency and antialiasing (using 8 bits per channel).</span></span>

> [!WARNING]
> <span data-ttu-id="92b6c-162">在載入或儲存 32 BPP 影像時，許多影像編輯工具都不會保留最高順序的8位 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="92b6c-162">Many image editing tools do not preserve the highest order 8-bit alpha channel when loading or saving 32 BPP images.</span></span>

 

<span data-ttu-id="92b6c-163">若要在高對比模式中正確顯示影像，其必須為 4 BPP palletized 像素格式。</span><span class="sxs-lookup"><span data-stu-id="92b6c-163">For an image to display correctly in high-contrast mode, it must be in a 4 BPP palletized pixel format.</span></span> <span data-ttu-id="92b6c-164">轉譯影像時，功能區架構會根據影像的高對比內容重新對應特定色彩。</span><span class="sxs-lookup"><span data-stu-id="92b6c-164">When the image is rendered, the Ribbon framework remaps specific colors based on the high-contrast context of the image.</span></span>

<span data-ttu-id="92b6c-165">下表列出架構的高對比色彩轉譯行為。</span><span class="sxs-lookup"><span data-stu-id="92b6c-165">The following table lists the high-contrast color rendering behavior of the framework.</span></span>



<span data-ttu-id="92b6c-166">像素色彩</span><span class="sxs-lookup"><span data-stu-id="92b6c-166">Pixel color</span></span>

<span data-ttu-id="92b6c-167">RGB 值</span><span class="sxs-lookup"><span data-stu-id="92b6c-167">RGB value</span></span>

<span data-ttu-id="92b6c-168">行為</span><span class="sxs-lookup"><span data-stu-id="92b6c-168">Behavior</span></span>

<span data-ttu-id="92b6c-169">白色背景</span><span class="sxs-lookup"><span data-stu-id="92b6c-169">White background</span></span>

<span data-ttu-id="92b6c-170">深色背景</span><span class="sxs-lookup"><span data-stu-id="92b6c-170">Dark Background</span></span>

<span data-ttu-id="92b6c-171">品紅</span><span class="sxs-lookup"><span data-stu-id="92b6c-171">MAGENTA</span></span>

<span data-ttu-id="92b6c-172">800080</span><span class="sxs-lookup"><span data-stu-id="92b6c-172">800080</span></span>

<span data-ttu-id="92b6c-173">透明</span><span class="sxs-lookup"><span data-stu-id="92b6c-173">Transparent</span></span>

<span data-ttu-id="92b6c-174">透明</span><span class="sxs-lookup"><span data-stu-id="92b6c-174">Transparent</span></span>

<span data-ttu-id="92b6c-175">黑</span><span class="sxs-lookup"><span data-stu-id="92b6c-175">BLACK</span></span>

<span data-ttu-id="92b6c-176">000000</span><span class="sxs-lookup"><span data-stu-id="92b6c-176">000000</span></span>

<span data-ttu-id="92b6c-177">色彩 \_ WINDOWTEXT</span><span class="sxs-lookup"><span data-stu-id="92b6c-177">COLOR\_WINDOWTEXT</span></span>

<span data-ttu-id="92b6c-178">白色</span><span class="sxs-lookup"><span data-stu-id="92b6c-178">WHITE</span></span>

<span data-ttu-id="92b6c-179">白色</span><span class="sxs-lookup"><span data-stu-id="92b6c-179">WHITE</span></span>

<span data-ttu-id="92b6c-180">FFFFFF</span><span class="sxs-lookup"><span data-stu-id="92b6c-180">FFFFFF</span></span>

<span data-ttu-id="92b6c-181">色彩 \_ 視窗</span><span class="sxs-lookup"><span data-stu-id="92b6c-181">COLOR\_WINDOW</span></span>

<span data-ttu-id="92b6c-182">黑</span><span class="sxs-lookup"><span data-stu-id="92b6c-182">BLACK</span></span>

<span data-ttu-id="92b6c-183">暗灰色</span><span class="sxs-lookup"><span data-stu-id="92b6c-183">DARK GRAY</span></span>

<span data-ttu-id="92b6c-184">808080</span><span class="sxs-lookup"><span data-stu-id="92b6c-184">808080</span></span>

<span data-ttu-id="92b6c-185">色彩 \_ 3DSHADOW</span><span class="sxs-lookup"><span data-stu-id="92b6c-185">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="92b6c-186">色彩 \_ 3DSHADOW</span><span class="sxs-lookup"><span data-stu-id="92b6c-186">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="92b6c-187">灰色</span><span class="sxs-lookup"><span data-stu-id="92b6c-187">GRAY</span></span>

<span data-ttu-id="92b6c-188">C0C0C0</span><span class="sxs-lookup"><span data-stu-id="92b6c-188">C0C0C0</span></span>

<span data-ttu-id="92b6c-189">色彩 \_ 3DFACE</span><span class="sxs-lookup"><span data-stu-id="92b6c-189">COLOR\_3DFACE</span></span>

<span data-ttu-id="92b6c-190">色彩 \_ 3DFACE</span><span class="sxs-lookup"><span data-stu-id="92b6c-190">COLOR\_3DFACE</span></span>

<span data-ttu-id="92b6c-191">淺灰色</span><span class="sxs-lookup"><span data-stu-id="92b6c-191">LIGHT GRAY</span></span>

<span data-ttu-id="92b6c-192">DFDFDF</span><span class="sxs-lookup"><span data-stu-id="92b6c-192">DFDFDF</span></span>

<span data-ttu-id="92b6c-193">色彩 \_ 3DLIGHT</span><span class="sxs-lookup"><span data-stu-id="92b6c-193">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="92b6c-194">色彩 \_ 3DLIGHT</span><span class="sxs-lookup"><span data-stu-id="92b6c-194">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="92b6c-195">深藍色</span><span class="sxs-lookup"><span data-stu-id="92b6c-195">DARK BLUE</span></span>

<span data-ttu-id="92b6c-196">000080</span><span class="sxs-lookup"><span data-stu-id="92b6c-196">000080</span></span>

<span data-ttu-id="92b6c-197">n/a</span><span class="sxs-lookup"><span data-stu-id="92b6c-197">n/a</span></span>

<span data-ttu-id="92b6c-198">白色</span><span class="sxs-lookup"><span data-stu-id="92b6c-198">WHITE</span></span>



 

<span data-ttu-id="92b6c-199">如需功能區架構所支援之影像格式的詳細資訊，請參閱下列各項：</span><span class="sxs-lookup"><span data-stu-id="92b6c-199">For more information on the image formats supported by the Ribbon framework, see the following:</span></span>

-   <span data-ttu-id="92b6c-200">[BITMAPINFOHEADER 結構](/previous-versions//dd183376(v=vs.85)) -描述 32 BPP ARGB 像素格式。</span><span class="sxs-lookup"><span data-stu-id="92b6c-200">[BITMAPINFOHEADER structure](/previous-versions//dd183376(v=vs.85)) - describes the 32 BPP ARGB pixel format.</span></span>
-   <span data-ttu-id="92b6c-201">[CreateDIBSection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) 函式-說明如何建立 32 BPP ARGB 像素格式的影像。</span><span class="sxs-lookup"><span data-stu-id="92b6c-201">[CreateDIBSection function](/windows/win32/api/wingdi/nf-wingdi-createdibsection) - describes how to create a 32 BPP ARGB pixel format image.</span></span>
-   <span data-ttu-id="92b6c-202">[LoadImage](/windows/win32/api/winuser/nf-winuser-loadimagea) 函式-說明如何載入 32 BPP ARGB 像素格式的影像。</span><span class="sxs-lookup"><span data-stu-id="92b6c-202">[LoadImage function](/windows/win32/api/winuser/nf-winuser-loadimagea) - describes how to load a 32 BPP ARGB pixel format image.</span></span>

## <a name="accessibility"></a><span data-ttu-id="92b6c-203">協助工具選項</span><span class="sxs-lookup"><span data-stu-id="92b6c-203">Accessibility</span></span>

<span data-ttu-id="92b6c-204">依賴映射資源來提供資訊、傳達控制項功能，以及公開應用程式狀態，以在應用程式設計和開發期間增加協助工具需求的需求。</span><span class="sxs-lookup"><span data-stu-id="92b6c-204">Relying on image resources to provide information, convey control functionality, and expose application state, increases the need for accessibility requirements during application design and development.</span></span>

<span data-ttu-id="92b6c-205">針對基本的高對比支援，功能區允許在高對比主題為使用中時，顯示一組個別的影像檔案。</span><span class="sxs-lookup"><span data-stu-id="92b6c-205">For basic high contrast support, the Ribbon allows for a separate set of image files to be displayed when a high-contrast theme is active.</span></span> <span data-ttu-id="92b6c-206">這些影像可以是 32 BPP 或 4 BPP，其中的色彩會對應到特殊的小元件，其中的色彩會根據作用中高對比主題的前景和背景色彩反轉。</span><span class="sxs-lookup"><span data-stu-id="92b6c-206">These images can be 32 BPP or 4 BPP, with colors mapped to a special palette where dark and light colors are inverted depending on the foreground and background colors of the active high-contrast theme.</span></span>

<span data-ttu-id="92b6c-207">下列範例示範如何在功能區標記中宣告高對比影像資源：</span><span class="sxs-lookup"><span data-stu-id="92b6c-207">The following example demonstrates how high-contrast image resources are declared in Ribbon markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="92b6c-208">相關主題</span><span class="sxs-lookup"><span data-stu-id="92b6c-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92b6c-209">**SmallImages**</span><span class="sxs-lookup"><span data-stu-id="92b6c-209">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[<span data-ttu-id="92b6c-210">UI \_ PKEY \_ SmallImage</span><span class="sxs-lookup"><span data-stu-id="92b6c-210">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[<span data-ttu-id="92b6c-211">**LargeImages**</span><span class="sxs-lookup"><span data-stu-id="92b6c-211">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[<span data-ttu-id="92b6c-212">UI \_ PKEY \_ LargeImage</span><span class="sxs-lookup"><span data-stu-id="92b6c-212">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[<span data-ttu-id="92b6c-213">**SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="92b6c-213">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="92b6c-214">UI \_ PKEY \_ SmallHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="92b6c-214">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[<span data-ttu-id="92b6c-215">**LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="92b6c-215">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="92b6c-216">UI \_ PKEY \_ LargeHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="92b6c-216">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 