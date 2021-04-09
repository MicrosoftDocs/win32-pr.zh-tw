---
title: 點陣圖來源效果
description: 使用點陣圖來源效果從 IWICBitmapSource 產生 ID2D1Image，以做為效果圖形中的輸入。
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- 點陣圖來源效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a439c94f0f520b318b3cb3511775dbec58b6e139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844240"
---
# <a name="bitmap-source-effect"></a><span data-ttu-id="e75e5-104">點陣圖來源效果</span><span class="sxs-lookup"><span data-stu-id="e75e5-104">Bitmap source effect</span></span>

<span data-ttu-id="e75e5-105">使用點陣圖來源效果從 [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource)產生 [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) ，以做為效果圖形中的輸入。</span><span class="sxs-lookup"><span data-stu-id="e75e5-105">Use the bitmap source effect to generate an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) from a [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) for use as an input in an effect graph.</span></span> <span data-ttu-id="e75e5-106">此效果會執行 CPU 的調整和旋轉。</span><span class="sxs-lookup"><span data-stu-id="e75e5-106">This effect performs scaling and rotation on the CPU.</span></span> <span data-ttu-id="e75e5-107">它也可以選擇性地產生系統記憶體 mipmap，這可以是在各種減少解析度上主動調整非常大型影像的效能優化。</span><span class="sxs-lookup"><span data-stu-id="e75e5-107">It can also optionally generate a system memory mipmap, which can be a performance optimization for actively scaling very large images at various reduced resolutions.</span></span>

