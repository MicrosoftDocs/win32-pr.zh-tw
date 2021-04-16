---
title: 醒目顯示和陰影效果
description: 調整影像的醒目顯示和陰影。
ms.assetid: ebbb7d99-9144-ffff-af73-d89e7d269924
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d595a5b82a2df0b0b0bab14c03e6a807511ed61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104553668"
---
# <a name="highlights-and-shadows-effect"></a><span data-ttu-id="44012-103">醒目顯示和陰影效果</span><span class="sxs-lookup"><span data-stu-id="44012-103">Highlights and shadows effect</span></span>

<span data-ttu-id="44012-104">調整影像的醒目顯示和陰影。</span><span class="sxs-lookup"><span data-stu-id="44012-104">Adjusts the highlights and shadows of the image.</span></span>

<span data-ttu-id="44012-105">這項效果的 CLSID 是 CLSID \_ D2D1HighlightsShadows。</span><span class="sxs-lookup"><span data-stu-id="44012-105">The CLSID for this effect is CLSID\_D2D1HighlightsShadows.</span></span>

-   [<span data-ttu-id="44012-106">範例影像</span><span class="sxs-lookup"><span data-stu-id="44012-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="44012-107">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="44012-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="44012-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="44012-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="44012-109">需求</span><span class="sxs-lookup"><span data-stu-id="44012-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="44012-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="44012-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="44012-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="44012-111">Example image</span></span>

![效果輸出的範例](images/highlights-and-shadows-effect.png)

## <a name="sample-code"></a><span data-ttu-id="44012-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="44012-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> highlightsAndShadowsEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HighlightsShadows, &highlightsAndShadowsEffect);
 
highlightsAndShadowsEffect->SetInput(0, bitmap);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, 0.0f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, 0.5f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, 0.2f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="44012-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="44012-114">Effect properties</span></span>

<span data-ttu-id="44012-115">醒目顯示和陰影效果的屬性是由 [**D2D1 \_ HIGHLIGHTSANDSHADOWS \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="44012-115">The properties for the highlights and shadows effect are defined by the [**D2D1\_HIGHLIGHTSANDSHADOWS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="44012-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="44012-116">Requirements</span></span>

| <span data-ttu-id="44012-117">需求</span><span class="sxs-lookup"><span data-stu-id="44012-117">Requirement</span></span> | <span data-ttu-id="44012-118">值</span><span class="sxs-lookup"><span data-stu-id="44012-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="44012-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44012-119">Minimum supported client</span></span> | <span data-ttu-id="44012-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44012-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="44012-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44012-121">Minimum supported server</span></span> | <span data-ttu-id="44012-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44012-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="44012-123">標頭</span><span class="sxs-lookup"><span data-stu-id="44012-123">Header</span></span>                   | <span data-ttu-id="44012-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="44012-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="44012-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="44012-125">Library</span></span>                  | <span data-ttu-id="44012-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="44012-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="44012-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="44012-127">Related topics</span></span>

* [<span data-ttu-id="44012-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="44012-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
