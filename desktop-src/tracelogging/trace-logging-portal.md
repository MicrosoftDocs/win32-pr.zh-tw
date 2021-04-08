---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103683944"
---
# <a name="tracelogging"></a><span data-ttu-id="eb64a-103">TraceLogging</span><span class="sxs-lookup"><span data-stu-id="eb64a-103">TraceLogging</span></span>

## <a name="purpose"></a><span data-ttu-id="eb64a-104">目的</span><span class="sxs-lookup"><span data-stu-id="eb64a-104">Purpose</span></span>

<span data-ttu-id="eb64a-105">TraceLogging 是新的 Windows 10 事件追蹤架構，適用于使用者模式應用程式和核心模式驅動程式。</span><span class="sxs-lookup"><span data-stu-id="eb64a-105">TraceLogging is the new Windows 10 event tracing framework for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="eb64a-106">TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。</span><span class="sxs-lookup"><span data-stu-id="eb64a-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eb64a-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="eb64a-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb64a-108">主題</span><span class="sxs-lookup"><span data-stu-id="eb64a-108">Topic</span></span></th>
<th><span data-ttu-id="eb64a-109">描述</span><span class="sxs-lookup"><span data-stu-id="eb64a-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb64a-110"><a href="trace-logging-about.md">關於 TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="eb64a-110"><a href="trace-logging-about.md">About TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="eb64a-111">TraceLogging 是使用者模式應用程式和核心模式驅動程式的新 Windows 10 事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="eb64a-111">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="eb64a-112">TraceLogging 是適用于 Windows (ETW) 之自我描述事件追蹤的格式。</span><span class="sxs-lookup"><span data-stu-id="eb64a-112">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="eb64a-113">TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。</span><span class="sxs-lookup"><span data-stu-id="eb64a-113">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb64a-114"><a href="tracelogging-using-tracelogging.md">使用 TraceLogging</a></span><span class="sxs-lookup"><span data-stu-id="eb64a-114"><a href="tracelogging-using-tracelogging.md">Using TraceLogging</a></span></span><br/></td>
<td><span data-ttu-id="eb64a-115">下列主題提供原生和 managed 程式碼的 TraceLogging 快速入門，以及範例。</span><span class="sxs-lookup"><span data-stu-id="eb64a-115">The following topics provide a TraceLogging quick start for native and managed code, with examples.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb64a-116"><a href="trace-logging-reference.md">TraceLogging 參考</a></span><span class="sxs-lookup"><span data-stu-id="eb64a-116"><a href="trace-logging-reference.md">TraceLogging Reference</a></span></span><br/></td>
<td><span data-ttu-id="eb64a-117">下列主題提供有關原生 TraceLogging API 的資訊。</span><span class="sxs-lookup"><span data-stu-id="eb64a-117">The following topics provide information about the native TraceLogging API.</span></span><br/> <span data-ttu-id="eb64a-118">TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。</span><span class="sxs-lookup"><span data-stu-id="eb64a-118">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="eb64a-119">TraceLogging 可讓您包含事件的結構化資料、使事件相互關聯，而且不需要個別的檢測資訊清單 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="eb64a-119">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span><br/> <span data-ttu-id="eb64a-120"><span class="underline">適用于 WinRT 開發人員</span></span><span class="sxs-lookup"><span data-stu-id="eb64a-120"><span class="underline">For WinRT developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="eb64a-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> 已在 Windows 10 中擴充，可記錄自我描述 WINDOWS (ETW) 事件的事件追蹤，而不需要資訊清單。</span><span class="sxs-lookup"><span data-stu-id="eb64a-121"><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span></li>
<li><span data-ttu-id="eb64a-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> 已在 Windows 10 中擴充，以提供活動開始和停止方法，這些方法可讓您控制開始和停止事件的格式和內容。</span><span class="sxs-lookup"><span data-stu-id="eb64a-122"><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="eb64a-123">此外，也可以嵌套活動。</span><span class="sxs-lookup"><span data-stu-id="eb64a-123">Additionally, activities can be nested.</span></span></li>
</ul><span data-ttu-id="eb64a-124">
<span class="underline">針對 managed 程式碼 (Microsoft .NET Framework) 開發人員</span></span><span class="sxs-lookup"><span data-stu-id="eb64a-124">
<span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="eb64a-125">舊版 .NET Framework 隨附的 <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> 類別已支援寫入 ETW 事件，而不需要資訊清單。</span><span class="sxs-lookup"><span data-stu-id="eb64a-125">The <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="eb64a-126">不過，開發人員必須使用 EventSource 作為基類，並將屬性和方法新增至已自動轉換成 ETW 資訊清單的衍生類別。</span><span class="sxs-lookup"><span data-stu-id="eb64a-126">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="eb64a-127">現在，開發人員不需要從 EventSource 衍生，而可以改為直接使用 EventSource 來記錄不需要資訊清單的自我描述事件。</span><span class="sxs-lookup"><span data-stu-id="eb64a-127">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span></li>
</ul><span data-ttu-id="eb64a-128">
<span class="underline">適用于 C/c + + 開發人員</span></span><span class="sxs-lookup"><span data-stu-id="eb64a-128">
<span class="underline">For C/C++ developers</span></span></span><br/>
<ul>
<li><span data-ttu-id="eb64a-129">TraceLoggingProvider 是在使用者或核心模式中，適用于 C/c + + 開發人員的建議 API。</span><span class="sxs-lookup"><span data-stu-id="eb64a-129">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="eb64a-130">這個 API 並不適合用於動態 (腳本) 案例（例如 JAVAscript）。</span><span class="sxs-lookup"><span data-stu-id="eb64a-130">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="eb64a-131">下列連結說明 C/c + + API。</span><span class="sxs-lookup"><span data-stu-id="eb64a-131">The following links describe the C/C++ API.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a><span data-ttu-id="eb64a-132">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="eb64a-132">Developer audience</span></span>

<span data-ttu-id="eb64a-133">TraceLogging 的設計目的是要讓使用者模式應用程式開發人員以及想要在程式碼中加入追蹤的核心模式驅動程式開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="eb64a-133">TraceLogging is designed for use by user-mode application developers and kernel-mode driver developers who want to add tracing to their code.</span></span>

