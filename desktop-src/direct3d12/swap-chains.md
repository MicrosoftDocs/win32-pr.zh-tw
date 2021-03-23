---
title: 交換鏈
description: 交換鏈會控制背景的緩衝區旋轉，形成圖形動畫的基礎。
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbc7ec1b62ba620b42bc85c1c1f491ff7ba952d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104548407"
---
# <a name="swap-chains"></a>交換鏈

交換鏈會控制背景的緩衝區旋轉，形成圖形動畫的基礎。

## <a name="overview"></a>概觀

Direct3D 12 中交換鏈的程式設計模型與舊版 D3D 中的程式設計模型不同。 現在不支援在 D3D10 和 D3D11 中提供的程式設計便利性，例如支援自動資源輪替。 自動啟用資源輪替的應用程式，可在呈現的實際介面變更每個畫面時轉譯相同的 API 物件。 使用 Direct3D 12 變更交換鏈的行為，讓 Direct3D 12 的其他功能具有低 CPU 的額外負荷。 不支援自動色彩索引鍵和取樣，但明顯的延展和旋轉仍是。

### <a name="buffer-lifetime"></a>緩衝區存留期

您可以藉由確保交換鏈所擁有的一組緩衝區在交換鏈的存留期內不會變更，讓應用程式儲存參考緩衝區的預建描述項。 在呼叫特定 Api 之前， [**IDXGISwapChain：： GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) 所傳回的緩衝區集不會變更：

-   [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

[**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)傳回的緩衝區順序永遠不會變更。

[**IDXGISwapChain3：： GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) 會將目前背景緩衝區的索引傳回給應用程式。

### <a name="swap-effects"></a>交換效果

唯一支援的交換效果是 [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) 和 [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect)，其要求緩衝區計數必須大於1。

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>在視窗模式和全螢幕模式之間轉換

Direct3D 12 不支援 (FSE) 的全螢幕獨佔模式。 相反地，當遊戲是唯一顯示在畫面上的應用程式時，OS 會使用稱為全螢幕 optimisations 的策略 (FSO) 來達成與 FSE 類似的效果，而不會有效能上的缺點。 如需 FSO 的詳細資訊，請參閱 [揭開全螢幕 Optimisations](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/)。

Direct3D 12 在視窗模式和全螢幕模式之間進行轉換時，會維持應用程式必須呼叫 [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) 的限制 (D3D11 翻轉模型交換鏈的限制) 。

[**IDXGISwapChain：： SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)轉換不會變更交換鏈中應用程式可見的緩衝區集合。 只有 [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) 和 [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) 呼叫會建立或終結應用程式可見的緩衝區。 不過，在 Direct3D 12 [**IDXGISwapChain：： SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) 中不會進入全螢幕獨佔模式，而只會變更解析度和重新整理速率以允許全螢幕 optimisations。 應用程式不需要使用此方法即可進行這些變更

當或 [**IDXGISwapChain**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) 時，會呼叫:P 重新傳送或 [**IDXGISwapChain1：:P**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) 重新傳送，要顯示的背景緩衝區必須處於 [**D3D12 \_ 資源 \_ 狀態 \_ 目前**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) 狀態。 如果不是這種情況，就會發生 **DXGI \_ 錯誤 \_ 無效 \_ 呼叫** 而失敗。

全螢幕交換鏈會繼續具有 [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) (FALSE 的限制，Null) 必須在交換鏈的最終版本之前呼叫。 在 Direct3D 12 裝置上執行的交換鏈上， **SetFullscreenState** (FALSE) 成功。

目前的作業會在建立 swapchain 時所提供的3D 佇列上執行，而應用程式可自由地顯示多個交換鏈，以及記錄和執行命令清單。

當圖形的最後一部分運作 (例如，在計算佇列上進行框架後處理) ，或不包含裝置的圖形佇列，建立第二個要呈現的3D 佇列可能會很有説明，並防止呈現延遲時間延遲到下一個畫面格的開始。 

### <a name="example"></a>範例

下列範例程式碼會出現在主要轉譯迴圈中：

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>建立交換鏈

使用 [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)、 [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)或 [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) 呼叫時，請注意 *pDevice* 參數實際上需要 Direct3D 12 中直接命令佇列的指標，而不是裝置。

### <a name="presenting-on-windows-7"></a>在 Windows 7 上展示

在 Windows 7 上以 Direct3D 12 為目標時，不會顯示 Direct3D 12 的必要 DXGI 類型，因此您必須使用 D3D12On7 提供的 **ID3D12CommandQueueDownLevel** (從直接命令佇列中查詢，) 才會出現。

您可以將開啟的命令清單提供給 Windows 7 目前的方法，然後使用、關閉，並自動提交給裝置。 您必須提供必須為應用程式建立的後置緩衝區、必須是已認可的資源、必須是單一取樣，而且必須是下列其中一種格式。

* **DXGI_FORMAT_R16G16B16A16_FLOAT**
* **DXGI_FORMAT_R10G10B10A2_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**
* **DXGI_FORMAT_B8G8R8X8_UNORM**
* **DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**

## <a name="related-topics"></a>相關主題

* [D3D12_HEAP_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)
* [DirectX advanced learning 影片教學課程：調節幀](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [轉譯](rendering.md)
