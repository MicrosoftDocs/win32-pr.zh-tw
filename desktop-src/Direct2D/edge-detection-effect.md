---
title: 邊緣偵測效果
description: 篩選出影像的內容，並在影像的對比區段邊緣留下線條。
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47239bede77dc5d32582c6e83c8101e5c9bbf2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025497"
---
# <a name="edge-detection-effect"></a><span data-ttu-id="5b733-103">邊緣偵測效果</span><span class="sxs-lookup"><span data-stu-id="5b733-103">Edge-detection effect</span></span>

<span data-ttu-id="5b733-104">篩選出影像的內容，並在影像的對比區段邊緣留下線條。</span><span class="sxs-lookup"><span data-stu-id="5b733-104">Filters out the content of an image, leaving lines at the edges of contrasting sections of the image.</span></span>

<span data-ttu-id="5b733-105">這項效果的 CLSID 是 CLSID \_ D2D1EdgeDetection。</span><span class="sxs-lookup"><span data-stu-id="5b733-105">The CLSID for this effect is CLSID\_D2D1EdgeDetection.</span></span>

-   [<span data-ttu-id="5b733-106">範例影像</span><span class="sxs-lookup"><span data-stu-id="5b733-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="5b733-107">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="5b733-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="5b733-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="5b733-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="5b733-109">需求</span><span class="sxs-lookup"><span data-stu-id="5b733-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5b733-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b733-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="5b733-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="5b733-111">Example image</span></span>

![效果輸出的範例](images/edge-detection-effect.png)

## <a name="sample-code"></a><span data-ttu-id="5b733-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="5b733-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="5b733-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="5b733-114">Effect properties</span></span>

<span data-ttu-id="5b733-115">Edge 偵測效果的屬性是由 [**D2D1 \_ EDGEDETECTION \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="5b733-115">The properties for the edge detection effect are defined by the [**D2D1\_EDGEDETECTION\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b733-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b733-116">Requirements</span></span>



| <span data-ttu-id="5b733-117">需求</span><span class="sxs-lookup"><span data-stu-id="5b733-117">Requirement</span></span> | <span data-ttu-id="5b733-118">值</span><span class="sxs-lookup"><span data-stu-id="5b733-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="5b733-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b733-119">Minimum supported client</span></span> | <span data-ttu-id="5b733-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b733-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5b733-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b733-121">Minimum supported server</span></span> | <span data-ttu-id="5b733-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b733-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5b733-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5b733-123">Header</span></span>                   | <span data-ttu-id="5b733-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="5b733-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="5b733-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="5b733-125">Library</span></span>                  | <span data-ttu-id="5b733-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="5b733-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="5b733-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b733-127">Related topics</span></span>

* [<span data-ttu-id="5b733-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="5b733-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
