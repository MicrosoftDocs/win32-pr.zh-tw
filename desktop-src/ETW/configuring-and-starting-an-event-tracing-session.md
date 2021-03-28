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
# <a name="configuring-and-starting-an-event-tracing-session"></a><span data-ttu-id="bf92f-103">設定和啟動事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-103">Configuring and Starting an Event Tracing Session</span></span>

<span data-ttu-id="bf92f-104">若要設定事件追蹤會話，請使用 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構來指定會話的屬性。</span><span class="sxs-lookup"><span data-stu-id="bf92f-104">To configure an event tracing session, use the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure to specify the properties of the session.</span></span> <span data-ttu-id="bf92f-105">您配置給 **事件 \_ 追蹤 \_ 屬性** 結構的記憶體必須夠大，才能同時包含在記憶體中結構後面的會話和記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="bf92f-105">The memory you allocate for the **EVENT\_TRACE\_PROPERTIES** structure must be large enough to also contain the session and log file names that follow the structure in memory.</span></span>

<span data-ttu-id="bf92f-106">指定會話的屬性之後，請呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) 函數來啟動會話。</span><span class="sxs-lookup"><span data-stu-id="bf92f-106">After you specify the properties of the session, call the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function to start the session.</span></span> <span data-ttu-id="bf92f-107">如果函式成功， *SessionHandle* 參數會包含會話控制碼，而 **LoggerNameOffset** 屬性將會包含會話名稱的位移。</span><span class="sxs-lookup"><span data-stu-id="bf92f-107">If the function succeeds, the *SessionHandle* parameter will contain the session handle, and the **LoggerNameOffset** property will contain the offset to the name of the session.</span></span>

<span data-ttu-id="bf92f-108">若要啟用您想要將事件記錄到會話的提供者，請呼叫 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函式來啟用傳統提供者和 [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) 函式，以啟用以 [資訊清單為基礎的](about-event-tracing.md) 提供者。</span><span class="sxs-lookup"><span data-stu-id="bf92f-108">To enable the providers that you want to log events to your session, call the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to enable classic providers and the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable [manifest-based](about-event-tracing.md) providers.</span></span> <span data-ttu-id="bf92f-109">若要在 Windows 8.1、Windows Server 2012 R2 和更新版本上，將您想要記錄事件的「提供者」記錄至特定條件，請呼叫 [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) 函數。</span><span class="sxs-lookup"><span data-stu-id="bf92f-109">To enable providers that you want log events to your session filtering on specific conditions on Windows 8.1,Windows Server 2012 R2, and later, call the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function.</span></span>

<span data-ttu-id="bf92f-110">此外，您也可以透過呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 函式來追蹤事件的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="bf92f-110">In addition, you can also trace additional information on an event with a call to the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function.</span></span> <span data-ttu-id="bf92f-111">**TraceSetInformation** 會將其他追蹤資訊放入事件的 [擴充資料] 區段中，而且可以包含追蹤版本資訊之類的資訊，或目前在系統上註冊的提供者。</span><span class="sxs-lookup"><span data-stu-id="bf92f-111">**TraceSetInformation** puts additional trace information into the extended data section of an event, and can include information such as the trace version info, or what providers are currently registered on the system.</span></span> <span data-ttu-id="bf92f-112">如需詳細資訊，請參閱 [取出其他事件追蹤資料](retrieving-additional-event-tracing-data.md)。</span><span class="sxs-lookup"><span data-stu-id="bf92f-112">For more information, see [Retrieving Additional Event Tracing Data](retrieving-additional-event-tracing-data.md).</span></span>

