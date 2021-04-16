---
title: Windows 中的圖形 Api
description: 本文討論 Windows 圖形功能和 Api。
ms.assetid: 54cd5027-cdcf-fc4a-40a9-beacfaa08681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7543ee7c5e3cdbfb022cc9299dd5ddd3cdd36981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382565"
---
# <a name="graphics-apis-in-windows"></a>Windows 中的圖形 Api

Windows Vista 支援全新的顯示器驅動程式模型，此模型在引進 Windows Driver Model (適用于 Windows 98 的 WDM) 之後，可代表視頻驅動程式設計的主要修訂。 這個經過重新設計的模型反映2D 光柵作業和 GDI 應用程式世界的影片硬體演進，以及具有固定函式圖形硬體的3D 遊戲，最後到可支援多種高效能圖形應用程式的新式可程式化圖形處理單元 (GPU) 。 Windows 7 和 Windows 8 在 Windows Vista 圖形基礎結構上提供其他圖形功能和 Api 來建立。 本文討論 Windows 圖形功能和 Api。

-   [背景](#background)
-   [Direct3D 9](#direct3d-9)
-   [Direct3D 9Ex](#direct3d-9ex)
-   [Direct3D 10](#direct3d-10)
-   [Direct3D 10。1](#direct3d-101)
-   [Direct3D 11](#direct3d-11)
-   [Direct3D 11。1](#direct3d-111)
-   [Opengl](#opengl)
-   [應用程式相容性、GDI 及舊版的 Direct3D](#application-compatibility-gdi-and-older-versions-of-direct3d)
-   [建議](#recommendations)

## <a name="background"></a>背景

從 Windows 的早期日子起，程式設計圖形的主要 API 是圖形裝置介面 (GDI) 。 此 API 設計用來處理許多2D 輸出裝置，並形成 Windows 使用者介面體驗的基礎。 DirectDraw 和 Direct3D 是以替代 Api 的形式導入，可支援全螢幕遊戲和3D 轉譯為現有硬體的延伸模組。 與 GDI 的互動相當複雜。 使用 Direct3D 元素之傳統 GDI 元素的有效混合已受到此設計的限制。 Windows XP 版本的 WDM （稱為 XPDM）會反映 GDI 和 Direct3D 的並存本質 (請參閱 [圖 1]) 。

**圖1。Windows XP 中的圖形 Api**

![xpdm](images/graphics-apis-in-windows-xp.gif)

多年來，3D 視訊卡的威力大幅增加了這項功能專用的大部分硬體。 新的驅動程式模型、Windows 顯示驅動程式模型 (WDDM) 、將 GPU 和 Direct3D 帶到 forefront，讓您能夠建立全新的3D 桌面體驗，以完美地將 GDI 的2D 世界與新式可程式化 Gpu 的強大混合。 使用 WDDM，影片硬體會完全由 Direct3D 驅動，而所有其他圖形介面會透過以 Direct3D 為中心的新驅動程式模型與視頻硬體通訊 (請參閱 [圖 2]) 。

**[圖 2]Windows Vista 中的圖形 Api**

![wddm](images/graphics-apis-in-windows-vista.gif)

如需有關 WDDM 的詳細資訊，請參閱 MSDN 上的 [Windows Vista 顯示驅動程式模型 (WDDM) 設計指南](/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide) 。

## <a name="direct3d-9"></a>Direct3D 9

第9版的 DirectX 首次發行于2002的 Windows 中，後續更新為2003和2004。 此 API 代表多年來的 DirectX 技術演進，為 Direct3D 引進功能更強大的著色器程式設計模型，以及由數以千計的出貨標題所支援的成熟度。 Direct3D 9 是 Windows Vista 上的主要圖形介面。 它仍然是理想的 API，可用來撰寫需要在各種現有硬體和 Windows 版本上執行的3D 遊戲和應用程式。 使用 Direct3D 9 介面的應用程式不會隱藏新驅動程式模型的詳細資料，但在幕後，作業系統會充分利用新功能，以提供真正多工的 GPU、更有效率的資源管理和健全的效能。

為了確保與舊版 Windows 的完全相容，舊有的驅動程式模型必須使用新的 Windows Vista 顯示驅動程式模型來模擬。 例如，當全螢幕應用程式失去焦點時，它必須假設它已遺失視訊記憶體中的所有資源 (VRAM) 並重載建立為非受控資源的資源，即使新的驅動程式模型會以透明的方式處理資源，而不會從裝置內容中收回這些資源也是一樣。 即使是受管理的和預設資源類型的概念，也是舊的驅動程式模型所特有。 另一個範例是在配置非受控 (預設集區) 資源超過可用 VRAM 數量時的預期失敗，即使新的驅動程式模型可提供幾乎無限的虛擬視訊記憶體數量也是一樣。 基於這些需求，在 Windows Vista 上執行的 Direct3D 應用程式仍會收到這些錯誤狀況。 因此，他們在使用基本 Direct3D 9 介面完全使用新驅動程式模型的某些功能時，將會受到限制。

雖然 Windows Vista 的新系統隨附的視訊卡將包含 WDDM 驅動程式，而新的驅動程式有許多常用的視訊卡，但 Windows Vista 仍繼續支援使用較舊的 XPDM 驅動程式進行升級和公司版本的能力。 在使用舊驅動程式模型的系統上，您必須使用 Direct3D 9 和舊版介面，而圖形系統的操作與 Windows XP (圖 1) 的作業非常類似。 需要 WDDM 才能讓應用程式使用 Direct3D 9Ex、Direct3D 10 和更新版本。

## <a name="direct3d-9ex"></a>Direct3D 9Ex

Direct3D 9Ex 介面可讓您存取標準 Direct3D 9 API 的一些延伸模組，以公開虛擬資源配置、新的遺失裝置語義，以及一些在 Windows Vista 上執行時可用的其他新功能。 藉由建立此擴充物件，Direct3D 9 API 會使用新的語義，因此需要應用程式使用不同的邏輯 (因此，您可以) 不同的程式碼路徑，以針對新的條件類型建立、管理和錯誤處理。 此 API 僅適用于 Windows Vista，且需要 WDDM 驅動程式。 由於 Direct3D 9Ex 使用的 API 和驅動程式程式碼路徑與 Direct3D 9 不同，因此支援此 API 需要您應用程式的額外測試案例。

建立新 Direct3D 9Ex API 的主要原因，是為了讓您能夠完整存取 WDDM 的新功能，同時維持對現有 Direct3D 應用程式的相容性。 新的3D 桌面以及許多 Windows Vista 特定的應用程式會使用這個版本的 Direct3D 9，但是在舊版的 XPDM 驅動程式上執行時，這些應用程式無法運作。 由於 Direct3D 9Ex API 將永遠不會出現在舊版的 Windows 上，因為不支援 WDDM，所以標準 Direct3D 9 介面涵蓋了更廣大的系統組合。 針對可利用下一代影片硬體的高效能應用程式，最新版本10的 Direct3D 提供許多不是由 Direct3D 9Ex 所公開的新功能。 因此，針對遊戲和大部分其他應用程式，Direct3D 9 或 Direct3D 10 是建議使用的 API。

> [!Note]  
> DirectX SDK 不提供適用于 Direct3D 9Ex 介面的範例、標頭或程式庫。 MSDN Library 和 Windows SDK (先前稱為 Platform SDK) 包含可用的檔、標頭和程式庫。

 

如需 Direct3D 9Ex 的詳細資訊，請參閱 MDSN 上 [的適用于 Windows Vista 的 DirectX](/previous-versions//ms681824(v=vs.85)) 。

## <a name="direct3d-10"></a>Direct3D 10

為了充分瞭解新的 Windows Vista 驅動程式模型和新一代硬體的潛力，已建立全新版本的 Direct3D API。 雖然 WDDM 消除了對現有圖形系統效能的一些限制，但是 Direct3D 10 更進一步地探討現有 Direct3D API 中的設計瓶頸，並大幅簡化 GPU 程式設計工作。

新的 API 完全消除了一些固定函式的層面，並以可程式化的結構來取代，並大幅簡化內部實作為。 舊版 Direct3D 中數百項功能位已完全消除並取代為一組定義完善的功能，而這些功能對特定的資源格式只有一些選擇性的使用案例。 需要大量 CPU 的資源建立和驗證現在在新的 API 中具有明確的語法。 這可讓您更容易預測效能行為，並大幅減少個別繪製的額外負荷。 您可以將資源重新設定為多個表單，以在各種階段有效率地使用，而此功能集會在格式的使用案例上施加較少的限制。 另外還有新的區塊壓縮的一般地圖材質格式。

在新的 API 中，著色器常數和裝置狀態是明確的資源，可讓您更有效率地在硬體上進行快取，並大幅簡化驅動程式驗證。 可程式化著色器模型已跨頂點和圖元著色器進行整合，並使用定義完善的計算模型和運算子來更具表達性。 此外，已新增幾何著色器階段，以在頂點著色器階段之後對基本專案運作。 在管線的頂點和幾何著色器階段中，GPU 工作的結果可以串流處理至影片 RAM 以供重複使用，以提供極複雜的多階段 GPU 作業，並使 CPU 的互動降到最短。

所有這些增強功能都能提供下一代的圖形技術，並擴充應用程式將工作離線載入至 GPU 的能力。 卸載可讓您以 GPU 為基礎的更複雜的字元外觀、加速變形技術、陰影磁片區產生和延伸、物件和物理系統，這些都是以 GPU 為基礎、更複雜的資料，結合成有效率的大型繪圖批次、程式詳細資料、即時的光線追蹤置換對應、單一傳遞 cube 對應產生，以及許多其他技術—全都可釋出 CPU

為了在 Direct3D 10 中提供此層級的創新，較舊的硬體無法表示為新介面的部分實作為。 視訊卡可以支援所有的新功能，或它不是支援 Direct3D 10 功能的卡片。 因此，雖然 Direct3D 9 可以驅動具有許多缺少功能位和使用限制的 DirectX7 紀元硬體，但是 Direct3D 10 只適用于新一代的視訊卡。 若要讓應用程式支援較舊的影片硬體，它也必須支援 Direct3D 9 介面。 未來的 Direct3D 版本將會建立在第10版上，將它擴充至新版的 API，同時確保 Direct3D 10 功能的嚴格超集合。

如需 Direct3D 10 的詳細資訊，請參閱 [direct3d 10](/windows/desktop/direct3d10/d3d10-graphics)。

## <a name="direct3d-101"></a>Direct3D 10。1

Windows Vista Service Pack 1 擴充了 Direct3D 10 API 與 Direct3D 10.1，這會新增選用介面和額外的著色器模型，以支援支援 Direct3D 10.1 的視訊卡的新硬體功能。 所有能夠支援 Direct3D 10.1 的硬體也都能完全支援 Direct3D 10 的所有功能，而遊戲開發人員可以利用 Direct3D 10.1 的其他功能（如果有的話）。

> [!Note]  
> Direct3D 10.1 是 Windows 7 desktop 所使用的圖形 API。

 

> [!Note]  
> Windows 7 和 Windows Vista update ([KB 971644](https://support.microsoft.com/kb/971644)) 將 DXGI 1.1、10level9 功能等級和 WARP10 裝置的支援新增至現有的 DIRECT3D 10.1 API。

 

## <a name="direct3d-11"></a>Direct3D 11

Windows 7 支援以 Direct3D 10.1 API 設計為基礎的新版本 Direct3D （Direct3D 11）。 API 的新功能包括多執行緒轉譯和資源建立、計算著色器、10level9 功能等級和 WARP10 軟體轉譯裝置的支援，以及新的 Direct3D 11 類別硬體功能，例如使用輪廓 & 網域著色器、BC6H 和 BC7 材質壓縮格式、著色器模型5.0，以及動態著色器連結。 新的 API 可以使用現有的 Direct3D 10 和10.1 類別的視訊卡、某些 Direct3D 9 卡透過10level9 功能等級（具有有限的功能支援），以及最新一代的 Direct3D 11 類別視訊卡。

除了 Direct3D 11 API，Windows 7 還包含 DXGI 1.1、Direct2D、DirectWrite 和 WDDM 1.1 驅動程式的支援。

> [!Note]  
> Direct3D 11 和相關 Api 也可作為 Windows Vista 的更新 (請參閱 [KB 971644](https://support.microsoft.com/kb/971644)) 。

 

## <a name="direct3d-111"></a>Direct3D 11。1

Windows 8 使用 Direct3D 11.1 擴充 [direct3d 11 API](#direct3d-11) 。 Direct3D 11.1 支援 [功能等級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 為11、10 \_ x 和 9 x 支援的所有現有硬體 \_ ，以及新的11個 \_ 功能等級。

除了 [Direct3D 11.1 API](/windows/desktop/direct3d11/direct3d-11-1-features)之外，Windows 8 還包含 [DXGI 1.2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)、 [DIRECT2D 裝置](/windows/desktop/Direct2D/devices-and-device-contexts)內容，以及 WDDM 1.2 驅動程式的支援。

> [!Note]  
> 如果您想要讓 Windows Store 應用程式使用 DirectX 來設計3D 圖形程式，您可以使用 Direct3D 11.1 API。 如需使用 DirectX 進行3D 圖形程式設計的詳細資訊，請參閱 [使用 directx 的3d 圖形簡介](/previous-versions/windows/apps/hh465137(v=win.10))。

 

**適用于 Windows 7 的平臺更新：** Windows 7 或 Windows Server 2008 R2 上的 [Direct3D 11.1 API](/windows/desktop/direct3d11/direct3d-11-1-features) 已安裝適用于 [Windows 7 的 Platform Update](https://support.microsoft.com/kb/2670838) 的部分支援。 如需 Windows 7 平臺更新的詳細資訊，請參閱 [windows 7 的平臺更新](platform-update-for-windows-7.md)。

## <a name="opengl"></a>Opengl

Windows Vista、Windows 7 和 Windows 8 提供與 Windows XP for OpenGL 相同的支援，可讓視訊卡製造商為 OpenGL 提供可安裝的用戶端驅動程式 (ICD) 提供硬體加速支援。 請注意，這類 ICDs 的較新版本需要完整支援 Windows Vista、Windows 7 或 Windows 8。 如果未安裝任何 ICD，系統會在大部分情況下切換回 OpenGL v1.1 軟體層。

## <a name="application-compatibility-gdi-and-older-versions-of-direct3d"></a>應用程式相容性、GDI 及舊版的 Direct3D

Windows Vista、Windows 7 和 Windows 8 圖形系統都是設計來支援各種不同的硬體和使用案例，以啟用新的技術，同時繼續支援現有的系統。 現有的圖形介面（例如 GDI、GDI + 和舊版的 Direct3D）仍會繼續在 Windows Vista 和 Windows 7 上運作，但可能的話，會在內部重新對應。 這表示大部分現有的 Windows 應用程式將會繼續運作。

Windows Vista、Windows 7 和 Windows 8 繼續支援與 Windows XP 相同的 Direct3D 和 DirectDraw 介面，再改回 DirectX (的第3版，但 Direct3D's 保留模式除外，但已移除) 。 就像 Windows XP Professional x64 Edition 一樣，在較新版本的 Windows 上的64位原生應用程式僅限於 Direct3D9、DirectDraw7 或較新的介面。 高效能應用程式應該使用 Direct3D 9 或更新版本，以確保它們具有最接近硬體功能的相符項。

## <a name="recommendations"></a>建議

為圖形化應用程式選取 API 時，請考慮下列建議：

-   如果您的應用程式必須支援 Windows XP 或較早的 Windows 版本，請使用 Direct3D 9。
-   如果您想要支援使用 XPDM 驅動程式執行的 Windows Vista 或 Windows 7，請使用 Direct3D 9。 如果是 Windows Vista 或 Windows 7 系統，但缺少 Direct3D 10 或更佳的影片硬體，您可以選擇使用現有的 Windows XP Direct3D 9 程式碼路徑，或透過 Direct3D 10.1 或 Direct3D 11 API 使用10level9 功能等級。
-   使用 Direct3D 11 來充分利用 Windows Vista、Windows 7 和 Windows 8 下一代的影片硬體。 Windows Store 應用程式必須使用 Direct3D 11 或更新版本。

 

 