> [!Note]  
> <span data-ttu-id="e75e5-108">點陣圖來源效果接受其輸入做為屬性，而不是影像輸入。</span><span class="sxs-lookup"><span data-stu-id="e75e5-108">The bitmap source effect takes its input as a property, not as an image input.</span></span> <span data-ttu-id="e75e5-109">您必須使用 [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) 方法，而不是 [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) 方法。</span><span class="sxs-lookup"><span data-stu-id="e75e5-109">You must use the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method, not the [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method.</span></span> <span data-ttu-id="e75e5-110">*WicBitmapSource* 屬性可讓您指定影像輸入資料。</span><span class="sxs-lookup"><span data-stu-id="e75e5-110">The *WicBitmapSource* property is where you specify the image input data.</span></span>

 

<span data-ttu-id="e75e5-111">這項效果的 CLSID 是 CLSID \_ D2D1BitmapSource。</span><span class="sxs-lookup"><span data-stu-id="e75e5-111">The CLSID for this effect is CLSID\_D2D1BitmapSource.</span></span>

-   [<span data-ttu-id="e75e5-112">效果屬性</span><span class="sxs-lookup"><span data-stu-id="e75e5-112">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e75e5-113">插補模式</span><span class="sxs-lookup"><span data-stu-id="e75e5-113">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="e75e5-114">Orientation</span><span class="sxs-lookup"><span data-stu-id="e75e5-114">Orientation</span></span>](#orientation)
-   [<span data-ttu-id="e75e5-115">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="e75e5-115">Alpha modes</span></span>](#alpha-modes)
-   [<span data-ttu-id="e75e5-116">備註</span><span class="sxs-lookup"><span data-stu-id="e75e5-116">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="e75e5-117">需求</span><span class="sxs-lookup"><span data-stu-id="e75e5-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e75e5-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="e75e5-118">Related topics</span></span>](#related-topics)

## <a name="effect-properties"></a><span data-ttu-id="e75e5-119">效果屬性</span><span class="sxs-lookup"><span data-stu-id="e75e5-119">Effect properties</span></span>



| <span data-ttu-id="e75e5-120">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="e75e5-120">Display name and index enumeration</span></span>                                                          | <span data-ttu-id="e75e5-121">Description</span><span class="sxs-lookup"><span data-stu-id="e75e5-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e75e5-122">WicBitmapSource</span><span class="sxs-lookup"><span data-stu-id="e75e5-122">WicBitmapSource</span></span><br/> <span data-ttu-id="e75e5-123">D2D1 \_ BITMAPSOURCE \_ 的 \_ \_ 版本 WIC 點陣圖 \_ 來源</span><span class="sxs-lookup"><span data-stu-id="e75e5-123">D2D1\_BITMAPSOURCE\_PROP\_WIC\_BITMAP\_SOURCE</span></span><br/>         | <span data-ttu-id="e75e5-124">[IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) ，其中包含要載入的影像資料。</span><span class="sxs-lookup"><span data-stu-id="e75e5-124">The [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) containing the image data to be loaded.</span></span><br/> <span data-ttu-id="e75e5-125">此類型為 [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource)。</span><span class="sxs-lookup"><span data-stu-id="e75e5-125">The type is [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource).</span></span><br/> <span data-ttu-id="e75e5-126">預設值是 NULL。</span><span class="sxs-lookup"><span data-stu-id="e75e5-126">The default value is NULL.</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="e75e5-127">調整</span><span class="sxs-lookup"><span data-stu-id="e75e5-127">Scale</span></span><br/> <span data-ttu-id="e75e5-128">D2D1 \_ BITMAPSOURCE \_ 的 \_ 範圍調整</span><span class="sxs-lookup"><span data-stu-id="e75e5-128">D2D1\_BITMAPSOURCE\_PROP\_SCALE</span></span><br/>                                 | <span data-ttu-id="e75e5-129">以 X 和 Y 方向的比例量。</span><span class="sxs-lookup"><span data-stu-id="e75e5-129">The scale amount in the X and Y direction.</span></span> <span data-ttu-id="e75e5-130">效果會將寬度乘以 X 值，並將高度乘以 Y 值。</span><span class="sxs-lookup"><span data-stu-id="e75e5-130">The effect multiplies the width by the X value and the height by the Y value.</span></span> <span data-ttu-id="e75e5-131">這個屬性是 \_ \_ 定義為： (X 刻度、Y 尺規) 的 D2D1 向量2f。</span><span class="sxs-lookup"><span data-stu-id="e75e5-131">This property is a D2D1\_VECTOR\_2F defined as: (X scale, Y scale).</span></span> <span data-ttu-id="e75e5-132">尺規數量為 FLOAT、無量，且必須為正數或0。</span><span class="sxs-lookup"><span data-stu-id="e75e5-132">The scale amounts are FLOAT, unitless, and must be positive or 0.</span></span><br/> <span data-ttu-id="e75e5-133">此類型為 D2D1 \_ VECTOR \_ 2f。</span><span class="sxs-lookup"><span data-stu-id="e75e5-133">The type is D2D1\_VECTOR\_2F.</span></span><br/> <span data-ttu-id="e75e5-134">預設值為 {1.0 f、1.0 f}。</span><span class="sxs-lookup"><span data-stu-id="e75e5-134">The default value is {1.0f, 1.0f}.</span></span><br/>                                                                           |
| <span data-ttu-id="e75e5-135">InterpolationMode.</span><span class="sxs-lookup"><span data-stu-id="e75e5-135">InterpolationMode.</span></span><br/> <span data-ttu-id="e75e5-136">D2D1 \_ BITMAPSOURCE \_ 的 \_ 內插補點 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="e75e5-136">D2D1\_BITMAPSOURCE\_PROP\_INTERPOLATION\_MODE</span></span><br/>      | <span data-ttu-id="e75e5-137">用來調整影像的插補模式。</span><span class="sxs-lookup"><span data-stu-id="e75e5-137">The interpolation mode used to scale the image.</span></span> <span data-ttu-id="e75e5-138">如需詳細資訊，請參閱 [插補模式](#interpolation-modes) 。</span><span class="sxs-lookup"><span data-stu-id="e75e5-138">See [Interpolation modes](#interpolation-modes) for more info.</span></span><br/> <span data-ttu-id="e75e5-139">如果模式停用 mipmap，則 BitmapSouce 會以 Scale 和 EnableDPICorrection 屬性所決定的解析度來快取影像。</span><span class="sxs-lookup"><span data-stu-id="e75e5-139">If the mode disables the mipmap, then BitmapSouce will cache the image at the resolution determined by the Scale and EnableDPICorrection properties.</span></span><br/> <span data-ttu-id="e75e5-140">此類型為 D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="e75e5-140">The type is D2D1\_BITMAPSOURCE\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="e75e5-141">預設值為 D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ 線性。</span><span class="sxs-lookup"><span data-stu-id="e75e5-141">The default value is D2D1\_BITMAPSOURCE\_INTERPOLATION\_MODE\_LINEAR.</span></span><br/> |
| <span data-ttu-id="e75e5-142">EnableDPICorrection</span><span class="sxs-lookup"><span data-stu-id="e75e5-142">EnableDPICorrection</span></span><br/> <span data-ttu-id="e75e5-143">D2D1 \_ BITMAPSOURCE \_ 的 \_ 支援 \_ DPI \_ 修正</span><span class="sxs-lookup"><span data-stu-id="e75e5-143">D2D1\_BITMAPSOURCE\_PROP\_ENABLE\_DPI\_CORRECTION</span></span><br/> | <span data-ttu-id="e75e5-144">如果您將此設定為 TRUE，效果將會調整輸入影像，以將 [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) 所報告的 DPI 轉換成裝置內容的 DPI。</span><span class="sxs-lookup"><span data-stu-id="e75e5-144">If you set this to TRUE, the effect will scale the input image to convert the DPI reported by [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) to the DPI of the device context.</span></span> <span data-ttu-id="e75e5-145">效果會使用您使用 InterpolationMode 屬性設定的插補模式。</span><span class="sxs-lookup"><span data-stu-id="e75e5-145">The effect uses the interpolation mode you set with the InterpolationMode property.</span></span> <span data-ttu-id="e75e5-146">如果您將此設定為 FALSE，則效果會使用96.0 的 DPI 作為輸出影像。</span><span class="sxs-lookup"><span data-stu-id="e75e5-146">If you set this to FALSE, the effect uses a DPI of 96.0 for the output image.</span></span><br/> <span data-ttu-id="e75e5-147">此類型為 BOOL。</span><span class="sxs-lookup"><span data-stu-id="e75e5-147">The type is BOOL.</span></span><br/> <span data-ttu-id="e75e5-148">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="e75e5-148">The default value is FALSE.</span></span><br/>   |
| <span data-ttu-id="e75e5-149">AlphaMode</span><span class="sxs-lookup"><span data-stu-id="e75e5-149">AlphaMode</span></span><br/> <span data-ttu-id="e75e5-150">D2D1 \_ BITMAPSOURCE \_ 的 \_ ALPHA \_ 模式</span><span class="sxs-lookup"><span data-stu-id="e75e5-150">D2D1\_BITMAPSOURCE\_PROP\_ALPHA\_MODE</span></span><br/>                       | <span data-ttu-id="e75e5-151">輸出的 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="e75e5-151">The alpha mode of the output.</span></span> <span data-ttu-id="e75e5-152">這可以是預乘或直接。</span><span class="sxs-lookup"><span data-stu-id="e75e5-152">This can be either premultiplied or straight.</span></span> <span data-ttu-id="e75e5-153">如需詳細資訊，請參閱 [Alpha 模式](#alpha-modes) 。</span><span class="sxs-lookup"><span data-stu-id="e75e5-153">See [Alpha modes](#alpha-modes) for more info.</span></span><br/> <span data-ttu-id="e75e5-154">此類型為 D2D1 \_ BITMAPSOURCE \_ ALPHA \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="e75e5-154">The type is D2D1\_BITMAPSOURCE\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="e75e5-155">預設值是預乘的 D2D1 \_ BITMAPSOURCE \_ ALPHA \_ 模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e75e5-155">The default value is D2D1\_BITMAPSOURCE\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="e75e5-156">Orientation</span><span class="sxs-lookup"><span data-stu-id="e75e5-156">Orientation</span></span><br/> <span data-ttu-id="e75e5-157">D2D1 \_ BITMAPSOURCE 的 \_ 主張 \_ 方向</span><span class="sxs-lookup"><span data-stu-id="e75e5-157">D2D1\_BITMAPSOURCE\_PROP\_ORIENTATION</span></span><br/>                     | <span data-ttu-id="e75e5-158">要在影像上執行的翻轉和/或旋轉操作。</span><span class="sxs-lookup"><span data-stu-id="e75e5-158">A flip and/or rotation operation to be performed on the image.</span></span> <span data-ttu-id="e75e5-159">如需詳細資訊，請參閱 [方向](#orientation) 。</span><span class="sxs-lookup"><span data-stu-id="e75e5-159">See [Orientation](#orientation) for more info.</span></span><br/> <span data-ttu-id="e75e5-160">此類型為 D2D1 \_ BITMAPSOURCE \_ 方向。</span><span class="sxs-lookup"><span data-stu-id="e75e5-160">The type is D2D1\_BITMAPSOURCE\_ORIENTATION.</span></span><br/> <span data-ttu-id="e75e5-161">預設值為 D2D1 \_ BITMAPSOURCE \_ 方向預設值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e75e5-161">The default value is D2D1\_BITMAPSOURCE\_ORIENTATION\_DEFAULT.</span></span><br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a><span data-ttu-id="e75e5-162">插補模式</span><span class="sxs-lookup"><span data-stu-id="e75e5-162">Interpolation modes</span></span>

<span data-ttu-id="e75e5-163">效果會在縮放影像或更正 DPI 時，使用此模式來進行插補。</span><span class="sxs-lookup"><span data-stu-id="e75e5-163">The effect interpolates using this mode when it scales an image or when it corrects the DPI.</span></span> <span data-ttu-id="e75e5-164">此效果使用的插補模式是由 CPU 計算，而不是 GPU。</span><span class="sxs-lookup"><span data-stu-id="e75e5-164">The interpolation modes this effect uses are calculated by the CPU, not the GPU.</span></span>



| <span data-ttu-id="e75e5-165">Name</span><span class="sxs-lookup"><span data-stu-id="e75e5-165">Name</span></span>                                                       | <span data-ttu-id="e75e5-166">描述</span><span class="sxs-lookup"><span data-stu-id="e75e5-166">Description</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e75e5-167">\_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 BITMAPSOURCE 插補模式</span><span class="sxs-lookup"><span data-stu-id="e75e5-167">D2D1\_BITMAPSOURCE\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span> | <span data-ttu-id="e75e5-168">範例最接近的單一點，並使用該點。</span><span class="sxs-lookup"><span data-stu-id="e75e5-168">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="e75e5-169">不會產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="e75e5-169">Doesn't generate a mipmap.</span></span>                                                                                                                                                           |
| <span data-ttu-id="e75e5-170">D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ 線性</span><span class="sxs-lookup"><span data-stu-id="e75e5-170">D2D1\_BITMAPSOURCE\_INTERPOLATION\_MODE\_LINEAR</span></span>            | <span data-ttu-id="e75e5-171">使用四個點取樣和線性插補。</span><span class="sxs-lookup"><span data-stu-id="e75e5-171">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="e75e5-172">不會產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="e75e5-172">Doesn't generate a mipmap.</span></span>                                                                                                                                                        |
| <span data-ttu-id="e75e5-173">D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ 立方</span><span class="sxs-lookup"><span data-stu-id="e75e5-173">D2D1\_BITMAPSOURCE\_INTERPOLATION\_MODE\_CUBIC</span></span>             | <span data-ttu-id="e75e5-174">使用16個範例三核心來進行插補。</span><span class="sxs-lookup"><span data-stu-id="e75e5-174">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="e75e5-175">不會產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="e75e5-175">Doesn't generate a mipmap.</span></span>                                                                                                                                                          |
| <span data-ttu-id="e75e5-176">D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ FANT</span><span class="sxs-lookup"><span data-stu-id="e75e5-176">D2D1\_BITMAPSOURCE\_INTERPOLATION\_MODE\_FANT</span></span>              | <span data-ttu-id="e75e5-177">使用 WIC fant 插補，與 [**IWICBitmapScaler**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) 介面相同。</span><span class="sxs-lookup"><span data-stu-id="e75e5-177">Uses the WIC fant interpolation, the same as the [**IWICBitmapScaler**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) interface.</span></span> <span data-ttu-id="e75e5-178">不會產生 mipmap。</span><span class="sxs-lookup"><span data-stu-id="e75e5-178">Doesn't generate a mipmap.</span></span>                                                                                       |
| <span data-ttu-id="e75e5-179">D2D1 \_ BITMAPSOURCE \_ 插補 \_ 模式 \_ MIPMAP \_ 線性</span><span class="sxs-lookup"><span data-stu-id="e75e5-179">D2D1\_BITMAPSOURCE\_INTERPOLATION\_MODE\_MIPMAP\_LINEAR</span></span>    | <span data-ttu-id="e75e5-180">使用雙線性插補，在系統記憶體中產生 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="e75e5-180">Generates mipmap chain in system memory using bilinear interpolation.</span></span> <span data-ttu-id="e75e5-181">針對每個 mipmap，效果會使用雙線性插補來調整為最接近的0.5 倍數，然後使用線性插補來調整剩餘的數量。</span><span class="sxs-lookup"><span data-stu-id="e75e5-181">For each mipmap the effect scales to the nearest multiple of 0.5 using bilinear interpolation and then scales the remaining amount using linear interpolation.</span></span> |



 

## <a name="orientation"></a><span data-ttu-id="e75e5-182">Orientation</span><span class="sxs-lookup"><span data-stu-id="e75e5-182">Orientation</span></span>

<span data-ttu-id="e75e5-183">方向屬性可以用來套用內嵌于影像內的 EXIF 方向旗標。</span><span class="sxs-lookup"><span data-stu-id="e75e5-183">The Orientation property can be used to apply an EXIF orientation flag that is embedded within an image.</span></span>



| <span data-ttu-id="e75e5-184">Name</span><span class="sxs-lookup"><span data-stu-id="e75e5-184">Name</span></span>                                                                    | <span data-ttu-id="e75e5-185">描述</span><span class="sxs-lookup"><span data-stu-id="e75e5-185">Description</span></span>                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e75e5-186">D2D1 \_ BITMAPSOURCE \_ 方向 \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="e75e5-186">D2D1\_BITMAPSOURCE\_ORIENTATION\_DEFAULT</span></span>                                | <span data-ttu-id="e75e5-187">預設值。</span><span class="sxs-lookup"><span data-stu-id="e75e5-187">Default.</span></span> <span data-ttu-id="e75e5-188">效果不會變更輸入的方向。</span><span class="sxs-lookup"><span data-stu-id="e75e5-188">The effect doesn't change the orientation of the input.</span></span>   |
| <span data-ttu-id="e75e5-189">D2D1 \_ BITMAPSOURCE \_ 方向 \_ \_ 水準翻轉</span><span class="sxs-lookup"><span data-stu-id="e75e5-189">D2D1\_BITMAPSOURCE\_ORIENTATION\_FLIP\_HORIZONTAL</span></span>                       | <span data-ttu-id="e75e5-190">水準翻轉影像。</span><span class="sxs-lookup"><span data-stu-id="e75e5-190">Flips the image horizontally.</span></span>                                      |
| <span data-ttu-id="e75e5-191">D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE180</span><span class="sxs-lookup"><span data-stu-id="e75e5-191">D2D1\_BITMAPSOURCE\_ORIENTATION\_ROTATE\_CLOCKWISE180</span></span>                   | <span data-ttu-id="e75e5-192">以順時針旋轉180度旋轉影像。</span><span class="sxs-lookup"><span data-stu-id="e75e5-192">Rotates the image clockwise 180 degrees.</span></span>                           |
| <span data-ttu-id="e75e5-193">D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE180 \_ 翻轉 \_ 水準</span><span class="sxs-lookup"><span data-stu-id="e75e5-193">D2D1\_BITMAPSOURCE\_ORIENTATION\_ROTATE\_CLOCKWISE180\_FLIP\_HORIZONTAL</span></span> | <span data-ttu-id="e75e5-194">以順時針180度旋轉影像，並水準翻轉。</span><span class="sxs-lookup"><span data-stu-id="e75e5-194">Rotates the image clockwise 180 degrees and flips it horizontally.</span></span> |
| <span data-ttu-id="e75e5-195">D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE270 \_ 翻轉 \_ 水準</span><span class="sxs-lookup"><span data-stu-id="e75e5-195">D2D1\_BITMAPSOURCE\_ORIENTATION\_ROTATE\_CLOCKWISE270\_FLIP\_HORIZONTAL</span></span> | <span data-ttu-id="e75e5-196">以順時針270度旋轉影像，並水準翻轉。</span><span class="sxs-lookup"><span data-stu-id="e75e5-196">Rotates the image clockwise 270 degrees and flips it horizontally.</span></span> |
| <span data-ttu-id="e75e5-197">D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE90</span><span class="sxs-lookup"><span data-stu-id="e75e5-197">D2D1\_BITMAPSOURCE\_ORIENTATION\_ROTATE\_CLOCKWISE90</span></span>                    | <span data-ttu-id="e75e5-198">以順時針旋轉90度旋轉影像。</span><span class="sxs-lookup"><span data-stu-id="e75e5-198">Rotates the image clockwise 90 degrees.</span></span>                            |
| <span data-ttu-id="e75e5-199">D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE90 \_ 翻轉 \_ 水準</span><span class="sxs-lookup"><span data-stu-id="e75e5-199">D2D1\_BITMAPSOURCE\_ORIENTATION\_ROTATE\_CLOCKWISE90\_FLIP\_HORIZONTAL</span></span>  | <span data-ttu-id="e75e5-200">以順時針90度旋轉影像，並水準翻轉。</span><span class="sxs-lookup"><span data-stu-id="e75e5-200">Rotates the image clockwise 90 degrees and flips it horizontally.</span></span>  |
| <span data-ttu-id="e75e5-201">D2D1 \_ BITMAPSOURCE \_ 方向 \_ 旋轉 \_ CLOCKWISE270</span><span class="sxs-lookup"><span data-stu-id="e75e5-201">D2D1\_BITMAPSOURCE\_ORIENTATION\_ROTATE\_CLOCKWISE270</span></span>                   | <span data-ttu-id="e75e5-202">以順時針旋轉270度旋轉影像。</span><span class="sxs-lookup"><span data-stu-id="e75e5-202">Rotates the image clockwise 270 degrees.</span></span>                           |



 

<span data-ttu-id="e75e5-203">此程式碼片段示範如何從) propkey 中定義的 EXIF 方向值轉換 (在 D2D1 \_ BITMAPSOURCE \_ 方向值。</span><span class="sxs-lookup"><span data-stu-id="e75e5-203">This code snippet demonstrates how to convert from EXIF orientation values (defined in propkey.h) to D2D1\_BITMAPSOURCE\_ORIENTATION values.</span></span>


```C++
#include <propkey.h>
#include <d2d1effects.h>

D2D1_BITMAPSOURCE_ORIENTATION GetBitmapSourceOrientation(unsigned short PhotoOrientation)
{
       switch (PhotoOrientation)
       {
       case PHOTO_ORIENTATION_NORMAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       case PHOTO_ORIENTATION_FLIPHORIZONTAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE180:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180;
       case PHOTO_ORIENTATION_FLIPVERTICAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_TRANSPOSE: 
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE270:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90;
       case PHOTO_ORIENTATION_TRANSVERSE:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE90:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270;
       default:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       }
}
```



## <a name="alpha-modes"></a><span data-ttu-id="e75e5-204">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="e75e5-204">Alpha modes</span></span>



| <span data-ttu-id="e75e5-205">Name</span><span class="sxs-lookup"><span data-stu-id="e75e5-205">Name</span></span>                                           | <span data-ttu-id="e75e5-206">描述</span><span class="sxs-lookup"><span data-stu-id="e75e5-206">Description</span></span>                                            |
|------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="e75e5-207">預 \_ 乘的 D2D1 BITMAPSOURCE \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="e75e5-207">D2D1\_BITMAPSOURCE\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="e75e5-208">效果輸出使用預乘 Alpha。</span><span class="sxs-lookup"><span data-stu-id="e75e5-208">The effect output uses premultiplied alpha.</span></span><br/> |
| <span data-ttu-id="e75e5-209">D2D1 \_ BITMAPSOURCE \_ ALPHA \_ 模式 \_ 直接</span><span class="sxs-lookup"><span data-stu-id="e75e5-209">D2D1\_BITMAPSOURCE\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="e75e5-210">效果輸出會使用直接 Alpha。</span><span class="sxs-lookup"><span data-stu-id="e75e5-210">The effect output uses straight alpha.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="e75e5-211">備註</span><span class="sxs-lookup"><span data-stu-id="e75e5-211">Remarks</span></span>

<span data-ttu-id="e75e5-212">若要在同時使用 WIC 和 [Direct2D](./direct2d-portal.md) 時將效能優化，您應該使用 [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) ，根據您的應用程式案例和映射的原生精確度，轉換成適當的像素格式。</span><span class="sxs-lookup"><span data-stu-id="e75e5-212">To optimize performance when using WIC and [Direct2D](./direct2d-portal.md) together, you should use [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) to convert to an appropriate pixel format based your app s scenario and the image s native precision.</span></span>

<span data-ttu-id="e75e5-213">在大多數情況下，您的應用程式 [Direct2D](./direct2d-portal.md) 管線只需要每個通道8個位 (bpc) 的精確度，或者影像只提供8個 bpc 的有效位數，因此您應該轉換為 GUID \_ WICPixelFormat32bppPBGRA。</span><span class="sxs-lookup"><span data-stu-id="e75e5-213">In most cases, either your app s [Direct2D](./direct2d-portal.md) pipeline only requires 8 bits per channel (bpc) of precision, or the image only provides 8 bpc precision, and therefore you should convert to GUID\_WICPixelFormat32bppPBGRA.</span></span> <span data-ttu-id="e75e5-214">但是，如果您想要利用影像所提供的額外精確度 (例如，以超過 8 bpc 的精確度來儲存 XR 或 TIFF) ，您應該使用以 RGBA 為基礎的像素格式。</span><span class="sxs-lookup"><span data-stu-id="e75e5-214">However, if you want to take advantage of extra precision provided by an image (for example, a JPEG-XR or TIFF stored with greater than 8 bpc precision), you should use an RGBA-based pixel format.</span></span> <span data-ttu-id="e75e5-215">下表提供更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e75e5-215">The below table provides more details.</span></span>



| <span data-ttu-id="e75e5-216">需要的精確度</span><span class="sxs-lookup"><span data-stu-id="e75e5-216">Desired precision</span></span>   | <span data-ttu-id="e75e5-217">影像的原生精確度</span><span class="sxs-lookup"><span data-stu-id="e75e5-217">Native precision of the image</span></span> | <span data-ttu-id="e75e5-218">建議的像素格式</span><span class="sxs-lookup"><span data-stu-id="e75e5-218">Recommended pixel format</span></span>                |
|---------------------|-------------------------------|-----------------------------------------|
| <span data-ttu-id="e75e5-219">每個通道8個位</span><span class="sxs-lookup"><span data-stu-id="e75e5-219">8 bits per channel</span></span>  | <span data-ttu-id="e75e5-220"><= 每個通道8位</span><span class="sxs-lookup"><span data-stu-id="e75e5-220"><= 8 bits per channel</span></span>      | <span data-ttu-id="e75e5-221">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="e75e5-221">GUID\_WICPixelFormat32bppPBGRA</span></span>          |
| <span data-ttu-id="e75e5-222">越高越好</span><span class="sxs-lookup"><span data-stu-id="e75e5-222">As high as possible</span></span> | <span data-ttu-id="e75e5-223"><= 每個通道8位</span><span class="sxs-lookup"><span data-stu-id="e75e5-223"><= 8 bits per channel</span></span>      | <span data-ttu-id="e75e5-224">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="e75e5-224">GUID\_WICPixelFormat32bppPBGRA</span></span>          |
| <span data-ttu-id="e75e5-225">越高越好</span><span class="sxs-lookup"><span data-stu-id="e75e5-225">As high as possible</span></span> | <span data-ttu-id="e75e5-226">每個通道 > 8 個位</span><span class="sxs-lookup"><span data-stu-id="e75e5-226">> 8 bits per channel</span></span>       | <span data-ttu-id="e75e5-227">RGBA 頻道順序，預乘 Alpha</span><span class="sxs-lookup"><span data-stu-id="e75e5-227">RGBA channel order, premultiplied alpha</span></span> |



 

<span data-ttu-id="e75e5-228">由於許多影像格式支援多個精確度層級，因此您應該使用 [**IWICBitmapSource：： GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) 來取得影像的原生像素格式，然後使用 [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) 來判斷該格式的每個有效位數通道位數。</span><span class="sxs-lookup"><span data-stu-id="e75e5-228">Because many image formats support multiple levels of precision, you should use [**IWICBitmapSource::GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) to obtain the image s native pixel format, and then use [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) to determine how many bits per channel of precision are available for that format.</span></span> <span data-ttu-id="e75e5-229">另請注意，並非所有硬體都支援高精確度的像素格式。</span><span class="sxs-lookup"><span data-stu-id="e75e5-229">Also, note that not all hardware supports high precision pixel formats.</span></span> <span data-ttu-id="e75e5-230">在這些情況下，您的應用程式可能需要切換回彎曲裝置，以支援高精確度。</span><span class="sxs-lookup"><span data-stu-id="e75e5-230">In those cases your app may need to fall back to the WARP device to support high precision.</span></span>

## <a name="requirements"></a><span data-ttu-id="e75e5-231">規格需求</span><span class="sxs-lookup"><span data-stu-id="e75e5-231">Requirements</span></span>



| <span data-ttu-id="e75e5-232">需求</span><span class="sxs-lookup"><span data-stu-id="e75e5-232">Requirement</span></span> | <span data-ttu-id="e75e5-233">值</span><span class="sxs-lookup"><span data-stu-id="e75e5-233">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e75e5-234">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e75e5-234">Minimum supported client</span></span> | <span data-ttu-id="e75e5-235">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e75e5-235">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e75e5-236">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e75e5-236">Minimum supported server</span></span> | <span data-ttu-id="e75e5-237">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e75e5-237">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e75e5-238">標頭</span><span class="sxs-lookup"><span data-stu-id="e75e5-238">Header</span></span>                   | <span data-ttu-id="e75e5-239">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="e75e5-239">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="e75e5-240">程式庫</span><span class="sxs-lookup"><span data-stu-id="e75e5-240">Library</span></span>                  | <span data-ttu-id="e75e5-241">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="e75e5-241">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e75e5-242">相關主題</span><span class="sxs-lookup"><span data-stu-id="e75e5-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e75e5-243">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="e75e5-243">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

