---
title: Direct3D 9Ex 改善
description: 本主題說明 Windows 7 新增的翻轉模式支援，以及其在 Direct3D 9Ex 和桌面視窗管理員中相關聯的現有統計資料。
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376229"
---
# <a name="direct3d-9ex-improvements"></a>Direct3D 9Ex 改善

本主題說明 Windows 7 新增的翻轉模式支援，以及其在 Direct3D 9Ex 和桌面視窗管理員中相關聯的現有統計資料。 目標應用程式包括以影片或畫面播放速率為基礎的展示應用程式。 使用 Direct3D 9Ex Flip 模式的應用程式，可以在啟用 DWM 時減少系統資源載入。 呈現與翻轉模式相關聯的統計資料增強功能，可讓 Direct3D 9Ex 應用程式藉由提供即時意見反應和修正機制，更有效地控制簡報的速率。 內含範例資源的詳細說明和指標。

本主題包含下列各節。

-   [適用于 Windows 7 的 Direct3D 9Ex 改進功能](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [Direct3D 9EX 翻轉模式簡報](#direct3d-9ex-flip-mode-presentation)
-   [程式設計模型和 Api](#programming-model-and-apis)
    -   [如何加入 Direct3D 9Ex Flip 模型](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [Direct3D 9Ex Flip 模型應用程式的設計指導方針](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [Direct3D 9Ex Flip 模型應用程式的框架同步處理](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [當 DWM 關閉時，視窗化應用程式的框架同步處理](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [Direct3D 9Ex Flip 模型的逐步解說和目前的統計資料範例](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [框架同步處理的程式設計建議摘要](#summary-of-programming-recommendations-for-frame-synchronization)
-   [Direct3D 9Ex 改進的結論](#conclusion-about-direct3d-9ex-improvements)
-   [呼叫動作](#call-to-action)
-   [相關主題](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a>適用于 Windows 7 的 Direct3D 9Ex 改進功能

Direct3D 9Ex 的翻轉模式展示是在 Direct3D 9Ex 中呈現影像的改良模式，可有效率地將轉譯的影像交給 Windows 7 桌面視窗管理員 (DWM) 以進行撰寫。 從 Windows Vista 開始，DWM 撰寫了整個桌面。 啟用 DWM 時，視窗模式應用程式會使用名為 Blt 模式的方法，將其內容顯示在桌面上， (或 Blt 模型) 。 使用 Blt 模型時，DWM 會針對桌面組合維護一份 Direct3D 9Ex 呈現的表面。 當應用程式更新時，新的內容會透過 blt 複製到 DWM 介面。 針對包含 Direct3D 和 GDI 內容的應用程式，GDI 資料也會複製到 DWM 介面上。

在 Windows 7 中提供、DWM 的翻轉模式 (或翻轉模型) 是一種新的表示方法，基本上可讓您在視窗模式應用程式和 DWM 之間傳遞應用程式介面的控制碼。 除了儲存資源，Flip 模型還支援增強的目前統計資料。

目前的統計資料是應用程式可用來同步處理影片和音訊串流以及從影片播放問題中復原的畫面格時間資訊。 [目前的統計資料] 中的畫面格時間資訊可讓應用程式調整其影片畫面的呈現率，以提供更流暢的簡報。 在 Windows Vista 中，如果 DWM 針對桌面電腦群組合維護了一個對應的框架介面複本，則應用程式可以使用 DWM 提供的統計資料。 在 Windows 7 中，針對現有的應用程式，這種取得目前統計資料的方法仍會提供。

在 Windows 7 中，採用 Flip 模型的 Direct3D 9Ex 型應用程式應該使用 D3D9Ex Api 來取得目前的統計資料。 啟用 DWM 時，視窗模式和全螢幕獨佔模式 Direct3D 9Ex 應用程式在使用翻轉模型時，可能會預期出現相同的統計資料資訊。 Direct3D 9Ex Flip 模型目前的統計資料可讓應用程式即時查詢目前的統計資料，而不是在畫面上顯示畫面格之後：相同的現有統計資料資訊可供視窗模式 Flip-Model 啟用的應用程式作為全螢幕應用程式;D3D9Ex Api 中新增的旗標，可讓 Flip 模型應用程式有效地在呈現時捨棄延遲的畫面格。

以 Windows 7 為目標的新影片或以畫面播放速率為基礎的簡報應用程式應該使用 Direct3D 9Ex Flip 模型。 由於 DWM 與 Direct3D 9Ex 執行時間之間的同步處理，使用翻轉模型的應用程式應指定2到 4 backbuffers，以確保呈現順暢。 使用目前統計資料資訊的應用程式，將可受益于使用已啟用 Flip 模型的現有統計資料增強功能。

## <a name="direct3d-9ex-flip-mode-presentation"></a>Direct3D 9EX 翻轉模式簡報

當 DWM 開啟時，以及當應用程式處於視窗模式時（而非全螢幕獨佔模式），系統上的 Direct3D 9Ex 翻轉模式效能改進相當重要。 下表和圖例顯示記憶體頻寬使用量的簡化比較，以及選擇翻轉模型與預設使用量 Blt 模型的視窗化應用程式的系統讀取和寫入。



| Blt 模式存在於 DWM                                                                                                 | D3D9Ex 反轉模式存在於 DWM                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 1. 應用程式會更新其框架 (寫) <br/>                                                                 | 1. 應用程式會更新其框架 (寫) <br/>                     |
| 2. Direct3D runtime 會將介面內容複寫到 DWM 重新導向介面 (讀取、寫入) <br/>                       | 2. Direct3D runtime 將應用程式介面傳遞至 DWM<br/>        |
| 3. 在共用表面複製完成之後，DWM 會將應用程式介面轉譯至螢幕 (讀取、寫入) <br/> | 3. DWM 將應用程式介面轉譯至螢幕 (讀取、寫入) <br/> |



 

![比較 blt 模型和翻轉模型的圖例](images/blt-flip-mode-present.png)

Flip 模式存在：減少由 DWM 針對視窗化框架組合所撰寫的讀取和寫入次數，以減少系統記憶體使用量。 這樣可減少系統電源耗用量和整體的記憶體使用量。

無論應用程式是在視窗模式或全螢幕獨佔模式中，應用程式都可以利用 Direct3D 9Ex 翻轉模式，在 DWM 開啟時顯示統計資料的增強功能。

## <a name="programming-model-and-apis"></a>程式設計模型和 Api

新的影片或畫面播放速率：在 Windows 7 上使用 Direct3D 9Ex Api 的測量應用程式，可以利用在 Windows 7 上執行時，由翻轉模式所提供的記憶體和省電以及改良的簡報。  (在舊版 Windows 上執行時，Direct3D 執行時間會將應用程式預設為目前的 Blt 模式。 ) 

目前的翻轉模式會要求應用程式在 DWM 開啟時，可以利用即時目前的統計資料意見反應和修正機制。 不過，使用「翻轉」模式的應用程式在使用並行 GDI API 轉譯時，應該要知道有何限制。

您可以修改現有的應用程式，以利用新開發應用程式的相同優點和警告，來利用翻轉模式。

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a>如何加入 Direct3D 9Ex Flip 模型

以 Windows 7 為目標的 Direct3D 9Ex 應用程式可以藉由建立具有 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) 列舉值的交換鏈，加入宣告 Flip 模型。 為了加入宣告 Flip 模型，應用程式會指定 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters) 結構，然後在呼叫 [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) API 時，傳遞此結構的指標。 本節說明以 Windows 7 為目標的應用程式如何使用 **IDirect3D9Ex：： CreateDeviceEx** 加入宣告 Flip 模型。 如需有關 **IDirect3D9Ex：： CreateDeviceEx** API 的詳細資訊，請參閱 **MSDN 上的 IDirect3D9Ex：： CreateDeviceEx**。

為了方便起見，這裡會重複 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters) 和 [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) 的語法。

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

當您修改 Windows 7 的 Direct3D 9Ex 應用程式以加入宣告 Flip 模型時，您應該考慮下列有關 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters)之指定成員的專案：

<dl> <dt>

**BackBufferCount**
</dt> <dd>

僅 (Windows 7) 

當 **SwapEffect** 設定為新的 D3DSWAPEFFECT \_ FLIPEX 交換鏈效果類型時，背景緩衝區計數應等於或大於2，以防止應用程式效能受到 DWM 等候上一個現有緩衝區釋放的結果影響。

當應用程式也使用與 D3DSWAPEFFECT FLIPEX 相關聯的現有統計資料時 \_ ，我們建議您將背景緩衝區計數設定為2到4。

\_在 Windows Vista 或舊版作業系統上使用 D3DSWAPEFFECT FLIPEX 將會從 [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)傳回失敗。

</dd> <dt>

**SwapEffect**
</dt> <dd>

僅 (Windows 7) 

\_當應用程式採用具有 DWM 的翻轉模式時，新的 D3DSWAPEFFECT FLIPEX 交換鏈效果類型會指定。 它可讓應用程式更有效率地使用記憶體和電源，也可讓應用程式在視窗模式下利用全螢幕的顯示統計資料。 全螢幕應用程式行為不會受到影響。 如果視窗化設定為 **TRUE** ，且 **SWAPEFFECT** 設定為 D3DSWAPEFFECT \_ FLIPEX，則執行時間會建立一個額外的背景緩衝區，並將任何控制碼都旋轉為在呈現時成為前端緩衝區的緩衝區。

</dd> <dt>

**旗標**
</dt> <dd>

僅 (Windows 7) 

如果 **SwapEffect** 設定為新的 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect)交換鏈效果類型，則無法設定 [D3DPRESENTFLAG 可 \_ 鎖定 \_ 背景緩衝區](/windows/desktop/direct3d9/d3dpresentflag)旗標。

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a>Direct3D 9Ex Flip 模型應用程式的設計指導方針

使用下列各節中的指導方針來設計您的 Direct3D 9Ex Flip 模型應用程式。

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a>在 Blt 模式的不同 HWND 中使用翻轉模式存在

應用程式應該使用存在於其他 Api 未設為目標之 HWND 中的 Direct3D 9Ex Flip 模式，包括 Blt 模式目前的 Direct3D 9Ex、其他版本的 Direct3D 或 GDI。 目前可以使用翻轉模式呈現給子視窗;也就是說，當應用程式不會在相同 HWND 中與 Blt 模型混合使用時，可以使用翻轉模型，如下圖所示。

![direct3d 父視窗和 gdi 子視窗的圖例，每個視窗都有自己的 hwnd](images/parent-d3d.png)

![gdi 父視窗和 direct3d 子視窗的圖例，每個視窗都有自己的 hwnd](images/parent-gdi.png)

因為 Blt 模型會維護一個額外的介面複本，所以可以透過 Direct3D 和 GDI 的分次更新，將 GDI 和其他 Direct3D 內容新增至相同的 HWND。 使用翻轉模型，只會顯示已傳遞至 DWM 之 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) 交換鏈中的 Direct3D 9Ex 內容。 將會忽略所有其他 Blt 模型 Direct3D 或 GDI 內容更新，如下列圖例所示。

![當使用 flip 模型，且 direct3d 和 gdi 內容在相同 hwnd 中時，可能不會顯示的 gdi 文字圖例](images/d3d-gdi-same-hwnd.png)

![在啟用 dwm 且應用程式處於視窗模式時的 direct3d 和 gdi 內容圖例](images/d3d-gdinotext-same-hwnd.png)

因此，您應該針對交換鏈緩衝區介面啟用翻轉模型，其中 Direct3D 9Ex Flip 模型會單獨轉譯成整個 HWND。

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a>請勿搭配 GDI 的 ScrollWindow 或 ScrollWindowEx 使用翻轉模型

某些 Direct3D 9Ex 應用程式會在觸發使用者滾動事件時，使用 GDI 的 ScrollWindow 或 ScrollWindowEx 函數來更新視窗內容。 ScrollWindow 和 ScrollWindowEx 會在滾動視窗時，在螢幕上執行視窗內容的 blts。 這些函式也需要 GDI 和 Direct3D 9Ex 內容的 Blt 模型更新。 使用其中一種函式的應用程式不一定會在應用程式處於視窗模式且已啟用 DWM 的情況下，于畫面上顯示可見的視窗內容滾動。 建議您不要在應用程式中使用 GDI 的 ScrollWindow 和 ScrollWindowEx Api，而是改為在螢幕上重新繪製其內容以回應滾動。

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a>\_每個 HWND 使用一個 D3DSWAPEFFECT FLIPEX 交換鏈

使用翻轉模型的應用程式不應使用以相同 HWND 為目標的多個翻轉模型交換鏈。

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a>Direct3D 9Ex Flip 模型應用程式的框架同步處理

目前的統計資料是媒體應用程式用來同步處理影片和音訊串流以及從影片播放問題中復原的畫面格時間資訊。 若要啟用目前的統計資料可用性，Direct3D 9Ex 應用程式必須確定應用程式傳遞給 [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的 *BehaviorFlags* 參數包含裝置行為旗標 [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate)。

為了方便起見， [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) 的語法會在此重複。

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

Direct3D 9Ex Flip 模型會加入 [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) 簡報旗標，以強制執行 [D3DPRESENT \_ 間隔 \_ 立即](/windows/desktop/direct3d9/d3dpresent) 呈現旗標行為。 Direct3D 9Ex 應用程式會在應用程式傳遞給 IDirect3DDevice9Ex 的 *dwFlags* 參數中指定這些呈現旗標 [**：:P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)，如下所示。

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

當您針對 Windows 7 修改 Direct3D 9Ex 應用程式時，您應該考慮下列有關指定 [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) 簡報旗標的資訊：

<dl> <dt>

[D3DPRESENT \_ DONOTFLIP](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

此旗標僅適用于全螢幕模式或

僅 (Windows 7) 

當應用程式在 [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的呼叫中，將 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters)的 **SwapEffect** 成員設定為 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) 。

</dd> <dt>

[D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

僅 (Windows 7) 

只有當應用程式在 [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的呼叫中將 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters)的 **SwapEffect** 成員設定為 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect)時，才能指定此旗標。 應用程式可以使用此旗標，立即在 DWM 目前的佇列中更新具有數個框架的介面，基本上會略過中繼框架。

啟用視窗 FlipEx 功能的應用程式可以使用此旗標，立即更新具有在 DWM 目前佇列中的框架，並略過中繼框架的介面。 如果媒體應用程式想要捨棄已偵測為最晚的畫面格，並在組合時顯示後續的畫面格，這特別有用。 [**IDirect3DDevice9Ex：**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 如果未正確指定此旗標，:P resentex 會傳回不正確參數錯誤。

</dd> </dl>

為了取得目前的統計資料資訊，應用程式會呼叫 [**IDirect3DSwapChain9Ex：： GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) API 來取得 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats)結構。

[**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats)結構包含 [**IDirect3DDevice9Ex：:P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)呼叫的相關統計資料。 您必須使用 [**IDirect3D9Ex：： CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) 呼叫搭配 [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) 旗標來建立裝置。 否則， [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 傳回的資料是未定義的。 啟用翻轉模型的 Direct3D 9Ex 交換鏈，可提供視窗內和全螢幕模式的統計資訊資訊。

針對啟用 Blt 模型的 Direct3D 9Ex 在視窗模式中交換鏈，所有 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) 結構值都是零。

針對 FlipEx 目前的統計資料， [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 會 \_ \_ \_ 在下列情況下傳回 D3DERR 目前的統計資料：

-   第一次呼叫 [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ，表示序列的開頭
-   從 on 到 off 的 DWM 轉換
-   模式變更：以視窗模式切換至全螢幕或全螢幕到全螢幕轉換

為了方便起見，這裡會重複 [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 的語法。

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

[**IDirect3DSwapChain9Ex：： GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)方法會傳回最後一個 PresentCount，也就是與交換鏈相關聯之顯示裝置所建立的最後一個成功呼叫的目前識別碼。 此存在識別碼是 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats)結構之 **PresentCount** 成員的值。 針對啟用 Blt 模型的 Direct3D 9Ex 交換鏈，在視窗模式中，所有 **D3DPRESENTSTATS** 結構值都是零。

為了方便起見， [**IDirect3DSwapChain9Ex：： GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) 的語法會在此重複。

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

當您針對 Windows 7 修改 Direct3D 9Ex 應用程式時，您應該考慮下列有關 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) 結構的資訊：

-   [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)傳回的 PresentCount 值不會在 [](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) \_ *DONOTWAIT* 參數中指定 D3DPRESENT dwFlags 的 PresentEx 呼叫傳回失敗時進行更新。
-   使用 D3DPRESENT DONOTFLIP 呼叫 [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 時 \_ ， [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 呼叫會成功，但當應用程式處於視窗模式時，則不會傳回更新的 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) 結構。
-   [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats)中的 **PresentRefreshCount** 與 **SyncRefreshCount** ：
    -   當應用程式在每個 vsync 上呈現時， **PresentRefreshCount** 等於 **SyncRefreshCount** 。
    -   當提交目前的時間時，會在 vsync 間隔取得 **SyncRefreshCount** ， **SyncQPCTime** 大約是與 vsync 間隔相關聯的時間。

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a>當 DWM 關閉時，視窗化應用程式的框架同步處理

當 DWM 為 off 時，視窗型應用程式會直接顯示到監視器畫面，而不會通過翻轉鏈。 在 Windows Vista 中，當 DWM 為 off 時，不支援取得視窗型應用程式的畫面格統計資訊。 為了維護應用程式不需要 DWM 感知的 API，當 DWM 為 off 時，Windows 7 會傳回視窗型應用程式的框架統計資訊。 當 DWM 為 off 時所傳回的框架統計資料只是估計。

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a>Direct3D 9Ex Flip 模型的 Walk-Through 和目前的統計資料範例

**加入宣告 FlipEx presentation for Direct3D 9Ex 範例**

1.  確定範例應用程式是在 Windows 7 或更新版本的作業系統版本上執行。
2.  在 [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的呼叫中，將 [**D3DPRESENT \_ 參數**](/windows/desktop/direct3d9/d3dpresent-parameters)的 **SwapEffect** 成員設定為 [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) 。


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



**若要同時加入宣告與 Direct3D 9Ex 範例相關聯的現有統計資料 FlipEx**

-   Set [D3DCREATE \_ ENABLE \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) in [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex)的 *BehaviorFlags* 參數。


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



**若要避免，請偵測並從問題中復原**

1.  佇列目前的呼叫：建議的背景緩衝區計數是從2到4。
2.  Direct3D 9Ex 範例會新增隱含背景緩衝區，實際的目前佇列長度為背景緩衝區計數 + 1。
3.  建立協助程式目前的佇列結構，以將所有成功提交的現有識別碼儲存 (PresentCount) 以及相關聯、已計算/預期的 PresentRefreshCount。
4.  若要偵測出問題發生：

    -   呼叫 [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85))。
    -   取得 (PresentCount) 的目前識別碼，以及顯示所顯示之統計資料的 vsync 計數 (PresentRefreshCount) 的框架。
    -   在與目前識別碼相關聯的範例程式碼) 中，取出預期的 PresentRefreshCount (TargetRefresh。
    -   如果實際的 PresentRefreshCount 晚于預期，就會發生問題。

5.  若要從問題中復原：

    -   計算 \_ 範例程式碼) 中 (g iImmediates 變數略過的框架數目。
    -   以 interval D3DPRESENT FORCEIMMEDIATE 呈現略過的框架 \_ 。

**故障偵測和復原的考慮**

1.  損毀修復會在範例程式碼中使用 N (g \_ iQueueDelay 變數) 出現的呼叫數，其中 N (g \_ iQueueDelay) 等於 g \_ IImmediates 加上目前佇列的長度，也就是：

    -   略過具有出現間隔的框架 D3DPRESENT \_ FORCEIMMEDIATE，加上
    -   需要處理的佇列呈現

2.  在範例) 中，將限制設定為問題的 (故障 \_ 修復 \_ 限制。 如果範例應用程式無法從太長 (（例如，1秒）或在60Hz 監視器) 上的 60 vsyncs 復原，請跳過間歇性的動畫，並重設目前的協助程式佇列。


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



**範例案例**

-   下圖顯示背景緩衝區計數為4的應用程式。 實際的出現佇列長度為5。

    ![applicas 轉譯的畫面格和呈現佇列的圖例](images/sample-scenario.png)

    畫面格 A 的目標是在同步間隔計數為1時進入螢幕上的畫面，但偵測到它顯示于同步間隔計數4。 因此發生問題。 後續3個畫面格會以 D3DPRESENT \_ INTERVAL \_ FORCEIMMEDIATE 呈現。 在復原之前，問題應該總共有8個出現的呼叫-下一個畫面會根據其目標同步間隔計數來顯示。

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a>框架同步處理的程式設計建議摘要

-   建立所有 LastPresentCount 識別碼的備份清單， (透過) [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) 取得的所有識別碼，以及所有提交的相關預估 PresentRefreshCount。
    > [!Note]  
    > 當應用程式使用 D3DPRESENT DONOTFLIP 呼叫 [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 時 \_ ， [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 呼叫會成功，但當應用程式處於視窗模式時，則不會傳回更新的 [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) 結構。

     

-   呼叫 [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) 來取得與所顯示的每個畫面格目前識別碼相關聯的實際 PresentRefreshCount，以確保應用程式處理失敗時，會從呼叫傳回。
-   如果實際 PresentRefreshCount 晚于預估 PresentRefreshCount，則會偵測到問題。 藉由提交延遲的畫面格來彌補 D3DPRESENT \_ FORCEIMMEDIATE。
-   當目前的佇列中有一個畫面格出現時，所有後續排入佇列的框架都會延遲出現。 D3DPRESENT \_ FORCEIMMEDIATE 將只會更正下一個要在所有已排入佇列的框架之後呈現的畫面格。 因此，目前的佇列或背景緩衝區計數不應該太長，因此不太能趕上畫面格的問題。 最佳背景緩衝區計數是2到4。
-   如果估計的 PresentRefreshCount 晚于實際的 PresentRefreshCount，則可能發生 DWM 節流。 可能的解決方案如下：

    -   減少目前的佇列長度
    -   使用任何其他方法減少 GPU 記憶體需求，除了減少目前的佇列長度 (也就是降低品質、移除效果等等) 
    -   指定 [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) 以防止一般 DWM 節流

-   在下列案例中，確認應用程式顯示功能和框架統計資料效能：

    -   on 和 off 的 DWM
    -   全螢幕專屬和視窗模式
    -   較低的功能硬體

-   當應用程式無法從有 D3DPRESENT FORCEIMMEDIATE 的大量 glitched 框架復原時 \_ ，可能會執行下列作業：

    -   以較少的工作負載呈現，以降低 CPU 和 GPU 使用量。
    -   在影片解碼的情況下，藉由降低品質以及 CPU 和 GPU 使用量來加快解碼的速度。

## <a name="conclusion-about-direct3d-9ex-improvements"></a>Direct3D 9Ex 改進的結論

在 Windows 7 上，在簡報期間顯示影片或量測計畫面播放速率的應用程式，可以選擇切換至 Flip 模型。 與 Flip 模型 Direct3D 9Ex 相關聯的目前統計資料改善，可讓應用程式受益于每個畫面播放速率的簡報，並提供即時意見反應來偵測和修復問題。 採用 Direct3D 9Ex Flip 模型的開發人員應該以不同的 HWND 作為目標，將 GDI 內容和畫面播放速率同步處理的目標設為帳戶。 請參閱本主題中的詳細資料和 MSDN 檔。 如需其他檔，請參閱 [MSDN 上的 DirectX 開發人員中心](/previous-versions/windows/apps/hh452744(v=win.10))。

## <a name="call-to-action"></a>動作的呼叫

當您建立嘗試同步處理展示畫面播放速率或從顯示問題中復原的應用程式時，建議您在 Windows 7 上使用 Direct3D 9Ex 翻轉模型及其目前的統計資料。

## <a name="related-topics"></a>相關主題

[MSDN 上的 DirectX 開發人員中心](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> </dl>