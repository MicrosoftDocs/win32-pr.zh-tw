---
description: Microsoft DirectX Graphic Infrastructure (DXGI) 1.2 新增了下列功能。
ms.assetid: E2D8DA99-4EA2-4847-B699-80A6994C66C0
title: DXGI 1.2 改善
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd274918d179bc7adeb8dd132fe604cf56d80f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971274"
---
# <a name="dxgi-12-improvements"></a><span data-ttu-id="18f65-103">DXGI 1.2 改善</span><span class="sxs-lookup"><span data-stu-id="18f65-103">DXGI 1.2 improvements</span></span>

<span data-ttu-id="18f65-104">Microsoft DirectX Graphic Infrastructure (DXGI) 1.2 新增了下列功能。</span><span class="sxs-lookup"><span data-stu-id="18f65-104">The following functionality has been added in Microsoft DirectX Graphics Infrastructure (DXGI) 1.2.</span></span>

## <a name="presentation-enhancements-and-optimizations"></a><span data-ttu-id="18f65-105">簡報增強功能和優化</span><span class="sxs-lookup"><span data-stu-id="18f65-105">Presentation enhancements and optimizations</span></span>

<span data-ttu-id="18f65-106">DXGI 1.2 利用新的翻轉模型交換鏈、內容保護、無視窗的呈現方式，以及您在其中指定已變更矩形和捲動區域的優化簡報，來增強展示。</span><span class="sxs-lookup"><span data-stu-id="18f65-106">DXGI 1.2 enhances presentation with a new flip-model swap chain, content protection, windowless presentation, and optimized presentation wherein you specify dirty rectangles and scrolled areas.</span></span> <span data-ttu-id="18f65-107">簡報也增強了 stereoscopic 3D 顯示器行為。</span><span class="sxs-lookup"><span data-stu-id="18f65-107">Presentation is also enhanced with stereoscopic 3D display behavior.</span></span>

<span data-ttu-id="18f65-108">您可以使用下列 DXGI 1.2 API 來增強簡報。</span><span class="sxs-lookup"><span data-stu-id="18f65-108">You can use the following DXGI 1.2 API for enhanced presentation.</span></span>

