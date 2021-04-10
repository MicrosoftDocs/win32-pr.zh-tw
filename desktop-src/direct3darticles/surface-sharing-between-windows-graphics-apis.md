---
title: Windows 圖形 API 之間共用的介面
description: 本主題提供在 Windows 圖形 Api （包括 Direct3D 11、Direct2D、DirectWrite、Direct3D 10 和 Direct3D 9Ex）之間使用介面共用的互通性技術總覽。
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d889797902c964e603adefc51b25039afca7d46
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103683223"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a><span data-ttu-id="50a28-103">Windows 圖形 API 之間共用的介面</span><span class="sxs-lookup"><span data-stu-id="50a28-103">Surface Sharing Between Windows Graphics APIs</span></span>

<span data-ttu-id="50a28-104">本主題提供在 Windows 圖形 Api （包括 Direct3D 11、Direct2D、DirectWrite、Direct3D 10 和 Direct3D 9Ex）之間使用介面共用的互通性技術總覽。</span><span class="sxs-lookup"><span data-stu-id="50a28-104">This topic provides a technical overview of interoperability using surface sharing between Windows graphics APIs, including Direct3D 11, Direct2D, DirectWrite, Direct3D 10, and Direct3D 9Ex.</span></span> <span data-ttu-id="50a28-105">如果您已經瞭解這些 Api，這份檔可協助您在針對 Windows 7 或 Windows Vista 作業系統設計的應用程式中，使用多個 Api 轉譯成相同的介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-105">If you already have a working knowledge of these APIs, this paper can help you use multiple APIs to render to the same surface in an application designed for the Windows 7 or Windows Vista operating systems.</span></span> <span data-ttu-id="50a28-106">本主題也提供最佳做法指導方針和其他資源的指標。</span><span class="sxs-lookup"><span data-stu-id="50a28-106">This topic also provides best practice guidelines and pointers to additional resources.</span></span>

> [!Note]  
> <span data-ttu-id="50a28-107">針對 DirectX 11.1 執行時間上的 Direct2D 和 DirectWrite 互通性，您可以使用 [Direct2D 裝置和裝置](/windows/desktop/Direct2D/devices-and-device-contexts) 內容直接轉譯至 Direct3D 11 裝置。</span><span class="sxs-lookup"><span data-stu-id="50a28-107">For Direct2D and DirectWrite interoperability on the DirectX 11.1 runtime, you can use [Direct2D devices and device contexts](/windows/desktop/Direct2D/devices-and-device-contexts) to render directly to Direct3D 11 devices.</span></span>

 

