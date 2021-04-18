---
title: RGB 到色調效果
description: 將 RGB 影像轉換成 HSL (色調、飽和度、亮度) 或 HSV (色調、飽和度、值) 色彩空間。
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384490"
---
# <a name="rgb-to-hue-effect"></a><span data-ttu-id="b4f1d-103">RGB 到色調效果</span><span class="sxs-lookup"><span data-stu-id="b4f1d-103">RGB-to-hue effect</span></span>

<span data-ttu-id="b4f1d-104">將 RGB 影像轉換成 HSL (色調、飽和度、亮度) 或 HSV (色調、飽和度、值) 色彩空間。</span><span class="sxs-lookup"><span data-stu-id="b4f1d-104">Converts an RGB image to either the HSL (Hue, Saturation, Lightness) or HSV (Hue, Saturation, Value) color spaces.</span></span>

<span data-ttu-id="b4f1d-105">HSL 和 HSV 是兩種不同的模型，用來表示圓柱色彩空間中的 RGB 色彩。</span><span class="sxs-lookup"><span data-stu-id="b4f1d-105">HSL and HSV are two different models for representing an RGB color in a cylindrical color space.</span></span> <span data-ttu-id="b4f1d-106">這些功能很有用，因為它們可讓您使用更直覺的概念（例如色調和強度），以及結合紅色、綠色和藍色值，來使用色彩的原因。</span><span class="sxs-lookup"><span data-stu-id="b4f1d-106">They are useful because they allow you to reason about a color using more intuitive concepts like hue and intensity versus combining red, green and blue values.</span></span>

<span data-ttu-id="b4f1d-107">此效果會將輸出資料正規化 (的色調、HSV 或色調的飽和度值、在 HSL) 的飽和度、亮度、範圍 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="b4f1d-107">This effect normalizes the output data (hue, saturation value for HSV or hue, saturation, lightness for HSL) to the range \[0, 1\].</span></span>

<span data-ttu-id="b4f1d-108">這項效果的 CLSID 是 CLSID \_ D2D1RgbToHue。</span><span class="sxs-lookup"><span data-stu-id="b4f1d-108">The CLSID for this effect is CLSID\_D2D1RgbToHue.</span></span>

<span data-ttu-id="b4f1d-109">若要反轉此效果的行為，請使用 [色調到 RGB 效果](hue-to-rgb-effect.md)。</span><span class="sxs-lookup"><span data-stu-id="b4f1d-109">To reverse the behavior of this effect, use the [Hue to RGB effect](hue-to-rgb-effect.md).</span></span>

-   [<span data-ttu-id="b4f1d-110">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="b4f1d-110">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="b4f1d-111">效果屬性</span><span class="sxs-lookup"><span data-stu-id="b4f1d-111">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b4f1d-112">需求</span><span class="sxs-lookup"><span data-stu-id="b4f1d-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b4f1d-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4f1d-113">Related topics</span></span>](#related-topics)

## <a name="sample-code"></a><span data-ttu-id="b4f1d-114">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="b4f1d-114">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a><span data-ttu-id="b4f1d-115">效果屬性</span><span class="sxs-lookup"><span data-stu-id="b4f1d-115">Effect properties</span></span>

<span data-ttu-id="b4f1d-116">對比效果的屬性是由 [**D2D1 \_ RGBTOHUE \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="b4f1d-116">The properties for the contrast effect are defined by the [**D2D1\_RGBTOHUE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f1d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4f1d-117">Requirements</span></span>



| <span data-ttu-id="b4f1d-118">需求</span><span class="sxs-lookup"><span data-stu-id="b4f1d-118">Requirement</span></span> | <span data-ttu-id="b4f1d-119">值</span><span class="sxs-lookup"><span data-stu-id="b4f1d-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="b4f1d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4f1d-120">Minimum supported client</span></span> | <span data-ttu-id="b4f1d-121">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4f1d-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b4f1d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4f1d-122">Minimum supported server</span></span> | <span data-ttu-id="b4f1d-123">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4f1d-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b4f1d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b4f1d-124">Header</span></span>                   | <span data-ttu-id="b4f1d-125">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="b4f1d-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="b4f1d-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="b4f1d-126">Library</span></span>                  | <span data-ttu-id="b4f1d-127">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="b4f1d-127">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="b4f1d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4f1d-128">Related topics</span></span>

* [<span data-ttu-id="b4f1d-129">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="b4f1d-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
