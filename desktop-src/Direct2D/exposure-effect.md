---
title: 曝光效果
description: 增加或減少影像的曝光。
ms.assetid: d384f539-5c19-53c7-e52b-bf833e221449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6f5bda52fecc0b5e3896515b04a6560f17da49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934761"
---
# <a name="exposure-effect"></a><span data-ttu-id="5f74f-103">曝光效果</span><span class="sxs-lookup"><span data-stu-id="5f74f-103">Exposure effect</span></span>

<span data-ttu-id="5f74f-104">增加或減少影像的曝光。</span><span class="sxs-lookup"><span data-stu-id="5f74f-104">Increase or decreases the exposure of the image.</span></span>

<span data-ttu-id="5f74f-105">這項效果的 CLSID 是 CLSID \_ D2D1Exposure。</span><span class="sxs-lookup"><span data-stu-id="5f74f-105">The CLSID for this effect is CLSID\_D2D1Exposure.</span></span>

-   [<span data-ttu-id="5f74f-106">範例影像</span><span class="sxs-lookup"><span data-stu-id="5f74f-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="5f74f-107">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="5f74f-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="5f74f-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="5f74f-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="5f74f-109">需求</span><span class="sxs-lookup"><span data-stu-id="5f74f-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5f74f-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f74f-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="5f74f-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="5f74f-111">Example image</span></span>

![效果輸出的範例](images/exposure-effect.png)

## <a name="sample-code"></a><span data-ttu-id="5f74f-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="5f74f-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> exposureEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Exposure, &exposureEffect);
 
exposureEffect->SetInput(0, bitmap);
exposureEffect->SetValue(D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(exposureEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="5f74f-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="5f74f-114">Effect properties</span></span>

<span data-ttu-id="5f74f-115">曝光效果的屬性是由 [**D2D1 \_ 曝光 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="5f74f-115">The properties for the exposure effect are defined by the [**D2D1\_EXPOSURE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f74f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f74f-116">Requirements</span></span>



| <span data-ttu-id="5f74f-117">需求</span><span class="sxs-lookup"><span data-stu-id="5f74f-117">Requirement</span></span> | <span data-ttu-id="5f74f-118">值</span><span class="sxs-lookup"><span data-stu-id="5f74f-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="5f74f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f74f-119">Minimum supported client</span></span> | <span data-ttu-id="5f74f-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f74f-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5f74f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f74f-121">Minimum supported server</span></span> | <span data-ttu-id="5f74f-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f74f-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="5f74f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5f74f-123">Header</span></span>                   | <span data-ttu-id="5f74f-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="5f74f-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="5f74f-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="5f74f-125">Library</span></span>                  | <span data-ttu-id="5f74f-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="5f74f-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="5f74f-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f74f-127">Related topics</span></span>

* [<span data-ttu-id="5f74f-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="5f74f-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




