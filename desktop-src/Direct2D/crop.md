---
title: 裁剪效果
description: 使用裁剪效果來輸出影像的指定區域。
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- 裁剪效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843532"
---
# <a name="crop-effect"></a><span data-ttu-id="c7683-104">裁剪效果</span><span class="sxs-lookup"><span data-stu-id="c7683-104">Crop effect</span></span>

<span data-ttu-id="c7683-105">使用裁剪效果來輸出影像的指定區域。</span><span class="sxs-lookup"><span data-stu-id="c7683-105">Use the crop effect to output a specified region of an image.</span></span>

<span data-ttu-id="c7683-106">這項效果的 CLSID 是 CLSID \_ D2D1Crop。</span><span class="sxs-lookup"><span data-stu-id="c7683-106">The CLSID for this effect is CLSID\_D2D1Crop.</span></span>

-   [<span data-ttu-id="c7683-107">範例影像</span><span class="sxs-lookup"><span data-stu-id="c7683-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="c7683-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="c7683-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="c7683-109">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="c7683-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="c7683-110">需求</span><span class="sxs-lookup"><span data-stu-id="c7683-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c7683-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7683-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="c7683-112">範例影像</span><span class="sxs-lookup"><span data-stu-id="c7683-112">Example image</span></span>



| <span data-ttu-id="c7683-113">之前</span><span class="sxs-lookup"><span data-stu-id="c7683-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| <span data-ttu-id="c7683-115">After</span><span class="sxs-lookup"><span data-stu-id="c7683-115">After</span></span>                                                      |
| ![轉換後的影像。](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="c7683-117">效果屬性</span><span class="sxs-lookup"><span data-stu-id="c7683-117">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c7683-118">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="c7683-118">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="c7683-119">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="c7683-119">Type and default value</span></span></th>
<th><span data-ttu-id="c7683-120">Description</span><span class="sxs-lookup"><span data-stu-id="c7683-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7683-121">Rect</span><span class="sxs-lookup"><span data-stu-id="c7683-121">Rect</span></span><br/></td>
<td><span data-ttu-id="c7683-122">D2D1_VECTOR_4F</span><span class="sxs-lookup"><span data-stu-id="c7683-122">D2D1_VECTOR_4F</span></span><br/></td>
<td><span data-ttu-id="c7683-123">要裁剪的區域 (左、上、寬度、高度) 的形式指定為向量。</span><span class="sxs-lookup"><span data-stu-id="c7683-123">The region to be cropped specified as a vector in the form (left, top, width, height).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7683-124">D2D1_CROP_PROP_RECT</span><span class="sxs-lookup"><span data-stu-id="c7683-124">D2D1_CROP_PROP_RECT</span></span><br/></td>
<td><span data-ttu-id="c7683-125">{-FLT_MAX、-FLT_MAX、FLT_MAX、FLT_MAX}</span><span class="sxs-lookup"><span data-stu-id="c7683-125">{-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}</span></span><br/></td>
<td><span data-ttu-id="c7683-126">單位為 Dip。</span><span class="sxs-lookup"><span data-stu-id="c7683-126">The units are in DIPs.</span></span> <br/>
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="c7683-127">如果矩形與輸入影像的邊緣界限重迭，則會截斷。</span><span class="sxs-lookup"><span data-stu-id="c7683-127">The Rect will be truncated if it overlaps the edge boundaries of the input image.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7683-128">D2D1_CROP_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="c7683-128">D2D1_CROP_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="c7683-129">D2D1_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="c7683-129">D2D1_BORDER_MODE</span></span> <br/> <span data-ttu-id="c7683-130">D2D1_BORDER_MODE_SOFT</span><span class="sxs-lookup"><span data-stu-id="c7683-130">D2D1_BORDER_MODE_SOFT</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="c7683-131">D2D1_BORDER_MODE_SOFT：如果裁剪矩形落在小數圖元座標上，效果會套用消除鋸齒以產生軟邊緣。</span><span class="sxs-lookup"><span data-stu-id="c7683-131">D2D1_BORDER_MODE_SOFT : If the crop rectangle falls on fractional pixel coordinates, the effect applies antialiasing which results in a soft edge.</span></span></li>
<li><span data-ttu-id="c7683-132">D2D1_BORDER_MODE_HARD：如果裁剪矩形落在小數圖元座標上，效果會個，進而導致硬性邊緣。</span><span class="sxs-lookup"><span data-stu-id="c7683-132">D2D1_BORDER_MODE_HARD : If the crop rectangle falls on fractional pixel coordinates, the effect clamps which results in a hard edge.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a><span data-ttu-id="c7683-133">輸出點陣圖</span><span class="sxs-lookup"><span data-stu-id="c7683-133">Output bitmap</span></span>

<span data-ttu-id="c7683-134">這項效果的輸出是 Rect 屬性的大小。</span><span class="sxs-lookup"><span data-stu-id="c7683-134">The output of this effect is the size of the Rect property.</span></span> <span data-ttu-id="c7683-135">長度和寬度為 calc</span><span class="sxs-lookup"><span data-stu-id="c7683-135">The length and width are calc</span></span>

<span data-ttu-id="c7683-136">ulated 使用以下的方公式：</span><span class="sxs-lookup"><span data-stu-id="c7683-136">ulated using the equations here:</span></span> <dl> <span data-ttu-id="c7683-137">輸出長度（以圖元為單位） = (Rect。左) \* (使用者的 DPI/96) </span><span class="sxs-lookup"><span data-stu-id="c7683-137">Output length in Pixels=(Rect.Right-Rect.Left)\*(User's DPI/96)</span></span>  
<span data-ttu-id="c7683-138">輸出高度（以圖元為單位） = (Rect.Bottom-Rect.Top) \* (使用者的 DPI/96) </span><span class="sxs-lookup"><span data-stu-id="c7683-138">Output height in pixels=(Rect.Bottom-Rect.Top)\*(User's DPI/96)</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="c7683-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7683-139">Requirements</span></span>



| <span data-ttu-id="c7683-140">需求</span><span class="sxs-lookup"><span data-stu-id="c7683-140">Requirement</span></span> | <span data-ttu-id="c7683-141">值</span><span class="sxs-lookup"><span data-stu-id="c7683-141">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7683-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7683-142">Minimum supported client</span></span> | <span data-ttu-id="c7683-143">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7683-143">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c7683-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7683-144">Minimum supported server</span></span> | <span data-ttu-id="c7683-145">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7683-145">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="c7683-146">標頭</span><span class="sxs-lookup"><span data-stu-id="c7683-146">Header</span></span>                   | <span data-ttu-id="c7683-147">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="c7683-147">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="c7683-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7683-148">Library</span></span>                  | <span data-ttu-id="c7683-149">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="c7683-149">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="c7683-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="c7683-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7683-151">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="c7683-151">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

