---
description: SystemTraceProvider 是一種核心提供者，具有 Windows 7、Windows Server 2008 R2 和更新版本支援的一組預先定義核心事件。
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: 設定並啟動 SystemTraceProvider 會話
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386738"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="d7f41-103">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="d7f41-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="d7f41-104">SystemTraceProvider 是一種核心提供者，具有 Windows 7、Windows Server 2008 R2 和更新版本支援的一組預先定義核心事件。</span><span class="sxs-lookup"><span data-stu-id="d7f41-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="d7f41-105">在 Windows 7 和 Windows Server 2008 R2 上，SystemTraceProvider 只能用於 NT Kernel 記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="d7f41-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="d7f41-106">在 Windows 8、Windows Server 2012 和更新版本上，SystemTraceProvider 最多可多工記錄，最多8個記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="d7f41-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="d7f41-107">記錄器會話的前兩個位置是保留給 NT 核心記錄器和圓形核心內容記錄器。</span><span class="sxs-lookup"><span data-stu-id="d7f41-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="d7f41-108">如需使用 NT Kernel 記錄器會話作為追蹤提供者的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="d7f41-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="d7f41-109">在 Windows 10 SDK 組建20348和更新版本上，您可以透過個別的系統提供者來設定 SystemTraceProvider，這些提供者可以使用 [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) （例如 Windows 事件提供者的標準事件追蹤）來控制。</span><span class="sxs-lookup"><span data-stu-id="d7f41-109">On Windows 10 SDK build 20348 and later, the SystemTraceProvider can be configured via separate System Providers, which can be controlled with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) like standard Event Tracing for Windows event providers.</span></span> <span data-ttu-id="d7f41-110">如需系統提供者、關鍵字以及對應的舊版旗標和群組的完整清單，請參閱 [系統提供者](system-providers.md)</span><span class="sxs-lookup"><span data-stu-id="d7f41-110">For a full list of system providers, keywords, and corresponding legacy flags and groups, see [System Providers](system-providers.md)</span></span>

## <a name="enable-a-systemtraceprovider-session"></a><span data-ttu-id="d7f41-111">啟用 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="d7f41-111">Enable a SystemTraceProvider session</span></span>

<span data-ttu-id="d7f41-112">若要讓 SystemTraceProvider 啟動 NT Kernel 記錄器以外的會話，請執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="d7f41-112">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command:</span></span>

<span data-ttu-id="d7f41-113">**tracelog.exe-start MySession-f c： \\ Kernel1 .etl-EFLAG PROC \_ THREAD + LOADER + CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="d7f41-113">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="d7f41-114">若要以程式設計方式啟用 SystemTraceProvider 來啟動 NT Kernel 記錄器以外的會話，請使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="d7f41-114">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="d7f41-115">定義私用記錄器名稱。</span><span class="sxs-lookup"><span data-stu-id="d7f41-115">Define a private logger name.</span></span>

    <span data-ttu-id="d7f41-116">**\#定義私用 \_ 記錄器 \_ 名稱 L "部分私用追蹤會話"**</span><span class="sxs-lookup"><span data-stu-id="d7f41-116">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="d7f41-117">在控制器上，設定 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構的下列成員。</span><span class="sxs-lookup"><span data-stu-id="d7f41-117">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="d7f41-118">將 **LogFileMode** 設定為 **事件 \_ 追蹤 \_ 系統 \_ 記錄器 \_ 模式**。</span><span class="sxs-lookup"><span data-stu-id="d7f41-118">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="d7f41-119">將 **LoggerName** 設定為私用記錄器，而不是 **核心 \_ 記錄器 \_ 名稱**。</span><span class="sxs-lookup"><span data-stu-id="d7f41-119">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="d7f41-120">請確定 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **Wnode Guid** 成員未設定為 **SystemTraceControlGuid**。</span><span class="sxs-lookup"><span data-stu-id="d7f41-120">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="d7f41-121">您必須將新的 **GUID** 指派給這個成員。</span><span class="sxs-lookup"><span data-stu-id="d7f41-121">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="d7f41-122">在取用者上，將 [**事件 \_ 追蹤 \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea)記錄檔結構的 **LoggerName** 成員設定至此私用記錄器。</span><span class="sxs-lookup"><span data-stu-id="d7f41-122">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="d7f41-123">如果您想要讓非系統管理員或非 TCB 進程可以代表協力廠商應用程式使用 SystemTraceProvider 來啟動程式碼剖析追蹤會話，則您需要授與使用者設定檔許可權，然後將此使用者新增至為記錄器會話建立的會話 **GUID** () 和系統追蹤提供者 **GUID** ，以啟用系統追蹤提供者。</span><span class="sxs-lookup"><span data-stu-id="d7f41-123">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="d7f41-124">如需詳細資訊，請參閱 [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="d7f41-124">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d7f41-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="d7f41-125">Related topics</span></span>

[<span data-ttu-id="d7f41-126">設定和啟動私用記錄器會話</span><span class="sxs-lookup"><span data-stu-id="d7f41-126">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)

[<span data-ttu-id="d7f41-127">設定和啟動自動記錄器會話</span><span class="sxs-lookup"><span data-stu-id="d7f41-127">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)

[<span data-ttu-id="d7f41-128">設定和啟動事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="d7f41-128">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)

[<span data-ttu-id="d7f41-129">設定和啟動 NT Kernel 記錄器會話</span><span class="sxs-lookup"><span data-stu-id="d7f41-129">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)

[<span data-ttu-id="d7f41-130">系統提供者</span><span class="sxs-lookup"><span data-stu-id="d7f41-130">System Providers</span></span>](system-providers.md)

[<span data-ttu-id="d7f41-131">更新事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="d7f41-131">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)

 

 
