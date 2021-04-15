---
description: 本主題包含下列各節。
ms.assetid: 0522ccbf-e754-470a-8199-004fcbaa927d
title: DXGI 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 324a5be26aade17385a6ab0b7d347015497a2a3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467533"
---
# <a name="dxgi-overview"></a>DXGI 總覽

Microsoft DirectX Graphic Infrastructure (DXGI) 可辨識圖形的某些部分會比其他部分慢得多。 DXGI 的主要目標是管理可獨立于 DirectX graphics runtime 的低層級工作。 DXGI 提供適用于未來圖形元件的通用架構;利用 DXGI 的第一個元件是 Microsoft Direct3D 10。

在舊版的 Direct3D 中，像是硬體裝置的列舉、將轉譯的畫面格呈現至輸出、控制 gamma，以及管理全螢幕轉換等低層級工作，都包含在 Direct3D 執行時間中。 這些工作現在會在 DXGI 中執行。

DXGI 的用途是與核心模式驅動程式和系統硬體通訊，如下圖所示。

![應用程式、dxgi 和驅動程式和硬體之間的通訊圖表](images/dxgi-dll.png)

應用程式可以直接存取 DXGI，或呼叫 D3D11 \_ 1. h、D3D11 .h、D3D10 1 .h 或 D3D10 中的 Direct3D api， \_ 這會為您處理 DXGI 的通訊。 如果您的應用程式需要列舉裝置，或控制資料呈現給輸出的方式，您可能會想要直接使用 DXGI。

本主題包含下列各節。

