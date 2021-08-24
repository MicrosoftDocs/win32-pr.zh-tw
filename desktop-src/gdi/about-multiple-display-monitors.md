---
description: 當多個監視器是桌面的一部分時，物件可以在監視器之間順暢地移動。
ms.assetid: eb7576c6-322c-48d0-abbb-bdc3b34976c3
title: 關於多顯示器監視器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c28c8ccbd9abbcbcee696bb927c5aa484df7b23d6aba811ff95145d447109b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400508"
---
# <a name="about-multiple-display-monitors"></a>關於多顯示器監視器

當多個監視器是桌面的一部分時，物件可以在監視器之間順暢地移動。 也就是說，您可以將視窗或快捷方式從某個監視器拖曳到另一個監視器，而您可以調整視窗的大小以涵蓋多個監視器。 此外，如果某個監視器安裝在另一個監視器之上，則離開上方監視器底部的游標會顯示在下方監視器的上方。

一般情況下，使用者會在系統中排列監視器，以反映實體顯示單位的相片順序;例如，並存或最上層的一或多個位置。 使用者會使用 [監視] 索引標籤來執行此工作，這會透過主控台取代 [**顯示內容**] 對話方塊中的 [**設定**] 索引標籤。 這些監視器必須形成一個連續的區域，也就是每個監視器至少會在一個邊緣的一部分上觸及另一個監視器。

移動或調整視窗大小時，標題的部分一定會顯示出來，讓使用者可以使用滑鼠移動視窗並調整其大小。 游標移動受限於監視器區域，因此一律為可見。 Shell 圖示位於與工作列相同的監視器上，而工作列可以位於任何監視器上，請參閱 [舊版程式的多個監視器考慮](multiple-monitor-considerations-for-older-programs.md)。

多個監視器系統會影響特定的按鍵組合。 ALT + PRINTSCRN 按鍵組合會取得前景視窗的快照集，如同往常一樣。 但是，PRINTSCRN 鍵會取得具有滑鼠的監視器快照。 CTRL + PRINTSCRN 按鍵組合會取得整個虛擬畫面的快照集，請參閱 [虛擬螢幕](the-virtual-screen.md)。

對多個監視器的支援在單一顯示環境中執行時，不會影響應用程式的效能。 也就是說，在單一顯示器系統上執行時，高效能圖形作業程式碼中不會有額外的負荷。 不過，在多個監視器系統中，如果應用程式只在其中一個圖形裝置上執行，效能會稍微受到影響。 此外，如果應用程式跨越多個顯示器，效能可能會受到大幅影響，特別是針對需要大量圖形的作業。

*全螢幕* 是作業系統所提供的一項功能，可讓使用者將應用程式切換成特殊狀態，讓應用程式可以直接存取 VGA 圖形硬體。 對於需要高效能的遊戲和其他以圖形為主的應用程式，這是一項重要的功能。 此外，開發人員通常會使用它來進行文字編輯，因為它可讓文字滾動更快速。

在多重監視器環境中，只有一個圖形裝置可與 VGA 相容。 這是電腦硬體的限制，需要只有一部裝置回應任何硬體位址。 因為 VGA 硬體相容性標準需要特定的硬體位址，電腦中只能有一個 VGA 圖形裝置，而且只有此裝置可以實際回應 VGA 位址。 因此，需要全螢幕的應用程式只會在支援 VGA 硬體相容性的特定裝置上執行。

本總覽提供下列主題的相關資訊。

-   [虛擬畫面](the-virtual-screen.md)
-   [HMONITOR 和裝置內容](hmonitor-and-the-device-context.md)
-   [列舉和顯示控制項](enumeration-and-display-control.md)
-   [多個監視系統計量](multiple-monitor-system-metrics.md)
-   [使用多個監視器作為獨立顯示器](using-multiple-monitors-as-independent-displays.md)
-   [多顯示器顯示器上的色彩](colors-on-multiple-display-monitors.md)
-   [將物件放置在多個顯示監視器上](positioning-objects-on-multiple-display-monitors.md)
-   [不同系統上的多個監視器應用程式](multiple-monitor-applications-on-different-systems.md)
-   [舊版程式的多個監視器考慮](multiple-monitor-considerations-for-older-programs.md)

 

 



