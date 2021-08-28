---
title: 使用 DirectX 搭配高動態範圍顯示和進階色彩
description: 本主題提供使用 Windows 10 advanced color support 將高動態範圍 Direct3D 11 和 Direct3D 12 內容轉譯為 HDR10 顯示的技術總覽。
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 8577d9737bd1f5f22f5e550dbcef503151c84dc1a147cf510820b589283b4990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120559"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a>使用具有高動態範圍的 DirectX 顯示和先進的色彩

本主題提供使用 Windows 10 advanced color support 將高動態範圍 (HDR) Direct3D 11 和 Direct3D 12 內容輸出至 HDR10 顯示器的技術總覽。 它會摘要說明輸出至 HDR10 顯示器的一些主要概念差異，相較于傳統標準動態範圍 (SDR) 顯示。 此外，它也涵蓋了應用程式正確支援 Windows advanced color 以及建議和最佳作法的關鍵技術需求。

## <a name="introduction"></a>簡介

Windows 10 支援 HDR 和其他先進的色彩顯示，可提供比傳統 SDR 顯示明顯更高的色彩精確度。 您可以使用 Direct3D、Direct2D 和其他圖形 Api，將 HDR 內容轉譯成可顯示的功能。

Windows advanced color 指的是數個相關技術，第一次是在 Windows 10 1703 版中引進，以提供超過傳統標準動態範圍 (SDR) 顯示色彩功能的支援。 以下說明這三個主要的擴充功能。 最常見的 advanced color display （HDR10）類型支援這三種擴充功能。

### <a name="high-dynamic-range"></a>高動態範圍

