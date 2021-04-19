---
title: 'ID2D1Brush SetTransform 方法 (D2d1 \_ 1 .h) '
description: 設定套用至筆刷的轉換。
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- SetTransform 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997036"
---
# <a name="id2d1brushsettransform-methods"></a><span data-ttu-id="17da6-104">ID2D1Brush：： SetTransform 方法</span><span class="sxs-lookup"><span data-stu-id="17da6-104">ID2D1Brush::SetTransform methods</span></span>

<span data-ttu-id="17da6-105">設定套用至筆刷的轉換。</span><span class="sxs-lookup"><span data-stu-id="17da6-105">Sets the transformation applied to the brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="17da6-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="17da6-106">Overload list</span></span>



| <span data-ttu-id="17da6-107">方法</span><span class="sxs-lookup"><span data-stu-id="17da6-107">Method</span></span>                                                                                       | <span data-ttu-id="17da6-108">描述</span><span class="sxs-lookup"><span data-stu-id="17da6-108">Description</span></span>                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span data-ttu-id="17da6-109">[**SetTransform (D2D1 \_ 矩陣 \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="17da6-109">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="17da6-110">設定套用至筆刷的轉換。</span><span class="sxs-lookup"><span data-stu-id="17da6-110">Sets the transformation applied to the brush.</span></span><br/> |
| <span data-ttu-id="17da6-111">[**SetTransform (D2D1 \_ 矩陣 \_ 3X2 \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="17da6-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="17da6-112">設定套用至筆刷的轉換。</span><span class="sxs-lookup"><span data-stu-id="17da6-112">Sets the transformation applied to the brush.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="17da6-113">備註</span><span class="sxs-lookup"><span data-stu-id="17da6-113">Remarks</span></span>

<span data-ttu-id="17da6-114">當您使用筆刷繪製時，它會在呈現目標的座標空間中繪製。</span><span class="sxs-lookup"><span data-stu-id="17da6-114">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="17da6-115">筆刷不會自動自行定位，以配合正在繪製的物件;根據預設，它們會在呈現目標的原點 (0、0) 開始繪製。</span><span class="sxs-lookup"><span data-stu-id="17da6-115">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="17da6-116">您可以藉由設定起點和終點，將 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 所定義的漸層「移動」至目的地區域。</span><span class="sxs-lookup"><span data-stu-id="17da6-116">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="17da6-117">同樣地，您可以藉由變更中央和半徑來移動 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 所定義的漸層。</span><span class="sxs-lookup"><span data-stu-id="17da6-117">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="17da6-118">若要將 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 的內容對齊正在繪製的區域，您可以使用 **SetTransform** 方法將點陣圖轉譯為所需的位置。</span><span class="sxs-lookup"><span data-stu-id="17da6-118">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the **SetTransform** method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="17da6-119">此轉換只會影響筆刷;它不會影響呈現目標所繪製的任何其他內容。</span><span class="sxs-lookup"><span data-stu-id="17da6-119">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="17da6-120">下圖顯示使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 填滿位於 (100，100) 之矩形的效果。</span><span class="sxs-lookup"><span data-stu-id="17da6-120">The following illustrations show the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="17da6-121">左圖上的圖例顯示填滿矩形的結果，而不會轉換筆刷：點陣圖是在轉譯目標的原點繪製。</span><span class="sxs-lookup"><span data-stu-id="17da6-121">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="17da6-122">如此一來，矩形中只會出現點陣圖的一部分。</span><span class="sxs-lookup"><span data-stu-id="17da6-122">As a result, only a portion of the bitmap appears in the rectangle.</span></span>

<span data-ttu-id="17da6-123">右邊的圖例顯示轉換 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 的結果，使其內容會向右移動50圖元，並向下移動50圖元。</span><span class="sxs-lookup"><span data-stu-id="17da6-123">The illustration on the right shows the result of transforming the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="17da6-124">點陣圖現在會填滿矩形。</span><span class="sxs-lookup"><span data-stu-id="17da6-124">The bitmap now fills the rectangle.</span></span>

![兩個方塊的圖例，其中一個是以沒有已轉換筆刷的點陣圖繪製，另一個則使用已轉換的筆刷繪製](images/brushes-ovw-transform.png)

## <a name="examples"></a><span data-ttu-id="17da6-126">範例</span><span class="sxs-lookup"><span data-stu-id="17da6-126">Examples</span></span>

<span data-ttu-id="17da6-127">下列程式碼範例示範如何建立在上圖中右圖所示的轉換。</span><span class="sxs-lookup"><span data-stu-id="17da6-127">The following code examples show how to create the transformation shown in the right diagram in the preceding illustration.</span></span> <span data-ttu-id="17da6-128">首先，將翻譯套用至 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)，並沿著 y 軸沿著 X 軸和50圖元向下移動筆刷50圖元。</span><span class="sxs-lookup"><span data-stu-id="17da6-128">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="17da6-129">然後使用 **ID2D1BitmapBrush** 來填滿左上角的矩形，其位於 (100、100) ，而右下角的 (200，200) 。</span><span class="sxs-lookup"><span data-stu-id="17da6-129">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a><span data-ttu-id="17da6-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="17da6-130">Requirements</span></span>



| <span data-ttu-id="17da6-131">需求</span><span class="sxs-lookup"><span data-stu-id="17da6-131">Requirement</span></span> | <span data-ttu-id="17da6-132">值</span><span class="sxs-lookup"><span data-stu-id="17da6-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17da6-133">標頭</span><span class="sxs-lookup"><span data-stu-id="17da6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="17da6-134"><dt>D2d1 \_ 1. h (包括 D2d1) </dt></span><span class="sxs-lookup"><span data-stu-id="17da6-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="17da6-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="17da6-135">Library</span></span><br/> | <dl> <span data-ttu-id="17da6-136"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="17da6-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="17da6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="17da6-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="17da6-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17da6-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="17da6-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17da6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17da6-140">筆刷概觀</span><span class="sxs-lookup"><span data-stu-id="17da6-140">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="17da6-141">**ID2D1Brush**</span><span class="sxs-lookup"><span data-stu-id="17da6-141">**ID2D1Brush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

<span data-ttu-id="17da6-142">�</span><span class="sxs-lookup"><span data-stu-id="17da6-142">�</span></span>

<span data-ttu-id="17da6-143">�</span><span class="sxs-lookup"><span data-stu-id="17da6-143">�</span></span>
