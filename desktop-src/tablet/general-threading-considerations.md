---
description: 一般執行緒考慮的總覽。
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: 一般執行緒考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f4c6f2aa76775d3d88e8ea60c3899a2d8ac47e5ef07fddbbdfaca96196dee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092572"
---
# <a name="general-threading-considerations"></a>一般執行緒考慮

以下是針對 Tablet PC 進行開發時的一般執行緒考慮。

-   [應用程式和非應用程式執行緒](#application-and-non-application-threads)
-   [效能考量](#performance-considerations)
    -   [事件處理常式](#event-handlers)
    -   [AutoRedraw 屬性](#autoredraw-property)
    -   [DynamicRendering 屬性](#dynamicrendering-property)
-   [事件執行緒考慮](#event-threading-considerations)
    -   [InkCollector 和 InkOverlay 物件事件](#inkcollector-and-inkoverlay-objects-events)
    -   [筆跡物件和筆劃集合事件](#ink-object-and-strokes-collection-events)
    -   [辨識事件](#recognition-events)
    -   [畫筆輸入面板事件](#pen-input-panel-events)
-   [相關主題](#related-topics)

## <a name="application-and-non-application-threads"></a>應用程式和非應用程式執行緒

所有筆墨事件都是在個別、高優先順序的筆墨線程上產生。 即使應用程式執行速度很慢，也可讓筆墨順暢地流動。 不過，事件處理常式可能會變慢或封鎖筆墨的轉譯。

背景辨識方法呼叫所產生的所有辨識事件都是在個別的一般優先順序背景辨識執行緒上處理。

系統會在應用程式的主要使用者介面上產生所有滑鼠事件 (UI) 執行緒。

## <a name="performance-considerations"></a>效能考量

### <a name="event-handlers"></a>事件處理常式

Tablet PC 平臺應用程式開發介面 (API) 具有事件（而非通知模型）的互動式模型。 讓事件處理常式中的程式碼保持簡短，以減少筆墨轉譯遭到封鎖的時間。 Tablet PC 的筆墨集合不會被封鎖，但您的應用程式在封鎖應用程式時不會收到筆墨。

### <a name="autoredraw-property"></a>AutoRedraw 屬性

當您的應用程式執行自訂轉譯時，或是當應用程式對繪製問題很敏感時，您可以自行處理重新繪製，並將 [**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control.md)控制項的 [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw)屬性設定為 **false** 。 使用下表中的事件來處理重新繪製。



| 物件或控制項                                            | 事件                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) 物件<br/> | 基礎控制項的[控制項。無效](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1)的和[control. 小畫家](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1)事件。<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) 物件<br/>     | 基礎控制項的[控制項。無效](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1)的和[control. 小畫家](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1)事件。<br/>                                 |
| [InkPicture](inkpicture-control.md) 控制<br/>      | [InkPicture](inkpicture-control.md)控制項的繼承[控制項。無效](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1)的和[control. 小畫家](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1)事件。<br/> |



 

### <a name="dynamicrendering-property"></a>DynamicRendering 屬性

當您的應用程式執行自訂轉譯時，或是當您想要資訊（而不是筆墨）時，您可以自行處理筆墨的版面配置，並藉由將 [**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件或 [InkPicture](inkpicture-control.md)控制項的 [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering)屬性設定為 **false** ，來關閉筆跡的即時呈現。

## <a name="event-threading-considerations"></a>事件執行緒考慮

Tablet PC 平臺 API 事件會在不同的執行緒上引發。

### <a name="inkcollector-and-inkoverlay-objects-events"></a>InkCollector 和 InkOverlay 物件事件

大部分的 [**InkCollector**](inkcollector-class.md) 和 [**InkOverlay**](inkoverlay-class.md) 物件事件都會在筆墨線程上引發。 只有這些物件的滑鼠事件會在 UI 執行緒上引發。 例如，針對 **InkCollector** 物件，會在 UI 執行緒上引發 [**MouseDown**](inkcollector-mousedown.md) 事件，並在筆墨線程上引發 [**CursorDown**](inkcollector-cursordown.md) 事件。

### <a name="ink-object-and-strokes-collection-events"></a>筆跡物件和筆劃集合事件

[**筆墨**](inkdisp-class.md)物件和 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合事件可能來自筆墨線程或 UI 執行緒。 當您的應用程式操作 **筆墨** 物件或 **筆劃** 集合時，會在 UI 執行緒中產生事件。 當 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件更新 **筆墨** 物件或 **筆劃** 集合時，會在筆墨線程中產生事件。

[InkPicture](inkpicture-control-reference.md)和[InkEdit](inkedit-control-reference.md)控制項會在單一執行緒的單元 (STA) 中運作。 當 InkPicture 或 InkEdit 控制項更新 [**筆墨**](inkdisp-class.md) 物件或 [**筆劃**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合時，會在 UI 執行緒上引發事件。

### <a name="recognition-events"></a>辨識事件

辨識事件是在 UI 執行緒或背景辨識執行緒上引發。

-   [InkEdit](inkedit-control-reference.md)控制項的辨識方法只 [會在 UI](/previous-versions/ms836436(v=msdn.10))執行緒上) 或 [**RecognitionResult**](inkedit-recognitionresult.md) (Automation) 事件，來引發 [**辨識**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) (受控程式庫。
-   [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的 [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)和 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)方法會引發背景辨識執行緒上的 [**辨識和**](inkrecognizercontext-recognition.md) [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md)事件。

### <a name="pen-input-panel-events"></a>畫筆輸入面板事件

[**PenInputPanel**](peninputpanel-class.md) 事件會在建立 **PenInputPanel** 物件的執行緒上引發。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[InkCollector. DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[DynamicRendering。](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[InkPicture. DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[InkCollector. AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[AutoRedraw。](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[InkPicture. AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

