---
title: 比較 Direct2D 和 GDI 硬體加速
description: Direct2D 和 GDI 都是立即模式2D 轉譯 Api，兩者都提供某種程度的硬體加速。
ms.assetid: 0028a0c3-445d-46b7-b55b-46dff3bce9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f05dce8719f4d07d3160c65b88570391c3eb736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315259"
---
# <a name="comparing-direct2d-and-gdi-hardware-acceleration"></a>比較 Direct2D 和 GDI 硬體加速

[Direct2D](./direct2d-portal.md) 和 [GDI](/windows/desktop/gdi/windows-gdi) 都是立即模式2d 轉譯 api，兩者都提供某種程度的硬體加速。 本主題探討 Direct2D 與 GDI 之間的差異，包括過去和目前這兩個 Api 的硬體加速功能差異。

本主題包含下列部分：

-   [Direct2D 和 GDI 之間的差異](#differences-between-direct2d-and-gdi)
-   [GDI 和 Direct2D 硬體加速](#gdi-and-direct2d-hardware-acceleration)
    -   [增加顯示驅動程式的複雜度和大小](#increasing-complexity-and-size-of-display-drivers)
    -   [同步處理會話和全球核心位址空間時遇到困難](#difficulty-in-synchronizing-session-and-global-kernel-address-spaces)
    -   [複合視窗管理](#composited-window-management)
-   [Windows 7 中的 GDI 轉譯](#gdi-rendering-in-windows-7)
-   [Windows 7 中的對比 Direct2D 和 GDI 加速](#contrasting-direct2d-and-gdi-acceleration-in-windows-7)
    -   [資源的位置](#location-of-resources)
    -   [轉譯方法](#rendering-method)
    -   [延展性](#scalability)
    -   [位置](#location-of-resources)
    -   [硬體加速的可用性](#availability-of-hardware-acceleration)
    -   [展示模型](#presentation-model)
-   [結論](#conclusion)

## <a name="differences-between-direct2d-and-gdi"></a>Direct2D 和 GDI 之間的差異

[GDI](/windows/desktop/gdi/windows-gdi) 會轉譯不透明的別名幾何，例如多邊形、橢圓形和線條。 它會轉譯別名和 ClearType 文字，並且可支援透過 AlphaBlend API 的透明混色。 不過，其透明度的處理不一致，大部分的 GDI Api 只會忽略 Alpha 色板。 少數 GDI Api 可保證 Alpha 通道在作業之後會包含哪些內容。 更重要的是，GDI 的轉譯不會輕易地對應至3D 作業，而且新式 GPU 最有效率地呈現在其轉譯引擎的3D 部分。 例如， [Direct2D](./direct2d-portal.md)的鋸齒線條是設計來實作為在 GPU 上轉譯的兩個三角形，而 GDI 則使用 Bresenham 的線條繪製演算法。

[Direct2D](./direct2d-portal.md) 會轉譯不透明、透明、別名和消除鋸齒的基本專案。 新式 Ui 通常會利用透明度和動畫。 Direct2D 可讓您更輕鬆地建立新式 UI，因為它對於它接受和轉譯透明內容的方式有嚴格的保證，而且其所有基本專案都是使用硬體加速來呈現。 Direct2D 不是 [GDI](/windows/desktop/gdi/windows-gdi)的純超集合：在 GPU 上執行的 GPU 不存在於 Direct2D 時，可能會過長慢的基本專案。 因為 Direct2D 是以這種方式來強調3D 加速，所以也很容易與 Direct3D 搭配使用。

自 Windows NT 4 起， [GDI](/windows/desktop/gdi/windows-gdi) 已在核心模式中執行。 應用程式會呼叫 GDI，然後呼叫其核心模式對應專案，其會將基本專案傳遞至其本身的驅動程式模型。 然後，此驅動程式會將結果傳送至全域核心模式顯示驅動程式。

從 Windows 2000 開始， [gdi](/windows/desktop/gdi/windows-gdi) 和 gdi 驅動程式已在核心的獨立空間中執行，稱為「會話空間」。 每個登入會話都會建立一個會話位址空間，而每個 GDI 實例會在此相異核心模式位址空間中獨立執行。 不過，Direct2D 會在使用者模式中執行，並透過使用者模式 Direct3D 驅動程式，將繪製命令傳遞至核心模式驅動程式。

![圖 1-相較于 gdi 的 direct2d](images/direct2d-vs-gdi1.png)

## <a name="gdi-and-direct2d-hardware-acceleration"></a>GDI 和 Direct2D 硬體加速

[Direct2D](./direct2d-portal.md)與[GDI](/windows/desktop/gdi/windows-gdi)硬體加速之間最重要的差異是驅動它們的基礎技術。 Direct2D 在最上層的 Direct3D 上具有多層式，而且 GDI 具有自己的驅動程式模型， (的 DDI) 的 GDI 設備磁碟機介面，這會對應至 GDI 基本專案。 Direct3D 驅動程式模型會對應至 GPU 中的3D 轉譯硬體所呈現的內容。 當您第一次定義 GDI DDI 時，大部分的顯示器加速硬體以 GDI 基本專案為目標。 經過一段時間之後，就能更強調地強調3D 遊戲加速，並減少應用程式加速。 因此，BitBlt API 是硬體加速的，而其他大部分的 GDI 作業則不會發生。

這會將變更順序的階段設定為 [GDI](/windows/desktop/gdi/windows-gdi) 呈現給顯示器的方式。 下圖顯示 GDI 顯示器轉譯如何從 Windows XP 變更為 Windows 7。

![圖 2-gdi 顯示呈現的演進](images/direct2d-vs-gdi2.png)

另外還有一些其他因素會導致 [GDI](/windows/desktop/gdi/windows-gdi) 驅動程式模型的變更，如下所述。

### <a name="increasing-complexity-and-size-of-display-drivers"></a>增加顯示驅動程式的複雜度和大小

3D 驅動程式在一段時間後會變得更複雜。 更複雜的程式碼通常會有更多瑕疵，使驅動程式在驅動程式 bug 無法導致系統重新開機的使用者模式中存在。 如上圖所示，顯示驅動程式會分割成複雜的使用者模式元件和較簡單的核心模式元件。

### <a name="difficulty-in-synchronizing-session-and-global-kernel-address-spaces"></a>同步處理會話和全球核心位址空間時遇到困難

在 Windows XP 中，顯示驅動程式存在於兩個不同的位址空間中：會話空間和核心空間。 驅動程式的元件需要回應電源管理事件之類的事件。 這必須與會話位址空間中的驅動程式狀態同步處理。 這是一項困難的工作，當顯示驅動程式嘗試處理這些相異的位址空間時，可能會導致瑕疵。

### <a name="composited-window-management"></a>複合視窗管理

桌面視窗管理員 (DWM) （在 Windows 7 中引進的組合視窗管理員）會將所有視窗轉譯成非螢幕表面，然後將它們組合在一起，以顯示在畫面上。 這需要 [GDI](/windows/desktop/gdi/windows-gdi) 才能轉譯成介面，然後 Direct3D 會將其轉譯為顯示。 這會造成 XP 驅動程式模型發生問題，因為 GDI 和 Direct3D 是平行驅動程式堆疊。

如此一來，在 Windows Vista 中， [GDI](/windows/desktop/gdi/windows-gdi) DDI 顯示驅動程式會實作為 Microsoft 提供的標準顯示驅動程式 (CDD) 將 GDI 內容轉譯成系統記憶體點陣圖以組成螢幕。

## <a name="gdi-rendering-in-windows-7"></a>Windows 7 中的 GDI 轉譯

在 Windows Vista 中使用的驅動程式模型需要影片記憶體介面和系統記憶體介面都支援每個 [GDI](/windows/desktop/gdi/windows-gdi) 視窗。 這會導致系統記憶體用於每個 GDI 視窗。

因此，Windows 7 中的 [GDI](/windows/desktop/gdi/windows-gdi) 已再次變更。 . GDI 不會轉譯成系統記憶體介面，而是為了轉譯成光圈記憶體區段而不會呈現。 您可以從包含視窗內容的視訊記憶體介面更新口徑記憶體。 GDI 可以轉譯回光圈記憶體，然後將結果傳回視窗介面。 由於記憶體區段是由 GPU 定址，因此 GPU 可以加速這些更新至視訊記憶體介面。 例如，在這些情況下，文字轉譯、BitBlts、AlphaBlend、TransparentBlt 和 StretchBlt 全都加速。

## <a name="contrasting-direct2d-and-gdi-acceleration-in-windows-7"></a>Windows 7 中的對比 Direct2D 和 GDI 加速

[Direct2D](./direct2d-portal.md) 和 [GDI](/windows/desktop/gdi/windows-gdi) 都是2D 立即模式轉譯 api，並為硬體加速。 不過，這兩個 Api 中仍有一些差異。

### <a name="location-of-resources"></a>資源的位置

[GDI](/windows/desktop/gdi/windows-gdi) 預設會在系統記憶體中維護其資源（尤其是點陣圖）。 [Direct2D](./direct2d-portal.md) 會在顯示介面卡上的視訊記憶體中維護其資源。 當 GDI 需要更新視訊記憶體時，必須透過匯流排來完成這項作業，除非資源已在光圈記憶體區段中，或是可以直接表示作業。 相反地，Direct2D 只會將其基本專案轉譯為 Direct3D 基本專案，因為這些資源已經在視訊記憶體中。

### <a name="rendering-method"></a>轉譯方法

為了維持相容性， [GDI](/windows/desktop/gdi/windows-gdi) 會使用 CPU 來執行其轉譯的大型部分，以佔用記憶體。 相反地， [Direct2D](./direct2d-portal.md) 會將其 api 呼叫轉譯為 Direct3D 基本專案和繪圖作業。 然後，會在 GPU 上轉譯結果。 當將口徑記憶體複製到代表 GDI 視窗的視訊記憶體介面時，會在 GPU 上執行某些 GDI 轉譯。

### <a name="scalability"></a>延展性

[Direct2D](./direct2d-portal.md)的轉譯呼叫是 GPU 的所有獨立命令資料流程。 每個 Direct2D factory 都代表不同的 Direct3D 裝置。 [GDI](/windows/desktop/gdi/windows-gdi) 會針對系統上的所有應用程式使用一個命令資料流程。 GDI 的方法可能會產生 GPU 和 CPU 轉譯內容的額外負荷。

### <a name="location"></a>Location

[Direct2D](./direct2d-portal.md) 完全以使用者模式運作，包括 direct3d 執行時間和使用者模式 Direct3D 驅動程式。 這有助於防止核心中的程式碼缺失造成系統損毀。 不過， [GDI](/windows/desktop/gdi/windows-gdi)在核心模式的會話空間中有大部分的功能，且其 API 介面在使用者模式中。

### <a name="availability-of-hardware-acceleration"></a>硬體加速的可用性

[GDI](/windows/desktop/gdi/windows-gdi) 是 windows XP 上的硬體加速功能，當桌面視窗管理員正在執行，且有 WDDM 1.1 驅動程式正在使用中時，會在 windows 7 上加速。 [Direct2D](./direct2d-portal.md) 是幾乎任何 WDDM 驅動程式的硬體加速，以及 DWM 是否正在使用中。 在 Vista 上，GDI 一律會在 CPU 上呈現。

### <a name="presentation-model"></a>展示模型

當您第一次設計 Windows 時，記憶體不足，無法讓每個視窗都儲存在自己的點陣圖中。 如此一來， [GDI](/windows/desktop/gdi/windows-gdi) 一律會以邏輯方式直接轉譯至螢幕，並套用各種裁剪區域，以確保應用程式不會在其視窗之外轉譯。 在 [Direct2D](./direct2d-portal.md) 模型中，應用程式會轉譯為背景緩衝區，並在應用程式完成繪製時顯示結果。 如此一來，Direct2D 就可以處理動畫案例，比 GDI 更流暢地。

## <a name="conclusion"></a>結論

現有的 [GDI](/windows/desktop/gdi/windows-gdi) 程式碼在 Windows 7 下將繼續正常運作。 不過，在撰寫新的圖形轉譯程式碼時，應該考慮 [Direct2D](./direct2d-portal.md) ，因為它會更充分利用新式 gpu。

 

 