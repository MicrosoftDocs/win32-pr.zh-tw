---
title: 色調影響
description: 分離項效果會減少影像中的唯一色彩數目。
ms.assetid: e6686998-1246-b3b7-6f4f-212568c3191c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c98c55154300f7b29c23c24e97570335c6e930f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025269"
---
# <a name="posterize-effect"></a><span data-ttu-id="6ba55-103">色調影響</span><span class="sxs-lookup"><span data-stu-id="6ba55-103">Posterize effect</span></span>

<span data-ttu-id="6ba55-104">分離項效果會減少影像中的唯一色彩數目。</span><span class="sxs-lookup"><span data-stu-id="6ba55-104">The posterize effect reduces the number of unique colors in an image.</span></span>

<span data-ttu-id="6ba55-105">這項效果的 CLSID 是 CLSID \_ D2D1Posterize。</span><span class="sxs-lookup"><span data-stu-id="6ba55-105">The CLSID for this effect is CLSID\_D2D1Posterize.</span></span>

-   [<span data-ttu-id="6ba55-106">範例影像</span><span class="sxs-lookup"><span data-stu-id="6ba55-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="6ba55-107">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="6ba55-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="6ba55-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="6ba55-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="6ba55-109">需求</span><span class="sxs-lookup"><span data-stu-id="6ba55-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6ba55-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ba55-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6ba55-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="6ba55-111">Example image</span></span>

![效果輸出的範例](images/posterize-effect.png)

## <a name="sample-code"></a><span data-ttu-id="6ba55-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="6ba55-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> posterizeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Posterize, &posterizeEffect);
 
posterizeEffect->SetInput(0, bitmap);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, 4);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(posterizeEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="6ba55-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="6ba55-114">Effect properties</span></span>

<span data-ttu-id="6ba55-115">分離項效果的屬性是由 [**D2D1 的 \_ 分離 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) 項屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="6ba55-115">The properties for the posterize effect are defined by the [**D2D1\_POSTERIZE\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba55-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ba55-116">Requirements</span></span>



| <span data-ttu-id="6ba55-117">需求</span><span class="sxs-lookup"><span data-stu-id="6ba55-117">Requirement</span></span> | <span data-ttu-id="6ba55-118">值</span><span class="sxs-lookup"><span data-stu-id="6ba55-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="6ba55-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ba55-119">Minimum supported client</span></span> | <span data-ttu-id="6ba55-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ba55-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6ba55-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ba55-121">Minimum supported server</span></span> | <span data-ttu-id="6ba55-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ba55-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6ba55-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6ba55-123">Header</span></span>                   | <span data-ttu-id="6ba55-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="6ba55-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="6ba55-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ba55-125">Library</span></span>                  | <span data-ttu-id="6ba55-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="6ba55-126">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="6ba55-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ba55-127">Related topics</span></span>

* [<span data-ttu-id="6ba55-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="6ba55-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


