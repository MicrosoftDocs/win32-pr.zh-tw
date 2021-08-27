---
title: Windows 上的高 DPI 桌面應用程式開發
description: 此內容的目標物件是想要更新桌面應用程式以處理動態顯示器縮放比例 (的開發人員也稱為
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01958791dccd7c836babedbe726233797eddb646
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471324"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Windows 上的高 DPI 桌面應用程式開發

此內容的目標物件是想要更新傳統型應用程式的開發人員，以處理顯示比例因素 (每英寸的點或 DPI) 變更，讓其應用程式在轉譯的任何顯示器上都有清晰的外觀。

首先，如果您要從頭開始建立新的 Windows 應用程式，強烈建議您建立[通用 Windows 平臺 (UWP) ](/windows/uwp/get-started/whats-a-uwp)應用程式。 UWP 應用程式會自動 &mdash; 動態 &mdash; 調整其執行所在的每個顯示器。

使用舊版 Windows 程式設計技術的桌面應用程式 (原始 Win32 程式設計、Windows Forms、Windows Presentation Framework (WPF) 等）。 ) 無法自動處理 DPI 調整，而不需要額外的開發人員工作。 如果沒有這樣的工作，應用程式會在許多常見的使用案例中呈現模糊或大小不正確。 本檔提供有關更新桌面應用程式以正確轉譯的相關內容和資訊。

## <a name="display-scale-factor--dpi"></a>顯示縮放比例 & DPI

隨著顯示器技術的進展，顯示器面板製造商已將遞增的圖元數封裝到其面板上的每個實體空間單位中。 這會導致新式顯示器面板的每英寸 (DPI) 比以往更高。 在過去，大部分顯示器的實體空間每個線性英寸都有96圖元 (96 DPI) ;在2017中，可以立即取得幾乎 300 DPI 或更高版本的顯示器。

大部分舊版桌面 UI 架構都有內建的假設，在進程存留期間，顯示 DPI 不會變更。  此假設不再成立，因為在應用程式進程的存留期內，顯示 Dpi 經常變更數次。 顯示比例因數/DPI 變更的一些常見案例如下：

-   多重監視器的安裝，其中每個顯示器都有不同的縮放比例，而應用程式會從一個顯示器移至另一個 (例如4K 和1080p 顯示器) 
-   使用低 DPI 的外部顯示器來停駐和移除高 DPI 的膝上型電腦 (或反之亦然) 
-   從高 DPI 膝上型電腦/平板電腦透過遠端桌面連線至低 DPI 裝置 (或反之亦然) 
-   在應用程式執行時變更顯示比例因數設定

在這些情況下，UWP 應用程式會自動為新的 DPI 重繪其本身。 在預設情況下，如果沒有其他開發人員工作，桌面應用程式就不會執行。 未執行此額外工作來回應 DPI 變更的桌面應用程式，可能會對使用者顯示模糊或大小不正確。

## <a name="dpi-awareness-mode"></a>DPI 感知模式

桌面應用程式必須告訴 Windows 是否支援 DPI 縮放比例。 根據預設，系統會將桌面應用程式的 DPI 感知和點陣圖延伸到其視窗。 藉由設定下列其中一種可用的 DPI 感知模式，應用程式可以明確地分辨 Windows 其要如何處理 DPI 調整：

### <a name="dpi-unaware"></a>不知道 DPI

DPI 感知應用程式會以固定的 DPI 值 96 (100% ) 轉譯。 當這些應用程式在顯示比例大於 96 DPI 的螢幕上執行時，Windows 會將應用程式點陣圖延展到預期的實體大小。 這會導致應用程式出現模糊。

### <a name="system-dpi-awareness"></a>系統 DPI 感知

以系統 DPI 感知的桌面應用程式，通常會在使用者登入的時間內，收到主要連線監視器的 DPI。 在初始化期間，它們會適當地配置 UI， (調整大小控制項、選擇字型大小、載入資產等 ) 使用該系統的 DPI 值。 如此一來，系統 DPI 感知的應用程式不會縮放 (點陣圖，Windows 在以該單一 DPI 呈現的顯示器轉譯) 。 當應用程式移至具有不同縮放比例的顯示器時，或如果顯示比例因數變更時，Windows 會以點陣圖調整應用程式的視窗，使其看起來模糊不清。 實際上，系統 DPI 感知的桌面應用程式只會在單一顯示器縮放比例轉譯 crisply，每次 DPI 變更時變得模糊。

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Per-Monitor 和 Per-Monitor (V2) DPI 感知

建議您更新傳統型應用程式，以使用個別監視器 DPI 感知模式，讓它們可以在每次 DPI 變更時立即正確轉譯。 當應用程式向 Windows 報告想要在此模式中執行時，Windows 不會在 DPI 變更時以點陣圖延展應用程式，而是將[WM \_ DPICHANGED](wm-dpichanged.md)傳送至應用程式視窗。 然後，應用程式必須負責處理新 DPI 的大小調整。 大部分的桌面應用程式所使用的 UI 架構 (Windows 的通用控制項 (comctl32.dll) 、Windows Forms、Windows Presentation Framework 等等。 ) 不支援自動 DPI 縮放，因此需要開發人員調整大小並重新調整其視窗的內容。

有兩個版本的 Per-Monitor 認知，應用程式可以將自己註冊為：第1版和第2版 (PMv2) 。 註冊在 PMv2 感知模式中執行的進程會導致：

1.  當 DPI 變更 (最上層和子系 Hwnd 時，所要通知的應用程式) 
2.  應用程式查看每個顯示的原始圖元
3.  應用程式永遠不會依 Windows 縮放點陣圖
4.  自動的非工作區 (視窗標題、捲軸等 ) DPI 縮放比例 Windows
5.  Win32 對話方塊 (從[CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) 自動以 Windows 調整的 DPI
6.  主題-在通用控制項中繪製點陣圖資產 (核取方塊、按鈕背景等 ) 會自動以適當的 DPI 縮放比例呈現

在 Per-Monitor v2 感知模式中執行時，會在應用程式的 DPI 變更時通知應用程式。 如果應用程式不會為新的 DPI 調整本身的大小，則應用程式 UI 會出現太小或太大的 (，視先前和新的 DPI 值) 的差異而定。

> [!Note]  
> Per-Monitor V1 (PMv1) 感知的功能非常有限。 建議應用程式使用 PMv2。

下表顯示應用程式如何在不同的情況下呈現：


| DPI 感知模式 | Windows引進的版本 | 應用程式的 DPI 視圖 | DPI 變更的行為 | 
|--------------------|----------------------------|---------------------------|------------------------|
| 知道 | N/A | 所有顯示器都是 96 DPI | 點陣圖延展 (模糊)  | 
| 系統 | Vista | 所有顯示器都有相同的 DPI (在目前的使用者會話開始時主顯示器的 DPI)  | 點陣圖延展 (模糊)  | 
| Per-Monitor | 8.1 | 應用程式視窗主要所在的顯示器 DPI | <ul><li>最上層 HWND 會收到 DPI 變更的通知</li><li>沒有任何 UI 元素的 DPI 縮放比例。</li></ul><br /> | 
| Per-Monitor V2 | Windows 10 Creators Update (1703)  | 應用程式視窗主要所在的顯示器 DPI | <ul><li>最上層 <span class="underline">和</span> 子系 hwnd 會收到 DPI 變更的通知</li></ul><br /><span class="underline">自動調整 DPI 規模：</span><ul><li>非工作區</li><li>主題- (comctl32.dll V6) 的通用控制項中繪製的點陣圖</li><li>對話方塊 (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>) </li></ul><br /> | 


### <a name="per-monitor-v1-dpi-awareness"></a>每台監視器 (V1) DPI 感知

Per-Monitor V1 DPI 感知模式 (PMv1) 是 Windows 8.1 引進的。 此 DPI 感知模式相當有限，僅提供下列功能。 建議桌面應用程式使用 Windows 10 1703 或更新版本上支援的 Per-Monitor v2 感知模式。

針對個別監視器感知的初始支援僅提供下列應用程式：

1.  最上層的 Hwnd 會收到 DPI 變更的通知，並提供新的建議大小
2.  Windows 不會以點陣圖延展應用程式 UI
3.  應用程式會看到所有顯示的實體圖元 (請參閱虛擬化) 

在 Windows 10 1607 或更新版本中，PMv1 應用程式也可能會在 WM NCCREATE 期間呼叫[EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) ， \_ 要求 Windows 正確地調整視窗的非工作區。

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>UI 架構/技術的每個監視器 DPI 調整支援

下表顯示從 Windows 10 1703 的各種 Windows UI 架構所提供的每個監視器 DPI 感知支援層級：


| 架構/技術 | 支援 | 作業系統版本 | 處理的 DPI 縮放比例 | 深入閱讀 | 
|------------------------|---------|------------|------------------------|-----------------|
| 通用 Windows 平台 (UWP) | 完整 | 1607 | UI 架構 | <a href="/windows/uwp/get-started/whats-a-uwp">通用 Windows 平台 (UWP)</a> | 
| 原始 Win32/通用控制項 V6 (comctl32.dll)  | <ul><li>傳送至所有 Hwnd 的 DPI 變更通知訊息</li><li>主題-繪製的資產會在通用控制項中正確呈現</li><li>自動調整對話方塊的 DPI</li></ul> | 1703 | 應用程式 | <a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub樣品</a> | 
| Windows Forms | 某些控制項的每個監視器的自動 DPI 縮放比例有限 | 1703 | UI 架構 | <a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Windows Forms 中的高 DPI 支援</a> | 
| Windows Presentation Framework (WPF) | 原生 WPF 應用程式將會以 DPI 比例調整裝載于其他架構中的 WPF，而 WPF 中裝載的其他架構則不會自動調整 | 1607 | UI 架構 | <a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub樣品</a> | 
| GDI | 無 | N/A | 應用程式 | 查看 <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI 高 DPI 縮放比例</a> | 
| GDI+ | 無 | N/A | 應用程式 | 查看 <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI 高 DPI 縮放比例</a> | 
| MFC | 無 | N/A | 應用程式 | N/A | 




 

## <a name="updating-existing-applications"></a>更新現有的應用程式

若要更新現有的桌面應用程式，以適當地處理 DPI 調整，必須更新其 UI 的重要部分，以回應 DPI 變更。

大部分的桌面應用程式都是以系統 DPI 感知模式來執行。 系統 DPI 感知的應用程式通常會調整為主顯示器的 DPI， (系統匣在 Windows 會話啟動) 時的顯示器。 當 DPI 變更時，Windows 會以點陣圖延展這些應用程式的 UI，這通常會導致它們模糊。 當更新系統 DPI 感知應用程式，使其變成個別監視器 DPI 感知時，處理 UI 配置的程式碼需要更新，如此一來，它不僅會在應用程式初始化期間執行，還會在收到 Win32) 的情況下 ([WM \_ DPICHANGED](wm-dpichanged.md) 的 DPI 變更通知時執行。 這通常需要重新驗證程式代碼中的任何假設，UI 只需要調整一次。

此外，在 Win32 程式設計的情況下，許多 Win32 Api 都沒有任何 DPI 或顯示內容，因此它們只會傳回相對於系統 DPI 的值。 在您的程式碼中尋找某些 Api，並以 DPI 感知的變異數取代這些 Api，可能會很有用。 有些具有 DPI 感知變異的常見 Api 如下：



| 單一 DPI 版本   | Per-Monitor 版本        |
|----------------------|----------------------------|
| GetSystemMetrics     | GetSystemMetricsForDpi     |
| AdjustWindowRectEx   | AdjustWindowRectExForDpi   |
| SystemParametersInfo | SystemParametersInfoForDpi |
| GetDpiForMonitor     | GetDpiForWindow            |



 

在您的程式碼基底中搜尋採用固定 DPI 的硬式編碼大小也是個不錯的主意，以正確的 DPI 縮放比例的程式碼取代它們。 以下是包含所有這些建議的範例：

### <a name="example"></a>範例：

下列範例顯示簡化的 Win32 案例，以建立子系 HWND。 對 CreateWindow 的呼叫會假設應用程式是以 96 DPI 執行，而且在較高的 Dpi 中，按鈕的大小或位置都不正確：


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



下列更新的程式碼顯示：

1.  視窗建立程式碼 DPI 針對其父視窗的 DPI 調整子 HWND 的位置和大小
2.  藉由重新置放並調整子系 HWND 的大小來回應 DPI 變更
3.  以回應 DPI 變更的程式碼移除和取代的硬式編碼大小


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



更新系統 DPI 感知應用程式時，需要遵循的一些常見步驟如下：

1.  使用應用程式資訊清單 (或其他方法，將處理常式標示為個別監視器 DPI 感知 (V2) ，取決於) 使用) 的 UI 架構 (。
2.  讓 UI 版面配置邏輯可重複使用，並將其移出應用程式初始化程式碼，以便 \_ 在 Windows (Win32) 程式設計) 的情況下，于發生 DPI 變更 (WM DPICHANGED 時重複使用。
3.  將假設 DPI 機密資料 (DPI/字型/大小/等等的任何程式碼失效。 ) 永遠不需要更新。 在處理常式初始化時快取字型大小和 DPI 值是非常常見的作法。 更新應用程式以使其成為個別監視器 DPI 感知時，必須在每次遇到新的 DPI 時重新評估 DPI 敏感的資料。
4.  發生 DPI 變更時，請重載新 DPI 的 (或重新圖像) 任何點陣圖資產，或選擇性地將目前載入的資產延展到正確的大小。
5.  不 Per-Monitor DPI 感知的 Api 的 Grep，並將其取代為適用) Per-Monitor DPI 感知 Api (。 範例：將 GetSystemMetrics 取代為 GetSystemMetricsForDpi。
6.  在多重顯示/多 DPI 系統上測試您的應用程式。
7.  如果您的應用程式中有任何最上層視窗無法更新為適當的 DPI 縮放比例，請使用下列所述的混合模式 DPI 縮放 () ，以允許系統將這些最上層視窗的點陣圖延展。

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Mixed-Mode DPI 調整 (子進程的 DPI 縮放比例) 

更新應用程式以支援個別監視器 DPI 感知時，有時可能會使應用程式中的每個視窗不穩定或無法更新一次。 這可能只是因為更新和測試所有 UI 所需的時間和精力，或是因為您的應用程式可能會載入協力廠商 UI) ，而不是您需要執行的所有 UI 程式碼 (。 在這些情況下，Windows 提供一種方式，讓您能夠輕鬆進入每個監視器的認知，方法是讓您只在其原始的 DPI 感知模式中執行一些應用程式視窗 (最上層) ，同時將您的時間和精力集中在更新 UI 的重要部分。

以下是這種情況的圖例：您可以將主要的應用程式 UI 更新為圖例中的「主視窗」 () ，以使用個別監視器 DPI 感知來執行，同時在現有的模式中執行其他視窗 ( 「次要視窗」 ) 。

![認知模式之間的 DPI 縮放比例差異](images/hub-page-illustrations.png)

在 Windows 10 周年更新 (1607) 之前，進程的 DPI 感知模式是整個進程的屬性。 從 Windows 10 周年更新開始，您現在可以針對每個 **最上層** 視窗設定這個屬性。  (**子** 視窗必須繼續符合其父系的縮放大小。 ) 最上層視窗會定義為沒有父系的視窗。 這通常是具有最小化、最大化和關閉按鈕的「一般」視窗。 子進程 DPI 感知的目的是要讓次要 ui 隨 Windows (點陣圖調整) ，同時將您的時間和資源集中在更新主要 UI 上。

若要啟用子進程 DPI 感知，請在任何視窗建立呼叫之前和之後呼叫 [**SetThreadDpiAwarenessCoNtext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) 。 所建立的視窗會與您透過 SetThreadDpiAwarenessCoNtext 設定的 DPI 感知相關聯。 使用第二個呼叫來還原目前線程的 DPI 感知。

雖然使用子進程 DPI 調整可讓您依賴 Windows 來為您的應用程式進行某些 DPI 調整，但它可能會增加應用程式的複雜度。 請務必瞭解這種方法的缺點，以及它所引進之複雜性的本質。 如需子進程 DPI 感知的詳細資訊，請參閱 [混合模式 Dpi 縮放比例和 DPI 感知 api。](high-dpi-improvements-for-desktop-applications.md)

## <a name="testing-your-changes"></a>測試您的變更

在您更新應用程式以使其成為個別監視器 DPI 感知之後，請務必驗證應用程式是否正確地回應混合 DPI 環境中的 DPI 變更。 測試的一些細節包括：

1.  在不同 DPI 值的顯示之間來回移動應用程式視窗
2.  在顯示不同 DPI 值的情況上啟動應用程式
3.  當應用程式正在執行時，變更監視的縮放比例
4.  變更您用來作為主顯示器的顯示器、登出 _Windows_，然後在重新登入之後重新測試您的應用程式。 這在尋找使用硬式編碼大小/維度的程式碼時特別有用。

## <a name="common-pitfalls-win32"></a>Win32)  (常見的陷阱

**不使用在 WM DPICHANGED 中提供的建議矩形 \_**

當 Windows 傳送您的應用程式視窗至 [**WM \_ DPICHANGED**](wm-dpichanged.md)訊息時，此訊息會包含建議的矩形，您應該使用該矩形來調整視窗的大小。 您的應用程式必須使用這個矩形來調整本身的大小，因為這樣會：

1.  確定在顯示器之間拖曳時，滑鼠游標會在視窗上保持相同的相對位置
2.  防止應用程式視窗進入遞迴的 DPI 變更迴圈，其中一個 DPI 變更會觸發後續的 DPI 變更，而這會觸發另一個 DPI 變更。

如果您有應用程式特定的需求，而無法使用 Windows 在 WM DPICHANGED 訊息中提供的建議矩形 \_ ，請參閱 [**wm \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md)。 這則訊息可用來提供 Windows 在發生 DPI 變更時所要使用的所需大小，同時仍能避免上述問題。

**缺乏虛擬化的相關檔**

當 HWND 或進程以 DPI 感知或系統 DPI 感知的形式執行時，可以 Windows 來延展點陣圖。 發生這種情況時，Windows 會將某些 api 的 DPI 機密資訊調整並轉換成呼叫執行緒的座標空間。 例如，如果不知道 DPI 的執行緒在高 DPI 顯示器上執行時查詢螢幕大小，Windows 將會虛擬化指定給應用程式的答案，就像螢幕是 96 DPI 單位一樣。 或者，當目前使用者的會話開始時，當系統 DPI 感知執行緒與不同 DPI 上的顯示器互動時，Windows 會將某些 API 呼叫調整成以其原始的 DPI 縮放比例執行時，將會使用此 HWND 所使用的座標空間。

當您將傳統型應用程式更新為正確調整時，可能很難知道哪些 API 呼叫可以根據執行緒內容傳回虛擬化值;這項資訊目前不是由 Microsoft 所充分記載。 請注意，如果您從不感知 DPI 或系統 DPI 感知的執行緒內容呼叫任何系統 API，則傳回值可能會虛擬化。 因此，請確定您的執行緒是在與螢幕或個別視窗互動時所預期的 DPI 內容中執行。 使用 [SetThreadDpiAwarenessCoNtext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)暫時變更執行緒的 DPI 內容時，請務必在您完成時還原舊的內容，以避免在應用程式中的其他位置造成不正確的行為。

**許多 Windows api 都沒有 DPI 內容**

許多舊版 Windows api 都不會在其介面中包含 DPI 或 HWND 內容。 因此，開發人員通常必須執行額外的工作來處理任何 DPI 機密資訊的調整，例如大小、點或圖示。 例如，使用 [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) 的開發人員必須使用點陣圖延展已載入的圖示，或使用替代的 api 來載入適當 DPI 大小的正確圖示，例如 [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew)。

**強制重設整個進程的 DPI 感知**

一般而言，進程初始化之後，就無法變更您進程的 DPI 感知模式。 但是，如果您嘗試中斷視窗樹狀結構中的所有 hwnd 都有相同的 DPI 感知模式，Windows 可以強制變更您進程的 DPI 感知模式。 在所有版本的 Windows （從 Windows 10 1703），在不同的 DPI 感知模式中，hwnd 樹狀結構中不能有不同的 hwnd。 如果您嘗試建立中斷此規則的父子式關聯性，可以重設整個進程的 DPI 感知。 這可以透過下列方式觸發：

1.  一個 CreateWindow 呼叫，其中傳入的父視窗是與呼叫執行緒不同的 DPI 感知模式。
2.  這兩個視窗與不同 DPI 感知模式相關聯的 SetParent 呼叫。

下表顯示當您嘗試違反此規則時所發生的情況：



| 作業                 | Windows 8.1                                  | Windows 10 (1607 及更早版本)                 | Windows 10 (1703 和更新版本)                   |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| 在進程內) 的 CreateWindow (    | N/A                                          | **子系繼承** (混合模式)               | **子系繼承** (混合模式)               |
|  (跨進程) 的 CreateWindow | 呼叫端進程的 **強制重設** ()        | **子系繼承** (混合模式)               | 呼叫端進程的 **強制重設** ()        |
| SetParent (同進程)        | N/A                                          | 目前進程的 **強制重設** ()         | **失敗** (錯誤 \_ 的 \_ 狀態無效)              |
| SetParent (跨進程)     | 子視窗進程的 **強制重設** ()  | 子視窗進程的 **強制重設** ()  | 子視窗進程的 **強制重設** ()  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[高 DPI API 參考](high-dpi-reference.md)
</dt> <dt>

[混合模式 DPI 縮放比例和 DPI 感知 Api。](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

