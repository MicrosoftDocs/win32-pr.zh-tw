---
title: 如何使用 Axis-Aligned 剪切矩形裁剪
description: 顯示如何使用軸對齊的剪輯矩形來裁剪區域。
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104553898"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a><span data-ttu-id="c43c0-103">如何使用 Axis-Aligned 剪切矩形裁剪</span><span class="sxs-lookup"><span data-stu-id="c43c0-103">How to Clip with an Axis-Aligned Clip Rectangle</span></span>

<span data-ttu-id="c43c0-104">本主題說明如何使用軸對齊的剪輯矩形來裁剪影像。</span><span class="sxs-lookup"><span data-stu-id="c43c0-104">This topic describes how to clip an image with an axis-aligned clip rectangle.</span></span> <span data-ttu-id="c43c0-105">這種方法只會產生矩形剪輯，因為內容界限會對齊矩形的座標軸。</span><span class="sxs-lookup"><span data-stu-id="c43c0-105">This approach produces only rectangular clips, because the content bounds are aligned to the axis of the rectangle.</span></span> <span data-ttu-id="c43c0-106">這種方法比使用具有內容界限的圖層更有效率。</span><span class="sxs-lookup"><span data-stu-id="c43c0-106">This approach is more efficient than using layers with the content bounds.</span></span> <span data-ttu-id="c43c0-107">如需詳細資訊，請參閱[圖層總覽](direct2d-layers-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c43c0-107">For more information, see[Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="c43c0-108">**若要使用軸對齊的剪輯矩形進行裁剪**</span><span class="sxs-lookup"><span data-stu-id="c43c0-108">**To clip with an axis-aligned clip rectangle**</span></span>

1.  <span data-ttu-id="c43c0-109">從資源載入原始映射。</span><span class="sxs-lookup"><span data-stu-id="c43c0-109">Load the original image from a resource.</span></span> <span data-ttu-id="c43c0-110">如需有關如何載入點陣圖的詳細資訊，請參閱 [如何從資源載入點陣圖](how-to-load-a-bitmap-from-a-resource.md)。</span><span class="sxs-lookup"><span data-stu-id="c43c0-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="c43c0-111">呼叫 [**ID2D1RenderTarget：:P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 來指定矩形。</span><span class="sxs-lookup"><span data-stu-id="c43c0-111">Call [**ID2D1RenderTarget::PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) to specify a rectangle.</span></span> <span data-ttu-id="c43c0-112">轉譯命令會裁剪至矩形。</span><span class="sxs-lookup"><span data-stu-id="c43c0-112">The rendering commands are clipped to the rectangle.</span></span>

3.  <span data-ttu-id="c43c0-113">繪製原始影像。</span><span class="sxs-lookup"><span data-stu-id="c43c0-113">Paint the original image.</span></span>
4.  <span data-ttu-id="c43c0-114">呼叫 [**ID2D1RenderTarget：:P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) ，從轉譯目標中移除最後一個軸對齊的剪輯。</span><span class="sxs-lookup"><span data-stu-id="c43c0-114">Call [**ID2D1RenderTarget::PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the last axis-aligned clip from the render target.</span></span>

<span data-ttu-id="c43c0-115">例如，在下圖中，左邊的原始點陣圖是 200 \* 130 圖元。</span><span class="sxs-lookup"><span data-stu-id="c43c0-115">For example, in the following illustration, the original bitmap on the left is 200\*130 pixels.</span></span> <span data-ttu-id="c43c0-116">右邊的點陣圖是裁剪成軸對齊剪切矩形的原始點陣圖。</span><span class="sxs-lookup"><span data-stu-id="c43c0-116">The bitmap on the right is the original bitmap clipped to the axis-aligned clip rectangle.</span></span> <span data-ttu-id="c43c0-117">維度 (20，20) 至 (100，100) 。</span><span class="sxs-lookup"><span data-stu-id="c43c0-117">The dimensions are (20, 20) to (100, 100).</span></span>

![裁剪點陣圖前後的金魚點陣圖圖例](images/cliparegion-axisalignedclip.png)

<span data-ttu-id="c43c0-119">若要建立裁剪的影像，請建立矩形結構作為裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="c43c0-119">To create the clipped image, create a rectangle structure as the clipping area.</span></span> <span data-ttu-id="c43c0-120">使用裁剪區域來呼叫 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) ，並繪製原始影像。</span><span class="sxs-lookup"><span data-stu-id="c43c0-120">Call [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) with the clipping area and paint the original image.</span></span> <span data-ttu-id="c43c0-121">呼叫 [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) 以從轉譯目標中移除剪輯。</span><span class="sxs-lookup"><span data-stu-id="c43c0-121">Call [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the clip from the render target.</span></span> <span data-ttu-id="c43c0-122">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="c43c0-122">The following code shows how to do this.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a><span data-ttu-id="c43c0-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="c43c0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c43c0-124">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="c43c0-124">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 