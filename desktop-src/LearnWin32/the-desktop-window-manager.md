---
title: 桌面視窗管理員
description: .
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73167b762a9952eb508f09e70f3d4183b3b7a018
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300775"
---
# <a name="the-desktop-window-manager"></a>桌面視窗管理員

在 Windows Vista 之前，Windows 程式會直接在螢幕上繪製。 換句話說，程式會直接寫入視訊卡所顯示的記憶體緩衝區。 如果視窗沒有正確地重新繪製，則這種方法可能會造成視覺構件。 比方說，如果使用者將一個視窗拖曳到另一個視窗，而且下一個視窗無法迅速重新繪製，最上層的視窗就會留下一個線索：

![顯示重新繪製構件的螢幕擷取畫面。](images/graphics04.png)

原因是這兩個 windows 繪製至相同的記憶體區域。 拖曳最上方的視窗時，必須重新繪製其下的視窗。 如果重新繪製的速度太慢，則會導致上圖所示的構件。

Windows Vista 藉由引進桌面視窗管理員 (DWM) 來徹底改變 windows 的繪製方式。 當 DWM 啟用時，視窗不會再直接繪製到顯示緩衝區。 相反地，每個視窗會繪製到螢幕上的記憶體緩衝區，也稱為 *螢幕外介面*。 DWM 接著會將這些介面合成至螢幕。

![顯示 dwm 如何將桌面合成的圖表。](images/graphics05.png)

DWM 提供許多優於舊版圖形架構的優點。

-   減少重新繪製訊息。 當視窗被另一個視窗阻擋時，受阻礙的視窗就不需要重新繪製。
-   專案減少。 先前，拖曳視窗可以建立視覺構件，如所述。
-   視覺效果。 因為 DWM 負責撰寫螢幕，所以它可以轉譯半透明和模糊的視窗區域。
-   高 DPI 的自動調整。 雖然調整不是處理高 DPI 的理想方式，但這是較舊的應用程式（不是針對高 DPI 設定所設計）的可行回復。  (我們稍後會在 [DPI 和 Device-Independent 圖元](dpi-and-device-independent-pixels.md)一節中返回此主題。 ) 
-   替代的視圖。 DWM 可以用各種有趣的方式來使用螢幕外表面。 例如，DWM 是 Windows Flip 3D、縮圖和動畫轉換背後的技術。

不過請注意，不保證會啟用 DWM。 圖形配接器可能不支援 DWM 系統需求，使用者可以透過 [ **系統屬性** ] 控制台停用 dwm。 這表示您的程式不應依賴 DWM 的重新繪製行為。 使用已停用的 DWM 測試您的程式，以確定它會正確地重新繪製。

## <a name="next"></a>下一個

[保留模式與立即模式](retained-mode-versus-immediate-mode.md)

 

 