動態範圍是指場景中最大和最小亮度之間的差異;這通常是以 nits) 的每個平方英尺 (candelas 來測量。 真實世界的場景（例如此終止）通常會有10個量級的亮度的動態範圍;人們可以在調整之後辨別更大的範圍。

![在標示的場景中具有亮度和最深點的終止圖](images/HDR-HDR.jpg)

自從 Direct3D 9 以來，圖形引擎能夠在內部呈現其幕後，且實際精確的精確度。 不過，一般標準動態範圍顯示只會重現3倍以上的亮度數量級，因此任何 HDR 轉譯的內容都必須 tonemapped (壓縮) 到有限的顯示範圍內。 新的 HDR 顯示，包括符合 HDR10 (BT) standard 的新 HDR，並突破這項限制。

### <a name="wide-color-gamut-with-automatic-system-color-management"></a>具有自動系統色彩管理的寬色彩範圍

色彩色域指的是顯示可能重現之色調的範圍和飽和度。 人類眼所能觀察到的最飽和自然色彩是純粹的單色 light，例如，鐳射產生什麼。 不過，主流取用者顯示器通常只能在 sRGB 範圍內重現色彩，這只代表所有人類可感知色彩的35%。 下圖是 "光譜 locus" 的標記法，或指定的亮度層級 (的所有可感知色彩) ，其中較小的三角形是 sRGB 範圍。

![人力光譜 locus 和 sRGB gamut 的圖表](images/HDR-WCG.jpg)

高層級的電腦顯示器具有長時間支援的色彩 gamuts，其寬度遠高於 sRGB，例如 Adobe RGB 和 D65-P3。 而這些寬範圍顯示變得更為普遍。 不過，在 advanced 色彩之前，Windows 不會執行應用程式的任何系統層級色彩管理。 這表示，如果轉譯的 DirectX 應用程式（例如，純紅色或 RGB (1.0、0.0、0.0) 至其交換鏈），Windows 只會掃描顯示器可能重現的最飽和紅色，無論顯示器的實際色彩範圍為何。

需要高顏色精確度的應用程式可以查詢顯示器的色彩功能 (例如，使用 ICC 設定檔) ，以及執行自己的同進程色彩管理，以正確地鎖定顯示器的色彩範圍。 不過，大部分的應用程式和視覺內容會假設顯示為 sRGB，而且它們依賴作業系統來滿足此假設。

Windows advanced 色彩會新增系統層級的自動色彩管理。 桌面視窗管理員 (DWM) 是 Windows ' 組合器。 啟用 advanced color 時，DWM 會從應用程式視覺內容的 colorspace 執行明確的色彩轉換，到標準的組合色彩空間，也就是 scRGB。 Windows 然後將組成的畫面格緩衝區內容轉換成顯示器的原生色彩空間。 如此一來，傳統的 sRGB 內容就會自動取得色彩精確的行為，而 advanced color 感知的應用程式可以利用顯示器的完整色彩功能。

### <a name="deep-precisionbit-depth"></a>深度精確度/位深度

數值有效位數（或位深度）指的是表示或區分相似但不同的色彩，而不含內條紋或成品。 主要電腦會顯示每個色頻支援8個位，而人類眼需要至少10-12 位的精確度來避免可感知扭曲，而不需要利用遞色或不同的視圖條件等技術。

![風車在每個顏色通道的模擬2位上的圖片，與每個通道8個位的圖片](images/HDR-bitdepth.jpg)

在使用 advanced 色彩之前，DWM 限制視窗化應用程式只會在每個顏色通道的8個位輸出內容，即使顯示器支援較高的位深度也一樣。 啟用 advanced color 時，DWM 會使用 IEEE 半精確度浮點數來執行其組合 (FP16) ，消除任何瓶頸，並允許使用顯示的完整精確度。

## <a name="system-requirements"></a>系統需求

### <a name="operating-system-os"></a>作業系統 (OS)

先進的色彩支援首次隨附于 Windows 10，版本1703，並已在每次更新時大幅改進。 本主題假設您的應用程式是以 Windows 10、1903版或更新版本為目標。

### <a name="display"></a>顯示

若要利用高動態範圍，您必須具有支援 HDR10 標準的顯示器。 Windows 最適合與已通過[DisplayHDR 認證](https://displayhdr.org/)的顯示器搭配使用。

### <a name="graphics-processor-gpu"></a>圖形處理器 (GPU) 

需要最新的 GPU。 若要支援 HDR10 顯示，Windows 10 需要下列其中一項。

* Nvidia GeForce 1000 系列 (Pascal) 或更新版本
* AMD Radeon RX 400 系列 (Polaris) 或更新版本
* 選取的 Intel Core 7 系列 (Kaby Lake) 或更新版本

請注意，視案例而定，需要額外的硬體需求，包括硬體編解碼器加速 (10 位 HEVC、10位 VP9 等等 ) 和 PlayReady 支援 (SL3000) 。 如需更具體的資訊，請洽詢您的 GPU 廠商。

### <a name="graphics-driver-wddm"></a>圖形驅動程式 (WDDM) 

強烈建議您從 Windows Update 或從 GPU 廠商或電腦製造商的網站，取得最新的可用圖形驅動程式。 針對 Windows 10、1903版和更新版本，我們建議支援至少 Windows 顯示驅動程式模型的驅動程式 (WDDM) 2.6 版。

## <a name="supported-rendering-apis"></a>支援的轉譯 Api

Windows 10 支援各種不同的轉譯 api 和架構。 先進的色彩支援基本上依賴您的應用程式，能夠使用 DXGI 或 Visual Layer Api 來執行新式簡報。

* [DirectX Graphic Infrastructure (DXGI) ](../direct3ddxgi/dx-graphics-dxgi.md)
* [視覺化層 (Windows) 的組合](/windows/uwp/composition/visual-layer)

因此，任何可以輸出至其中一種展示方法的轉譯 API 都可以支援 advanced 色彩。 這包括但不限於這些。

* [Direct3D 11](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [Direct3D 12](../direct3d12/direct3d-12-graphics.md)
* [Direct2D](../direct2d/direct2d-portal.md)
* [Win2D](https://github.com/Microsoft/Win2D)
  * 需要使用較低層級的 **CanvasSwapChain** 或 **CanvasSwapChainPanel** api。
* [**Windows.UI.Input.Inking**](/uwp/api/Windows.UI.Input.Inking)
  * 支援使用 DirectX 進行自訂的幹筆墨轉譯。
* [XAML](/windows/uwp/xaml-platform/)
  * 支援使用 **MediaPlayerElement** 播放 HDR 影片。
  * 支援使用 **Image** 元素解碼 JPEG XR 影像。
  * 支援使用 **SwapChainPanel** 的 DirectX interop。

## <a name="handling-dynamic-display-capabilities"></a>處理動態顯示功能

Windows 10 支援從電源有效率的整合式面板，到高階遊戲監視器和電視的強大高度色彩顯示。 Windows 使用者預期您的應用程式將能順暢地處理所有的變化，包括無所不在的現有 SDR 顯示器。

Windows 10 可對使用者提供 HDR 和 advanced color 功能的控制權。 您的應用程式必須偵測目前顯示器的設定，並動態回應功能的任何變更。 可能的原因有很多，例如，使用者啟用或停用某項功能，或是在不同顯示器之間移動應用程式，或系統的電源狀態變更。

### <a name="universal-windows-platform-uwp-apps"></a>通用 Windows 平台 (UWP) 應用程式

如果您要撰寫 UWP 應用程式，而不論您所使用的圖形轉譯 API 為何，請使用 [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) 來取得顯示功能。 從 [**DisplayInformation：： GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo)取得 **AdvancedColorInfo** 的實例。

若要檢查目前作用中的「高級」色彩種類，請使用 [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) 屬性。 在 Windows 10、1903版和更新版本中，這會傳回三個可能值的其中一個： **SDR**、 **WCG** 或 **HDR**。 這是最重要的檢查屬性，您應該設定轉譯和呈現管線以回應使用中的種類。

若要檢查支援的 advanced 色彩種類，但不一定要使用，請呼叫 [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable)。 例如，您可以使用此資訊來提示使用者流覽至 Windows 設定應用程式，讓他們可以啟用 HDR 或 WCG。

**AdvancedColorInfo** 的其他成員會提供有關面板實體色彩磁片區的量化資訊 (明亮度和色度) ，其對應于2006靜態 HDR 中繼資料。 您應使用此資訊來設定應用程式的 HDR tonemapping 和 gamut 對應。

若要處理 advanced color 功能的變更，請註冊 [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) 事件。 如果顯示的 advanced color 功能的任何參數因任何原因而變更，就會引發此事件。

藉由取得 **AdvancedColorInfo** 的新實例，並檢查哪些值已變更，來處理這個事件。

### <a name="desktop-win32-directx-apps"></a>Desktop (Win32) DirectX 應用程式

如果您要撰寫 Win32 應用程式，並使用 DirectX 轉譯，請使用 [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) 來取得顯示功能。 透過 [**IDXGIOutput6：： GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1)取得此結構的實例。

若要檢查目前作用中的「高階」色彩種類，請使用 [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)類型的 **ColorSpace** 屬性，並包含下列其中一個值：

* **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**，SDR
* **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**、HDR

> [!Note]
> 其他 advanced 色彩類型（例如 WCG）會被 DXGI 視為 SDR。 您無法使用 DXGI 來識別 WCG 顯示器。

> [!Note]
> DXGI 不會讓您檢查目前支援的 advanced 色彩類型，但目前不會使用。

**DXGI_OUTPUT_DESC1** 的其他成員大部分會提供與2006靜態 HDR 中繼資料相關之面板實體色彩磁片區的量化資訊， (亮度和色度) 。 您應使用此資訊來設定應用程式的 HDR tonemapping 和 gamut 對應。

Win32 應用程式沒有原生機制可回應 advanced color 功能變更。 相反地，如果您的應用程式使用轉譯迴圈，則您應該使用每個畫面格來查詢 [**IDXGIFactory1：： IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) 。 如果報告 **為 FALSE**，則您應該取得新的 **DXGI_OUTPUT_DESC1**，並檢查哪些值已變更。

此外，您的 Win32 訊息抽取應該會處理 [**WM_SIZE**](../winmsg/wm-size.md) 訊息，這表示您的應用程式可能已在不同顯示器之間移動。

> [!Note]
> 若要取得新的 **DXGI_OUTPUT_DESC1**，您必須取得目前的顯示。 不過，您不應該呼叫 **IDXGISwapChain：： GetContainingOutput**。 這是因為當 **DXGIFactory：： IsCurrent** 為 false，並重新建立交換鏈以將目前的輸出結果設為暫時性的黑色畫面時，交換鏈會傳回過時的 DXGI 輸出。 相反地，我們建議您列舉所有 DXGI 輸出的界限，並判斷哪一個輸出與您應用程式視窗的範圍有最大的交集。

下列程式碼範例來自于 [DirectX-圖形範例存放庫](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR)。

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a>設定您的 DirectX 交換鏈

一旦您判斷出目前的顯示器支援 advanced color 功能之後，請依照下列方式設定交換鏈。

### <a name="use-a-flip-presentation-model-effect"></a>使用翻轉展示模型效果

使用 CreateSwapChainFor 建立交換鏈時 **[Hwnd |組合 |CoreWindow]** 方法中，您必須選取 [ **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** ] 或 [ **DXGI_SWAP_EFFECT_FLIP_DISCARD** ] 選項來使用 DXGI 翻轉模型，讓您的交換鏈符合從 DWM 和各種全螢幕優化進行的 advanced color 處理。 如需詳細資訊，請參閱，以取得 [最佳效能，請使用 [DXGI 反轉模型](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) ] 主題。

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a>選項 1。 使用 FP16 像素格式和 scRGB 色彩空間

Windows 10 支援兩種主要的像素格式和色彩空間組合，以用於 advanced 色彩。 根據您應用程式的特定需求選取一個。

針對一般用途的應用程式，在建立交換鏈時，建議您指定 [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)。 這在您的 [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)也稱為 *FP16* 。 根據預設，以浮點數像素格式建立的交換鏈會視為使用 [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) 色彩空間，也稱為 *scRGB*。

這種組合可提供您數位範圍和精確度，以指定幾乎任何實際可能的色彩，並執行任意處理，包括混色。 此外，如果您使用的是 Direct2D、Win2D 或 Windows，則這是包含 advanced color 內容之任何交換鏈或中繼目標的唯一支援組合。 

此選項的主要缺點是，它會每圖元耗用64位，相較于傳統 UINT8 的 SDR 像素格式，這會使 GPU 頻寬和記憶體耗用量加倍。 此外，scRGB 使用非正規化 [0，1] 範圍內的數值，表示位於 sRGB 範圍之外的色彩，以及/或大於 80 nits 的亮度。 例如，scRGB (1.0、1.0、1.0) 以 80 nits 編碼標準 D65 白色;但是，scRGB (12.5、12.5、12.5) 會以較亮的 1000 nits 編碼相同的 D65 白色。 某些圖形作業需要標準化的數值範圍，您必須修改作業或重新標準化色彩值。

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a>選項2：使用 UINT10/RGB10 像素格式和 HDR10/BT. 2100 色彩空間

針對使用 HDR10 編碼內容的應用程式（例如 media player），或是預期在全螢幕案例（例如遊戲）中使用的應用程式，在建立交換鏈時，您應該考慮在 [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)中指定 [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 。 根據預設，這會被視為使用 sRGB 色彩空間;因此，您必須明確地呼叫 [**IDXGISwapChain3：： SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)，並設定為您的色彩空間 [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)，也稱為 HDR10/BT. 2100。

相較于 FP16，此組合具有更嚴格的限制。 您只能將此使用於 Direct3D 11 或 Direct3D 12。 此外，UINT10/HDR10 具有中繼格式的限制，因為它會使用 2084 EOTF ( "gamma" 函式) （高度非線性），並將其優化為電傳格式，因為它只提供2位的 Alpha。

不過，在應用程式的最終輸出中使用時，此組合可以提供強大的效能優化。 它會使用與傳統 UINT8 SDR 像素格式相同的每個圖元32位。 此外，在特定的全螢幕案例中，作業系統可以直接掃描 HDR10 介面，以優化效能。

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a>當顯示器處於 SDR 模式時使用 advanced 色交換鏈

即使顯示器不支援您的內容所需的部分或所有高階色彩功能，您也可以使用 advanced color swap chain。 在這些情況下，桌面視窗管理員 (DWM) 會 downconvert 您的內容以符合顯示器的功能。 在 Windows 10、1903版和更新版本中，它會執行數位裁剪;例如，如果您轉譯成 FP16 的 scRGB 交換鏈，則會裁剪 [0，1] 數值範圍以外的所有專案。

如果您的應用程式視窗 straddling 了具有不同 advanced 色彩功能的兩個或多個顯示，也會發生此 downconversion 行為。 **AdvancedColorInfo** 和 **IDXGIOutput6** 是抽象化的，只會報告「主要」顯示的特性 (定義為包含視窗) 中央的顯示。

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a>使用 SDR 參考白色層級正確轉譯 SDR 內容

在許多案例中，您的應用程式會想要同時轉譯 SDR 和 HDR 內容;例如，透過 HDR 影片轉譯字幕或傳輸控制項，或將 UI 轉譯為遊戲場景。 請務必瞭解 *sdr 參考白色層級* 的概念，以確保您的 sdr 內容在 HDR 顯示器上看起來正確。

Windows 會將 HDR 內容視為 _場景參考_，表示特定的色彩值應該顯示在特定的亮度層級;例如，scRGB (1.0、1.0、1.0) 和 HDR10 (497、497、497) 都會以 80 nits 的亮度來精確編碼 D65 的白色。 同時，通常會將 SDR 內容視為 _輸出參考_ (或顯示) ，這表示其亮度會保留給使用者或裝置;例如，sRGB (1.0、1.0、1.0) 將 D65 白色編碼為 HDR 範例中的白色，但在任何亮度最高的情況下，會為其設定顯示的亮度。 Windows 可讓使用者將 [ _SDR 參考] 的白色層級_ 調整為其喜好設定;這是 Windows 將會轉譯 sRGB (1.0、1.0、1.0) 的亮度。 在桌面 HDR 監視器上，SDR 參考白色層級通常設定為大約 200 nits。

> [!Note]
> 在支援亮度控制項（例如膝上型電腦）的顯示器上，Windows 也會調整 HDR () 場景的亮度，以符合使用者所需的亮度層級，但應用程式看不到這一點。 除非您嘗試保證 HDR 信號的精確度重現，否則您通常可以忽略此情況。

如果您的應用程式一律會將 SDR 和 HDR 轉譯成不同的表面，並依賴作業系統組合，則 Windows 會自動執行正確的調整，以將 sdr 內容提升為所需的白色層級。 例如，如果您的應用程式使用 XAML，並將 HDR 內容轉譯為它自己的 **SwapChainPanel**。

但是，如果您的應用程式會將自己的 SDR 和 HDR 內容組合成單一介面，您就必須自行負責執行 SDR 參考白色層級調整。 否則，如果有一般的桌上型電腦觀賞條件，則 SDR 內容可能會顯得太暗。 首先，您必須取得目前的 SDR 參考白色層級，然後您必須調整您正在轉譯之任何 SDR 內容的色彩值。

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a>步驟 1： 取得目前的 SDR 參考白色層級

目前，只有 UWP 應用程式可以透過 [**AdvancedColorInfo SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits)取得目前的 SDR 參考白色層級。 此 API 需要 [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)。

### <a name="step-2-adjust-color-values-of-sdr-content"></a>步驟 2： 調整 SDR 內容的色彩值

Windows 定義 80 nits; 的名義或預設參考白色層級因此，如果您要轉譯標準 sRGB (1.0、1.0、1.0) 白色 FP16 交換鏈，則會以 80 nits 的亮度重現。 為了符合實際的使用者定義參考白色層級，您必須將來自 80 nits 的 SDR 內容調整為透過 **AdvancedColorInfo SdrWhiteLevelInNits** 所指定的層級。

如果您是使用 FP16 和 scRGB 進行轉譯，或是使用線性 (1.0) gamma 的任何色彩空間，則您只要將 SDR 色彩值乘以 _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_ 就可以了。 如果您使用的是 Direct2D，則會有預先定義的常數 [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f)，其值為80。

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

如果您要使用非線性 gamma 色彩空間（例如 HDR10）進行轉譯，則執行 SDR 白色層級調整更為複雜;如果您要撰寫自己的圖元著色器，您應該考慮轉換成線性 gamma 以套用調整。

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a>使用 tonemapping 將 HDR 內容調整為顯示器的功能

HDR 和 advanced 色彩的顯示方式在其功能方面會有很大的差異。 例如，最小和最大的亮度，以及它們能夠重現的色彩範圍。 在許多情況下，您的 HDR 內容將包含超過顯示功能的色彩。 為了獲得最佳的影像品質，您必須執行 HDR tonemapping，基本上是壓縮色彩範圍以符合顯示，同時最能保留內容的視覺意圖。

要適應的最重要單一參數是最大的亮度，也稱為 MaxCLL (內容精簡級) ;更精密的 tonemappers 也會調整最小的亮度 (MinCLL) 和/或色彩主要複本。

### <a name="step-1-get-the-displays-color-volume-capabilities"></a>步驟 1： 取得顯示器的色彩音量功能

#### <a name="universal-windows-platform-uwp-apps"></a>通用 Windows 平台 (UWP) 應用程式

使用 [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) 來取得顯示器的色彩音量。

#### <a name="win32-desktop-directx-apps"></a>Win32 (desktop) DirectX 應用程式

使用 [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) 取得顯示器的色彩音量。

### <a name="step-2-get-the-contents-color-volume-information"></a>步驟 2： 取得內容的色彩量資訊

根據您的 HDR 內容來源位置而定，有多種可能的方式可判斷其亮度和色域資訊。 某些 HDR 影片和影像檔案包含2006中繼資料。 如果您的內容是以動態方式轉譯，則您可以從內部轉譯階段中解壓縮場景資訊，例如場景中最亮的光源。

更一般但計算成本昂貴的解決方案，是在轉譯的框架上執行長條圖或其他分析階段。 [Direct2D advanced color IMAGES SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)示範如何使用 Direct2D 進行此作業;最相關的程式碼片段包含在下面：

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a>步驟 3： 執行 HDR tonemapping 操作

Tonemapping 本身就是一個失真的程式，可針對許多感知或目標計量進行優化，因此沒有一個標準演算法。 Windows 在 Direct2D 和媒體基礎 HDR 影片播放管線中提供內建的[HDR tonemapper 效果](../direct2d/hdr-tone-map-effect.md)。 一些其他常用的演算法包括 ACE Filmic、Reinhard 和 ITU-R BT. 2390-3 EETF (電氣傳輸功能) 。

簡化的 Reinhard tonemapper 運算子如下所示。

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a>捕獲 HDR 和 WCG 內容

支援指定像素格式的 Api，例如 Windows 中的格式 [**。**](/uwp/api/windows.graphics.capture)IDXGIOutput5： capture 命名空間和 [**：:D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1)方法，提供在不遺失圖元資訊的情況下，捕獲 HDR 和 WCG 內容的功能。 請注意，在取得內容畫面格之後，需要進行額外的處理。 例如，HDR 與 SDR 的音調對應 (例如，SDR 螢幕擷取畫面會複製網際網路共用) ，並以適當的格式儲存內容 (例如，JPEG XR) 。

## <a name="additional-resources"></a>其他資源

* 搭配 directx [11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)directx 12 *的 directx 工具套件使用 HDR* 轉譯  /  [](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering)。 逐步解說如何使用 DirectX 工具套件 (DirectXTK) ，將 HDR 支援新增至 DirectX 應用程式。
* [Direct2D advanced color IMAGES SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)。 UWP SDK 範例會使用 Direct2D 來執行 advanced color 感知 HDR 和 WCG 影像檢視器。 示範 UWP 應用程式的各種最佳做法，包括回應顯示功能變更，以及對 SDR 白色層級進行調整。
* [Direct3D 12 HDR desktop 範例](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR)。 執行基本 Direct3D 12 HDR 場景的桌面 SDK 範例。
* [Direct3D 12 HDR UWP 範例](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR)。 與上述範例相同的 UWP。
* [XBOX ATG SIMPLEHDR PC 範例](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC)。 執行基本 Direct3D 11 HDR 場景的桌面 SDK 範例。
