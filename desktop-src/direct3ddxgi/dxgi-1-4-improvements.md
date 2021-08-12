---
description: Microsoft DirectX Graphic Infrastructure (DXGI) 1.4 新增或變更了下列功能，主要是支援 Direct3D 12。
ms.assetid: DEA901EA-B0F9-41D9-802C-ED1D6A7888E0
title: DXGI 1.4 改進
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef5777f50a149da6ccb2893bcac8a8f509c86cdff40d94889155c2e5e1eb12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289552"
---
# <a name="dxgi-14-improvements"></a>DXGI 1.4 改進

Microsoft DirectX Graphic Infrastructure (DXGI) 1.4 新增或變更了下列功能，主要是支援 Direct3D 12。

## <a name="cheaper-adapter-enumeration"></a>較便宜的介面卡列舉

針對 Direct3D 12，無法再從裝置回溯至用來建立它的 [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) 。 也無法再將 D3D \_ 驅動程式類型的扭曲提供給 \_ \_ [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)。 若要更輕鬆地進行開發，您可以使用 [**IDXGIFactory4**](/windows/win32/api/DXGI1_4/nn-dxgi1_4-idxgifactory4) 來處理這兩者。 [**IDXGIFactory4：： EnumAdapterByLuid**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid) (設計成與 [**ID3D12Device：：) GetAdapterLuid**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid) 配對，可讓應用程式抓取建立 Direct3D 12 裝置的介面卡相關資訊。 [**IDXGIFactory4：： EnumWarpAdapter**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter) 提供可提供給 **D3D12CreateDevice** 使用變形轉譯器的介面卡。

## <a name="video-memory-budget-tracking"></a>影片記憶體預算追蹤

建議應用程式開發人員使用視訊記憶體保留系統，以通知作業系統沒有應用程式無法移出的實體視訊記憶體數量。

進程可用的實體記憶體數量稱為「影片記憶體預算」。 在背景進程喚醒和睡眠的情況下，預算可能會明顯波動;當使用者切換到另一個應用程式時，就會大幅波動。 當預算變更時，應用程式可以收到通知，而且會輪詢目前的預算和目前耗用的記憶體數量。 如果應用程式不在其預算內，則會間歇性凍結程式以允許其他應用程式執行，並/或建立 Api 將會傳回失敗。 [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3)介面提供與這項功能有關的方法，特別是 [**QueryVideoMemoryInfo**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo)和 [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent)。

如需詳細資訊，請參閱「 [常駐](../direct3d12/residency.md)」上的 Direct3D 12 主題。

## <a name="direct3d-12-swapchain-changes"></a>Direct3D 12 Swapchain 變更

某些現有的 Direct3D 11 swapchain 功能已被取代，以達到 Direct3D 12 的額外負擔。 雖然已對 Direct3D 12 的概念進行其他變更，或為 Direct3D 12 功能提供更好的支援。

**不變背景緩衝區身分識別**

在 Direct3D 11 中，應用程式可以呼叫 [**GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) ( 0，.。。 僅 ) 一次。 每個 [**出現**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-present) 的呼叫都會以隱含方式變更所傳回介面的資源識別。 由於所需的 CPU 負擔和彈性的資源描述項設計，Direct3D 12 不再支援該隱含資源身分識別變更。 因此，應用程式必須針對每個使用 swapchain 所建立的緩衝區，以手動方式呼叫 **GetBuffer** 。 應用程式必須 **在呼叫後**，以手動方式轉譯為序列中的下一個緩衝區。 建議應用程式為 **每個緩衝區** 建立描述項的快取，而不是重新建立每個緩衝區的最多物件。

**多介面卡支援**

在多重 GPU 介面卡上建立 swapchain 時，會在節點1上建立 backbuffers，而且只支援單一命令佇列。 [**ResizeBuffers1**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1) 可讓應用程式在不同的節點上建立 backbuffers，讓不同的命令佇列可以搭配使用。 這些功能可 (AFR) 技術，以搭配 swapchain 使用，以提供替代的框架轉譯。 請參閱 [多介面卡系統](../direct3d12/multi-engine.md)。

**其他**

-   必須將命令佇列物件傳遞給 [**CreateSwapChain**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-createswapchain) 方法，而不是 Direct3D 12 裝置物件。
-   只支援下列兩個 flip 模型交換效果： <dl> \_ \_ \_ \_ 當應用程式在呈現之前完全轉譯背景緩衝區，或想要輕鬆地支援多個介面卡案例時，建議您最好採用 DXGI 交換效果翻轉捨棄。  
    \_ \_ \_ \_ 使用部分呈現優化或定期從先前顯示的 backbuffers 中讀取的應用程式應該使用 DXGI 交換效果反轉順序。  
    </dl>
-   [**SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) no longer exclusively owns the display, so user-initiated operating system elements can seamlessly appear in front of application output. Volume settings is an example of this.

## <a name="related-topics"></a>相關主題

[Direct3D 12 硬體功能等級](../direct3d12/hardware-feature-levels.md)

[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
