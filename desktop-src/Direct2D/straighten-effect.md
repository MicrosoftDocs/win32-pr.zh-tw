---
title: 伸直效果
description: 旋轉並選擇性地調整影像。
ms.assetid: aa37cdf1-bbb6-db4e-45a7-67c7cc16b7b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8e521ca4c0c452301c0f8031c94ba8c22efe80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104557667"
---
# <a name="straighten-effect"></a><span data-ttu-id="d963d-103">伸直效果</span><span class="sxs-lookup"><span data-stu-id="d963d-103">Straighten effect</span></span>

<span data-ttu-id="d963d-104">旋轉並選擇性地調整影像。</span><span class="sxs-lookup"><span data-stu-id="d963d-104">Rotates and optionally scales an image.</span></span>

<span data-ttu-id="d963d-105">這項效果的 CLSID 是 CLSID \_ D2D1Straighten。</span><span class="sxs-lookup"><span data-stu-id="d963d-105">The CLSID for this effect is CLSID\_D2D1Straighten.</span></span>

-   [<span data-ttu-id="d963d-106">範例影像</span><span class="sxs-lookup"><span data-stu-id="d963d-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="d963d-107">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="d963d-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="d963d-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="d963d-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="d963d-109">需求</span><span class="sxs-lookup"><span data-stu-id="d963d-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d963d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="d963d-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="d963d-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="d963d-111">Example image</span></span>

![效果輸出的範例](images/straighten-effect.png)

## <a name="sample-code"></a><span data-ttu-id="d963d-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="d963d-113">Sample code</span></span>


```cpp
ComPtr<ID2D1Effect> straightenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Straighten, &straightenEffect);
 
straightenEffect->SetInput(0, bitmap);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_ANGLE, 12.0f);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, true);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_SCALE_MODE, D2D1_STRAIGHTEN_SCALE_MODE_LINEAR);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(straightenEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="d963d-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="d963d-114">Effect properties</span></span>

<span data-ttu-id="d963d-115">伸直效果的屬性是由 [**D2D1 的 \_ 伸直 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="d963d-115">The properties for the straighten effect are defined by the [**D2D1\_STRAIGHTEN\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d963d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d963d-116">Requirements</span></span>



| <span data-ttu-id="d963d-117">需求</span><span class="sxs-lookup"><span data-stu-id="d963d-117">Requirement</span></span> | <span data-ttu-id="d963d-118">值</span><span class="sxs-lookup"><span data-stu-id="d963d-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="d963d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d963d-119">Minimum supported client</span></span> | <span data-ttu-id="d963d-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d963d-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d963d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d963d-121">Minimum supported server</span></span> | <span data-ttu-id="d963d-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d963d-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d963d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d963d-123">Header</span></span>                   | <span data-ttu-id="d963d-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="d963d-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="d963d-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="d963d-125">Library</span></span>                  | <span data-ttu-id="d963d-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="d963d-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="d963d-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="d963d-127">Related topics</span></span>

* [<span data-ttu-id="d963d-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="d963d-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

