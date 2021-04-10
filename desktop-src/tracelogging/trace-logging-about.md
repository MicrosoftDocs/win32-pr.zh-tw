---
title: 關於 TraceLogging
description: TraceLogging 是使用者模式應用程式和核心模式驅動程式的新 Windows 10 事件追蹤。
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c2b1ca72385a51df1e0cd82f3e91c198f15b5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842412"
---
# <a name="about-tracelogging"></a><span data-ttu-id="87c55-103">關於 TraceLogging</span><span class="sxs-lookup"><span data-stu-id="87c55-103">About TraceLogging</span></span>

<span data-ttu-id="87c55-104">TraceLogging 是使用者模式應用程式和核心模式驅動程式的新 Windows 10 事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="87c55-104">TraceLogging is the new Windows 10 event tracing for user-mode applications and kernel-mode drivers.</span></span> <span data-ttu-id="87c55-105">TraceLogging 是適用于 Windows (ETW) 之自我描述事件追蹤的格式。</span><span class="sxs-lookup"><span data-stu-id="87c55-105">TraceLogging is a format for self-describing Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="87c55-106">TraceLogging 適用于 Windows (ETW) 的事件追蹤，並提供更簡單的方式來檢測程式碼。</span><span class="sxs-lookup"><span data-stu-id="87c55-106">TraceLogging builds on Event Tracing for Windows (ETW) and provides a simplified way to instrument code.</span></span>

<span data-ttu-id="87c55-107">TraceLogging 為 Windows 軟體追蹤預處理器 (的 WPP) 提供簡單的增強功能，可讓您將具有事件的結構化資料包括在內、使事件相互關聯的功能，以及全都不需要個別的檢測資訊清單 XML 檔案。</span><span class="sxs-lookup"><span data-stu-id="87c55-107">TraceLogging offers the simplicity of Windows software trace preprocessor (WPP) with the added benefit of being able to include structured data with events, the capability of correlating events, and all without requiring a separate instrumentation manifest XML file.</span></span> <span data-ttu-id="87c55-108">事件是自我描述的，表示包含檢測資訊清單的二進位檔不需要在系統上註冊，就能使用追蹤資料協助程式 (TDH) Api 來解碼和顯示事件。</span><span class="sxs-lookup"><span data-stu-id="87c55-108">Events are self-describing which means that a binary containing the instrumentation manifest does not need to be registered on the system in order to use the Trace Data Helper (TDH) APIs to decode and show events.</span></span>

