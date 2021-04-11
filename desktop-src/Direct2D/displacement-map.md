---
title: 置換地圖效果
description: 使用置換地圖效果，以第二個輸入影像的濃度值取代輸入影像的圖元。
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- 置換地圖效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093900"
---
# <a name="displacement-map-effect"></a><span data-ttu-id="d1ac8-104">置換地圖效果</span><span class="sxs-lookup"><span data-stu-id="d1ac8-104">Displacement map effect</span></span>

<span data-ttu-id="d1ac8-105">使用置換地圖效果，以第二個輸入影像的濃度值取代輸入影像的圖元。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-105">Use the displacement map effect to displace the pixels of the input image by the intensity values of a second input image.</span></span>

<span data-ttu-id="d1ac8-106">這項效果的 CLSID 是 CLSID \_ D2D1DisplacementMap。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-106">The CLSID for this effect is CLSID\_D2D1DisplacementMap.</span></span>

-   [<span data-ttu-id="d1ac8-107">範例影像</span><span class="sxs-lookup"><span data-stu-id="d1ac8-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="d1ac8-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="d1ac8-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="d1ac8-109">色彩頻道</span><span class="sxs-lookup"><span data-stu-id="d1ac8-109">Color channels</span></span>](#color-channels)
-   [<span data-ttu-id="d1ac8-110">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="d1ac8-110">Output Bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="d1ac8-111">需求</span><span class="sxs-lookup"><span data-stu-id="d1ac8-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d1ac8-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1ac8-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="d1ac8-113">範例影像</span><span class="sxs-lookup"><span data-stu-id="d1ac8-113">Example image</span></span>



| <span data-ttu-id="d1ac8-114">之前</span><span class="sxs-lookup"><span data-stu-id="d1ac8-114">Before</span></span>                                                           |
|------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)       |
| <span data-ttu-id="d1ac8-116">After</span><span class="sxs-lookup"><span data-stu-id="d1ac8-116">After</span></span>                                                            |
| ![轉換後的影像。](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="d1ac8-118">輸出中圖元的位置是使用下列公式來決定：</span><span class="sxs-lookup"><span data-stu-id="d1ac8-118">The locations of the pixels in the output are determined using this formula:</span></span>

<span data-ttu-id="d1ac8-119">C ' (x，y) = C (x + 縮放 \* (XChannelSelector (置換點陣圖 (x、y) ) -0.5) 、y + 尺規 \* (YChannelSelector (置換點陣圖 (x、y) ) -0.5) ) </span><span class="sxs-lookup"><span data-stu-id="d1ac8-119">C' (x,y)=C(x+ scale\*(XChannelSelector(Displacement Bitmap (x,y))-0.5),y+ scale\*(YChannelSelector(Displacement Bitmap (x,y))-0.5))</span></span>

<span data-ttu-id="d1ac8-120">其中：</span><span class="sxs-lookup"><span data-stu-id="d1ac8-120">Where:</span></span><dl> <span data-ttu-id="d1ac8-121">*C (x，y)* 是 (x，y) 的輸出圖元。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-121">*C  (x, y)* is the output pixel at (x, y).</span></span>  
<span data-ttu-id="d1ac8-122">*C (x，y)* 是 (x，y) 的輸入圖元。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-122">*C (x, y)* is the input pixel at (x, y).</span></span>  
<span data-ttu-id="d1ac8-123">*置換點陣圖 (x，y)* 是指定座標的位移圖元濃度</span><span class="sxs-lookup"><span data-stu-id="d1ac8-123">*Displacement Bitmap (x, y)* is the displacement pixel intensity at the specified coordinates</span></span>  
<span data-ttu-id="d1ac8-124">從以 X 方向取代輸入影像的置換點陣圖， *XChannelSelector* 所選 RGBA 通道的濃度。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-124">*XChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the X direction.</span></span>  
<span data-ttu-id="d1ac8-125">從以 Y 方向取代輸入影像的置換點陣圖， *YChannelSelector* 所選 RGBA 通道的濃度。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-125">*YChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the Y direction.</span></span>  
</dl>

<span data-ttu-id="d1ac8-126">效果會根據尺規屬性和置換影像的強度來 resamples 輸入影像。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-126">The effect resamples the input image according to the scale property and the intensity of the displacement image.</span></span> <span data-ttu-id="d1ac8-127">如果在輸入影像中的圖元之間進行取樣，則會使用雙線性插補。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-127">It uses bilinear interpolation if sampling from between pixels in the input image.</span></span>

<span data-ttu-id="d1ac8-128">此效果適用于直接和預乘的 Alpha 影像。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-128">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="d1ac8-129">輸出 Alpha 格式與輸入格式相同。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-129">The output alpha format is the same as the input format.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="d1ac8-130">效果屬性</span><span class="sxs-lookup"><span data-stu-id="d1ac8-130">Effect properties</span></span>



| <span data-ttu-id="d1ac8-131">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="d1ac8-131">Display name and index enumeration</span></span>                                                   | <span data-ttu-id="d1ac8-132">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="d1ac8-132">Type and default value</span></span>                                                   | <span data-ttu-id="d1ac8-133">Description</span><span class="sxs-lookup"><span data-stu-id="d1ac8-133">Description</span></span>                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ac8-134">調整</span><span class="sxs-lookup"><span data-stu-id="d1ac8-134">Scale</span></span><br/> <span data-ttu-id="d1ac8-135">D2D1 \_ DISPLACEMENTMAP \_ 的 \_ 範圍調整</span><span class="sxs-lookup"><span data-stu-id="d1ac8-135">D2D1\_DISPLACEMENTMAP\_PROP\_SCALE</span></span><br/>                       | <span data-ttu-id="d1ac8-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d1ac8-136">FLOAT</span></span><br/> <span data-ttu-id="d1ac8-137">0.0f</span><span class="sxs-lookup"><span data-stu-id="d1ac8-137">0.0f</span></span><br/>                                         | <span data-ttu-id="d1ac8-138">將所選通道的強度與置換影像相乘。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-138">Multiplies the intensity of the selected channel from the displacement image.</span></span> <span data-ttu-id="d1ac8-139">您設定此屬性的愈高，效果越多取代圖元</span><span class="sxs-lookup"><span data-stu-id="d1ac8-139">The higher you set this property, the more the effect displaces the pixels</span></span><br/>                       |
| <span data-ttu-id="d1ac8-140">XChannelSelect</span><span class="sxs-lookup"><span data-stu-id="d1ac8-140">XChannelSelect</span></span><br/> <span data-ttu-id="d1ac8-141">D2D1 \_ DISPLACEMENTMAP \_ 精選 \_ X \_ CHANNEL \_ SELECT</span><span class="sxs-lookup"><span data-stu-id="d1ac8-141">D2D1\_DISPLACEMENTMAP\_PROP\_X\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="d1ac8-142">D2D1 \_ 通道 \_ 選取器</span><span class="sxs-lookup"><span data-stu-id="d1ac8-142">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="d1ac8-143">D2D1 \_ 通道 \_ 選取器 \_ A</span><span class="sxs-lookup"><span data-stu-id="d1ac8-143">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="d1ac8-144">效果會從這個色頻中取出濃度，並用它來以 X 方向取代影像。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-144">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the X direction.</span></span> <span data-ttu-id="d1ac8-145">如需詳細資訊，請參閱 [色彩通道](#color-channels) 。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-145">See [Color channels](#color-channels) for more info.</span></span><br/> |
| <span data-ttu-id="d1ac8-146">YChannelSelect</span><span class="sxs-lookup"><span data-stu-id="d1ac8-146">YChannelSelect</span></span><br/> <span data-ttu-id="d1ac8-147">D2D1 \_ DISPLACEMENTMAP \_ 的 \_ Y \_ 通道 \_ 選取</span><span class="sxs-lookup"><span data-stu-id="d1ac8-147">D2D1\_DISPLACEMENTMAP\_PROP\_Y\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="d1ac8-148">D2D1 \_ 通道 \_ 選取器</span><span class="sxs-lookup"><span data-stu-id="d1ac8-148">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="d1ac8-149">D2D1 \_ 通道 \_ 選取器 \_ A</span><span class="sxs-lookup"><span data-stu-id="d1ac8-149">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="d1ac8-150">效果會從這個色頻中取出濃度，並用它來以 Y 方向取代影像。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-150">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the Y direction.</span></span> <span data-ttu-id="d1ac8-151">如需詳細資訊，請參閱 [色彩通道](#color-channels) 。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-151">See [Color channels](#color-channels) for more info.</span></span><br/> |



 

## <a name="color-channels"></a><span data-ttu-id="d1ac8-152">色彩頻道</span><span class="sxs-lookup"><span data-stu-id="d1ac8-152">Color channels</span></span>



| <span data-ttu-id="d1ac8-153">列舉型別</span><span class="sxs-lookup"><span data-stu-id="d1ac8-153">Enumeration</span></span>                | <span data-ttu-id="d1ac8-154">描述</span><span class="sxs-lookup"><span data-stu-id="d1ac8-154">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="d1ac8-155">D2D1 \_ 通道 \_ 選取器 \_ R</span><span class="sxs-lookup"><span data-stu-id="d1ac8-155">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="d1ac8-156">效果會將紅色通道的強度輸出解壓縮。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-156">The effect extracts the intensity output from the red channel.</span></span>   |
| <span data-ttu-id="d1ac8-157">D2D1 \_ 通道 \_ 選取器 \_ G</span><span class="sxs-lookup"><span data-stu-id="d1ac8-157">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="d1ac8-158">效果會從綠色頻道中取出濃度輸出。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-158">The effect extracts the intensity output from the green channel.</span></span> |
| <span data-ttu-id="d1ac8-159">D2D1 \_ 通道 \_ 選取器 \_ B</span><span class="sxs-lookup"><span data-stu-id="d1ac8-159">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="d1ac8-160">效果會從藍色通道中解壓縮濃度輸出。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-160">The effect extracts the intensity output from the blue channel.</span></span>  |
| <span data-ttu-id="d1ac8-161">D2D1 \_ 通道 \_ 選取器 \_ A</span><span class="sxs-lookup"><span data-stu-id="d1ac8-161">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="d1ac8-162">效果會將 Alpha 色板的濃度輸出解壓縮。</span><span class="sxs-lookup"><span data-stu-id="d1ac8-162">The effect extracts the intensity output from the alpha channel.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="d1ac8-163">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="d1ac8-163">Output Bitmap</span></span>

<span data-ttu-id="d1ac8-164">您可以使用下列方程式來判斷輸出點陣圖的大小上限：</span><span class="sxs-lookup"><span data-stu-id="d1ac8-164">You can determine the maximum size of the output bitmap with these equations:</span></span>

<span data-ttu-id="d1ac8-165">輸出點陣圖？</span><span class="sxs-lookup"><span data-stu-id="d1ac8-165">Output Bitmap?</span></span> <span data-ttu-id="d1ac8-166">圖元 = (輸入點陣圖大小？ (Dip) + 縮放) \* (使用者 DPI/96) </span><span class="sxs-lookup"><span data-stu-id="d1ac8-166">Pixels=(Input Bitmap Size?(DIPs)+Scale)\*(User DPI/96)</span></span>

<span data-ttu-id="d1ac8-167">輸出點陣圖<sub>y</sub> 圖元 = (輸入點陣圖大小<sub>y</sub> (dip) + 縮放) \* (使用者 DPI/96) </span><span class="sxs-lookup"><span data-stu-id="d1ac8-167">Output Bitmap<sub>y</sub> Pixels=(Input Bitmap Size<sub>y</sub>(DIPs) + Scale)\*(User DPI/96)</span></span>

## <a name="requirements"></a><span data-ttu-id="d1ac8-168">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1ac8-168">Requirements</span></span>



| <span data-ttu-id="d1ac8-169">需求</span><span class="sxs-lookup"><span data-stu-id="d1ac8-169">Requirement</span></span> | <span data-ttu-id="d1ac8-170">值</span><span class="sxs-lookup"><span data-stu-id="d1ac8-170">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ac8-171">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1ac8-171">Minimum supported client</span></span> | <span data-ttu-id="d1ac8-172">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1ac8-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d1ac8-173">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1ac8-173">Minimum supported server</span></span> | <span data-ttu-id="d1ac8-174">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1ac8-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d1ac8-175">標頭</span><span class="sxs-lookup"><span data-stu-id="d1ac8-175">Header</span></span>                   | <span data-ttu-id="d1ac8-176">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="d1ac8-176">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="d1ac8-177">程式庫</span><span class="sxs-lookup"><span data-stu-id="d1ac8-177">Library</span></span>                  | <span data-ttu-id="d1ac8-178">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="d1ac8-178">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="d1ac8-179">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1ac8-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1ac8-180">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="d1ac8-180">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

