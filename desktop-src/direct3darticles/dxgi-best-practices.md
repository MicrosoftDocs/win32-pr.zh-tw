---
title: DirectX Graphic Infrastructure (DXGI) 最佳作法
description: 本文討論主要的移植問題。
ms.assetid: 2df92ffe-1bfc-d682-2770-20cf0c831c9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be992fe2346868eb3481482325297a2c9ec27ee61bdd2c65f83b0f916fc22308
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290235"
---
# <a name="directx-graphics-infrastructure-dxgi-best-practices"></a>DirectX Graphic Infrastructure (DXGI) ：最佳作法

Microsoft DirectX Graphics Infrastructure (DXGI) 是新的子系統，其在封裝部分 Direct3D 10、10.1、11 和 11.1 所需低層級工作的 Windows Vista 中引進， 從 Direct3D 9 程式設計師的觀點來看，DXGI 包含了大部分的程式碼，可供列舉、交換鏈建立，以及之前封裝至 Direct3D 9 Api 的簡報。 當您將應用程式移植至 DXGI 和 Direct3D 2.x 和 Direct3D 11. x 時，您需要考慮一些考慮，以確保進程能順利執行。

本文討論主要的移植問題。

-   [全螢幕問題](#full-screen-issues)
-   [多個監視器](#multiple-monitors)
-   [視窗樣式和 DXGI](#window-styles-and-dxgi)
-   [多執行緒和 DXGI](#multithreading-and-dxgi)
-   [Gamma 和 DXGI](#gamma-and-dxgi)
-   [DXGI 1。1](#dxgi-11)
-   [DXGI 1。2](#dxgi-12)

## <a name="full-screen-issues"></a>Full-Screen 問題

從 Direct3D 9 移植至 DXGI 以及 Direct3D 2.x 或 Direct3D 11. x，與從視窗間移至全螢幕模式的相關問題通常可能會造成開發人員的麻煩。 主要的問題是因為 Direct3D 9 應用程式與 DXGI 應用程式不同，所以需要更多實際操作的方法來追蹤視窗樣式和視窗狀態。 當模式變更程式碼移植到在 DXGI 上執行時，通常會造成非預期的行為。

通常，Direct3D 9 應用程式會藉由設定前端緩衝區的解析度、強制裝置進入全螢幕獨佔模式，然後將背景緩衝區解析度設定為相符，來處理轉換成全螢幕模式。 不同的路徑用於視窗大小的變更，因為每當應用程式收到 WM 大小的訊息時，都必須從視窗進程進行管理 \_ 。

DXGI 藉由結合這兩種案例來嘗試簡化此方法。 例如，當視窗框線以視窗模式拖曳時，應用程式會收到 WM 大小的 \_ 訊息。 DXGI 會攔截這則訊息，並自動調整前端緩衝區的大小。 應用程式所需執行的工作，就是呼叫 [**IDXGISwapChain：： ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) ，將背景緩衝區大小調整成以 WM 大小的參數傳遞的大小 \_ 。 同樣地，當應用程式需要在全螢幕和視窗模式之間切換時，應用程式可以直接呼叫 [**IDXGISwapChain：： SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)。 DXGI 會調整前端緩衝區大小以符合新選取的全螢幕模式，並將 WM 大小的 \_ 訊息傳送至應用程式。 應用程式會再次呼叫 **ResizeBuffers**，就像是拖曳視窗框線一樣。

上述說明的方法會遵循非常特殊的路徑。 DXGI 預設會將全螢幕解析度設定為桌面解析度。 不過，許多應用程式會切換至慣用的全螢幕解析度。 在這種情況下，DXGI 提供 [**IDXGISwapChain：： ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)。 這應該在呼叫 [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)之前呼叫。 雖然這些方法可以依相反順序呼叫 (**SetFullscreenState** ，接著 **ResizeTarget**) ，這樣做會導致額外的 WM \_ 大小訊息傳送至應用程式。  (這麼做也會導致閃爍，因為 DXGI 可能會強制執行兩個模式的變更 ) 。呼叫 **SetFullscreenState** 之後，建議您再次呼叫 **ResizeTarget** ，並將 [**dxgi \_ 模式 \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85))的 **RefreshRate** 成員設為零。這在 DXGI 中不是作業指令，但可以避免重新整理頻率的問題，接下來將會討論。

處於全螢幕模式時，會停用桌面視窗管理員 (DWM) 。 DXGI 可以執行翻轉來呈現背景緩衝區內容，而不是執行 array.blit，這會在視窗模式中執行。 但是，如果不符合特定的需求，此效能增益可能會復原。 為了確保 DXGI 會進行翻轉而非 array.blit，前端緩衝區和背景緩衝區的大小必須相同。 如果應用程式正確處理其 WM \_ 大小的訊息，這應該不會造成問題。 此外，格式必須相同。

大部分應用程式的問題都是重新整理頻率。 在 [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) 的呼叫中指定的重新整理速率必須是由交換鏈所使用的 [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) 物件所列舉的更新速率。 如果應用程式零出傳遞至 **ResizeTarget** 的 [**Dxgi \_ 模式 \_ DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) **RefreshRate** 成員，則 DXGI 可以自動計算此值。 請務必不要假設一定會支援特定的重新整理頻率，並且只是將值硬式編碼。 開發人員通常會選擇 60 Hz 作為重新整理頻率，而不知道來自監視器的列舉重新整理率大約是監視器的 60000/1001 Hz。 如果重新整理率不符合預期的重新整理速率60，則會強制執行 DXGI 以全螢幕模式執行 array.blit，而不是翻轉。

開發人員經常面臨的最後一個問題，就是如何在全螢幕模式下變更全螢幕解析度。 呼叫 [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) 和 [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) 有時會成功，但全螢幕解析度仍會保持桌面解析度。 此外，開發人員也可以建立全螢幕的交換鏈，並提供特定的解決方式，只是要找出所有傳入的數位都是電腦解析度的預設值。 除非另有指示，否則 DXGI 預設為全螢幕交換鏈的桌面解析度。 建立全螢幕交換鏈時，必須將 [**dxgi \_ 交換 \_ 鏈 \_ DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)結構的 **旗標** 成員設為 [**dxgi \_ 交換 \_ 鏈 \_ 旗標 \_ 允許 \_ 模式 \_ 切換**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)，以覆寫 DXGI 的預設行為。 此旗標也可以傳遞至 **ResizeTarget** ，以動態方式啟用或停用此功能。

## <a name="multiple-monitors"></a>多個監視器

搭配多個監視器使用 DXGI 時，有兩個要遵循的規則。

第一個規則適用于在多個監視器上建立兩個或多個全螢幕交換鏈。 建立這類交換鏈時，最好將所有交換鏈建立為視窗視窗，然後將它們設定為全螢幕。 如果交換鏈是在全螢幕模式中建立，則建立第二個交換鏈會導致模式變更傳送至第一個交換鏈，這可能會導致全螢幕模式終止。

第二個規則會套用到輸出。 關注建立交換鏈時使用的輸出。 使用 DXGI 時， [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) 物件可控制交換鏈在全螢幕時所使用的監視。 與 DXGI 不同的是，Direct3D 9 沒有輸出的概念。

## <a name="window-styles-and-dxgi"></a>視窗樣式和 DXGI

在全螢幕和視窗模式之間切換時，Direct3D 9 應用程式必須執行許多工作。 大部分的工作都牽涉到變更視窗樣式，以新增和移除框線、加入捲軸等等。 當應用程式移植至 DXGI 和 Direct3D 2.x 或 Direct3D 11. x 時，此程式碼通常會保留在原處。 視所做的變更而定，切換模式可能會導致非預期的行為。 例如，當切換至視窗模式時，應用程式可能不會再有視窗框架或視窗框線，儘管有專門設定這些樣式的程式碼。 發生這種情況是因為 DXGI 現在會處理其本身的大部分變更。 手動設定視窗樣式可能會干擾 DXGI，而這可能會造成非預期的行為。

建議的行為是盡可能少的工作，並讓 DXGI 處理與視窗的大部分互動。 但是，如果應用程式需要處理自己的視窗化行為，則可以使用 [**IDXGIFactory：： MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation) 來指示 DXGI 停用部分自動視窗處理。

## <a name="multithreading-and-dxgi"></a>多執行緒和 DXGI

在多執行緒應用程式中使用 DXGI以確保不會發生死結，要特別注意。 因為 DXGI 與視窗間的緊密互動，所以會偶爾將視窗訊息傳送至相關聯的應用程式視窗。 DXGI 需要進行視窗間的變更才能繼續，因此它會使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)，也就是同步呼叫。 應用程式必須在 **SendMessage** 傳回之前處理視窗訊息。

在具有 DXGI 呼叫的應用程式中，以及在相同執行緒 (或單一執行緒應用程式) 的應用程式中，幾乎需要完成一些工作。 當 DXGI 呼叫與訊息提取位於相同執行緒上時， [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 會呼叫視窗的 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))。 這會略過訊息泵，並允許在呼叫 **SendMessage** 之後繼續執行。 請記住， [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) 呼叫（例如 [**IDXGISwapChain：:P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)重新傳送）也會被視為 DXGI 呼叫;DXGI 可能會延遲 [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) 或 [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) 中的工作，直到呼叫 **存在** 為止。

如果 DXGI 呼叫和訊息提取位於不同的執行緒上，則必須小心，以避免發生鎖死。 當訊息泵和 SendMessage 位於不同的執行緒上時， [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 會將訊息新增至視窗的訊息佇列，並等候視窗處理該訊息。 如果視窗程式忙碌或不是由訊息抽取呼叫，訊息可能永遠不會被處理，而 DXGI 將會無限期等候。

例如，如果應用程式在某個執行緒上具有訊息提取，並在另一個執行緒上轉譯，則可能會想要變更模式。 訊息泵執行緒會告知轉譯執行緒變更模式，並等候直到模式變更完成為止。 不過，轉譯執行緒會呼叫 DXGI 函式，然後再呼叫 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)，以封鎖直到訊息提取處理訊息為止。 發生鎖死的原因是兩個執行緒現在已被封鎖，而且正在等候彼此。 若要避免這種情況，絕對不會封鎖訊息提取。 如果無法避免區塊，則所有的 DXGI 互動都應該在與訊息提取相同的執行緒上進行。

## <a name="gamma-and-dxgi"></a>Gamma 和 DXGI

雖然在 Direct3D 10. x 或 Direct3D 11. x 中最好使用 SRGB 紋理來處理 gamma，否則，如果開發人員想要使用不同的 gamma 值而不是2.2，或使用不支援 SRGB 的轉譯目標格式，則 gamma 會變得很有用。 當您透過 DXGI 設定 gamma 曲線時，請注意兩個問題。 第一個問題是，傳遞至 [**IDXGIOutput：： SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) 的遞增值是 float 值，而不是 **文字** 值。 此外，請確定從 Direct3D 9 移植的程式碼在將這些值傳遞至 **SetGammaControl** 之前，不會嘗試轉換成 **文字** 值。

第二個問題是，在變更為全螢幕模式之後， [**SetGammaControl**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol) 可能不會運作，相依于所使用的 [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput) 物件。 當變更為全螢幕模式時，DXGI 會建立新的輸出物件，並針對輸出上的所有後續作業使用物件。 如果在全螢幕模式切換之前所列舉的輸出上呼叫 **SetGammaControl** ，則不會將呼叫導向至 DXGI 目前使用的輸出。 若要避免這個問題，請呼叫 [**IDXGISwapChain：： GetContainingOutput**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput) 來取得目前的輸出，然後呼叫此輸出的 **SetGammaControl** 來取得正確的行為。

如需使用 gamma 更正的詳細資訊，請參閱 [使用 gamma 修正](/windows/desktop/direct3ddxgi/using-gamma-correction)。

## <a name="dxgi-11"></a>DXGI 1。1

Windows 7 中包含的 Direct3D 11 執行時間，並安裝到 Windows Vista (請參閱[KB971644](https://support.microsoft.com/kb/971644)) 包含1.1 版的 DXGI。 這項更新會新增許多新格式的定義 (特別是 BGRA、10位 X2 偏差和 Direct3D 11 的 BC6H 和 BC7 材質壓縮) ，以及新版本的 DXGI factory 和介面卡介面 ([**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1)、 [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1)、 [**IDXGIAdapter1**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter1)) 以列舉遠端桌面連線。

使用 Direct3D 11 時，執行時間預設會在使用 Null [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter)指標呼叫 [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice)或 [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain)時，使用 DXGI 1.1。 不支援在相同的進程中混合使用 DXGI 1.0 和 DXGI 1.1。 也不支援在相同的進程中混合來自不同 factory 的 DXGI 物件實例。 因此，當您使用 DirectX 11 時，任何明確使用的 DXGI 介面都會使用「DXGI.DLL」中 [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1)進入點所建立的 [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) ，以確保應用程式一律使用 DXGI 1.1。

## <a name="dxgi-12"></a>DXGI 1。2

Windows 8 中包含的 Direct3D 11.1 執行時間也包含了 DXGI 的1.2 版。

DXGI 1.2 會啟用下列功能：

-   身歷聲轉譯
-   每圖元16個位元組格式

    -   \_ \_ \_ 現在完全支援 dxgi 格式 B5G6R5 UNORM 和 dxgi \_ 格式 \_ \_ 的 B5G5R5A1 UNORM
    -   已新增新的 DXGI \_ 格式 \_ B5G5R5A1 \_ UNORM 格式

-   影片格式
-   新的 DXGI 介面

如需有關 DXGI 1.2 功能的詳細資訊，請參閱 [dxgi 1.2 增強](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)功能。

 

 