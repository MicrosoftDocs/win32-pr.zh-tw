---
description: VMR 與
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: VMR 與上一個 DirectShow 轉譯器的比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9401361c5b258fdff09bf25351a79bf8315dabfb0c82636d7d8c3c9ffcdd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903268"
---
# <a name="vmr-vs-previous-directshow-renderers"></a>VMR 與上一個 DirectShow 轉譯器的比較

使用舊的篩選器時，圖形中會需要不同的轉譯器，視硬體設定而定。

[影片](video-renderer-filter.md)轉譯器篩選器用來轉譯非影片埠案例中的單一影片串流。 它是以圖形硬體技術為基礎，這項技術目前已超過五年，而在較舊版本的 DirectDraw 上。 在某些情況下，它會使用 GDI 來呈現。 這樣做的目的是為了節省影片資源，這些資源在五年前都有更多限制，或在 DirectDraw 中克服與多重監視器支援相關的限制。 VMR-7 或 VMR-9 都不會使用 GDI 來呈現;VMR-7 完全以 DirectDraw 7 為基礎，而 VMR-9 是以 Direct3D 9 為基礎。

在 VMR 覆迭之前的影片埠或多個影片輸入串流的案例中，會使用[Mixer](overlay-mixer-filter.md)濾波器進行轉譯。 此篩選器只會使用圖形配接器上的硬體重迭，因此通常會限制為大部分卡片所提供的一個重迭表面。 覆迭 Mixer 會執行目的地色彩金鑰，但無法進行 Alpha 混色。 因為它沒有視窗管理員，所以它必須使用第二個篩選器，也就是影片轉譯器，用於視窗管理。 VMR 具有真正的 Alpha 混色，而且除了硬體重迭之外，還可以在軟體中建立多個重迭。

在影片埠案例中，應用程式會在影片上覆迭隱藏式輔助字幕或其他 VBI 資料，需要額外的篩選器（ [VBI Surface](vbi-surface-allocator.md)配置器），才能為 VBI 文字配置額外的視訊記憶體。 針對 Isv，VMR 7 會將配置和轉譯功能合併成用於所有案例的單一篩選，以簡化應用程式開發。 有了 VMR，就不再需要 VBI Surface 配置器。 此篩選器會在 Windows XP 中取代為新的[影片埠管理員](video-port-manager.md)篩選器，它會執行所有先前由重迭 Mixer 執行的影片埠工作。

> [!Note]  
> VMR-9 不支援視訊連接埠。

 

VMR 比舊版轉譯器更健全，部分是因為如果您使用的是 VMR-9) 介面，則只會使用 DirectDraw 7 (或 Direct3D 9，而不是舊的轉譯器，其使用舊版和新版 DirectDraw 的混合介面。 VMR 也採用新的映射呈現機制，其設計目的是要支援 Direct3D、更高的 VRAM 和影片記憶體頻寬，以及硬體加速功能。 有了 VMR，重點在於處理前端，並減少對影片埠和覆迭的相依性。 但即使是所有的新功能，VMR 的設計是為了與現有應用程式的最大相容性。

VMR 也是可擴充的。 應用程式可以提供自己的子元件來執行自訂的影片效果，以及/或掌控配置和轉譯流程。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於影片混合轉譯](about-the-video-mixing-render.md)
</dt> </dl>

 

 



