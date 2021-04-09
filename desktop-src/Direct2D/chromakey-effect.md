---
title: 色度鍵效果
description: 將指定的色彩加或減到 Alpha 的誤差。 例如，色度按鍵可以移除影像的背景，以進行綠色螢幕重迭效果。
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843408"
---
# <a name="chroma-key-effect"></a><span data-ttu-id="c08bd-104">色度鍵效果</span><span class="sxs-lookup"><span data-stu-id="c08bd-104">Chroma-key effect</span></span>

<span data-ttu-id="c08bd-105">將指定的色彩加或減到 Alpha 的誤差。</span><span class="sxs-lookup"><span data-stu-id="c08bd-105">Converts a given color plus or minus a tolerance to alpha.</span></span> <span data-ttu-id="c08bd-106">例如，色度按鍵可以移除影像的背景，以進行綠色螢幕重迭效果。</span><span class="sxs-lookup"><span data-stu-id="c08bd-106">For example, chroma-key can remove the background of an image for a green-screen overlay effect.</span></span>

<span data-ttu-id="c08bd-107">這項效果的 CLSID 是 CLSID \_ D2D1ChromaKey。</span><span class="sxs-lookup"><span data-stu-id="c08bd-107">The CLSID for this effect is CLSID\_D2D1ChromaKey.</span></span>

-   [<span data-ttu-id="c08bd-108">範例影像</span><span class="sxs-lookup"><span data-stu-id="c08bd-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="c08bd-109">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="c08bd-109">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="c08bd-110">效果屬性</span><span class="sxs-lookup"><span data-stu-id="c08bd-110">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c08bd-111">需求</span><span class="sxs-lookup"><span data-stu-id="c08bd-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c08bd-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="c08bd-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c08bd-113">範例影像</span><span class="sxs-lookup"><span data-stu-id="c08bd-113">Example image</span></span>

![效果輸出的範例](images/chromakey-effect.png)

> [!Note]  
> <span data-ttu-id="c08bd-115">在此範例中，色度按鍵效果的輸出是具有棋盤透明背景的第二個影像。</span><span class="sxs-lookup"><span data-stu-id="c08bd-115">In this example, the output of the chroma-key effect is the second image with the checkerboard transparent background.</span></span> <span data-ttu-id="c08bd-116">第三個影像會將它與背景影像合併，以進行最後的綠色螢幕重迭。</span><span class="sxs-lookup"><span data-stu-id="c08bd-116">The third image combines this with a background image for the final green-screen overlay.</span></span>

## <a name="sample-code"></a><span data-ttu-id="c08bd-117">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="c08bd-117">Sample code</span></span>

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="c08bd-118">效果屬性</span><span class="sxs-lookup"><span data-stu-id="c08bd-118">Effect properties</span></span>

<span data-ttu-id="c08bd-119">色度按鍵效果的屬性是由 [**D2D1 \_ CHROMAKEY \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="c08bd-119">The properties for the chroma-key effect are defined by the [**D2D1\_CHROMAKEY\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c08bd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c08bd-120">Requirements</span></span>

| <span data-ttu-id="c08bd-121">需求</span><span class="sxs-lookup"><span data-stu-id="c08bd-121">Requirement</span></span> | <span data-ttu-id="c08bd-122">值</span><span class="sxs-lookup"><span data-stu-id="c08bd-122">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="c08bd-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c08bd-123">Minimum supported client</span></span> | <span data-ttu-id="c08bd-124">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c08bd-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c08bd-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c08bd-125">Minimum supported server</span></span> | <span data-ttu-id="c08bd-126">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c08bd-126">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c08bd-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c08bd-127">Header</span></span>                   | <span data-ttu-id="c08bd-128">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="c08bd-128">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="c08bd-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="c08bd-129">Library</span></span>                  | <span data-ttu-id="c08bd-130">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="c08bd-130">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="c08bd-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="c08bd-131">Related topics</span></span>

* [<span data-ttu-id="c08bd-132">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="c08bd-132">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
