---
title: 浮凸效果
description: 建立影像的灰階版本，如同已將其加上戳記。
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dde087eb7f85fcd68615c39730bf6208024fc43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685916"
---
# <a name="emboss-effect"></a><span data-ttu-id="6c590-103">浮凸效果</span><span class="sxs-lookup"><span data-stu-id="6c590-103">Emboss effect</span></span>

<span data-ttu-id="6c590-104">建立影像的灰階版本，如同已將其加上戳記。</span><span class="sxs-lookup"><span data-stu-id="6c590-104">Creates a grayscale version of the image that appears as though it has been stamped into paper.</span></span>

<span data-ttu-id="6c590-105">這項效果的 CLSID 是 CLSID \_ D2D1Emboss。</span><span class="sxs-lookup"><span data-stu-id="6c590-105">The CLSID for this effect is CLSID\_D2D1Emboss.</span></span>

-   [<span data-ttu-id="6c590-106">範例影像</span><span class="sxs-lookup"><span data-stu-id="6c590-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="6c590-107">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="6c590-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="6c590-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="6c590-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="6c590-109">需求</span><span class="sxs-lookup"><span data-stu-id="6c590-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6c590-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="6c590-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6c590-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="6c590-111">Example image</span></span>

![效果輸出的範例](images/emboss-effect.png)

## <a name="sample-code"></a><span data-ttu-id="6c590-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="6c590-113">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="6c590-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="6c590-114">Effect properties</span></span>

<span data-ttu-id="6c590-115">浮凸效果的屬性是由 [**D2D1 \_ 浮凸 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="6c590-115">The properties for the emboss effect are defined by the [**D2D1\_EMBOSS\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c590-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c590-116">Requirements</span></span>



| <span data-ttu-id="6c590-117">需求</span><span class="sxs-lookup"><span data-stu-id="6c590-117">Requirement</span></span> | <span data-ttu-id="6c590-118">值</span><span class="sxs-lookup"><span data-stu-id="6c590-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="6c590-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c590-119">Minimum supported client</span></span> | <span data-ttu-id="6c590-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c590-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6c590-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c590-121">Minimum supported server</span></span> | <span data-ttu-id="6c590-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c590-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6c590-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6c590-123">Header</span></span>                   | <span data-ttu-id="6c590-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="6c590-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="6c590-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c590-125">Library</span></span>                  | <span data-ttu-id="6c590-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="6c590-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="6c590-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="6c590-127">Related topics</span></span>

* [<span data-ttu-id="6c590-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="6c590-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
