---
title: 銳化效果
description: 將影像銳化。
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54203cfeb786204500c905e2ff4cfc83bf9719e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685827"
---
# <a name="sharpen-effect"></a><span data-ttu-id="a5072-103">銳化效果</span><span class="sxs-lookup"><span data-stu-id="a5072-103">Sharpen effect</span></span>

<span data-ttu-id="a5072-104">將影像銳化。</span><span class="sxs-lookup"><span data-stu-id="a5072-104">Sharpens the image.</span></span>

<span data-ttu-id="a5072-105">這項效果的 CLSID 是 CLSID \_ D2D1Sharpen。</span><span class="sxs-lookup"><span data-stu-id="a5072-105">The CLSID for this effect is CLSID\_D2D1Sharpen.</span></span>

-   [<span data-ttu-id="a5072-106">範例影像</span><span class="sxs-lookup"><span data-stu-id="a5072-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="a5072-107">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="a5072-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="a5072-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="a5072-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="a5072-109">需求</span><span class="sxs-lookup"><span data-stu-id="a5072-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a5072-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5072-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="a5072-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="a5072-111">Example image</span></span>

![效果輸出的範例](images/sharpen-effect.png)

## <a name="sample-code"></a><span data-ttu-id="a5072-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="a5072-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="a5072-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="a5072-114">Effect properties</span></span>

<span data-ttu-id="a5072-115">銳化效果的屬性是由 [**D2D1 \_ 銳化 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="a5072-115">The properties for the sharpen effect are defined by the [**D2D1\_SHARPEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5072-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5072-116">Requirements</span></span>



| <span data-ttu-id="a5072-117">需求</span><span class="sxs-lookup"><span data-stu-id="a5072-117">Requirement</span></span> | <span data-ttu-id="a5072-118">值</span><span class="sxs-lookup"><span data-stu-id="a5072-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="a5072-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5072-119">Minimum supported client</span></span> | <span data-ttu-id="a5072-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5072-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a5072-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5072-121">Minimum supported server</span></span> | <span data-ttu-id="a5072-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5072-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="a5072-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a5072-123">Header</span></span>                   | <span data-ttu-id="a5072-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="a5072-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="a5072-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5072-125">Library</span></span>                  | <span data-ttu-id="a5072-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="a5072-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="a5072-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5072-127">Related topics</span></span>

* [<span data-ttu-id="a5072-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="a5072-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



