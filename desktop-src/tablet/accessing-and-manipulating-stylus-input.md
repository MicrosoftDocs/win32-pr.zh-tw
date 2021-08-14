---
description: Tablet PC 包含的技術，可在收集的 tablet 畫筆資料時進行互動。
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: 存取和操作手寫筆輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df56b690a8b7459f42e7d692e47dff4e9f1c00330e02cc0c912d7a3ca3dda02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452055"
---
# <a name="accessing-and-manipulating-stylus-input"></a>存取和操作手寫筆輸入

Tablet PC 包含的技術，可在收集的 tablet 畫筆資料時進行互動。 [**RealTimeStylus**](realtimestylus-class.md)類別是 StylusInput 應用程式開發介面 (API) 的一部分，可提供 tablet 畫筆資料串流的存取權。 這些 Api 可讓您獨立地捕捉、中斷和修改資料流程，而不需要轉譯和收集筆跡。

StylusInput Api 的設計目的是：

-   提供 tablet 畫筆資料串流的即時存取。
-   透過將 UI 執行緒上的封包資料排入佇列，並將筆墨集合設為單一執行緒，讓使用者介面 (UI) 執行緒封鎖動態筆墨轉譯。
-   使用 [**InkCollector**](inkcollector-class.md) 物件、 [**InkOverlay**](inkoverlay-class.md) 物件、 [InkPicture](inkpicture-control-reference.md) 控制項或 [InkEdit](inkedit-control-reference.md) 控制項來收集筆跡，以提高效能並降低整體執行緒的使用。

StylusInput Api 不是設計來與 [**InkCollector**](inkcollector-class.md) 物件、 [**InkOverlay**](inkoverlay-class.md) 物件、 [InkPicture](inkpicture-control-reference.md) 控制項或 [InkEdit](inkedit-control-reference.md) 控制項搭配使用。

當您需要直接與 tablet 畫筆資料流程互動，或當應用程式可能封鎖即時筆跡時，請使用 [**RealTimeStylus**](realtimestylus-class.md) 物件。 當這些物件的預設行為提供您所需的行為時，請使用 [**InkCollector**](inkcollector-class.md) 物件、 [**InkOverlay**](inkoverlay-class.md) 物件、 [InkPicture](inkpicture-control-reference.md) 控制項或 [InkEdit](inkedit-control-reference.md) 控制項。

## <a name="in-this-section"></a>本節內容

下列各節說明 StylusInput Api 的元素：

-   [StylusInput Api 的架構](architecture-of-the-stylusinput-apis.md)
-   [使用 StylusInput Api](working-with-the-stylusinput-apis.md)
    -   [使用 RealTimeStylus 類別](working-with-the-realtimestylus-class.md)
    -   [外掛程式和 RealTimeStylus 類別](plug-ins-and-the-realtimestylus-class.md)
    -   [外掛程式資料和 RealTimeStylus 類別](plug-in-data-and-the-realtimestylus-class.md)
    -   [StylusInput Api 的執行注意事項](implementation-notes-for-the-stylusinput-apis.md)
    -   [筆墨-集合外掛程式](ink-collection-plug-ins.md)
    -   [動態轉譯器外掛程式](dynamic-renderer-plug-ins.md)
    -   [辨識器外掛程式](recognizer-plug-ins.md)
-   [使用 StylusInput Api 時的考慮](considerations-when-using-the-stylusinput-apis.md)
    -   [StylusInput Api 的設計考慮](design-considerations-for-the-stylusinput-apis.md)
    -   [StylusInput Api 的執行緒考慮](threading-considerations-for-the-stylusinput-apis.md)

[串聯的 RealTimeStylus 模型](the-cascaded-realtimestylus-model.md)

-   [StylusInput Api 的錯誤處理考慮](error-handling-considerations-for-the-stylusinput-apis.md)
-   [StylusInput Api 的效能考慮](performance-considerations-for-the-stylusinput-apis.md)
-   [StylusInput Api 的部分信任考慮](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[RealTimeStylus 外掛程式範例](realtimestylus-plug-in-sample.md)
</dt> <dt>

[RealTimeStylus 筆墨集合範例](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



