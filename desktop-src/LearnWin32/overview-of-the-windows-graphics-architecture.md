---
title: Windows 圖形架構總覽
description: 描述 Windows 中的 c + +/COM 圖形 Api。
ms.assetid: 9654b18b-d615-455d-a92a-6fc2ccda469e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45ba44f54b947d923b888d51080ff0335119a1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "104116013"
---
# <a name="overview-of-the-windows-graphics-architecture"></a>Windows 圖形架構總覽

Windows 為圖形提供數個 c + +/COM Api。 這些 Api 如下圖所示。

![顯示 windows 圖形 api 的圖表。](images/graphics01.png)

-   圖形裝置介面 (GDI) 是適用于 Windows 的原始圖形介面。 GDI 是先針對16位 Windows 撰寫，然後針對32位和64位 Windows 進行更新。
-   GDI + 是在 Windows XP 中引進，做為 GDI 的後繼。 您可以透過一組包裝一般 C 函式的 c + + 類別來存取 GDI + 程式庫。 .NET Framework 也會在 **System. 繪圖** 命名空間中提供 managed 版本的 gdi +。
-   Direct3D 支援立體圖形。
-   Direct2D 是適用于2D 圖形的新式 API，這是 GDI 和 GDI + 的後繼。
-   DirectWrite 是文字版面配置和點陣化引擎。 您可以使用 GDI 或 Direct2D 來繪製柵格化文字。
-   DirectX Graphic Infrastructure (DXGI) 會執行低層級的工作，例如呈現輸出的畫面格。 大部分的應用程式不會直接使用 DXGI。 而是做為圖形驅動程式與 Direct3D 之間的中繼層。

Direct2D 和 DirectWrite 是在 Windows 7 中引進的。 您也可以透過平臺更新，在 Windows Vista 和 Windows Server 2008 上使用這些功能。 如需詳細資訊，請參閱 [Windows Vista 的平臺更新](../win7ip/platform-update-for-windows-vista-portal.md)。

Direct2D 是此課程模組的焦點。 雖然 GDI 和 GDI + 都能在 Windows 中繼續受到支援，但建議針對新程式使用 Direct2D 和 DirectWrite。 在某些情況下，混合的技術可能更實用。 在這些情況下，Direct2D 和 DirectWrite 是設計來與 GDI 交互操作。

下一節將說明 Direct2D 的一些優點。

### <a name="hardware-acceleration"></a>硬體加速

*硬體加速* 的一詞是指圖形處理器 (GPU) （而非 CPU）所執行的圖形計算。 新式 Gpu 已針對轉譯圖形中所使用的計算類型進行高度優化。 一般來說，從 CPU 移至 GPU 的工作越多越好。

雖然 GDI 支援某些作業的硬體加速，但許多 GDI 作業都會系結至 CPU。 Direct2D 會分層置於 Direct3D 之上，並充分利用 GPU 提供的硬體加速。 如果 GPU 不支援 Direct2D 所需的功能，則 Direct2D 會切換回軟體轉譯。 整體來說，Direct2D 在大部分情況下都優於 GDI 和 GDI +。

### <a name="transparency-and-anti-aliasing"></a>透明度和消除鋸齒

Direct2D 支援完整硬體加速的 Alpha 混合 (透明度) 。

GDI 對 Alpha 混色的支援有限。 大部分 GDI 函數不支援 Alpha 混色，雖然 GDI 支援在 bitblt 作業期間進行 Alpha 混色。 GDI + 支援透明度，但 Alpha 混合是由 CPU 所執行，因此不會受益于硬體加速。

硬體加速 Alpha-混合也啟用了消除鋸齒功能。 *別名* 是藉由取樣連續函式所造成的成品。 例如，當曲線轉換成圖元時，別名可能會造成不規則的外觀。 \[3 \] 任何可減少別名所造成之成品的技巧，都會被視為一種消除鋸齒的形式。 在圖形中，消除鋸齒是藉由使用背景來混合邊緣來完成。 例如，以下是由 GDI 繪製的圓形，以及 Direct2D 所繪製的相同圓形。

![direct2d 中消除鋸齒技術的圖例。](images/graphics02.png)

下圖顯示每個圓形的詳細資料。

![上一個影像的詳細資料。](images/graphics03.png)

GDI (左) 所繪製的圓形是由黑色圖元所組成，大約是曲線。 Direct2D 繪製的圓形 (right) 使用混色來建立更平滑的曲線。

當 GDI) 繪製幾何 (線條和曲線時，不支援消除鋸齒。 GDI 可以使用 ClearType 來繪製消除鋸齒的文字;除此之外，GDI 文字也是別名。 文字的別名特別明顯，因為不規則線條會中斷字型設計，讓文字更容易閱讀。 雖然 GDI + 支援消除鋸齒，但是它會由 CPU 套用，因此效能不如 Direct2D。

### <a name="vector-graphics"></a>向量圖形

Direct2D 支援 *向量圖形*。 在向量圖形中，數學公式是用來表示線條和曲線。 這些公式與螢幕解析度無關，因此可以調整成任意的維度。 當影像必須調整以支援不同的監視器大小或螢幕解析度時，向量圖形特別有用。

## <a name="next"></a>下一個

[桌面視窗管理員](the-desktop-window-manager.md)

 

 
