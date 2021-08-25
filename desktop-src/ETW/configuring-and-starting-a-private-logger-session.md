---
description: 私用事件追蹤會話是使用者模式的事件追蹤會話，它會在與&郵件的事件追蹤提供者相同的進程中執行 \# ; 私用會話和它所啟用的提供者必須全都在相同的進程中。
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: 設定和啟動私用記錄器會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf15db05c03e5a412cf07ee6e020d2321380f2d48abba465669dc807729fe38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901498"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>設定和啟動私用記錄器會話

私用事件追蹤會話是使用者模式的事件追蹤會話，它會在與事件追蹤提供者相同的進程中執行，私用會話和它所啟用的提供者必須全都在相同的進程中。 使用私用會話的好處是，私用會話不會計入同時執行的64事件追蹤會話上限。

設定和啟動私人會話類似于啟動一般事件追蹤會話。 差別在於 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **Wnode guid** 成員必須包含提供者的 **guid** ，而不是會話，而提供者必須已經註冊 guid。 請注意，如果您也 \_ \_ \_ 在進程記錄模式中設定事件追蹤私用 \_ ，您可以針對會話和提供者使用不同的 **GUID** 。 如需啟動一般事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。

請注意，您無法從 DllMain 啟動、停止或清除私用追蹤會話;您應該在 DLL 的初始化和結束常式中這樣做。

從 Windows 8.1 到 Windows 10， [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)函式和「[**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)」和「[**事件 \_ 篩選器 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)元」結構可以使用1607版、「事件內容」、「範圍」和「堆疊逐步篩選」篩選器，以篩選記錄器會話中的特定條件。 如需事件裝載篩選準則的詳細資訊，請參閱 [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)和 [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) 函式以及 **啟用 \_ 追蹤 \_ 參數**、 **事件 \_ 篩選器 \_ 描述** 元和承載 [**\_ 篩選 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) 述詞結構。

從 Windows 10，版本1703，低許可權使用者現在可以在啟動的進程中啟動私用記錄器會話。 在啟用或啟動私人會話之前，提供者不再需要註冊，這表示提供者「預先啟用」類似于非私用會話提供者。 個別進程有8個系統範圍私用記錄器的限制。 為了提高跨進程案例的效能，建議使用會話 Api 的篩選 (包括啟動全系統私用記錄器時的 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)、 [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace)、 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)和 [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) 。 請注意，相同的篩選器應該傳遞至所有會話 Api。 如需篩選的詳細資訊，請參閱 [**事件 \_ 追蹤 \_ 屬性 \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)。

如需啟動事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。

如需啟動 NT Kernel 記錄器會話的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。

如需啟動全域記錄器會話的詳細資訊，請參閱設定 [和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)。

如需啟動自動記錄器會話的詳細資訊，請參閱設定 [和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定並啟動 SystemTraceProvider 會話](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[設定和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[設定和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[設定和啟動 NT Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**事件 \_ 追蹤 \_ 屬性 \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**事件 \_ 篩選器 \_ 描述項**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**裝載 \_ 篩選述詞 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[更新事件追蹤會話](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
