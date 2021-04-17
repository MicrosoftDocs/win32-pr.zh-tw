---
title: 框線效果
description: 使用框線效果，從邊緣延伸影像。
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- 框線效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104514269"
---
# <a name="border-effect"></a><span data-ttu-id="2e50f-104">框線效果</span><span class="sxs-lookup"><span data-stu-id="2e50f-104">Border effect</span></span>

<span data-ttu-id="2e50f-105">使用框線效果，從邊緣延伸影像。</span><span class="sxs-lookup"><span data-stu-id="2e50f-105">Use the border effect to extend an image from the edges.</span></span> <span data-ttu-id="2e50f-106">您可以使用此效果來重複影像邊緣的圖元、將圖元換成影像的另一端，或在點陣圖框線之間鏡像圖元以延伸點陣圖區域。</span><span class="sxs-lookup"><span data-stu-id="2e50f-106">You can use this effect to repeat the pixels from the edges of the image, wrap the pixels from the opposite end of the image, or mirror the pixels across the bitmap border to extend the bitmap region.</span></span>

<span data-ttu-id="2e50f-107">這項效果的 CLSID 是 CLSID \_ D2D1Border。</span><span class="sxs-lookup"><span data-stu-id="2e50f-107">The CLSID for this effect is CLSID\_D2D1Border.</span></span>

## <a name="example-images"></a><span data-ttu-id="2e50f-108">範例影像</span><span class="sxs-lookup"><span data-stu-id="2e50f-108">Example images</span></span>

<span data-ttu-id="2e50f-109">此處的範例會使用每種模式來顯示框線效果的輸出。</span><span class="sxs-lookup"><span data-stu-id="2e50f-109">The examples here show the output of the border effect using each mode.</span></span> <span data-ttu-id="2e50f-110">輸出大小是無限的，但這些範例影像會裁剪成大小的兩倍。</span><span class="sxs-lookup"><span data-stu-id="2e50f-110">The output size is infinite, but these example images are cropped to twice the size.</span></span>

### <a name="mirror"></a><span data-ttu-id="2e50f-111">鏡像</span><span class="sxs-lookup"><span data-stu-id="2e50f-111">Mirror</span></span>



| <span data-ttu-id="2e50f-112">之前</span><span class="sxs-lookup"><span data-stu-id="2e50f-112">Before</span></span>                                                    |
|-----------------------------------------------------------|
| ![顯示效果之前影像的螢幕擷取畫面。](images/border-before.jpg) |
| <span data-ttu-id="2e50f-114">After</span><span class="sxs-lookup"><span data-stu-id="2e50f-114">After</span></span>                                                     |
| ![顯示轉換後影像的螢幕擷取畫面。](images/10-border.png)   |



 

### <a name="clamp"></a><span data-ttu-id="2e50f-116">Clamp</span><span class="sxs-lookup"><span data-stu-id="2e50f-116">Clamp</span></span>



| <span data-ttu-id="2e50f-117">之前</span><span class="sxs-lookup"><span data-stu-id="2e50f-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![顯示夾具效果之前影像的螢幕擷取畫面。](images/border-before.jpg)     |
| <span data-ttu-id="2e50f-119">After</span><span class="sxs-lookup"><span data-stu-id="2e50f-119">After</span></span>                                                         |
| ![顯示夾具轉換之後影像的螢幕擷取畫面。](images/10-border-clamp.png) |



 

### <a name="wrap"></a><span data-ttu-id="2e50f-121">包裝</span><span class="sxs-lookup"><span data-stu-id="2e50f-121">Wrap</span></span>



