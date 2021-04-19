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
# <a name="dxgi-12-improvements"></a>DXGI 1.2 改善

Microsoft DirectX Graphic Infrastructure (DXGI) 1.2 新增了下列功能。

## <a name="presentation-enhancements-and-optimizations"></a>簡報增強功能和優化

DXGI 1.2 利用新的翻轉模型交換鏈、內容保護、無視窗的呈現方式，以及您在其中指定已變更矩形和捲動區域的優化簡報，來增強展示。 簡報也增強了 stereoscopic 3D 顯示器行為。

您可以使用下列 DXGI 1.2 API 來增強簡報。

-   [**IDXGIDisplayControl::IsStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled)
-   [**IDXGIDisplayControl::SetStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled)
-   [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)
-   [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
-   [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
-   [**IDXGIFactory2::IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)
-   [**IDXGIFactory2::RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
-   [**IDXGIFactory2::RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
-   [**IDXGIFactory2::UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
-   [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
-   [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
-   [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
-   [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)
-   [**IDXGIOutput1::GetDisplaySurfaceData1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1)
-   [**IDXGIOutput1::FindClosestMatchingMode1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1)
-   [**IDXGIResource1::CreateSubresourceSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface)
-   [**IDXGISurface2::GetResource**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgisurface2-getresource)
-   [**IDXGISwapChain1::GetDesc1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1)
-   [**IDXGISwapChain1::GetFullscreenDesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc)
-   [**IDXGISwapChain1::GetHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd)
-   [**IDXGISwapChain1::GetCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
-   [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**IDXGISwapChain1::IsTemporaryMonoSupported**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported)
-   [**IDXGISwapChain1::GetRestrictToOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrestricttooutput)
-   [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)
-   [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)
-   [**IDXGISwapChain1::SetRotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
-   [**IDXGISwapChain1::GetRotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)

如需如何使用 DXGI 1.2 API 以增強簡報的詳細資訊，請參閱 [使用翻轉模型、中途矩形和捲動區域增強簡報](dxgi-1-2-presentation-improvements.md)。

如需如何判斷您是否可以在身歷聲中轉譯的詳細資訊，請參閱 [以身歷聲呈現的資料，並通知身歷聲狀態](stereo-rendering-stereo-status-notifying.md)。

如需如何判斷應用程式遮蔽狀態變更的資訊，請參閱不 [需要在轉譯時等候事件](waiting-when-occluded.md)。

如需有關在螢幕上顯示內容時資料值如何變更的資訊，請參閱 [轉換色彩空間的資料](converting-data-color-space.md)。

## <a name="desktop-duplication"></a>桌面複製

Windows 8 停用標準 Windows 2000 顯示驅動程式模型 (XDDM) 鏡像驅動程式。 DXGI 1.2 提供桌面複製 API 作為替代方案。 桌面複製 API 可讓您從遠端存取桌面映射以進行共同作業案例。

桌面複製 API 包含下列方法。

-   [**IDXGIOutput1：:D uplicateOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
-   [**IDXGIOutputDuplication::GetDesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getdesc)
-   [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)
-   [**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects)
-   [**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects)
-   [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape)
-   [**IDXGIOutputDuplication::MapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface)
-   [**IDXGIOutputDuplication::UnMapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface)
-   [**IDXGIOutputDuplication::ReleaseFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-releaseframe)

如需如何使用桌面複製 API 的詳細資訊，請參閱 [桌面複製 api](desktop-dup-api.md)。

## <a name="improved-usage-of-shared-resources-and-synchronized-events"></a>改善共用資源的使用和已同步處理的事件

在舊版的 Windows 中，應用程式會使用連續輪詢來判斷圖形處理單元 (GPU) 是否已完成處理任意命令。 DXGI 1.2 可讓應用程式將事件佇列至 DXGI 裝置。 然後，應用程式可以等待 DXGI 裝置通知事件，以判斷 GPU 已完成執行所有轉譯命令。 DXGI 1.2 可讓多個裝置透過 NT 控制碼共用資源。

您可以使用下列 DXGI 1.2 API 和 Direct3D 11.1 API 來共用資源和同步處理事件。

-   [**IDXGIDevice2::EnqueueSetEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
-   [**IDXGIResource1::CreateSharedHandle**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
-   [**IDXGIFactory2::GetSharedResourceAdapterLuid**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
-   [**ID3D11Device1::OpenSharedResource1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
-   [**ID3D11Device1::OpenSharedResourceByName**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)
-   [**D3D11 \_ 資源的 \_ 其他 \_ 共用 \_ NTHANDLE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="offer-the-video-memory-of-resources"></a>提供資源的視訊記憶體

DXGI 1.2 可讓應用程式以低額外負荷提供其資源的視訊記憶體。 藉由提供視訊記憶體，作業系統可以釋放視訊記憶體。

此 DXGI 1.2 功能包含下列方法。

-   [**IDXGIDevice2::OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources)
-   [**IDXGIDevice2::ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources)

您可以使用 [**ID3D11Debug：： SetFeatureMask**](/windows/win32/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask) 方法來設定功能遮罩旗標，以在您的應用程式中偵測 [**IDXGIDevice2：： OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) 和 [**IDXGIDevice2：： ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) 方法的行為。

## <a name="gpu-preemption-at-finer-granularity-levels-for-wddm-12-driver-model"></a>適用于 WDDM 1.2 驅動程式模型的更細微細微性層級的 GPU 搶先

從 Windows 顯示驅動程式模型開始 (WDDM) 1.2 驅動程式模型，WDDM 排程器可以在更細微的細微性層級上，搶先處理 GPU 的應用程式工作執行。 DXGI 1.2 可讓您判斷 GPU 優先的資料細微性層級。

此 DXGI 1.2 功能包含下列方法。

-   [**IDXGIAdapter2::GetDesc2**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiadapter2-getdesc2)

## <a name="debugging-apis"></a>調試 Api

Windows 8 SDK 提供額外的調試功能。 您可以使用下列 Dxgidebug.dll 的 DXGI Api 來對應用程式進行偵錯工具：

-   [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)
-   [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug)
-   [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

若要存取 [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)，請呼叫 [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) 函數來取得 Dxgidebug.dll，並呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來取得 **DXGIGetDebugInterface** 的位址。 然後，您可以呼叫 **DXGIGetDebugInterface** 來取得 [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug) 或 [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) 介面。

如需有關如何從遠端偵測 DirectX 應用程式的詳細資訊，請參閱 [從遠端偵錯 directx 應用程式](../direct3dtools/debugging-directx-apps-remotely.md)。

## <a name="related-topics"></a>相關主題

[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
