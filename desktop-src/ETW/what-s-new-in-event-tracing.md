---
description: 本節說明每個版本中 Windows 新增至事件追蹤的新功能。
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: 事件追蹤的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da1c6f1b54ae8bc4b91bd511bface8569bcf43b2893329b1b0462b46c001724
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102018"
---
# <a name="whats-new-in-event-tracing"></a>事件追蹤的新功能

本節說明每個版本中 Windows 新增至事件追蹤的新功能。

## <a name="windows-10-version-1709"></a>Windows 10 (版本 1709)

ETW 現在可以選擇性地追蹤已啟用至會話之所有提供者的二進位檔。 追蹤會針對在呼叫之前啟用會話的提供者，以及針對會話啟用的所有未來提供者，套用追溯。 您現在也可以查詢作業系統所允許的目前設定的最大系統記錄器數目。 如需詳細資訊，請參閱 [**追蹤 \_ 資訊 \_ 類別**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)列舉的 **TraceProviderBinaryTracking** 和 **TraceMaxLoggersQuery** 值，以及如何 [取出其他事件追蹤資料](retrieving-additional-event-tracing-data.md)。

ETW 現在可以根據事件名稱篩選事件。 您也可以決定哪些事件會取得其堆疊。 如需詳細資訊，請參閱事件 **\_ 篩選器 \_ 類型 \_ 事件 \_ 名稱**、 **事件 \_ 篩選器 \_ 類型 \_ STACKWALK \_ 名稱** 和 **事件 \_ 篩選器 \_ 類型 \_ STACKWALK 層 \_ 級 \_** 的 [**事件 \_ 篩選器 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) 項結構的層級值，以及相關聯的 [**事件 \_ 篩選器 \_ 事件 \_ 名稱**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) 和 [**事件 \_ 篩選 \_ 層級 \_ kw**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) 結構。

## <a name="windows-10"></a>Windows 10

[TraceLogging](../tracelogging/trace-logging-portal.md) 是以 ETW 為基礎，可讓您以簡化的方式檢測原生、.Net 和 WinRT 開發人員的程式碼。 TraceLogging 可讓您包含事件的結構化資料、使事件相互關聯，而且不需要個別的檢測資訊清單 XML 檔案。

加入[提供者特性](provider-traits.md)是將更多資料附加至個別提供者註冊的方法。 它們可用於以資訊清單為基礎或 TraceLogging 的提供者。 目前支援將提供者名稱和/或提供者群組新增至個別提供者註冊。 提供者群組是一項新功能，可讓多個 ETW 提供者依所屬群組的匯總進行控制。

