---
description: 變數重新整理率顯示需要卸載才能啟用，這也稱為 &\# 0034; vsync&\# 0034; 支援。
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: 變數重新整理率顯示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349592ce49d1008f6337b53c7f524ac7303907f75cd99205fe79bf55988b934b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288921"
---
# <a name="variable-refresh-rate-displays"></a>變數重新整理率顯示

變數重新整理率顯示 *需要卸載* 才能啟用，這也稱為「vsync 關閉」支援。

-   [變數重新整理率顯示/Vsync 關閉](#variable-refresh-rate-displaysvsync-off)
-   [相關主題](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>變數重新整理率顯示/Vsync 關閉

您可以在建立和呈現交換鏈時設定某些旗標，藉以支援變數重新整理率顯示。

若要使用這項功能，應用程式使用者必須在已安裝[KB3156421](https://support.microsoft.com/kb/3156421)或年度更新版的 Windows 10 系統上。 這項功能適用于所有版本的 Direct3D 11 和12（使用 **DXGI \_ 交換 \_ 效果 \_ 翻轉 \_ \*** 交換效果）。

若要將 vsync 支援新增至您的應用程式，您可以參考 Direct3D 12 的完整執行範例， **D3D12Fullscreen** (請參閱) 的 [工作範例](../direct3d12/working-samples.md) 。 在範例程式碼中也不會明確地呼叫幾個點，但您必須注意。

-   [**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (或 [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) 必須具有相同的交換鏈建立旗標 (DXGI \_ 交換 \_ 鏈旗標允許將 \_ \_ \_) 傳遞給 [](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present)它， (或 [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)) 。
-   \_有 DXGI 存在 \_ ， \_ 只可搭配同步處理間隔0使用。 當使用同步處理間隔0時，建議您一律傳遞此撕裂旗標（如果 [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) 回報有可能會卸載，而且應用程式處於視窗模式） *，* 包括不含框線的全螢幕模式。 如需詳細資訊，請參閱 [**DXGI \_ 呈現**](dxgi-present.md) 常數。
-   停用 vsync 並不一定會 uncap 您的畫面播放速率：開發人員也必須確定 [**存在**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) 的呼叫不會受到其他計時事件的節流 (例如以 `CompositionTarget::Rendering` XAML 為基礎的應用程式) 中的事件。

下列程式碼會回顧一些您需要新增到應用程式的重要部分。

``` syntax
//--------------------------------------------------------------------------------------------------------
// Check Tearing Support
//--------------------------------------------------------------------------------------------------------

// Determines whether tearing support is available for fullscreen borderless windows.

void DXSample::CheckTearingSupport()
{
// Rather than create the 1.5 factory interface directly, we create the 1.4
// interface and query for the 1.5 interface. This will enable the graphics
// debugging tools which might not support the 1.5 factory interface.

    ComPtr<IDXGIFactory4> factory4;
    HRESULT hr = CreateDXGIFactory1(IID_PPV_ARGS(&factory4));
    BOOL allowTearing = FALSE;
    if (SUCCEEDED(hr))
    { 
        ComPtr<IDXGIFactory5> factory5;
        hr = factory4.As(&factory5);
        if (SUCCEEDED(hr))
        {
            hr = factory5->CheckFeatureSupport(DXGI_FEATURE_PRESENT_ALLOW_TEARING, &allowTearing, sizeof(allowTearing));
        }
    }
    m_tearingSupport = SUCCEEDED(hr) && allowTearing;
}

//--------------------------------------------------------------------------------------------------------
// Set up swapchain properly
//--------------------------------------------------------------------------------------------------------

// It is recommended to always use the tearing flag when it is supported.
swapChainDesc.Flags = m_tearingSupport ? DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING : 0;

//--------------------------------------------------------------------------------------------------------
// Present
//--------------------------------------------------------------------------------------------------------

UINT presentFlags = (m_tearingSupport && m_windowedMode) ? DXGI_PRESENT_ALLOW_TEARING : 0;

// Present the frame.
ThrowIfFailed(m_swapChain->Present(0, presentFlags));
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXGI 1.5 改進](dxgi-1-5-improvements.md)
</dt> <dt>

[DXGI 的程式設計指南](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