<span data-ttu-id="bf92f-113">最多八個追蹤會話可以從相同的 [資訊清單](about-event-tracing.md) 提供者啟用和接收事件。</span><span class="sxs-lookup"><span data-stu-id="bf92f-113">Up to eight trace sessions can enable and receive events from the same [manifest-based](about-event-tracing.md) provider.</span></span> <span data-ttu-id="bf92f-114">不過，只有一個追蹤會話可以啟用 [傳統](about-event-tracing.md) 提供者。</span><span class="sxs-lookup"><span data-stu-id="bf92f-114">However, only one trace session can enable a [classic](about-event-tracing.md) provider.</span></span> <span data-ttu-id="bf92f-115">如果有一個以上的追蹤會話嘗試啟用傳統提供者，當第二個會話啟用提供者時，第一個會話會停止接收事件。</span><span class="sxs-lookup"><span data-stu-id="bf92f-115">If more than one trace session tries to enable a classic provider, the first session would stop receiving events when the second session enables the provider.</span></span> <span data-ttu-id="bf92f-116">例如，如果 Session A enabled Provider 1 and then Session B enabled Provider 1，則只有會話 B 會接收來自提供者1的事件。</span><span class="sxs-lookup"><span data-stu-id="bf92f-116">For example, if Session A enabled Provider 1 and then Session B enabled Provider 1, only Session B would receive events from Provider 1.</span></span>

<span data-ttu-id="bf92f-117">您可以使用這三個函式中的任一個來啟用提供者，但如果您使用 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 來啟用以資訊清單為基礎的提供者，則可能會遺失功能，因為您將無法提供 MatchAllKeyword 值、指定要包含在事件中的擴充資料項目，或提供提供者定義的篩選資料。</span><span class="sxs-lookup"><span data-stu-id="bf92f-117">You can use any of the three functions to enable a provider but you may lose functionality if you use [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) to enable a manifest-based provider because you will not be able to provide a MatchAllKeyword value, specify extended data items to include in the event, or provide provider-defined filter data.</span></span> <span data-ttu-id="bf92f-118">如需詳細資訊，請參閱每個函數的 [備註] 區段。</span><span class="sxs-lookup"><span data-stu-id="bf92f-118">For more information, see the Remarks section of each function.</span></span>

<span data-ttu-id="bf92f-119">在 Windows 8.1、Windows Server 2012 R2 和更新版本上， [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) 函式可以使用事件承載、範圍和堆疊逐步篩選，以及 [**啟用 \_ 追蹤 \_ 參數**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) 和 [**事件 \_ 篩選 \_ 描述**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) 項結構，以篩選記錄器會話中的特定條件。</span><span class="sxs-lookup"><span data-stu-id="bf92f-119">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="bf92f-120">如需事件裝載篩選準則的詳細資訊，請參閱 [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)和 [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) 函式以及 **啟用 \_ 追蹤 \_ 參數**、 **事件 \_ 篩選器 \_ 描述** 元和承載 [**\_ 篩選 \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) 述詞結構。</span><span class="sxs-lookup"><span data-stu-id="bf92f-120">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="bf92f-121">若要判斷用來啟用以資訊清單為基礎之提供者的層級和關鍵字，請使用下列其中一個命令：</span><span class="sxs-lookup"><span data-stu-id="bf92f-121">To determine the level and keywords used to enable a manifest-based provider, use one of the following commands:</span></span>

-   <span data-ttu-id="bf92f-122">**Logman** \**查詢\*\*\*提供者-名稱*</span><span class="sxs-lookup"><span data-stu-id="bf92f-122">**Logman** **query** *provider-name*</span></span>
-   <span data-ttu-id="bf92f-123">**Wevtutil** **gp** *提供者-名稱*</span><span class="sxs-lookup"><span data-stu-id="bf92f-123">**Wevtutil** **gp** *provider-name*</span></span>

<span data-ttu-id="bf92f-124">這些命令只會列出層級和關鍵字，提供者必須記錄可能控制器的任何篩選資料需求。</span><span class="sxs-lookup"><span data-stu-id="bf92f-124">The commands list the level and keywords only, the provider must document any filter data requirements for potential controllers.</span></span>

<span data-ttu-id="bf92f-125">若要列舉以資訊清單為基礎的提供者，請使用 **Wevtutil** **ep**。</span><span class="sxs-lookup"><span data-stu-id="bf92f-125">To enumerate the manifest-based providers use **Wevtutil** **ep**.</span></span>

