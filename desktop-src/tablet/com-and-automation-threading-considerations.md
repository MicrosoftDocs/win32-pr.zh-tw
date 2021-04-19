---
description: 當使用元件物件模型 (COM) 和自動化時，會指定下列 Tablet PC 執行緒考慮。
ms.assetid: cf8feba5-a391-4396-a5d8-1ef58df304a7
title: COM 和自動化執行緒考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe0cf67d427ce89074a605f664e94f35d3d3eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971346"
---
# <a name="com-and-automation-threading-considerations"></a>COM 和自動化執行緒考慮

當使用元件物件模型 (COM) 和自動化時，會指定下列 Tablet PC 執行緒考慮。

-   [執行緒安全性](#thread-safety)
-   [STA 和 MTA 應用程式](#sta-and-mta-applications)
-   [InkCollector 和 InkOverlay](#inkcollector-and-inkoverlay)
-   [事件接收器](#event-sinks)
-   [事件處理常式內的例外狀況](#exceptions-within-event-handlers)
-   [相關主題](#related-topics)

## <a name="thread-safety"></a>執行緒安全性

除了 [InkPicture](inkpicture-control.md) 和 [InkEdit](inkedit-control.md) 控制項以外，Tablet PC 物件是安全線程，而且會標示為兩者。 藉由標示為兩者，它們可以在單一執行緒的單元 (STA) 或多執行緒的單元 (MTA) 中執行。

Windows form 使用 STA 模型，因為 windows form 是以原生 Win32 視窗為基礎，而原生 Win32 視窗原本就是單元執行緒。

## <a name="sta-and-mta-applications"></a>STA 和 MTA 應用程式

如果您的應用程式在 MTA 中執行，或使用自由執行緒封送處理器 (FTM) ，您必須撰寫安全線程的程式碼;不過，藉由這麼做，您就可以改善某些事件處理效能問題。

## <a name="inkcollector-and-inkoverlay"></a>InkCollector 和 InkOverlay

您的應用程式不應該釋出其最終的 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件參考，因而直接從筆墨線程終結物件。 相反地，應用程式應該從應用程式執行緒釋放 **InkCollector** 或 **InkOverlay** 物件。

**注意：** 標示為 MTA 或使用 FTM 的應用程式（允許從筆墨線程直接呼叫應用程式的公寓）可以直接從筆墨線程釋放其 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件的最終參考;不過，這會導致無法復原的應用程式失敗。

## <a name="event-sinks"></a>事件接收器

如果您的應用程式未使用 FTM，而且在不同的單元中建立物件和其事件接收器，則事件會在服務事件接收器的執行緒上執行。

## <a name="exceptions-within-event-handlers"></a>事件處理常式內的例外狀況

從 Tablet PC 事件處理常式內擲回的例外狀況會取用，而其餘或您的應用程式看不到這些例外狀況。 同樣地，也不會從 Tablet PC 事件處理常式傳播 HRESULT 值。 如果使用 COM 層的應用程式擲回例外狀況，背景執行緒就會終止，而例外狀況將會遺失。 不會呼叫任何其他事件處理常式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[C + + 事件接收器範例](c---event-sinks-sample.md)
</dt> <dt>

[一般執行緒考慮](general-threading-considerations.md)
</dt> <dt>

[Managed 程式庫執行緒考慮](managed-library-threading-considerations.md)
</dt> </dl>

 

 



