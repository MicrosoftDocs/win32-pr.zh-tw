---
title: 支援的像素格式和 Alpha 模式
description: 描述每個呈現目標型別所支援的像素格式和 Alpha 模式。
ms.assetid: 09b1f9c6-1780-4733-ac22-9e8c21466b67
keywords:
- Direct2D，像素格式
- Direct2D，Alpha 模式
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9a3777cac7cc0a258002d1475fb7b1c6dd2546ca
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104093495"
---
# <a name="supported-pixel-formats-and-alpha-modes"></a><span data-ttu-id="7a7ea-105">支援的像素格式和 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-105">Supported Pixel Formats and Alpha Modes</span></span>

<span data-ttu-id="7a7ea-106">本主題說明 Direct2D 各個部分所支援的像素格式和 Alpha 模式，包括每個轉譯目標型別、 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)和 [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-106">This topic describes the pixel formats and alpha modes supported by the various parts of Direct2D, including each render target type, the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap), and [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource).</span></span> <span data-ttu-id="7a7ea-107">包含以下幾節。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-107">It contains the following sections.</span></span>

-   [<span data-ttu-id="7a7ea-108">針對 DXGI 映射來源支援的 YUV 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-108">Supported YUV Formats for DXGI Image Source</span></span>](#supported-yuv-formats-for-dxgi-image-source)
-   [<span data-ttu-id="7a7ea-109">指定呈現目標的像素格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-109">Specifying a Pixel Format for a Render Target</span></span>](#specifying-a-pixel-format-for-a-render-target)
-   [<span data-ttu-id="7a7ea-110">支援的 ID2D1HwndRenderTarget 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-110">Supported Formats for ID2D1HwndRenderTarget</span></span>](#supported-formats-for-id2d1hwndrendertarget)
-   [<span data-ttu-id="7a7ea-111">支援的 ID2D1DeviceCoNtext 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-111">Supported formats for ID2D1DeviceContext</span></span>](#supported-formats-for-id2d1devicecontext)
-   [<span data-ttu-id="7a7ea-112">相容轉譯目標支援的格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-112">Supported Formats for Compatible Render Target</span></span>](#supported-formats-for-compatible-render-target)
-   [<span data-ttu-id="7a7ea-113">適用于 DXGI 介面轉譯目標的支援格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-113">Supported Formats for DXGI Surface Render Target</span></span>](#supported-formats-for-dxgi-surface-render-target)
-   [<span data-ttu-id="7a7ea-114">WIC 點陣圖轉譯目標支援的格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-114">Supported Formats for WIC Bitmap Render Target</span></span>](#supported-formats-for-wic-bitmap-render-target)
-   [<span data-ttu-id="7a7ea-115">支援的 ID2D1DCRenderTarget 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-115">Supported Formats for ID2D1DCRenderTarget</span></span>](#supported-formats-for-id2d1dcrendertarget)
-   [<span data-ttu-id="7a7ea-116">為 ID2D1Bitmap 指定像素格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-116">Specifying a Pixel Format for an ID2D1Bitmap</span></span>](#specifying-a-pixel-format-for-an-id2d1bitmap)
    -   [<span data-ttu-id="7a7ea-117">支援的 WIC 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-117">Supported WIC Formats</span></span>](#supported-wic-formats)
-   [<span data-ttu-id="7a7ea-118">使用不支援的格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-118">Using an Unsupported Format</span></span>](#using-an-unsupported-format)
-   [<span data-ttu-id="7a7ea-119">關於 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-119">About Alpha Modes</span></span>](#about-alpha-modes)
    -   [<span data-ttu-id="7a7ea-120">關於預乘和直接 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-120">About Premultiplied and Straight Alpha Modes</span></span>](#about-premultiplied-and-straight-alpha-modes)
    -   [<span data-ttu-id="7a7ea-121">直線和預乘 Alpha 之間的差異</span><span class="sxs-lookup"><span data-stu-id="7a7ea-121">The Differences Between Straight and Premultiplied Alpha</span></span>](#the-differences-between-straight-and-premultiplied-alpha)
    -   [<span data-ttu-id="7a7ea-122">呈現目標的 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-122">Alpha Mode for Render Targets</span></span>](#alpha-mode-for-render-targets)
    -   [<span data-ttu-id="7a7ea-123">ClearType 和 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-123">ClearType and Alpha Modes</span></span>](#cleartype-and-alpha-modes)
-   [<span data-ttu-id="7a7ea-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a7ea-124">Related topics</span></span>](#related-topics)

## <a name="supported-yuv-formats-for-dxgi-image-source"></a><span data-ttu-id="7a7ea-125">針對 DXGI 映射來源支援的 YUV 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-125">Supported YUV Formats for DXGI Image Source</span></span>

<span data-ttu-id="7a7ea-126">[**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)是一種抽象的圖元提供者。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-126">An [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) is an abstracted provider of pixels.</span></span> <span data-ttu-id="7a7ea-127">它可以從 WIC ([**CreateImageSourceFromWic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) 或 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)) 來具現化。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-127">It can be instantiated from either WIC ([**CreateImageSourceFromWic**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic)) or an [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ([**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi)).</span></span>

<span data-ttu-id="7a7ea-128">[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) 支援與 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)相同的一組像素格式和 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-128">[**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) supports the same set of pixel formats and alpha modes as [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

<span data-ttu-id="7a7ea-129">除了上述以外，從 [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)具現化的 [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)也支援一些 YUV 像素格式，包括將平面資料分割成多個表面。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-129">In addition to the above, an [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) that is instantiated from [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) also supports some YUV pixel formats, including planar data split into multiple surfaces.</span></span> <span data-ttu-id="7a7ea-130">如需每個像素格式需求的詳細資訊，請參閱 [**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi) 。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-130">See [**CreateImageSourceFromDxgi**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromdxgi) for more information about requirements for each pixel format.</span></span>



| <span data-ttu-id="7a7ea-131">格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-131">Format</span></span>                    |
|---------------------------|
| <span data-ttu-id="7a7ea-132">DXGI \_ 格式 \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="7a7ea-132">DXGI\_FORMAT\_AYUV</span></span>        |
| <span data-ttu-id="7a7ea-133">DXGI \_ 格式 \_ NV12</span><span class="sxs-lookup"><span data-stu-id="7a7ea-133">DXGI\_FORMAT\_NV12</span></span>        |
| <span data-ttu-id="7a7ea-134">DXGI \_ 格式 \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="7a7ea-134">DXGI\_FORMAT\_YUY2</span></span>        |
| <span data-ttu-id="7a7ea-135">DXGI \_ 格式 \_ P208</span><span class="sxs-lookup"><span data-stu-id="7a7ea-135">DXGI\_FORMAT\_P208</span></span>        |
| <span data-ttu-id="7a7ea-136">DXGI \_ 格式 \_ V208</span><span class="sxs-lookup"><span data-stu-id="7a7ea-136">DXGI\_FORMAT\_V208</span></span>        |
| <span data-ttu-id="7a7ea-137">DXGI \_ 格式 \_ V408</span><span class="sxs-lookup"><span data-stu-id="7a7ea-137">DXGI\_FORMAT\_V408</span></span>        |
| <span data-ttu-id="7a7ea-138">DXGI \_ 格式 \_ R8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-138">DXGI\_FORMAT\_R8\_UNORM</span></span>   |
| <span data-ttu-id="7a7ea-139">DXGI \_ 格式 \_ R8G8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-139">DXGI\_FORMAT\_R8G8\_UNORM</span></span> |



 

## <a name="specifying-a-pixel-format-for-a-render-target"></a><span data-ttu-id="7a7ea-140">指定呈現目標的像素格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-140">Specifying a Pixel Format for a Render Target</span></span>

<span data-ttu-id="7a7ea-141">當您建立轉譯目標時，您必須指定它的像素格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-141">When you create a render target, you must specify its pixel format.</span></span> <span data-ttu-id="7a7ea-142">若要指定像素格式，您可以使用 [**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)結構來設定 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)結構的 **pixelFormat** 成員。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-142">To specify the pixel format, you use a [**D2D1\_PIXEL\_FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) structure to set the **pixelFormat** member of a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure.</span></span> <span data-ttu-id="7a7ea-143">然後，將該結構傳遞至適當的 Create 方法，例如 [**ID2D1Factory：： CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-143">Then, you pass that structure to the appropriate Create method, such as [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span></span>

<span data-ttu-id="7a7ea-144">[**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)結構有兩個欄位：</span><span class="sxs-lookup"><span data-stu-id="7a7ea-144">The [**D2D1\_PIXEL\_FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) structure has two fields:</span></span>

-   <span data-ttu-id="7a7ea-145">**format**（ [DXGI \_ 格式](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 值），描述每個圖元中通道的大小和相片順序，以及</span><span class="sxs-lookup"><span data-stu-id="7a7ea-145">**format**, a [DXGI\_FORMAT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) value that describes the size and arrangement of channels in each pixel, and</span></span>
-   <span data-ttu-id="7a7ea-146">**Alpha**， [**D2D1 \_ Alpha \_ 模式**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 值，描述如何解讀 Alpha 資訊。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-146">**alpha**, a [**D2D1\_ALPHA\_MODE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) value that describes how alpha information is interpreted.</span></span>

<span data-ttu-id="7a7ea-147">下列範例會建立 [**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) 結構，並用它來指定 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)的像素格式和 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-147">The following example creates a [**D2D1\_PIXEL\_FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) structure and uses it to specify the pixel format and alpha mode of an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a pixel format and initial its format
// and alphaMode fields.
D2D1_PIXEL_FORMAT pixelFormat = D2D1::PixelFormat(
    DXGI_FORMAT_B8G8R8A8_UNORM,
    D2D1_ALPHA_MODE_IGNORE
    );

D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties();
props.pixelFormat = pixelFormat;

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    props,
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRT
    );

```



<span data-ttu-id="7a7ea-148">不同的呈現目標支援不同的格式和 Alpha 模式組合。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-148">Different render targets support different format and alpha mode combinations.</span></span> <span data-ttu-id="7a7ea-149">下列各節列出每個呈現目標所支援的格式和 Alpha 組合。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-149">The following sections list the format and alpha combinations supported by each render target.</span></span>

## <a name="supported-formats-for-id2d1hwndrendertarget"></a><span data-ttu-id="7a7ea-150">支援的 ID2D1HwndRenderTarget 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-150">Supported Formats for ID2D1HwndRenderTarget</span></span>

<span data-ttu-id="7a7ea-151">[**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)支援的格式取決於它是使用硬體或軟體所呈現，還是 Direct2D 預設會自動處理轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-151">The supported formats for an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) depend on whether it renders by using hardware or software, or whether Direct2D handles the rendering mode automatically by default.</span></span>

> [!Note]  
> <span data-ttu-id="7a7ea-152">建議您使用 [**DXGI \_ format \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) 做為像素格式，以獲得更好的效能。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-152">We recommend that you use [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) as the pixel format for better performance.</span></span> <span data-ttu-id="7a7ea-153">這對軟體呈現目標特別有用。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-153">This is particularly helpful for software render targets.</span></span> <span data-ttu-id="7a7ea-154">BGRA 格式目標的執行效果優於 RGBA 格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-154">BGRA format targets perform better than RGBA formats.</span></span>

 

<span data-ttu-id="7a7ea-155">當您建立 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)時，您可以使用 [**D2D1 \_ 轉譯 \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) 結構來指定轉譯選項。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-155">When you create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), you use the [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure to specify rendering options.</span></span> <span data-ttu-id="7a7ea-156">選項包括像素格式，如上一節所述。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-156">The options include the pixel format, as noted in the previous section.</span></span> <span data-ttu-id="7a7ea-157">此結構的 [類型] 欄位可讓您指定轉譯目標是要呈現給硬體或軟體，還是 Direct2D 應該自動判斷轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-157">The type field of this structure enables you to specify whether the render target renders to hardware or software, or whether Direct2D should automatically determine the rendering mode.</span></span>

<span data-ttu-id="7a7ea-158">若要啟用 Direct2D 以判斷轉譯目標是使用硬體或軟體轉譯，請使用 [**D2D1 \_ 轉譯 \_ 目標 \_ 類型 \_ 預設**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 設定。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-158">To enable Direct2D to determine whether the render target uses hardware or software rendering, use the [**D2D1\_RENDER\_TARGET\_TYPE\_DEFAULT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) setting.</span></span>

<span data-ttu-id="7a7ea-159">下表列出使用 [ [**D2D1 轉譯 \_ \_ 目標 \_ 類型] \_ 預設**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)設定所建立之 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)物件的支援格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-159">The following table lists the supported formats for [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects that are created by using the [**D2D1\_RENDER\_TARGET\_TYPE\_DEFAULT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) setting.</span></span>



| <span data-ttu-id="7a7ea-160">格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-160">Format</span></span>                        | <span data-ttu-id="7a7ea-161">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-161">Alpha mode</span></span>                       |
|-------------------------------|----------------------------------|
| <span data-ttu-id="7a7ea-162">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-162">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-163">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-163">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-164">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-164">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-165">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-165">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-166">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-166">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-167">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-167">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-168">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-168">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-169">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-169">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-170">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-170">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-171">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-171">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-172">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-172">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-173">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-173">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |



 

<span data-ttu-id="7a7ea-174">若要強制轉譯目標使用硬體呈現，請使用 [**D2D1 轉譯 \_ \_ 目標 \_ 類型 \_ 硬體**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 設定。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-174">To force a render target to use hardware rendering, use the [**D2D1\_RENDER\_TARGET\_TYPE\_HARDWARE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) setting.</span></span> <span data-ttu-id="7a7ea-175">下表列出明確使用硬體轉譯的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 物件所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-175">The following table lists the supported formats for [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects that explicitly use hardware rendering.</span></span>



| <span data-ttu-id="7a7ea-176">格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-176">Format</span></span>                        | <span data-ttu-id="7a7ea-177">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-177">Alpha mode</span></span>                       |
|-------------------------------|----------------------------------|
| <span data-ttu-id="7a7ea-178">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-178">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-179">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-179">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-180">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-180">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-181">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-181">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-182">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-182">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-183">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-183">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-184">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-184">DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-185">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-185">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-186">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-186">DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-187">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-187">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-188">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-188">DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-189">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-189">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-190">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-190">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-191">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-191">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-192">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-192">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-193">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-193">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-194">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-194">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-195">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-195">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |



 

<span data-ttu-id="7a7ea-196">若要強制轉譯目標使用軟體呈現，請使用 [**D2D1 轉譯 \_ \_ 目標 \_ 類型 \_ 軟體**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 設定。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-196">To force a render target to use software rendering, use the [**D2D1\_RENDER\_TARGET\_TYPE\_SOFTWARE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) setting.</span></span> <span data-ttu-id="7a7ea-197">下表列出明確使用軟體轉譯的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 物件所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-197">The following table lists the supported formats for [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) objects that explicitly use software rendering.</span></span>



| <span data-ttu-id="7a7ea-198">格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-198">Format</span></span>                        | <span data-ttu-id="7a7ea-199">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-199">Alpha mode</span></span>                       |
|-------------------------------|----------------------------------|
| <span data-ttu-id="7a7ea-200">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-200">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-201">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-201">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-202">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-202">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-203">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-203">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-204">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-204">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-205">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-205">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-206">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-206">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-207">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-207">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-208">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-208">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-209">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-209">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-210">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-210">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-211">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-211">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |



 

<span data-ttu-id="7a7ea-212">無論 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 是否為硬體加速，預設的 [dxgi \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式都會使用 [dxgi \_ 格式 \_ B8G8R8A8](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ，而 [**D2D1 \_ Alpha \_ 模式 \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的 Alpha 模式預設會使用 **D2D1 \_ Alpha \_ 模式 \_ 忽略** 。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-212">Regardless of whether the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) is hardware accelerated, the [DXGI\_FORMAT\_UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format uses [DXGI\_FORMAT\_B8G8R8A8](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) by default and the [**D2D1\_ALPHA\_MODE\_UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alpha mode uses **D2D1\_ALPHA\_MODE\_IGNORE** by default.</span></span>

## <a name="supported-formats-for-id2d1devicecontext"></a><span data-ttu-id="7a7ea-213">支援的 ID2D1DeviceCoNtext 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-213">Supported formats for ID2D1DeviceContext</span></span>

<span data-ttu-id="7a7ea-214">從 Windows 8 開始， [**裝置內容**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) 會利用更多的 [**Direct3D 高色彩格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) ，例如：</span><span class="sxs-lookup"><span data-stu-id="7a7ea-214">Starting with Windows 8 the [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) takes advantage of more of the [**Direct3D high color formats**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) like:</span></span>

-   <span data-ttu-id="7a7ea-215">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="7a7ea-215">DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>
-   <span data-ttu-id="7a7ea-216">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="7a7ea-216">DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>
-   <span data-ttu-id="7a7ea-217">DXGI \_ 格式 \_ R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-217">DXGI\_FORMAT\_R16G16B16A16\_UNORM</span></span>
-   <span data-ttu-id="7a7ea-218">DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="7a7ea-218">DXGI\_FORMAT\_R16G16B16A16\_FLOAT</span></span>
-   <span data-ttu-id="7a7ea-219">DXGI \_ 格式 \_ R32G32B32A32 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="7a7ea-219">DXGI\_FORMAT\_R32G32B32A32\_FLOAT</span></span>

<span data-ttu-id="7a7ea-220">使用 [**ID2D1DeviceCoNtext：： IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) 方法來查看格式是否適用于特定的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-220">Use the [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) method to see if a format works on a particular device context.</span></span> <span data-ttu-id="7a7ea-221">這些格式也可以在 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)上運作。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-221">These formats may also work on an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget).</span></span>

<span data-ttu-id="7a7ea-222">這些格式除了 Windows 7 中的 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 介面所支援的格式之外。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-222">These formats are in addition to the formats supported by the [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) interface in Windows 7.</span></span> <span data-ttu-id="7a7ea-223">如需詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md) 內容。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-223">See [Devices and Device Contexts](devices-and-device-contexts.md) for more information.</span></span>

## <a name="supported-formats-for-compatible-render-target"></a><span data-ttu-id="7a7ea-224">相容轉譯目標支援的格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-224">Supported Formats for Compatible Render Target</span></span>

<span data-ttu-id="7a7ea-225">相容的轉譯目標 (由其中一個 [**ID2D1RenderTarget：： CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))方法所建立的 [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) ，) 會繼承其所建立之轉譯目標的支援格式和 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-225">A compatible render target (an [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) that is created by one of the [**ID2D1RenderTarget::CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) methods) inherits the supported formats and alpha modes of the render target that created it.</span></span> <span data-ttu-id="7a7ea-226">相容的轉譯目標也支援下列格式和 Alpha 模式組合，無論其父系支援何種組合。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-226">A compatible render target also supports the following format and alpha mode combinations, regardless of what its parent supports.</span></span>



| <span data-ttu-id="7a7ea-227">格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-227">Format</span></span>                  | <span data-ttu-id="7a7ea-228">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-228">Alpha mode</span></span>                       |
|-------------------------|----------------------------------|
| <span data-ttu-id="7a7ea-229">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-229">DXGI\_FORMAT\_A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-230">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-230">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-231">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-231">DXGI\_FORMAT\_A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-232">\_直接 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-232">D2D1\_ALPHA\_MODE\_STRAIGHT</span></span>      |
| <span data-ttu-id="7a7ea-233">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-233">DXGI\_FORMAT\_UNKNOWN</span></span>   | <span data-ttu-id="7a7ea-234">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-234">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |



 

<span data-ttu-id="7a7ea-235">[ [DXGI \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式] 預設會使用父轉譯目標格式，而 [ [**D2D1 \_ Alpha \_ ] 模式 \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的 [Alpha] 模式則使用預設預 **乘的 D2D1 \_ Alpha \_ 模式 \_** 。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-235">The [DXGI\_FORMAT\_UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format uses the parent render target format by default and the [**D2D1\_ALPHA\_MODE\_UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alpha mode uses **D2D1\_ALPHA\_MODE\_PREMULTIPLIED** by default.</span></span>

## <a name="supported-formats-for-dxgi-surface-render-target"></a><span data-ttu-id="7a7ea-236">適用于 DXGI 介面轉譯目標的支援格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-236">Supported Formats for DXGI Surface Render Target</span></span>

<span data-ttu-id="7a7ea-237">DXGI 轉譯目標是由其中一個 [**ID2D1Factory：： CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))方法所建立的 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-237">A DXGI render target is an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) that is created by one of the [**ID2D1Factory::CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) methods.</span></span> <span data-ttu-id="7a7ea-238">它支援下列格式和 Alpha 模式組合。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-238">It supports the following format and alpha mode combinations.</span></span>



| <span data-ttu-id="7a7ea-239">格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-239">Format</span></span>                        | <span data-ttu-id="7a7ea-240">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-240">Alpha mode</span></span>                       |
|-------------------------------|----------------------------------|
| <span data-ttu-id="7a7ea-241">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-241">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-242">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-242">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-243">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-243">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-244">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-244">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-245">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-245">DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-246">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-246">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-247">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-247">DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-248">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-248">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-249">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-249">DXGI\_FORMAT\_A8\_UNORM</span></span>       | <span data-ttu-id="7a7ea-250">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-250">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-251">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-251">DXGI\_FORMAT\_A8\_UNORM</span></span>       | <span data-ttu-id="7a7ea-252">\_直接 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-252">D2D1\_ALPHA\_MODE\_STRAIGHT</span></span>      |
| <span data-ttu-id="7a7ea-253">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-253">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-254">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-254">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-255">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-255">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-256">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-256">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |



 

> [!Note]  
> <span data-ttu-id="7a7ea-257">格式必須符合 dxgi 介面呈現目標所繪製之 DXGI 介面的格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-257">The format must match the format of the DXGI surface to which the DXGI surface render target draws.</span></span>

 

<span data-ttu-id="7a7ea-258">[ [Dxgi \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ] 格式預設會使用 dxgi 介面格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-258">The [DXGI\_FORMAT\_UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format uses the DXGI surface format by default.</span></span> <span data-ttu-id="7a7ea-259">請勿使用 [**D2D1 \_ Alpha \_ 模式 \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的 Alpha 模式搭配 DXGI 介面轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-259">Do not use the [**D2D1\_ALPHA\_MODE\_UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alpha mode with a DXGI surface render target.</span></span> <span data-ttu-id="7a7ea-260">它沒有預設值，而且會導致 DXGI 表面呈現目標建立失敗。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-260">It has no default value and will cause the DXGI surface render target creation to fail.</span></span>

## <a name="supported-formats-for-wic-bitmap-render-target"></a><span data-ttu-id="7a7ea-261">WIC 點陣圖轉譯目標支援的格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-261">Supported Formats for WIC Bitmap Render Target</span></span>

<span data-ttu-id="7a7ea-262">WIC 點陣圖轉譯目標是由其中一個 [**ID2D1Factory：： CreateWicBitmapRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))方法所建立的 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-262">A WIC bitmap render target is an [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) that is created by one of the [**ID2D1Factory::CreateWicBitmapRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) methods.</span></span> <span data-ttu-id="7a7ea-263">它支援下列格式和 Alpha 模式組合。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-263">It supports the following format and alpha mode combinations.</span></span>



| <span data-ttu-id="7a7ea-264">格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-264">Format</span></span>                        | <span data-ttu-id="7a7ea-265">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-265">Alpha mode</span></span>                       |
|-------------------------------|----------------------------------|
| <span data-ttu-id="7a7ea-266">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-266">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-267">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-267">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-268">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-268">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-269">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-269">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-270">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-270">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-271">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-271">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-272">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-272">DXGI\_FORMAT\_A8\_UNORM</span></span>       | <span data-ttu-id="7a7ea-273">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-273">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-274">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-274">DXGI\_FORMAT\_A8\_UNORM</span></span>       | <span data-ttu-id="7a7ea-275">\_直接 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-275">D2D1\_ALPHA\_MODE\_STRAIGHT</span></span>      |
| <span data-ttu-id="7a7ea-276">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-276">DXGI\_FORMAT\_A8\_UNORM</span></span>       | <span data-ttu-id="7a7ea-277">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-277">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-278">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-278">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-279">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-279">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-280">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-280">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-281">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-281">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-282">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-282">DXGI\_FORMAT\_UNKNOWN</span></span>         | <span data-ttu-id="7a7ea-283">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-283">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |



 

<span data-ttu-id="7a7ea-284">WIC 點陣圖目標的像素格式必須符合 WIC 點陣圖的像素格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-284">The pixel format of the WIC bitmap target must match the pixel format of the WIC bitmap.</span></span>

<span data-ttu-id="7a7ea-285">在預設情況下，[DXGI \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 格式使用 wic 點陣圖格式，而 [**D2D1 \_ Alpha \_ 模式 \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的 Alpha 模式預設會使用 wic 點陣圖 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-285">The [DXGI\_FORMAT\_UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format uses the WIC bitmap format by default and the [**D2D1\_ALPHA\_MODE\_UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alpha mode uses WIC bitmap alpha mode by default.</span></span>

## <a name="supported-formats-for-id2d1dcrendertarget"></a><span data-ttu-id="7a7ea-286">支援的 ID2D1DCRenderTarget 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-286">Supported Formats for ID2D1DCRenderTarget</span></span>

<span data-ttu-id="7a7ea-287">[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)支援下列格式和 Alpha 模式組合。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-287">An [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) supports the following format and alpha mode combinations.</span></span>



| <span data-ttu-id="7a7ea-288">格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-288">Format</span></span>                        | <span data-ttu-id="7a7ea-289">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-289">Alpha mode</span></span>                       |
|-------------------------------|----------------------------------|
| <span data-ttu-id="7a7ea-290">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-290">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-291">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-291">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-292">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-292">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-293">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-293">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |



 

<span data-ttu-id="7a7ea-294">請勿使用 [DXGI \_ 格式 \_ 未知](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 的格式或 [**D2D1 \_ Alpha 模式的 \_ \_ 未知**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha 模式與 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-294">Do not use the [DXGI\_FORMAT\_UNKNOWN](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format or the [**D2D1\_ALPHA\_MODE\_UNKNOWN**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alpha mode with an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span> <span data-ttu-id="7a7ea-295">它沒有預設值，而且會造成 **ID2D1DCRenderTarget** 建立失敗。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-295">It has no default value and will cause the **ID2D1DCRenderTarget** creation to fail.</span></span>

## <a name="specifying-a-pixel-format-for-an-id2d1bitmap"></a><span data-ttu-id="7a7ea-296">為 ID2D1Bitmap 指定像素格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-296">Specifying a Pixel Format for an ID2D1Bitmap</span></span>

<span data-ttu-id="7a7ea-297">一般而言， [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 物件支援下列格式和 Alpha 模式 (有一些限制，如接下來的段落所述。 ) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-297">Generally, [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) objects support the following formats and alpha modes (with some restrictions, described in the paragraphs that follow.)</span></span>



| <span data-ttu-id="7a7ea-298">格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-298">Format</span></span>                                                      | <span data-ttu-id="7a7ea-299">Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-299">Alpha mode</span></span>                       |
|-------------------------------------------------------------|----------------------------------|
| <span data-ttu-id="7a7ea-300">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-300">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>                               | <span data-ttu-id="7a7ea-301">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-301">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-302">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-302">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>                               | <span data-ttu-id="7a7ea-303">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-303">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-304">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-304">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>                               | <span data-ttu-id="7a7ea-305">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-305">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-306">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-306">DXGI\_FORMAT\_A8\_UNORM</span></span>                                     | <span data-ttu-id="7a7ea-307">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-307">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-308">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-308">DXGI\_FORMAT\_A8\_UNORM</span></span>                                     | <span data-ttu-id="7a7ea-309">\_直接 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-309">D2D1\_ALPHA\_MODE\_STRAIGHT</span></span>      |
| <span data-ttu-id="7a7ea-310">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-310">DXGI\_FORMAT\_A8\_UNORM</span></span>                                     | <span data-ttu-id="7a7ea-311">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-311">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-312">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-312">DXGI\_FORMAT\_UNKNOWN</span></span>                                       | <span data-ttu-id="7a7ea-313">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-313">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-314">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-314">DXGI\_FORMAT\_UNKNOWN</span></span>                                       | <span data-ttu-id="7a7ea-315">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-315">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-316">DXGI \_ 格式 \_ 未知</span><span class="sxs-lookup"><span data-stu-id="7a7ea-316">DXGI\_FORMAT\_UNKNOWN</span></span>                                       | <span data-ttu-id="7a7ea-317">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-317">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-318">DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-318">DXGI\_FORMAT\_B8G8R8X8\_UNORM (Windows 8.1 and later, only)</span></span> | <span data-ttu-id="7a7ea-319">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-319">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-320">DXGI \_ 格式 \_ BC1 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-320">DXGI\_FORMAT\_BC1\_UNORM (Windows 8.1 and later, only)</span></span>      | <span data-ttu-id="7a7ea-321">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-321">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-322">DXGI \_ 格式 \_ BC1 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-322">DXGI\_FORMAT\_BC1\_UNORM (Windows 8.1 and later, only)</span></span>      | <span data-ttu-id="7a7ea-323">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-323">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-324">DXGI \_ 格式 \_ BC1 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-324">DXGI\_FORMAT\_BC1\_UNORM (Windows 8.1 and later, only)</span></span>      | <span data-ttu-id="7a7ea-325">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-325">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-326">DXGI \_ 格式 \_ BC2 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-326">DXGI\_FORMAT\_BC2\_UNORM (Windows 8.1 and later, only)</span></span>      | <span data-ttu-id="7a7ea-327">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-327">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-328">DXGI \_ 格式 \_ BC2 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-328">DXGI\_FORMAT\_BC2\_UNORM (Windows 8.1 and later, only)</span></span>      | <span data-ttu-id="7a7ea-329">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-329">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-330">DXGI \_ 格式 \_ BC2 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-330">DXGI\_FORMAT\_BC2\_UNORM (Windows 8.1 and later, only)</span></span>      | <span data-ttu-id="7a7ea-331">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-331">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |
| <span data-ttu-id="7a7ea-332">DXGI \_ 格式 \_ BC3 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-332">DXGI\_FORMAT\_BC3\_UNORM (Windows 8.1 and later, only)</span></span>      | <span data-ttu-id="7a7ea-333">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-333">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-334">DXGI \_ 格式 \_ BC3 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-334">DXGI\_FORMAT\_BC3\_UNORM (Windows 8.1 and later, only)</span></span>      | <span data-ttu-id="7a7ea-335">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-335">D2D1\_ALPHA\_MODE\_IGNORE</span></span>        |
| <span data-ttu-id="7a7ea-336">DXGI \_ 格式 \_ BC3 \_ UNORM (Windows 8.1 和更新版本，只能) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-336">DXGI\_FORMAT\_BC3\_UNORM (Windows 8.1 and later, only)</span></span>      | <span data-ttu-id="7a7ea-337">未知的 D2D1 \_ ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-337">D2D1\_ALPHA\_MODE\_UNKNOWN</span></span>       |



 

<span data-ttu-id="7a7ea-338">當您使用 [**ID2D1RenderTarget：： CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)方法時，您可以使用 [**D2D1 \_ BITMAP \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties)結構的 **pixelFormat** 欄位來指定新轉譯目標的像素格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-338">When you use the [**ID2D1RenderTarget::CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) method, you use the **pixelFormat** field of a [**D2D1\_BITMAP\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) structure to specify the pixel format of the new render target.</span></span> <span data-ttu-id="7a7ea-339">它必須符合 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 來源的像素格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-339">It must match the pixel format of the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) source.</span></span>

<span data-ttu-id="7a7ea-340">當您使用 [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap))方法時，您可以使用 [**D2D1 \_ 點陣圖 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties)結構的 **pixelFormat** 欄位 (而不是 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)結構的 **pixelFormat** 成員) 指定新轉譯目標的像素格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-340">When you use the [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) method, you use the **pixelFormat** field of a [**D2D1\_BITMAP\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) structure (instead of the **pixelFormat** member of a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure) to specify the pixel format of the new render target.</span></span> <span data-ttu-id="7a7ea-341">它必須符合 WIC 點陣圖來源的像素格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-341">It must match the pixel format of the WIC bitmap source.</span></span>

> [!Note]  
> <span data-ttu-id="7a7ea-342">如需 (BCn) 像素格式之區塊壓縮的詳細資訊，請參閱 [區塊壓縮](block-compression.md)。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-342">For more information about support for block compressed (BCₙ) pixel formats, see [Block compression](block-compression.md).</span></span>

 

### <a name="supported-wic-formats"></a><span data-ttu-id="7a7ea-343">支援的 WIC 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-343">Supported WIC Formats</span></span>

<span data-ttu-id="7a7ea-344">當您使用 [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap))方法從 WIC 點陣圖建立點陣圖，或搭配 [**IWICBitmapLock**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock)使用 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)方法時，WIC 來源的格式必須是 Direct2D 所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-344">When you use the [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties__id2d1bitmap)) method to create a bitmap from a WIC bitmap, or when you use the [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) method with an [**IWICBitmapLock**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmaplock), the WIC source must be in a format supported by Direct2D.</span></span>



| <span data-ttu-id="7a7ea-345">WIC 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-345">WIC format</span></span>                     | <span data-ttu-id="7a7ea-346">對應的 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-346">Corresponding DXGI format</span></span>     | <span data-ttu-id="7a7ea-347">對應的 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-347">Corresponding alpha mode</span></span>                                        |
|--------------------------------|-------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="7a7ea-348">GUID \_ WICPixelFormat8bppAlpha</span><span class="sxs-lookup"><span data-stu-id="7a7ea-348">GUID\_WICPixelFormat8bppAlpha</span></span>  | <span data-ttu-id="7a7ea-349">DXGI \_ 格式 \_ A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-349">DXGI\_FORMAT\_A8\_UNORM</span></span>       | <span data-ttu-id="7a7ea-350">預 \_ \_ 乘的 D2D1 Alpha 模式 \_ 直接或 D2D1 \_ Alpha \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-350">D2D1\_ALPHA\_MODE\_STRAIGHT or D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span> |
| <span data-ttu-id="7a7ea-351">GUID \_ WICPixelFormat32bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="7a7ea-351">GUID\_WICPixelFormat32bppPRGBA</span></span> | <span data-ttu-id="7a7ea-352">DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-352">DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-353">D2D1 \_ Alpha \_ 模式 \_ 的預乘或 D2D1 \_ Alpha \_ 模式 \_ 略過</span><span class="sxs-lookup"><span data-stu-id="7a7ea-353">D2D1\_ALPHA\_MODE\_PREMULTIPLIED or D2D1\_ALPHA\_MODE\_IGNORE</span></span>   |
| <span data-ttu-id="7a7ea-354">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="7a7ea-354">GUID\_WICPixelFormat32bppBGR</span></span>   | <span data-ttu-id="7a7ea-355">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-355">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-356">D2D1 \_ ALPHA \_ 模式 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="7a7ea-356">D2D1\_ALPHA\_MODE\_IGNORE</span></span>                                       |
| <span data-ttu-id="7a7ea-357">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="7a7ea-357">GUID\_WICPixelFormat32bppPBGRA</span></span> | <span data-ttu-id="7a7ea-358">DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="7a7ea-358">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span> | <span data-ttu-id="7a7ea-359">預 \_ 乘的 D2D1 ALPHA \_ 模式 \_</span><span class="sxs-lookup"><span data-stu-id="7a7ea-359">D2D1\_ALPHA\_MODE\_PREMULTIPLIED</span></span>                                |



 

<span data-ttu-id="7a7ea-360">如需示範如何將 WIC 點陣圖轉換成支援格式的範例，請參閱 [如何從檔案載入點陣圖](how-to-load-a-direct2d-bitmap-from-a-file.md)。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-360">For an example that shows how to convert a WIC bitmap to a supported format, see [How to Load a Bitmap from a File](how-to-load-a-direct2d-bitmap-from-a-file.md).</span></span>

## <a name="using-an-unsupported-format"></a><span data-ttu-id="7a7ea-361">使用不支援的格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-361">Using an Unsupported Format</span></span>

<span data-ttu-id="7a7ea-362">使用上述表格中所列的像素格式和 Alpha 模式以外的任何組合，會導致 [**D2DERR \_ 不支援的 \_ 圖元 \_ 格式**](direct2d-error-codes.md) 或 **電子 \_ INVALIDARG** 錯誤。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-362">Using any combination other than the pixel formats and alpha modes that are listed in the earlier tables results in a [**D2DERR\_UNSUPPORTED\_PIXEL\_FORMAT**](direct2d-error-codes.md) or an **E\_INVALIDARG** error.</span></span>

## <a name="about-alpha-modes"></a><span data-ttu-id="7a7ea-363">關於 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-363">About Alpha Modes</span></span>

### <a name="about-premultiplied-and-straight-alpha-modes"></a><span data-ttu-id="7a7ea-364">關於預乘和直接 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-364">About Premultiplied and Straight Alpha Modes</span></span>

<span data-ttu-id="7a7ea-365">[**D2D1 \_ Alpha \_ 模式**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)列舉指出 Alpha 色板是使用預乘 Alpha、直立的 Alpha，還是應該忽略並視為不透明。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-365">The [**D2D1\_ALPHA\_MODE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) enumeration indicates whether the alpha channel uses premultiplied alpha, straight alpha, or should be ignored and considered opaque.</span></span> <span data-ttu-id="7a7ea-366">若使用直接 Alpha，Alpha 色板會指出一個值，對應至色彩的透明程度。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-366">With straight alpha, the alpha channel indicates a value that corresponds to how transparent a color is.</span></span>

<span data-ttu-id="7a7ea-367">無論目的地格式為何，色彩一律會藉由 Direct2D 繪製命令和筆刷來視為直接 Alpha。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-367">Colors are always treated as straight alpha by Direct2D drawing commands and brushes, regardless of the destination format.</span></span>

<span data-ttu-id="7a7ea-368">使用預乘 Alpha 時，每個色頻都會依 Alpha 值調整。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-368">With premultiplied alpha, each color channel is scaled by the alpha value.</span></span> <span data-ttu-id="7a7ea-369">一般而言，沒有色頻值大於 Alpha 色板值。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-369">Typically, no color channel value is greater than the alpha channel value.</span></span> <span data-ttu-id="7a7ea-370">如果以乘前格式的色頻值大於 Alpha 色板，則標準來源過度混色數學會建立加法 blend。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-370">If a color channel value in a pre-multiplied format is greater than the alpha channel, the standard source-over blending math creates an additive blend.</span></span>

<span data-ttu-id="7a7ea-371">Alpha 色板本身的值在直線和乘乘的 Alpha 中都相同。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-371">The value of the alpha channel itself is the same in both straight and pre-multiplied alpha.</span></span>

### <a name="the-differences-between-straight-and-premultiplied-alpha"></a><span data-ttu-id="7a7ea-372">直線和預乘 Alpha 之間的差異</span><span class="sxs-lookup"><span data-stu-id="7a7ea-372">The Differences Between Straight and Premultiplied Alpha</span></span>

<span data-ttu-id="7a7ea-373">使用直接 Alpha 描述 RGBA 色彩時，色彩的 Alpha 值會儲存在 Alpha 色板中。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-373">When describing an RGBA color by using straight alpha, the alpha value of the color is stored in the alpha channel.</span></span> <span data-ttu-id="7a7ea-374">例如，若要描述60% 不透明的紅色色彩，請使用下列值： (255、0、0、255 \* 0.6) = (255、0、0、153) 。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-374">For example, to describe a red color that is 60% opaque, use the following values: (255, 0, 0, 255 \* 0.6) = (255, 0, 0, 153).</span></span> <span data-ttu-id="7a7ea-375">255值表示全紅色，153 (是 255) 的60% 表示色彩應該有60% 的不透明度。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-375">The 255 value indicates full red, and 153 (which is 60 percent of 255) indicates that the color should have an opacity of 60 percent.</span></span>

<span data-ttu-id="7a7ea-376">使用預乘 Alpha 描述 RGBA 色彩時，每個色彩會乘以 Alpha 值： (255 \* 0.6、0 \* 0.6、0 \* 0.6、255 \* 0.6) = (153、0、0、153) 。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-376">When describing an RGBA color by using premultiplied alpha, each color is multiplied by the alpha value: (255 \* 0.6, 0 \* 0.6, 0 \* 0.6, 255 \* 0.6) = (153, 0, 0, 153).</span></span>

<span data-ttu-id="7a7ea-377">無論轉譯目標的 Alpha 模式為何， [**D2D1 \_ 色彩 \_ F**](d2d1-color-f.md) 值一律會轉譯為純 Alpha。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-377">Regardless of the alpha mode of the render target, [**D2D1\_COLOR\_F**](d2d1-color-f.md) values are always interpreted as straight alpha.</span></span> <span data-ttu-id="7a7ea-378">例如，當指定要搭配使用預乘 Alpha 模式之轉譯目標使用的 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 色彩時，請指定色彩，就像轉譯目標使用的是直接 Alpha 一樣。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-378">For example, when specifying the color of an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) for use with a render target that uses the premultiplied alpha mode, specify the color just as you would if the render target used straight alpha.</span></span> <span data-ttu-id="7a7ea-379">當您使用筆刷繪製時，Direct2D 會為您將色彩轉譯成目的地格式。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-379">When you paint with the brush, Direct2D translates the color to the destination format for you.</span></span>

### <a name="alpha-mode-for-render-targets"></a><span data-ttu-id="7a7ea-380">呈現目標的 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-380">Alpha Mode for Render Targets</span></span>

<span data-ttu-id="7a7ea-381">無論 Alpha 模式設定為何，轉譯目標的內容都支援透明度。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-381">Regardless of the alpha mode setting, a render target's contents support transparency.</span></span> <span data-ttu-id="7a7ea-382">例如，如果您繪製部分透明的紅色矩形，且其轉譯目標具有 [**D2D1 \_ Alpha \_ 模式 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)的 Alpha 模式，則矩形會顯示為粉紅色 (如果背景是白色) 。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-382">For example, if you draw a partly transparent red rectangle with a render target with an alpha mode of [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), the rectangle will appear pink (if the background is white).</span></span>

<span data-ttu-id="7a7ea-383">如果您在 Alpha 模式 [**D2D1 預 \_ 乘的 Alpha \_ \_ 模式**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)時繪製部分透明的紅色矩形，矩形會顯示為粉紅色 (假設背景是白色) ，而您可以透過它來查看呈現目標背後的任何內容。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-383">If you draw a partly transparent red rectangle when the alpha mode is [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), the rectangle will appear pink (assuming the background is white) and you can see through it to whatever is behind the render target.</span></span> <span data-ttu-id="7a7ea-384">當您使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) 轉譯成透明視窗，或當您使用相容的轉譯目標 ([**CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) 方法所建立的呈現目標，) 建立支援透明度的點陣圖時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-384">This is useful when you use a [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to render to a transparent window or when you use an compatible render target (a render targeted created by the [**CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) method) to create a bitmap that supports transparency.</span></span>

### <a name="cleartype-and-alpha-modes"></a><span data-ttu-id="7a7ea-385">ClearType 和 Alpha 模式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-385">ClearType and Alpha Modes</span></span>

<span data-ttu-id="7a7ea-386">如果您針對轉譯目標指定 [**D2D1 \_ Alpha \_ 模式 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 以外的 Alpha 模式，則文字消除鋸齒模式會自動從 [**D2D1 \_ 文字 \_ 消除鋸齒模式 \_ CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) 變更為 **D2D1 \_ 文字 \_ 消除鋸齒 \_ 模式灰階**。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-386">If you specify an alpha mode other than [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) for a render target, the text antialiasing mode automatically changes from [**D2D1\_TEXT\_ANTIALIAS\_MODE CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) to **D2D1\_TEXT\_ANTIALIAS\_MODE GRAYSCALE**.</span></span> <span data-ttu-id="7a7ea-387"> (當您指定 **D2D1 \_ Alpha \_ 模式 \_** 的 Alpha 模式時，Direct2D 會根據轉譯目標的種類為您設定 Alpha。 ) </span><span class="sxs-lookup"><span data-stu-id="7a7ea-387">(When you specify an alpha mode of **D2D1\_ALPHA\_MODE\_UNKNOWN**, Direct2D sets the alpha for you, depending on the kind of render target.)</span></span>

<span data-ttu-id="7a7ea-388">您可以使用 [**SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) 方法，將文字消除鋸齒模式變更回 [**D2D1 \_ 文字 \_ 消除鋸齒 \_ 模式 CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode)，但是將 CLEARTYPE 文字轉譯成透明介面可能會產生無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-388">You can use the [**SetTextAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode) method to change the text antialias mode back to [**D2D1\_TEXT\_ANTIALIAS\_MODE CLEARTYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode), but rendering ClearType text to a transparent surface can create unpredictable results.</span></span> <span data-ttu-id="7a7ea-389">如果您想要將 ClearType 文字轉譯成透明轉譯目標，建議您使用下列其中一種方法。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-389">If you want to render ClearType text to an transparent render target, we recommend that you use one of the following two techniques.</span></span>

-   <span data-ttu-id="7a7ea-390">您可以使用 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) 方法，將轉譯目標裁剪至將呈現文字的區域，然後呼叫 [**Clear**](id2d1rendertarget-clear.md) 方法並指定不透明的色彩，然後轉譯您的文字。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-390">Use the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) method to clip the render target to the area where the text will be rendered, then call the [**Clear**](id2d1rendertarget-clear.md) method and specify an opaque color, then render your text.</span></span>
-   <span data-ttu-id="7a7ea-391">您可以使用 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) ，在要呈現文字的區域後方繪製不透明的矩形。</span><span class="sxs-lookup"><span data-stu-id="7a7ea-391">Use [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f_id2d1brush_float_id2d1strokestyle)) to draw an opaque rectangle behind the area where the text will be rendered.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a7ea-392">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a7ea-392">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a7ea-393">**D2D1 \_ 圖元 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="7a7ea-393">**D2D1\_PIXEL\_FORMAT**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format)
</dt> <dt>

[<span data-ttu-id="7a7ea-394">**D2D1 \_ ALPHA \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="7a7ea-394">**D2D1\_ALPHA\_MODE**</span></span>](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)
</dt> <dt>

[<span data-ttu-id="7a7ea-395">DXGI \_ 格式</span><span class="sxs-lookup"><span data-stu-id="7a7ea-395">DXGI\_FORMAT</span></span>](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> </dl>

 

 