| <span data-ttu-id="2e50f-122">之前</span><span class="sxs-lookup"><span data-stu-id="2e50f-122">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![顯示環繞效果之前影像的螢幕擷取畫面。](images/border-before.jpg)    |
| <span data-ttu-id="2e50f-124">After</span><span class="sxs-lookup"><span data-stu-id="2e50f-124">After</span></span>                                                        |
| ![顯示換行轉換之後影像的螢幕擷取畫面。](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="2e50f-126">效果屬性</span><span class="sxs-lookup"><span data-stu-id="2e50f-126">Effect properties</span></span>



| <span data-ttu-id="2e50f-127">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="2e50f-127">Display name and index enumeration</span></span>                                  | <span data-ttu-id="2e50f-128">Description</span><span class="sxs-lookup"><span data-stu-id="2e50f-128">Description</span></span>                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e50f-129">邊緣模式 X</span><span class="sxs-lookup"><span data-stu-id="2e50f-129">Edge Mode X</span></span><br/> <span data-ttu-id="2e50f-130">D2D1 \_ 框線 \_ 樣式 \_ 邊緣 \_ 模式 \_ X</span><span class="sxs-lookup"><span data-stu-id="2e50f-130">D2D1\_BORDER\_PROP\_EDGE\_MODE\_X</span></span><br/> | <span data-ttu-id="2e50f-131">效果 X 方向的邊緣模式。</span><span class="sxs-lookup"><span data-stu-id="2e50f-131">The edge mode in the X direction for the effect.</span></span> <span data-ttu-id="2e50f-132">您可以將此設定為 [夾具]、[換行] 或 [鏡像]。</span><span class="sxs-lookup"><span data-stu-id="2e50f-132">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="2e50f-133">如需詳細資訊，請參閱 [邊緣模式](#edge-modes) 。</span><span class="sxs-lookup"><span data-stu-id="2e50f-133">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="2e50f-134">此類型為 D2D1 \_ BORDER \_ EDGE \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="2e50f-134">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="2e50f-135">預設值為 D2D1 \_ BORDER \_ EDGE \_ 模式 \_ 夾具。</span><span class="sxs-lookup"><span data-stu-id="2e50f-135">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |
| <span data-ttu-id="2e50f-136">邊緣模式 Y</span><span class="sxs-lookup"><span data-stu-id="2e50f-136">Edge Mode Y</span></span><br/> <span data-ttu-id="2e50f-137">D2D1 \_ 框線 \_ 的 \_ 側邊 \_ 模式 \_ Y</span><span class="sxs-lookup"><span data-stu-id="2e50f-137">D2D1\_BORDER\_PROP\_EDGE\_MODE\_Y</span></span><br/> | <span data-ttu-id="2e50f-138">效果 Y 方向的邊緣模式。</span><span class="sxs-lookup"><span data-stu-id="2e50f-138">The edge mode in the Y direction for the effect.</span></span> <span data-ttu-id="2e50f-139">您可以將此設定為 [夾具]、[換行] 或 [鏡像]。</span><span class="sxs-lookup"><span data-stu-id="2e50f-139">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="2e50f-140">如需詳細資訊，請參閱 [邊緣模式](#edge-modes) 。</span><span class="sxs-lookup"><span data-stu-id="2e50f-140">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="2e50f-141">此類型為 D2D1 \_ BORDER \_ EDGE \_ 模式。</span><span class="sxs-lookup"><span data-stu-id="2e50f-141">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="2e50f-142">預設值為 D2D1 \_ BORDER \_ EDGE \_ 模式 \_ 夾具。</span><span class="sxs-lookup"><span data-stu-id="2e50f-142">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |



 

## <a name="edge-modes"></a><span data-ttu-id="2e50f-143">邊緣模式</span><span class="sxs-lookup"><span data-stu-id="2e50f-143">Edge modes</span></span>



| <span data-ttu-id="2e50f-144">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="2e50f-144">Display name and index enumeration</span></span>                            | <span data-ttu-id="2e50f-145">Description</span><span class="sxs-lookup"><span data-stu-id="2e50f-145">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2e50f-146">Clamp</span><span class="sxs-lookup"><span data-stu-id="2e50f-146">Clamp</span></span><br/> <span data-ttu-id="2e50f-147">D2D1 \_ BORDER \_ EDGE \_ 模式 \_ 夾具</span><span class="sxs-lookup"><span data-stu-id="2e50f-147">D2D1\_BORDER\_EDGE\_MODE\_CLAMP</span></span><br/>   | <span data-ttu-id="2e50f-148">重複影像邊緣的圖元。</span><span class="sxs-lookup"><span data-stu-id="2e50f-148">Repeats the pixels from the edges of the image.</span></span>      |
| <span data-ttu-id="2e50f-149">包裝</span><span class="sxs-lookup"><span data-stu-id="2e50f-149">Wrap</span></span><br/> <span data-ttu-id="2e50f-150">D2D1 \_ 框線 \_ 邊緣 \_ 模式 \_ 換行</span><span class="sxs-lookup"><span data-stu-id="2e50f-150">D2D1\_BORDER\_EDGE\_MODE\_WRAP</span></span><br/>     | <span data-ttu-id="2e50f-151">使用影像之相對端邊緣的圖元。</span><span class="sxs-lookup"><span data-stu-id="2e50f-151">Uses pixels from the opposite end edge of the image.</span></span> |
| <span data-ttu-id="2e50f-152">鏡像</span><span class="sxs-lookup"><span data-stu-id="2e50f-152">Mirror</span></span><br/> <span data-ttu-id="2e50f-153">D2D1 \_ BORDER \_ EDGE \_ 模式 \_ 鏡像</span><span class="sxs-lookup"><span data-stu-id="2e50f-153">D2D1\_BORDER\_EDGE\_MODE\_MIRROR</span></span><br/> | <span data-ttu-id="2e50f-154">反映影像邊緣的圖元。</span><span class="sxs-lookup"><span data-stu-id="2e50f-154">Reflects pixels about the edge of the image.</span></span>         |



 

## <a name="output-bitmap"></a><span data-ttu-id="2e50f-155">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="2e50f-155">Output bitmap</span></span>

<span data-ttu-id="2e50f-156">除了0大小的輸入影像之外，所有輸入的輸出點陣圖大小都是無限的。</span><span class="sxs-lookup"><span data-stu-id="2e50f-156">The output bitmap size is infinite for all inputs, except a 0 sized input image.</span></span> <span data-ttu-id="2e50f-157">如果輸入影像的高度或寬度為0，則輸出大小為0。</span><span class="sxs-lookup"><span data-stu-id="2e50f-157">If the height or the width of an input image is 0, the output size is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e50f-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e50f-158">Requirements</span></span>



| <span data-ttu-id="2e50f-159">需求</span><span class="sxs-lookup"><span data-stu-id="2e50f-159">Requirement</span></span> | <span data-ttu-id="2e50f-160">值</span><span class="sxs-lookup"><span data-stu-id="2e50f-160">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e50f-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e50f-161">Minimum supported client</span></span> | <span data-ttu-id="2e50f-162">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e50f-162">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2e50f-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e50f-163">Minimum supported server</span></span> | <span data-ttu-id="2e50f-164">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e50f-164">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2e50f-165">標頭</span><span class="sxs-lookup"><span data-stu-id="2e50f-165">Header</span></span>                   | <span data-ttu-id="2e50f-166">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="2e50f-166">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="2e50f-167">程式庫</span><span class="sxs-lookup"><span data-stu-id="2e50f-167">Library</span></span>                  | <span data-ttu-id="2e50f-168">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="2e50f-168">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="2e50f-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e50f-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e50f-170">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="2e50f-170">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

