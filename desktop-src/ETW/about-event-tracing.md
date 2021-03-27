---
description: Windows 事件追蹤 (ETW) 是高效率的核心層級追蹤功能，讓您能記錄核心或應用程式定義的事件記錄檔。
ms.assetid: 0eaa7bd3-8537-483a-b0d6-db3b790a6f3d
title: 關於事件追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2f13284cec1d9300c23241fafe154f277f72a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943581"
---
# <a name="about-event-tracing"></a><span data-ttu-id="5e5ce-103">關於事件追蹤</span><span class="sxs-lookup"><span data-stu-id="5e5ce-103">About Event Tracing</span></span>

<span data-ttu-id="5e5ce-104">Windows 事件追蹤 (ETW) 是高效率的核心層級追蹤功能，讓您能記錄核心或應用程式定義的事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-104">Event Tracing for Windows (ETW) is an efficient kernel-level tracing facility that lets you log kernel or application-defined events to a log file.</span></span> <span data-ttu-id="5e5ce-105">您可以即時或從記錄檔取用事件，並使用這些事件來對應用程式進行偵錯工具，或判斷應用程式中發生效能問題的位置。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-105">You can consume the events in real time or from a log file and use them to debug an application or to determine where performance issues are occurring in the application.</span></span>

<span data-ttu-id="5e5ce-106">ETW 可讓您以動態方式啟用或停用事件追蹤，讓您可以在實際執行環境中執行詳細追蹤，而不需要重新開機電腦或應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-106">ETW lets you enable or disable event tracing dynamically, allowing you to perform detailed tracing in a production environment without requiring computer or application restarts.</span></span>

<span data-ttu-id="5e5ce-107">事件追蹤 API 分成三個不同的元件：</span><span class="sxs-lookup"><span data-stu-id="5e5ce-107">The Event Tracing API is broken into three distinct components:</span></span>

