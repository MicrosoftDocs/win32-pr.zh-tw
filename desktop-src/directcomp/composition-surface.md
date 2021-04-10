---
title: 組合介面
description: 本主題說明 Microsoft DirectComposition 支援的表面類型類型。
ms.assetid: E19B4F0E-1CFA-4E93-BB6A-BFB701BC72CA
keywords:
- 組合介面
- DirectComposition 邏輯介面
- DirectComposition 虛擬介面
- 更新邏輯介面
- 邏輯介面，更新
- 修剪虛擬介面
- 虛擬介面，修剪
- 修剪虛擬介面
- 調整虛擬表面的大小
- 虛擬 surace，調整大小
- 調整虛擬表面的大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4bd30bfbd1de91444b7076184db597cd7a8c82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023653"
---
# <a name="composition-surface"></a>組合介面

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題說明 Microsoft DirectComposition 支援的表面類型類型。

-   [DirectComposition 邏輯介面](#directcomposition-logical-surface)
    -   [更新邏輯介面](#updating-a-logical-surface)
    -   [暫停邏輯介面的更新](#suspending-updates-to-a-logical-surface)
    -   [繼續更新邏輯介面](#resuming-updates-to-a-logical-surface)
    -   [結束對邏輯介面的更新](#suspending-updates-to-a-logical-surface)
    -   [使用邏輯介面的範例](#example-of-using-a-logical-surface)
-   [DirectComposition 虛擬介面](#directcomposition-virtual-surface)
    -   [調整虛擬表面的大小](#resizing-a-virtual-surface)
    -   [修剪虛擬介面](#trimming-a-virtual-surface)
-   [相關主題](#related-topics)

## <a name="directcomposition-logical-surface"></a>DirectComposition 邏輯介面

DirectComposition 會公開 [**IDCompositionSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) 物件來代表邏輯組合介面。 DirectComposition 會公開您可用來建立、更新及刪除這些邏輯介面的 Api。 每個介面都可以與一或多個視覺效果相關聯。 應用程式負責管理邏輯介面的存留期。

### <a name="updating-a-logical-surface"></a>更新邏輯介面

應用程式可以藉由呼叫 [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) ，並在應用程式想要更新的邏輯介面上指定矩形的大小和位移，來更新邏輯介面。 DirectComposition 會配置指定大小的矩形，然後傳回介面和應用程式需要繪製或更新的對應位移。 更新矩形的限制會依介面大小來系結。 例如，40 100 圖元介面的更新矩形最多可 (0、0、40100) 。 此外，可更新的區域會由 guard 矩形強制執行。 因為一次只能有一個防護矩形，所以一次只能更新一個邏輯介面。 如果未在先前呼叫 **BeginDraw** 之後呼叫 [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)或 [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) ， **BeginDraw** 會傳回錯誤碼。 應用程式可以將 **BeginDraw** 的認可呼叫新增至批次，但在呼叫和認可 **EndDraw** 之前不會生效。

### <a name="suspending-updates-to-a-logical-surface"></a>暫停邏輯介面的更新

需要更新不同表面的應用程式可以在目前的更新上呼叫 [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) ，然後呼叫 [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) 來開始新的更新。 Microsoft DirectComposition 允許多個更新，但是一次只能有一個作用中。 這表示您必須先在某個介面上呼叫 **SuspendDraw** 或 [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) ，然後再于下一個介面上呼叫 **BeginDraw** 。 不同于 **EndDraw**，認可的批次可以包含處於 **SuspendDraw** 狀態的介面，但在呼叫 **EndDraw** 之前，這類更新將不會顯示在畫面上。

### <a name="resuming-updates-to-a-logical-surface"></a>繼續更新邏輯介面

應用程式可以藉由呼叫 [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)來繼續更新處於 [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)狀態的介面。 只有在已暫停的介面上才能呼叫這個方法。

### <a name="ending-updates-to-a-logical-surface"></a>結束對邏輯介面的更新

呼叫 [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) 和 [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 是在螢幕上查看點陣圖更新變更的唯一方式。 對 **EndDraw** 的每個呼叫都必須有對應的 [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) 呼叫，才能移除防護矩形。 邏輯介面會保留所有更新，直到呼叫 **Commit** 為止。 您也可以在處於 [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)狀態的介面上呼叫 **EndDraw** ，因為 **EndDraw** 是隱含的 resume/end。 在您呼叫 **EndDraw** 之後，更新的內容會顯示在畫面上並予以捨棄，如此一來，就可以重複使用更新的記憶體來進行後續更新。

### <a name="example-of-using-a-logical-surface"></a>使用邏輯介面的範例

下列範例說明當應用程式建立由兩個視覺效果組成的視覺化樹狀結構，然後需要更新與視覺效果相關聯的兩個邏輯介面的特定區域時，應用程式會採取的步驟：

1.  建立 DirectComposition 裝置。
2.  建立由根節點和視覺效果1和2組成的視覺化樹狀結構。
3.  建立邏輯介面1和2。
4.  呼叫 [**SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) 以將邏輯介面與視覺效果1和2產生關聯。
5.  在邏輯介面1的子矩形上呼叫 [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) 。
6.  更新 DirectComposition 所傳回之位移上的介面。
7.  選擇性步驟：
    1.  在邏輯介面1上呼叫 [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) 。
    2.  在邏輯介面2的子矩形上呼叫 [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) 。
    3.  更新 DirectComposition 所傳回之位移上的介面。
    4.  在邏輯介面2上呼叫 [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) 。
    5.  在邏輯介面1上呼叫 [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) 。
8.  更新 DirectComposition 所傳回之位移上的介面。
9.  在邏輯介面1上呼叫 [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) 。
10. 呼叫 [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)。

## <a name="directcomposition-virtual-surface"></a>DirectComposition 虛擬介面

DirectComposition 會公開 [**IDCompositionVirtualSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvirtualsurface) 介面，以代表一個虛擬介面，也就是邏輯介面的集合 (圖格) 排列在固定的方格中，並具有固定大小的磚。 應用程式會在建立時指定虛擬材質的大小。 大小會建立虛擬介面的界限。 介面可以與一或多個視覺效果相關聯。

當虛擬介面初始化時，不會受到實際配置的支援。 換句話說，它並不會保留任何位。 DirectComposition 會配置磚 (也就是，在應用程式開始更新介面之後) 組合表面物件。 應用程式會藉由呼叫 [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) ，並指定與虛擬介面座標相關的區域，來更新虛擬介面。 然後，DirectComposition 會配置必要的磚來保存更新，並傳回復合介面和 offset 以進行更新。

如同邏輯介面，您可以在虛擬介面上呼叫 [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)、 [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)、 [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) 和 [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) 。 此外，DirectComposition 會公開可用來調整大小和修剪現有虛擬介面的方法。

### <a name="resizing-a-virtual-surface"></a>調整虛擬表面的大小

重 [**設大小**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-resize) 方法會變更虛擬介面的界限，這表示任何新的更新或配置都必須落在新大小所設定的界限內。 應用程式會使用重 **設大小** 來告訴 DirectComposition，虛擬介面的特定區域不再需要，而且可以回收。 如果重 **設大小** 會縮小虛擬介面，應用程式就無法再更新新界限以外的區域。

下圖顯示 3 x 3 的虛擬介面，調整大小為2。 紅色區域代表在調整大小作業中捨棄的圖格，而 DirectComposition 會回收記憶體。 在調整大小之後，應用程式無法在不重新調整虛擬介面大小的情況下，對紅色區域進行更新。

![調整虛擬表面的大小 ](images/resize-virtual-surface.png)

調整大小作業會立即生效。 DirectComposition 不會等待應用程式呼叫 [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 以進行調整大小的更新。 例如，假設應用程式會進行下列呼叫順序。


```
pVirtualSurface->Resize(0, 0);
pVirtualSurface->Resize(INT_MAX, INT_MAX);
pDevice->Commit();
```



在此範例中，應用程式會失去第一次調整大小的所有內容。 第二個調整大小沒有任何作用，即使在 [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)之前呼叫它也一樣。 在此情況下，螢幕上不會顯示任何內容。

### <a name="trimming-a-virtual-surface"></a>修剪虛擬介面

[**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim)方法會識別應用程式所需的虛擬介面區域。 它不會調整虛擬介面界限的大小，但會告訴 DirectComposition 目前需要配置哪些邏輯表面。

在下圖中，綠色方形是應用程式的視口。 應用程式一開始會轉譯為虛擬介面 (藍色) 的前六個磚， (位於此圖格的淺灰色) 。 當虛擬介面所表示的頁面滾動時，應用程式需要轉譯最後六個磚。 應用程式會呼叫 [**Trim**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvirtualsurface-trim) 來指出最後六個磚所定義的區域是內容所在的位置，而其餘的時間則不需要。 DirectComposition 接著可以選擇回收最初表示前六個磚的邏輯表面 (暗灰色) 。

![修剪虛擬介面](images/trim-virtual-surface.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectComposition 概念](directcomposition-concepts.md)
</dt> </dl>

 

 