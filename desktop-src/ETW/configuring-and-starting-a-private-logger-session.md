---
description: 私用事件追蹤會話是使用者模式的事件追蹤會話，它會在與&郵件的事件追蹤提供者相同的進程中執行 \# ; 私用會話和它所啟用的提供者必須全都在相同的進程中。
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: 設定和啟動私用記錄器會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469225"
---
# <a name="configuring-and-starting-a-private-logger-session"></a><span data-ttu-id="e198b-103">設定和啟動私用記錄器會話</span><span class="sxs-lookup"><span data-stu-id="e198b-103">Configuring and Starting a Private Logger Session</span></span>

<span data-ttu-id="e198b-104">私用事件追蹤會話是使用者模式的事件追蹤會話，它會在與事件追蹤提供者相同的進程中執行，私用會話和它所啟用的提供者必須全都在相同的進程中。</span><span class="sxs-lookup"><span data-stu-id="e198b-104">A private event tracing session is a user-mode event tracing session that runs in the same process as its event trace providers—the private session and the providers that it enables must all be in the same process.</span></span> <span data-ttu-id="e198b-105">使用私用會話的好處是，私用會話不會計入同時執行的64事件追蹤會話上限。</span><span class="sxs-lookup"><span data-stu-id="e198b-105">The benefit of using a private session is that the private session does not count against the maximum of 64 event tracing sessions executing simultaneously.</span></span>

<span data-ttu-id="e198b-106">設定和啟動私人會話類似于啟動一般事件追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="e198b-106">Configuring and starting a private session is similar to starting a normal event trace session.</span></span> <span data-ttu-id="e198b-107">差別在於 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **Wnode guid** 成員必須包含提供者的 **guid** ，而不是會話，而提供者必須已經註冊 guid。</span><span class="sxs-lookup"><span data-stu-id="e198b-107">The difference is that **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure must contain the **GUID** of the provider, not the session, and the provider must have already registered the GUID.</span></span> <span data-ttu-id="e198b-108">請注意，如果您也 \_ \_ \_ 在進程記錄模式中設定事件追蹤私用 \_ ，您可以針對會話和提供者使用不同的 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="e198b-108">Note that if you also set the EVENT\_TRACE\_PRIVATE\_IN\_PROC logging mode, you can use a different **GUID** for the session and provider.</span></span> <span data-ttu-id="e198b-109">如需啟動一般事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。</span><span class="sxs-lookup"><span data-stu-id="e198b-109">For details on starting a normal event trace session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="e198b-110">請注意，您無法從 DllMain 啟動、停止或清除私用追蹤會話;您應該在 DLL 的初始化和結束常式中這樣做。</span><span class="sxs-lookup"><span data-stu-id="e198b-110">Note that you cannot start, stop, or flush a private trace session from DllMain; you should do so in the initialization and finalization routines of the DLL.</span></span>

<span data-ttu-id="e198b-111">從 Windows 8.1 到 Windows 10， [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) 函式和「 [**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) 」和「 [**事件 \_ 篩選器 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) 元」結構可以使用1607版、「事件內容」、「範圍」和「堆疊逐步篩選」篩選器，以篩選記錄器會話中的特定條件。</span><span class="sxs-lookup"><span data-stu-id="e198b-111">From Windows 8.1 to Windows 10, version 1607, event payload, scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="e198b-112">如需事件裝載篩選準則的詳細資訊，請參閱 [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)和 [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) 函式以及 **啟用 \_ 追蹤 \_ 參數**、 **事件 \_ 篩選器 \_ 描述** 元和承載 [**\_ 篩選 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) 述詞結構。</span><span class="sxs-lookup"><span data-stu-id="e198b-112">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="e198b-113">從 Windows 10，版本1703，低許可權使用者現在可以在啟動的進程中啟動私用記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="e198b-113">Starting with Windows 10, version 1703, low privilege users can now start a private logger session in processes they started.</span></span> <span data-ttu-id="e198b-114">在啟用或啟動私人會話之前，提供者不再需要註冊，這表示提供者「預先啟用」類似于非私用會話提供者。</span><span class="sxs-lookup"><span data-stu-id="e198b-114">The provider no longer needs to be registered prior to enabling or starting the private session, meaning the provider is "pre-enabled" similar to how non-private session providers are.</span></span> <span data-ttu-id="e198b-115">個別進程有8個系統範圍私用記錄器的限制。</span><span class="sxs-lookup"><span data-stu-id="e198b-115">There is a limit of 8 system wide private loggers to an individual process.</span></span> <span data-ttu-id="e198b-116">為了提高跨進程案例的效能，建議使用會話 Api 的篩選 (包括啟動全系統私用記錄器時的 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)、 [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace)、 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)和 [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) 。</span><span class="sxs-lookup"><span data-stu-id="e198b-116">For increased performance in cross process scenarios, it's recommended to use filtering for session APIs (including [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**QueryTrace**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea), and [**StopTrace**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) when starting a system wide private logger.</span></span> <span data-ttu-id="e198b-117">請注意，相同的篩選器應該傳遞至所有會話 Api。</span><span class="sxs-lookup"><span data-stu-id="e198b-117">Note that the same filters should be passed to all session APIs.</span></span> <span data-ttu-id="e198b-118">如需篩選的詳細資訊，請參閱 [**事件 \_ 追蹤 \_ 屬性 \_ V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)。</span><span class="sxs-lookup"><span data-stu-id="e198b-118">For more information about filters, see [**EVENT\_TRACE\_PROPERTIES\_V2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).</span></span>

<span data-ttu-id="e198b-119">如需啟動事件追蹤會話的詳細資訊，請參閱設定 [和啟動事件追蹤會話](configuring-and-starting-an-event-tracing-session.md)。</span><span class="sxs-lookup"><span data-stu-id="e198b-119">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="e198b-120">如需啟動 NT Kernel 記錄器會話的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="e198b-120">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="e198b-121">如需啟動全域記錄器會話的詳細資訊，請參閱設定 [和啟動全域記錄器會話](configuring-and-starting-the-global-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="e198b-121">For details on starting a Global Logger session, see [Configuring and Starting a Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="e198b-122">如需啟動自動記錄器會話的詳細資訊，請參閱設定 [和啟動自動記錄器會話](configuring-and-starting-an-autologger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="e198b-122">For details on starting an AutoLogger session, see [Configuring and Starting an AutoLogger Session](configuring-and-starting-an-autologger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e198b-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e198b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e198b-124">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="e198b-124">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="e198b-125">設定和啟動自動記錄器會話</span><span class="sxs-lookup"><span data-stu-id="e198b-125">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="e198b-126">設定和啟動事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="e198b-126">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="e198b-127">設定和啟動 NT Kernel 記錄器會話</span><span class="sxs-lookup"><span data-stu-id="e198b-127">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="e198b-128">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="e198b-128">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="e198b-129">**啟用 \_ 追蹤 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="e198b-129">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="e198b-130">**事件 \_ 追蹤 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="e198b-130">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="e198b-131">**事件 \_ 追蹤 \_ 屬性 \_ V2**</span><span class="sxs-lookup"><span data-stu-id="e198b-131">**EVENT\_TRACE\_PROPERTIES\_V2**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[<span data-ttu-id="e198b-132">**事件 \_ 篩選器 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="e198b-132">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="e198b-133">**裝載 \_ 篩選述詞 \_**</span><span class="sxs-lookup"><span data-stu-id="e198b-133">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="e198b-134">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="e198b-134">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="e198b-135">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="e198b-135">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="e198b-136">更新事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="e198b-136">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
