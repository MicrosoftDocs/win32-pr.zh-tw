---
title: 對比效果
description: 增加或減少影像的對比。
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025204"
---
# <a name="contrast-effect"></a><span data-ttu-id="7d189-103">對比效果</span><span class="sxs-lookup"><span data-stu-id="7d189-103">Contrast effect</span></span>

<span data-ttu-id="7d189-104">增加或減少影像的對比。</span><span class="sxs-lookup"><span data-stu-id="7d189-104">Increases or decreases the contrast of an image.</span></span>

<span data-ttu-id="7d189-105">這項效果的 CLSID 是 CLSID \_ D2D1Contrast。</span><span class="sxs-lookup"><span data-stu-id="7d189-105">The CLSID for this effect is CLSID\_D2D1Contrast.</span></span>

<span data-ttu-id="7d189-106">對比函式會使用兩個分段二 polynomials 來修改每個色頻的值，其會在點 (0.5、0.5) 上符合斜率持續性。</span><span class="sxs-lookup"><span data-stu-id="7d189-106">The contrast function modifies each color channel value using two, piecewise quadratic polynomials that meet with slope continuity at the point (0.5, 0.5).</span></span>

![分段第二次 polynomials 符合斜率持續性， (0.5，0.5) ](images/contrast-effect-slope.png)

-   [<span data-ttu-id="7d189-108">範例影像</span><span class="sxs-lookup"><span data-stu-id="7d189-108">Example Images</span></span>](#example-images)
-   [<span data-ttu-id="7d189-109">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="7d189-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="7d189-110">效果屬性</span><span class="sxs-lookup"><span data-stu-id="7d189-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="7d189-111">需求</span><span class="sxs-lookup"><span data-stu-id="7d189-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7d189-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d189-112">Related topics</span></span>](#related-topics)

## <a name="example-images"></a><span data-ttu-id="7d189-113">範例影像</span><span class="sxs-lookup"><span data-stu-id="7d189-113">Example images</span></span>

<span data-ttu-id="7d189-114">此範例會顯示套用最大對比度的效果的輸出 (對比度 = 1.0) 。</span><span class="sxs-lookup"><span data-stu-id="7d189-114">This example shows the output of the effect with maximum contrast applied (Contrast = 1.0).</span></span>

<span data-ttu-id="7d189-115">之前</span><span class="sxs-lookup"><span data-stu-id="7d189-115">Before</span></span>

![套用效果之前的影像](images/contrast-effect-before.png)

<span data-ttu-id="7d189-117">After</span><span class="sxs-lookup"><span data-stu-id="7d189-117">After</span></span>

![套用效果之後的影像](images/contrast-effect-after.png)

## <a name="sample-code"></a><span data-ttu-id="7d189-119">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="7d189-119">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="7d189-120">效果屬性</span><span class="sxs-lookup"><span data-stu-id="7d189-120">Effect properties</span></span>

<span data-ttu-id="7d189-121">對比效果的屬性是由 [**D2D1 \_ 對比 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="7d189-121">The properties for the contrast effect are defined by the [**D2D1\_CONTRAST\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d189-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d189-122">Requirements</span></span>

| <span data-ttu-id="7d189-123">需求</span><span class="sxs-lookup"><span data-stu-id="7d189-123">Requirement</span></span> | <span data-ttu-id="7d189-124">值</span><span class="sxs-lookup"><span data-stu-id="7d189-124">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="7d189-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d189-125">Minimum supported client</span></span> | <span data-ttu-id="7d189-126">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d189-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7d189-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d189-127">Minimum supported server</span></span> | <span data-ttu-id="7d189-128">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d189-128">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7d189-129">標頭</span><span class="sxs-lookup"><span data-stu-id="7d189-129">Header</span></span>                   | <span data-ttu-id="7d189-130">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="7d189-130">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="7d189-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="7d189-131">Library</span></span>                  | <span data-ttu-id="7d189-132">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="7d189-132">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="7d189-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d189-133">Related topics</span></span>

* [<span data-ttu-id="7d189-134">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="7d189-134">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
