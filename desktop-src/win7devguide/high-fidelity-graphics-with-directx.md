---
title: 使用 DirectX 的高精確度圖形
description: Windows 的應用程式開發人員一直使用 Microsoft DirectX 來提供高品質、硬體加速、3d 圖形。
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9ecb5d6403745162f19b16eea15c22ef7f9676b14bd291226af2f8321483b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086641"
---
# <a name="high-fidelity-graphics-with-directx"></a>使用 DirectX 的高精確度圖形

Windows 的應用程式開發人員一直使用 Microsoft DirectX 來提供高品質、硬體加速、3d 圖形。 當技術推出1995時，開發人員可以為遊戲和工程應用程式提供高品質的3D 圖形，讓玩家和專業人員願意為3D 圖形面板支付額外費用。 現在，即使是最便宜的電腦也包含可支援的3D 圖形硬體。

為了充分利用這些圖形功能，Windows Vista 引進了 Windows 顯示驅動程式模型 (WDDM) 基礎結構，可讓多個應用程式和服務共用圖形處理單元的資源 (GPU) 。 桌面視窗管理員 (DWM) 會使用這項技術來建立3d 工作切換的動畫、提供應用程式視窗的動態縮圖影像，以及為桌面應用程式提供 Windows 的 Aero 玻璃效果。

Windows 7 讓應用程式開發人員手上的圖形功能更多。 在一組新的 DirectXAPIs 中，Microsoft Win32 開發人員可以利用 Gpu 中最新的創新功能，將快速、可擴充、高品質、2D 和3D 圖形、文字和影像新增至其應用程式。 在最新的 *LCD* 顯示器上，DirectXAPIs 可使用每個色彩元件大於8個位的色彩深度，顯示桌面和視窗內容。

