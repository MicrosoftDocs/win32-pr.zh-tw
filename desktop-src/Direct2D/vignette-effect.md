---
title: Vignette 效果
description: 將邊緣的輸入影像淡化至使用者集色彩。
ms.assetid: 34da221f-44a2-1d01-d88d-d7846b9770b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fe9302a86a49b060aa05ecb856ce43122d946d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104934"
---
# <a name="vignette-effect"></a><span data-ttu-id="01ed8-103">Vignette 效果</span><span class="sxs-lookup"><span data-stu-id="01ed8-103">Vignette effect</span></span>

<span data-ttu-id="01ed8-104">將邊緣的輸入影像淡化至使用者集色彩。</span><span class="sxs-lookup"><span data-stu-id="01ed8-104">Fades the input image at the edges to a user-set color.</span></span>

<span data-ttu-id="01ed8-105">這項效果的 CLSID 是 CLSID \_ D2D1Vignette。</span><span class="sxs-lookup"><span data-stu-id="01ed8-105">The CLSID for this effect is CLSID\_D2D1Vignette.</span></span>

-   [<span data-ttu-id="01ed8-106">範例影像</span><span class="sxs-lookup"><span data-stu-id="01ed8-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="01ed8-107">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="01ed8-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="01ed8-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="01ed8-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="01ed8-109">需求</span><span class="sxs-lookup"><span data-stu-id="01ed8-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="01ed8-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="01ed8-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="01ed8-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="01ed8-111">Example image</span></span>

![效果輸出的範例](images/vignette-effect.png)

## <a name="sample-code"></a><span data-ttu-id="01ed8-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="01ed8-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> vignetteEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Vignette, &vignetteEffect);
 
vignetteEffect->SetInput(0, bitmap);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_COLOR, );
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_TRANSITION_SIZE, 0.1f);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_STRENGTH, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(vignetteEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="01ed8-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="01ed8-114">Effect properties</span></span>

<span data-ttu-id="01ed8-115">Vignette 效果的屬性是由 [**D2D1 \_ vignette \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="01ed8-115">The properties for the vignette effect are defined by the [**D2D1\_VIGNETTE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="01ed8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="01ed8-116">Requirements</span></span>

| <span data-ttu-id="01ed8-117">需求</span><span class="sxs-lookup"><span data-stu-id="01ed8-117">Requirement</span></span> | <span data-ttu-id="01ed8-118">值</span><span class="sxs-lookup"><span data-stu-id="01ed8-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="01ed8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01ed8-119">Minimum supported client</span></span> | <span data-ttu-id="01ed8-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01ed8-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="01ed8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01ed8-121">Minimum supported server</span></span> | <span data-ttu-id="01ed8-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01ed8-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="01ed8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="01ed8-123">Header</span></span>                   | <span data-ttu-id="01ed8-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="01ed8-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="01ed8-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="01ed8-125">Library</span></span>                  | <span data-ttu-id="01ed8-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="01ed8-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="01ed8-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="01ed8-127">Related topics</span></span>

* [<span data-ttu-id="01ed8-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="01ed8-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
