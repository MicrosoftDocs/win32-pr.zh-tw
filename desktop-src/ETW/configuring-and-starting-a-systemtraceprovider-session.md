---
description: SystemTraceProvider 是一種核心提供者，具有 Windows 7、Windows Server 2008 R2 和更新版本支援的一組預先定義核心事件。
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: 設定並啟動 SystemTraceProvider 會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972228"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="4d95f-103">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="4d95f-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="4d95f-104">SystemTraceProvider 是一種核心提供者，具有 Windows 7、Windows Server 2008 R2 和更新版本支援的一組預先定義核心事件。</span><span class="sxs-lookup"><span data-stu-id="4d95f-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="4d95f-105">在 Windows 7 和 Windows Server 2008 R2 上，SystemTraceProvider 只能用於 NT Kernel 記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="4d95f-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="4d95f-106">在 Windows 8、Windows Server 2012 和更新版本上，SystemTraceProvider 最多可多工記錄，最多8個記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="4d95f-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="4d95f-107">記錄器會話的前兩個位置是保留給 NT 核心記錄器和圓形核心內容記錄器。</span><span class="sxs-lookup"><span data-stu-id="4d95f-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="4d95f-108">如需使用 NT Kernel 記錄器會話作為追蹤提供者的詳細資訊，請參閱設定 [和啟動 Nt Kernel 記錄器會話](configuring-and-starting-the-nt-kernel-logger-session.md)。</span><span class="sxs-lookup"><span data-stu-id="4d95f-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="4d95f-109">若要讓 SystemTraceProvider 啟動 NT Kernel 記錄器以外的會話，請執行下列命令。</span><span class="sxs-lookup"><span data-stu-id="4d95f-109">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command.</span></span>

<span data-ttu-id="4d95f-110">**tracelog.exe-start MySession-f c： \\ Kernel1 .etl-EFLAG PROC \_ THREAD + LOADER + CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="4d95f-110">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="4d95f-111">若要以程式設計方式啟用 SystemTraceProvider 來啟動 NT Kernel 記錄器以外的會話，請使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="4d95f-111">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="4d95f-112">定義私用記錄器名稱。</span><span class="sxs-lookup"><span data-stu-id="4d95f-112">Define a private logger name.</span></span>

    <span data-ttu-id="4d95f-113">**\#定義私用 \_ 記錄器 \_ 名稱 L "部分私用追蹤會話"**</span><span class="sxs-lookup"><span data-stu-id="4d95f-113">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="4d95f-114">在控制器上，設定 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構的下列成員。</span><span class="sxs-lookup"><span data-stu-id="4d95f-114">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="4d95f-115">將 **LogFileMode** 設定為 **事件 \_ 追蹤 \_ 系統 \_ 記錄器 \_ 模式**。</span><span class="sxs-lookup"><span data-stu-id="4d95f-115">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="4d95f-116">將 **LoggerName** 設定為私用記錄器，而不是 **核心 \_ 記錄器 \_ 名稱**。</span><span class="sxs-lookup"><span data-stu-id="4d95f-116">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="4d95f-117">請確定 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **Wnode Guid** 成員未設定為 **SystemTraceControlGuid**。</span><span class="sxs-lookup"><span data-stu-id="4d95f-117">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="4d95f-118">您必須將新的 **GUID** 指派給這個成員。</span><span class="sxs-lookup"><span data-stu-id="4d95f-118">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="4d95f-119">在取用者上，將 [**事件 \_ 追蹤 \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea)記錄檔結構的 **LoggerName** 成員設定至此私用記錄器。</span><span class="sxs-lookup"><span data-stu-id="4d95f-119">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="4d95f-120">如果您想要讓非系統管理員或非 TCB 進程可以代表協力廠商應用程式使用 SystemTraceProvider 來啟動程式碼剖析追蹤會話，則您需要授與使用者設定檔許可權，然後將此使用者新增至為記錄器會話建立的會話 **GUID** () 和系統追蹤提供者 **GUID** ，以啟用系統追蹤提供者。</span><span class="sxs-lookup"><span data-stu-id="4d95f-120">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="4d95f-121">如需詳細資訊，請參閱 [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="4d95f-121">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4d95f-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d95f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d95f-123">設定和啟動私用記錄器會話</span><span class="sxs-lookup"><span data-stu-id="4d95f-123">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="4d95f-124">設定和啟動自動記錄器會話</span><span class="sxs-lookup"><span data-stu-id="4d95f-124">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="4d95f-125">設定和啟動事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="4d95f-125">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="4d95f-126">設定和啟動 NT Kernel 記錄器會話</span><span class="sxs-lookup"><span data-stu-id="4d95f-126">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="4d95f-127">更新事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="4d95f-127">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
