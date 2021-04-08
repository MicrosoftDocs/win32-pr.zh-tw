---
title: Windows Advanced 點陣化平臺 (變形) 指南
description: 本文說明 Windows Advanced 點陣化平臺 (變形) 和下列各方面的變形。
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c09c29dd7b935542f0238cde0a71cbc97fce23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682843"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Windows Advanced 點陣化平臺 (變形) 指南

本文說明 Windows Advanced 點陣化平臺 (變形) 和下列各方面的變形。

-   [什麼是變形？](#what-is-warp)
-   [彎曲的優點](#warp-benefits)
    -   [移除自訂軟體 Rasterizers 的需求](#removing-the-need-for-custom-software-rasterizers)
    -   [從圖形硬體啟用最大效能](#enabling-maximum-performance-from-graphics-hardware)
    -   [當 Direct3D 硬體無法使用時啟用轉譯](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [運用現有的軟體轉譯資源](#leveraging-existing-resources-for-software-rendering)
    -   [啟用不需要圖形硬體的案例](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [完成 DirectX 圖形平台](#completing-the-directx-graphics-platform)
-   [變形功能和需求](#warp-capabilities-and-requirements)
-   [如何使用變形](#how-to-use-warp)
-   [適用于變形的建議應用程式類型](#recommended-application-types-for-warp)
    -   [休閒遊戲](#casual-games)
    -   [現有的非遊戲應用程式](#existing-non-gaming-applications)
    -   [先進的轉譯遊戲](#advanced-rendering-games)
    -   [其他應用程式](#other-applications)
-   [變形架構和效能](#warp-architecture-and-performance)
-   [扭曲一致性](#warp-conformance)

## <a name="what-is-warp"></a>什麼是變形？

變形是高速、完全一致的軟體轉譯器。 它是由 Direct3D 11 執行時間引進的 DirectX 圖形技術元件。 您可以使用 KB971644 更新，在 Windows 7、Windows Server 2008 R2 和 Windows Vista 上安裝 Direct3D 11 執行時間 \[ \] 。 上述 Windows 8、Windows 10、Windows Server 2012 & 和 Windows RT 包含 Direct3D 11.1 執行時間，其具有更新版的變形。 Windows 10 Fall Creators Update (1709) 包含支援 Direct3D 11 和 Direct3D 12 執行時間的變形版本。

## <a name="warp-benefits"></a>彎曲的優點

變形可提供下列優點：

-   [移除自訂軟體 Rasterizers 的需求](#removing-the-need-for-custom-software-rasterizers)
-   [從圖形硬體啟用最大效能](#enabling-maximum-performance-from-graphics-hardware)
-   [當 Direct3D 硬體無法使用時啟用轉譯](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [運用現有的軟體轉譯資源](#leveraging-existing-resources-for-software-rendering)
-   [啟用不需要圖形硬體的案例](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [完成 DirectX 圖形平台](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>移除自訂軟體 Rasterizers 的需求

變形可簡化開發工作，方法是免除建立自訂軟體轉譯器的需求，並為其調整應用程式，而不是調整應用程式的硬體。 藉由提供單一的一般用途軟體轉譯器，您就不再需要以多種方式撰寫映射轉譯演算法，就能在具有不同特性和功能的硬體或軟體上執行。 您仍然可以透過多種方式來執行演算法，以達到更佳的效能或調整;不過，您不需要變更用來執行這些演算法的 API 或轉譯架構。 相反地，您可以專注于建立絕佳的 Direct3D 10 或更新版本的應用程式，使其看起來相同，並在硬體或軟體中執行得很好。

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>從圖形硬體啟用最大效能

當應用程式調整為有效率地在硬體上執行時，它也會在變形時有效率地執行。 反之也成立;任何調整為可在變形上正常執行的應用程式，都能在硬體上順利執行。 使用 Direct3D 10 和更新版本的應用程式，可能無法在不同硬體上有效率地調整規模。 對硬體的變形具有類似的效能設定檔，因此針對大型批次調整應用程式、將狀態變更降至最低、移除同步處理的點或鎖定將可受益于硬體和變形。

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>當 Direct3D 硬體無法使用時啟用轉譯

變形可在各種情況下快速轉譯，而不需要或無法使用硬體，包括：

-   當使用者沒有任何支援 Direct3D 的硬體時
-   當應用程式以服務的形式或在伺服器環境中執行時
-   當應用程式想要保留 Direct3D 硬體資源供其他用途使用時
-   未安裝視訊卡時
-   當視頻驅動程式無法使用或無法正常運作時
-   當視訊卡記憶體不足、停止回應，或需要太多系統資源才能初始化

### <a name="leveraging-existing-resources-for-software-rendering"></a>運用現有的軟體轉譯資源

有很大的社區、許多書籍、網站、Sdk、範例、白皮書、郵寄清單和其他資源，可協助您利用 Direct3D 10 和更新版本的著色器型影像呈現。 您可以利用變形作為軟體回復，在使用硬體或軟體執行應用程式時，使用現有的硬體相關知識來改善應用程式的效能。 此外，來自圖形配接器廠商和 DirectX SDK 的許多絕佳工具，都可協助您設計、建立、開發、偵測及分析圖形應用程式的效能問題。 這些工具和知識現在可讓您在使用變形時，對以硬體和軟體為目標的應用程式開發獲益。

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>啟用不需要圖形硬體的案例

各種演算法和應用程式 (影像處理演算法、列印、遠端處理、虛擬電腦和其他模擬器、高品質的字型轉譯、圖表、圖形等) 通常已針對 CPU 優化，因為它們並不相依于硬體。 透過變形，您可以使用單一架構來執行這些演算法和應用程式，並可在軟體中完整執行;但是，如果有硬體加速可用，您可以利用它。

### <a name="completing-the-directx-graphics-platform"></a>完成 DirectX 圖形平台

即使在沒有 Direct3D 10 和更新版本的圖形硬體的電腦上，變形也可讓您存取所有 Direct3D 10 和更新版本的圖形功能。 Direct3D 10 已移除功能位 (caps) ;也就是說，您不再需要驗證圖形硬體是否有圖形功能可供使用，因為 Direct3D 10 和更新版本保證此可用性。 您現在可以使用各式各樣視訊卡的所有功能，知道其應用程式的行為和外觀都相同。 您可以調整這些應用程式的效能，只要在低端視訊卡上停用昂貴的圖形功能，或轉譯成較小的目標。

## <a name="warp-capabilities-and-requirements"></a>變形功能和需求

變形完全支援所有 Direct3D 10 和10.1 功能。 例如，「變形」支援下列最重要的功能：

-   Direct3D 10 和10.1 規格的所有有效位數需求
-   Direct3D 11 搭配功能層級 9 \_ 1、9 \_ 2、9 \_ 3、10 \_ 0 和 10 1 (使用時，如需 \_ 功能等級的詳細資訊，請參閱 [**D3D \_ 功能 \_ 層級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)) 
-   所有選用的材質格式，例如從浮點數呈現的多重取樣轉譯目標和取樣
-   反鋸齒的高品質轉譯，高品質的高品質轉譯 (MSAA) 
-   各向異性篩選
-   32位和64位應用程式和大型位址感知32位應用程式

當您在 Windows 7 SP1 或 Windows Server 2008 R2 SP1 上安裝 [適用于 windows 7 的平臺更新](https://support.microsoft.com/kb/2670838) 時，該作業系統接著會包含 direct3d 11.1 執行時間，以及在與 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1、9 \_ 2、9 \_ 3、10 \_ 0、10 \_ 1 和 11 \_ 0 搭配使用時，支援 direct3d 11. x 的變形版本。

Windows 8、Windows 10、Windows Server 2012 & 以上，且 Windows RT 包含 Direct3D 11.1 執行時間和新版本的變形。 此版本在與 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1、9 \_ 2、9 \_ 3、10 \_ 0、10 \_ 1、11 \_ 0 和 11 \_ 1 搭配使用時，支援 Direct3D 11. x。

Windows 10 Fall Creators Update (1709) 包含新版本的變形，支援 [Direct3D 12](../direct3d12/direct3d-12-graphics.md) 功能等級 12 \_ 0 和 12 \_ 1。 

變形的最小電腦需求與 Windows Vista 的需求相同，特別是：

-   最小 800 MHz CPU
-   不需要 MMX、SSE 或 SSE2
-   最小 512 MB 的 RAM

## <a name="how-to-use-warp"></a>如何使用變形

Direct3D 10、10.1、11和12元件可以使用您在建立裝置時可指定的其他驅動程式類型 (例如，當您) 呼叫 [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) 函式時。 此驅動程式類型為 [**D3D10 \_ 驅動程式 \_ 類型 \_ 彎曲**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) 或 [**D3D \_ 驅動程式 \_ 類型的 \_ 變形**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)。 當您指定此驅動程式類型時，執行時間會建立變形裝置，而且不會初始化硬體裝置。

由於變形使用的是與參考轉譯器相同的 Direct3D 軟體介面，因此可支援使用參考轉譯器來執行的任何 Direct3D 應用程式都可以使用變形進行測試。 若要使用變形，請將 D3d10warp.dll 重新命名為 D3d10ref.dll，並將它放在與範例或應用程式相同的資料夾中。 接下來，當您切換至 ref 時，您會看到變形轉譯。

如果您將變形重新命名為 D3d10ref.dll，並將其放在 C： \\ Program Files (x86) \\ MICROSOFT DirectX SDK (2010 年6月) \\ 範例 \\ c + + \\ Direct3D \\ Bin \\ x86，您可以按一下範例中的 [切換參考] 按鈕，或使用命令列上指定的/ref 執行範例，以針對變形執行所有 DirectX 範例。

## <a name="recommended-application-types-for-warp"></a>適用于變形的建議應用程式類型

所有能夠使用 Direct3D 的應用程式都可以使用變形。 這包括下列類型的應用程式：

-   [休閒遊戲](#casual-games)
-   [現有的非遊戲應用程式](#existing-non-gaming-applications)
-   [先進的轉譯遊戲](#advanced-rendering-games)
-   [其他應用程式](#other-applications)

### <a name="casual-games"></a>休閒遊戲

遊戲通常有簡單的呈現需求。 不過，它們也需要使用可能需要硬體加速的令人印象深刻的視覺效果。 大部分適用于 Windows 的最優秀銷售遊戲專案都是模擬或休閒的遊戲，兩者都不需要高效能圖形。 不過，這兩種遊戲樣式大幅受益于新式著色器式圖形以及調整硬體的能力。

### <a name="existing-non-gaming-applications"></a>現有的非遊戲應用程式

大量圖形應用程式在其轉譯層中需要的程式碼路徑數目不限。 「變形」可讓這些應用程式執行以大量電腦設定為目標的單一 Direct3D 程式碼路徑。

### <a name="advanced-rendering-games"></a>先進的轉譯遊戲

遊戲開發人員可能會想要找出圖形配接器或驅動程式特定的轉譯錯誤。 因此，所有遊戲（甚至是極具圖形需求的遊戲），都可以利用變形來呈現其內容。 您可以使用變形來驗證您發現的任何視覺構件是轉譯錯誤或硬體或驅動程式的問題。

### <a name="other-applications"></a>其他應用程式

適用于變形的目標應用程式也包含可能目前未使用 Direct3D 10 或 Direct3D 10.1 的應用程式。 這些目標應用程式包括必須一律在所有電腦上運作的應用程式、不寫入影像處理演算法之 CPU 和 GPU 版本的影像處理應用程式、速度或使用 GPU 的影像處理演算法不重要，例如列印，以及顯示先進3D 圖形的模擬器和虛擬環境。

## <a name="warp-architecture-and-performance"></a>變形架構和效能

變形是以參考轉譯器程式碼基底為基礎。 因此，「變形」會對 Direct3D 10 和更新版本和 DXGI 使用相同的軟體介面。 在 Windows 7 中，[windows 系統] 資料夾中的 [D3d10warp.dll] 中包含了變形。 64位電腦上安裝了兩個版本的變形，也就是 x86 和 x64 版。 在特定情況下，x64 版本的執行速度可能較快，因為包含在變形中的程式碼產生器可以利用使用者執行64位應用程式時可用的其他暫存器。

變形包含下列兩個高速的即時編譯器：

-   高階的中繼語言編譯器，可將 HLSL 位元組程式碼和目前的轉譯狀態轉換成幾何著色器 (GS) 、頂點著色器 (VS) 和圖元著色器 (PS) 管線階段的工作流程。
-   高效能的即時程式碼產生器，可採用這些命令，並產生優化的 SSE2、SSE 4.1、x86、x64、arm 和 arm64 元件程式碼。

「變形」會使用在 Windows Vista 中引進的執行緒集區和複雜的工作管理和相依性追蹤，讓轉譯管線的所有部分能有效率地分散到可用的 CPU 核心上。

變形會使用延後轉譯。 也就是說，變形可以批次轉譯命令，只有當有足夠的資料可有效率地使用所有 CPU 資源時，才會進行點陣化。 在主應用程式執行緒上工作會最小化，讓應用程式能儘快提交命令。 如果應用程式也是多執行緒的應用程式，而且它使用執行緒集區，則工作會平均分散在變形與應用程式之間。

已調整變形程式碼產生器，以充分利用新式 CPU 架構。 即使電腦不支援 SSE，還是可以執行 Windows Vista 和更新版本作業系統的所有電腦上的變形。 不過，已針對支援 SSE2 的電腦優化變形。 它也包含 AMD 和 Intel 處理器特定架構的優化，以及 SSE 4.1 擴充功能的支援。

變形不需要圖形硬體即可執行。 即使在硬體無法使用或無法初始化的情況下，它也可以執行。

為了在 Direct3D 10 和更新版本的硬體上執行而設計和建立的應用程式和範例，在沒有任何變形的情況下，可能會使用變形來正常執行。 不過，我們建議您盡可能降低品質設定和解析度，以達到可用的畫面播放速率。 您可以使用變形來開發和調整可在硬體和軟體上正常執行的應用程式。

由於變形會使用多個 CPU 核心，因此最適合用於新式的四核心 Cpu。 在已安裝 SSE 4.1 擴充功能的電腦上，變形也會明顯地執行。 Microsoft 在具有八個或更多核心和 SSE 4.1 的電腦上執行了大幅的測試和效能調整，因為這些高階電腦在 Windows 7 和更新版本的作業系統存留期間將會越來越普遍。

當變形在 CPU 上執行時，相較于圖形配接器，會有數種限制。 CPU 的前端匯流排速度通常大約或低於 10 GB/秒。 相反地，圖形配接器通常有專用的記憶體，會使用20到 100GB/s 或更多的圖形頻寬。 圖形硬體也有固定的函式單位，可執行複雜且昂貴的工作（例如紋理篩選、格式解壓縮或轉換），以非同步方式執行，但不會有額外負荷或耗電量。 在一般 CPU 上執行這些作業，對於耗電量和效能週期而言很昂貴。

Intel Penryn 3.0 g h z 四核心機器的典型效能數字顯示，在某些情況下，可能會在某些情況下優於低端整合 Direct3D 10 和更新版本的圖形 Gpu。 低端離散圖形硬體的速度通常比執行這些基準測試的變形更快4到5倍。 這些低終端的整合或獨立 Gpu 最少使用 CPU 資源。 在許多應用程式中，中間範圍或高端圖形卡的速度明顯比變形，特別是當應用程式可以利用這些圖形卡片提供的平行處理原則和記憶體頻寬時。

變形不是圖形硬體的替代方案，特別是在執行低端 Direct3D 10 和更新版本的離散硬體之後，這項功能也不是那麼合理。 變形的目標是要讓應用程式以 Direct3D 10 層級硬體為目標，而不會有明顯不同的程式碼路徑或測試需求，不論它們是在硬體或軟體中執行。

下列兩個表格顯示具有各種 Cpu 和圖形配接器的變形範例資料。

第一個表格顯示使用 Direct3D 10 Crysis 在800x600 上執行的變形範例資料，並在其最低層級上執行所有品質設定：

| CPU                         | Time   | 平均 FPS | 最小 FPS | 最小框架 | 最大 FPS | 最大框架 |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 核心 @ 3.0 GHz     | 271.57 | 7.36    | 3.46    | 1966      | 15.01   | 995       |
| Penryn 4 核心 @ 3.0 GHz      | 351.35 | 5.69    | 2.49    | 1967      | 10.95   | 980       |
| Penryn 2 核心 @ 3.0 GHz      | 573.98 | 3.48    | 1.35    | 1964      | 6.61    | 988       |
| 核心2雙核 @ 2.6 GHz         | 707.19 | 2.83    | 0.81    | 1959      | 5.18    | 982       |
| 核心2雙核 @ 2.4 GHz         | 763.25 | 2.62    | 0.76    | 1964      | 4.70    | 984       |
| 核心2雙核 @ 2.1 GHz         | 908.87 | 2.20    | 0.64    | 1965      | 3.72    | 986       |
| 具有強8核心 @ 2.0 GHz        | 424.04 | 4.72    | 1.84    | 1967      | 9.56    | 988       |
| AMD FX74 4 核心 @ 3.0 GHz    | 583.12 | 3.43    | 1.41    | 1967      | 5.78    | 986       |
| Phenom 9550 4 核心 @ 2.2 GHz | 664.69 | 3.01    | 0.53    | 1959      | 5.46    | 987       |

第二個表格顯示在各種圖形配接器上執行相同測試的範例資料：

| 顯卡         | Time   | 平均 FPS | 最小 FPS | 最小框架 | 最大 FPS | 最大框架 |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23.58  | 84.80   | 60.78   | 1957      | 130.83  | 1022      |
| NVIDIA 8500 GT        | 47.63  | 41.99   | 25.67   | 1986      | 72.57   | 991       |
| NVIDIA Quadro 290     | 67.16  | 29.78   | 18.19   | 1969      | 49.87   | 1017      |
| NVIDIA 8400 GS        | 59.01  | 33.89   | 21.22   | 1962      | 51.82   | 1021      |
| ATI 3400              | 53.79  | 37.18   | 22.97   | 618       | 59.77   | 1021      |
| ATI 3200              | 67.19  | 29.77   | 18.91   | 1963      | 45.74   | 980       |
| ATI 2400 PRO          | 67.04  | 29.83   | 17.97   | 606       | 45.91   | 987       |
| Intel DX10 整合 | 386.94 | 5.17    | 1.74    | 1974      | 16.22   | 995       |

## <a name="warp-conformance"></a>扭曲一致性

「變形」會將所有標準 Windows 硬體品質實驗室 (WHQL) 符合性測試，以驗證 Direct3D 硬體裝置。

已針對一組 Direct3D 10 和 Direct3D 10.1 應用程式和基準測試，以及針對 DirectX、NVIDIA 和 AMD 的 SDK 範例，測試了變形。

在測試期間，使用 Windows 的 [PIX](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) 偵錯工具和分析工具進行變形;Microsoft 有一個大型的應用程式框架庫，可用來在硬體和變形之間進行比較。 大部分的影像在硬體和變形之間看起來幾乎相同;有時可能會發生微小的差異，而是在 Direct3D 10 規格所定義的容限範圍內。