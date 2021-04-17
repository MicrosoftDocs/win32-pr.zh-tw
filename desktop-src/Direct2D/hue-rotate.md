---
title: 色調 rotatation 效果
description: 使用 [色調旋轉效果] 可根據旋轉角度套用色彩矩陣，以改變影像的色調。
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- 色調 rotatation 效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104566090"
---
# <a name="hue-rotatation-effect"></a><span data-ttu-id="7e2c0-104">色調 rotatation 效果</span><span class="sxs-lookup"><span data-stu-id="7e2c0-104">Hue rotatation effect</span></span>

<span data-ttu-id="7e2c0-105">使用 [色調旋轉效果] 可根據旋轉角度套用色彩矩陣，以改變影像的色調。</span><span class="sxs-lookup"><span data-stu-id="7e2c0-105">Use the hue rotate effect to alter the hue of an image by applying a color matrix based on the rotation angle.</span></span>

<span data-ttu-id="7e2c0-106">這項效果的 CLSID 是 CLSID \_ D2D1HueRotation。</span><span class="sxs-lookup"><span data-stu-id="7e2c0-106">The CLSID for this effect is CLSID\_D2D1HueRotation.</span></span>

-   [<span data-ttu-id="7e2c0-107">範例影像</span><span class="sxs-lookup"><span data-stu-id="7e2c0-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="7e2c0-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="7e2c0-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="7e2c0-109">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="7e2c0-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="7e2c0-110">需求</span><span class="sxs-lookup"><span data-stu-id="7e2c0-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7e2c0-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e2c0-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="7e2c0-112">範例影像</span><span class="sxs-lookup"><span data-stu-id="7e2c0-112">Example image</span></span>

<span data-ttu-id="7e2c0-113">此處的範例會顯示色調旋轉效果的輸入和輸出影像，旋轉角度為270度。</span><span class="sxs-lookup"><span data-stu-id="7e2c0-113">The example here shows the input and output images of the hue rotate effect with a rotation angle of 270 degrees.</span></span>



| <span data-ttu-id="7e2c0-114">之前</span><span class="sxs-lookup"><span data-stu-id="7e2c0-114">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)   |
| <span data-ttu-id="7e2c0-116">After</span><span class="sxs-lookup"><span data-stu-id="7e2c0-116">After</span></span>                                                        |
| ![轉換後的影像。](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="7e2c0-118">效果會依據旋轉角度 (*？*) 您使用 [D2D1 HUEROTATION] [ \_ \_ 屬性角度] 屬性指定，來計算色彩矩陣 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7e2c0-118">The effect calculates a color matrix based on the rotation angle (*?*) you specify with the D2D1\_HUEROTATION\_PROP\_ANGLE property.</span></span> <span data-ttu-id="7e2c0-119">以下是矩陣方等。</span><span class="sxs-lookup"><span data-stu-id="7e2c0-119">Here are the matrix equations.</span></span>

![色調旋轉計算](images/hue-formula.png)

<span data-ttu-id="7e2c0-121">所建立的矩陣只取決於旋轉角度。</span><span class="sxs-lookup"><span data-stu-id="7e2c0-121">The matrix created depends only on the rotation angle.</span></span> <span data-ttu-id="7e2c0-122">如果您需要特定的矩陣，您可以使用 [色彩矩陣](color-matrix.md) 效果。</span><span class="sxs-lookup"><span data-stu-id="7e2c0-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="7e2c0-123">效果屬性</span><span class="sxs-lookup"><span data-stu-id="7e2c0-123">Effect properties</span></span>



| <span data-ttu-id="7e2c0-124">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="7e2c0-124">Display name and index enumeration</span></span>                         | <span data-ttu-id="7e2c0-125">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="7e2c0-125">Type and default value</span></span>           | <span data-ttu-id="7e2c0-126">Description</span><span class="sxs-lookup"><span data-stu-id="7e2c0-126">Description</span></span>                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| <span data-ttu-id="7e2c0-127">角度</span><span class="sxs-lookup"><span data-stu-id="7e2c0-127">Angle</span></span><br/> <span data-ttu-id="7e2c0-128">D2D1 \_ HUEROTATION \_ 的 \_ 角度</span><span class="sxs-lookup"><span data-stu-id="7e2c0-128">D2D1\_HUEROTATION\_PROP\_ANGLE</span></span><br/> | <span data-ttu-id="7e2c0-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="7e2c0-129">FLOAT</span></span><br/> <span data-ttu-id="7e2c0-130">0.0f</span><span class="sxs-lookup"><span data-stu-id="7e2c0-130">0.0f</span></span><br/> | <span data-ttu-id="7e2c0-131">用來旋轉色調的角度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="7e2c0-131">The angle to rotate the hue, in degrees.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="7e2c0-132">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="7e2c0-132">Output bitmap</span></span>

<span data-ttu-id="7e2c0-133">輸出點陣圖大小與輸入點陣圖大小相同。</span><span class="sxs-lookup"><span data-stu-id="7e2c0-133">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e2c0-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e2c0-134">Requirements</span></span>



| <span data-ttu-id="7e2c0-135">需求</span><span class="sxs-lookup"><span data-stu-id="7e2c0-135">Requirement</span></span> | <span data-ttu-id="7e2c0-136">值</span><span class="sxs-lookup"><span data-stu-id="7e2c0-136">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2c0-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e2c0-137">Minimum supported client</span></span> | <span data-ttu-id="7e2c0-138">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e2c0-138">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7e2c0-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e2c0-139">Minimum supported server</span></span> | <span data-ttu-id="7e2c0-140">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e2c0-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7e2c0-141">標頭</span><span class="sxs-lookup"><span data-stu-id="7e2c0-141">Header</span></span>                   | <span data-ttu-id="7e2c0-142">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="7e2c0-142">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="7e2c0-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="7e2c0-143">Library</span></span>                  | <span data-ttu-id="7e2c0-144">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="7e2c0-144">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="7e2c0-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="7e2c0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e2c0-146">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="7e2c0-146">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

