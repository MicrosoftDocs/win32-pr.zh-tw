---
title: 關於 Direct2D
description: 介紹 Direct2D，這是一個 API，可讓 Win32 開發人員能夠執行具有優異效能和視覺品質的2D 圖形轉譯工作。
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D，關於
- Direct2D，互通性
- Direct2D，效能
- Direct2D，可用性
- Direct2D，應用程式
- 互通性，Direct2D
- Direct2D 的效能
- Direct2D 的可用性
- 適用于 Direct2D 的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe011b2d61fbb116efa4818f0db988d24e39fcb707e3ae42ddc0fb91f065652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825575"
---
# <a name="about-direct2d"></a>關於 Direct2D

本主題將介紹 Direct2D，這是一個 API，可讓 Win32 開發人員能夠執行具有優異效能和視覺品質的2D 圖形轉譯工作。

## <a name="what-is-direct2d"></a>什麼是 Direct2D？

Direct2D 是一種硬體加速的即時模式2d 圖形 API，可為2D 幾何、點陣圖和文字提供高效能和高品質的呈現。 Direct2D API 的設計目的是要與使用 GDI、GDI+ 或 Direct3D 的現有程式碼交互操作。

Direct2D 主要是設計來供下列開發人員類別使用：

-   大型企業規模原生應用程式的開發人員。
-   建立可供下游開發人員取用的控制項工具組和程式庫的開發人員。
-   需要伺服器端呈現2D 圖形的開發人員。
-   使用 Direct3D 圖形並需要簡單、高效能的2D 和文字轉譯（用於功能表、使用者介面 (UI) 元素，以及 (HUDs) ）的開發人員。

## <a name="why-direct2d"></a>為什麼要 Direct2D？

在 Microsoft Windows 中建立新的2d 圖形 API 的主要動機包括下列各項：

-   為了跟上 Windows 使用者習慣的不斷增加的視覺效果豐富程度。
-   讓開發人員撰寫2D 轉譯程式碼，以直接調整其執行所在之電腦的圖形處理硬體。
-   讓開發人員撰寫程式碼，以轉譯可在服務內容中執行的2D 圖形。

在最近幾年，終端使用者開始預期數位體驗的視覺精確度更高。 此趨勢會反映在消費性電子產品中。 GPS 裝置、媒體播放裝置、行動電話和數位攝影機在一年後提供一致的體驗。 這種趨勢也可以在電影、電視、影片遊戲和網路上的圖形內容多樣性中看到。 為了持續掌握這些變更，開發人員會一直要求將現有的 Windows 應用程式放到下一層的視覺效果豐富。

新式 Windows 電腦中的圖形處理器也不斷演進，並以影片遊戲圖形的進展以及 Windows Media Center 和 Aero 等 Windows 體驗的部分來推動。 某些 Windows 的應用程式可以使用 Microsoft Direct3D 和 Windows Presentation Foundation (WPF) 來利用新式 gpu。 雖然 Direct3D 有提供高階的3-d 圖形應用程式，而 WPF 滿足 .net 開發人員的需求，但開發人員還是有一些與以 GDI 和 GDI+ 為基礎的大型現有程式碼基底，或是想要在其 Direct3D 應用程式中納入高品質2d 圖形的開發人員的差距。

最後，可以在服務中使用的圖形 API 需求，已成為在企業和 Web 開發案例中工作之開發人員的新興需求。 現有的轉譯 Api 著重在單一使用者會話中的用戶端轉譯。 因此，在服務內容中使用時，它們可能會在穩定和可調整性區域中縮短。 需要新的 API 才能解決此情況。

## <a name="high-performance-with-maximum-availability"></a>具有最高可用性的高效能

Direct2D 是使用 Direct3D 10.1 API 建立的使用者模式程式庫。 這表示 Direct2D 應用程式受益于新式主流 Gpu 上的硬體加速轉譯。 使用 Direct3D 10 層級9轉譯，也可以在舊版 Direct3D 9 硬體上達成硬體加速。 這種組合可為現有 Windows 電腦上的圖形硬體提供絕佳的效能。

> [!Note]  
> 從 Windows 8 開始，Direct2D 是使用 Direct3D 11.1 API 所建立。

 

下圖顯示 Direct2D 的分層架構。

![direct2d 分層架構的圖表](images/direct2d-architectual-layering.png)

在使用硬體加速的情況下，Direct2D 包含高效能的軟體轉譯器。 在軟體中轉譯時，使用 Direct2D 體驗的應用程式明顯比使用 GDI+，且具有類似的視覺品質更佳的呈現效能。 軟體轉譯器也是設計來在服務內容中使用。

使用 Direct2D 轉譯的內容也可以使用 Windows 7 作業系統中的遠端桌面通訊協定 (RDP) 基礎結構，在遠端顯示。 開發人員可以選取顯示電腦上的 GPU 處理轉譯，還是在本機轉譯並以點陣圖形式傳送。 您可以根據所需的填滿率和轉譯的圖形基本數量來建立此選擇。 當顯示電腦執行早于 Windows 7 的作業系統時，會透過網路傳輸點陣圖來執行遠端顯示器轉譯。

藉由提供軟體回復、遠端桌面和服務轉譯，提供單一 API 來結合 Direct3D 與高可用性的效能，Direct2D 可讓開發人員在許多不同的案例中，有單一的高效能轉譯效能。

## <a name="visual-quality"></a>視覺品質

使用 Direct2D for graphics 的應用程式可提供比使用 GDI 來達成更高的視覺品質。 Direct2D 會使用每個基本的消除鋸齒，在呈現的內容中提供更平滑的曲線和線條。 當轉譯2D 基本專案時，也有完整的透明度和 Alpha 混合支援。 下圖會比較在左側) 上使用 GDI (轉譯的別名內容，以及右邊) 上 Direct2D (轉譯的反鋸齒內容。

![以 gdi 和 direct2d 呈現的曲線和線條圖例](images/rendering-curves-and-lines.png)

開發人員可以指定以別名呈現的向量圖形。 這適用于需要貼齊至固定圖元界限的案例中，例如指標或尺規等 UI 元素。如果輸出的 GDI 樣式必須相符，或在轉譯程式中透過多重取樣消除鋸齒或其他其他機制來執行消除鋸齒，則會使用此專案。

## <a name="interoperability"></a>互通性

使用 GDI 和 Direct3D 的介面層級互通性，讓開發人員能夠更輕鬆地整合以 Direct2D 為基礎的呈現。 使用 gdi、GDI+ 或 Direct3D 來轉譯內容的應用程式，可以從使用 Direct2D 來呈現其應用程式的特定區域開始，然後隨著時間移至透過 Direct2D 執行轉譯的模型，主要是針對外掛程式或舊版擴充性使用 GDI。

Direct2D 也可讓您輕鬆地使用適用于高品質文字的[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) ，以及[Microsoft Windows 影像處理元件 (WIC) ](https://msdn.microsoft.com/library/ms737408.aspx)的先進映射功能。

如需有關 Direct2D 互通性的詳細資訊，請參閱 [DIRECT2D SDK 的互通性一節。](interoperability.md)

## <a name="summary"></a>摘要

Microsoft Direct2D 可讓開發人員在其應用程式中建立2D 圖形功能，以提供透過 GDI 改善的視覺品質，以及利用新式 Gpu 進行調整的效能特性。 Direct2D 互通性模型可讓開發人員一次選擇性地將部分應用程式與 GDI、GDI+ 或 Direct3D 轉譯一起遷移。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 8 的 Direct2D 快速入門](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Direct2D API 概觀](the-direct2d-api.md)
</dt> </dl>

 

 