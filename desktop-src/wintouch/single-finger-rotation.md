---
title: Single-Finger 旋轉
description: 本節說明如何使用 pivot 點來旋轉物件。
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Touch，旋轉
- Windows Touch，操作
- Windows Touch，單指旋轉
- Windows Touch，資料透視點旋轉
- 操作，旋轉
- 旋轉，pivot 點
- 旋轉，單指
- 手勢，單指旋轉
- 單一手指旋轉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d74263f502749e2aaf942c4bbec5aa0a284e76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839623"
---
# <a name="single-finger-rotation"></a><span data-ttu-id="5272f-112">Single-Finger 旋轉</span><span class="sxs-lookup"><span data-stu-id="5272f-112">Single-Finger Rotation</span></span>

<span data-ttu-id="5272f-113">本節說明如何使用 pivot 點來旋轉物件。</span><span class="sxs-lookup"><span data-stu-id="5272f-113">This section explains how to rotate an object using a pivot point.</span></span>

<span data-ttu-id="5272f-114">下圖說明單一手指旋轉。</span><span class="sxs-lookup"><span data-stu-id="5272f-114">The following image illustrates single-finger rotation.</span></span>

![顯示兩種類型的單一手指旋轉的圖例：圍繞中心或邊緣的周圍](images/sfrotation.png)

<span data-ttu-id="5272f-116">在範例 A 中，會使用旋轉手勢來旋轉物件中心點周圍的物件。</span><span class="sxs-lookup"><span data-stu-id="5272f-116">In example A, the object is rotated around the center point of the object by using the rotation gesture.</span></span> <span data-ttu-id="5272f-117">在 B 範例中，物件的旋轉方式是在物件的邊緣周圍移動單一手指。</span><span class="sxs-lookup"><span data-stu-id="5272f-117">In example B, the object is rotated by moving a single finger around the edge of the object.</span></span> <span data-ttu-id="5272f-118">操作處理器會使用資料透視點和 pivot 半徑值來啟用這項旋轉。</span><span class="sxs-lookup"><span data-stu-id="5272f-118">The manipulation processor enables this rotation by using pivot point and pivot radius values.</span></span> <span data-ttu-id="5272f-119">下圖說明單一手指旋轉的元件。</span><span class="sxs-lookup"><span data-stu-id="5272f-119">The following image illustrates the components of single-finger rotation.</span></span>

![圖例顯示單一手指旋轉的元件： pivotpointx、pivotpointy 和 pivotradius](images/sfrotation-components.png)

<span data-ttu-id="5272f-121">設定 [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)、 [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)和 [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) 值之後，後續的轉譯訊息將會納入旋轉。</span><span class="sxs-lookup"><span data-stu-id="5272f-121">After you set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy), and [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) values, subsequent translation messages will incorporate rotation.</span></span> <span data-ttu-id="5272f-122">Pivot 半徑越大，x 和 y 的變更就必須等於旋轉物件。</span><span class="sxs-lookup"><span data-stu-id="5272f-122">The larger the pivot radius, the greater the change in x and y must be to rotate the object.</span></span> <span data-ttu-id="5272f-123">下列程式碼顯示如何在操作處理器中設定這些值。</span><span class="sxs-lookup"><span data-stu-id="5272f-123">The following code shows how these values could be set in the manipulation processor.</span></span>


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



<span data-ttu-id="5272f-124">在上述範例中，物件的邊緣距離 (調整為 40%) 用來作為 pivot 半徑。</span><span class="sxs-lookup"><span data-stu-id="5272f-124">In the previous example, the distance to the edge of the object (scaled to 40 percent) is used as the pivot radius.</span></span> <span data-ttu-id="5272f-125">因為物件大小會納入考慮，所以此計算對每個物件差異都有效。</span><span class="sxs-lookup"><span data-stu-id="5272f-125">Because the object size is taken into consideration, this calculation is valid for every object delta.</span></span> <span data-ttu-id="5272f-126">當物件進行調整時，pivot 半徑會成長。</span><span class="sxs-lookup"><span data-stu-id="5272f-126">As the object scales, the pivot radius grows.</span></span> <span data-ttu-id="5272f-127">此值和物件的中心 x 和 y 值會傳遞給操作處理器，以在資料透視點周圍旋轉物件。</span><span class="sxs-lookup"><span data-stu-id="5272f-127">This value and the object's center x and y values are passed to the manipulation processor to rotate the object around the pivot point.</span></span>

> [!Note]  
> <span data-ttu-id="5272f-128">[**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)值絕不能介於0.0 到1.0 之間。</span><span class="sxs-lookup"><span data-stu-id="5272f-128">The [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) value should never be between 0.0 and 1.0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5272f-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="5272f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5272f-130">操作</span><span class="sxs-lookup"><span data-stu-id="5272f-130">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> <dt>

[<span data-ttu-id="5272f-131">**PivotRadius**</span><span class="sxs-lookup"><span data-stu-id="5272f-131">**PivotRadius**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[<span data-ttu-id="5272f-132">**PivotPointX**</span><span class="sxs-lookup"><span data-stu-id="5272f-132">**PivotPointX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[<span data-ttu-id="5272f-133">**PivotPointY**</span><span class="sxs-lookup"><span data-stu-id="5272f-133">**PivotPointY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