-   [<span data-ttu-id="18f65-109">**IDXGIDisplayControl::IsStereoEnabled**</span><span class="sxs-lookup"><span data-stu-id="18f65-109">**IDXGIDisplayControl::IsStereoEnabled**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled)
-   [<span data-ttu-id="18f65-110">**IDXGIDisplayControl::SetStereoEnabled**</span><span class="sxs-lookup"><span data-stu-id="18f65-110">**IDXGIDisplayControl::SetStereoEnabled**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled)
-   [<span data-ttu-id="18f65-111">**IDXGIFactory2::CreateSwapChainForHwnd**</span><span class="sxs-lookup"><span data-stu-id="18f65-111">**IDXGIFactory2::CreateSwapChainForHwnd**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)
-   [<span data-ttu-id="18f65-112">**IDXGIFactory2::CreateSwapChainForCoreWindow**</span><span class="sxs-lookup"><span data-stu-id="18f65-112">**IDXGIFactory2::CreateSwapChainForCoreWindow**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
-   [<span data-ttu-id="18f65-113">**IDXGIFactory2::CreateSwapChainForComposition**</span><span class="sxs-lookup"><span data-stu-id="18f65-113">**IDXGIFactory2::CreateSwapChainForComposition**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
-   [<span data-ttu-id="18f65-114">**IDXGIFactory2::IsWindowedStereoEnabled**</span><span class="sxs-lookup"><span data-stu-id="18f65-114">**IDXGIFactory2::IsWindowedStereoEnabled**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)
-   [<span data-ttu-id="18f65-115">**IDXGIFactory2::RegisterStereoStatusWindow**</span><span class="sxs-lookup"><span data-stu-id="18f65-115">**IDXGIFactory2::RegisterStereoStatusWindow**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
-   [<span data-ttu-id="18f65-116">**IDXGIFactory2::RegisterStereoStatusEvent**</span><span class="sxs-lookup"><span data-stu-id="18f65-116">**IDXGIFactory2::RegisterStereoStatusEvent**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
-   [<span data-ttu-id="18f65-117">**IDXGIFactory2::UnregisterStereoStatus**</span><span class="sxs-lookup"><span data-stu-id="18f65-117">**IDXGIFactory2::UnregisterStereoStatus**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
-   [<span data-ttu-id="18f65-118">**IDXGIFactory2::RegisterOcclusionStatusWindow**</span><span class="sxs-lookup"><span data-stu-id="18f65-118">**IDXGIFactory2::RegisterOcclusionStatusWindow**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
-   [<span data-ttu-id="18f65-119">**IDXGIFactory2::RegisterOcclusionStatusEvent**</span><span class="sxs-lookup"><span data-stu-id="18f65-119">**IDXGIFactory2::RegisterOcclusionStatusEvent**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
-   [<span data-ttu-id="18f65-120">**IDXGIFactory2::UnregisterOcclusionStatus**</span><span class="sxs-lookup"><span data-stu-id="18f65-120">**IDXGIFactory2::UnregisterOcclusionStatus**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
-   [<span data-ttu-id="18f65-121">**IDXGIOutput1::GetDisplayModeList1**</span><span class="sxs-lookup"><span data-stu-id="18f65-121">**IDXGIOutput1::GetDisplayModeList1**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)
-   [<span data-ttu-id="18f65-122">**IDXGIOutput1::GetDisplaySurfaceData1**</span><span class="sxs-lookup"><span data-stu-id="18f65-122">**IDXGIOutput1::GetDisplaySurfaceData1**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1)
-   [<span data-ttu-id="18f65-123">**IDXGIOutput1::FindClosestMatchingMode1**</span><span class="sxs-lookup"><span data-stu-id="18f65-123">**IDXGIOutput1::FindClosestMatchingMode1**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1)
-   [<span data-ttu-id="18f65-124">**IDXGIResource1::CreateSubresourceSurface**</span><span class="sxs-lookup"><span data-stu-id="18f65-124">**IDXGIResource1::CreateSubresourceSurface**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface)
-   [<span data-ttu-id="18f65-125">**IDXGISurface2::GetResource**</span><span class="sxs-lookup"><span data-stu-id="18f65-125">**IDXGISurface2::GetResource**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgisurface2-getresource)
-   [<span data-ttu-id="18f65-126">**IDXGISwapChain1::GetDesc1**</span><span class="sxs-lookup"><span data-stu-id="18f65-126">**IDXGISwapChain1::GetDesc1**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1)
-   [<span data-ttu-id="18f65-127">**IDXGISwapChain1::GetFullscreenDesc**</span><span class="sxs-lookup"><span data-stu-id="18f65-127">**IDXGISwapChain1::GetFullscreenDesc**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc)
-   [<span data-ttu-id="18f65-128">**IDXGISwapChain1::GetHwnd**</span><span class="sxs-lookup"><span data-stu-id="18f65-128">**IDXGISwapChain1::GetHwnd**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd)
-   [<span data-ttu-id="18f65-129">**IDXGISwapChain1::GetCoreWindow**</span><span class="sxs-lookup"><span data-stu-id="18f65-129">**IDXGISwapChain1::GetCoreWindow**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
-   [<span data-ttu-id="18f65-130">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="18f65-130">**IDXGISwapChain1::Present1**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [<span data-ttu-id="18f65-131">**IDXGISwapChain1::IsTemporaryMonoSupported**</span><span class="sxs-lookup"><span data-stu-id="18f65-131">**IDXGISwapChain1::IsTemporaryMonoSupported**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported)
-   [<span data-ttu-id="18f65-132">**IDXGISwapChain1::GetRestrictToOutput**</span><span class="sxs-lookup"><span data-stu-id="18f65-132">**IDXGISwapChain1::GetRestrictToOutput**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrestricttooutput)
-   [<span data-ttu-id="18f65-133">**IDXGISwapChain1::SetBackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="18f65-133">**IDXGISwapChain1::SetBackgroundColor**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)
-   [<span data-ttu-id="18f65-134">**IDXGISwapChain1::GetBackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="18f65-134">**IDXGISwapChain1::GetBackgroundColor**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)
-   [<span data-ttu-id="18f65-135">**IDXGISwapChain1::SetRotation**</span><span class="sxs-lookup"><span data-stu-id="18f65-135">**IDXGISwapChain1::SetRotation**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
-   [<span data-ttu-id="18f65-136">**IDXGISwapChain1::GetRotation**</span><span class="sxs-lookup"><span data-stu-id="18f65-136">**IDXGISwapChain1::GetRotation**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)

<span data-ttu-id="18f65-137">如需如何使用 DXGI 1.2 API 以增強簡報的詳細資訊，請參閱 [使用翻轉模型、中途矩形和捲動區域增強簡報](dxgi-1-2-presentation-improvements.md)。</span><span class="sxs-lookup"><span data-stu-id="18f65-137">For more info about how to use the DXGI 1.2 API for enhanced presentation, see [Enhancing presentation with the flip model, dirty rectangles, and scrolled areas](dxgi-1-2-presentation-improvements.md).</span></span>

<span data-ttu-id="18f65-138">如需如何判斷您是否可以在身歷聲中轉譯的詳細資訊，請參閱 [以身歷聲呈現的資料，並通知身歷聲狀態](stereo-rendering-stereo-status-notifying.md)。</span><span class="sxs-lookup"><span data-stu-id="18f65-138">For info about how to determine whether you can render in stereo, see [Rendering in stereo and notifying about stereo status](stereo-rendering-stereo-status-notifying.md).</span></span>

<span data-ttu-id="18f65-139">如需如何判斷應用程式遮蔽狀態變更的資訊，請參閱不 [需要在轉譯時等候事件](waiting-when-occluded.md)。</span><span class="sxs-lookup"><span data-stu-id="18f65-139">For info about how to determine changes in your app's occlusion status, see [Waiting on an event when rendering is unnecessary](waiting-when-occluded.md).</span></span>

<span data-ttu-id="18f65-140">如需有關在螢幕上顯示內容時資料值如何變更的資訊，請參閱 [轉換色彩空間的資料](converting-data-color-space.md)。</span><span class="sxs-lookup"><span data-stu-id="18f65-140">For info about how data values change when you present content to the screen, see [Converting data for the color space](converting-data-color-space.md).</span></span>

## <a name="desktop-duplication"></a><span data-ttu-id="18f65-141">桌面複製</span><span class="sxs-lookup"><span data-stu-id="18f65-141">Desktop duplication</span></span>

<span data-ttu-id="18f65-142">Windows 8 停用標準 Windows 2000 顯示驅動程式模型 (XDDM) 鏡像驅動程式。</span><span class="sxs-lookup"><span data-stu-id="18f65-142">Windows 8 disables standard Windows 2000 Display Driver Model (XDDM) mirror drivers.</span></span> <span data-ttu-id="18f65-143">DXGI 1.2 提供桌面複製 API 作為替代方案。</span><span class="sxs-lookup"><span data-stu-id="18f65-143">DXGI 1.2 provides the desktop duplication API as an alternative.</span></span> <span data-ttu-id="18f65-144">桌面複製 API 可讓您從遠端存取桌面映射以進行共同作業案例。</span><span class="sxs-lookup"><span data-stu-id="18f65-144">The desktop duplication API provides remote access to the desktop image for collaboration scenarios.</span></span>

<span data-ttu-id="18f65-145">桌面複製 API 包含下列方法。</span><span class="sxs-lookup"><span data-stu-id="18f65-145">The desktop duplication API consists of the following methods.</span></span>

-   [<span data-ttu-id="18f65-146">**IDXGIOutput1：:D uplicateOutput**</span><span class="sxs-lookup"><span data-stu-id="18f65-146">**IDXGIOutput1::DuplicateOutput**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
-   [<span data-ttu-id="18f65-147">**IDXGIOutputDuplication::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="18f65-147">**IDXGIOutputDuplication::GetDesc**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getdesc)
-   [<span data-ttu-id="18f65-148">**IDXGIOutputDuplication::AcquireNextFrame**</span><span class="sxs-lookup"><span data-stu-id="18f65-148">**IDXGIOutputDuplication::AcquireNextFrame**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)
-   [<span data-ttu-id="18f65-149">**IDXGIOutputDuplication::GetFrameDirtyRects**</span><span class="sxs-lookup"><span data-stu-id="18f65-149">**IDXGIOutputDuplication::GetFrameDirtyRects**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects)
-   [<span data-ttu-id="18f65-150">**IDXGIOutputDuplication::GetFrameMoveRects**</span><span class="sxs-lookup"><span data-stu-id="18f65-150">**IDXGIOutputDuplication::GetFrameMoveRects**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects)
-   [<span data-ttu-id="18f65-151">**IDXGIOutputDuplication::GetFramePointerShape**</span><span class="sxs-lookup"><span data-stu-id="18f65-151">**IDXGIOutputDuplication::GetFramePointerShape**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape)
-   [<span data-ttu-id="18f65-152">**IDXGIOutputDuplication::MapDesktopSurface**</span><span class="sxs-lookup"><span data-stu-id="18f65-152">**IDXGIOutputDuplication::MapDesktopSurface**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface)
-   [<span data-ttu-id="18f65-153">**IDXGIOutputDuplication::UnMapDesktopSurface**</span><span class="sxs-lookup"><span data-stu-id="18f65-153">**IDXGIOutputDuplication::UnMapDesktopSurface**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface)
-   [<span data-ttu-id="18f65-154">**IDXGIOutputDuplication::ReleaseFrame**</span><span class="sxs-lookup"><span data-stu-id="18f65-154">**IDXGIOutputDuplication::ReleaseFrame**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-releaseframe)

<span data-ttu-id="18f65-155">如需如何使用桌面複製 API 的詳細資訊，請參閱 [桌面複製 api](desktop-dup-api.md)。</span><span class="sxs-lookup"><span data-stu-id="18f65-155">For more info about how to use the desktop duplication API, see [Desktop Duplication API](desktop-dup-api.md).</span></span>

## <a name="improved-usage-of-shared-resources-and-synchronized-events"></a><span data-ttu-id="18f65-156">改善共用資源的使用和已同步處理的事件</span><span class="sxs-lookup"><span data-stu-id="18f65-156">Improved usage of shared resources and synchronized events</span></span>

<span data-ttu-id="18f65-157">在舊版的 Windows 中，應用程式會使用連續輪詢來判斷圖形處理單元 (GPU) 是否已完成處理任意命令。</span><span class="sxs-lookup"><span data-stu-id="18f65-157">In previous versions of Windows, apps use continuous polling to determine whether the graphics processing unit (GPU) is finished processing arbitrary commands.</span></span> <span data-ttu-id="18f65-158">DXGI 1.2 可讓應用程式將事件佇列至 DXGI 裝置。</span><span class="sxs-lookup"><span data-stu-id="18f65-158">DXGI 1.2 enables an app to queue an event to a DXGI device.</span></span> <span data-ttu-id="18f65-159">然後，應用程式可以等待 DXGI 裝置通知事件，以判斷 GPU 已完成執行所有轉譯命令。</span><span class="sxs-lookup"><span data-stu-id="18f65-159">The app can then wait for the DXGI device to signal the event to determine that the GPU finished executing all rendering commands.</span></span> <span data-ttu-id="18f65-160">DXGI 1.2 可讓多個裝置透過 NT 控制碼共用資源。</span><span class="sxs-lookup"><span data-stu-id="18f65-160">DXGI 1.2 enables multiple devices to share a resource through a NT handle.</span></span>

<span data-ttu-id="18f65-161">您可以使用下列 DXGI 1.2 API 和 Direct3D 11.1 API 來共用資源和同步處理事件。</span><span class="sxs-lookup"><span data-stu-id="18f65-161">You can use the following DXGI 1.2 API and Direct3D 11.1 API to share resources and synchronize events.</span></span>

-   [<span data-ttu-id="18f65-162">**IDXGIDevice2::EnqueueSetEvent**</span><span class="sxs-lookup"><span data-stu-id="18f65-162">**IDXGIDevice2::EnqueueSetEvent**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
-   [<span data-ttu-id="18f65-163">**IDXGIResource1::CreateSharedHandle**</span><span class="sxs-lookup"><span data-stu-id="18f65-163">**IDXGIResource1::CreateSharedHandle**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
-   [<span data-ttu-id="18f65-164">**IDXGIFactory2::GetSharedResourceAdapterLuid**</span><span class="sxs-lookup"><span data-stu-id="18f65-164">**IDXGIFactory2::GetSharedResourceAdapterLuid**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
-   [<span data-ttu-id="18f65-165">**ID3D11Device1::OpenSharedResource1**</span><span class="sxs-lookup"><span data-stu-id="18f65-165">**ID3D11Device1::OpenSharedResource1**</span></span>](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
-   [<span data-ttu-id="18f65-166">**ID3D11Device1::OpenSharedResourceByName**</span><span class="sxs-lookup"><span data-stu-id="18f65-166">**ID3D11Device1::OpenSharedResourceByName**</span></span>](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)
-   [<span data-ttu-id="18f65-167">**D3D11 \_ 資源的 \_ 其他 \_ 共用 \_ NTHANDLE**</span><span class="sxs-lookup"><span data-stu-id="18f65-167">**D3D11\_RESOURCE\_MISC\_SHARED\_NTHANDLE**</span></span>](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="offer-the-video-memory-of-resources"></a><span data-ttu-id="18f65-168">提供資源的視訊記憶體</span><span class="sxs-lookup"><span data-stu-id="18f65-168">Offer the video memory of resources</span></span>

<span data-ttu-id="18f65-169">DXGI 1.2 可讓應用程式以低額外負荷提供其資源的視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="18f65-169">DXGI 1.2 enables an app to offer the video memory of its resources with low overhead.</span></span> <span data-ttu-id="18f65-170">藉由提供視訊記憶體，作業系統可以釋放視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="18f65-170">By offering the video memory, the operating system can free the video memory.</span></span>

<span data-ttu-id="18f65-171">此 DXGI 1.2 功能包含下列方法。</span><span class="sxs-lookup"><span data-stu-id="18f65-171">This DXGI 1.2 feature consists of the following methods.</span></span>

-   [<span data-ttu-id="18f65-172">**IDXGIDevice2::OfferResources**</span><span class="sxs-lookup"><span data-stu-id="18f65-172">**IDXGIDevice2::OfferResources**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources)
-   [<span data-ttu-id="18f65-173">**IDXGIDevice2::ReclaimResources**</span><span class="sxs-lookup"><span data-stu-id="18f65-173">**IDXGIDevice2::ReclaimResources**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources)

<span data-ttu-id="18f65-174">您可以使用 [**ID3D11Debug：： SetFeatureMask**](/windows/win32/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask) 方法來設定功能遮罩旗標，以在您的應用程式中偵測 [**IDXGIDevice2：： OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) 和 [**IDXGIDevice2：： ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) 方法的行為。</span><span class="sxs-lookup"><span data-stu-id="18f65-174">You can use the [**ID3D11Debug::SetFeatureMask**](/windows/win32/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask) method to set feature-mask flags that debug the behavior of the [**IDXGIDevice2::OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) and [**IDXGIDevice2::ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) methods in your app.</span></span>

## <a name="gpu-preemption-at-finer-granularity-levels-for-wddm-12-driver-model"></a><span data-ttu-id="18f65-175">適用于 WDDM 1.2 驅動程式模型的更細微細微性層級的 GPU 搶先</span><span class="sxs-lookup"><span data-stu-id="18f65-175">GPU preemption at finer granularity levels for WDDM 1.2 driver model</span></span>

<span data-ttu-id="18f65-176">從 Windows 顯示驅動程式模型開始 (WDDM) 1.2 驅動程式模型，WDDM 排程器可以在更細微的細微性層級上，搶先處理 GPU 的應用程式工作執行。</span><span class="sxs-lookup"><span data-stu-id="18f65-176">Starting with the Windows Display Driver Model (WDDM) 1.2 driver model, the WDDM scheduler can preempt the GPU's execution of application tasks at finer granularity levels.</span></span> <span data-ttu-id="18f65-177">DXGI 1.2 可讓您判斷 GPU 優先的資料細微性層級。</span><span class="sxs-lookup"><span data-stu-id="18f65-177">DXGI 1.2 lets you determine the GPU preemption granularity levels.</span></span>

<span data-ttu-id="18f65-178">此 DXGI 1.2 功能包含下列方法。</span><span class="sxs-lookup"><span data-stu-id="18f65-178">This DXGI 1.2 feature consists of the following method.</span></span>

-   [<span data-ttu-id="18f65-179">**IDXGIAdapter2::GetDesc2**</span><span class="sxs-lookup"><span data-stu-id="18f65-179">**IDXGIAdapter2::GetDesc2**</span></span>](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiadapter2-getdesc2)

## <a name="debugging-apis"></a><span data-ttu-id="18f65-180">調試 Api</span><span class="sxs-lookup"><span data-stu-id="18f65-180">Debugging APIs</span></span>

<span data-ttu-id="18f65-181">Windows 8 SDK 提供額外的調試功能。</span><span class="sxs-lookup"><span data-stu-id="18f65-181">The Windows 8 SDK provides additional debugging capability.</span></span> <span data-ttu-id="18f65-182">您可以使用下列 Dxgidebug.dll 的 DXGI Api 來對應用程式進行偵錯工具：</span><span class="sxs-lookup"><span data-stu-id="18f65-182">You can use the following DXGI APIs from Dxgidebug.dll to debug your app:</span></span>

-   [<span data-ttu-id="18f65-183">**DXGIGetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="18f65-183">**DXGIGetDebugInterface**</span></span>](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)
-   [<span data-ttu-id="18f65-184">**IDXGIDebug**</span><span class="sxs-lookup"><span data-stu-id="18f65-184">**IDXGIDebug**</span></span>](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug)
-   [<span data-ttu-id="18f65-185">**IDXGIInfoQueue**</span><span class="sxs-lookup"><span data-stu-id="18f65-185">**IDXGIInfoQueue**</span></span>](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

<span data-ttu-id="18f65-186">若要存取 [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)，請呼叫 [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函數來取得 Dxgidebug.dll，並呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來取得 **DXGIGetDebugInterface** 的位址。</span><span class="sxs-lookup"><span data-stu-id="18f65-186">To access [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface), call the [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function to get Dxgidebug.dll and the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to get the address of **DXGIGetDebugInterface**.</span></span> <span data-ttu-id="18f65-187">然後，您可以呼叫 **DXGIGetDebugInterface** 來取得 [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug) 或 [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) 介面。</span><span class="sxs-lookup"><span data-stu-id="18f65-187">You can then call **DXGIGetDebugInterface** to obtain the [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug) or [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) interface.</span></span>

<span data-ttu-id="18f65-188">如需有關如何從遠端偵測 DirectX 應用程式的詳細資訊，請參閱 [從遠端偵錯 directx 應用程式](../direct3dtools/debugging-directx-apps-remotely.md)。</span><span class="sxs-lookup"><span data-stu-id="18f65-188">For info about how to debug DirectX apps remotely, see [Debugging DirectX apps remotely](../direct3dtools/debugging-directx-apps-remotely.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="18f65-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="18f65-189">Related topics</span></span>

[<span data-ttu-id="18f65-190">DXGI 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="18f65-190">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
