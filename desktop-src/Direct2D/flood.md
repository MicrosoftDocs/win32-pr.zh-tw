---
title: 大量效果
description: 使用洪水效果，根據指定的色彩和 Alpha 值產生點陣圖。 當您想要特定色彩作為效果的輸入（例如背景色彩）時，可以使用此效果。
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- 大量效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934759"
---
# <a name="flood-effect"></a><span data-ttu-id="4cbbb-105">大量效果</span><span class="sxs-lookup"><span data-stu-id="4cbbb-105">Flood effect</span></span>

<span data-ttu-id="4cbbb-106">使用洪水效果，根據指定的色彩和 Alpha 值產生點陣圖。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-106">Use the flood effect to generate a bitmap based on the specified color and alpha value.</span></span> <span data-ttu-id="4cbbb-107">當您想要特定色彩作為效果的輸入（例如背景色彩）時，可以使用此效果。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-107">You can use this effect when you want a specific color as an input for an effect, like a background color.</span></span>

> [!Note]  
> <span data-ttu-id="4cbbb-108">效果會依照指定的色彩值沿著指定的色彩值傳遞。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-108">The effect passes along the specified color value as specified.</span></span> <span data-ttu-id="4cbbb-109">如果您打算將輸出傳遞到預期已預先相乘輸入的效果，則必須手動將值相乘。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-109">You must manually pre-multiply the values if you plan to pass the output to effects that expect a pre-multiplied input.</span></span>

 

<span data-ttu-id="4cbbb-110">這項效果的 CLSID 是 CLSID \_ D2D1Flood。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-110">The CLSID for this effect is CLSID\_D2D1Flood.</span></span>

<span data-ttu-id="4cbbb-111">洪水效果沒有輸入影像。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-111">The flood effect has no input image.</span></span>

-   [<span data-ttu-id="4cbbb-112">範例影像</span><span class="sxs-lookup"><span data-stu-id="4cbbb-112">Example image</span></span>](#example-image)
-   [<span data-ttu-id="4cbbb-113">效果屬性</span><span class="sxs-lookup"><span data-stu-id="4cbbb-113">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="4cbbb-114">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="4cbbb-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="4cbbb-115">需求</span><span class="sxs-lookup"><span data-stu-id="4cbbb-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4cbbb-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="4cbbb-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="4cbbb-117">範例影像</span><span class="sxs-lookup"><span data-stu-id="4cbbb-117">Example image</span></span>

![輸出綠色的洪水效果影像範例。](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="4cbbb-119">效果屬性</span><span class="sxs-lookup"><span data-stu-id="4cbbb-119">Effect properties</span></span>



| <span data-ttu-id="4cbbb-120">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="4cbbb-120">Display name and index enumeration</span></span>                   | <span data-ttu-id="4cbbb-121">Description</span><span class="sxs-lookup"><span data-stu-id="4cbbb-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cbbb-122">Color</span><span class="sxs-lookup"><span data-stu-id="4cbbb-122">Color</span></span><br/> <span data-ttu-id="4cbbb-123">D2D1 \_ 洪水 \_ 的 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="4cbbb-123">D2D1\_FLOOD\_PROP\_COLOR</span></span><br/> | <span data-ttu-id="4cbbb-124">點陣圖的色彩和不透明度。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-124">The color and opacity of the bitmap.</span></span> <span data-ttu-id="4cbbb-125">這個屬性是 D2D1 \_ 向量 \_ 4F。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-125">This property is a D2D1\_VECTOR\_4F.</span></span> <span data-ttu-id="4cbbb-126">每個通道的個別值都屬於 FLOAT、未系結和無數量的型別。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-126">The individual values for each channel are of type FLOAT, unbounded and unitless.</span></span> <span data-ttu-id="4cbbb-127">效果不會修改通道的值。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-127">The effect doesn't modify the values for the channels.</span></span><br/> <span data-ttu-id="4cbbb-128">每個通道的 RGBA 值範圍從0到1。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-128">The RGBA values for each channel range from 0 to 1.</span></span><br/> <span data-ttu-id="4cbbb-129">此類型為 D2D1 \_ VECTOR \_ 4F。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-129">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="4cbbb-130">預設值為 {0.0 f、0.0 f、0.0 f、1.0 f}。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-130">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="4cbbb-131">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="4cbbb-131">Output bitmap</span></span>

<span data-ttu-id="4cbbb-132">此效果會產生邏輯上無限大小的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="4cbbb-132">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cbbb-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cbbb-133">Requirements</span></span>



| <span data-ttu-id="4cbbb-134">需求</span><span class="sxs-lookup"><span data-stu-id="4cbbb-134">Requirement</span></span> | <span data-ttu-id="4cbbb-135">值</span><span class="sxs-lookup"><span data-stu-id="4cbbb-135">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4cbbb-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cbbb-136">Minimum supported client</span></span> | <span data-ttu-id="4cbbb-137">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cbbb-137">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4cbbb-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cbbb-138">Minimum supported server</span></span> | <span data-ttu-id="4cbbb-139">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cbbb-139">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4cbbb-140">標頭</span><span class="sxs-lookup"><span data-stu-id="4cbbb-140">Header</span></span>                   | <span data-ttu-id="4cbbb-141">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="4cbbb-141">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="4cbbb-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="4cbbb-142">Library</span></span>                  | <span data-ttu-id="4cbbb-143">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="4cbbb-143">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="4cbbb-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="4cbbb-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cbbb-145">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="4cbbb-145">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

