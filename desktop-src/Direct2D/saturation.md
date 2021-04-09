---
title: 飽和度效果
description: 使用此效果來改變影像的飽和度。
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- 飽和度效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024970"
---
# <a name="saturation-effect"></a><span data-ttu-id="ae5f1-104">飽和度效果</span><span class="sxs-lookup"><span data-stu-id="ae5f1-104">Saturation effect</span></span>

<span data-ttu-id="ae5f1-105">使用此效果來改變影像的飽和度。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-105">Use this effect to alter the saturation of an image.</span></span> <span data-ttu-id="ae5f1-106">飽和度效果是 [色彩矩陣](color-matrix.md) 效果的特製化。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-106">The saturation effect is a specialization of the [color matrix](color-matrix.md) effect.</span></span>

<span data-ttu-id="ae5f1-107">這項效果的 CLSID 是 CLSID \_ D2D1Saturation。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-107">The CLSID for this effect is CLSID\_D2D1Saturation.</span></span>

-   [<span data-ttu-id="ae5f1-108">範例影像</span><span class="sxs-lookup"><span data-stu-id="ae5f1-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ae5f1-109">效果屬性</span><span class="sxs-lookup"><span data-stu-id="ae5f1-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ae5f1-110">需求</span><span class="sxs-lookup"><span data-stu-id="ae5f1-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ae5f1-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="ae5f1-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ae5f1-112">範例影像</span><span class="sxs-lookup"><span data-stu-id="ae5f1-112">Example image</span></span>

<span data-ttu-id="ae5f1-113">此處的範例顯示飽和度為0% 的飽和度效果輸入和輸出影像。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-113">The example here shows the input and output images of the saturation effect with a saturation of 0%.</span></span>



| <span data-ttu-id="ae5f1-114">之前</span><span class="sxs-lookup"><span data-stu-id="ae5f1-114">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)  |
| <span data-ttu-id="ae5f1-116">After</span><span class="sxs-lookup"><span data-stu-id="ae5f1-116">After</span></span>                                                       |
| ![轉換後的影像。](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="ae5f1-118">效果會根據在此方程式中的飽和度值 (*s* 來計算色彩矩陣，) 您使用 [D2D1 \_ 飽和度 \_ ] \_ 屬性飽和度屬性來指定。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-118">The effect calculates a color matrix based on the saturation value (*s* in the equation here) you specify with the D2D1\_SATURATION\_PROP\_SATURATION property.</span></span> <span data-ttu-id="ae5f1-119">矩陣方程式如下所示。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-119">The matrix equation is shown here.</span></span>

![計算飽和度矩陣的公式。](images/saturation-formula.png)

<span data-ttu-id="ae5f1-121">所建立的矩陣只取決於飽和度值。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-121">The matrix created depends only on the saturation value.</span></span> <span data-ttu-id="ae5f1-122">如果您需要特定的矩陣，您可以使用 [色彩矩陣](color-matrix.md) 效果。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

<span data-ttu-id="ae5f1-123">此效果會取用和輸出預乘的 Alpha 影像。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-123">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="ae5f1-124">除非完全不透明，否則效果無法用於直接的 Alpha 影像。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-124">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="ae5f1-125">效果屬性</span><span class="sxs-lookup"><span data-stu-id="ae5f1-125">Effect properties</span></span>



| <span data-ttu-id="ae5f1-126">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="ae5f1-126">Display name and index enumeration</span></span>                                  | <span data-ttu-id="ae5f1-127">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="ae5f1-127">Type and default value</span></span>           | <span data-ttu-id="ae5f1-128">Description</span><span class="sxs-lookup"><span data-stu-id="ae5f1-128">Description</span></span>                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5f1-129">飽和度</span><span class="sxs-lookup"><span data-stu-id="ae5f1-129">Saturation</span></span><br/> <span data-ttu-id="ae5f1-130">D2D1 \_ 飽和度 \_ 的 \_ 飽和度</span><span class="sxs-lookup"><span data-stu-id="ae5f1-130">D2D1\_SATURATION\_PROP\_SATURATION</span></span><br/> | <span data-ttu-id="ae5f1-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ae5f1-131">FLOAT</span></span><br/> <span data-ttu-id="ae5f1-132">0.5 f</span><span class="sxs-lookup"><span data-stu-id="ae5f1-132">0.5f</span></span><br/> | <span data-ttu-id="ae5f1-133">影像的飽和度。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-133">The saturation of the image.</span></span> <span data-ttu-id="ae5f1-134">您可以將飽和度設定為介於0和1之間的值。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-134">You can set the saturation to a value between 0 and 1.</span></span> <span data-ttu-id="ae5f1-135">如果您將它設定為1，則輸出影像會完全飽和。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-135">If you set it to 1 the output image is fully saturated.</span></span> <span data-ttu-id="ae5f1-136">如果您將它設定為0，則輸出影像為單色。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-136">If you set it to 0 the output image is monochrome.</span></span> <span data-ttu-id="ae5f1-137">飽和度值沒有用。</span><span class="sxs-lookup"><span data-stu-id="ae5f1-137">The saturation value is unitless.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ae5f1-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae5f1-138">Requirements</span></span>



| <span data-ttu-id="ae5f1-139">需求</span><span class="sxs-lookup"><span data-stu-id="ae5f1-139">Requirement</span></span> | <span data-ttu-id="ae5f1-140">值</span><span class="sxs-lookup"><span data-stu-id="ae5f1-140">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5f1-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae5f1-141">Minimum supported client</span></span> | <span data-ttu-id="ae5f1-142">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae5f1-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ae5f1-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae5f1-143">Minimum supported server</span></span> | <span data-ttu-id="ae5f1-144">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae5f1-144">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ae5f1-145">標頭</span><span class="sxs-lookup"><span data-stu-id="ae5f1-145">Header</span></span>                   | <span data-ttu-id="ae5f1-146">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="ae5f1-146">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ae5f1-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="ae5f1-147">Library</span></span>                  | <span data-ttu-id="ae5f1-148">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="ae5f1-148">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ae5f1-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="ae5f1-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae5f1-150">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ae5f1-150">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

