---
description: 本檔適用于想要使用 ETW 的使用者模式應用程式。 如需檢測以核心模式執行之設備磁碟機的相關資訊，請參閱 [WPP 軟體追蹤]，並將事件追蹤新增至 Windows 驅動程式套件 (WDK) 中 Kernel-Mode 的驅動程式。
ms.assetid: 3de69436-671b-46a2-8d92-4eb3af2a4233
title: 事件追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9802635fffddfea79c979534771605af13949d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320707"
---
# <a name="event-tracing"></a><span data-ttu-id="a2057-104">事件追蹤</span><span class="sxs-lookup"><span data-stu-id="a2057-104">Event Tracing</span></span>

## <a name="purpose"></a><span data-ttu-id="a2057-105">目的</span><span class="sxs-lookup"><span data-stu-id="a2057-105">Purpose</span></span>

<span data-ttu-id="a2057-106">Windows 事件追蹤 (ETW) 可讓應用程式設計人員能夠啟動和停止事件追蹤會話、檢測應用程式以提供追蹤事件，以及使用追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="a2057-106">Event Tracing for Windows (ETW) provides application programmers the ability to start and stop event tracing sessions, instrument an application to provide trace events, and consume trace events.</span></span> <span data-ttu-id="a2057-107">追蹤事件包含事件標頭和提供者定義的資料，可描述應用程式或作業的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a2057-107">Trace events contain an event header and provider-defined data that describes the current state of an application or operation.</span></span> <span data-ttu-id="a2057-108">您可以使用這些事件來對應用程式進行偵錯工具並執行容量和效能分析。</span><span class="sxs-lookup"><span data-stu-id="a2057-108">You can use the events to debug an application and perform capacity and performance analysis.</span></span>

<span data-ttu-id="a2057-109">本檔適用于想要使用 ETW 的使用者模式應用程式。</span><span class="sxs-lookup"><span data-stu-id="a2057-109">This documentation is for user-mode applications that want to use ETW.</span></span> <span data-ttu-id="a2057-110">如需檢測以核心模式執行之設備磁碟機的相關資訊，請參閱 [ [WPP 軟體追蹤](/windows-hardware/drivers/devtest/wpp-software-tracing) ]，並 [將事件追蹤新增至](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) Windows 驅動程式套件 (WDK) 中 Kernel-Mode 的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="a2057-110">For information about instrumenting device drivers that run in kernel mode, see [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Adding Event Tracing to Kernel-Mode Drivers](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-) in the Windows Driver Kit (WDK).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a2057-111">適用時</span><span class="sxs-lookup"><span data-stu-id="a2057-111">Where applicable</span></span>

<span data-ttu-id="a2057-112">當您想要檢測應用程式、將使用者或核心事件記錄至記錄檔，並使用記錄檔中的事件時，請使用 ETW。</span><span class="sxs-lookup"><span data-stu-id="a2057-112">Use ETW when you want to instrument your application, log user or kernel events to a log file, and consume events from a log file or in real time.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a2057-113">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="a2057-113">Developer audience</span></span>

<span data-ttu-id="a2057-114">ETW 是針對撰寫使用者模式應用程式的 C 和 c + + 開發人員所設計。</span><span class="sxs-lookup"><span data-stu-id="a2057-114">ETW is designed for C and C++ developers who write user-mode applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a2057-115">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="a2057-115">Run-time requirements</span></span>

<span data-ttu-id="a2057-116">ETW 包含在 Microsoft Windows 2000 和更新版本中。</span><span class="sxs-lookup"><span data-stu-id="a2057-116">ETW is included in Microsoft Windows 2000 and later.</span></span> <span data-ttu-id="a2057-117">如需哪些作業系統需要哪些作業系統才能使用特定功能的相關資訊，請參閱函式檔集的需求一節。</span><span class="sxs-lookup"><span data-stu-id="a2057-117">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="a2057-118">在 .NET 程式碼中處理 ETW 追蹤</span><span class="sxs-lookup"><span data-stu-id="a2057-118">Process ETW traces in .NET code</span></span>

<span data-ttu-id="a2057-119">您可以使用 [.Net TRACEPROCESSING API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) 來分析應用程式和其他軟體元件的 ETW 追蹤。</span><span class="sxs-lookup"><span data-stu-id="a2057-119">You can use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="a2057-120">Microsoft 內部使用此 API 來分析產生 Windows 工程系統的 ETW 資料，而且它也可用來為 [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer)中的多個資料表加上電源。</span><span class="sxs-lookup"><span data-stu-id="a2057-120">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="a2057-121">此 API 會以 NuGet 套件的形式提供。</span><span class="sxs-lookup"><span data-stu-id="a2057-121">This API is available as a NuGet package.</span></span>

<span data-ttu-id="a2057-122">如需詳細資訊，請參閱[這篇文章](/windows/apps/trace-processing/overview)。</span><span class="sxs-lookup"><span data-stu-id="a2057-122">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a2057-123">本節內容</span><span class="sxs-lookup"><span data-stu-id="a2057-123">In this section</span></span>



| <span data-ttu-id="a2057-124">主題</span><span class="sxs-lookup"><span data-stu-id="a2057-124">Topic</span></span>                                                                     | <span data-ttu-id="a2057-125">描述</span><span class="sxs-lookup"><span data-stu-id="a2057-125">Description</span></span>                                                                        |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2057-126">事件追蹤的新功能</span><span class="sxs-lookup"><span data-stu-id="a2057-126">What's New in Event Tracing</span></span>](what-s-new-in-event-tracing.md)<br/> | <span data-ttu-id="a2057-127">在每個版本中新增至事件追蹤的新功能。</span><span class="sxs-lookup"><span data-stu-id="a2057-127">New features that were added to Event Tracing in each release.</span></span><br/>          |
| [<span data-ttu-id="a2057-128">關於事件追蹤</span><span class="sxs-lookup"><span data-stu-id="a2057-128">About Event Tracing</span></span>](about-event-tracing.md)<br/>                 | <span data-ttu-id="a2057-129">事件追蹤的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="a2057-129">General information about Event Tracing.</span></span><br/>                                |
| [<span data-ttu-id="a2057-130">使用事件追蹤</span><span class="sxs-lookup"><span data-stu-id="a2057-130">Using Event Tracing</span></span>](using-event-tracing.md)<br/>                 | <span data-ttu-id="a2057-131">說明如何使用 ETW API 的工作相關主題。</span><span class="sxs-lookup"><span data-stu-id="a2057-131">Task-related topics that describe how to use the ETW API.</span></span><br/>               |
| [<span data-ttu-id="a2057-132">事件追蹤參考</span><span class="sxs-lookup"><span data-stu-id="a2057-132">Event Tracing Reference</span></span>](event-tracing-reference.md)<br/>         | <span data-ttu-id="a2057-133">ETW 函數和其他程式設計專案的詳細描述。</span><span class="sxs-lookup"><span data-stu-id="a2057-133">Detailed descriptions of ETW functions and other programming elements.</span></span> <br/> |



 

 

 
