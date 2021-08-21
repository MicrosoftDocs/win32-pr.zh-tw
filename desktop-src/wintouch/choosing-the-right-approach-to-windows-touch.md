---
title: 選擇正確的方法來 Windows Touch
description: 本節說明您可以使用 Windows Touch 不同的方法。
ms.assetid: 983023e4-355b-45ba-8572-d93c460d2ff8
keywords:
- Windows觸控、不同的方法
- Windows觸控、選擇方法
- Windows觸控、增強應用程式
- Windows觸控、縮放支援
- WindowsTouch，舊版支援
- Windows觸控、RealTimeStylus 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5ad8be1a460b7c91b01a4c566566c424feabc10206482cca72ae3739584c75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030345"
---
# <a name="choosing-the-right-approach-to-windows-touch"></a>選擇正確的方法來 Windows Touch

本節說明您可以使用 Windows Touch 不同的方法。

您可以透過許多方式使用 Windows Touch 功能來增強應用程式。 在您採用方法之前，您應該考慮您想要如何處理您的應用程式。 以下是 Windows Touch 的一般案例：

-   您希望應用程式的行為與舊版 Windows 中的行為相同，但希望 Windows Touch 訊息的行為一致。
-   您想要在您的應用程式中進行自訂物件旋轉、轉譯、移動或縮放支援。
-   您希望您的應用程式能夠更精細地解讀 Windows Touch 手勢，或在特別針對 Windows Touch 輸入優化的應用程式上解讀多次觸控。
-   您有一個使用 [**RealTimeStylus**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus)物件的應用程式，而且想要使用 Windows Touch 功能來增強它。

## <a name="you-want-your-application-to-behave-as-it-did-in-legacy-versions-of-windows"></a>您希望應用程式的行為與舊版 Windows

在 Windows 7 中，應用程式預設會產生可啟用 Windows Touch 功能的訊息。 例如，平移手勢會觸發 WM \_ \* 捲軸訊息。 除了平移支援之外，Windows 7 中的預設 WM 軌跡 \_ 處理常式也支援界限意見反應、縮放，以及按下和點擊。 您也可以透過舊版支援來啟用界限意見反應。 如需手勢如何對應至訊息的詳細資訊，請參閱[Windows Touch 手勢總覽](windows-touch-gestures-overview.md)。 只想要使用這種基本功能的開發人員不需要直接使用 Windows Touch API。

> [!Note]  
> 自訂捲軸處理常式必須支援適用于 **wm \_ VSCROLL** 訊息的 **SM \_ THUMBPOSITION** 要求，且必須支援 sb **\_ HSCROLL** 訊息的 **sb \_ LINELEFT** 要求和 **sb \_ LINERIGHT** 要求。

 

-   [舊版對於移動捲軸的支援](legacy-support-for-panning-with-scrollbars.md)區段說明如何確保您的應用程式在 Windows 7 中的行為如同使用者預期。

## <a name="you-want-custom-object-rotation-translation-panning-or-zoom-support"></a>您想要自訂物件旋轉、轉譯、移動流覽或縮放支援

如果您需要有限的觸控支援，但 Windows 7 提供的預設行為對您的應用程式而言並不夠，您可以使用筆勢來增強您的應用程式。 藉由使用筆勢，您可以藉由處理 [**WM \_ 手勢**](wm-gesture.md) 訊息來解讀手勢命令。 如需筆勢的詳細資訊，請參閱[Windows Touch 手勢](guide-multi-touch-gestures.md)一節。 如果您的應用程式只需要支援高度細微的旋轉、改善的縮放支援或單指移動，手勢就是進行 Windows Touch 開發的最佳方法。 除了解讀手勢訊息，您也可以選擇支援界限意見反應。 如需界限意見反應的詳細資訊，請參閱[Windows Touch 程式設計參考](windows-touch-programming-reference.md)的[界限意見](boundary-feedback.md)一節。 在 Windows 7 中，命令提示字元和 Internet Explorer 利用界限意見反應和手勢。

-   [改進單一手指移動體驗](improving-the-single-finger-panning-experience.md)一節說明如何藉由處理 [**WM \_ 手勢**](wm-gesture.md)訊息來自訂移動流覽體驗。

## <a name="you-want-fine-grained-gesture-interpretation-or-custom-handling-of-multiple-touch-points"></a>您需要更細緻的手勢解讀或多個觸控點的自訂處理

如果您想要比 [**WM \_ 手勢**](wm-gesture.md) 訊息所提供的手勢更明確地控制手勢，或想要在多個物件上解讀多個手勢，則應該使用操作處理器。 操作處理器基本上是筆勢的超集合。 使用操作處理器需要您針對將原始觸控資料摘要至的操作，執行事件接收器。

如果您想要在解讀手勢以外的情況下使用簡單的物件物理，您應該搭配操作處理器使用慣性處理器。 慣性處理器適用于操作處理器，方法是在操作完成時從操作處理器取得速度值。

如果您想要在您的應用程式中解讀多個觸控點，您應該建立一封 [**WM \_ 觸控**](wm-touchdown.md) 訊息的訊息處理常式。

-   [Windows Touch 輸入](guide-multi-touch-input.md)區段會說明如何解讀 [**WM \_ 觸控**](wm-touchdown.md)訊息。
-   [偵測 [和追蹤多個觸控點](detecting-and-tracking-multiple-touch-points.md) ] 區段會示範如何建立可解讀多個輸入的簡單應用程式。
-   [操作和慣性](manipulation-and-inertia.md)區段說明如何啟用最具彈性的方法來 Windows Touch。

## <a name="you-want-to-enable-windows-touch-input-to-an-application-that-uses-the-realtimestylus"></a>您想要對使用 RealTimeStylus 的應用程式啟用 Windows Touch 輸入

如果您想要針對 Tablet PC 平臺上的多個連絡人啟用輸入，您必須執行可解讀 Windows Touch 資料的自訂 RealTimeStylus 外掛程式。 Microsoft 引進了 [**ITablet3**](/windows/desktop/tablet/itablet3) 和 [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) 介面，可讓您從多個連絡人外掛程式的連絡人輸入。 這些介面可簡化擴充 RealTimeStylus 外掛程式，以支援多個接觸點。

若要檢查是否已啟用多個連絡人的支援，請呼叫 [**IsMultiTouch**](/windows/desktop/tablet/itablet3-ismultitouch)。 若要檢查支援的連絡人數目，請呼叫 [**GetMaximumCursors**](/windows/desktop/tablet/itablet3-getmaximumcursors)。 若要啟用或停用多連絡人支援，請呼叫 [**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)。

> [!Note]  
> 如果您未在多個 RealTimeStylus 中啟用多個連絡人點，則會收到軌跡訊息，例如平移和縮放。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計指南](programming-guide.md)
</dt> </dl>

 

 