<span data-ttu-id="bf92f-126">若為傳統提供者，則是由提供者進行記錄，並提供給可能控制器的嚴重性層級，或啟用它支援的旗標。</span><span class="sxs-lookup"><span data-stu-id="bf92f-126">For classic providers, it is up to the provider to document and make available to potential controllers the severity levels or enable flags that it supports.</span></span> <span data-ttu-id="bf92f-127">如果提供者想要由任何控制器啟用，則提供者應該接受0的嚴重性層級，並啟用旗標，並將0解讀為要求執行預設記錄 (可能) 的任何內容。</span><span class="sxs-lookup"><span data-stu-id="bf92f-127">If the provider wants to be enabled by any controller, the provider should accept 0 for the severity level and enable flags and interpret 0 as a request to perform default logging (whatever that may be).</span></span>

<span data-ttu-id="bf92f-128">您可以在提供者註冊本身之前或之後，啟用提供者。</span><span class="sxs-lookup"><span data-stu-id="bf92f-128">You can enable the provider before or after the provider registers itself.</span></span> <span data-ttu-id="bf92f-129">啟用提供者之後，ETW 接著會呼叫提供者的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="bf92f-129">After enabling the provider, ETW will then call the provider's callback function.</span></span> <span data-ttu-id="bf92f-130">如果未註冊提供者，ETW 會在其註冊之後，呼叫提供者的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="bf92f-130">If the provider is not registered, ETW will call the provider's callback function after it registers itself.</span></span>

<span data-ttu-id="bf92f-131">您也可以使用 [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) 函式來停用提供者 (停止將事件記錄到您的會話) 或更新記錄層級或啟用提供者的旗標。</span><span class="sxs-lookup"><span data-stu-id="bf92f-131">You can also use the [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) function to disable the provider (stop it from logging events to your session) or to update the logging level or enable flags of the provider.</span></span> <span data-ttu-id="bf92f-132">使用 [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) 函式，您可以停用提供者或更新層級、關鍵字、延伸資料和篩選資料。</span><span class="sxs-lookup"><span data-stu-id="bf92f-132">With the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function, you can disable the provider or update the level, keywords, extended data and filter data.</span></span> <span data-ttu-id="bf92f-133">每次呼叫 **EnableTrace** 或 **EnableTraceEx** 函式時，ETW 都會呼叫提供者的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="bf92f-133">Each time you call the **EnableTrace** or **EnableTraceEx** function, ETW calls the provider's callback function.</span></span> <span data-ttu-id="bf92f-134">此提供者會在會話停用提供者之前保持啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="bf92f-134">The provider remains enabled for the session until the session disables the provider.</span></span>

<span data-ttu-id="bf92f-135">若要在收集事件之後停止追蹤會話，請呼叫 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 函式， \_ 並 \_ \_ 以控制項程式碼的形式傳遞事件追蹤控制停止。</span><span class="sxs-lookup"><span data-stu-id="bf92f-135">To stop the trace session after collecting events, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function and pass EVENT\_TRACE\_CONTROL\_STOP as the control code.</span></span> <span data-ttu-id="bf92f-136">若要指定要停止的會話，您可以將從先前呼叫所取得的事件追蹤會話控制碼傳遞至 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) 函式，或傳遞先前啟動之會話的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf92f-136">To specify the session to stop, you can pass the event tracing session handle obtained from an earlier call to the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function, or the name of a previously started session.</span></span> <span data-ttu-id="bf92f-137">停止會話之前，請務必停用所有提供者。</span><span class="sxs-lookup"><span data-stu-id="bf92f-137">Be sure to disable all providers before stopping the session.</span></span> <span data-ttu-id="bf92f-138">如果您在第一次停用提供者之前停止會話，ETW 將會停用提供者，並嘗試呼叫提供者的控制項回呼函數。</span><span class="sxs-lookup"><span data-stu-id="bf92f-138">If you stop the session before first disabling the provider, ETW will disable the provider and try to call the provider's control callback function.</span></span> <span data-ttu-id="bf92f-139">如果啟動會話的應用程式在未停用提供者或呼叫 **ControlTrace** 函式的情況下結束，則提供者會保持啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="bf92f-139">If the application that started the session ends without disabling the provider or calling the **ControlTrace** function, the provider remains enabled.</span></span>

