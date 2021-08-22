---
description: 事件追蹤取用者可以處理來自一或多個提供者的事件。
ms.assetid: 039a9f66-228e-4258-9967-2b2cd7d31091
title: '取用事件 (事件追蹤) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42761bed132c5416a99888e067a1192571a527f39506e8964d5ea0209135b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269358"
---
# <a name="consuming-events-event-tracing"></a>取用事件 (事件追蹤) 

事件追蹤取用者可以處理來自一或多個提供者的事件。 取用者可以從記錄檔或即時處理事件。 您可以在控制器指定會話的即時記錄模式時，即時使用事件。 基於效能考慮，不建議在 Windows Vista 之前進行即時處理。

若要指定您要從中處理事件的追蹤會話，請使用 [**事件 \_ 追蹤 \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) 記錄檔結構。 您必須針對您想要處理的每個記錄檔或即時會話，初始化此結構的複本。

若要使用記錄檔中的事件，請將 **LogFileName** 成員設定為記錄檔的名稱。 若要使用即時會話中的事件，請將 **LoggerName** 成員設定為會話名稱。 您也可以使用此結構來指定 [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka) 回呼，以及用來處理事件的 [*>app >eventcallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback) 或 [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback) 回呼。

-   [**EventRecordCallback**](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)：接收並處理所有事件 (包括從一或多個記錄檔和即時會話) 的標頭事件。 如果您使用追蹤資料協助程式函式來剖析事件資料，或您想要取得事件的相關中繼資料，則會執行此回呼。
-   [*>App >eventcallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)：接收並處理所有事件 (包括從一或多個記錄檔和即時會話) 的標頭事件。
-   [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)-接收和處理有關目前緩衝區的摘要資訊，例如遺失的事件。 ETW 會在將緩衝區中的所有事件傳遞給取用者之後，呼叫回呼。 取用者也可以使用此回呼來取消事件處理;但是，如果您要即時取用事件，ETW 會傳遞事件，直到控制器停止會話為止。

定義一個或多個追蹤會話之後，請針對您要處理的每個追蹤會話呼叫 [**OpenTrace**](/windows/win32/api/evntrace/nf-evntrace-opentracea) 函數;您可以處理一或多個記錄檔中的事件，但只能從一個即時會話處理。 然後，您會將 **OpenTrace** 傳回的追蹤會話控制碼清單傳遞給 [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace) 函數。 **ProcessTrace** 函式會結合事件、將事件排序為時間順序，然後一次將它們傳遞給回呼。 您可以使用 *StartTime* 和 *EndTime* 參數，將事件篩選成隻包含落在特定時間範圍內的事件。 **ProcessTrace** 函式會封鎖執行緒，直到您的取用者處理追蹤會話中的所有事件、 [*BufferCallback*](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)傳回 **FALSE** 或您呼叫 [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace)。

**在 Windows Vista 之前：** 只有在 [**ProcessTrace**](/windows/win32/api/evntrace/nf-evntrace-processtrace)傳回之後，您才可以呼叫 [**CloseTrace**](/windows/win32/api/evntrace/nf-evntrace-closetrace) 。

如需示範如何使用資訊清單、MOF 或 TMF 檔案所發佈事件的範例，請參閱 [使用 TDH 抓取事件資料](retrieving-event-data-using-tdh.md)。 請注意，從 Windows Vista 開始，您應該使用追蹤資料協助程式 (TDH) 函數來取用事件。

如需示範如何取用使用 MOF 發佈之事件的範例，請參閱 [使用 Mof 來取得事件資料](retrieving-event-data-using-mof.md)。

 

 
