---
title: D1110 排清失敗
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: 呈現目標的 Flush 呼叫失敗
keywords:
- D1110 排清失敗 Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4821ba291f3adc8d22d1d1298a88c74b47dc648b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382805"
---
# <a name="d1110-flush-failure"></a><span data-ttu-id="03a7a-104">D1110： Flush 失敗</span><span class="sxs-lookup"><span data-stu-id="03a7a-104">D1110: Flush Failure</span></span>

<span data-ttu-id="03a7a-105">轉譯目標失敗資源的 Flush 呼叫 \[  \] 。</span><span class="sxs-lookup"><span data-stu-id="03a7a-105">A Flush call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="03a7a-106">標記 \[ *tag1*、 *tag2* \] 。</span><span class="sxs-lookup"><span data-stu-id="03a7a-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="03a7a-107">預留位置</span><span class="sxs-lookup"><span data-stu-id="03a7a-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="03a7a-108"><span id="resource"></span><span id="RESOURCE"></span>*資源*</span><span class="sxs-lookup"><span data-stu-id="03a7a-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="03a7a-109">呈現目標的位址。</span><span class="sxs-lookup"><span data-stu-id="03a7a-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="03a7a-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span><span class="sxs-lookup"><span data-stu-id="03a7a-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="03a7a-111">第一個標記值。</span><span class="sxs-lookup"><span data-stu-id="03a7a-111">The first tag value.</span></span> <span data-ttu-id="03a7a-112">如需詳細資訊，請參閱 [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) 。</span><span class="sxs-lookup"><span data-stu-id="03a7a-112">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="03a7a-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="03a7a-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="03a7a-114">第二個標記值。</span><span class="sxs-lookup"><span data-stu-id="03a7a-114">The second tag value.</span></span> <span data-ttu-id="03a7a-115">如需詳細資訊，請參閱 [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) 。</span><span class="sxs-lookup"><span data-stu-id="03a7a-115">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="03a7a-116">錯誤層級</span><span class="sxs-lookup"><span data-stu-id="03a7a-116">Error Level</span></span> | <span data-ttu-id="03a7a-117">警告</span><span class="sxs-lookup"><span data-stu-id="03a7a-117">Warning</span></span> |



 

## <a name="examples"></a><span data-ttu-id="03a7a-118">範例</span><span class="sxs-lookup"><span data-stu-id="03a7a-118">Examples</span></span>

<span data-ttu-id="03a7a-119">**範例1：** 下列程式碼顯示繪製呼叫處於無效狀態。</span><span class="sxs-lookup"><span data-stu-id="03a7a-119">**Example 1:** The following code shows that a draw call is in an invalid state.</span></span> <span data-ttu-id="03a7a-120">若要避免出現警告訊息，請使用 [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) \_ \_ \_ 在 [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 呼叫之前設定 D2D1 消除鋸齒模式反鋸齒。</span><span class="sxs-lookup"><span data-stu-id="03a7a-120">To avoid the warning message, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set D2D1\_ANTIALIAS\_MODE\_ANTIALIASED before a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) call.</span></span>


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





<span data-ttu-id="03a7a-121">此範例會產生下列 debug 訊息：</span><span class="sxs-lookup"><span data-stu-id="03a7a-121">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

<span data-ttu-id="03a7a-122">**範例2：** 下列程式碼顯示在 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)呼叫之後呼叫 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 。</span><span class="sxs-lookup"><span data-stu-id="03a7a-122">**Example 2:** The following code shows that the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called after the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call.</span></span>


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



<span data-ttu-id="03a7a-123">此範例會產生下列 debug 訊息：</span><span class="sxs-lookup"><span data-stu-id="03a7a-123">This example produces the following debug message:</span></span>

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a><span data-ttu-id="03a7a-124">可能的原因</span><span class="sxs-lookup"><span data-stu-id="03a7a-124">Possible Causes</span></span>

<span data-ttu-id="03a7a-125">因為有兩個原因，所以 [**清除**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 呼叫可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="03a7a-125">The [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call can fail for one of two reasons.</span></span> <span data-ttu-id="03a7a-126">它可能會因為在 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)呼叫之外呼叫方法而失敗，否則可能會失敗，因為其中一個轉譯目標作業產生的錯誤，自從上次排清呼叫或 **EndDraw** 呼叫之後已經處理過。</span><span class="sxs-lookup"><span data-stu-id="03a7a-126">It may fail because the method was called outside of the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)/[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call, or it may fail because there was an error produced by one of the render target operations that have been processed since the last **Flush** call or **EndDraw** call.</span></span> <span data-ttu-id="03a7a-127">若要修正此問題，應用程式應判斷錯誤的原因，並採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="03a7a-127">To fix the issue, the application should determine the cause of the error and take the appropriate action.</span></span>

## <a name="fixes"></a><span data-ttu-id="03a7a-128">修正</span><span class="sxs-lookup"><span data-stu-id="03a7a-128">Fixes</span></span>

<span data-ttu-id="03a7a-129">[**清除**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)呼叫可能會失敗的原因有很多。</span><span class="sxs-lookup"><span data-stu-id="03a7a-129">There are many reasons that a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call might fail.</span></span> <span data-ttu-id="03a7a-130">應用程式應該判斷錯誤的原因，並採取適當的動作。</span><span class="sxs-lookup"><span data-stu-id="03a7a-130">The application should determine the cause of the error and take the appropriate action.</span></span>

 

 