<span data-ttu-id="bf92f-140">如果 [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) 成功，則會更新會話屬性以反映最終的屬性值，並執行事件追蹤會話的統計資料。</span><span class="sxs-lookup"><span data-stu-id="bf92f-140">If [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) is successful, the session properties are updated to reflect the final property values and run statistics for the event tracing session.</span></span>

<span data-ttu-id="bf92f-141">如需啟動事件追蹤會話的範例，請參閱下列內容：</span><span class="sxs-lookup"><span data-stu-id="bf92f-141">For an example that starts an event tracing session, see the following:</span></span>

-   <span data-ttu-id="bf92f-142">[此範例會建立會話並啟用以資訊清單為基礎的提供者](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) -啟動追蹤會話、啟用以資訊清單為基礎的提供者、停用提供者，然後停止會話。</span><span class="sxs-lookup"><span data-stu-id="bf92f-142">[Example that Creates a Session and Enables a Manifest-based Provider](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) - starts a trace session, enables a manifest-based provider, disables the provider and then stops the session.</span></span>

<span data-ttu-id="bf92f-143">如需啟動追蹤會話的詳細資訊，請參閱下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="bf92f-143">For details on starting a trace session, see one of the following:</span></span>

-   [<span data-ttu-id="bf92f-144">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-144">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
-   [<span data-ttu-id="bf92f-145">設定和啟動 NT Kernel 記錄器會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-145">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [<span data-ttu-id="bf92f-146">設定和啟動自動記錄器會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-146">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
-   [<span data-ttu-id="bf92f-147">設定和啟動全域記錄器會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-147">Configuring and Starting the Global Logger Session</span></span>](configuring-and-starting-the-global-logger-session.md)
-   [<span data-ttu-id="bf92f-148">設定和啟動私用記錄器會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-148">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a><span data-ttu-id="bf92f-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf92f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf92f-150">設定和啟動私用記錄器會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-150">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="bf92f-151">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-151">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="bf92f-152">設定和啟動自動記錄器會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-152">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="bf92f-153">設定和啟動 NT Kernel 記錄器會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-153">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="bf92f-154">**ControlTrace**</span><span class="sxs-lookup"><span data-stu-id="bf92f-154">**ControlTrace**</span></span>](/windows/win32/api/evntrace/nf-evntrace-controltracea)
</dt> <dt>

[<span data-ttu-id="bf92f-155">**EnableTrace**</span><span class="sxs-lookup"><span data-stu-id="bf92f-155">**EnableTrace**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletrace)
</dt> <dt>

[<span data-ttu-id="bf92f-156">**EnableTraceEx**</span><span class="sxs-lookup"><span data-stu-id="bf92f-156">**EnableTraceEx**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
</dt> <dt>

[<span data-ttu-id="bf92f-157">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="bf92f-157">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="bf92f-158">**啟用 \_ 追蹤 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="bf92f-158">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="bf92f-159">**事件 \_ 篩選器 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="bf92f-159">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="bf92f-160">**事件 \_ 追蹤 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="bf92f-160">**EVENT\_TRACE\_PROPERTIES**</span></span>](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[<span data-ttu-id="bf92f-161">**裝載 \_ 篩選述詞 \_**</span><span class="sxs-lookup"><span data-stu-id="bf92f-161">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="bf92f-162">**StartTrace**</span><span class="sxs-lookup"><span data-stu-id="bf92f-162">**StartTrace**</span></span>](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[<span data-ttu-id="bf92f-163">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="bf92f-163">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="bf92f-164">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="bf92f-164">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="bf92f-165">更新事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="bf92f-165">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