-   <span data-ttu-id="5e5ce-108">[控制器](#controllers)，可啟動和停止事件追蹤會話並啟用提供者</span><span class="sxs-lookup"><span data-stu-id="5e5ce-108">[Controllers](#controllers), which start and stop an event tracing session and enable providers</span></span>
-   <span data-ttu-id="5e5ce-109">提供事件的[提供者](#providers)</span><span class="sxs-lookup"><span data-stu-id="5e5ce-109">[Providers](#providers), which provide the events</span></span>
-   <span data-ttu-id="5e5ce-110">取用事件的取用[者](#consumers)</span><span class="sxs-lookup"><span data-stu-id="5e5ce-110">[Consumers](#consumers), which consume the events</span></span>

<span data-ttu-id="5e5ce-111">下圖顯示事件追蹤模型。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-111">The following diagram shows the event tracing model.</span></span>

![事件追蹤模型](images/etdiag2.png)

## <a name="controllers"></a><span data-ttu-id="5e5ce-113">控制器</span><span class="sxs-lookup"><span data-stu-id="5e5ce-113">Controllers</span></span>

<span data-ttu-id="5e5ce-114">控制器是一種應用程式，可定義記錄檔的大小和位置、啟動和停止 [事件追蹤會話](event-tracing-sessions.md)、啟用提供者，讓它們可以將事件記錄到會話、管理緩衝集區的大小，以及取得會話的執行統計資料。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-114">Controllers are applications that define the size and location of the log file, start and stop [event tracing sessions](event-tracing-sessions.md), enable providers so they can log events to the session, manage the size of the buffer pool, and obtain execution statistics for sessions.</span></span> <span data-ttu-id="5e5ce-115">會話統計資料包含使用的緩衝區數目、傳遞的緩衝區數目，以及遺失的事件和緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-115">Session statistics include the number of buffers used, the number of buffers delivered, and the number of events and buffers lost.</span></span> 

<span data-ttu-id="5e5ce-116">如需詳細資訊，請參閱 [控制事件追蹤會話](controlling-event-tracing-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-116">For more information, see [Controlling Event Tracing Sessions](controlling-event-tracing-sessions.md).</span></span>

## <a name="providers"></a><span data-ttu-id="5e5ce-117">提供者</span><span class="sxs-lookup"><span data-stu-id="5e5ce-117">Providers</span></span>

<span data-ttu-id="5e5ce-118">提供者是包含事件追蹤檢測的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-118">Providers are applications that contain event tracing instrumentation.</span></span> <span data-ttu-id="5e5ce-119">在提供者註冊本身之後，控制器就可以在提供者中啟用或停用事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-119">After a provider registers itself, a controller can then enable or disable event tracing in the provider.</span></span> <span data-ttu-id="5e5ce-120">提供者會定義要啟用或停用的解釋。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-120">The provider defines its interpretation of being enabled or disabled.</span></span> <span data-ttu-id="5e5ce-121">一般而言，啟用的提供者會產生事件，而停用的提供者則不會產生事件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-121">Generally, an enabled provider generates events, while a disabled provider does not.</span></span> <span data-ttu-id="5e5ce-122">這可讓您在應用程式中新增事件追蹤，而不需要每次都產生事件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-122">This lets you add event tracing to your application without requiring that it generate events all the time.</span></span> 

<span data-ttu-id="5e5ce-123">雖然 ETW 模型會將控制器和提供者分成不同的應用程式，但應用程式可以同時包含這兩個元件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-123">Although the ETW model separates the controller and provider into separate applications, an application can include both components.</span></span>

<span data-ttu-id="5e5ce-124">如需詳細資訊，請參閱 [提供事件](providing-events.md)。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-124">For more information, see [Providing Events](providing-events.md).</span></span>

### <a name="types-of-providers"></a><span data-ttu-id="5e5ce-125">提供者類型</span><span class="sxs-lookup"><span data-stu-id="5e5ce-125">Types of Providers</span></span>

<span data-ttu-id="5e5ce-126">提供者有四種主要類型： MOF (傳統) 提供者、WPP 提供者、資訊清單型提供者和 TraceLogging 提供者。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-126">There are four main types of providers: MOF (classic) providers, WPP providers, manifest-based providers, and TraceLogging providers.</span></span> <span data-ttu-id="5e5ce-127">如果您要撰寫不需要支援舊版系統的 Windows Vista 或更新版本的應用程式，則應該使用以資訊清單為基礎的提供者或 TraceLogging 提供者。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-127">You should use a manifest-based provider or a TraceLogging provider if you are writing applications for Windows Vista or later that do not need to support legacy systems.</span></span>

#### <a name="mof-classic-providers"></a><span data-ttu-id="5e5ce-128">MOF (傳統) 提供者：</span><span class="sxs-lookup"><span data-stu-id="5e5ce-128">MOF (classic) providers:</span></span>

-   <span data-ttu-id="5e5ce-129">使用 [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 和 [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函數來註冊和寫入事件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-129">Use the [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) and [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) functions to register and write events.</span></span>
-   <span data-ttu-id="5e5ce-130">使用 MOF 類別來定義事件，讓取用者知道其使用方式。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-130">Use MOF classes to define events so that consumers know how to consume them.</span></span>
-   <span data-ttu-id="5e5ce-131">一次只能由一個追蹤會話啟用。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-131">Can be enabled by only one trace session at a time.</span></span>

#### <a name="wpp-providers"></a><span data-ttu-id="5e5ce-132">WPP 提供者：</span><span class="sxs-lookup"><span data-stu-id="5e5ce-132">WPP providers:</span></span>

-   <span data-ttu-id="5e5ce-133">使用 [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) 和 [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) 函數來註冊和寫入事件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-133">Use the [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) and [TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) functions to register and write events.</span></span>
-   <span data-ttu-id="5e5ce-134"> (將相關聯的 TMF 檔案編譯成二進位的 .pdb) ，其中包含從預處理器掃描原始程式碼中的 WPP 檢測所推斷的解碼資訊。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-134">Have associated TMF files (compiled into a binary's .pdb) containing decoding information inferred from the preprocessor's scan of WPP instrumentation in source code.</span></span>
-   <span data-ttu-id="5e5ce-135">一次只能由一個追蹤會話啟用。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-135">Can be enabled by only one trace session at a time.</span></span>

#### <a name="manifest-based-providers"></a><span data-ttu-id="5e5ce-136">以資訊清單為基礎的提供者：</span><span class="sxs-lookup"><span data-stu-id="5e5ce-136">Manifest-based providers:</span></span>

-   <span data-ttu-id="5e5ce-137">使用 [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) 和 [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) 來註冊和寫入事件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-137">Use [EventRegister](/windows/desktop/api/Evntprov/nf-evntprov-eventregister) and [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) to register and write events.</span></span>
-   <span data-ttu-id="5e5ce-138">使用資訊清單來定義事件，讓取用者知道其使用方式。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-138">Use a manifest to define events so that consumers know how to consume them.</span></span>
-   <span data-ttu-id="5e5ce-139">最多可以同時啟用八個追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-139">Can be enabled by up to eight trace sessions simultaneously.</span></span>

#### <a name="tracelogging-providers"></a><span data-ttu-id="5e5ce-140">[TraceLogging](/windows/desktop/tracelogging/trace-logging-about) 提供者：</span><span class="sxs-lookup"><span data-stu-id="5e5ce-140">[TraceLogging](/windows/desktop/tracelogging/trace-logging-about) providers:</span></span>

-   <span data-ttu-id="5e5ce-141">使用 [TraceLoggingRegister](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) 和 [TraceLoggingWrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) 來註冊和寫入事件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-141">Use [TraceLoggingRegister](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) and [TraceLoggingWrite](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) to register and write events.</span></span>
-   <span data-ttu-id="5e5ce-142">使用自我描述事件，讓事件本身包含使用這些事件的所有必要資訊。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-142">Use self-describing events so that the events themselves contain all required information for consuming them.</span></span>
-   <span data-ttu-id="5e5ce-143">最多可以同時啟用八個追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-143">Can be enabled by up to eight trace sessions simultaneously.</span></span>

<span data-ttu-id="5e5ce-144">所有事件提供者基本上都是使用 api 的事件追蹤系列 ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent)適用于舊版技術，而[EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite) / [EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)則適用于較新的) 。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-144">All event providers fundamentally use the Event Tracing family of APIs ([TraceEvent](/windows/win32/api/evntrace/nf-evntrace-traceevent) for legacy technologies and [EventWrite](/windows/desktop/api/Evntprov/nf-evntprov-eventwrite)/[EventWriteEx](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) for newer ones).</span></span> <span data-ttu-id="5e5ce-145">事件提供者在其儲存于事件裝載中的欄位類型，以及它們儲存相關事件解碼資訊的位置，都是不同的。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-145">Event providers simply differ in what field types they store in event payloads and where they store the associated event decoding information.</span></span>

## <a name="consumers"></a><span data-ttu-id="5e5ce-146">取用者</span><span class="sxs-lookup"><span data-stu-id="5e5ce-146">Consumers</span></span>

<span data-ttu-id="5e5ce-147">取用者是選取一或多個事件追蹤會話作為事件來源的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-147">Consumers are applications that select one or more event tracing sessions as a source of events.</span></span> <span data-ttu-id="5e5ce-148">取用者可以同時從多個事件追蹤會話要求事件;系統會依時間順序傳遞事件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-148">A consumer can request events from multiple event tracing sessions simultaneously; the system delivers the events in chronological order.</span></span> <span data-ttu-id="5e5ce-149">取用者可以接收儲存在記錄檔中的事件，或接收即時傳遞事件的會話。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-149">Consumers can receive events stored in log files, or from sessions that deliver events in real time.</span></span> <span data-ttu-id="5e5ce-150">處理事件時，取用者可以指定開始和結束時間，而且只會傳遞在指定時間範圍內發生的事件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-150">When processing events, a consumer can specify start and end times, and only events that occur in the specified time frame will be delivered.</span></span> 

<span data-ttu-id="5e5ce-151">如需詳細資訊，請參閱 [使用事件](consuming-events.md)。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-151">For more information, see [Consuming Events](consuming-events.md).</span></span>

## <a name="missing-events"></a><span data-ttu-id="5e5ce-152">遺失的事件</span><span class="sxs-lookup"><span data-stu-id="5e5ce-152">Missing Events</span></span>

<span data-ttu-id="5e5ce-153">Perfmon、系統診斷和其他系統工具可能會報告事件記錄檔中遺失的事件，並指出 Windows 的事件追蹤 (ETW) 可能不是最佳的設定。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-153">Perfmon, System Diagnostics, and other system tools may report on missing events in the Event Log and indicate that the settings for Event Tracing for Windows (ETW) may not be optimal.</span></span> <span data-ttu-id="5e5ce-154">事件可能會因為許多原因而遺失：</span><span class="sxs-lookup"><span data-stu-id="5e5ce-154">Events can be lost for a number of reasons:</span></span>

-   <span data-ttu-id="5e5ce-155">事件大小總計大於64K。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-155">The total event size is greater than 64K.</span></span> <span data-ttu-id="5e5ce-156">這包括 ETW 標頭加上資料或承載。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-156">This includes the ETW header plus the data or payload.</span></span> <span data-ttu-id="5e5ce-157">使用者無法控制這些遺漏的事件，因為事件大小是由應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-157">A user has no control over these missing events since the event size is configured by the application.</span></span>

-   <span data-ttu-id="5e5ce-158">ETW 緩衝區大小小於事件大小總計。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-158">The ETW buffer size is smaller than the total event size.</span></span> <span data-ttu-id="5e5ce-159">使用者無法控制這些遺漏的事件，因為事件大小是由記錄事件的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-159">A user has no control over these missing events since the event size is configured by the application logging the events.</span></span>

-   <span data-ttu-id="5e5ce-160">針對即時記錄，即時取用者不會消耗足夠的事件，也不會完全存在，然後備份檔案就會填滿。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-160">For real-time logging, the real-time consumer is not consuming events fast enough or is not present altogether and then the backing file is filling up.</span></span> <span data-ttu-id="5e5ce-161">如果事件記錄檔服務在記錄事件時停止並啟動，就會產生這種情況。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-161">This can result if the Event Log service is stopped and started when events are being logged.</span></span> <span data-ttu-id="5e5ce-162">使用者無法控制這些遺漏的事件。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-162">A user has no control over these missing events.</span></span>

-   <span data-ttu-id="5e5ce-163">記錄到檔案時，磁片太慢，無法跟上記錄速度。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-163">When logging to a file, the disk is too slow to keep up with the logging rate.</span></span>

<span data-ttu-id="5e5ce-164">基於上述原因，請向產生事件的應用程式或服務的提供者報告這些問題。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-164">For any of these reasons, please report these problems to the provider of the application or service that is generating the events.</span></span> <span data-ttu-id="5e5ce-165">這些問題只能由應用程式開發人員或記錄事件的服務來修正。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-165">These issues can only be fixed by the application developer or the service logging the events.</span></span> <span data-ttu-id="5e5ce-166">如果事件記錄服務中正在報告遺失的事件，這可能表示事件記錄檔服務的設定有問題。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-166">If the missing events are being reported in the Event Log Service, this may indicate a problem with the configuration of the Event Log service.</span></span> <span data-ttu-id="5e5ce-167">使用者可能會有有限的功能，可增加事件記錄檔服務所要使用的最大磁碟空間，這可能會減少遺失的事件數目。</span><span class="sxs-lookup"><span data-stu-id="5e5ce-167">The user may have some limited ability to increase the maximum disk space to be used by the Event Log Service which may reduce the number of missing events.</span></span>

 

 
