---
title: 棕褐色效果
description: 將影像轉換成懷舊色調。
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6ead1d439e86cbd35be14d1f0ae32923de408d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934258"
---
# <a name="sepia-effect"></a><span data-ttu-id="ebeb9-103">棕褐色效果</span><span class="sxs-lookup"><span data-stu-id="ebeb9-103">Sepia effect</span></span>

<span data-ttu-id="ebeb9-104">將影像轉換成懷舊色調。</span><span class="sxs-lookup"><span data-stu-id="ebeb9-104">Converts an image to sepia tones.</span></span>

<span data-ttu-id="ebeb9-105">這項效果的 CLSID 是 CLSID \_ D2D1Sepia。</span><span class="sxs-lookup"><span data-stu-id="ebeb9-105">The CLSID for this effect is CLSID\_D2D1Sepia.</span></span>

-   [<span data-ttu-id="ebeb9-106">範例影像</span><span class="sxs-lookup"><span data-stu-id="ebeb9-106">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="ebeb9-107">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="ebeb9-107">Sample Code</span></span>](#sample-code)
-   [<span data-ttu-id="ebeb9-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="ebeb9-108">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ebeb9-109">需求</span><span class="sxs-lookup"><span data-stu-id="ebeb9-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ebeb9-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebeb9-110">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ebeb9-111">範例影像</span><span class="sxs-lookup"><span data-stu-id="ebeb9-111">Example image</span></span>

![效果輸出的範例](images/sepia-effect.png)

## <a name="sample-code"></a><span data-ttu-id="ebeb9-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="ebeb9-113">Sample code</span></span>


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a><span data-ttu-id="ebeb9-114">效果屬性</span><span class="sxs-lookup"><span data-stu-id="ebeb9-114">Effect properties</span></span>

<span data-ttu-id="ebeb9-115">棕褐色效果的屬性是由 [**D2D1 的 \_ 棕褐色 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="ebeb9-115">The properties for the sepia effect are defined by the [**D2D1\_SEPIA\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebeb9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebeb9-116">Requirements</span></span>



| <span data-ttu-id="ebeb9-117">需求</span><span class="sxs-lookup"><span data-stu-id="ebeb9-117">Requirement</span></span> | <span data-ttu-id="ebeb9-118">值</span><span class="sxs-lookup"><span data-stu-id="ebeb9-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="ebeb9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebeb9-119">Minimum supported client</span></span> | <span data-ttu-id="ebeb9-120">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebeb9-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ebeb9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebeb9-121">Minimum supported server</span></span> | <span data-ttu-id="ebeb9-122">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebeb9-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ebeb9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ebeb9-123">Header</span></span>                   | <span data-ttu-id="ebeb9-124">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="ebeb9-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="ebeb9-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="ebeb9-125">Library</span></span>                  | <span data-ttu-id="ebeb9-126">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="ebeb9-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="ebeb9-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebeb9-127">Related topics</span></span>

* [<span data-ttu-id="ebeb9-128">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="ebeb9-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




