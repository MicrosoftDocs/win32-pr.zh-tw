---
description: Windows 8 在 DXGI 1.2 中新增對 flip 展示模型及其相關聯的目前統計資料的支援。
ms.assetid: E132DAF5-80B7-4C52-A760-3779CC140CE7
title: DXGI 翻轉模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ee82febd13a3b57a06d93fd01eb8d230d6b78a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846404"
---
# <a name="dxgi-flip-model"></a>DXGI 翻轉模型

Windows 8 在 DXGI 1.2 中新增對 flip 展示模型及其相關聯的目前統計資料的支援。 Windows 8 的 DXGI 翻轉表示模型類似于 Windows 7 的 [DIRECT3D 9EX 翻轉模式展示](../direct3darticles/direct3d-9ex-improvements.md)。 以影片或畫面播放速率為基礎的展示應用程式（例如遊戲）可以利用翻轉簡報模型來獲益。 使用 DXGI 反轉展示模型的應用程式可降低系統資源的載入並提升效能。 應用程式也可以透過提供即時意見反應和修正機制，使用目前的統計資料增強功能搭配翻轉展示模型，更有效地控制簡報率。

-   [比較 DXGI 翻轉模型和 BitBlt 模型](#comparing-the-dxgi-flip-model-and-the-bitblt-model)
-   [如何使用 DXGI 翻轉模型](#how-to-use-dxgi-flip-model)
-   [DXGI 翻轉模型應用程式的框架同步處理](#frame-synchronization-of-dxgi-flip-model-apps)
-   [避免、偵測和從問題中復原](#avoiding-detecting-and-recovering-from-glitches)
-   [相關主題](#related-topics)

## <a name="comparing-the-dxgi-flip-model-and-the-bitblt-model"></a>比較 DXGI 翻轉模型和 BitBlt 模型

執行時間會使用位區塊傳輸 (bitblt) 並翻轉簡報模型，以在顯示監視器上顯示圖形內容。 Bitblt 和翻轉展示模型之間的最大差異，在於背景緩衝區內容如何取得 Windows 8 DWM 以進行組合。 在 bitblt 模型中，會在每次呼叫 IDXGISwapChain1 時，將背景緩衝區的內容複寫到重新導向介面 [**：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)。 在反轉模型中，所有背景緩衝區都會與桌面視窗管理員 (DWM) 共用。 因此，DWM 可以直接從這些背景緩衝區中撰寫，而不需要任何額外的複製作業。 一般而言，翻轉模型較有效率。 翻轉模型也提供更多功能，例如增強的目前統計資料。

如果您有使用 Windows 圖形裝置介面 (GDI) 直接寫入 [**HWND**](../winprog/windows-data-types.md) 的舊版元件，請使用 bitblt 模型。

當應用程式處於視窗模式時，DXGI 翻轉模型的效能改進相當重要。 此表格中的順序和圖例比較記憶體頻寬的使用方式，以及選擇翻轉模型與 bitblt 模型的視窗化應用程式的系統讀取和寫入。



| 步驟 | BitBlt 模型存在於 DWM                                                                               | 對 DWM 呈現的 DXGI 反轉模型                                   |
|------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 1.   | 應用程式會更新其框架 (寫入) <br/>                                                              | 應用程式會更新其框架 (寫入) <br/>                     |
| 2.   | Direct3D runtime 會將介面內容複寫到 DWM 重新導向介面 (讀取、寫入) <br/>            | Direct3D runtime 將應用程式介面傳遞至 DWM<br/>        |
| 3.   | 共用的表面複製完成之後，DWM 會將應用程式介面轉譯至螢幕 (讀取、寫入) <br/> | DWM 會將應用程式介面轉譯至螢幕 (讀取、寫入) <br/> |



 

![比較 blt 模型和翻轉模型的圖例](images/blt-flip-mode-present.png)

Flip 模型藉由針對 DWM 的視窗化框架組合，減少 Direct3D runtime 的讀取和寫入次數，以減少系統記憶體使用量。

## <a name="how-to-use-dxgi-flip-model"></a>如何使用 DXGI 翻轉模型

以 Windows 8 為目標的 Direct3D 11.1 應用程式會藉由建立具有 [**dxgi \_ 交換 \_ 效果 \_ \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)的交換鏈，以反轉在 [**dxgi \_ 交換 \_ 鏈 \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)結構的 **SwapEffect** 成員中設定的連續列舉值，來使用 flip 模型。 當您將 **SwapEffect** 設定為 [ **dxgi \_ 交換 \_ 效果] \_ 反向 \_** 時，也請將 [ **dxgi \_ 交換 \_ 鏈 \_ DESC1** ] 的這些成員設定為指定的值：

-   **BufferCount** 至介於2到16之間的值，以避免因為等待 DWM 釋出先前的展示緩衝區而導致效能下降。
-   將格式 **設定** 為 DXGI \_ 格式 \_ R16G16B16A16 \_ FLOAT、DXGI \_ format \_ B8G8R8A8 \_ UNORM 或 dxgi \_ format \_ R8G8B8A8 \_ UNORM
-   **SampleDesc** 成員所指定之 [**dxgi 範例 \_ \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc)結構的 **計數****成員，** 因為不支援多個範例消除鋸齒 (MSAA) **\_ \_**

如果您在 Windows 7 或更早版本的作業系統上使用 [**DXGI \_ 交換 \_ 效果 \_ 反轉 \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) ，則裝置建立會失敗。 當您使用翻轉模型時，您可以在視窗模式中使用全螢幕的顯示統計資料。 全螢幕的行為不會受到影響。 如果您將 **Null** 傳遞給視窗型交換鏈的 [**IDXGIFactory2：： CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)的 *PFullscreenDesc* 參數，並將 **SwapEffect** 設定為 **DXGI \_ 交換效果的 \_ \_ \_ 順序**，則執行時間會建立一個額外的背景緩衝區，並將任何控制碼都轉換成在呈現時成為前端緩衝區的緩衝區。

當您使用 flip 模型時，請考慮下列秘訣：

-   每個 [**HWND**](../winprog/windows-data-types.md)使用一個翻轉模型交換鏈。 請勿將多個翻轉模型交換鏈的目標設為相同的 **HWND**。
-   請勿搭配 GDI 的 [**ScrollWindow**](/windows/win32/api/winuser/nf-winuser-scrollwindow) 或 [**ScrollWindowEx**](/windows/win32/api/winuser/nf-winuser-scrollwindowex) 函式使用翻轉模型交換鏈。 某些 Direct3D 應用程式會在使用者滾動事件發生後，使用 GDI 的 **ScrollWindow** 和 **ScrollWindowEx** 函數來更新視窗內容。 **ScrollWindow** 和 **ScrollWindowEx** 會在使用者滾動視窗時，在螢幕上執行視窗內容的 bitblts。 這些函式也需要 GDI 和 Direct3D 內容的 bitblt 模型更新。 當應用程式處於視窗模式時，使用任一功能的應用程式不一定會在螢幕上顯示可見的視窗內容滾動。 我們建議您不要使用 GDI 的 **ScrollWindow** 和 **ScrollWindowEx** 函式，而是改為在螢幕上重新繪製 gdi 和 Direct3D 內容以回應滾動。
-   在不是其他 Api （包括 DXGI bitblt 展示模型、其他版本的 Direct3D 或 GDI）的 [**HWND**](../winprog/windows-data-types.md) 中使用翻轉模型。 因為 bitblt 模型會維護一個額外的介面複本，所以您可以透過 Direct3D 和 GDI 的分次更新，將 GDI 和其他 Direct3D 內容新增至相同的 **HWND** 。 當您使用翻轉模型時，只會看到執行時間傳遞給 DWM 之翻轉模型交換鏈中的 Direct3D 內容。 執行時間會忽略所有其他 bitblt 模型 Direct3D 或 GDI 內容更新。

## <a name="frame-synchronization-of-dxgi-flip-model-apps"></a>DXGI 翻轉模型應用程式的框架同步處理

目前的統計資料是媒體應用程式用來同步處理影片和音訊串流以及從影片播放問題復原的畫面格時間資訊。 應用程式可以使用目前統計資料中的畫面格時間資訊，來調整其影片畫面的呈現率，以提供更流暢的簡報。 若要取得目前的統計資料資訊，請呼叫 [**IDXGISwapChain：： GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) 方法以取得 [**DXGI \_ 框架 \_ 統計資料**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics) 結構。 **DXGI \_畫面格 \_ 統計資料** 報含 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) 呼叫的相關統計資料。 翻轉模型交換鏈會以視窗模式和全螢幕模式提供目前的統計資料資訊。 若為視窗模式中的 bitblt 模型交換鏈，所有的 **DXGI \_ 框架 \_ 統計資料** 值都是零。

若為 flip 模型目前的統計資料， [**IDXGISwapChain：： GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics) 會在這些情況下傳回非 **\_ 交集的錯誤 \_ 框架 \_ 統計資料 \_** ：

-   第一次呼叫 [**GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics)，表示序列的開頭
-   模式變更：以視窗模式切換至全螢幕或全螢幕到全螢幕轉換

[**DXGI \_ 框架 \_ 統計資料**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics)的 **PresentRefreshCount**、 **SyncRefreshCount** 和 **SyncQPCTime** 成員中的值具有下列特性：

-   當應用程式在每個 vsync 上呈現時， **PresentRefreshCount** 等於 **SyncRefreshCount** 。
-   當提交目前的時間時，會在 vsync 間隔取得 **SyncRefreshCount** ， **SyncQPCTime** 大約是與 vsync 間隔相關聯的時間。

[**IDXGISwapChain：： GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount)方法會傳回最後一個最新的計數，也就是與交換鏈相關聯之顯示裝置所進行的最後一個成功 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)呼叫的目前識別碼。 此存在識別碼是 [**DXGI \_ 框架 \_ 統計資料**](/windows/desktop/api/DXGI/ns-dxgi-dxgi_frame_statistics)結構的 **PresentCount** 成員的值。 針對 bitblt 模型交換鏈，在視窗模式中，所有的 **DXGI \_ 框架 \_ 統計資料** 值都是零。

## <a name="avoiding-detecting-and-recovering-from-glitches"></a>避免、偵測和從問題中復原

執行這些步驟，以避免、偵測和復原框架簡報中的問題：

1.  佇列 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (呼叫，也就是呼叫 **IDXGISwapChain1：:P resent1** 多次，這會導致它們在佇列) 中收集。
2.  建立目前的佇列結構來儲存所有成功提交的 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)的目前識別碼 (由 [**IDXGISwapChain：： GetLastPresentCount**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getlastpresentcount) 傳回) 以及相關聯的計算/預期 **PresentRefreshCount** 值。
3.  若要偵測出問題：

    -   呼叫 [**IDXGISwapChain：： GetFrameStatistics**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-getframestatistics)。
    -   針對此框架，請取得 (**PresentCount**) 和 vsync 計數的目前識別碼，其中作業系統會將最後一個影像呈現給監視器 (**PresentRefreshCount**) 。
    -   取得與目前識別碼相關聯的預期 **PresentRefreshCount** ，以及您先前儲存在目前佇列結構中的識別碼。
    -   如果實際的 **PresentRefreshCount** 晚于預期的 **PresentRefreshCount**，就會發生問題。

4.  若要從問題中復原：

    -   計算要跳到從問題中復原的畫面格數。 例如，如果步驟3顯示 () **PresentRefreshCount** 的預期 vsync 計數 (**PresentCount**) 為5，而目前識別碼的實際 vsync 計數是8，則要從問題中略過的畫面格數目是3個畫面格。
    -   將0傳遞給 IDXGISwapChain1 的呼叫次數 *SyncInterval* 參數 [**：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) ，以捨棄並略過此數目的畫面格。

        > [!Note]  
        > 如果問題是由大量的框架所組成，請呼叫 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) ，並將 *旗標* 參數設定為 [**DXGI \_ 存在 \_ 重新開機**](dxgi-present.md) ，以捨棄並略過所有未完成佇列的呈現。

         

以下是從畫面格簡報中復原問題的範例案例：

![在畫面格簡報中從問題中復原的範例案例圖例](images/frame-sync-glitch-recover.png)

在範例案例中，您預期畫面格 A 在 vsync 計數為1時進入螢幕。 但是您實際上會偵測到畫面上顯示為4的 vsync 計數。 因此，您可以判斷發生問題。 然後，您可以捨棄3個框架，也就是您可以將0傳遞給 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)的3個呼叫中的 *SyncInterval* 參數。 在上述範例案例中，若要從問題中復原，您需要總共8個 **IDXGISwapChain1：:P resent1** 的呼叫。 然後，會根據您預期的 vsync 計數來顯示第9個框架。

