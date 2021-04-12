---
title: 磚效果
description: 使用磚效果來重複指定的影像區域。
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- 磚效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025176"
---
# <a name="tile-effect"></a><span data-ttu-id="23d0f-104">磚效果</span><span class="sxs-lookup"><span data-stu-id="23d0f-104">Tile effect</span></span>

<span data-ttu-id="23d0f-105">使用磚效果來重複指定的影像區域。</span><span class="sxs-lookup"><span data-stu-id="23d0f-105">Use the tile effect to repeat the specified region of the image.</span></span>

<span data-ttu-id="23d0f-106">這項效果的 CLSID 是 CLSID \_ D2D1Tile。</span><span class="sxs-lookup"><span data-stu-id="23d0f-106">The CLSID for this effect is CLSID\_D2D1Tile.</span></span>

## <a name="example-image"></a><span data-ttu-id="23d0f-107">範例影像</span><span class="sxs-lookup"><span data-stu-id="23d0f-107">Example image</span></span>



| <span data-ttu-id="23d0f-108">之前</span><span class="sxs-lookup"><span data-stu-id="23d0f-108">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| <span data-ttu-id="23d0f-110">After</span><span class="sxs-lookup"><span data-stu-id="23d0f-110">After</span></span>                                                      |
| ![轉換後的影像。](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="23d0f-112">效果屬性</span><span class="sxs-lookup"><span data-stu-id="23d0f-112">Effect properties</span></span>



| <span data-ttu-id="23d0f-113">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="23d0f-113">Display name and index enumeration</span></span>                | <span data-ttu-id="23d0f-114">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="23d0f-114">Type and default value</span></span>                                              | <span data-ttu-id="23d0f-115">Description</span><span class="sxs-lookup"><span data-stu-id="23d0f-115">Description</span></span>                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23d0f-116">Rect</span><span class="sxs-lookup"><span data-stu-id="23d0f-116">Rect</span></span><br/> <span data-ttu-id="23d0f-117">D2D1 \_ 圖格的圖示 \_ \_ RECT</span><span class="sxs-lookup"><span data-stu-id="23d0f-117">D2D1\_TILE\_PROP\_RECT</span></span><br/> | <span data-ttu-id="23d0f-118">D2D1 \_ 向量 \_ 4F</span><span class="sxs-lookup"><span data-stu-id="23d0f-118">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="23d0f-119">{0.0 f、0.0 f、100.0 f、100.0 f}</span><span class="sxs-lookup"><span data-stu-id="23d0f-119">{0.0f, 0.0f, 100.0f, 100.0f}</span></span><br/> | <span data-ttu-id="23d0f-120">要並排顯示之影像的區域。</span><span class="sxs-lookup"><span data-stu-id="23d0f-120">The region of the image to be tiled.</span></span> <span data-ttu-id="23d0f-121">這個屬性是 D2D1 \_ 向量 \_ 4F，定義為： (左、上、右、下) 。</span><span class="sxs-lookup"><span data-stu-id="23d0f-121">This property is a D2D1\_VECTOR\_4F defined as: (left, top, right, bottom).</span></span> <span data-ttu-id="23d0f-122">單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="23d0f-122">The units are in DIPs.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="23d0f-123">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="23d0f-123">Output bitmap</span></span>

<span data-ttu-id="23d0f-124">此效果會產生邏輯上無限大小的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="23d0f-124">This effect generates a logically infinite sized bitmap.</span></span>

<span data-ttu-id="23d0f-125">您可以在呼叫 ID2D1DeviceCoNtext 時設定大小，以並排顯示影像並輸出特定大小，而不會產生任何其他效果 [**：:D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))。</span><span class="sxs-lookup"><span data-stu-id="23d0f-125">You can tile an image and output a certain size without any additional effects by setting the size when you call [**ID2D1DeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span></span>

## <a name="requirements"></a><span data-ttu-id="23d0f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="23d0f-126">Requirements</span></span>



| <span data-ttu-id="23d0f-127">需求</span><span class="sxs-lookup"><span data-stu-id="23d0f-127">Requirement</span></span> | <span data-ttu-id="23d0f-128">值</span><span class="sxs-lookup"><span data-stu-id="23d0f-128">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23d0f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23d0f-129">Minimum supported client</span></span> | <span data-ttu-id="23d0f-130">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23d0f-130">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="23d0f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23d0f-131">Minimum supported server</span></span> | <span data-ttu-id="23d0f-132">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23d0f-132">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="23d0f-133">標頭</span><span class="sxs-lookup"><span data-stu-id="23d0f-133">Header</span></span>                   | <span data-ttu-id="23d0f-134">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="23d0f-134">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="23d0f-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="23d0f-135">Library</span></span>                  | <span data-ttu-id="23d0f-136">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="23d0f-136">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="23d0f-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="23d0f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23d0f-138">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="23d0f-138">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