定期捕捉狀態是允許定期傳送至提供者的捕獲狀態通知的方式。 啟用此功能時，只會將通知傳送至先前已啟用目前會話的提供者註冊。 如果通知有任何) ，每個提供者都可以定義自己的回應 (。 如需執行的詳細資料，請參閱 [**追蹤 \_ 定期 \_ 捕捉 \_ 狀態 \_ 資訊**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info)。

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 與 Windows Server 2012 R2

下列功能已新增至 Windows 8.1 和 Windows Server 2012 R2 上的事件追蹤。

支援使用 [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) 函式所使用之事件承載、範圍和堆疊逐步篩選的函式，以及 [**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) 和 [**事件 \_ 篩選 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) 項結構，以篩選記錄器會話中的特定條件。 如需詳細資訊，請參閱

-   [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**TdhCleanupPayloadEventFilterDescriptor**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**TdhDeletePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

此外，請參閱 [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) 函數的詳盡修訂檔，以及這些功能所使用的 [ [**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) ] 和 [ [**事件 \_ 篩選器 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) 元結構]。

定義事件裝載篩選述詞的結構，描述如何篩選新 [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) 函式所使用之追蹤會話中的單一欄位，以及事件識別碼和堆疊逐步篩選所使用的新結構。 如需詳細資訊，請參閱

-   [**事件 \_ 篩選器 \_ 事件 \_ 識別碼**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**裝載 \_ 篩選述詞 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

取得提供者資訊清單中的事件資訊的函式。 如需詳細資訊，請參閱

-   [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**TdhGetManifestEventInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

結構，定義新 [**TdhEnumerateManifestProviderEvents**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) 函式所使用之提供者資訊清單中的事件陣列。 如需詳細資訊，請參閱

-   [**提供者 \_ 事件 \_ 資訊**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 與 Windows Server 2012

下列功能已新增至 Windows 8 和 Windows Server 2012 上的事件追蹤。

在註冊物件上執行作業、提供事件承載剖析、提供追蹤提供者流覽、查詢事件追蹤會話設定，以及處理 relogged 追蹤檔案的函式。 如需詳細資訊，請參閱

-   [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**TdhCloseDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**TdhGetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**TdhGetWppProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**TdhGetWppMessage**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**TdhLoadManifestFromBinary**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**TdhOpenDecodingHandle**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**TdhSetDecodingParameter**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**TraceQueryInformation**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

介面，可提供追蹤程式的 relogger 資訊，以及記錄事件的時間、存取特定事件的資料，以及存取可讓事件追蹤記錄檔 (ETL) 檔的 relogger 功能。 如需詳細資訊，請參閱

-   [**ITraceEvent**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**ITraceEventCallback**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**ITraceRelogger**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

新函數和介面所使用的其他列舉。 如需詳細資訊，請參閱

-   [**事件 \_ 資訊 \_ 類別**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**追蹤 \_ 查詢 \_ 資訊 \_ 類別**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 與 Windows Server 2008 R2

此版本已新增下列功能：

-   提供者在資訊清單中定義篩選的能力。 在 Windows Vista 中，控制器可將篩選資料傳遞給提供者。 但是，資訊清單中未定義篩選資料的配置，因此提供者必須使用其他方法將篩選定義提供給控制器。 在此版本中，提供者可以在資訊清單中定義篩選定義， (查看 [**ProviderType**](../wes/eventmanifestschema-providertype-complextype.md)複雜類型) 的 [**篩選**] 屬性。 然後，控制器可以使用 [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) 函數來判斷篩選定義。 使用篩選準則的提供者應該使用 [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) 函式來寫入事件。
-   能夠使用單一緩衝區來收集多個處理器上所產生的事件。 使用單一緩衝區可避免在多處理器電腦上出現順序不會出現的事件。 如需詳細資訊，請參閱 [**事件 \_ 追蹤 \_ \_ 每個 \_ 處理器的 \_ 緩衝**](logging-mode-constants.md) 記錄模式。 根據預設，ETW 會使用每個處理器的緩衝區。
-   捕獲事件堆疊追蹤的能力。 若要啟用核心事件的堆疊追蹤，請參閱 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 函數。 若要啟用使用者事件的堆疊追蹤，請參閱 [**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)之 **EnableProperty** 成員的 **事件 \_ 啟用 \_ 屬性 \_ 堆疊 \_ 追蹤** 旗標。
-   使用 **事件 \_ 追蹤 \_ 私用 \_ 記錄器 \_ 模式** 記錄模式來指定 **事件 \_ 追蹤 \_ 緩衝 \_ 模式** 或 **事件追蹤檔案模式的 [ \_ \_ \_ \_ NEWFILE** 記錄] 模式 (查看 [記錄模式常數](logging-mode-constants.md)) 。
-   能夠同步啟用提供者。 預設會以非同步方式啟用提供者。 若要同步啟用提供者，請設定 [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)的 *Timeout* 參數。
-   控制器要求提供者記錄其狀態的能力。 如需詳細資訊，請參閱 [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)之 *ControlCode* 參數的 **事件 \_ 控制項程式 \_ 代碼 \_ 捕捉 \_ 狀態** 旗標。
-   取用者使用 [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty) 函數來格式化事件資料的能力。
-   在不包含提供者的電腦上，將事件資訊清單事件解碼的能力。 如需詳細資訊，請參閱 [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest) 函數。

此版本已新增下列函式：

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**EventWriteEx**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**TdhEnumerateProviderFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**TdhFormatProperty**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**TdhLoadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**TdhUnloadManifest**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

此版本已新增下列結構：

-   [**傳統 \_ 事件 \_ 識別碼**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**事件 \_ 擴充 \_ 專案 \_ 堆疊 \_ TRACE32**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**事件 \_ 擴充 \_ 專案 \_ 堆疊 \_ TRACE64**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**事件 \_ 篩選 \_ 標頭**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**提供者 \_ 篩選 \_ 資訊**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

此版本中加入了下列列舉：

-   [**追蹤 \_ 資訊 \_ 類別**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

此版本中新增了下列 MOF 類別：

-   [**StackWalk**](stackwalk.md)
-   [**StackWalk \_ 事件**](stackwalk-event.md)

 

 