透過 directx，Win32 開發人員也可以使用 GPU 的平行處理原則來進行一般用途的計算，例如影像處理，並可轉譯成 directx 10 硬體、directx 9 硬體、CPU 或遠端 Windows 電腦。 這些技術的設計目的是要與 Windows 圖形裝置介面 (GDI) 和 Windows GDI+ 交互操作，以確保開發人員可以輕鬆地將現有的投資保留在 Win32 程式碼中。  (查看 [2009 年3月 DIRECTX SDK 的新功能](/previous-versions//bb173043(v=vs.85))。 ) 

這些增強的圖形功能是由下列以 *COM* 為基礎的 api 提供：

-   繪製2D 圖形的[Direct2D](../direct2d/direct2d-portal.md) 。
-   用來排列和轉譯文字的[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) 。
-   用於處理和顯示影像的[Windows 影像處理元件](/windows/desktop/wic/-wic-lh)。
-   用來繪製3D 圖形的[Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics) 。
-   適用于繪製3D 圖形的[Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ，並可讓您存取下一代 GPU 技術，例如鑲嵌式、對材質串流的支援有限，以及一般目的計算。
-   [DirectX Graphic Infrastructure (DXGI) ](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) 來管理本機和遠端顯示裝置和 GPU 資源，以及提供 DIRECTX 和 GDI 之間的互通性。

## <a name="direct2d"></a>Direct2D

[Direct2D](../direct2d/direct2d-portal.md)以 Microsoft Direct3D 10 為基礎，提供 Win32 開發人員立即模式、解析度無關的 2d api，使用下一代圖形硬體的強大功能，同時與現今的 GDI/GDI+ 應用程式和 Direct3D 10 應用程式交互操作。 Direct2D 提供高品質的2D 轉譯，效能優於 GDI 及 GDI+。 它可讓 Win32 開發人員更細微地控制資源和其管理。  (參閱 [Direct2D](../direct2d/direct2d-portal.md)。 ) 

## <a name="directwrite"></a>DirectWrite

現今許多應用程式都必須支援高品質的文字轉譯、解析度無關的大綱字型，以及完整的 Unicode 文字和版面配置支援。 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)是新的 DirectX 元件，可提供下列功能和更多功能：

-   與裝置無關的文字版面配置系統，可改善檔和 UI 中的文字可讀性。
-   可使用 GDI、 [Direct2D](../direct2d/direct2d-portal.md)或應用程式特定轉譯技術的高品質、子圖元、 *ClearType* 文字轉譯。
-   與 [Direct2D](../direct2d/direct2d-portal.md)搭配使用時，硬體加速文字。
-   支援多重格式的文字。
-   支援 *OpenType* 字型的先進印刷樣式功能。
-   支援所有支援語言的文字版面配置和轉譯。
-   GDI 相容的版面配置和轉譯。

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)字型系統可啟用「任意字型」字型使用方式，使用者不需要執行個別的安裝步驟就能使用字型，也可以使用改良的字型分組階層來協助進行手動或程式設計的字型探索。 這些 Api 支援測量、繪製和點擊測試多重格式的文字。 DirectWrite 處理全域和當地語系化應用程式的所有支援語言中的文字，並以 Windows 7 中找到的主要語言基礎結構為基礎。 DirectWrite 也為想要執行自己的版面配置和 Unicode 到影像處理的開發人員提供低層級的圖像轉譯 api。  (參閱[DirectWrite](../directwrite/direct-write-portal.md)。 ) 

## <a name="windows-imaging-component"></a>Windows Imaging Component

在 Windows Vista 中， [Windows 影像處理元件](/windows/desktop/wic/-wic-lh)引進了可延伸的架構，可用於處理影像和影像中繼資料。 Windows 影像處理元件支援的影像格式包括 *JPEG*、 *PNG* 和 *TIFF*，以及支援的元資料格式包括 *XMP* 和 *EXIF*。 使用 Windows 7，Windows 影像處理元件提供漸進式影像解碼、擴充的 *PNG* 功能、 *GIF* 中繼資料，以及橫跨 *APPn* 區段的中繼資料支援，藉此拓寬其標準合規性。  (查看[Windows 7 的 WIC 新功能](/previous-versions//ee720061(v=vs.85))。 ) 

## <a name="direct3d-11"></a>Direct3D 11

Microsoft direct3d 11 擴充了 Direct3D 10 管線的功能，並提供 Windows 的7個遊戲和高階3d 應用程式，並提供對即將推出的 gpu 和多核心 cpu 的有效率、穩固且可調整的存取。 除了 Direct3D 10 中所找到的功能之外，Direct3D 11 還引進了幾項新功能。

幾何和高序位介面現在可鑲嵌，以支援修補和細分表面表示中可調整的動態內容。

為了充分利用多個 CPU 核心提供的平行處理能力，多執行緒會將應用程式、執行時間和驅動程式呼叫分散到多個核心，以增加每個畫面格的潛在轉譯呼叫數目。 此外，資源的建立和管理已針對多執行緒使用進行優化，可為串流提供更有效率的動態材質管理。

已針對 Direct3D 11 建立新的一般用途計算著色器。 不同于現有的著色器，這些是可程式化管線的延伸模組，可讓您的應用程式完全在 GPU 上執行更多工作，而不受 CPU 影響。 在 Direct3D 10 中引進的 [**DrawAuto**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto)已擴充，可與計算著色器互動。

高階網底語言有幾項改良 ([HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)) ，例如著色器中的有限形式動態連結，以改善特製化複雜度，以及類別和介面等物件導向程式設計結構。  (查看 [2009 年3月 DIRECTX SDK 的新功能](/previous-versions//bb173043(v=vs.85))。 ) 

## <a name="direct3d-10-improvements"></a>Direct3D 10 改良功能

Direct3D 10 包含重新設計的圖形管線，具有可程式化的著色器階段和不可變的狀態物件，用於初始化固定函式階段。 狀態物件會簡化管線，並藉由最小化所需的狀態變更數目來提升效能。 著色器階段的可程式性現在提供高階的陰影語言延伸模組，以支援無限制的著色器指令、一般化的著色器資源，以及整數和位計算。

管線也會引進幾何著色器階段，以將整個工作從 CPU 卸載至 GPU。 這個新階段可讓您建立幾何、將資料串流至記憶體，以及轉譯沒有 CPU 互動的幾何。

另外還有其他幾項改良功能是為了加快效能而設計的。 前提轉譯會執行遮蔽剔除，以減少轉譯的幾何數量。 實例 Api 可透過繪製類似物件的多個實例，大幅減少需要傳輸至 GPU 的幾何量。 材質陣列可讓 GPU 在不需要 CPU 介入的情況下進行紋理交換。

Direct3D 10 和 Direct3D 11 新增了幾項功能，以擴充可使用這些 Api 設定的範圍。 [Windows Advanced 點陣平臺 (變形) ](/windows/desktop/direct3darticles/directx-warp)為 Direct3D 10 實行快速、多核心的可調整 CPU 轉譯，在沒有圖形硬體的系統上啟用全功能的圖形轉譯。 新增「功能等級」，特別稱為 [direct3d 10 層級 9](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9)，可讓 direct3d 10 和 direct3d 11APIs 驅動 Microsoft Direct3D 9 類別的硬體，並擴充 direct3d 10 或 direct3d 11 應用程式可將目標設為市場上幾乎每一部電腦系統的設定數目。  (參閱 [Direct3D 10 圖形](../direct3d10/d3d10-graphics.md)。 ) 

## <a name="directxgdi-interoperability"></a>DirectX/GDI 互通性

在 Windows Vista 中，使用 DirectX 和 GDI 轉譯為共用表面的應用程式行為會根據 DWM 是開啟或關閉而有所不同。 此外，當 DWM 開啟時，使用 DirectX 和 GDI 的應用程式在 Windows Vista 上的行為會與 Windows XP 不同。 這會導致許多 isv 在 Windows Vista 上執行應用程式時停用 DWM，以確保一致的行為。 透過 Windows 7 中的 DirectX 增強功能，應用程式現在可以自由混合 directx 和 GDI，而不需要停用 DWM。 Windows 7 也可利用更有效率的 Direct3D 10 api，針對需要在 DirectX 和 GDI 之間進行交互操作的案例提供更佳的效能。  (參閱 [Direct2D 和 GDI 互通性總覽](../direct2d/direct2d-and-gdi-interoperation-overview.md)。 ) 

 

 