-   [列舉介面卡](#enumerating-adapters)
    -   [列舉 Windows 8 的介面卡的新資訊](#new-info-about-enumerating-adapters-for-windows-8)
-   [展示](#presentation)
    -   [建立交換鏈](#create-a-swap-chain)
    -   [交換鏈的護理和饋送](#care-and-feeding-of-the-swap-chain)
    -   [處理視窗調整大小](#handling-window-resizing)
    -   [選擇 DXGI 輸出和大小](#choosing-the-dxgi-output-and-size)
    -   [在 Full-Screen 模式中進行調試](#debugging-in-full-screen-mode)
    -   [終結交換鏈](#destroying-a-swap-chain)
    -   [使用旋轉的監視器](#using-a-rotated-monitor)
    -   [切換模式](#switching-modes)
    -   [全螢幕的效能秘訣](#full-screen-performance-tip)
    -   [多執行緒考慮](#multithread-considerations)
-   [DLLMain 的 DXGI 回應](#dxgi-responses-from-dllmain)
-   [DXGI 1.1 變更](#dxgi-11-changes)
-   [DXGI 1.2 變更](#dxgi-12-changes)
-   [相關主題](#related-topics)

若要查看 Direct3D 11 硬體支援的格式：

-   [Direct3D 功能等級12.1 硬體的 DXGI 格式支援](hardware-support-for-direct3d-12-1-formats.md)
-   [Direct3D 功能等級12.0 硬體的 DXGI 格式支援](hardware-support-for-direct3d-12-0-formats.md)
-   [Direct3D 功能等級11.1 硬體的 DXGI 格式支援](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Direct3D 功能等級11.0 硬體的 DXGI 格式支援](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Direct3D 10Level9 格式的硬體支援](/previous-versions//ff471324(v=vs.85))
-   [Direct3D 10.1 格式的硬體支援](/previous-versions//cc627091(v=vs.85))
-   [適用于 Direct3D 10 格式的硬體支援](/previous-versions//cc627090(v=vs.85))

## <a name="enumerating-adapters"></a>列舉介面卡

介面卡是您電腦的硬體和軟體功能的抽象概念。 您的電腦上通常會有許多介面卡。 某些裝置會在硬體 (（像是您的視訊卡) ）中執行，而有些則是在軟體 (（例如 Direct3D 參考轉譯器) ）中執行。 介面卡會執行圖形應用程式所使用的功能。 下圖顯示具有單一電腦的系統、兩張介面卡 (視訊卡) 和三個輸出監視器。

![具有兩張視訊卡和三部監視器的電腦圖表](images/dxgi-terms.png)

列舉這些硬體時，DXGI 會為每個輸出建立 [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) 介面 (或監視) 和每張視訊卡的 [**IDXGIAdapter2**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2) 介面 (即使是內建于主機板) 的視訊卡。 列舉是藉由使用 [**IDXGIFactory**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) 介面呼叫 [**IDXGIFactory：： EnumAdapters**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-enumadapters)來傳回一組代表影片硬體的 [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) 介面。

DXGI 1.1 新增了 [**IDXGIFactory1**](/windows/win32/api/DXGI/nn-dxgi-idxgifactory1) 介面。 [**IDXGIFactory1：： EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) 會傳回一組代表影片硬體的 [**IDXGIAdapter1**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter1) 介面。

如果您想要在使用 Direct3D Api 時選取特定的影片硬體功能，建議您在每個介面卡控制碼和可能的硬體 [功能層級](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)反復呼叫 [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)或 [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain)函式。 如果指定的介面卡支援功能層級，則此函式會成功。

### <a name="new-info-about-enumerating-adapters-for-windows-8"></a>列舉 Windows 8 的介面卡的新資訊

從 Windows 8 開始，稱為「Microsoft 基本轉譯驅動程式」的介面卡一律會存在。 此介面卡具有 **0x1414** 的 VendorId 以及 **0x8c** 的 DeviceID。 此介面卡也會在其 [**dxgi \_ 介面卡 \_ DESC2**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_adapter_desc2)結構的 **旗標** 成員中設定 [ [**dxgi \_ adapter \_ 旗 \_**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag)標] 軟體值。 此介面卡是僅限轉譯的裝置，沒有顯示輸出。 DXGI 永遠不會傳回此介面卡 [**移除的 dxgi \_ 錯誤 \_ 裝置 \_**](dxgi-error.md) 。

如果電腦的顯示驅動程式無法運作或已停用，電腦的主要 (**Null**) 介面卡可能也稱為「Microsoft 基本轉譯驅動程式」。 但此介面卡有輸出，且未設定 [**DXGI \_ 介面卡 \_ 旗標 \_ 軟體**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) 值。 作業系統和應用程式預設會使用此介面卡。 如果已安裝或啟用顯示驅動程式，則應用程式可能會收到此介面卡 [**移除的 DXGI \_ 錯誤 \_ 裝置 \_**](dxgi-error.md) ，然後必須重新列舉介面卡。

當電腦的主要顯示器介面卡是「Microsoft 基本顯示器介面卡」 ([變形](../direct3d11/overviews-direct3d-11-devices-create-warp.md) 介面卡) 時，該電腦也會有第二張介面卡。 第二張介面卡是僅限轉譯的裝置，沒有顯示輸出，而 DXGI 永遠不會傳回 [**dxgi \_ 錯誤 \_ 裝置 \_**](dxgi-error.md)。

如果您想要將變形用於轉譯、計算或其他長時間執行的工作，建議使用僅限轉譯的裝置。 您可以藉由呼叫 [**IDXGIFactory1：： EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) 方法，取得僅限轉譯裝置的指標。 當您在 [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)的 *DriverType* 參數中指定 [**D3D \_ 驅動程式 \_ 類型 \_ 變形**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type)時，也會建立僅限轉譯的裝置，因為變形裝置也會使用僅呈現的變形介面卡。

## <a name="presentation"></a>簡報

您應用程式的工作是轉譯畫面格，並要求 DXGI 將這些畫面呈現給輸出。 如果應用程式有兩個可用的緩衝區，它可以在呈現另一個緩衝區時轉譯一個緩衝區。 應用程式可能需要兩個以上的緩衝區，這取決於轉譯框架所需的時間，或呈現所需的畫面播放速率。 所建立的緩衝區集會稱為交換鏈，如下所示。

![交換鏈的圖例](images/dxgi-swap-chain.png)

-   [建立交換鏈](#create-a-swap-chain)
-   [交換鏈的護理和饋送](#care-and-feeding-of-the-swap-chain)
-   [處理視窗調整大小](#handling-window-resizing)
-   [選擇 DXGI 輸出和大小](#choosing-the-dxgi-output-and-size)
-   [在 Full-Screen 模式中進行調試](#debugging-in-full-screen-mode)
-   [終結交換鏈](#destroying-a-swap-chain)
-   [使用旋轉的監視器](#using-a-rotated-monitor)
-   [切換模式](#switching-modes)
-   [全螢幕的效能秘訣](#full-screen-performance-tip)
-   [多執行緒考慮](#multithread-considerations)

交換鏈有一個前端緩衝區和一或多個背景緩衝區。 每個應用程式都會建立自己的交換鏈。 為了將資料呈現的速度最大化到輸出，交換鏈幾乎一律會在顯示子系統的記憶體中建立，如下圖所示。

![顯示子系統的圖例](images/dxgi-adapter.png)

顯示子系統 (通常是視訊卡，但可以在主機板上執行) 包含 GPU、數位轉類比轉換器 (DAC) 和記憶體。 交換鏈是在此記憶體內配置，以非常快速的方式進行呈現。 顯示子系統會將前端緩衝區中的資料呈現給輸出。

交換鏈的設定是以全螢幕或視窗模式繪製，如此就不需要知道輸出是視窗型或全螢幕。 全螢幕模式的交換鏈可以藉由切換顯示器解析度，來將效能優化。

### <a name="create-a-swap-chain"></a>建立交換鏈結

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 10 之間的差異： Direct3D 10 是使用 DXGI 的第一個圖形元件。 DXGI 有一些不同的交換鏈行為。<br/>
<ul>
<li>在 DXGI 中，交換鏈會在建立交換鏈時系結至視窗。 這種變更可改善效能並節省記憶體。 舊版 Direct3D 允許交換鏈變更交換鏈所系結的視窗。</li>
<li>在 DXGI 中，交換鏈會在建立時系結至轉譯裝置。 Direct3D 建立的裝置函式傳回的裝置物件會執行 <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> 介面。 您可以呼叫 <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> 來查詢裝置的對應 <a href="/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgidevice2"><strong>IDXGIDevice2</strong></a> 介面。 變更轉譯裝置需要重新建立交換鏈。</li>
<li><p>在 DXGI 中，可用的交換效果是 DXGI_SWAP_EFFECT_DISCARD 並 DXGI_SWAP_EFFECT_SEQUENTIAL。 從 Windows 8 開始也可以使用 DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL 交換效果。 下表顯示 Direct3D 9 至 DXGI swap 效果定義的對應。 </p>
<table>
<thead>
<tr class="header">
<th>D3D9 交換效果</th>
<th>DXGI 交換效果</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DSWAPEFFECT_DISCARD</td>
<td>DXGI_SWAP_EFFECT_DISCARD</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_COPY</td>
<td>具有1個緩衝區的 DXGI_SWAP_EFFECT_SEQUENTIAL</td>
</tr>
<tr class="odd">
<td>D3DSWAPEFFECT_FLIP</td>
<td>具有2個或多個緩衝區的 DXGI_SWAP_EFFECT_SEQUENTIAL</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_FLIPEX</td>
<td>具有2個或多個緩衝區的 DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</td>
</tr>
</tbody>
</table>
<p></p>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



 

交換鏈的緩衝區會以特定的大小和特定格式建立。 應用程式會指定這些值 (或您可以在啟動時繼承目標視窗) 的大小，然後視需要在視窗大小變更時加以修改，以回應使用者輸入或程式事件。

建立交換鏈之後，您通常會想要在其中呈現影像。 以下是設定 Direct3D 內容以轉譯成交換鏈的程式碼片段。 此程式碼會從交換鏈中解壓縮緩衝區、從該緩衝區建立轉譯目標視圖，然後在裝置上進行設定：


```
ID3D11Resource * pBB;
ThrowFailure( pSwapChain->GetBuffer(0, __uuidof(pBB),    
  reinterpret_cast<void**>(&pBB)), "Couldn't get back buffer");
ID3D11RenderTargetView * pView;
ThrowFailure( pD3D11Device->CreateRenderTargetView(pBB, NULL, &pView), 
  "Couldn't create view" );
pD3D11DeviceContext->OMSetRenderTargets(1, &pView, 0);
        
```



當您的應用程式將畫面格轉譯成交換鏈緩衝區之後，請呼叫 [**IDXGISwapChain1：:P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)。 然後，應用程式就可以轉譯下一個影像。

### <a name="care-and-feeding-of-the-swap-chain"></a>交換鏈的護理和饋送

轉譯影像之後，請呼叫 [**IDXGISwapChain1：:P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) ，然後轉譯下一個影像。 這是您責任的範圍。

如果您先前已呼叫 [**IDXGIFactory：： MakeWindowAssociation**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation)，使用者可以按 Alt-Enter 按鍵組合，而 DXGI 會在視窗模式和全螢幕模式之間轉換您的應用程式。 建議使用 **IDXGIFactory：： MakeWindowAssociation** ，因為強烈需要使用者的標準控制機制。

雖然您不需要撰寫超過所述的程式碼，但有幾個簡單的步驟可以讓您的應用程式更具回應性。 最重要的考慮是調整交換鏈的緩衝區大小，以回應輸出視窗的調整大小。 應用程式的最佳路由當然是回應 WM 的 \_ 大小，然後呼叫 [**IDXGISwapChain：： ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers)，傳遞訊息參數中所包含的大小。 這種行為顯然讓您的應用程式在拖曳視窗的框線時，能夠適當地回應使用者，但這也是啟用平滑全螢幕轉換的確切功能。 \_當這類轉換發生時，您的視窗將會收到 WM 大小的訊息，而呼叫 **IDXGISwapChain：： ResizeBuffers** 是交換鏈的機會，可重新配置緩衝區的儲存體以進行最佳展示。 這就是為什麼在呼叫 **IDXGISwapChain：： ResizeBuffers** 之前，應用程式必須釋放現有緩衝區上任何參考的原因。

無法呼叫 [**IDXGISwapChain：： ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) 來回應切換至全螢幕模式 (最自然的原因是，為了回應 WM \_ 大小) ，可能會妨礙翻轉的優化，其中 DXGI 可以直接交換要顯示的緩衝區，而不是複製全螢幕的資料。

[**IDXGISwapChain1：:P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 將會通知您，您的輸出視窗是否透過 **DXGI \_ 狀態 \_ pixels occluded** 完全 pixels occluded。 發生這種情況時，我們建議您藉由呼叫 **IDXGISwapChain1：:P resent1** 與 **DXGI \_ 目前的 \_ 測試**) 來進入待命模式 (，因為用來呈現框架的資源會浪費。 使用 **DXGI \_ 現狀 \_ 測試** 可防止在仍執行遮蔽檢查時顯示任何資料。 一旦 **IDXGISwapChain1 之後，:P resent1** 會傳回 S \_ OK，您應該結束待命模式; 請勿使用傳回碼來切換回待命模式，因為這樣可能會讓交換鏈無法進入全螢幕模式。

從 Windows 8 開始提供的 Direct3D 11.1 執行時間會提供翻轉模型交換鏈， (也就是具有 [**dxgi \_ 交換 \_ 效果 \_ \_**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect)的交換鏈，會反轉在 [**dxgi \_ 交換 \_ 鏈 \_ DESC**](/windows/win32/api/DXGI/ns-dxgi-dxgi_swap_chain_desc)或 [**dxgi \_ 交換 \_ 鏈) \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)的 **SwapEffect** 成員中設定的連續值。 當您向翻轉模型交換鏈呈現輸出的畫面格時，DXGI 會將後置緩衝區從所有管線狀態位置（例如輸出合併轉譯目標）解除系結，以寫入回緩衝區0。 因此，我們建議您在轉譯為背景緩衝區之前，立即呼叫 [**>id3d11devicecoNtext：： OMSetRenderTargets**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets) 。 例如，請勿呼叫 **OMSetRenderTargets** ，然後執行計算著色器工作，而不會結束轉譯至資源。 如需翻轉模型交換鏈及其優點的詳細資訊，請參閱 [DXGI 翻轉模型](dxgi-flip-model.md)。

> [!NOTE]  
> 在 Direct3D 10 和 Direct3D 11 中，您不需要呼叫 [**IDXGISwapChain：： GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) ，就能在呼叫 [**IDXGISwapChain1：:P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 之後取回緩衝區0，因為為了方便起見，後端緩衝區的身分識別會變更。 在 Direct3D 12 中不會發生這種情況，您的應用程式必須改為手動追蹤緩衝區索引。

### <a name="handling-window-resizing"></a>處理視窗調整大小

您可以使用 [**IDXGISwapChain：： ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) 方法來處理視窗調整大小。 在呼叫 **ResizeBuffers** 之前，您必須釋放交換鏈緩衝區的所有未完成參考。 通常保存交換鏈緩衝區之參考的物件是呈現目標視圖。

下列範例程式碼示範如何從 WindowProc 處理常式內針對 WM 大小的訊息呼叫 [**ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) \_ ：


```
    case WM_SIZE:
        if (g_pSwapChain)
        {
            g_pd3dDeviceContext->OMSetRenderTargets(0, 0, 0);

            // Release all outstanding references to the swap chain's buffers.
            g_pRenderTargetView->Release();

            HRESULT hr;
            // Preserve the existing buffer count and format.
            // Automatically choose the width and height to match the client rect for HWNDs.
            hr = g_pSwapChain->ResizeBuffers(0, 0, 0, DXGI_FORMAT_UNKNOWN, 0);
                                            
            // Perform error handling here!

            // Get buffer and create a render-target-view.
            ID3D11Texture2D* pBuffer;
            hr = g_pSwapChain->GetBuffer(0, __uuidof( ID3D11Texture2D),
                                         (void**) &pBuffer );
            // Perform error handling here!

            hr = g_pd3dDevice->CreateRenderTargetView(pBuffer, NULL,
                                                     &g_pRenderTargetView);
            // Perform error handling here!
            pBuffer->Release();

            g_pd3dDeviceContext->OMSetRenderTargets(1, &g_pRenderTargetView, NULL );

            // Set up the viewport.
            D3D11_VIEWPORT vp;
            vp.Width = width;
            vp.Height = height;
            vp.MinDepth = 0.0f;
            vp.MaxDepth = 1.0f;
            vp.TopLeftX = 0;
            vp.TopLeftY = 0;
            g_pd3dDeviceContext->RSSetViewports( 1, &vp );
        }
        return 1;
```



### <a name="choosing-the-dxgi-output-and-size"></a>選擇 DXGI 輸出和大小

根據預設，DXGI 會選擇包含視窗大部分工作區的輸出。 這是可用於 DXGI 的唯一選項，當它變成全螢幕本身以回應 alt 輸入時。 如果應用程式選擇移至全螢幕模式，則可以呼叫 [**IDXGISwapChain：： SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) ，並傳遞明確的 [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) (或 **Null**（如果應用程式很高興讓 DXGI 決定) ）。

若要在全螢幕或視窗視窗中調整輸出的大小，建議您呼叫 [**IDXGISwapChain：： ResizeTarget**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget)，因為這個方法也會調整目標視窗的大小。 由於目標視窗經過調整大小，作業系統會傳送 **WM \_ 大小**，而您的程式碼會自然地呼叫 [**IDXGISwapChain：： ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) 來回應。 因此，重新調整緩衝區大小，然後再調整目標大小，會浪費精力。

### <a name="debugging-in-full-screen-mode"></a>在全螢幕模式中進行調試

只有在絕對必要時，才會會讓出全螢幕模式的 DXGI 交換鏈。 這表示您可以使用多個監視器來偵測全螢幕應用程式，只要 [偵錯工具] 視窗不會與交換鏈的目標視窗重迭。 或者，您也可以不設定 **DXGI \_ 交換 \_ 鏈 \_ 旗標 \_ 允許 \_ 模式 \_ 切換** 旗標，來防止整個模式切換。

如果允許切換模式，當另一個視窗 pixels occluded 輸出視窗時，交換鏈將會放棄全螢幕模式。 遮蔽檢查是在 IDXGISwapChain1 期間執行 [**：:P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)或個別的執行緒，其目的是要監看應用程式是否變得沒有回應 (而不會再呼叫 **IDXGISwapChain1：:P resent1**) 。 若要停用個別執行緒造成切換的能力，請將下列登錄機碼設定為任何非零的值。

**HKCU \\ Software \\ Microsoft \\ DXGI \\ DisableFullscreenWatchdog**

### <a name="destroying-a-swap-chain"></a>終結交換鏈

您不得以全螢幕模式釋放交換鏈，因為這樣做可能會產生執行緒爭用 (這會導致 DXGI 引發無法持續性的例外狀況) 。 釋出交換鏈之前，請先切換至視窗模式 (使用 [**IDXGISwapChain：： SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) ( **FALSE**， **Null** ) ) 然後呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。

### <a name="using-a-rotated-monitor"></a>使用旋轉的監視器

應用程式不需要擔心監視器方向，而 DXGI 會在呈現期間旋轉交換鏈緩衝區（如有必要）。 當然，這種額外的旋轉可能會影響效能。 為了達到最佳效能，請執行下列動作來處理應用程式中的旋轉：

-   使用 **DXGI \_ 交換 \_ 鏈旗標 \_ \_ NONPREROTATED**。 這會通知 DXGI，讓應用程式產生旋轉的影像 (例如，藉由改變其投影矩陣) 。 要注意的是，這個旗標只有在全螢幕模式下才有效。
-   配置每個交換鏈緩衝區的旋轉大小。 如有必要，請使用 [**IDXGIOutput：： GetDesc**](/windows/win32/api/DXGI/nf-dxgi-idxgioutput-getdesc) 來取得這些值。

藉由在您的應用程式中執行旋轉，DXGI 只會進行複製，而不是複製和旋轉。

從 Windows 8 開始提供的 Direct3D 11.1 執行時間會提供翻轉模型交換鏈， (也就是具有 [**dxgi \_ 交換 \_ 效果 \_ \_**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect)的交換鏈會反轉在 [**dxgi \_ 交換 \_ 鏈 \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)的 **SwapEffect** 成員中設定的順序值) 。 為了充分利用反轉模型交換鏈提供的展示優化，我們建議您讓應用程式將內容導向至內容，以符合內容所在的特定輸出（當內容完全佔用輸出時）。 如需翻轉模型交換鏈及其優點的詳細資訊，請參閱 [DXGI 翻轉模型](dxgi-flip-model.md)。

### <a name="switching-modes"></a>切換模式

進行全螢幕的轉換時，DXGI 交換鏈可能會變更輸出的顯示模式。 若要啟用自動顯示模式變更，您必須在交換鏈描述中指定 **DXGI \_ 交換 \_ 鏈 \_ 旗標 \_ 允許 \_ 模式 \_ 切換** 。 如果顯示模式自動變更，DXGI 將會選擇最適中的模式 (大小和解析度不會變更，但色彩深度可能會) 。 調整交換鏈緩衝區的大小不會造成模式切換。 如果您選擇的後置緩衝區完全符合目標輸出所支援的顯示模式，交換鏈就會進行隱含的承諾，然後在該輸出上輸入全螢幕模式時，切換至該顯示模式。 因此，您可以選擇您的背景緩衝區大小和格式來選擇顯示模式。

### <a name="full-screen-performance-tip"></a>全螢幕的效能秘訣

當您在全螢幕應用程式上呼叫 [**IDXGISwapChain1：:P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 時，交換鏈會翻轉 (，而不是 blits 將背景緩衝區的內容) 至前端緩衝區。 這需要使用 (在 [ [**DXGI \_ 交換 \_ 鏈] \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)) 中指定的列舉顯示模式來建立交換鏈。 如果您無法列舉顯示模式，或在描述中不正確地指定顯示模式，交換鏈可能會改為執行位區塊傳輸 (bitblt) 。 Bitblt 會導致額外的延展複製以及某些提高的視頻記憶體使用量，而且難以偵測。 若要避免這個問題，請先列舉顯示模式，並正確地初始化交換鏈描述，再建立交換鏈。 這可確保在全螢幕模式中進行翻轉時的最大效能，並避免額外的記憶體額外負荷。

### <a name="multithread-considerations"></a>多執行緒考慮

當您在具有多個執行緒的應用程式中使用 DXGI 時，您必須小心避免建立鎖死，而兩個不同的執行緒正在等候彼此完成。 有兩種情況可能會發生這種情況。

-   轉譯執行緒不是訊息泵執行緒。
-   執行 DXGI API 的執行緒與建立視窗的執行緒不同。

當您使用全螢幕交換鏈時，請小心不要讓訊息泵執行緒在轉譯執行緒上等候。 比方說，從轉譯) 執行緒呼叫 [**IDXGISwapChain1：:P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (可能會導致轉譯執行緒在訊息抽取執行緒上等候。 當發生模式變更時，如果 **Present1** 呼叫：： SetWindowPos () 或：： SetWindowStyle () ，而且其中一個方法呼叫：： SendMessage () ，則可能會發生這種情況。 在此案例中，如果訊息提取執行緒有重要的區段來保護它，或如果轉譯執行緒遭到封鎖，則這兩個執行緒將會鎖死。

如需搭配多個執行緒使用 DXGI 的詳細資訊，請參閱多 [執行緒和 DXGI](../direct3d11/overviews-direct3d-11-render-multi-thread-intro.md)。

## <a name="dxgi-responses-from-dllmain"></a>DLLMain 的 DXGI 回應

因為 [**DllMain**](../dlls/dllmain.md) 函式無法保證載入和卸載 dll 的順序，建議您應用程式的 **DllMain** 函式不會呼叫 Direct3D 或 DXGI 函數或方法，包括建立或釋放物件的函式或方法。 如果您的應用程式 **DllMain** 函式呼叫特定元件，該元件可能會呼叫作業系統上不存在的另一個 DLL，導致作業系統損毀。 Direct3D 和 DXGI 可能會載入一組 Dll （通常是一組驅動程式），而這組驅動程式與電腦不同。 因此，即使您的應用程式不會在您的開發和測試電腦上損毀，而其 **DllMain** 函式會呼叫 DIRECT3D 或 DXGI 函數或方法，但在另一部電腦上執行時可能會損毀。

為了防止您建立可能導致作業系統損毀的應用程式，DXGI 在指定的情況下提供下列回應：

-   如果您應用程式的 [**DllMain**](../dlls/dllmain.md) 函式釋放其對 DXGI factory 的最後一個參考，則 DXGI 會引發例外狀況。
-   如果您的應用程式 [**DllMain**](../dlls/dllmain.md) 函式建立了 dxgi factory，則 dxgi 會傳回錯誤碼。

## <a name="dxgi-11-changes"></a>DXGI 1.1 變更

我們在 DXGI 1.1 中新增了下列功能。

-   同步處理的共用表面支援

    適用于 Direct3D 10.1 和 Direct3D 11 的同步共用表面，可在多個 Direct3D 裝置之間進行有效率的讀取和寫入介面共用 (可) Direct3D 10 和 Direct3D 11 裝置之間的共用。 請參閱 [**IDXGIKeyedMutex：： AcquireSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-acquiresync) 和 [**IDXGIKeyedMutex：： ReleaseSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-releasesync)。

-   高彩支援

    支援 DXGI \_ format \_ R10G10B10 \_ XR \_ 偏差 \_ A2 \_ UNORM 格式。

-   [**IDXGIDevice1：： SetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency)和 [ **IDXGIDevice1：： GetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-getmaximumframelatency)
-   [**IDXGIFactory1：： EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) 會列舉本機介面卡 (s) ，而不會連結任何監視器或輸出，以及已附加輸出) 的介面卡 (s。 第一個傳回的介面卡將是顯示桌面主要的本機介面卡。
-   BGRA 格式支援

    DXGI \_ format \_ B8G8R8A8 \_ UNORM 和 dxgi \_ format \_ B8G8R8A8 \_ UNORM \_ SRGB，請參閱 [**IDXGISurface1：： GetDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-getdc) 和 [**IDXGISurface1：： ReleaseDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-releasedc)。

## <a name="dxgi-12-changes"></a>DXGI 1.2 變更

我們在 DXGI 1.2 中新增了下列功能。

-   身歷聲交換鏈
-   [翻轉模型交換鏈](dxgi-flip-model.md)
-   優化簡報 (滾動、中途矩形和旋轉) 
-   改良的共用資源與同步處理
-   [桌面複製](desktop-dup-api.md)
-   優化視訊記憶體的使用
-   支援每圖元16個位 (bpp) 格式 (DXGI \_ 格式 \_ B5G6R5 \_ UNORM、dxgi \_ FORMAT \_ B5G5R5A1 \_ UNORM、DXGI \_ format \_ B4G4R4A4 \_ UNORM) 
-   調試 Api

如需有關 DXGI 1.2 的詳細資訊，請參閱 [dxgi 1.2 增強功能](dxgi-1-2-improvements.md)。

## <a name="related-topics"></a>相關主題

[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
