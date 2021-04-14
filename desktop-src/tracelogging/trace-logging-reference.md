---
title: TraceLogging 參考
description: 下列主題提供有關原生 TraceLogging API 的資訊。TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。
ms.assetid: 9E3F2140-DDB0-4C30-B7D0-A81F11823AA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d81874e7aeb1a0618716b00d225d215c382ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382709"
---
# <a name="tracelogging-reference"></a><span data-ttu-id="dc000-103">TraceLogging 參考</span><span class="sxs-lookup"><span data-stu-id="dc000-103">TraceLogging Reference</span></span>

<span data-ttu-id="dc000-104">下列主題提供有關原生 TraceLogging API 的資訊。</span><span class="sxs-lookup"><span data-stu-id="dc000-104">The following topics provide information about the native TraceLogging API.</span></span>

<span data-ttu-id="dc000-105">TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。</span><span class="sxs-lookup"><span data-stu-id="dc000-105">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span> <span data-ttu-id="dc000-106">TraceLogging 可讓您包含事件的結構化資料、使事件相互關聯，而且不需要個別的檢測資訊清單 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="dc000-106">TraceLogging allows you to include structured data with events, correlate events, and does not require a separate instrumentation manifest XML file.</span></span>

<span data-ttu-id="dc000-107"><span class="underline">適用于 WinRT 開發人員</span></span><span class="sxs-lookup"><span data-stu-id="dc000-107"><span class="underline">For WinRT developers</span></span></span>

-   <span data-ttu-id="dc000-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) 已在 Windows 10 中擴充，可記錄自我描述 WINDOWS (ETW) 事件的事件追蹤，而不需要資訊清單。</span><span class="sxs-lookup"><span data-stu-id="dc000-108">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span>
-   <span data-ttu-id="dc000-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) 已在 Windows 10 中擴充，以提供活動開始和停止方法，這些方法可讓您控制開始和停止事件的格式和內容。</span><span class="sxs-lookup"><span data-stu-id="dc000-109">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="dc000-110">此外，也可以嵌套活動。</span><span class="sxs-lookup"><span data-stu-id="dc000-110">Additionally, activities can be nested.</span></span>

<span data-ttu-id="dc000-111"><span class="underline">針對 managed 程式碼 (Microsoft .NET Framework) 開發人員</span></span><span class="sxs-lookup"><span data-stu-id="dc000-111"><span class="underline">For managed code (Microsoft .NET Framework) developers</span></span></span>

-   <span data-ttu-id="dc000-112">舊版 .NET Framework 隨附的 [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) 類別已支援寫入 ETW 事件，而不需要資訊清單。</span><span class="sxs-lookup"><span data-stu-id="dc000-112">The [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) class that shipped with previous versions of the .NET Framework already supports writing ETW events without the need for a manifest.</span></span> <span data-ttu-id="dc000-113">不過，開發人員必須使用 EventSource 作為基類，並將屬性和方法新增至已自動轉換成 ETW 資訊清單的衍生類別。</span><span class="sxs-lookup"><span data-stu-id="dc000-113">However, developers were required to use EventSource as a base class and add attributes and methods to the derived class that were turned into an ETW manifest automatically.</span></span> <span data-ttu-id="dc000-114">現在，開發人員不需要從 EventSource 衍生，而可以改為直接使用 EventSource 來記錄不需要資訊清單的自我描述事件。</span><span class="sxs-lookup"><span data-stu-id="dc000-114">Now, developers do not have to derive from EventSource and can instead use EventSource directly to log self-describing events that do not require a manifest.</span></span>

<span data-ttu-id="dc000-115"><span class="underline">適用于 C/c + + 開發人員</span></span><span class="sxs-lookup"><span data-stu-id="dc000-115"><span class="underline">For C/C++ developers</span></span></span>

-   <span data-ttu-id="dc000-116">TraceLoggingProvider 是在使用者或核心模式中，適用于 C/c + + 開發人員的建議 API。</span><span class="sxs-lookup"><span data-stu-id="dc000-116">TraceLoggingProvider.h is the recommended API for C/C++ developers in user or kernel mode.</span></span> <span data-ttu-id="dc000-117">這個 API 並不適合用於動態 (腳本) 案例（例如 JAVAscript）。</span><span class="sxs-lookup"><span data-stu-id="dc000-117">This API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="dc000-118">下列連結說明 C/c + + API。</span><span class="sxs-lookup"><span data-stu-id="dc000-118">The following links describe the C/C++ API.</span></span>

<!-- -->

-   [<span data-ttu-id="dc000-119">類別</span><span class="sxs-lookup"><span data-stu-id="dc000-119">Classes</span></span>](trace-logging-classes.md)
-   [<span data-ttu-id="dc000-120">函數</span><span class="sxs-lookup"><span data-stu-id="dc000-120">Functions</span></span>](trace-logging-functions.md)
-   [<span data-ttu-id="dc000-121">巨集</span><span class="sxs-lookup"><span data-stu-id="dc000-121">Macros</span></span>](trace-logging-macros.md)

<span data-ttu-id="dc000-122">請注意，WINVER 的值會影響 TraceLoggingProvider 的運作方式。</span><span class="sxs-lookup"><span data-stu-id="dc000-122">Note that the value of WINVER will impact the way TraceLoggingProvider.h behaves.</span></span>

-   <span data-ttu-id="dc000-123">如果在包含 <的> 之前未設定 WINVER，則 <windows .h> 會將 WINVER 設定為對應至 SDK 版本的預設值。</span><span class="sxs-lookup"><span data-stu-id="dc000-123">If WINVER is not set before including <windows.h>, then <windows.h> will set WINVER to a default value corresponding to the SDK version.</span></span>
-   <span data-ttu-id="dc000-124">使用 TraceLoggingProvider 將 WINVER 設為 0x0602 (Windows 8) 或更高版本時，程式將不會在 Windows Vista 或 Windows 7 上執行。</span><span class="sxs-lookup"><span data-stu-id="dc000-124">Using TraceLoggingProvider.h with WINVER set to 0x0602 (Windows 8) or higher, the program will not run on Windows Vista or Windows 7.</span></span>
-   <span data-ttu-id="dc000-125">使用 TraceLoggingProvider 將 WINVER 設為 0x0600 (Windows Vista) 或 0x0601 (Windows 7) 時，程式將會設定為相容性，並可在指定的 Windows 版本上運作。</span><span class="sxs-lookup"><span data-stu-id="dc000-125">Using TraceLoggingProvider.h with WINVER set to 0x0600 (Windows Vista) or 0x0601 (Windows 7), the program will be configured for compatibility and will work on the specified versions of Windows.</span></span>

 

 