<span data-ttu-id="50a28-108">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="50a28-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="50a28-109">簡介</span><span class="sxs-lookup"><span data-stu-id="50a28-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="50a28-110">API 互通性總覽</span><span class="sxs-lookup"><span data-stu-id="50a28-110">API Interoperability Overview</span></span>](#api-interoperability-overview)
-   [<span data-ttu-id="50a28-111">互通性案例</span><span class="sxs-lookup"><span data-stu-id="50a28-111">Interoperability Scenarios</span></span>](#interoperability-scenarios)
    -   [<span data-ttu-id="50a28-112">使用 Direct2D 共用 Direct3D 10.1 裝置</span><span class="sxs-lookup"><span data-stu-id="50a28-112">Direct3D 10.1 Device Sharing with Direct2D</span></span>](#direct3d-101-device-sharing-with-direct2d)
    -   [<span data-ttu-id="50a28-113">DXGI 1.1 同步共用的表面</span><span class="sxs-lookup"><span data-stu-id="50a28-113">DXGI 1.1 Synchronized Shared Surfaces</span></span>](#dxgi-11-synchronized-shared-surfaces)
    -   [<span data-ttu-id="50a28-114">Direct3D 9Ex 和 DXGI 型 Api 之間的互通性</span><span class="sxs-lookup"><span data-stu-id="50a28-114">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [<span data-ttu-id="50a28-115">結論</span><span class="sxs-lookup"><span data-stu-id="50a28-115">Conclusion</span></span>](#conclusion)

## <a name="introduction"></a><span data-ttu-id="50a28-116">簡介</span><span class="sxs-lookup"><span data-stu-id="50a28-116">Introduction</span></span>

<span data-ttu-id="50a28-117">在本檔中，Windows 圖形 API 互通性是指由不同的 Api 共用相同的呈現介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-117">In this document, Windows graphics API interoperability refers to the sharing of the same rendering surface by different APIs.</span></span> <span data-ttu-id="50a28-118">這種互通性可讓應用程式利用多個 Windows 圖形 Api 來建立吸引人的顯示器，並藉由維持與現有 Api 的相容性，讓您輕鬆地遷移至新的技術。</span><span class="sxs-lookup"><span data-stu-id="50a28-118">This kind of interoperability enables applications to create compelling displays by leveraging multiple Windows graphics APIs, and to ease migration to new technologies by maintaining compatibility with existing APIs.</span></span>

<span data-ttu-id="50a28-119">在 Windows 7 (和 Windows Vista SP2 （含 Windows 7 Interop 套件）中，使用 Vista 7IP) ，圖形轉譯 Api 是 Direct3D 11、Direct2D、Direct3D 10.1、Direct3D 10.0、Direct3D 9Ex、Direct3D 9c 及舊版 Direct3D Api，以及 GDI 和 GDI +。</span><span class="sxs-lookup"><span data-stu-id="50a28-119">In Windows 7 (and Windows Vista SP2 with Windows 7 Interop Pack, Vista 7IP), the graphics rendering APIs are Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c and earlier Direct3D APIs, as well GDI and GDI+.</span></span> <span data-ttu-id="50a28-120">Windows 影像處理元件 (WIC) 和 DirectWrite 是影像處理的相關技術，而 Direct2D 會執行文字轉譯。</span><span class="sxs-lookup"><span data-stu-id="50a28-120">Windows Imaging Component (WIC) and DirectWrite are related technologies for image processing, and Direct2D performs text rendering.</span></span> <span data-ttu-id="50a28-121">以 Direct3D 9c 和 Direct3D 9Ex 為基礎的 DirectX Video 加速 API (DXVA) 用於影片處理。</span><span class="sxs-lookup"><span data-stu-id="50a28-121">DirectX Video Acceleration API (DXVA), based on Direct3D 9c and Direct3D 9Ex, is used for video processing.</span></span>

<span data-ttu-id="50a28-122">隨著 Windows 圖形 Api 的發展，Microsoft 致力於確保 Api 之間的互通性。</span><span class="sxs-lookup"><span data-stu-id="50a28-122">As Windows graphics APIs evolve towards being Direct3D-based, Microsoft is investing more effort in ensuring interoperability across APIs.</span></span> <span data-ttu-id="50a28-123">根據 Direct3D Api 的新開發 Direct3D Api 和較高層級 Api 也會提供支援，讓您在需要時將相容性與舊版 Api 銜接。</span><span class="sxs-lookup"><span data-stu-id="50a28-123">Newly developed Direct3D APIs and higher level APIs based on Direct3D APIs also provide support where needed for bridging compatibility with older APIs.</span></span> <span data-ttu-id="50a28-124">為了說明，Direct2D 應用程式可以藉由共用 Direct3D 10.1 裝置，來使用 Direct3D 10.1。</span><span class="sxs-lookup"><span data-stu-id="50a28-124">To illustrate, Direct2D applications can use Direct3D 10.1 by sharing a Direct3D 10.1 device.</span></span> <span data-ttu-id="50a28-125">此外，Direct3D 11、Direct2D 和 Direct3D 10.1 Api 都能充分利用 DirectX Graphic Infrastructure (DXGI) 1.1，這會啟用完整支援這些 Api 之間互通性的同步共用表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-125">Also, Direct3D 11, Direct2D, and Direct3D 10.1 APIs can all take advantage of DirectX Graphics Infrastructure (DXGI) 1.1, which enables synchronized shared surfaces that fully support interoperability among these APIs.</span></span> <span data-ttu-id="50a28-126">透過從 DXGI 1.1 介面取得 GDI 裝置內容，以透過關聯性來與 GDI 互動的 DXGI 1.1 型 Api。</span><span class="sxs-lookup"><span data-stu-id="50a28-126">DXGI 1.1-based APIs interoperate with GDI, and with GDI+ by association, by obtaining the GDI device context from a DXGI 1.1 surface.</span></span> <span data-ttu-id="50a28-127">如需詳細資訊，請參閱 MSDN 上提供的 DXGI 和 GDI 互通性檔。</span><span class="sxs-lookup"><span data-stu-id="50a28-127">For more information, see the DXGI and GDI interoperability documentation available on MSDN.</span></span>

<span data-ttu-id="50a28-128">Direct3D 9Ex 執行時間支援未同步的介面共用。</span><span class="sxs-lookup"><span data-stu-id="50a28-128">Unsynchronized surface sharing is supported by the Direct3D 9Ex runtime.</span></span> <span data-ttu-id="50a28-129">以 DXVA 為基礎的影片應用程式，可以使用 direct3d 9Ex 和 DXGI 互通性協助程式進行 direct3d 9Ex 型 DXVA 與 Direct3D 11 for compute 著色器的互通性，或者可以與 Direct2D 互動以進行2D 控制項或文字轉譯。</span><span class="sxs-lookup"><span data-stu-id="50a28-129">DXVA-based video applications can use the Direct3D 9Ex and DXGI interoperability helper for Direct3D 9Ex-based DXVA interoperability with Direct3D 11 for compute shader, or can interoperate with Direct2D for 2D controls or text rendering.</span></span> <span data-ttu-id="50a28-130">WIC 和 DirectWrite 也會與 GDI、Direct2D 以及其他 Direct3D Api 相互關聯。</span><span class="sxs-lookup"><span data-stu-id="50a28-130">WIC and DirectWrite also interoperate with GDI, Direct2D, and by association, other Direct3D APIs.</span></span>

<span data-ttu-id="50a28-131">Direct3D 10.0、Direct3D 9c 和舊版 Direct3D 執行時間不支援共用的表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-131">Direct3D 10.0, Direct3D 9c, and older Direct3D runtimes do not support shared surfaces.</span></span> <span data-ttu-id="50a28-132">系統記憶體複本將繼續用於與 GDI 或 DXGI 型 Api 的互通性。</span><span class="sxs-lookup"><span data-stu-id="50a28-132">System memory copies will continue to be used for interoperability with GDI or DXGI-based APIs.</span></span>

<span data-ttu-id="50a28-133">請注意，本檔中的互通性案例指的是轉譯成共用轉譯介面的多個圖形 Api，而不是相同的應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="50a28-133">Note that the interoperability scenarios within this document refer to multiple graphics APIs rendering to a shared rendering surface, rather than to the same application window.</span></span> <span data-ttu-id="50a28-134">針對不同的介面，以不同表面為目標的個別 Api 進行同步處理時，會在本檔的討論範圍之外。</span><span class="sxs-lookup"><span data-stu-id="50a28-134">Synchronization for separate APIs targeting different surfaces that are then composited onto the same window is outside the scope of this paper.</span></span>

## <a name="api-interoperability-overview"></a><span data-ttu-id="50a28-135">API 互通性總覽</span><span class="sxs-lookup"><span data-stu-id="50a28-135">API Interoperability Overview</span></span>

<span data-ttu-id="50a28-136">您可以根據 API 對 API 案例和對應的互通性功能，來描述 Windows 圖形 Api 的介面共用互通性。</span><span class="sxs-lookup"><span data-stu-id="50a28-136">Surface sharing interoperability of Windows graphics APIs can be described in terms of API-to-API scenarios and the corresponding interoperability functionality.</span></span> <span data-ttu-id="50a28-137">從 Windows 7 開始，開始使用7IP 的 Windows Vista SP2，新的 Api 和相關聯的執行時間包括 Direct2D 和相關技術： Direct3D 11 和 DXGI 1.1。</span><span class="sxs-lookup"><span data-stu-id="50a28-137">As of Windows 7 and beginning with Windows Vista SP2 with 7IP, new APIs and associated runtimes include Direct2D and related technologies: Direct3D 11 and DXGI 1.1.</span></span> <span data-ttu-id="50a28-138">Windows 7 也改善了 GDI 效能。</span><span class="sxs-lookup"><span data-stu-id="50a28-138">GDI performance was also improved in Windows 7.</span></span> <span data-ttu-id="50a28-139">Windows Vista SP1 引進了 Direct3D 10.1。</span><span class="sxs-lookup"><span data-stu-id="50a28-139">Direct3D 10.1 was introduced in Windows Vista SP1.</span></span> <span data-ttu-id="50a28-140">下圖顯示 Api 之間的互通性支援。</span><span class="sxs-lookup"><span data-stu-id="50a28-140">The following diagram shows the interoperability support between APIs.</span></span>

![windows 圖形 api 之間的互通性支援圖表](images/surface-sharing-interoperability.png)

<span data-ttu-id="50a28-142">在此圖中，箭號會顯示連線 Api 可以存取相同介面的互通性案例。</span><span class="sxs-lookup"><span data-stu-id="50a28-142">In this diagram, arrows show interoperability scenarios in which the same surface can be accessible by the connected APIs.</span></span> <span data-ttu-id="50a28-143">藍色箭號表示 Windows Vista 中引進的互通性機制。</span><span class="sxs-lookup"><span data-stu-id="50a28-143">Blue arrows indicate interoperability mechanisms introduced in Windows Vista.</span></span> <span data-ttu-id="50a28-144">綠色箭號表示支援新 Api 或增強功能的互通性支援，可協助舊版 Api 與較新的 Api 交互操作。</span><span class="sxs-lookup"><span data-stu-id="50a28-144">Green arrows indicate interoperability support for new APIs or improvements that help older APIs to interoperate with newer APIs.</span></span> <span data-ttu-id="50a28-145">例如，綠色箭號代表裝置共用、同步處理的共用介面支援、Direct3D 9Ex/DXGI 同步處理協助程式，以及從相容的介面取得 GDI 裝置內容。</span><span class="sxs-lookup"><span data-stu-id="50a28-145">For example, green arrows represent device sharing, synchronized shared surface support, Direct3D 9Ex/DXGI synchronization helper, and obtaining a GDI device context from a compatible surface.</span></span>

## <a name="interoperability-scenarios"></a><span data-ttu-id="50a28-146">互通性案例</span><span class="sxs-lookup"><span data-stu-id="50a28-146">Interoperability Scenarios</span></span>

<span data-ttu-id="50a28-147">從 Windows 7 和 Windows Vista 7IP 開始，Windows 圖形 Api 的主流供應專案支援多個 Api 轉譯成相同的 DXGI 1.1 介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-147">As of Windows 7 and Windows Vista 7IP, mainstream offerings from Windows graphics APIs support multiple APIs rendering to the same DXGI 1.1 surface.</span></span>

<span data-ttu-id="50a28-148">**Direct3D 11、Direct3D 10.1、Direct2D-互通性**</span><span class="sxs-lookup"><span data-stu-id="50a28-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperability with each other**</span></span>

<span data-ttu-id="50a28-149">Direct3d 11、Direct3D 10.1 和 Direct2D Api (與其相關的 Api （例如 DirectWrite 和 WIC）) 可以使用 Direct3D 10.1 裝置共用或同步處理的共用介面彼此交互操作。</span><span class="sxs-lookup"><span data-stu-id="50a28-149">Direct3D 11, Direct3D 10.1 and Direct2D APIs (and its related APIs such as DirectWrite and WIC) can interoperate with each other using either Direct3D 10.1 device sharing or synchronized shared surfaces.</span></span>

### <a name="direct3d-101-device-sharing-with-direct2d"></a><span data-ttu-id="50a28-150">使用 Direct2D 共用 Direct3D 10.1 裝置</span><span class="sxs-lookup"><span data-stu-id="50a28-150">Direct3D 10.1 Device Sharing with Direct2D</span></span>

<span data-ttu-id="50a28-151">在 Direct2D 與 Direct3D 10.1 之間共用裝置，可讓應用程式使用相同的基礎 Direct3D 裝置物件，以順暢且有效率的方式將這兩個 Api 轉譯至相同的 DXGI 1.1 介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-151">Device sharing between Direct2D and Direct3D 10.1 allows an application to use both APIs to seamlessly and efficiently render onto the same DXGI 1.1 surface, using the same underlying Direct3D device object.</span></span> <span data-ttu-id="50a28-152">Direct2D 可讓您使用現有的 Direct3D 10.1 裝置來呼叫 Direct2D Api，並運用 Direct2D 建置於 Direct3D 10.1 和 DXGI 1.1 執行時間的事實。</span><span class="sxs-lookup"><span data-stu-id="50a28-152">Direct2D provides the ability to call Direct2D APIs using an existing Direct3D 10.1 device, leveraging the fact that Direct2D is built on top of Direct3D 10.1 and DXGI 1.1 runtimes.</span></span> <span data-ttu-id="50a28-153">下列程式碼片段說明 Direct2D 如何從與裝置相關聯的 DXGI 1.1 介面取得 Direct3D 10.1 裝置呈現目標。</span><span class="sxs-lookup"><span data-stu-id="50a28-153">The following code snippets illustrate how Direct2D obtains the Direct3D 10.1 device render target from a DXGI 1.1 surface associated with the device.</span></span> <span data-ttu-id="50a28-154">Direct3D 10.1 裝置轉譯目標可在 BeginDraw 和 EndDraw Api 之間執行 Direct2D 繪圖呼叫。</span><span class="sxs-lookup"><span data-stu-id="50a28-154">The Direct3D 10.1 device render target can execute Direct2D drawing calls between BeginDraw and EndDraw APIs.</span></span>


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



<span data-ttu-id="50a28-155">**備註**</span><span class="sxs-lookup"><span data-stu-id="50a28-155">**Remarks**</span></span>

-   <span data-ttu-id="50a28-156">相關聯的 Direct3D 10.1 裝置必須支援 BGRA 格式。</span><span class="sxs-lookup"><span data-stu-id="50a28-156">The associated Direct3D 10.1 device must support BGRA format.</span></span> <span data-ttu-id="50a28-157">該裝置是藉由使用參數 D3D10 \_ 建立 \_ 裝置 \_ BGRA 支援來呼叫 D3D10CreateDevice1 所建立 \_ 。</span><span class="sxs-lookup"><span data-stu-id="50a28-157">That device was created by calling D3D10CreateDevice1 with parameter D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT.</span></span> <span data-ttu-id="50a28-158">從 Direct3D 10 功能等級9.1 開始支援 BGRA 格式。</span><span class="sxs-lookup"><span data-stu-id="50a28-158">BGRA format is supported starting with Direct3D 10 feature level 9.1.</span></span>
-   <span data-ttu-id="50a28-159">應用程式不應建立多個與相同 Direct3D 10.1 裝置相關聯的 ID2D1RenderTargets。</span><span class="sxs-lookup"><span data-stu-id="50a28-159">The application should not create multiple ID2D1RenderTargets associating to the same Direct3D10.1 device.</span></span>
-   <span data-ttu-id="50a28-160">為了達到最佳效能，請隨時保留至少一個資源，例如與裝置相關聯的材質或表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-160">For optimal performance, keep at least one resource around at all times, such as textures or surfaces associated with the device.</span></span>

<span data-ttu-id="50a28-161">裝置共用適用于同進程的單一執行緒使用，這兩種轉譯裝置都是由 Direct3D 10.1 和 Direct2D 轉譯 Api 所共用。</span><span class="sxs-lookup"><span data-stu-id="50a28-161">Device sharing is suitable for in-process, single-threaded usage of one rendering device shared by both Direct3D 10.1 and Direct2D rendering APIs.</span></span> <span data-ttu-id="50a28-162">已同步處理的共用介面可讓 Direct3D 10.1、Direct2D 和 Direct3D 11 Api 使用多個轉譯裝置的多執行緒、同進程和跨進程使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-162">Synchronized shared surfaces enable multi-threaded, in-process and out-of-process usage of multiple rendering devices used by Direct3D 10.1, Direct2D and Direct3D 11 APIs.</span></span>

<span data-ttu-id="50a28-163">Direct3D 10.1 和 Direct2D 互通性的另一種方法是使用 ID3D1RenderTarget：： CreateSharedBitmap，它會從 IDXGISurface 建立 ID2D1Bitmap 物件。</span><span class="sxs-lookup"><span data-stu-id="50a28-163">Another method of Direct3D 10.1 and Direct2D interoperability is by using ID3D1RenderTarget::CreateSharedBitmap, which creates an ID2D1Bitmap object from IDXGISurface.</span></span> <span data-ttu-id="50a28-164">您可以將 Direct3D 10.1 場景寫入點陣圖，並使用 Direct2D 加以呈現。</span><span class="sxs-lookup"><span data-stu-id="50a28-164">You can write a Direct3D10.1 scene to the bitmap and render it with Direct2D.</span></span> <span data-ttu-id="50a28-165">如需詳細資訊，請參閱 [ID2D1RenderTarget：： CreateSharedBitmap 方法](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)。</span><span class="sxs-lookup"><span data-stu-id="50a28-165">For more information, see [ID2D1RenderTarget::CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span></span>

### <a name="direct2d-software-rasterization"></a><span data-ttu-id="50a28-166">Direct2D 軟體點陣化</span><span class="sxs-lookup"><span data-stu-id="50a28-166">Direct2D Software Rasterization</span></span>

<span data-ttu-id="50a28-167">使用 Direct2D software 轉譯器時，不支援使用 Direct3D 10.1 進行裝置共用，例如，藉由指定 D2D1 轉譯 \_ \_ 目標使用方式， \_ \_ \_ \_ 在 \_ \_ \_ 建立 Direct2D 轉譯目標時，于 D2D1 轉譯目標使用方式中強制軟體轉譯。</span><span class="sxs-lookup"><span data-stu-id="50a28-167">Device sharing with Direct3D 10.1 is not supported when using the Direct2D software renderer, for example, by specifying D2D1\_RENDER\_TARGET\_USAGE\_FORCE\_SOFTWARE\_RENDERING in D2D1\_RENDER\_TARGET\_USAGE when creating a Direct2D render target.</span></span>

<span data-ttu-id="50a28-168">Direct2D 可以使用 WARP10 軟體轉譯器與 Direct3D 10 或 Direct3D 11 共用裝置，但效能會大幅降低。</span><span class="sxs-lookup"><span data-stu-id="50a28-168">Direct2D can use the WARP10 software rasterizer to share device with Direct3D 10 or Direct3D 11, but the performance declines significantly.</span></span>

### <a name="dxgi-11-synchronized-shared-surfaces"></a><span data-ttu-id="50a28-169">DXGI 1.1 同步共用的表面</span><span class="sxs-lookup"><span data-stu-id="50a28-169">DXGI 1.1 Synchronized Shared Surfaces</span></span>

<span data-ttu-id="50a28-170">Direct3D 11、Direct3D 10.1 和 Direct2D Api 全都使用 DXGI 1.1，其提供的功能可將讀取和寫入相同的視訊記憶體介面， (DXGISurface1 由兩個或更多 Direct3D 裝置進行) 。</span><span class="sxs-lookup"><span data-stu-id="50a28-170">Direct3D 11, Direct3D 10.1 and Direct2D APIs all use DXGI 1.1, which provides the functionality to synchronize reading from and writing to the same video memory surface (DXGISurface1) by two or more Direct3D devices.</span></span> <span data-ttu-id="50a28-171">使用同步共用表面的轉譯裝置可以是 Direct3D 10.1 或 Direct3D 11 裝置，每個裝置都在相同的進程或跨進程中執行。</span><span class="sxs-lookup"><span data-stu-id="50a28-171">The rendering devices using synchronized shared surfaces can be Direct3D 10.1 or Direct3D 11 devices, each running in the same process or cross-processes.</span></span>

<span data-ttu-id="50a28-172">應用程式可以使用已同步處理的共用介面，從 Direct2D 轉譯目標物件取得 Direct3D 10.1 裝置，以便在任何 DXGI 1.1 型裝置（例如 Direct3D 11 和 Direct3D 10.1）或 Direct3D 11 和 Direct2D 之間互通。</span><span class="sxs-lookup"><span data-stu-id="50a28-172">Applications can use synchronized shared surfaces to interoperate between any DXGI 1.1-based devices, such as Direct3D 11 and Direct3D 10.1, or between Direct3D 11 and Direct2D, by obtaining the Direct3D 10.1 device from Direct2D render target object.</span></span>

<span data-ttu-id="50a28-173">在 Direct3D 10.1 和更新版本的 Api 中，若要使用 DXGI 1.1，請確定已使用 dxgi 1.1 factory 物件列舉的 DXGI 1.1 介面卡物件來建立 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="50a28-173">In Direct3D 10.1 and later APIs, to use DXGI 1.1, ensure that the Direct3D device is created using a DXGI 1.1 adapter object, which is enumerated from the DXGI 1.1 factory object.</span></span> <span data-ttu-id="50a28-174">呼叫 CreateDXGIFactory1 來建立 IDXGIFactory1 物件，並呼叫 EnumAdapters1 來列舉 IDXGIAdapter1 物件。</span><span class="sxs-lookup"><span data-stu-id="50a28-174">Call CreateDXGIFactory1 to create the IDXGIFactory1 object, and EnumAdapters1 to enumerate the IDXGIAdapter1 object.</span></span> <span data-ttu-id="50a28-175">IDXGIAdapter1 物件必須傳入作為 D3D10CreateDevice 或 D3D10CreateDeviceAndSwapChain 呼叫的一部分。</span><span class="sxs-lookup"><span data-stu-id="50a28-175">The IDXGIAdapter1 object needs to be passed in as part of D3D10CreateDevice or D3D10CreateDeviceAndSwapChain call.</span></span> <span data-ttu-id="50a28-176">如需有關 DXGI 1.1 Api 的詳細資訊，請參閱 [dxgi 的程式設計指南](https://msdn.microsoft.com/library/ee418147(VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="50a28-176">For more information on DXGI 1.1 APIs, please refer to the [Programming Guide for DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span></span>

### <a name="apis"></a><span data-ttu-id="50a28-177">API</span><span class="sxs-lookup"><span data-stu-id="50a28-177">APIs</span></span>

<span data-ttu-id="50a28-178">**D3D10 \_ 資源的 \_ 其他 \_ 共用 \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="50a28-178">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="50a28-179">建立已同步處理的共用資源時， \_ 請 \_ \_ \_ 在 D3D10 \_ 資源的 \_ 其他旗標中設定 D3D10 資源的其他共用 KEYEDMUTEX \_ 。</span><span class="sxs-lookup"><span data-stu-id="50a28-179">When creating the synchronized shared resource, set D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX in D3D10\_RESOURCE\_MISC\_FLAG.</span></span>  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



<span data-ttu-id="50a28-180">**D3D10 \_ 資源的 \_ 其他 \_ 共用 \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="50a28-180">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="50a28-181">啟用使用 IDXGIKeyedMutex：： AcquireSync 和 ReleaseSync Api 來同步處理所建立的資源。</span><span class="sxs-lookup"><span data-stu-id="50a28-181">Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs.</span></span> <span data-ttu-id="50a28-182">下列資源建立 Direct3D 10.1 Api 全都採用 D3D10 \_ 資源 \_ 其他 \_ 旗標參數，以支援新的旗標。</span><span class="sxs-lookup"><span data-stu-id="50a28-182">The following resource creation Direct3D 10.1 APIs that all take a D3D10\_RESOURCE\_MISC\_FLAG parameter have been extended to support the new flag.</span></span>  

-   <span data-ttu-id="50a28-183">ID3D10Device1::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="50a28-183">ID3D10Device1::CreateTexture1D</span></span>
-   <span data-ttu-id="50a28-184">ID3D10Device1::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="50a28-184">ID3D10Device1::CreateTexture2D</span></span>
-   <span data-ttu-id="50a28-185">ID3D10Device1::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="50a28-185">ID3D10Device1::CreateTexture3D</span></span>
-   <span data-ttu-id="50a28-186">ID3D10Device1::CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="50a28-186">ID3D10Device1::CreateBuffer</span></span>

  
<span data-ttu-id="50a28-187">如果使用 D3D10 資源的「其他共用 KEYEDMUTEX 旗標集合來呼叫任何列出的函 \_ \_ \_ \_ 式，則可以針對 IDXGIKeyedMutex 介面查詢傳回的介面，該介面會執行 AcquireSync 和 ReleaseSync api 來同步處理介面的存取。</span><span class="sxs-lookup"><span data-stu-id="50a28-187">If any of the listed functions are called with the D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX flag set, the interface returned can be queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface.</span></span> <span data-ttu-id="50a28-188">建立介面的裝置，以及使用 OpenSharedResource) 開啟介面 (的任何其他裝置，都必須在介面的任何轉譯命令之前呼叫 IDXGIKeyedMutex：： AcquireSync，並在完成轉譯時呼叫 IDXGIKeyedMutex：： ReleaseSync。</span><span class="sxs-lookup"><span data-stu-id="50a28-188">The device creating the surface and any other device opening the surface (using OpenSharedResource) is required to call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.</span></span>  
<span data-ttu-id="50a28-189">變形和 REF 裝置不支援共用資源。</span><span class="sxs-lookup"><span data-stu-id="50a28-189">WARP and REF devices do not support shared resources.</span></span> <span data-ttu-id="50a28-190">嘗試在彎曲或 REF 裝置上使用此旗標建立資源，會導致 create 方法傳回 E \_ OUTOFMEMORY 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="50a28-190">Attempting to create a resource with this flag on either a WARP or REF device will cause the create method to return an E\_OUTOFMEMORY error code.</span></span>  
<span data-ttu-id="50a28-191">**IDXGIKEYEDMUTEX 介面**</span><span class="sxs-lookup"><span data-stu-id="50a28-191">**IDXGIKEYEDMUTEX INTERFACE**</span></span>  
<span data-ttu-id="50a28-192">在 DXGI 1.1 （IDXGIKeyedMutex）中的新介面代表索引 mutex，可讓您獨佔存取多個裝置使用的共用資源。</span><span class="sxs-lookup"><span data-stu-id="50a28-192">A new interface in DXGI 1.1, IDXGIKeyedMutex, represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.</span></span> <span data-ttu-id="50a28-193">如需有關此介面和其兩種方法（AcquireSync 和 ReleaseSync）的參考檔，請參閱 [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="50a28-193">For reference documentation about this interface and its two methods, AcquireSync and ReleaseSync, see [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span></span>  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a><span data-ttu-id="50a28-194">範例：兩個 Direct3D 10.1 裝置之間的同步表面共用</span><span class="sxs-lookup"><span data-stu-id="50a28-194">Sample: Synchronized Surface Sharing Between two Direct3D 10.1 Devices</span></span>

<span data-ttu-id="50a28-195">下列範例說明如何在兩個 Direct3D 10.1 裝置之間共用一個表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-195">The example below illustrates sharing a surface between two Direct3D 10.1 devices.</span></span> <span data-ttu-id="50a28-196">同步處理的共用介面是由 Direct3D 10.1 裝置所建立。</span><span class="sxs-lookup"><span data-stu-id="50a28-196">The synchronized shared surface is created by a Direct3D10.1 device.</span></span>


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



<span data-ttu-id="50a28-197">相同的 Direct3D 10.1 裝置可以藉由呼叫 AcquireSync 來取得已同步處理的共用介面，然後藉由呼叫 ReleaseSync 來釋出其他裝置呈現的介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-197">The same Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the other device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="50a28-198">當您未與任何其他 Direct3D 裝置共用同步處理的共用介面時，建立者可以取得和釋放已同步處理的共用介面 (，藉由使用相同的索引鍵值取得和釋放) 開始和結束轉譯。</span><span class="sxs-lookup"><span data-stu-id="50a28-198">When not sharing the synchronized shared surface with any other Direct3D device, the creator can obtain and release the synchronized shared surface (to start and end rendering) by acquiring and release using the same key value.</span></span>


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



<span data-ttu-id="50a28-199">第二個 Direct3D 10.1 裝置可以藉由呼叫 AcquireSync 來取得已同步處理的共用介面，然後藉由呼叫 ReleaseSync 來釋放第一個裝置轉譯的介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-199">The second Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the first device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="50a28-200">請注意，裝置2可以使用與裝置 1 ReleaseSync 呼叫中所指定的相同金鑰值，來取得已同步處理的共用介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-200">Note that device 2 is able to acquire the synchronized shared surface using the same key value as the one specified in the ReleaseSync call by device 1.</span></span>


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



<span data-ttu-id="50a28-201">共用相同介面的其他裝置可以使用額外的按鍵來取得和釋放介面，如下列呼叫所示。</span><span class="sxs-lookup"><span data-stu-id="50a28-201">Additional devices sharing the same surface can take turns acquiring and releasing the surface by using additional keys, as shown in the following calls.</span></span>


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



<span data-ttu-id="50a28-202">請注意，真實世界的應用程式可能一律會轉譯成中繼表面，然後將它複製到共用表面，以防止在另一部共用介面的裝置上等候任何一個裝置。</span><span class="sxs-lookup"><span data-stu-id="50a28-202">Note that a real-world application might always render to an intermediate surface that is then copied into the shared surface to prevent any one device waiting on another device that shares the surface.</span></span>

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a><span data-ttu-id="50a28-203">搭配 Direct2D 和 Direct3D 11 使用同步共用的表面</span><span class="sxs-lookup"><span data-stu-id="50a28-203">Using Synchronized Shared Surfaces with Direct2D and Direct3D 11</span></span>

<span data-ttu-id="50a28-204">同樣地，針對 Direct3D 11 和 Direct3D 10.1 Api 之間的共用，您可以從 API 裝置建立已同步處理的共用介面，並與其他 API 裝置共用 (s) 、進出進程。</span><span class="sxs-lookup"><span data-stu-id="50a28-204">Similarly, for sharing between Direct3D 11 and Direct3D 10.1 APIs, a synchronized shared surface can be created from either API device and shared with the other API device(s), in or out of process.</span></span>

<span data-ttu-id="50a28-205">使用 Direct2D 的應用程式可以共用 Direct3D 10.1 裝置，並使用同步處理的共用介面與 Direct3D 11 或其他 Direct3D 10.1 裝置交互操作，不論它們屬於相同的進程或不同的進程。</span><span class="sxs-lookup"><span data-stu-id="50a28-205">Applications that use Direct2D can share a Direct3D 10.1 device and use a synchronized shared surface to interoperate with Direct3D 11 or other Direct3D 10.1 devices, whether they belong to the same process or different processes.</span></span> <span data-ttu-id="50a28-206">不過，對於單一進程、單一線程應用程式，裝置共用是 Direct2D 與 Direct3D 10 或 Direct3D 11 之間最高效能且有效率的互通性方法。</span><span class="sxs-lookup"><span data-stu-id="50a28-206">However, for single-process, single-thread applications, device sharing is the most high-performance and efficient method of interoperability between Direct2D and either Direct3D 10 or Direct3D 11.</span></span>

### <a name="software-rasterizer"></a><span data-ttu-id="50a28-207">軟體轉譯器</span><span class="sxs-lookup"><span data-stu-id="50a28-207">Software Rasterizer</span></span>

<span data-ttu-id="50a28-208">當應用程式使用 Direct3D 或 Direct2D software rasterizers （包括參考轉譯器和變形）（而不是使用圖形硬體加速）時，不支援同步共用的表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-208">Synchronized shared surfaces are not supported when applications use the Direct3D or Direct2D software rasterizers, including the reference rasterizer and WARP, instead of using graphics hardware acceleration.</span></span>

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a><span data-ttu-id="50a28-209">Direct3D 9Ex 和 DXGI 型 Api 之間的互通性</span><span class="sxs-lookup"><span data-stu-id="50a28-209">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>

<span data-ttu-id="50a28-210">Direct3D 9Ex Api 包含介面共用的概念，可讓其他 Api 從共用介面讀取。</span><span class="sxs-lookup"><span data-stu-id="50a28-210">Direct3D 9Ex APIs included the notion of surface sharing to allow other APIs to read from the shared surface.</span></span> <span data-ttu-id="50a28-211">為了共用對 Direct3D 9Ex 共用介面的讀取和寫入，您必須將手動同步處理新增至應用程式本身。</span><span class="sxs-lookup"><span data-stu-id="50a28-211">In order to share reading and writing to a Direct3D 9Ex shared surface, you must add manual synchronization to the application itself.</span></span>

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a><span data-ttu-id="50a28-212">Direct3D 9Ex 共用的表面加上手動同步處理協助程式</span><span class="sxs-lookup"><span data-stu-id="50a28-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span></span>

<span data-ttu-id="50a28-213">Direct3D 9Ex 和 Direct3D 10 或11互通性中最基本的工作，是將第一個裝置的單一介面從第一個裝置 (裝置 A) 傳送至第二個 (裝置 B) 如此一來，當裝置 B 取得介面上的控制碼時，即保證裝置 A 的轉譯已完成。</span><span class="sxs-lookup"><span data-stu-id="50a28-213">The most fundamental task in Direct3D 9Ex and Direct3D 10 or 11 interoperability is passing a single surface from the first device (device A) to the second (device B) such that when device B acquires a handle on the surface, device A's rendering is guaranteed to have completed.</span></span> <span data-ttu-id="50a28-214">因此，裝置 B 可以使用此介面，而不需要擔心。</span><span class="sxs-lookup"><span data-stu-id="50a28-214">Therefore, device B can use this surface without worry.</span></span> <span data-ttu-id="50a28-215">這非常類似于傳統生產者-取用者的問題，而此討論會以這種方式為問題建模。</span><span class="sxs-lookup"><span data-stu-id="50a28-215">This is very similar to the classic producer-consumer problem and this discussion models the problem that way.</span></span> <span data-ttu-id="50a28-216">第一個使用介面的裝置，然後會讓出它是生產者 (裝置 A) ，而最初等待的裝置是取用者 (裝置 B) 。</span><span class="sxs-lookup"><span data-stu-id="50a28-216">The first device that uses the surface and then relinquishes it is the producer (Device A), and the device that is initially waiting is the consumer (Device B).</span></span> <span data-ttu-id="50a28-217">任何真實世界的應用程式都比這個更複雜，而且會將多個生產者-取用者建立區塊串連在一起，以建立所需的功能。</span><span class="sxs-lookup"><span data-stu-id="50a28-217">Any real-world application is more sophisticated than this, and will chain together multiple producer-consumer building blocks to create the desired functionality.</span></span>

<span data-ttu-id="50a28-218">生產者-取用者組建區塊會使用表面的佇列在協助程式中實作為。</span><span class="sxs-lookup"><span data-stu-id="50a28-218">The producer-consumer building blocks are implemented in the helper by using a queue of surfaces.</span></span> <span data-ttu-id="50a28-219">介面會由取用者排入佇列，並由取用者清除佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-219">Surfaces are enqueued by the producer and dequeued by the consumer.</span></span> <span data-ttu-id="50a28-220">此協助程式引進三個 COM 介面： ISurfaceQueue、ISurfaceProducer 和 ISurfaceConsumer。</span><span class="sxs-lookup"><span data-stu-id="50a28-220">The helper introduces three COM interfaces: ISurfaceQueue, ISurfaceProducer, and ISurfaceConsumer.</span></span>

### <a name="high-level-overview-of-helper"></a><span data-ttu-id="50a28-221">Helper 的 High-Level 總覽</span><span class="sxs-lookup"><span data-stu-id="50a28-221">High-Level Overview of Helper</span></span>

<span data-ttu-id="50a28-222">ISurfaceQueue 物件是使用共用表面的建立區塊。</span><span class="sxs-lookup"><span data-stu-id="50a28-222">The ISurfaceQueue object is the building block for using the shared surfaces.</span></span> <span data-ttu-id="50a28-223">它是以初始化的 Direct3D 裝置所建立，並提供描述來建立固定的共用表面數目。</span><span class="sxs-lookup"><span data-stu-id="50a28-223">It is created with an initialized Direct3D device and a description to create a fixed number of shared surfaces.</span></span> <span data-ttu-id="50a28-224">佇列物件會管理資源的建立和開啟程式碼。</span><span class="sxs-lookup"><span data-stu-id="50a28-224">The queue object manages creation of resources and opening of code.</span></span> <span data-ttu-id="50a28-225">曲面的數目和類型是固定的;一旦建立介面之後，應用程式就無法新增或移除這些表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-225">The number and type of surfaces are fixed; once the surfaces are created, the application cannot add or remove them.</span></span>

<span data-ttu-id="50a28-226">ISurfaceQueue 物件的每個實例都會提供一種單向街道，可用來從產生的裝置傳送表面到取用的裝置。</span><span class="sxs-lookup"><span data-stu-id="50a28-226">Each instance of the ISurfaceQueue object provides a sort of one-way street that can be used to send surfaces from the producing device to the consuming device.</span></span> <span data-ttu-id="50a28-227">您可以使用多個這種單向街道，在特定應用程式的裝置之間啟用 surface 共用案例。</span><span class="sxs-lookup"><span data-stu-id="50a28-227">Multiple such one-way streets can be used to enable surface sharing scenarios between devices of specific applications.</span></span>

<span data-ttu-id="50a28-228">**建立/物件存留期**</span><span class="sxs-lookup"><span data-stu-id="50a28-228">**Creation/Object Lifetime**</span></span>  
<span data-ttu-id="50a28-229">有兩種方式可以建立佇列物件：透過 CreateSurfaceQueue，或透過 ISurfaceQueue 的複製方法。</span><span class="sxs-lookup"><span data-stu-id="50a28-229">There are two ways to create the queue object: through CreateSurfaceQueue, or through the Clone method of ISurfaceQueue.</span></span> <span data-ttu-id="50a28-230">因為介面是 COM 物件，所以會套用標準 COM 存留期管理。</span><span class="sxs-lookup"><span data-stu-id="50a28-230">Because the interfaces are COM objects, standard COM lifetime management applies.</span></span>  
<span data-ttu-id="50a28-231">**生產者/取用者模型**</span><span class="sxs-lookup"><span data-stu-id="50a28-231">**Producer/Consumer Model**</span></span>  
<span data-ttu-id="50a28-232">排入佇列 () ：生產者會呼叫此函式來表示它是使用介面完成，現在可供其他裝置使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-232">Enqueue (): The producer calls this function to indicate it is done with the surface, which can now become available to another device.</span></span> <span data-ttu-id="50a28-233">從這個函式傳回時，生產者裝置不再有介面的許可權，而且不安全地繼續使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-233">Upon returning from this function, the producer device no longer has rights to the surface and it is unsafe to continue using it.</span></span>  
<span data-ttu-id="50a28-234">清除佇列 () ：取用裝置會呼叫此函式以取得共用的介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-234">Dequeue (): The consuming device calls this function to get a shared surface.</span></span> <span data-ttu-id="50a28-235">API 可保證任何已清除佇列的表面都可供使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-235">The API guarantees that any dequeued surfaces are ready to be used.</span></span>  
<span data-ttu-id="50a28-236">**中繼資料**</span><span class="sxs-lookup"><span data-stu-id="50a28-236">**Metadata**</span></span>  
<span data-ttu-id="50a28-237">API 支援將中繼資料與共享的表面產生關聯。</span><span class="sxs-lookup"><span data-stu-id="50a28-237">The API supports associating metadata with the shared surfaces.</span></span>  
<span data-ttu-id="50a28-238">排入佇列 () 可選擇指定將傳遞給取用裝置的其他中繼資料。</span><span class="sxs-lookup"><span data-stu-id="50a28-238">Enqueue() has the option of specifying additional metadata that will be passed to the consuming device.</span></span> <span data-ttu-id="50a28-239">中繼資料必須小於建立時已知的最大值。</span><span class="sxs-lookup"><span data-stu-id="50a28-239">The metadata must be less than a maximum known at creation time.</span></span>  
<span data-ttu-id="50a28-240">清除佇列 () 可以選擇性地傳遞緩衝區和緩衝區大小的指標。</span><span class="sxs-lookup"><span data-stu-id="50a28-240">Dequeue() can optionally pass a buffer and a pointer to the size of the buffer.</span></span> <span data-ttu-id="50a28-241">佇列會以對應的排入佇列呼叫的中繼資料填入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="50a28-241">The queue fills in the buffer with the metadata from the corresponding Enqueue call.</span></span>  
<span data-ttu-id="50a28-242">**複製**</span><span class="sxs-lookup"><span data-stu-id="50a28-242">**Cloning**</span></span>  
<span data-ttu-id="50a28-243">每個 ISurfaceQueue 物件都會解決單向同步處理。</span><span class="sxs-lookup"><span data-stu-id="50a28-243">Each ISurfaceQueue object solves a one-way synchronization.</span></span> <span data-ttu-id="50a28-244">我們假設大部分的應用程式使用此 API 都將使用封閉式系統。</span><span class="sxs-lookup"><span data-stu-id="50a28-244">We assume that the vast majority of applications using this API will use a closed system.</span></span> <span data-ttu-id="50a28-245">有兩個裝置來回傳送表面的最簡單關閉系統需要兩個佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-245">The simplest closed system with two devices sending surfaces back and forth requires two queues.</span></span> <span data-ttu-id="50a28-246">ISurfaceQueue 物件具有複製 () 方法，可讓您建立多個屬於相同較大管線的佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-246">The ISurfaceQueue object has a Clone() method to make it possible to create multiple queues that are all part of the same larger pipeline.</span></span>  
<span data-ttu-id="50a28-247">複製會從現有的 ISurfaceQueue 物件建立新的物件，並共用它們之間所有已開啟的資源。</span><span class="sxs-lookup"><span data-stu-id="50a28-247">Clone creates a new ISurfaceQueue object from an existing one, and shares all the opened resources between them.</span></span> <span data-ttu-id="50a28-248">產生的物件與來源佇列有完全相同的表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-248">The resulting object has exactly the same surfaces as the source queue.</span></span> <span data-ttu-id="50a28-249">複製的佇列可以有不同的中繼資料大小。</span><span class="sxs-lookup"><span data-stu-id="50a28-249">Cloned queues can have different metadata sizes from each other.</span></span>  
<span data-ttu-id="50a28-250">**表面**</span><span class="sxs-lookup"><span data-stu-id="50a28-250">**Surfaces**</span></span>  
<span data-ttu-id="50a28-251">ISurfaceQueue 會負責建立及管理其表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-251">The ISurfaceQueue takes responsibility for creating and managing its surfaces.</span></span> <span data-ttu-id="50a28-252">將任意表面排入佇列是不正確。</span><span class="sxs-lookup"><span data-stu-id="50a28-252">It is not valid to enqueue arbitrary surfaces.</span></span> <span data-ttu-id="50a28-253">此外，介面應該只有一個使用中的「擁有者」。</span><span class="sxs-lookup"><span data-stu-id="50a28-253">Furthermore, a surface should only have one active "owner."</span></span> <span data-ttu-id="50a28-254">它應該是在特定的佇列上，或是由特定裝置使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-254">It should either be on a specific queue or being used by a specific device.</span></span> <span data-ttu-id="50a28-255">在多個佇列上，或讓裝置在排入佇列之後仍繼續使用介面，是不正確。</span><span class="sxs-lookup"><span data-stu-id="50a28-255">It is not valid to have it on multiple queues or for devices to continue using the surface after it is enqueued.</span></span>  
</dl>

### <a name="api-details"></a><span data-ttu-id="50a28-256">API 詳細資料</span><span class="sxs-lookup"><span data-stu-id="50a28-256">API Details</span></span>

### <a name="isurfacequeue"></a><span data-ttu-id="50a28-257">IsurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="50a28-257">IsurfaceQueue</span></span>

<span data-ttu-id="50a28-258">佇列負責建立和維護共用資源。</span><span class="sxs-lookup"><span data-stu-id="50a28-258">The queue is responsible for creating and maintaining the shared resources.</span></span> <span data-ttu-id="50a28-259">它也提供使用 Clone 來連鎖多個佇列的功能。</span><span class="sxs-lookup"><span data-stu-id="50a28-259">It also provides the functionality to chain multiple queues using Clone.</span></span> <span data-ttu-id="50a28-260">佇列具有開啟產生裝置和取用裝置的方法。</span><span class="sxs-lookup"><span data-stu-id="50a28-260">The queue has methods that open the producing device and a consuming device.</span></span> <span data-ttu-id="50a28-261">每次只能開啟其中一個。</span><span class="sxs-lookup"><span data-stu-id="50a28-261">Only one of each can be opened at any time.</span></span>

<span data-ttu-id="50a28-262">佇列會公開下列 Api：</span><span class="sxs-lookup"><span data-stu-id="50a28-262">The queue exposes the following APIs:</span></span>



|                             |                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="50a28-263">CreateSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="50a28-263">CreateSurfaceQueue</span></span>          | <span data-ttu-id="50a28-264">建立 ISurfaceQueue 物件 ("root" 佇列) 。</span><span class="sxs-lookup"><span data-stu-id="50a28-264">Creates an ISurfaceQueue object (the "root" queue).</span></span>                              |
| <span data-ttu-id="50a28-265">ISurfaceQueue::OpenConsumer</span><span class="sxs-lookup"><span data-stu-id="50a28-265">ISurfaceQueue::OpenConsumer</span></span> | <span data-ttu-id="50a28-266">傳回取用裝置清除佇列的介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-266">Returns an interface for the consuming device to dequeue.</span></span>                        |
| <span data-ttu-id="50a28-267">ISurfaceQueue::OpenProducer</span><span class="sxs-lookup"><span data-stu-id="50a28-267">ISurfaceQueue::OpenProducer</span></span> | <span data-ttu-id="50a28-268">傳回產生裝置排入佇列的介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-268">Returns an interface for the producing device to enqueue.</span></span>                        |
| <span data-ttu-id="50a28-269">ISurfaceQueue：： Clone</span><span class="sxs-lookup"><span data-stu-id="50a28-269">ISurfaceQueue::Clone</span></span>        | <span data-ttu-id="50a28-270">建立 ISurfaceQueue 物件，該物件會與根佇列物件共用表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-270">Creates an ISurfaceQueue object that shares surfaces with the root queue object.</span></span> |



 

<span data-ttu-id="50a28-271">**CreateSurfaceQueue**</span><span class="sxs-lookup"><span data-stu-id="50a28-271">**CreateSurfaceQueue**</span></span>  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



<span data-ttu-id="50a28-272">**成員**</span><span class="sxs-lookup"><span data-stu-id="50a28-272">**Members**</span></span>  

<span data-ttu-id="50a28-273">**寬度**、 **高度**  ：共用表面的維度。</span><span class="sxs-lookup"><span data-stu-id="50a28-273">**Width**, **Height**  The dimensions of the shared surfaces.</span></span> <span data-ttu-id="50a28-274">所有共用的表面都必須有相同的維度。</span><span class="sxs-lookup"><span data-stu-id="50a28-274">All shared surfaces must have the same dimensions.</span></span>  
<span data-ttu-id="50a28-275">**格式** 共用表面的格式。</span><span class="sxs-lookup"><span data-stu-id="50a28-275">**Format** The format of the shared surfaces.</span></span> <span data-ttu-id="50a28-276">所有共用的表面都必須具有相同的格式。</span><span class="sxs-lookup"><span data-stu-id="50a28-276">All shared surfaces must have the same format.</span></span> <span data-ttu-id="50a28-277">有效的格式取決於將使用的裝置，因為不同的裝置配對可以共用不同的格式類型。</span><span class="sxs-lookup"><span data-stu-id="50a28-277">The valid formats depend on the devices that will be used, because different pairs of devices can share different format types.</span></span>  
<span data-ttu-id="50a28-278">**NumSurfaces**  屬於佇列一部分的表面數目。</span><span class="sxs-lookup"><span data-stu-id="50a28-278">**NumSurfaces**  The number of surfaces that are part of the queue.</span></span> <span data-ttu-id="50a28-279">這是固定的數位。</span><span class="sxs-lookup"><span data-stu-id="50a28-279">This is a fixed number.</span></span>  
 <span data-ttu-id="50a28-280">**MetaDataSize**  元資料緩衝區的大小上限。</span><span class="sxs-lookup"><span data-stu-id="50a28-280">**MetaDataSize**  The maximum size of the metadata buffer.</span></span>  
<span data-ttu-id="50a28-281">**旗標**  用來控制佇列行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="50a28-281">**Flags**  Flags to control the behavior of the queue.</span></span> <span data-ttu-id="50a28-282">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="50a28-282">See Remarks.</span></span>  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="50a28-283">**參數**</span><span class="sxs-lookup"><span data-stu-id="50a28-283">**Parameters**</span></span>

 <span data-ttu-id="50a28-284">*pDesc* \[在 \]  要建立之共用介面佇列的描述中。</span><span class="sxs-lookup"><span data-stu-id="50a28-284">*pDesc* \[in\]  The description of the shared surface queue to be created.</span></span>  

 <span data-ttu-id="50a28-285">*pDevice* \[\]應該用來建立共用表面的裝置。</span><span class="sxs-lookup"><span data-stu-id="50a28-285">*pDevice* \[in\]  The device that should be used to create the shared surfaces.</span></span> <span data-ttu-id="50a28-286">這是 Windows Vista 中的一項功能，因此是明確的參數。</span><span class="sxs-lookup"><span data-stu-id="50a28-286">This is an explicit parameter because of a feature in Windows Vista.</span></span> <span data-ttu-id="50a28-287">若為 Direct3D 9 與 Direct3D 10 之間共用的介面，則必須使用 Direct3D 9 來建立這些表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-287">For surfaces shared between Direct3D 9 and Direct3D 10, the surfaces must be created with Direct3D 9.</span></span>  

 <span data-ttu-id="50a28-288">*ppQueue* \[傳回 \]  時，包含 ISurfaceQueue 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="50a28-288">*ppQueue* \[out\]  On return, contains a pointer to the ISurfaceQueue object.</span></span>  


<span data-ttu-id="50a28-289">**傳回值**</span><span class="sxs-lookup"><span data-stu-id="50a28-289">**Return Values**</span></span>

<span data-ttu-id="50a28-290">如果 *pDevice* 無法共用資源，此函式會傳回 DXGI \_ 錯誤 \_ 不正確 \_ 呼叫。</span><span class="sxs-lookup"><span data-stu-id="50a28-290">If *pDevice* is not capable of sharing resources, this function returns DXGI\_ERROR\_INVALID\_CALL.</span></span> <span data-ttu-id="50a28-291">此函數會建立資源。</span><span class="sxs-lookup"><span data-stu-id="50a28-291">This function creates the resources.</span></span> <span data-ttu-id="50a28-292">如果失敗，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="50a28-292">If it fails, it returns an error.</span></span> <span data-ttu-id="50a28-293">如果成功，則會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="50a28-293">If it succeeds, it returns S\_OK.</span></span>

<span data-ttu-id="50a28-294">**備註**</span><span class="sxs-lookup"><span data-stu-id="50a28-294">**Remarks**</span></span>

<span data-ttu-id="50a28-295">建立佇列物件也會建立所有的表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-295">Creating the queue object also creates all of the surfaces.</span></span> <span data-ttu-id="50a28-296">所有表面都會假設為2D 轉譯目標，並會使用 D3D10 系結轉譯 \_ \_ \_ 目標和 D3D10 系結 \_ \_ 著色器 \_ 資源旗標設定 (或不同執行時間) 的相等旗標來建立。</span><span class="sxs-lookup"><span data-stu-id="50a28-296">All surfaces are assumed to be 2D render targets and will be created with the D3D10\_BIND\_RENDER\_TARGET and D3D10\_BIND\_SHADER\_RESOURCE flags set (or the equivalent flags for the different runtimes).</span></span>

<span data-ttu-id="50a28-297">開發人員可以指定旗標，以指出多個執行緒是否會存取佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-297">The developer can specify a flag that indicates whether the queue will be accessed by multiple threads.</span></span> <span data-ttu-id="50a28-298">如果未將旗標設定 (**旗標** = = 0) ，則佇列將會由多個執行緒使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-298">If no flags are set (**Flags** == 0), the queue will be used by multiple threads.</span></span> <span data-ttu-id="50a28-299">開發人員可以指定單一執行緒存取，以關閉同步處理常式代碼，並針對這些案例提供效能改進。</span><span class="sxs-lookup"><span data-stu-id="50a28-299">The developer can specify single threaded access, which turns off the synchronization code and provides a performance improvement for those cases.</span></span> <span data-ttu-id="50a28-300">每個複製的佇列都有自己的旗標，因此系統中的不同佇列可能會有不同的同步控制。</span><span class="sxs-lookup"><span data-stu-id="50a28-300">Each cloned queue has its own flag, so it is possible for different queues in the system to have different synchronization controls.</span></span>

 <span data-ttu-id="50a28-301">**開啟生產者**</span><span class="sxs-lookup"><span data-stu-id="50a28-301">**Open a Producer**</span></span>  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



<span data-ttu-id="50a28-302">**參數**</span><span class="sxs-lookup"><span data-stu-id="50a28-302">**Parameters**</span></span>  

<span data-ttu-id="50a28-303">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50a28-303">*pDevice* \[in\]</span></span>  

<span data-ttu-id="50a28-304">將顯示在介面佇列上的生產者裝置。</span><span class="sxs-lookup"><span data-stu-id="50a28-304">The producer device that enqueues surfaces onto the surface queue.</span></span> 

<span data-ttu-id="50a28-305">*ppProducer* \[out 會將 \] 物件傳回給生產者介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-305">*ppProducer* \[out\] Returns an object to the producer interface.</span></span>  


<span data-ttu-id="50a28-306">**傳回值**</span><span class="sxs-lookup"><span data-stu-id="50a28-306">**Return Values**</span></span>

<span data-ttu-id="50a28-307">如果裝置無法共用介面，會傳回 DXGI \_ 錯誤 \_ 不正確 \_ 呼叫。</span><span class="sxs-lookup"><span data-stu-id="50a28-307">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="50a28-308">**開啟取用者**</span><span class="sxs-lookup"><span data-stu-id="50a28-308">**Open a Consumer**</span></span>  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



<span data-ttu-id="50a28-309">**參數**</span><span class="sxs-lookup"><span data-stu-id="50a28-309">**Parameters**</span></span>  
 <span data-ttu-id="50a28-310">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50a28-310">*pDevice* \[in\]</span></span>  
 <span data-ttu-id="50a28-311">清除介面佇列表面的取用者裝置。</span><span class="sxs-lookup"><span data-stu-id="50a28-311">The consumer device that dequeues surfaces from the surface queue.</span></span> 
 <span data-ttu-id="50a28-312">*ppConsumer* \[out 會將 \]  物件傳回到取用者介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-312">*ppConsumer* \[out\]  Returns an object to the consumer interface.</span></span>  


<span data-ttu-id="50a28-313">**傳回值**</span><span class="sxs-lookup"><span data-stu-id="50a28-313">**Return Values**</span></span>

<span data-ttu-id="50a28-314">如果裝置無法共用介面，會傳回 DXGI \_ 錯誤 \_ 不正確 \_ 呼叫。</span><span class="sxs-lookup"><span data-stu-id="50a28-314">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="50a28-315">**備註**</span><span class="sxs-lookup"><span data-stu-id="50a28-315">**Remarks**</span></span>

<span data-ttu-id="50a28-316">此函式會開啟輸入裝置之佇列中的所有表面，並加以快取。</span><span class="sxs-lookup"><span data-stu-id="50a28-316">This function opens all of the surfaces in the queue for the input device and caches them.</span></span> <span data-ttu-id="50a28-317">後續的清除佇列呼叫會直接移至快取，而不需要每次重新開啟介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-317">Subsequent calls to Dequeue will simply go to the cache and not have to reopen the surfaces each time.</span></span>



### <a name="cloning-an-idxgixsurfacequeue"></a><span data-ttu-id="50a28-318">複製識別碼XGIXSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="50a28-318">Cloning an IDXGIXSurfaceQueue</span></span>




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



<span data-ttu-id="50a28-319">**成員** **MetaDataSize** 和 **旗標** 具有與 CreateSurfaceQueue 相同的行為。</span><span class="sxs-lookup"><span data-stu-id="50a28-319">**Members** **MetaDataSize** and **Flags** have the same behavior as they do for CreateSurfaceQueue.</span></span>  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="50a28-320">**參數**</span><span class="sxs-lookup"><span data-stu-id="50a28-320">**Parameters**</span></span>

<span data-ttu-id="50a28-321">*pDesc* \[在 \] 提供要建立之複製物件描述的結構中。</span><span class="sxs-lookup"><span data-stu-id="50a28-321">*pDesc* \[in\] A struct that provides a description of the Clone object to be created.</span></span> <span data-ttu-id="50a28-322">此參數應初始化。</span><span class="sxs-lookup"><span data-stu-id="50a28-322">This parameter should be initialized.</span></span>  
<span data-ttu-id="50a28-323">*ppQueue* \[out 會傳回 \] 初始化的物件。</span><span class="sxs-lookup"><span data-stu-id="50a28-323">*ppQueue* \[out\] Returns the initialized object.</span></span>  
</dl>

<span data-ttu-id="50a28-324">**備註**</span><span class="sxs-lookup"><span data-stu-id="50a28-324">**Remarks**</span></span>

<span data-ttu-id="50a28-325">您可以從任何現有的佇列物件進行複製（即使它不是根目錄）。</span><span class="sxs-lookup"><span data-stu-id="50a28-325">You can clone from any existing queue object, even if it is not the root.</span></span>  
</dl>

### <a name="idxgixsurfaceconsumer"></a><span data-ttu-id="50a28-326">IDXGIXSurfaceConsumer</span><span class="sxs-lookup"><span data-stu-id="50a28-326">IDXGIXSurfaceConsumer</span></span>

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



<span data-ttu-id="50a28-327">**參數**</span><span class="sxs-lookup"><span data-stu-id="50a28-327">**Parameters**</span></span>  
<span data-ttu-id="50a28-328"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="50a28-328">*id* \[in\]</span></span>  
<span data-ttu-id="50a28-329">使用中裝置之2D 介面的 REFIID。</span><span class="sxs-lookup"><span data-stu-id="50a28-329">The REFIID of a 2D surface of the consuming device.</span></span>  

-   <span data-ttu-id="50a28-330">若為 IDirect3DDevice9，REFIID 應該是 \_ \_ Uuidof (IDirect3DTexture9) 。</span><span class="sxs-lookup"><span data-stu-id="50a28-330">For a IDirect3DDevice9, the REFIID should be \_\_uuidof(IDirect3DTexture9).</span></span>
-   <span data-ttu-id="50a28-331">若為 ID3D10Device，REFIID 應該是 \_ \_ Uuidof (ID3D10Texture2D) 。</span><span class="sxs-lookup"><span data-stu-id="50a28-331">For a ID3D10Device, the REFIID should be \_\_uuidof(ID3D10Texture2D).</span></span>
-   <span data-ttu-id="50a28-332">若為 ID3D11Device，REFIID 應該是 \_ \_ Uuidof (ID3D11Texture2D) 。</span><span class="sxs-lookup"><span data-stu-id="50a28-332">For a ID3D11Device, the REFIID should be \_\_uuidof(ID3D11Texture2D).</span></span>

<span data-ttu-id="50a28-333">*ppSurface* \[out 會將 \] 指標傳回至介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-333">*ppSurface* \[out\] Returns a pointer to the surface.</span></span>  
<span data-ttu-id="50a28-334">*pBuffer* \[在中，out \] 選擇性的參數，如果不是 **Null**，則在傳回時，會包含在對應的佇列呼叫上傳入的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="50a28-334">*pBuffer* \[in, out\] An optional parameter and if not **NULL**, on return, contains the metadata that was passed in on the corresponding enqueue call.</span></span>  
<span data-ttu-id="50a28-335">*pBufferSize* \[在中， \] *pBuffer* 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="50a28-335">*pBufferSize* \[in, out\] The size of *pBuffer*, in bytes.</span></span> <span data-ttu-id="50a28-336">傳回 *pBuffer* 中傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="50a28-336">Returns the number of bytes returned in *pBuffer*.</span></span> <span data-ttu-id="50a28-337">如果排入佇列的呼叫未提供中繼資料，則 *pBuffer* 會設定為0。</span><span class="sxs-lookup"><span data-stu-id="50a28-337">If the enqueue call did not provide metadata, *pBuffer* is set to 0.</span></span>  
<span data-ttu-id="50a28-338">*dwTimeout* \[中的 \] 指定超時值。</span><span class="sxs-lookup"><span data-stu-id="50a28-338">*dwTimeout* \[in\] Specifies a timeout value.</span></span> <span data-ttu-id="50a28-339">如需詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="50a28-339">See the Remarks for more detail.</span></span>  
</dl>

<span data-ttu-id="50a28-340">**傳回值**</span><span class="sxs-lookup"><span data-stu-id="50a28-340">**Return Values**</span></span>

<span data-ttu-id="50a28-341">\_如果指定了超時值，且函式未在超時值之前傳回，此函式可能會傳回等候時間。</span><span class="sxs-lookup"><span data-stu-id="50a28-341">This function can return WAIT\_TIMEOUT if a timeout value is specified and the function does not return before the time out value.</span></span> <span data-ttu-id="50a28-342">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="50a28-342">See Remarks.</span></span> <span data-ttu-id="50a28-343">如果沒有可用的介面，則函式會傳回，並將 *ppSurface* 設定為 **Null**， *pBufferSize* 設定為0，且傳回值為 0X80070120 (WIN32 \_ 到 \_ HRESULT (等候 \_ 超時) ) 。</span><span class="sxs-lookup"><span data-stu-id="50a28-343">If no surfaces are available, the function returns with *ppSurface* set to **NULL**, *pBufferSize* set to 0 and the return value is 0x80070120 (WIN32\_TO\_HRESULT(WAIT\_TIMEOUT)).</span></span>  
</dl>

<span data-ttu-id="50a28-344">**備註**</span><span class="sxs-lookup"><span data-stu-id="50a28-344">**Remarks**</span></span>

<span data-ttu-id="50a28-345">如果佇列是空的，此 API 就會封鎖。</span><span class="sxs-lookup"><span data-stu-id="50a28-345">This API can block if the queue is empty.</span></span> <span data-ttu-id="50a28-346">*DwTimeout* 參數的運作方式與 Windows 同步處理 api 相同，例如 WaitForSingleObject。</span><span class="sxs-lookup"><span data-stu-id="50a28-346">The *dwTimeout* parameter works identically to the Windows synchronization APIs, such as WaitForSingleObject.</span></span> <span data-ttu-id="50a28-347">若為非封鎖的行為，請使用 timeout 0。</span><span class="sxs-lookup"><span data-stu-id="50a28-347">For non-blocking behavior, use a timeout of 0.</span></span>  
</dl>

### <a name="isurfaceproducer"></a><span data-ttu-id="50a28-348">ISurfaceProducer</span><span class="sxs-lookup"><span data-stu-id="50a28-348">ISurfaceProducer</span></span>

<span data-ttu-id="50a28-349">此介面提供兩種可讓應用程式排入佇列的方法。</span><span class="sxs-lookup"><span data-stu-id="50a28-349">This interface provides two methods that allow the app to enqueue surfaces.</span></span> <span data-ttu-id="50a28-350">將介面排入佇列之後，介面指標就不再有效，而且不安全地使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-350">After a surface is enqueued, the surface pointer is no longer valid and is not safe to use.</span></span> <span data-ttu-id="50a28-351">應用程式應該以指標執行的唯一動作是釋放它。</span><span class="sxs-lookup"><span data-stu-id="50a28-351">The only action that the application should perform with the pointer is to release it.</span></span>



|                           |                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a28-352">ISurfaceProducer：：排入佇列</span><span class="sxs-lookup"><span data-stu-id="50a28-352">ISurfaceProducer::Enqueue</span></span> | <span data-ttu-id="50a28-353">將至佇列物件的介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-353">Enqueues a surface to the queue object.</span></span> <span data-ttu-id="50a28-354">此呼叫完成之後，就會使用介面來完成產生者，並為其他裝置準備好表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-354">After this call completes, the producer is done with the surface and the surface is ready for another device.</span></span> |
| <span data-ttu-id="50a28-355">ISurfaceProducer：： Flush</span><span class="sxs-lookup"><span data-stu-id="50a28-355">ISurfaceProducer::Flush</span></span>   | <span data-ttu-id="50a28-356">如果應用程式應該有非封鎖的行為，則會使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-356">Used if the applications should have non-blocking behavior.</span></span> <span data-ttu-id="50a28-357">如需詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="50a28-357">See Remarks for details.</span></span>                                                                  |



 

<span data-ttu-id="50a28-358">**排入佇列**</span><span class="sxs-lookup"><span data-stu-id="50a28-358">**Enqueue**</span></span>  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



<span data-ttu-id="50a28-359">**參數**</span><span class="sxs-lookup"><span data-stu-id="50a28-359">**Parameters**</span></span>  
<span data-ttu-id="50a28-360">*pSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50a28-360">*pSurface* \[in\]</span></span>  
<span data-ttu-id="50a28-361">產生裝置的表面，需要排入佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-361">The surface of the producing device that needs to be enqueued.</span></span> <span data-ttu-id="50a28-362">此介面必須是來自相同佇列網路的佇列表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-362">This surface must be a dequeued surface from the same queue network.</span></span> <span data-ttu-id="50a28-363">*pBuffer* \[\]用於傳入中繼資料的選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="50a28-363">*pBuffer* \[in\] An optional parameter, which is used to pass in metadata.</span></span> <span data-ttu-id="50a28-364">它應該指向將會傳遞至清除佇列呼叫的資料。</span><span class="sxs-lookup"><span data-stu-id="50a28-364">It should point to the data that will be passed on to the dequeue call.</span></span>  
<span data-ttu-id="50a28-365">*BufferSize* \[以 \] 位元組為單位的 *pBuffer* 大小。</span><span class="sxs-lookup"><span data-stu-id="50a28-365">*BufferSize* \[in\] The size of *pBuffer*, in bytes.</span></span>  
<span data-ttu-id="50a28-366">*旗標* \[在 \] 控制此函數行為的選擇性參數中。</span><span class="sxs-lookup"><span data-stu-id="50a28-366">*Flags* \[in\] An optional parameter that controls the behavior of this function.</span></span> <span data-ttu-id="50a28-367">唯一的旗標是介面佇列旗標不會 \_ \_ \_ \_ \_ 等候。</span><span class="sxs-lookup"><span data-stu-id="50a28-367">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="50a28-368">請參閱 Flush 的備註。</span><span class="sxs-lookup"><span data-stu-id="50a28-368">See the Remarks for Flush.</span></span> <span data-ttu-id="50a28-369">如果未傳遞旗標 (*旗標* = = 0) ，則會使用預設的封鎖行為。</span><span class="sxs-lookup"><span data-stu-id="50a28-369">If no flag is passed (*Flags* == 0), then the default blocking behavior is used.</span></span>  
</dl>

<span data-ttu-id="50a28-370">**傳回值**</span><span class="sxs-lookup"><span data-stu-id="50a28-370">**Return Values**</span></span>

<span data-ttu-id="50a28-371">\_ \_ \_ \_ 如果 \_ 使用介面佇列 \_ 旗標 \_ \_ 不等候旗標 \_ ，則此函式會傳回 DXGI 錯誤仍在繪圖中。</span><span class="sxs-lookup"><span data-stu-id="50a28-371">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if a SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span>  
</dl>

<span data-ttu-id="50a28-372">**備註**</span><span class="sxs-lookup"><span data-stu-id="50a28-372">**Remarks**</span></span>

-   <span data-ttu-id="50a28-373">此函式會將介面放在佇列上。</span><span class="sxs-lookup"><span data-stu-id="50a28-373">This function puts the surface on the queue.</span></span> <span data-ttu-id="50a28-374">如果應用程式未指定 SURFACE \_ QUEUE \_ 旗標 \_ ，則此函 \_ 式會 \_ 封鎖並進行 GPU CPU 同步處理，以確保已排入佇列之介面上的所有轉譯都已完成。</span><span class="sxs-lookup"><span data-stu-id="50a28-374">If the application does not specify SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT, this function is blocking and will do a GPU-CPU synchronization to assure that all the rendering on the enqueued surface is complete.</span></span> <span data-ttu-id="50a28-375">如果此函式成功，則會有介面可供清除佇列使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-375">If this function succeeds, a surface will be available for dequeue.</span></span> <span data-ttu-id="50a28-376">如果您想要非封鎖的行為，請使用「請勿 \_ \_ 等候」旗標。</span><span class="sxs-lookup"><span data-stu-id="50a28-376">If you want non-blocking behavior, use the DO\_NOT\_WAIT flag.</span></span> <span data-ttu-id="50a28-377">如需詳細資訊，請參閱 Flush () 。</span><span class="sxs-lookup"><span data-stu-id="50a28-377">See Flush() for details.</span></span>
-   <span data-ttu-id="50a28-378">根據 COM 參考計數規則，清除佇列所傳回的介面會 AddRef () 因此應用程式不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="50a28-378">As per the COM reference counting rules, the surface returned by Dequeue will be AddRef() so the application does not need to do this.</span></span> <span data-ttu-id="50a28-379">呼叫排入佇列之後，應用程式必須釋放介面，因為它們不再使用它。</span><span class="sxs-lookup"><span data-stu-id="50a28-379">After calling Enqueue, the application must Release the surface because they are no longer using it.</span></span>

<span data-ttu-id="50a28-380">**清除**</span><span class="sxs-lookup"><span data-stu-id="50a28-380">**Flush**</span></span>  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



<span data-ttu-id="50a28-381">**參數**</span><span class="sxs-lookup"><span data-stu-id="50a28-381">**Parameters**</span></span>  
<span data-ttu-id="50a28-382">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="50a28-382">*Flags* \[in\]</span></span>  
<span data-ttu-id="50a28-383">唯一的旗標是介面佇列旗標不會 \_ \_ \_ \_ \_ 等候。</span><span class="sxs-lookup"><span data-stu-id="50a28-383">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="50a28-384">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="50a28-384">See Remarks.</span></span> <span data-ttu-id="50a28-385">*nSurfaces* \[out \] 會傳回仍在暫止且未排清的表面數目。</span><span class="sxs-lookup"><span data-stu-id="50a28-385">*nSurfaces* \[out\] Returns the number of surfaces that are still pending and not flushed.</span></span>  
</dl>

<span data-ttu-id="50a28-386">**傳回值**</span><span class="sxs-lookup"><span data-stu-id="50a28-386">**Return Values**</span></span>

<span data-ttu-id="50a28-387">\_ \_ \_ \_ 如果 \_ 使用介面佇列 \_ 旗標 \_ \_ 不等候 \_ 旗標，則此函式會傳回 DXGI 錯誤仍在繪圖中。</span><span class="sxs-lookup"><span data-stu-id="50a28-387">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if the SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span> <span data-ttu-id="50a28-388">如果成功排清任何介面，則此函式會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="50a28-388">This function returns S\_OK if any surfaces were successfully flushed.</span></span> <span data-ttu-id="50a28-389">只有未排清任何介面時，此函式才會傳回 DXGI \_ 錯誤 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="50a28-389">This function returns DXGI\_ERROR\_WAS\_STILL\_DRAWING only if no surfaces were flushed.</span></span> <span data-ttu-id="50a28-390">然後，傳回值和 *nSurfaces* 會向應用程式指出已完成的工作，以及是否有任何工作需要進行。</span><span class="sxs-lookup"><span data-stu-id="50a28-390">Together, the return value and *nSurfaces* indicate to the application what work has been done and if any work is left to do.</span></span>  
</dl>

<span data-ttu-id="50a28-391">**備註**</span><span class="sxs-lookup"><span data-stu-id="50a28-391">**Remarks**</span></span>

<span data-ttu-id="50a28-392">只有在先前對排入佇列的呼叫使用「請勿等候」旗標，否則排清才有意義 \_ \_ ; 否則，它將不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="50a28-392">Flush is meaningful only if the previous call to enqueue used the DO\_NOT\_WAIT flag; otherwise, it will be a no-op.</span></span> <span data-ttu-id="50a28-393">如果使用「請勿等候」旗標來呼叫排入佇列，則會立即傳回加入 \_ \_ 佇列，且不保證 GPU CPU 同步處理。</span><span class="sxs-lookup"><span data-stu-id="50a28-393">If the call to enqueue used the DO\_NOT\_WAIT flag, enqueue returns immediately and the GPU-CPU synchronization is not guaranteed.</span></span> <span data-ttu-id="50a28-394">介面仍會被視為已排入佇列、產生的裝置無法繼續使用，但無法供清除佇列使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-394">The surface is still considered enqueued, the producing device cannot continue using it, but it is not available for dequeue.</span></span> <span data-ttu-id="50a28-395">為了嘗試認可要清除佇列的介面，必須呼叫 Flush。</span><span class="sxs-lookup"><span data-stu-id="50a28-395">In order to try to commit the surface for dequeue, Flush must be called.</span></span> <span data-ttu-id="50a28-396">排清會嘗試認可目前排入佇列的所有表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-396">Flush attempts to commit all of the surfaces that are currently enqueued.</span></span> <span data-ttu-id="50a28-397">如果未將旗標傳遞至 Flush，它會封鎖並清除整個佇列，使其中的所有表面都能清除佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-397">If no flag is passed to Flush, it will block and clear out the entire queue, readying all surfaces in it for dequeue.</span></span> <span data-ttu-id="50a28-398">如果使用「 \_ 不 \_ 等候」旗標，則佇列會檢查介面，查看是否有任何這些介面就緒; 此步驟未封鎖。</span><span class="sxs-lookup"><span data-stu-id="50a28-398">If the DO\_NOT\_WAIT flag is used, the queue will check the surfaces to see if any of them are ready; this step is non-blocking.</span></span> <span data-ttu-id="50a28-399">已完成 GPU CPU 同步處理的表面，將可供取用者裝置使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-399">Surfaces that have finished the GPU-CPU sync will be ready for the consumer device.</span></span> <span data-ttu-id="50a28-400">仍在擱置中的表面不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="50a28-400">Surfaces that are still pending will be unaffected.</span></span> <span data-ttu-id="50a28-401">函數會傳回仍需要排清的表面數目。</span><span class="sxs-lookup"><span data-stu-id="50a28-401">The function returns the number of surfaces that still need to be flushed.</span></span>

> [!Note]  
> <span data-ttu-id="50a28-402">Flush 不會中斷佇列的語法。</span><span class="sxs-lookup"><span data-stu-id="50a28-402">Flush will not break the queue semantics.</span></span> <span data-ttu-id="50a28-403">API 可保證先排入佇列的介面會在稍後排入佇列的介面之前認可，而不論何時發生 GPU CPU 同步處理。</span><span class="sxs-lookup"><span data-stu-id="50a28-403">The API guarantees that surfaces enqueued first will be committed before surfaces enqueued later, regardless of when the GPU-CPU sync happens.</span></span>

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a><span data-ttu-id="50a28-404">Direct3D 9Ex 和 DXGI Interop Helper：如何使用</span><span class="sxs-lookup"><span data-stu-id="50a28-404">Direct3D 9Ex and DXGI Interop Helper: How To Use</span></span>

<span data-ttu-id="50a28-405">我們預期大部分的使用案例都牽涉到兩個裝置共用許多表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-405">We expect most of the usage cases to involve two devices sharing a number of surfaces.</span></span> <span data-ttu-id="50a28-406">因為這也是最簡單的案例，這份檔會詳細說明如何使用 Api 來達成此目標、討論非封鎖的變化，並以有關為三部裝置初始化的簡短章節結尾。</span><span class="sxs-lookup"><span data-stu-id="50a28-406">Because this also happens to be the simplest scenario, this paper details how to use the APIs to achieve this goal, discusses a non-blocking variation, and ends with a brief section about initializing for three devices.</span></span>

### <a name="two-devices"></a><span data-ttu-id="50a28-407">兩部裝置</span><span class="sxs-lookup"><span data-stu-id="50a28-407">Two Devices</span></span>

<span data-ttu-id="50a28-408">使用此 helper 的範例應用程式可以搭配使用 Direct3D 9Ex 和 Direct3D 11。</span><span class="sxs-lookup"><span data-stu-id="50a28-408">The example application that uses this helper can use Direct3D 9Ex and Direct3D 11 together.</span></span> <span data-ttu-id="50a28-409">應用程式可以處理這兩個裝置的內容，並使用 Direct3D 9 呈現內容。</span><span class="sxs-lookup"><span data-stu-id="50a28-409">The application can process content with both devices, and present content using Direct3D 9.</span></span> <span data-ttu-id="50a28-410">處理可能表示轉譯內容、解碼影片、執行計算著色器等等。</span><span class="sxs-lookup"><span data-stu-id="50a28-410">Processing could mean rendering content, decoding video, running compute shaders, and so on.</span></span> <span data-ttu-id="50a28-411">在每個框架中，應用程式會先使用 Direct3D 11 處理，然後使用 Direct3D 9 處理，最後再以 Direct3D 9 呈現。</span><span class="sxs-lookup"><span data-stu-id="50a28-411">For every frame, the application will first process with Direct3D 11, then process with Direct3D 9, and finally present with Direct3D 9.</span></span> <span data-ttu-id="50a28-412">此外，使用 Direct3D 11 的處理會產生一些中繼資料，而 Direct3D 9 所存在的中繼資料將需要使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-412">Furthermore, the processing with Direct3D 11 will produce some metadata that the Direct3D 9 present will need to consume.</span></span> <span data-ttu-id="50a28-413">本節涵蓋三個對應至此順序的元件中的協助程式使用方式：初始化、主要迴圈和清除。</span><span class="sxs-lookup"><span data-stu-id="50a28-413">This section covers the helper usage in three parts that correspond to this sequence: Initialization, Main Loop, and Cleanup.</span></span>

<span data-ttu-id="50a28-414">**初始 化**</span><span class="sxs-lookup"><span data-stu-id="50a28-414">**Initialization**</span></span>  
<span data-ttu-id="50a28-415">初始化牽涉到下列步驟：</span><span class="sxs-lookup"><span data-stu-id="50a28-415">Initialization involves the following steps:</span></span>  

1.  <span data-ttu-id="50a28-416">初始化這兩個裝置。</span><span class="sxs-lookup"><span data-stu-id="50a28-416">Initialize both devices.</span></span>
2.  <span data-ttu-id="50a28-417">建立根佇列： m \_ 11to9Queue。</span><span class="sxs-lookup"><span data-stu-id="50a28-417">Create the Root Queue: m\_11to9Queue.</span></span>
3.  <span data-ttu-id="50a28-418">從根佇列複製： m \_ 9to11Queue。</span><span class="sxs-lookup"><span data-stu-id="50a28-418">Clone from the Root Queue: m\_9to11Queue.</span></span>
4.  <span data-ttu-id="50a28-419">在兩個佇列上呼叫 OpenProducer/OpenConsumer。</span><span class="sxs-lookup"><span data-stu-id="50a28-419">Call OpenProducer/OpenConsumer on both queues.</span></span>

<span data-ttu-id="50a28-420">佇列名稱會使用數位9和11來指出哪個 API 是生產者，而後者是取用者： **m \_ ***生產者*** 至取用 ***者*** 佇列**。</span><span class="sxs-lookup"><span data-stu-id="50a28-420">The queue names use the numbers 9 and 11 to indicate which API is the producer and which is the consumer: **m\_\*\*\*producer**\* to ***consumer*** Queue\*\*.</span></span> <span data-ttu-id="50a28-421">因此，m \_ 11to9Queue 會指出 direct3d 11 裝置會產生 direct3d 9 裝置所用的表面所使用的佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-421">Accordingly, m\_11to9Queue indicates a queue for which the Direct3D 11 device produces surfaces that the Direct3D 9 device consumes.</span></span> <span data-ttu-id="50a28-422">同樣地，m \_ 9to11Queue 表示一種佇列，而 direct3d 9 會產生 direct3d 11 所耗用的表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-422">Similarly, m\_9to11Queue indicates a queue for which Direct3D 9 produces surfaces that Direct3D 11 consumes.</span></span>  
<span data-ttu-id="50a28-423">根佇列一開始是完整的，且所有複製的佇列一開始都是空的。</span><span class="sxs-lookup"><span data-stu-id="50a28-423">The Root queue is initially full and all cloned queues are initially empty.</span></span> <span data-ttu-id="50a28-424">這應該不會造成應用程式的問題，但將和清除的第一個週期和中繼資料的可用性除外。</span><span class="sxs-lookup"><span data-stu-id="50a28-424">This should not be a problem for the application except for the first cycle of the Enqueues and Dequeues and the availability of metadata.</span></span> <span data-ttu-id="50a28-425">如果清除佇列要求中繼資料，但未設定任何 (可能是因為一開始沒有任何專案，或排入佇列未設定任何) ，所以清除佇列看到未收到任何中繼資料。</span><span class="sxs-lookup"><span data-stu-id="50a28-425">If a dequeue asks for metadata but none was set (either because nothing is there initially or the enqueue did not set anything), dequeue sees that no metadata was received.</span></span>  

1.  <span data-ttu-id="50a28-426">**初始化這兩個裝置。**</span><span class="sxs-lookup"><span data-stu-id="50a28-426">**Initialize Both Devices.**</span></span>  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  <span data-ttu-id="50a28-427">**建立根佇列。**</span><span class="sxs-lookup"><span data-stu-id="50a28-427">**Create the Root Queue.**</span></span>  
    <span data-ttu-id="50a28-428">此步驟也會建立表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-428">This step also creates the surfaces.</span></span> <span data-ttu-id="50a28-429">大小和格式限制等同于建立任何共用資源。</span><span class="sxs-lookup"><span data-stu-id="50a28-429">Size and format restrictions are identical to creating any shared resource.</span></span> <span data-ttu-id="50a28-430">元資料緩衝區的大小是在建立時固定的，在此情況下，我們只會傳遞 UINT。</span><span class="sxs-lookup"><span data-stu-id="50a28-430">The size of the metadata buffer is fixed at create time, and in this case, we'll just be passing a UINT.</span></span>  
    <span data-ttu-id="50a28-431">您必須使用固定的介面數目來建立佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-431">The queue must be created with a fixed number of surfaces.</span></span> <span data-ttu-id="50a28-432">效能將視案例而異。</span><span class="sxs-lookup"><span data-stu-id="50a28-432">Performance will vary depending on the scenario.</span></span> <span data-ttu-id="50a28-433">擁有多個表面可增加裝置忙碌的機會。</span><span class="sxs-lookup"><span data-stu-id="50a28-433">Having multiple surfaces increases the chances that devices are busy.</span></span> <span data-ttu-id="50a28-434">例如，如果只有一個介面，則這兩個裝置之間將不會有平行處理。</span><span class="sxs-lookup"><span data-stu-id="50a28-434">For example, if there is only one surface, then there will be no parallelization between the two devices.</span></span> <span data-ttu-id="50a28-435">另一方面，增加介面數量會增加記憶體使用量，這可能會降低效能。</span><span class="sxs-lookup"><span data-stu-id="50a28-435">On the other hand, increasing the number of surfaces increases the memory footprint, which can degrade performance.</span></span> <span data-ttu-id="50a28-436">此範例使用兩個表面。</span><span class="sxs-lookup"><span data-stu-id="50a28-436">This example uses two surfaces.</span></span>  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  <span data-ttu-id="50a28-437">**複製根佇列。**</span><span class="sxs-lookup"><span data-stu-id="50a28-437">**Clone the Root Queue.**</span></span>  
    <span data-ttu-id="50a28-438">每個複製的佇列都必須使用相同的表面，但可以有不同的元資料緩衝區大小和不同的旗標。</span><span class="sxs-lookup"><span data-stu-id="50a28-438">Each cloned queue must use the same surfaces but can have different metadata buffer sizes and different flags.</span></span> <span data-ttu-id="50a28-439">在此情況下，沒有從 Direct3D 9 到 Direct3D 11 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="50a28-439">In this case, there is no metadata from Direct3D 9 to Direct3D 11.</span></span>  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  <span data-ttu-id="50a28-440">**開啟生產者和取用者裝置。**</span><span class="sxs-lookup"><span data-stu-id="50a28-440">**Open the Producer and Consumer Devices.**</span></span>  
    <span data-ttu-id="50a28-441">應用程式必須在呼叫排入佇列和清除佇列之前執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="50a28-441">The application must perform this step before calling Enqueue and Dequeue.</span></span> <span data-ttu-id="50a28-442">開啟生產者和取用者會傳回包含排入佇列/清除佇列 Api 的介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-442">Opening a producer and consumer returns interfaces which contain the enqueue/dequeue APIs.</span></span>  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

<span data-ttu-id="50a28-443">**Main 迴圈**</span><span class="sxs-lookup"><span data-stu-id="50a28-443">**Main Loop**</span></span>  
<span data-ttu-id="50a28-444">佇列的使用方式是在傳統生產者/取用者問題之後進行模型化。</span><span class="sxs-lookup"><span data-stu-id="50a28-444">The usage of the queue is modeled after the classical producer/consumer problem.</span></span> <span data-ttu-id="50a28-445">請從每個裝置的觀點來思考這一點。</span><span class="sxs-lookup"><span data-stu-id="50a28-445">Think of this from a per-device perspective.</span></span> <span data-ttu-id="50a28-446">每個裝置都必須執行下列步驟：清除佇列以從其取用佇列中取得介面、在介面上處理，然後將其加入至其產生佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-446">Each device must perform these steps: dequeue to get a surface from its consuming queue, process on the surface, and then enqueue onto its producing queue.</span></span> <span data-ttu-id="50a28-447">針對 Direct3D 11 裝置，Direct3D 9 的使用方式幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="50a28-447">For the Direct3D 11 device, the Direct3D 9 usage is almost identical.</span></span>  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



<span data-ttu-id="50a28-448">**清除**</span><span class="sxs-lookup"><span data-stu-id="50a28-448">**Cleaning Up**</span></span>  
<span data-ttu-id="50a28-449">此步驟非常簡單。</span><span class="sxs-lookup"><span data-stu-id="50a28-449">This step is very straightforward.</span></span> <span data-ttu-id="50a28-450">除了清除 Direct3D Api 的一般步驟之外，應用程式也必須釋放傳回的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="50a28-450">In addition to the normal steps for cleaning up Direct3D APIs, the application must release the return COM interfaces.</span></span>  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a><span data-ttu-id="50a28-451">非封鎖使用</span><span class="sxs-lookup"><span data-stu-id="50a28-451">Non-Blocking Use</span></span>

<span data-ttu-id="50a28-452">上述範例適用于多執行緒使用案例，其中每個裝置都有自己的執行緒。</span><span class="sxs-lookup"><span data-stu-id="50a28-452">The previous example makes sense for a multithreaded usage case in which each device has its own thread.</span></span> <span data-ttu-id="50a28-453">此範例會使用 Api 的封鎖版本：無限的超時時間，而且沒有任何要排入佇列的旗標。</span><span class="sxs-lookup"><span data-stu-id="50a28-453">The example uses the blocking versions of the APIs: INFINITE for timeout, and no flag to enqueue.</span></span> <span data-ttu-id="50a28-454">如果您想要以非封鎖方式使用協助程式，則只需要進行一些變更。</span><span class="sxs-lookup"><span data-stu-id="50a28-454">If you want to use the helper in a non-blocking way, you need to make only a few changes.</span></span> <span data-ttu-id="50a28-455">本節顯示在一個執行緒上，對這兩個裝置的非封鎖使用。</span><span class="sxs-lookup"><span data-stu-id="50a28-455">This section shows non-blocking use with both devices on one thread.</span></span>

<span data-ttu-id="50a28-456">**初始 化**</span><span class="sxs-lookup"><span data-stu-id="50a28-456">**Initialization**</span></span>  
<span data-ttu-id="50a28-457">除了旗標以外，初始化也相同。</span><span class="sxs-lookup"><span data-stu-id="50a28-457">Initialization is identical except for the flags.</span></span> <span data-ttu-id="50a28-458">因為應用程式是單一執行緒，所以請使用該旗標來建立。</span><span class="sxs-lookup"><span data-stu-id="50a28-458">Because the application is single-threaded, use that flag for creation.</span></span> <span data-ttu-id="50a28-459">這會關閉部分同步處理常式代碼，這可能會改善效能。</span><span class="sxs-lookup"><span data-stu-id="50a28-459">This turns off some of the synchronization code, which potentially improves performance.</span></span>  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



<span data-ttu-id="50a28-460">開啟生產者和取用者裝置與封鎖範例中的相同。</span><span class="sxs-lookup"><span data-stu-id="50a28-460">Opening the producer and consumer devices are the same as in the blocking example.</span></span>  
<span data-ttu-id="50a28-461">**使用佇列**</span><span class="sxs-lookup"><span data-stu-id="50a28-461">**Using the Queue**</span></span>  
<span data-ttu-id="50a28-462">有許多方式可以非封鎖的方式使用佇列的各種效能特性。</span><span class="sxs-lookup"><span data-stu-id="50a28-462">There are many ways of using the queue in a non-blocking fashion with various performance characteristics.</span></span> <span data-ttu-id="50a28-463">下列範例很簡單，但由於過度旋轉和輪詢而效能不佳。</span><span class="sxs-lookup"><span data-stu-id="50a28-463">The following example is simple but has poor performance due to excessive spinning and polling.</span></span> <span data-ttu-id="50a28-464">儘管有這些問題，此範例也會示範如何使用 helper。</span><span class="sxs-lookup"><span data-stu-id="50a28-464">Despite these problems, the example shows how to use the helper.</span></span> <span data-ttu-id="50a28-465">方法是不斷地坐在迴圈和清除佇列、處理、排入佇列和排清。</span><span class="sxs-lookup"><span data-stu-id="50a28-465">The approach is to constantly sit in a loop and dequeue, process, enqueue, and flush.</span></span> <span data-ttu-id="50a28-466">如果有任何步驟因為無法使用資源而失敗，應用程式只會再次嘗試下一個迴圈。</span><span class="sxs-lookup"><span data-stu-id="50a28-466">If any of the steps fail because the resource is not available, the application simply tries again the next loop.</span></span>  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



<span data-ttu-id="50a28-467">比較複雜的解決方案可以從排入佇列和排清檢查傳回值，以判斷是否需要進行清除。</span><span class="sxs-lookup"><span data-stu-id="50a28-467">A more complex solution could check the return value from enqueue and from flush to determine if flushing is necessary.</span></span>  
</dl>

### <a name="three-devices"></a><span data-ttu-id="50a28-468">三個裝置</span><span class="sxs-lookup"><span data-stu-id="50a28-468">Three Devices</span></span>

<span data-ttu-id="50a28-469">擴充先前的範例以涵蓋多個裝置很簡單。</span><span class="sxs-lookup"><span data-stu-id="50a28-469">Extending the previous examples to cover multiple devices is straightforward.</span></span> <span data-ttu-id="50a28-470">下列程式碼會執行初始化。</span><span class="sxs-lookup"><span data-stu-id="50a28-470">The following code performs the initialization.</span></span> <span data-ttu-id="50a28-471">建立生產者/取用者物件之後，使用它們的程式碼就會相同。</span><span class="sxs-lookup"><span data-stu-id="50a28-471">After the Producer/Consumer objects have been created, the code to use them is the same.</span></span> <span data-ttu-id="50a28-472">此範例有三個裝置，因此有三個佇列。</span><span class="sxs-lookup"><span data-stu-id="50a28-472">This example has three devices and therefore three queues.</span></span> <span data-ttu-id="50a28-473">介面從 Direct3D 9 流至 Direct3D 10 到 Direct3D 11。</span><span class="sxs-lookup"><span data-stu-id="50a28-473">Surfaces flow from Direct3D 9 to Direct3D 10 to Direct3D 11.</span></span>


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



<span data-ttu-id="50a28-474">如先前所述，無論複製何種佇列，複製的運作方式都相同。</span><span class="sxs-lookup"><span data-stu-id="50a28-474">As mentioned earlier, cloning works the same way, no matter which queue is cloned.</span></span> <span data-ttu-id="50a28-475">例如，第二個複製呼叫可能已關閉 m \_ 9to10Queue 物件。</span><span class="sxs-lookup"><span data-stu-id="50a28-475">For example, the second Clone call could have been off of the m\_9to10Queue object.</span></span>


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a><span data-ttu-id="50a28-476">結論</span><span class="sxs-lookup"><span data-stu-id="50a28-476">Conclusion</span></span>

<span data-ttu-id="50a28-477">您可以建立使用互通性的解決方案，運用多個 DirectX Api 的強大功能。</span><span class="sxs-lookup"><span data-stu-id="50a28-477">You can create solutions that use interoperability to employ the power of multiple DirectX APIs.</span></span> <span data-ttu-id="50a28-478">Windows 圖形 API 互通性現在提供通用的 surface management runtime DXGI 1.1。</span><span class="sxs-lookup"><span data-stu-id="50a28-478">Windows graphics API interoperability now offers a common surface management runtime DXGI 1.1.</span></span> <span data-ttu-id="50a28-479">此執行時間可在新開發的 Api （例如 Direct3D 11、Direct3D 10.1 和 Direct2D）內啟用同步表面共用支援。</span><span class="sxs-lookup"><span data-stu-id="50a28-479">This runtime enables synchronized surface sharing support within newly developed APIs, such as Direct3D 11, Direct3D 10.1 and Direct2D.</span></span> <span data-ttu-id="50a28-480">新 Api 與現有 Api 之間的互通性改善有助於應用程式遷移和回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="50a28-480">Interoperability improvements between new APIs and existing APIs aid application migration and backward compatibility.</span></span> <span data-ttu-id="50a28-481">Direct3D 9Ex 和 DXGI 1.1 取用者 Api 可以交互操作，如透過 MSDN 程式碼庫中的範例 helper 程式碼提供的同步處理機制所示。</span><span class="sxs-lookup"><span data-stu-id="50a28-481">Direct3D 9Ex and DXGI 1.1 consumer APIs can interoperate, as shown with the synchronization mechanism provided through sample helper code on MSDN Code Gallery.</span></span>

 

 