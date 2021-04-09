---
title: 適用于 Windows 7 的平臺更新
description: 本主題說明 Windows 7 圖形堆疊元件的增強功能，可透過適用于 Windows 7 的平臺更新取得。
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fd1e6e2681673d2bb2bab7a4a6de42f77988eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842631"
---
# <a name="platform-update-for-windows-7"></a>適用于 Windows 7 的平臺更新

本主題說明 Windows 7 圖形堆疊元件的增強功能，可透過 [適用于 windows 7 的平臺更新取得](https://support.microsoft.com/kb/2670838)。

在 Windows 7 上安裝時，Windows 7 的平臺更新會以 Windows 8 中提供的功能更新 Windows 7。 例如，這些 Windows 8 元件會提供完整功能：

-   Direct2D 1.1 (包括 Direct2D 效果) 
-   DirectWrite
-   Windows 影像處理元件 (WIC)

這些都提供部分功能：

-   Direct3D 11。1
-   DXGI 1。2

例如，這個元件無法使用：

-   DirectComposition (DComp) 

請參閱下列主題，以取得有關使用平臺更新 Direct2D、DirectWrite 和 WIC 的詳細資訊：

-   [Windows 8 (Windows) 的 Direct2D 新功能 ](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Windows 8 (Windows) 的 DirectWrite 新功能 ](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Windows 8 (Windows) 中的 WIC 新功能 ](/previous-versions//hh994467(v=vs.85))

請參閱下列主題，以取得使用平臺更新之 Direct3D 和 DXGI 的相關資訊：

-   [D3D 11.1 功能](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [DXGI 1.2 改進](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

在安裝平臺更新之後，Direct3D 11.1 和 DXGI 1.2 中引進的介面將可搭配部分功能使用。 這些圖形元件的功能直接系結至圖形核心元件、圖形驅動程式和圖形硬體。 在 Windows 7 上使用 Direct3D 11.1 之前，請先熟悉下列細節：

-   Windows 8 引進了 WDDM 1.2 驅動程式模型，可針對所有 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)，在相關聯的 API 介面上提供改進。 閱讀 Direct3D 11.1 檔時，請瞭解 *新的驅動* 程式表示 WDDM 1.2 驅動程式。 在 Windows 7 上無法使用這些更新的驅動程式版本，以及透過 [**CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport)公開的大部分選擇性功能。 因為無法保證這些選用功能可供使用，所以當所需的功能無法使用時，請確定您的應用程式具有適當的回溯行為。

    有一個重要的例外狀況。 有幾項功能（例如具有常數緩衝區位移的 [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) ）需要新的 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10 和更高的驅動程式，但實際上是針對功能層級9進行模擬。 這項模擬適用于 Windows 7 （具有平臺更新）。 如需模擬哪些功能的詳細資訊，請參閱 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ 選項**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) 。

-   Windows 8 WDDM 1.2 驅動程式模型支援新一代的硬體，透過 D3D [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.1 來公開。 具有 platform update 的 Windows 7 僅支援 WDDM 1.1 驅動程式模型，因此 (透過平臺更新) ，無法使用功能層級11.1 硬體支援。 在具有平臺更新的 Windows 7 上， [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) 一律會傳回11.0 或更低的功能等級，但使用可在 windows 7 上用來測試11.1 程式碼路徑的參照裝置除外。 請只使用您的目標功能層級可用的功能，如功能層級參考中所述。
-   Windows 7 的平臺更新未完全支援 DGXI 1.2 中引進的一些新方法。您可以直接呼叫這些函式並檢查錯誤碼，來測試這些函式的可用性。 當所需的功能無法使用時，請確定您的應用程式以具有平臺更新的 Windows 7 為目標。 適用于 Windows 7 的平臺更新無法使用這些功能類別：

    -   立體聲
    -   Swapchains 未以 Hwnd 為目標
    -   遮蔽狀態通知
    -   桌面複製
    -   NT 處理資源

    具體而言，下列 Api 將會傳回 \_ 不支援的 dxgi 錯誤 \_ 、dxgi \_ 錯誤 \_ 不正確 \_ 呼叫、e \_ >notimpl 或 e \_ INVALIDARG：

    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**RegisterStereoStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**RegisterStereoStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**UnregisterStereoStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**RegisterOcclusionStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**RegisterOcclusionStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**UnregisterOcclusionStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)：：[**GetCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)：：[**SetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)：：[**GetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)：：[**DuplicateOutput**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)：：[**EnqueueSetEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)：：[**CreateSharedHandle**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**GetSharedResourceAdapterLuid**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)：：[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)：：[**OpenSharedResourceByName**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   這些 Api 具有行為差異，如下所述：
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) 採用 [**DXGI \_ 交換 \_ 鏈 \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) 結構，其具有用於 **調整** 的欄位。 [**DXGI \_在 \_**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) Windows 7 上，不支援使用平臺更新來調整 [無]，而且會在呼叫時使 **CreateSwapChainForHwnd** 傳回 DXGI \_ 錯誤不正確 \_ \_ 呼叫。
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)：：[**SetBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) 只有在使用 DXGI 調整無的 swapchain 上設定時才有用 \_ \_ 。 它的值仍會儲存並可抓取，但不會有任何作用。
    -   [**IDXGIDisplayControl**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)：：[**IsStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled)、 [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)：：[**IsWindowedStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)和 [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)：：[**IsTemporaryMonoSupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) 全都會傳回 **FALSE**。
    -   已新增 [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)：：[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)和 **IDXGIOutput1**：：[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) ，以加速身歷聲顯示模式。 Windows 7 的平臺更新不支援身歷聲，因此這個方法相當於 [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)：：[**FindClosestMatchingMode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) 做為 [**DXGI \_ 模式 \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1)。身歷聲一律會是 FALSE。
    -   適用于 Windows 7 的平臺更新不支援 [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)：：[**OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources)和 **IDXGIDevice2**：：[**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) 。 不過，執行時間仍然允許呼叫它們，並執行驗證，以便在非共用資源上正確使用它們。
    -   [變形](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) 裝置僅支援 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0。 也就是，在 [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice)的 *DriverType* 參數中傳遞 [D3D \_ 驅動程式 \_ 類型 \_ 變形](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)所建立的變形裝置不支援11.1，也不支援共用的表面。
-   如果開發人員目前使用 [**D3D11 \_ 建立 \_ 裝置 \_ 調試**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) 程式旗標來處理 Microsoft Visual Studio 2010 或更早版本中的應用程式，請注意 [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) 的呼叫將會失敗。 這是因為 D3D 11.1 執行時間現在需要 D3D11 \_1SDKLayers.dll 而不是 D3D11SDKLayers.dll。 若要取得這個新的 DLL (D3D11 \_1SDKLayers.dll) ，請安裝 [Windows 8 SDK](https://dev.windows.com/downloads/windows-8-sdk)或 [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)或 Visual Studio 2012 遠端偵錯工具。 請參閱 [Debug Layer](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) 檔以取得詳細資訊。

 

 