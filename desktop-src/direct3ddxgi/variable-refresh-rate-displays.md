---
description: 變數重新整理率顯示需要卸載才能啟用，這也稱為 &\# 0034; vsync&\# 0034; 支援。
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: 變數重新整理率顯示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6e658d84c51a6b51bc32855226194b9c22507e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187447"
---
# <a name="variable-refresh-rate-displays"></a><span data-ttu-id="e6fc5-103">變數重新整理率顯示</span><span class="sxs-lookup"><span data-stu-id="e6fc5-103">Variable refresh rate displays</span></span>

<span data-ttu-id="e6fc5-104">變數重新整理率顯示 *需要卸載* 才能啟用，這也稱為「vsync 關閉」支援。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-104">Variable refresh rate displays require *tearing* to be enabled, this is also known as "vsync-off" support.</span></span>

-   [<span data-ttu-id="e6fc5-105">變數重新整理率顯示/Vsync 關閉</span><span class="sxs-lookup"><span data-stu-id="e6fc5-105">Variable refresh rate displays/Vsync off</span></span>](#variable-refresh-rate-displaysvsync-off)
-   [<span data-ttu-id="e6fc5-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6fc5-106">Related topics</span></span>](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a><span data-ttu-id="e6fc5-107">變數重新整理率顯示/Vsync 關閉</span><span class="sxs-lookup"><span data-stu-id="e6fc5-107">Variable refresh rate displays/Vsync off</span></span>

<span data-ttu-id="e6fc5-108">您可以在建立和呈現交換鏈時設定某些旗標，藉以支援變數重新整理率顯示。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-108">Support for variable refresh rate displays is achieved by setting certain flags when creating and presenting the swap chain.</span></span>

<span data-ttu-id="e6fc5-109">若要使用這項功能，應用程式使用者必須在已安裝 [KB3156421](https://support.microsoft.com/kb/3156421) 或年度更新版的 Windows 10 系統上。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-109">To use this feature, app users need to be on Windows 10 systems with either [KB3156421](https://support.microsoft.com/kb/3156421) or the Anniversary Update installed.</span></span> <span data-ttu-id="e6fc5-110">這項功能適用于所有版本的 Direct3D 11 和12（使用 \**DXGI \_ 交換 \_ 效果 \_ FLIP \_ \** _ 交換效果）。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-110">The feature works on all versions of Direct3D 11 and 12 using \**DXGI\_SWAP\_EFFECT\_FLIP\_\** _ swap effects.</span></span>

<span data-ttu-id="e6fc5-111">若要將 vsync 支援新增至您的應用程式，您可以參考 Direct3D 12 的完整執行範例，_ *D3D12Fullscreen*\* (請參閱) 的 [工作範例](../direct3d12/working-samples.md) 。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-111">To add vsync-off support to your apps, you can refer to a complete running sample for Direct3D 12, _ *D3D12Fullscreen*\* (refer to [Working Samples](../direct3d12/working-samples.md)).</span></span> <span data-ttu-id="e6fc5-112">在範例程式碼中也不會明確地呼叫幾個點，但您必須注意。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-112">There are also a few points not explicitly called out in the sample code but you need to pay attention to.</span></span>

-   <span data-ttu-id="e6fc5-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (或 [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) 必須具有相同的交換鏈建立旗標 (DXGI \_ 交換 \_ 鏈旗標允許將 \_ \_ \_) 傳遞給 [](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present)它， (或 [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)) 。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (or [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) must have the same swap chain creation flag (DXGI\_SWAP\_CHAIN\_FLAG\_ALLOW\_TEARING) passed to it as [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (or [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span></span>
-   <span data-ttu-id="e6fc5-114">\_有 DXGI 存在 \_ ， \_ 只可搭配同步處理間隔0使用。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-114">DXGI\_PRESENT\_ALLOW\_TEARING can only be used with sync interval 0.</span></span> <span data-ttu-id="e6fc5-115">當使用同步處理間隔0時，建議您一律傳遞此撕裂旗標（如果 [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) 回報有可能會卸載，而且應用程式處於視窗模式） *，* 包括不含框線的全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-115">It is recommended to always pass this tearing flag when using sync interval 0 if [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) reports that tearing is supported *and* the app is in a windowed mode - including border-less fullscreen mode.</span></span> <span data-ttu-id="e6fc5-116">如需詳細資訊，請參閱 [**DXGI \_ 呈現**](dxgi-present.md) 常數。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-116">Refer to the [**DXGI\_PRESENT**](dxgi-present.md) constants for more details.</span></span>
-   <span data-ttu-id="e6fc5-117">停用 vsync 並不一定會 uncap 您的畫面播放速率：開發人員也必須確定 [**存在**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) 的呼叫不會受到其他計時事件的節流 (例如以 `CompositionTarget::Rendering` XAML 為基礎的應用程式) 中的事件。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-117">Disabling vsync does not necessarily uncap your frame rate: developers also need to make sure [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) calls are not throttled by other timing events (such as the `CompositionTarget::Rendering` event in an XAML-based app).</span></span>

<span data-ttu-id="e6fc5-118">下列程式碼會回顧一些您需要新增到應用程式的重要部分。</span><span class="sxs-lookup"><span data-stu-id="e6fc5-118">The code below recaps a few key pieces you need to add to your apps.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e6fc5-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6fc5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6fc5-120">DXGI 1.5 改進</span><span class="sxs-lookup"><span data-stu-id="e6fc5-120">DXGI 1.5 Improvements</span></span>](dxgi-1-5-improvements.md)
</dt> <dt>

[<span data-ttu-id="e6fc5-121">DXGI 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="e6fc5-121">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
