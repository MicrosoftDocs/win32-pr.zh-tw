---
title: 色調到 RGB 效果
description: 將 HSL (色調、飽和度、亮度) 或 HSV (色調、飽和度、值) 影像轉換成 RGB 色彩空間。
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934306"
---
# <a name="hue-to-rgb-effect"></a><span data-ttu-id="7a910-103">色調到 RGB 效果</span><span class="sxs-lookup"><span data-stu-id="7a910-103">Hue-to-RGB effect</span></span>

<span data-ttu-id="7a910-104">將 HSL (色調、飽和度、亮度) 或 HSV (色調、飽和度、值) 影像轉換成 RGB 色彩空間。</span><span class="sxs-lookup"><span data-stu-id="7a910-104">Converts an HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) image to the RGB color space.</span></span>

<span data-ttu-id="7a910-105">HSL 和 HSV 是兩種不同的模型，用來表示圓柱色彩空間中的 RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="7a910-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="7a910-106">這些功能很有用，因為它們可讓您使用更直覺的概念（例如色調和強度），以及結合紅色、綠色和藍色值，來使用色彩的原因。</span><span class="sxs-lookup"><span data-stu-id="7a910-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="7a910-107">這種效果會傳遞任何輸入 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="7a910-107">This effect passes through any input alpha values.</span></span>

<span data-ttu-id="7a910-108">這項效果的 CLSID 是 CLSID \_ D2D1HueToRgb。</span><span class="sxs-lookup"><span data-stu-id="7a910-108">The CLSID for this effect is CLSID\_D2D1HueToRgb.</span></span>

<span data-ttu-id="7a910-109">若要反轉此效果的行為，請使用 [RGB 到色調效果](rgb-to-hue-effect.md)。</span><span class="sxs-lookup"><span data-stu-id="7a910-109">To reverse the behavior of this effect, use the [RGB to Hue effect](rgb-to-hue-effect.md).</span></span>

-   [<span data-ttu-id="7a910-110">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="7a910-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="7a910-111">效果屬性</span><span class="sxs-lookup"><span data-stu-id="7a910-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="7a910-112">需求</span><span class="sxs-lookup"><span data-stu-id="7a910-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7a910-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a910-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="7a910-114">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="7a910-114">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="7a910-115">效果屬性</span><span class="sxs-lookup"><span data-stu-id="7a910-115">Effect properties</span></span>

<span data-ttu-id="7a910-116">對比效果的屬性是由 [**D2D1 \_ HUETORGB \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="7a910-116">The properties for the contrast effect are defined by the [**D2D1\_HUETORGB\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a910-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a910-117">Requirements</span></span>



| <span data-ttu-id="7a910-118">需求</span><span class="sxs-lookup"><span data-stu-id="7a910-118">Requirement</span></span> | <span data-ttu-id="7a910-119">值</span><span class="sxs-lookup"><span data-stu-id="7a910-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="7a910-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a910-120">Minimum supported client</span></span> | <span data-ttu-id="7a910-121">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a910-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7a910-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a910-122">Minimum supported server</span></span> | <span data-ttu-id="7a910-123">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a910-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7a910-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7a910-124">Header</span></span>                   | <span data-ttu-id="7a910-125">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="7a910-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="7a910-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="7a910-126">Library</span></span>                  | <span data-ttu-id="7a910-127">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="7a910-127">d2d1.lib, dxguid.lib</span></span>                              |



## <a name="related-topics"></a><span data-ttu-id="7a910-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a910-128">Related topics</span></span>

* [<span data-ttu-id="7a910-129">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="7a910-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