<span data-ttu-id="87c55-109">Windows 的事件追蹤 (ETW) 是在 windows 2000 中引進，並在 Windows Vista 中更新。</span><span class="sxs-lookup"><span data-stu-id="87c55-109">Event Tracing for Windows (ETW) was introduced with Windows 2000 and updated in Windows Vista.</span></span> <span data-ttu-id="87c55-110">Tracelogging 建置於 Windows Vista ETW Api 之上。</span><span class="sxs-lookup"><span data-stu-id="87c55-110">Tracelogging builds on top of the Windows Vista ETW APIs.</span></span> <span data-ttu-id="87c55-111">提供者可以使用 TraceLogging 技術，但仍可在 Windows Vista 上運作。</span><span class="sxs-lookup"><span data-stu-id="87c55-111">Providers can use the TraceLogging technology and still work on Windows Vista.</span></span> <span data-ttu-id="87c55-112">使用 Windows VistaAPIs) 的現有控制器 (可以用來控制 TraceLogging 提供者。</span><span class="sxs-lookup"><span data-stu-id="87c55-112">Existing controllers (using Windows VistaAPIs) can be used to control TraceLogging providers.</span></span>

<span data-ttu-id="87c55-113">TraceLogging 也與現有的工具相容。</span><span class="sxs-lookup"><span data-stu-id="87c55-113">TraceLogging is also compatible with existing tools.</span></span> <span data-ttu-id="87c55-114">仍支援使用以資訊清單為基礎之 ETW 的提供者。</span><span class="sxs-lookup"><span data-stu-id="87c55-114">Providers that use manifest-based ETW are still supported.</span></span> <span data-ttu-id="87c55-115">除非您想要利用 TraceLogging 提供的簡易性，否則您不需要將資訊清單型 ETW 提供者轉換為 TraceLogging 提供者。</span><span class="sxs-lookup"><span data-stu-id="87c55-115">You do not need to convert manifest based ETW providers to TraceLogging providers unless you wish to take advantage of the simplicity that TraceLogging provides.</span></span> <span data-ttu-id="87c55-116">也支援 WPP 追蹤。</span><span class="sxs-lookup"><span data-stu-id="87c55-116">WPP tracing is also still supported.</span></span>

<span data-ttu-id="87c55-117">TraceLogging 是以 ETW 為基礎，但引進了幾項重要的改進：</span><span class="sxs-lookup"><span data-stu-id="87c55-117">TraceLogging builds upon ETW but introduces several important improvements:</span></span>

-   <span data-ttu-id="87c55-118">追蹤事件就像 API 呼叫一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="87c55-118">Tracing an event is as simple as an API call.</span></span>
-   <span data-ttu-id="87c55-119">事件是自我描述的，且不需要包含已編譯事件資訊清單的任何其他二進位檔來解讀事件。</span><span class="sxs-lookup"><span data-stu-id="87c55-119">Events are self-describing and do not require any additional binaries containing the compiled event manifest to interpret the event.</span></span> <span data-ttu-id="87c55-120">事件中會記錄有關事件的所有中繼資料。</span><span class="sxs-lookup"><span data-stu-id="87c55-120">All the metadata about the event is recorded in the event.</span></span>
-   <span data-ttu-id="87c55-121">您可以透過開始和停止事件輕鬆地表示單一進程內的活動。</span><span class="sxs-lookup"><span data-stu-id="87c55-121">Activities inside a single process can be easily expressed through start and stop events.</span></span>
-   <span data-ttu-id="87c55-122">TraceLogging 與現有的檢測支援相容。</span><span class="sxs-lookup"><span data-stu-id="87c55-122">TraceLogging is compatible with existing instrumentation support.</span></span> <span data-ttu-id="87c55-123">新的 ETW Api 會繼續支援舊的提供者。</span><span class="sxs-lookup"><span data-stu-id="87c55-123">The new ETW APIs continue to support the old providers.</span></span> <span data-ttu-id="87c55-124">您可以針對策略性案例投資新的 ETW Api，同時保留舊的檢測點。</span><span class="sxs-lookup"><span data-stu-id="87c55-124">You can invest in the new ETW APIs for strategic scenarios while leaving your old instrumentation points as they are.</span></span>
-   <span data-ttu-id="87c55-125">TraceLogging 為 Windows 10、Xbox One 和 Windows 10 行動裝置版提供相同的事件追蹤 API。</span><span class="sxs-lookup"><span data-stu-id="87c55-125">TraceLogging offers the same event tracing API for Windows 10, Xbox One, and Windows 10 Mobile.</span></span>
-   <span data-ttu-id="87c55-126">您可以從 C、c + +、.NET 和 Windows 執行階段存取 TraceLogging Api。</span><span class="sxs-lookup"><span data-stu-id="87c55-126">TraceLogging APIs are accessible from C, C++, .NET, and Windows Runtime.</span></span>

## <a name="api-high-level-overview"></a><span data-ttu-id="87c55-127">API 高層級總覽</span><span class="sxs-lookup"><span data-stu-id="87c55-127">API high-level overview</span></span>

<span data-ttu-id="87c55-128">有三個不同的 TraceLogging Api，以不同開發人員的物件為目標。</span><span class="sxs-lookup"><span data-stu-id="87c55-128">There are three separate TraceLogging APIs that target different developer audiences.</span></span> <span data-ttu-id="87c55-129">每個 API 的設計目的是為了符合該 API 目標物件的不同需求集合。</span><span class="sxs-lookup"><span data-stu-id="87c55-129">Each API was designed to meet different sets of requirements as appropriate for the target audience of that API.</span></span>

<span data-ttu-id="87c55-130">適用于 WinRT 開發人員：</span><span class="sxs-lookup"><span data-stu-id="87c55-130">For WinRT developers:</span></span>

-   <span data-ttu-id="87c55-131">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) 已在 Windows 10 中擴充，可記錄自我描述 WINDOWS (ETW) 事件的事件追蹤，而不需要資訊清單。</span><span class="sxs-lookup"><span data-stu-id="87c55-131">[**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) has been extended in Windows 10 to log self-describing Event Tracing for Windows (ETW) events without the need for a manifest.</span></span>
-   <span data-ttu-id="87c55-132">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) 已在 Windows 10 中擴充，以提供活動開始和停止方法，這些方法可讓您控制開始和停止事件的格式和內容。</span><span class="sxs-lookup"><span data-stu-id="87c55-132">[**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) has been extended in Windows 10 to provide activity start and stop methods that provide control over the format and contents of the Start and Stop events.</span></span> <span data-ttu-id="87c55-133">此外，也可以嵌套活動。</span><span class="sxs-lookup"><span data-stu-id="87c55-133">Additionally, activities can be nested.</span></span>

<span data-ttu-id="87c55-134">針對 C/c + + 開發人員：</span><span class="sxs-lookup"><span data-stu-id="87c55-134">For C/C++ developers:</span></span>

-   <span data-ttu-id="87c55-135">TraceLoggingProvider 包含最有效率的 API，不過，此 API 並不適合用於動態 (腳本) 案例（例如 JAVAscript）。</span><span class="sxs-lookup"><span data-stu-id="87c55-135">TraceLoggingProvider.h contains the most efficient API, however this API is not well suited for use in dynamic (scripted) scenarios such as Javascript.</span></span> <span data-ttu-id="87c55-136">此 API 可用於使用者模式和核心模式程式碼。</span><span class="sxs-lookup"><span data-stu-id="87c55-136">This API can be used in user-mode and kernel-mode code.</span></span>

<span data-ttu-id="87c55-137">針對 managed 程式碼 (Microsoft .NET Framework) 開發人員：</span><span class="sxs-lookup"><span data-stu-id="87c55-137">For managed code (Microsoft .NET Framework) developers:</span></span>

-   <span data-ttu-id="87c55-138">舊版 .NET Framework 隨附的 [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) 類別已支援寫入 ETW 事件-自動產生資訊清單，並將資訊清單內嵌至事件資料流程。</span><span class="sxs-lookup"><span data-stu-id="87c55-138">The [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) class that shipped with previous versions of the .NET Framework already supported writing ETW events - automatically generating the manifest and embedding the manifest into the event stream.</span></span> <span data-ttu-id="87c55-139">不過，開發人員仍必須追蹤資訊清單以將事件解碼 (除非是在支援內嵌資訊清單) 的情況下運作。</span><span class="sxs-lookup"><span data-stu-id="87c55-139">However, the developer still had to keep track of the manifest to decode the events (unless working in a scenario where the embedded manifest was supported).</span></span> <span data-ttu-id="87c55-140">TraceLogging 可讓您完全刪除資訊清單。</span><span class="sxs-lookup"><span data-stu-id="87c55-140">TraceLogging allows the manifest to be eliminated completely.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87c55-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="87c55-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87c55-142">關於事件追蹤</span><span class="sxs-lookup"><span data-stu-id="87c55-142">About Event Tracing</span></span>](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 