以下是簡報事件的時間表。 每個垂直線都代表一個 vsync。 水準方向是時間，會增加到右邊。 您可以使用此圖來想像問題可能發生的情況。

![展示 eventsl 的時間行圖例](images/present-timeline.png)

下圖說明此順序：

1.  應用程式會在 vsync 上喚醒、轉譯藍色、呼叫 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)，然後回到睡眠狀態。
2.  圖形處理單元 (GPU) 從閒置喚醒、執行轉譯為藍色，然後返回睡眠狀態。
3.  DWM 會在下一個 vsync 中喚醒，並在其背景緩衝區中組成藍色，呼叫 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)，然後回到睡眠狀態。
4.  應用程式會喚醒、呈現綠色、呼叫 [**IDXGISwapChain1：:P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)，然後回到睡眠狀態。
    > [!Note]  
    > 當 GPU 執行藍色的組合時，應用程式會同時執行。

     

5.  接下來，GPU 會為應用程式呈現綠色。
6.  最後，數位到類比轉換器 (DAC) 在下一個 vsync 上顯示監視器上的 DWM 組合結果。

從時間表中，您可以想像出現統計資料的延遲，以及可能發生問題的方式。 例如，若要顯示幕幕上出現的綠色色彩的 DWM 問題，請想像 [擴展綠色/紅色] 方塊，讓綠色/紅色方塊的右邊符合紫色/紅色方塊的右邊。 在此案例中，DAC 會顯示兩個藍色框架，然後顯示綠色框架。 您可以看到這種問題發生于讀取目前的統計資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用翻轉模型、中途矩形和捲動區域增強簡報](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
