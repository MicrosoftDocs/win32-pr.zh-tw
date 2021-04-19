---
title: 'ID2D1Factory CreateTransformedGeometry 方法 (D2d1 .h) '
description: 轉換指定的幾何，並將結果儲存為 ID2D1TransformedGeometry 物件。
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- CreateTransformedGeometry 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978629"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a><span data-ttu-id="a1204-104">ID2D1Factory：： CreateTransformedGeometry 方法</span><span class="sxs-lookup"><span data-stu-id="a1204-104">ID2D1Factory::CreateTransformedGeometry methods</span></span>

<span data-ttu-id="a1204-105">轉換指定的幾何，並將結果儲存為 [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="a1204-105">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a1204-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="a1204-106">Overload list</span></span>



| <span data-ttu-id="a1204-107">方法</span><span class="sxs-lookup"><span data-stu-id="a1204-107">Method</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="a1204-108">描述</span><span class="sxs-lookup"><span data-stu-id="a1204-108">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1204-109">[**CreateTransformedGeometry (ID2D1Geometry \* 、D2D \_ 矩陣 \_ 3X2 \_ F \* 、ID2D1TransformedGeometry \* \*)**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a1204-109">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F\*,ID2D1TransformedGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span></span> | <span data-ttu-id="a1204-110">轉換指定的幾何，並將結果儲存為 [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="a1204-110">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |
| <span data-ttu-id="a1204-111">[**CreateTransformedGeometry (ID2D1Geometry \* 、D2D \_ 矩陣 \_ 3X2 \_ F&、ID2D1TransformedGeometry \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span><span class="sxs-lookup"><span data-stu-id="a1204-111">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F&,ID2D1TransformedGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span></span>  | <span data-ttu-id="a1204-112">轉換指定的幾何，並將結果儲存為 [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="a1204-112">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="a1204-113">備註</span><span class="sxs-lookup"><span data-stu-id="a1204-113">Remarks</span></span>

<span data-ttu-id="a1204-114">如同其他資源，轉換的幾何會繼承建立它之 factory 的資源空間和執行緒原則。</span><span class="sxs-lookup"><span data-stu-id="a1204-114">Like other resources, a transformed geometry inherits the resource space and threading policy of the factory that created it.</span></span> <span data-ttu-id="a1204-115">此物件是不可變的。</span><span class="sxs-lookup"><span data-stu-id="a1204-115">This object is immutable.</span></span>

<span data-ttu-id="a1204-116">使用 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 方法對轉換幾何進行筆劃時，筆劃寬度不會受到套用至幾何的轉換影響。</span><span class="sxs-lookup"><span data-stu-id="a1204-116">When stroking a transformed geometry with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method, the stroke width is not affected by the transform applied to the geometry.</span></span> <span data-ttu-id="a1204-117">筆劃寬度只會受到世界轉換的影響。</span><span class="sxs-lookup"><span data-stu-id="a1204-117">The stroke width is only affected by the world transform.</span></span>

## <a name="examples"></a><span data-ttu-id="a1204-118">範例</span><span class="sxs-lookup"><span data-stu-id="a1204-118">Examples</span></span>

<span data-ttu-id="a1204-119">下列範例會建立 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))，然後在不轉換的情況下繪製。</span><span class="sxs-lookup"><span data-stu-id="a1204-119">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), then draws it without transforming it.</span></span> <span data-ttu-id="a1204-120">它會產生下圖中顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="a1204-120">It produces the output shown in the following illustration.</span></span>

![矩形的圖例](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



<span data-ttu-id="a1204-122">下一個範例會使用轉譯目標，將幾何調整為3的因數，然後繪製。</span><span class="sxs-lookup"><span data-stu-id="a1204-122">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="a1204-123">下圖顯示在沒有轉換和轉換的情況下繪製矩形的結果;請注意，即使筆觸粗細為1，筆劃在轉換後會變粗。</span><span class="sxs-lookup"><span data-stu-id="a1204-123">The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![具有較粗筆觸的大型矩形內較小矩形的圖例](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="a1204-125">下一個範例會使用 **CreateTransformedGeometry** 方法，將幾何調整為3的因數，然後繪製它。</span><span class="sxs-lookup"><span data-stu-id="a1204-125">The next example uses the **CreateTransformedGeometry** method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="a1204-126">它會產生下圖中顯示的輸出。</span><span class="sxs-lookup"><span data-stu-id="a1204-126">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="a1204-127">請注意，雖然矩形更大，但其筆觸尚未增加。</span><span class="sxs-lookup"><span data-stu-id="a1204-127">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![具有相同筆劃的大型矩形內較小矩形的圖例](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a><span data-ttu-id="a1204-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1204-129">Requirements</span></span>



| <span data-ttu-id="a1204-130">需求</span><span class="sxs-lookup"><span data-stu-id="a1204-130">Requirement</span></span> | <span data-ttu-id="a1204-131">值</span><span class="sxs-lookup"><span data-stu-id="a1204-131">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a1204-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a1204-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a1204-133"><dt>D2d1。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1204-133"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1204-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1204-134">Library</span></span><br/> | <dl> <span data-ttu-id="a1204-135"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1204-135"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="a1204-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a1204-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1204-137"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1204-137"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1204-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1204-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1204-139">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="a1204-139">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
