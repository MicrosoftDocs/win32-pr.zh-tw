---
title: Morphology 效果
description: 在影像中使用 morphology 效果來精簡或加厚邊緣界限。
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- morphology 效果
- dilate 效果
- 瓦解效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104729"
---
# <a name="morphology-effect"></a><span data-ttu-id="85854-106">Morphology 效果</span><span class="sxs-lookup"><span data-stu-id="85854-106">Morphology effect</span></span>

<span data-ttu-id="85854-107">在影像中使用 morphology 效果來精簡或加厚邊緣界限。</span><span class="sxs-lookup"><span data-stu-id="85854-107">Use the morphology effect to thin or thicken edge boundaries in an image.</span></span> <span data-ttu-id="85854-108">此效果會建立一個核心，其為您所指定之寬度和高度值的2倍。</span><span class="sxs-lookup"><span data-stu-id="85854-108">This effect creates a kernel that is 2 times the Width and Height values you specify.</span></span> <span data-ttu-id="85854-109">此效果會將核心放在其所計算的圖元上，如果核心 (中的 dilating) 或最小值，則會傳回最大 (值（如果 eroding) 的話）。</span><span class="sxs-lookup"><span data-stu-id="85854-109">This effect centers the kernel on the pixel it is calculating and returns the maximum value in the kernel (if dilating) or minimum value in the kernel (if eroding).</span></span>

<span data-ttu-id="85854-110">這項效果的 CLSID 是 CLSID \_ D2D1Morphology。</span><span class="sxs-lookup"><span data-stu-id="85854-110">The CLSID for this effect is CLSID\_D2D1Morphology.</span></span>

## <a name="example-images"></a><span data-ttu-id="85854-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="85854-111">Example images</span></span>

<span data-ttu-id="85854-112">此範例顯示使用瓦解模式時的效果輸出。</span><span class="sxs-lookup"><span data-stu-id="85854-112">This example shows the output of the effect when using the erode mode.</span></span>



