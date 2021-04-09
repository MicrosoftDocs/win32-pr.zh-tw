---
title: 如何使用點陣圖作為不透明度遮罩
description: 顯示如何使用點陣圖遮罩來裁剪區域。
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933483"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a><span data-ttu-id="5d3e3-103">如何使用點陣圖作為不透明度遮罩</span><span class="sxs-lookup"><span data-stu-id="5d3e3-103">How to Use a Bitmap as an Opacity Mask</span></span>

<span data-ttu-id="5d3e3-104">本主題描述如何藉由呼叫 [**ID2D1Factory：： FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) 方法，使用點陣圖作為 opacty mask。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-104">This topic describes how to use a bitmap as an opacty mask by calling the [**ID2D1Factory::FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) method.</span></span> <span data-ttu-id="5d3e3-105">不透明度遮罩是一種點陣圖，可提供由 Alpha 色板表示的涵蓋範圍資訊，以控制所呈現內容的透明度。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-105">The opacity mask is a bitmap that supplies the coverage information that is represented by the alpha channel, which controls the transparency of the content that is rendered.</span></span> <span data-ttu-id="5d3e3-106">這種方法比使用具有不透明度遮罩的圖層更有效率。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-106">This approach is more efficient than using layers with an opacity mask.</span></span> <span data-ttu-id="5d3e3-107">如需詳細資訊，請參閱 [圖層總覽](direct2d-layers-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-107">For more information, see [Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="5d3e3-108">**若要裁剪區域**</span><span class="sxs-lookup"><span data-stu-id="5d3e3-108">**To clip a region**</span></span>

1.  <span data-ttu-id="5d3e3-109">從資源載入原始點陣圖。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-109">Load the original bitmap from a resource.</span></span> <span data-ttu-id="5d3e3-110">如需有關如何載入點陣圖的詳細資訊，請參閱 [如何從資源載入點陣圖](how-to-load-a-bitmap-from-a-resource.md)。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="5d3e3-111">從資源載入點陣圖遮罩。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-111">Load the bitmap mask from a resource.</span></span>
3.  <span data-ttu-id="5d3e3-112">使用原始點陣圖建立點陣圖筆刷。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-112">Create a bitmap brush with the original bitmap.</span></span> <span data-ttu-id="5d3e3-113">如需有關如何建立點陣圖筆刷的詳細資訊，請參閱 [如何建立點陣圖筆刷](how-to-create-a-bitmap-brush.md)。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-113">For information on how to create a bitmap brush, see [How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).</span></span>
4.  <span data-ttu-id="5d3e3-114">呼叫 [**ID2D1Factory：： SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) 可在轉譯目標上設定消除鋸齒模式，以 D2D1 \_ \_ \_ 別名為 [**ID2D1Factory：： FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 的鋸齒消除鋸齒模式運作。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-114">Call [**ID2D1Factory::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set antialias mode on the render target to D2D1\_ANTIALIAS\_MODE\_ALIASED for [**ID2D1Factory::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) to work.</span></span>
5.  <span data-ttu-id="5d3e3-115">使用點陣圖遮罩和轉譯目標上的點陣圖筆刷來呼叫 [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) ，以填滿剪輯。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-115">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) with the bitmap mask and the bitmap brush on the render target to fill the clip.</span></span>

<span data-ttu-id="5d3e3-116">下圖顯示左邊的原始點陣圖、中間的點陣圖遮罩，以及裁剪到右邊遮罩的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-116">The following illustration shows the original bitmap on the left, the bitmap mask in the center, and the bitmap clipped to the mask on the right.</span></span>

![金魚點陣圖、從點陣圖建立的魚狀遮罩，以及遮罩後產生的魚形點陣圖的圖例](images/cliparegion-opacitymask.png)

<span data-ttu-id="5d3e3-118">下列程式碼示範如何使用上圖所示的遮罩來裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-118">The following code shows how to clip the region with the mask shown in the preceding illustration.</span></span> <span data-ttu-id="5d3e3-119">它會先載入原始點陣圖和點陣圖遮罩。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-119">It first loads the original bitmap and the bitmap mask.</span></span> <span data-ttu-id="5d3e3-120">然後使用原始點陣圖建立點陣圖筆刷。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-120">And then creates a bitmap brush with the original bitmap.</span></span>


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



<span data-ttu-id="5d3e3-121">然後，它會呼叫 [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) 來設定消除鋸齒模式。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-121">It then calls [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set the antialias mode.</span></span> <span data-ttu-id="5d3e3-122">呼叫 [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) ，以使用點陣圖遮罩來裁剪原始點陣圖。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-122">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) to use a bitmap mask to clip the original bitmap.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="5d3e3-123">如需不透明度遮罩的詳細資訊，請參閱 [不透明度遮罩總覽](opacity-masks-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="5d3e3-123">For more information about opacity masks, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d3e3-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d3e3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d3e3-125">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="5d3e3-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 