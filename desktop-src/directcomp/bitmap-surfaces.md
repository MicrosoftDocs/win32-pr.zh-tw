---
title: 點陣圖物件
description: 本主題說明 DirectComposition 支援的點陣圖內容類型。
ms.assetid: BC32CF76-D5E4-4B25-AFD5-42E8DABFA0D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c390778fef1ee7ad96c90a8b7706fa635f3615ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382722"
---
# <a name="bitmap-objects"></a>點陣圖物件

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

Microsoft DirectComposition 是點陣圖組合引擎。 它可讓應用程式開發人員結合多個點陣圖，並以各種方式操作它們，以在應用程式 UI 中達成有趣的視覺效果和動畫。 本主題說明 DirectComposition 支援的點陣圖內容類型。

-   [點陣圖內容](#bitmap-content)
    -   [影片記憶體點陣圖](#video-memory-bitmaps)
    -   [視窗點陣圖](#window-bitmaps)
    -   [建立點陣圖內容與視覺效果的關聯](#associating-bitmap-content-with-a-visual)
    -   [Alpha 色板](#alpha-channel)
-   [相關主題](#related-topics)

## <a name="bitmap-content"></a>點陣圖內容

應用程式會藉由建立視覺物件，然後設定這些物件的 [content 屬性](basic-concepts.md) ，提供 DirectComposition 和點陣圖內容以供撰寫和建立動畫。 DirectComposition 不提供任何的點陣化服務。 應用程式必須使用其他以軟體為基礎或硬體加速的點陣化程式庫（例如 [Direct2D](../direct2d/direct2d-portal.md) 或 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ）來填入要組成的點陣圖。 撰寫之後，DirectComposition 會將構成點陣圖內容的傳遞至 [桌面視窗管理員 (DWM) ](/windows/desktop/dwm/dwm-overview) 以轉譯至螢幕。

**支援的點陣圖內容類型**  Microsoft DirectComposition 支援下列幾種點陣圖：

-   [影片記憶體點陣圖](#video-memory-bitmaps)
-   [視窗點陣圖](#window-bitmaps)

### <a name="video-memory-bitmaps"></a>影片記憶體點陣圖

影片記憶體點陣圖會使用 Microsoft DirectX 方法在硬體中進行柵格化， (包括 DX 對 GDI interop 模型) 。 它是由呼叫應用程式和 DirectComposition 可看見的跨進程共用表面所支援。 因為應用程式只能從 DirectComposition 材質的介面讀取，所以影片記憶體點陣圖不會遭到破壞。

### <a name="video-content"></a>影片內容

應用程式可以使用 DirectComposition 來撰寫影片畫面，以使用系結至 DirectComposition 介面的 DirectX 無視窗交換鏈。 就概念而言，DirectComposition 會將影片內容視為一系列的點陣圖。 DirectComposition 並不提供呈現影片畫面的方法。

DirectComposition 支援 DirectX 無視窗交換鏈（也就是未系結至特定視窗的交換鏈），並可讓兩個不同的應用程式跨進程界限共用無視窗的交換鏈。 共用無視窗交換鏈可啟用在一個進程中建立交換鏈的影片案例，並在第二個進程中搭配 DirectComposition 使用。 無視窗的交換鏈是使用 [**IDXGIFactory2：： CreateSwapChainForCompositionSurface**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) 方法建立的。

如需有關 DirectX 交換鏈的詳細資訊，請參閱 [DXGI 總覽](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)。

### <a name="stereo-content"></a>身歷聲內容

就概念而言，身歷聲交換鏈是由 Microsoft DirectX Graphic Infrastructure (DXGI) 表面，代表身歷聲3D 內容的左右聲道。 當使用身歷聲交換鏈作為視覺效果的點陣圖資源時，DirectComposition 會以身歷聲撰寫。 所有非身歷聲內容 (mono 內容) 都會被視為具有相同的左和右通道內容;也就是說，這兩個通道都使用相同的點陣圖內容。 DirectComposition 會個別撰寫所有的左邊內容和所有正確的內容。 如果顯示裝置的功能不是身歷聲，DirectComposition 會根據應用程式) 作為 mono 內容，並只使用點陣圖資源的資料來撰寫，來處理左邊或右邊的身歷聲通道 (。

DirectComposition 不支援建立或操作身歷聲內容，也無法將 mono 交換鏈升階為身歷聲配對。 應用程式必須先執行這些工作，才能將 DirectX 身歷聲內容呈現給 DirectComposition。 此外，應用程式必須提供深度感知的左邊和右邊通道位移;DirectComposition 無法調整左右通道位移，以修改已知的 DirectX 身歷聲內容深度。

當有支援身歷聲的硬體可用時，就會將 DirectX 身歷聲內容撰寫並保存到 DWM。

### <a name="window-bitmaps"></a>視窗點陣圖

「視窗點陣圖」不是真正的點陣圖，而是 DirectComposition 以分層最上層或子視窗的 rasterizations 即時取代的預留位置。 視窗點陣圖類似于 DWM 縮圖，不同之處在于縮圖可能包含許多視窗的投稿，例如擁有的非子視窗，而 DirectComposition 視窗點陣圖一律只是一個視窗和其子系的標記法。

由於 DirectComposition 可以存取所有視窗和所有視覺化樹狀結構的重新導向介面，因此它可以在多個視覺化樹狀結構中重複使用某個視窗的內容。 視窗必須分層，因為非分層視窗沒有專用的重新導向介面，因此它的點陣化不一定可供 DirectComposition。

若要使用視窗點陣圖，應用程式會將視覺效果與視窗控制碼產生關聯 (HWND) 。 之後，當視窗的內容變更時，DirectComposition 會重新撰寫視覺效果，包括當內容變更為與視窗相關聯的視覺化樹狀結構的結果時。 換句話說，如同 DWM 縮圖，DirectComposition 視窗點陣圖也是「即時」。

### <a name="associating-bitmap-content-with-a-visual"></a>建立點陣圖內容與視覺效果的關聯

針對這三種點陣圖，應用程式可以將相同點陣圖與多個視覺效果產生關聯，這表示單一記憶體配置可以用來顯示相同的內容數次。

### <a name="alpha-channel"></a>Alpha 色板

所有點陣圖都有32位的每個圖元 (BPP) 格式，其中包含8個位的每圖元透明度。 但是，應用程式可以指定 DirectComposition 應該如何使用 Alpha 色板。 尤其是，DirectComposition 可以採用 Alpha 色板，也可以完全忽略 Alpha，在這種情況下，點陣圖會被視為完全不透明。

額外的 Alpha 模式會忽略 Alpha 色板，但是會將紅色、綠色和藍色值視為每個通道的 Alpha 值，而不是將這些通道的一般轉譯視為色彩濃度。 這種模式適用于 ClearType 轉譯，需要有子圖元的涵蓋範圍資訊。 若要使用每個通道的 Alpha 模式，應用程式必須先使用 [Direct2D](../direct2d/direct2d-portal.md) 和 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) 將子圖元涵蓋範圍資料寫入點陣圖。 接下來，應用程式必須設定正確的 Alpha 模式，並在將點陣圖與視覺效果關聯時指定文字色彩。 DirectComposition 會將文字色彩與涵蓋範圍資料混合，以針對背景產生 ClearType 混色。

在 ClearType 演算法不適用的情況下（例如，如果點陣圖不是圖元對齊且軸對齊），或者如果需要繪製到中繼介面，DirectComposition 可以使用點陣圖中的子圖元涵蓋範圍資料，自動產生灰階的點陣化，而不會產生額外的費用。

如需詳細資訊，請參閱 [**IDCompositionDevice：： CreateSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurface)或 [**IDCompositionDevice：： CreateVirtualSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface)函數之 *AlphaMode* 參數的描述。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectComposition 概念](directcomposition-concepts.md)
</dt> </dl>

 

 