| <span data-ttu-id="85854-113">之前</span><span class="sxs-lookup"><span data-stu-id="85854-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| <span data-ttu-id="85854-115">After</span><span class="sxs-lookup"><span data-stu-id="85854-115">After</span></span>                                                      |
| ![轉換後的影像。](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="85854-117">效果屬性</span><span class="sxs-lookup"><span data-stu-id="85854-117">Effect properties</span></span>



| <span data-ttu-id="85854-118">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="85854-118">Display name and index enumeration</span></span>                          | <span data-ttu-id="85854-119">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="85854-119">Type and default value</span></span>                                                     | <span data-ttu-id="85854-120">描述</span><span class="sxs-lookup"><span data-stu-id="85854-120">Description</span></span>                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85854-121">[模式]</span><span class="sxs-lookup"><span data-stu-id="85854-121">Mode</span></span><br/> <span data-ttu-id="85854-122">D2D1 \_ MORPHOLOGY \_ 的 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="85854-122">D2D1\_MORPHOLOGY\_PROP\_MODE</span></span><br/>     | <span data-ttu-id="85854-123">D2D1 \_ MORPHOLOGY \_ 模式</span><span class="sxs-lookup"><span data-stu-id="85854-123">D2D1\_MORPHOLOGY\_MODE</span></span><br/> <span data-ttu-id="85854-124">D2D1 \_ MORPHOLOGY \_ 模式 \_ 瓦解</span><span class="sxs-lookup"><span data-stu-id="85854-124">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span><br/> | <span data-ttu-id="85854-125">Morphology 模式。</span><span class="sxs-lookup"><span data-stu-id="85854-125">The morphology mode.</span></span> <span data-ttu-id="85854-126">可用的模式有瓦解 (簡維) 和 dilate (加厚) 。</span><span class="sxs-lookup"><span data-stu-id="85854-126">The available modes are erode (flatten) and dilate (thicken).</span></span><br/> <span data-ttu-id="85854-127">如需詳細資訊，請參閱 [Morphology 模式](#morphology-modes) 。</span><span class="sxs-lookup"><span data-stu-id="85854-127">See [Morphology modes](#morphology-modes) for more info.</span></span><br/> |
| <span data-ttu-id="85854-128">寬度</span><span class="sxs-lookup"><span data-stu-id="85854-128">Width</span></span><br/> <span data-ttu-id="85854-129">D2D1 \_ MORPHOLOGY \_ 的 \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="85854-129">D2D1\_MORPHOLOGY\_PROP\_WIDTH</span></span><br/>   | <span data-ttu-id="85854-130">UINT</span><span class="sxs-lookup"><span data-stu-id="85854-130">UINT</span></span><br/> <span data-ttu-id="85854-131">1</span><span class="sxs-lookup"><span data-stu-id="85854-131">1</span></span><br/>                                               | <span data-ttu-id="85854-132">以 X 方向的核心大小。</span><span class="sxs-lookup"><span data-stu-id="85854-132">Size of the kernel in the X direction.</span></span> <span data-ttu-id="85854-133">單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="85854-133">The units are in DIPs.</span></span> <span data-ttu-id="85854-134">值必須介於1到100（含）之間。</span><span class="sxs-lookup"><span data-stu-id="85854-134">Values must be between 1 and 100 inclusive.</span></span>                                                         |
| <span data-ttu-id="85854-135">高度</span><span class="sxs-lookup"><span data-stu-id="85854-135">Height</span></span><br/> <span data-ttu-id="85854-136">D2D1 \_ MORPHOLOGY \_ 的 \_ 高度</span><span class="sxs-lookup"><span data-stu-id="85854-136">D2D1\_MORPHOLOGY\_PROP\_HEIGHT</span></span><br/> | <span data-ttu-id="85854-137">UINT</span><span class="sxs-lookup"><span data-stu-id="85854-137">UINT</span></span><br/> <span data-ttu-id="85854-138">1</span><span class="sxs-lookup"><span data-stu-id="85854-138">1</span></span><br/>                                               | <span data-ttu-id="85854-139">核心在 Y 方向的大小。</span><span class="sxs-lookup"><span data-stu-id="85854-139">Size of the kernel in the Y direction.</span></span> <span data-ttu-id="85854-140">單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="85854-140">The units are in DIPs.</span></span> <span data-ttu-id="85854-141">值必須介於1到100（含）之間。</span><span class="sxs-lookup"><span data-stu-id="85854-141">Values must be between 1 and 100 inclusive.</span></span>                                                         |



 

## <a name="morphology-modes"></a><span data-ttu-id="85854-142">Morphology 模式</span><span class="sxs-lookup"><span data-stu-id="85854-142">Morphology modes</span></span>



| <span data-ttu-id="85854-143">Name</span><span class="sxs-lookup"><span data-stu-id="85854-143">Name</span></span>                           | <span data-ttu-id="85854-144">描述</span><span class="sxs-lookup"><span data-stu-id="85854-144">Description</span></span>                                                    |
|--------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="85854-145">D2D1 \_ MORPHOLOGY \_ 模式 \_ 瓦解</span><span class="sxs-lookup"><span data-stu-id="85854-145">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span>  | <span data-ttu-id="85854-146">使用核心中每個 RGB 通道的最大值。</span><span class="sxs-lookup"><span data-stu-id="85854-146">The maximum value from each RGB channel in the kernel is used.</span></span> |
| <span data-ttu-id="85854-147">D2D1 \_ MORPHOLOGY \_ 模式 \_ DILATE</span><span class="sxs-lookup"><span data-stu-id="85854-147">D2D1\_MORPHOLOGY\_MODE\_DILATE</span></span> | <span data-ttu-id="85854-148">使用核心中每個 RGB 通道的最小值。</span><span class="sxs-lookup"><span data-stu-id="85854-148">The minimum value from each RGB channel in the kernel is used.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="85854-149">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="85854-149">Output bitmap</span></span>

<span data-ttu-id="85854-150">若為 DILATE 模式，輸出點陣圖大小會增加：</span><span class="sxs-lookup"><span data-stu-id="85854-150">For DILATE mode, the Output Bitmap size grows:</span></span> 

| <span data-ttu-id="85854-151">需求</span><span class="sxs-lookup"><span data-stu-id="85854-151">Requirement</span></span> | <span data-ttu-id="85854-152">值</span><span class="sxs-lookup"><span data-stu-id="85854-152">Value</span></span> |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="85854-153">輸出點陣圖成長 X =</span><span class="sxs-lookup"><span data-stu-id="85854-153">Output Bitmap Growth X =</span></span> | <span data-ttu-id="85854-154">整數 (浮點數 (寬度) \* ( (使用者 DPI) /96) ) </span><span class="sxs-lookup"><span data-stu-id="85854-154">INT(FLOAT(Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="85854-155">輸出點陣圖成長 Y =</span><span class="sxs-lookup"><span data-stu-id="85854-155">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="85854-156">INT (FLOAT (Height) \* ( (使用者 DPI) /96) ) </span><span class="sxs-lookup"><span data-stu-id="85854-156">INT(FLOAT(Height) \* ((User DPI) / 96))</span></span> |



 

<span data-ttu-id="85854-157">針對瓦解模式，輸出點陣圖大小會縮小：</span><span class="sxs-lookup"><span data-stu-id="85854-157">For ERODE mode, the Output Bitmap size shrinks:</span></span>

| <span data-ttu-id="85854-158">需求</span><span class="sxs-lookup"><span data-stu-id="85854-158">Requirement</span></span> | <span data-ttu-id="85854-159">值</span><span class="sxs-lookup"><span data-stu-id="85854-159">Value</span></span> |
|--------------------------|------------------------------------------|
| <span data-ttu-id="85854-160">輸出點陣圖成長 X =</span><span class="sxs-lookup"><span data-stu-id="85854-160">Output Bitmap Growth X =</span></span> | <span data-ttu-id="85854-161">INT (FLOAT ( 寬度) \* ( (使用者 DPI) /96) ) </span><span class="sxs-lookup"><span data-stu-id="85854-161">INT(FLOAT(-Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="85854-162">輸出點陣圖成長 Y =</span><span class="sxs-lookup"><span data-stu-id="85854-162">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="85854-163">INT (FLOAT (-Height) \* ( (使用者 DPI) /96) ) </span><span class="sxs-lookup"><span data-stu-id="85854-163">INT(FLOAT(-Height) \* ((User DPI) / 96))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="85854-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="85854-164">Requirements</span></span>



| <span data-ttu-id="85854-165">需求</span><span class="sxs-lookup"><span data-stu-id="85854-165">Requirement</span></span> | <span data-ttu-id="85854-166">值</span><span class="sxs-lookup"><span data-stu-id="85854-166">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85854-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85854-167">Minimum supported client</span></span> | <span data-ttu-id="85854-168">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85854-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="85854-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85854-169">Minimum supported server</span></span> | <span data-ttu-id="85854-170">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85854-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="85854-171">標頭</span><span class="sxs-lookup"><span data-stu-id="85854-171">Header</span></span>                   | <span data-ttu-id="85854-172">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="85854-172">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="85854-173">程式庫</span><span class="sxs-lookup"><span data-stu-id="85854-173">Library</span></span>                  | <span data-ttu-id="85854-174">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="85854-174">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="85854-175">相關主題</span><span class="sxs-lookup"><span data-stu-id="85854-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85854-176">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="85854-176">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

