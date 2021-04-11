---
title: 相容的 A8 轉譯目標總覽
description: 描述相容 A8 轉譯目標的基本概念，並提供示範如何使用它們的範例。
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "103933779"
---
# <a name="compatible-a8-render-targets-overview"></a><span data-ttu-id="19530-103">相容的 A8 轉譯目標總覽</span><span class="sxs-lookup"><span data-stu-id="19530-103">Compatible A8 render targets overview</span></span>

<span data-ttu-id="19530-104">本主題說明相容 A8 轉譯目標的基本概念，並提供如何使用它的範例。</span><span class="sxs-lookup"><span data-stu-id="19530-104">This topic describes the basics of a compatible A8 render target, and provides examples of how to use it.</span></span>

<span data-ttu-id="19530-105">相容的 A8 轉譯目標是相容的轉譯目標 ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) ，其使用 a8 像素格式 (DXGI \_ 格式 \_ A8 \_ UNORM) 。</span><span class="sxs-lookup"><span data-stu-id="19530-105">A compatible A8 render target is a compatible render target ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) that uses an A8 pixel format (DXGI\_FORMAT\_A8\_UNORM).</span></span> <span data-ttu-id="19530-106">您可以使用相容的 A8 轉譯目標來改善應用程式的效能，並在文字動畫期間提供更平滑的轉換。</span><span class="sxs-lookup"><span data-stu-id="19530-106">You can use a compatible A8 render target to improve the application's performance and provide smoother transitions during text animation.</span></span> <span data-ttu-id="19530-107">當您嘗試改善下列各項時，相容的 A8 轉譯目標特別有用：</span><span class="sxs-lookup"><span data-stu-id="19530-107">A compatible A8 render target is particular useful when you try to improve the following:</span></span>

-   <span data-ttu-id="19530-108">轉譯文字或消除鋸齒型幾何的應用程式畫面播放速率，其中只包含簡單的動畫，例如平移、旋轉、縮放或色彩變更。</span><span class="sxs-lookup"><span data-stu-id="19530-108">The frame rate of the application that renders text or anti-aliased geometry that includes only simple animations, such as translation, rotation, scale, or color changes.</span></span>

-   <span data-ttu-id="19530-109">應用程式的視覺化持續性，可在動畫期間伸展和 diminshes 文字。</span><span class="sxs-lookup"><span data-stu-id="19530-109">The visual continuity of the application that stretches and diminshes text during an animation.</span></span>

<span data-ttu-id="19530-110">若要建立相容的 A8 轉譯目標，請使用 [**ID2D1RenderTarget：： CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) 方法搭配 DXGI \_ 格式 \_ A8 \_ UNORM 像素格式，然後指定傳回的相容轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="19530-110">To create a compatible A8 render target, use the [**ID2D1RenderTarget::CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) method together with the DXGI\_FORMAT\_A8\_UNORM pixel format, and specify a returned compatible render target.</span></span> <span data-ttu-id="19530-111">如需像素格式的詳細資訊，請參閱 [支援的像素格式和 Alpha 模式](./supported-pixel-formats-and-alpha-modes.md)。</span><span class="sxs-lookup"><span data-stu-id="19530-111">For more information about pixel formats, see [Supported pixel formats and alpha modes](./supported-pixel-formats-and-alpha-modes.md).</span></span>

<span data-ttu-id="19530-112">例如，若要有效率地以動畫顯示下列螢幕擷取畫面中顯示的文字，請使用相容的 A8 轉譯目標，將文字快取為不透明度遮罩。</span><span class="sxs-lookup"><span data-stu-id="19530-112">For example, to efficiently animate the text that is shown in the following screen shot, use a compatible A8 render target to cache the text as an opacity mask.</span></span> <span data-ttu-id="19530-113">然後，將轉換套用至不透明度遮罩，以達成快速轉譯結果。</span><span class="sxs-lookup"><span data-stu-id="19530-113">Then, apply transformations to the opacity mask to achieve fast rendering results.</span></span>

![要建立動畫之文字的螢幕擷取畫面](images/a8rendertarget.png)

<span data-ttu-id="19530-115">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="19530-115">The following code shows how to do this.</span></span> <span data-ttu-id="19530-116">它會建立相容的 A8 轉譯目標、從中抓取點陣圖，然後使用 [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md)呈現點陣圖。</span><span class="sxs-lookup"><span data-stu-id="19530-116">It creates a compatible A8 render target, retrieves the bitmap from it, and then renders the bitmap by using [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).</span></span>

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a><span data-ttu-id="19530-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="19530-117">Related topics</span></span>

[<span data-ttu-id="19530-118">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="19530-118">Direct2D Reference</span></span>](reference.md)