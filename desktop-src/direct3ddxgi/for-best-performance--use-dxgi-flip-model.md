---
description: 本主題提供開發人員指引，說明如何在新式 Windows 的簡報堆疊中最大化效能和效率。
ms.assetid: B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1
title: 為了達到最佳效能，請使用 DXGI 翻轉模型
ms.topic: article
ms.date: 05/31/2018
ms.custom: RS5
ms.openlocfilehash: 2a1e671c03f468fd62b0b5bad0f008f84e62ca3c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106990917"
---
# <a name="for-best-performance-use-dxgi-flip-model"></a>為了達到最佳效能，請使用 DXGI 翻轉模型

本主題提供開發人員指引，說明如何在新式 Windows 的簡報堆疊中最大化效能和效率。 它會挑選 [DXGI 翻轉模型](dxgi-flip-model.md)、 [DirectX 12： Windows 10 中的簡報模式 (影片) ](https://www.youtube.com/watch?v=E3wTajGZOsA)，以及 [Windows 10 中的簡報增強：提早 (影片) ](https://www.youtube.com/watch?v=nUZVV_mssWQ) 。

## <a name="call-to-action"></a>喚起行動

如果您仍在使用 **dxgi \_ 交換 \_ 效果 \_ 捨棄** 或 **dxgi \_ swap \_ 效果 \_ 順序** (也稱為 「blt」) 目前的模型，這是時候停止的時候了！

切換至 **DXGI \_ 交換 \_ 效果會 \_ 翻轉 \_ 順序** 或 **DXGI \_ 交換效果，以 \_ \_ 反轉 \_** (也稱為 翻轉模型) 可提供較佳的效能、較低的耗電量，以及提供一組更豐富的功能。  (如需這些值的詳細資訊，請參閱 [DXGI \_ SWAP \_ 效果列舉](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) 。 ) 

相較于傳統的「全螢幕專屬」模式，翻轉模型的呈現方式，是讓視窗模式有效地等於或更好。 事實上，您可能會想要重新考慮您的應用程式是否真的需要全螢幕獨佔模式，因為 [翻轉模型無邊框] 視窗的優點包括更快的 Alt-Tab 切換，以及與新式顯示功能的整合更好。

為什麼是現在？ 在2018年4月更新之前，blt 模型會在混合式 GPU 設定（通常是在高階膝上型電腦上）（通常是在高階膝上型電腦 (參閱 [KB 3158621](https://support.microsoft.com/help/3158621/hybrid-graphics-and-vsync-results-in-graphic-tearing-in-some-games-and)) ）中使用，因此可能會導致顯示撕裂。 在2018年4月的更新中，已修正這項破壞，代價是有一些額外的工作。 如果您正在進行 blt，在混合式 Gpu 之間提供高 framerates，特別是在高解析度（例如4K）時，這種額外的工作可能會影響整體效能。 若要在這些系統上維持最佳效能，請從 blt 切換到「翻轉目前」模型。 此外，請考慮減少 swapchain 的解決方式，特別是如果它不是使用者 (互動的主要點，通常是使用 VR preview windows) 的情況。

## <a name="a-brief-history"></a>簡短歷程記錄

什麼是翻轉模型？ 替代方法是什麼？

在 Windows 7 之前，從 D3D 呈現內容的唯一方法是「blt」，或將它複製到視窗或螢幕所擁有的介面。 從 D3D9's FLIPEX swap 效果開始，到透過 \_ Windows 8 中的翻轉順序交換效果進入 DXGI，我們開發了一個更有效率的方式，就是使用最基本的桌面組合程式直接共用畫面上的內容，藉此將內容放在螢幕上。 如需此技術的概要說明，請參閱 [DXGI 翻轉模型](dxgi-flip-model.md) 。

這項優化是因為 DWM (桌面視窗管理員) ，也就是驅動 Windows 桌面的組合器。

## <a name="when-should-i-use-the-blt-model"></a>何時應該使用 blt 模型？

翻轉模型不提供一項功能，就是能夠擁有多個不同的 Api 來產生內容，這一切都是以並存的方式結合到相同的 **HWND** 中。 其中一個範例是使用 D3D 來繪製視窗背景，然後使用 [WINDOWS GDI](/windows/desktop/gdi/windows-gdi) 來繪製某個東西，或使用兩個不同的圖形 api，或使用來自相同 API 的兩個 swapchains，以產生替代的畫面格。 如果您不需要圖形元件之間的 **HWND** 層級 interop，則不需要 blt 模型。

原始的翻轉模型設計中未提供第二個功能，但現在已可供使用，這是以調節幀呈現的能力。 若為使用同步間隔0的應用程式，除非 [IDXGIFactory5：： CheckFeatureSupport](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) API 可供使用，否則不建議切換至 flip 模型，且支援的 **DXGI \_ 功能 \_ 目前 \_ 允許 \_** 卸載。 這項功能在最近版本的 Windows 10 和新式硬體上幾乎很普遍。

## <a name="directflip"></a>DirectFlip

如果您 [在 Windows 10 觀看了 DirectX 12：展示模式](https://www.youtube.com/watch?v=E3wTajGZOsA)，您會看到「直接翻轉」和「獨立翻轉」的相關討論。 這些是使用 flip model swapchains 為應用程式啟用的優化。 視視窗和緩衝區的設定而定，您可以完全略過桌面撰寫，並以專用的全螢幕方式直接將應用程式框架傳送到畫面。

在過去幾天，這些優化可以依照下列三種案例的其中一種來參與：

1.  **DirectFlip**：您的 swapchain 緩衝區符合螢幕尺寸，而您的視窗用戶端區域則涵蓋畫面。 應用程式 swapchain 是使用的，而不是使用 DWM swapchain 在螢幕上顯示。
2.  **具有面板 fitters 的 DirectFlip**：您的視窗用戶端區域涵蓋畫面，而您的 swapchain 緩衝區會在某些硬體相依的縮放比例內 (例如，螢幕的 0.25 x 至 4x) 。 GPU scanout 硬體可用來調整緩衝區，並將其傳送至顯示器。
3.  **具有多平面重迭 (MPO) 的 DirectFlip**：您的 swapchain 緩衝區會在視窗維度的某些硬體相依調整比例內。 DWM 可以為您的應用程式保留專用的硬體 scanout 平面，然後將它掃描出來，並將其延伸至螢幕的 Alpha 混合子領域。

使用視窗型翻轉模型，應用程式可以查詢不同 DirectFlip 案例的硬體支援，並透過使用 [IDXGIOutput6：： CheckHardwareCompositionSupport](/windows/desktop/api/DXGI1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport)來實行不同類型的動態調整。 要注意的一點是，如果使用了 panel fitters，資料指標可能會遇到延伸的副作用，這是透過 **DXGI \_ 硬體 \_ 組合 \_ 支援 \_ 旗 \_ \_** 標資料指標延展來指出。

一旦您的 swapchain 「DirectFlipped」之後，DWM 就可以進入睡眠狀態，而且只有在您的應用程式外部發生變更時才會喚醒。 您的應用程式框架會與全螢幕專屬的效率一樣，獨立地直接傳送到畫面。 這是「獨立翻轉」，可參與上述所有案例。 如果有其他桌面內容在最上層，則 DWM 可以順暢地轉換回組成的模式、有效率地將內容「反向撰寫」至應用程式前的內容，再進行翻轉，或利用 MPO 來維護獨立的翻轉模式。

查看 [PresentMon](https://github.com/GameTechDev/PresentMon) 工具以取得上述哪一個使用的見解。

## <a name="what-else-is-new-in-the-flip-model"></a>翻轉模型的新功能是什麼？

除了上述的增強功能（適用于標準 swapchains，而不需要特別特殊）之外，還有數個可供 flip 模型應用程式使用的功能：

-   使用 **DXGI \_ 交換 \_ 鏈旗標 \_ \_ 框架 \_ 延遲 \_ 可等候 \_ 物件** 來降低延遲。 在獨立的翻轉模式下，您可以在最新版本的 Windows 上獲得最少1個延遲的畫面格，並在撰寫時正常地回復至最小的可能。
    -   注意：發生問題，在 Windows 10 年度更新版及更早的版本中，至少有兩個延遲框架。 如需詳細資訊，請參閱 [此論壇主題](https://www.gamedev.net/forums/topic/686507-windows-10-dx12-low-latency-tearing-free-rendering/) 。 這在秋季建立者的更新中已修正。
-   **DXGI \_交換 \_ 效果 \_ 翻轉 \_ 捨棄** 可啟用「反轉合成」模式的直接翻轉，這會導致顯示桌面的整體工作較少。 DWM 可以在應用程式緩衝區上塗抹，然後將它們傳送到畫面，而不是在自己的 swapchains 中執行完整複製。
-   **DXGI \_交換 \_ 鏈 \_ 旗 \_ \_** 標即使在具有多平面重迭支援的系統上，即使在具有多平面重迭支援之系統上的視窗中，也能讓您的延遲比可等候物件
-   應用程式可控制在調整視窗大小時發生的內容調整，使用 swapchain 建立期間設定的 [DXGI \_ 調整](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling) 屬性。
-   HDR 格式的內容 (R10G10B10A2 \_ UNORM 或 R16G16B16A16 \_ FLOAT) 不會壓制，除非它是由 SDR 桌面組成。
-   顯示統計資料可在視窗模式中取得。
-   與 UWP (通用 Windows 平臺) 應用程式模型和 DX12 的相容性更高，因為這些只與 flip 模型相容。

## <a name="what-do-i-have-to-do-to-use-the-flip-model"></a>使用翻轉模型需要做什麼？

Flip 模型 swapchains 在 blt swapchains 之上有一些額外的需求：

1.  緩衝區計數必須至少為2。
2.  在 [出現](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) 呼叫之後，必須明確地將背景緩衝區重新系結至 D3D11 立即內容，才能再次使用。
3.  在呼叫 [SetFullscreenState](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)之後，應用程式必須在 **出現** 之前呼叫 [ResizeBuffers](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) 。
4.  MSAA (非取樣式消除鋸齒) swapchains 不會直接在翻轉模型中受到支援，因此應用程式必須先進行 MSAA 解析，然後再發出 **目前** 的。

## <a name="how-to-choose-the-right-rendering-and-presentation-resolutions"></a>如何選擇正確的轉譯和呈現解決方案

過去傳統的應用程式模式，是在使用者選取專用的全螢幕模式時，為使用者提供可供選擇的解決方案清單。 利用新式顯示器順暢地開始調整內容的能力，請考慮讓使用者能夠選擇轉譯解析度以進行效能調整，而不受輸出解析度影響，甚至是在視窗模式中。 此外，應用程式應該利用 **IDXGIOutput6：： CheckHardwareCompositionSupport** 來判斷他們是否需要在呈現內容之前先調整內容，或是應該讓硬體進行調整。

您的內容可能需要從一個 GPU 遷移到另一個 GPU，作為目前或組合作業的一部分。 這通常適用于多 GPU 膝上型電腦，或是已插入外部 Gpu 的系統。 當這些設定變得更常見，且高解析度顯示變得更常見時，呈現完整解析度 swapchain 的成本會增加。 如果您 swapchain 的目標不是使用者互動的主要點，則在使用 VR 標題（將 VR 場景的2D 預覽呈現至次要視窗）的情況下，請考慮使用較低的解析度 swapchain，將需要傳輸到不同 Gpu 的頻寬量降至最低。

## <a name="other-considerations"></a>其他考量

當您第一次要求 GPU 寫入 swapchain 背景緩衝區時，是 GPU 將會停止等候緩衝區變成可用狀態的時間。 可能的話，請盡可能將此點延遲到框架中。

 

 
