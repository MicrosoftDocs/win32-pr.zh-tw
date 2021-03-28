---
description: 若要設定事件追蹤會話，請使用事件 \_ 追蹤 \_ 屬性結構來指定會話的屬性。
ms.assetid: 8a6aa39c-ec81-42ac-a26e-29f1f6960220
title: 設定和啟動事件追蹤會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f86ec57975e8f12ede17e5e2cda962c010aa1af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973848"
---
# <a name="configuring-and-starting-an-event-tracing-session"></a>設定和啟動事件追蹤會話

若要設定事件追蹤會話，請使用 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構來指定會話的屬性。 您配置給 **事件 \_ 追蹤 \_ 屬性** 結構的記憶體必須夠大，才能同時包含在記憶體中結構後面的會話和記錄檔名稱。

指定會話的屬性之後，請呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) 函數來啟動會話。 如果函式成功， *SessionHandle* 參數會包含會話控制碼，而 **LoggerNameOffset** 屬性將會包含會話名稱的位移。

若要啟用您想要將事件記錄到會話的提供者，請呼叫 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函式來啟用傳統提供者和 [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) 函式，以啟用以 [資訊清單為基礎的](about-event-tracing.md) 提供者。 若要在 Windows 8.1、Windows Server 2012 R2 和更新版本上，將您想要記錄事件的「提供者」記錄至特定條件，請呼叫 [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) 函數。

此外，您也可以透過呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 函式來追蹤事件的其他資訊。 **TraceSetInformation** 會將其他追蹤資訊放入事件的 [擴充資料] 區段中，而且可以包含追蹤版本資訊之類的資訊，或目前在系統上註冊的提供者。 如需詳細資訊，請參閱 [取出其他事件追蹤資料](retrieving-additional-event-tracing-data.md)。

最多八個追蹤會話可以從相同的 [資訊清單](about-event-tracing.md) 提供者啟用和接收事件。 不過，只有一個追蹤會話可以啟用 [傳統](about-event-tracing.md) 提供者。 如果有一個以上的追蹤會話嘗試啟用傳統提供者，當第二個會話啟用提供者時，第一個會話會停止接收事件。 例如，如果 Session A enabled Provider 1 and then Session B enabled Provider 1，則只有會話 B 會接收來自提供者1的事件。

您可以使用這三個函式中的任一個來啟用提供者，但如果您使用 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 來啟用以資訊清單為基礎的提供者，則可能會遺失功能，因為您將無法提供 MatchAllKeyword 值、指定要包含在事件中的擴充資料項目，或提供提供者定義的篩選資料。 如需詳細資訊，請參閱每個函數的 [備註] 區段。

在 Windows 8.1、Windows Server 2012 R2 和更新版本上， [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) 函式可以使用事件承載、範圍和堆疊逐步篩選，以及 [**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) 和 [**事件 \_ 篩選 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) 項結構，以篩選記錄器會話中的特定條件。 如需事件裝載篩選準則的詳細資訊，請參閱 [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)和 [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) 函式以及 **啟用 \_ 追蹤 \_ 參數**、 **事件 \_ 篩選器 \_ 描述** 元和承載 [**\_ 篩選 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) 述詞結構。

若要判斷用來啟用以資訊清單為基礎之提供者的層級和關鍵字，請使用下列其中一個命令：

-   **Logman** **查詢***提供者-名稱*
-   **Wevtutil** **gp** *提供者-名稱*

這些命令只會列出層級和關鍵字，提供者必須記錄可能控制器的任何篩選資料需求。

若要列舉以資訊清單為基礎的提供者，請使用 **Wevtutil** **ep**。

若為傳統提供者，則是由提供者進行記錄，並提供給可能控制器的嚴重性層級，或啟用它支援的旗標。 如果提供者想要由任何控制器啟用，則提供者應該接受0的嚴重性層級，並啟用旗標，並將0解讀為要求執行預設記錄 (可能) 的任何內容。

您可以在提供者註冊本身之前或之後，啟用提供者。 啟用提供者之後，ETW 接著會呼叫提供者的回呼函式。 如果未註冊提供者，ETW 會在其註冊之後，呼叫提供者的回呼函數。

您也可以使用 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函式來停用提供者 (停止將事件記錄到您的會話) 或更新記錄層級或啟用提供者的旗標。 使用 [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) 函式，您可以停用提供者或更新層級、關鍵字、延伸資料和篩選資料。 每次呼叫 **EnableTrace** 或 **EnableTraceEx** 函式時，ETW 都會呼叫提供者的回呼函式。 此提供者會在會話停用提供者之前保持啟用狀態。

若要在收集事件之後停止追蹤會話，請呼叫 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 函式， \_ 並 \_ \_ 以控制項程式碼的形式傳遞事件追蹤控制停止。 若要指定要停止的會話，您可以將從先前呼叫所取得的事件追蹤會話控制碼傳遞至 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) 函式，或傳遞先前啟動之會話的名稱。 停止會話之前，請務必停用所有提供者。 如果您在第一次停用提供者之前停止會話，ETW 將會停用提供者，並嘗試呼叫提供者的控制項回呼函數。 如果啟動會話的應用程式在未停用提供者或呼叫 **ControlTrace** 函式的情況下結束，則提供者會保持啟用狀態。

如果 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 成功，則會更新會話屬性以反映最終的屬性值，並執行事件追蹤會話的統計資料。

如需啟動事件追蹤會話的範例，請參閱下列內容：

-   [此範例會建立會話並啟用以資訊清單為基礎的提供者](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) -啟動追蹤會話、啟用以資訊清單為基礎的提供者、停用提供者，然後停止會話。

如需啟動追蹤會話的詳細資訊，請參閱下列其中一項：

-   [設定並啟動 SystemTraceProvider 會話](configuring-and-starting-a-systemtraceprovider-session.md)
-   [設定和啟動 NT Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [設定和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)
-   [設定和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)
-   [設定和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定和啟動私用記錄器會話](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[設定並啟動 SystemTraceProvider 會話](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[設定和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[設定和啟動 NT Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)
</dt> <dt>

[**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace)
</dt> <dt>

[**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**事件 \_ 篩選器 \_ 描述項**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**裝載 \_ 篩選述詞 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[更新事件追蹤會話](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
