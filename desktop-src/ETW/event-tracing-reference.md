---
description: 列出與事件追蹤搭配使用的元素。
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: 事件追蹤參考
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973660"
---
# <a name="event-tracing-reference"></a><span data-ttu-id="ce512-103">事件追蹤參考</span><span class="sxs-lookup"><span data-stu-id="ce512-103">Event Tracing Reference</span></span>

<span data-ttu-id="ce512-104">您可以使用下列程式設計項目來撰寫應用程式，以併入事件追蹤：</span><span class="sxs-lookup"><span data-stu-id="ce512-104">You use the following programming elements to write applications that incorporate event tracing:</span></span>

-   [<span data-ttu-id="ce512-105">事件追蹤列舉</span><span class="sxs-lookup"><span data-stu-id="ce512-105">Event Tracing Enumerations</span></span>](/windows/desktop/api/_etw/#enumerations)
-   [<span data-ttu-id="ce512-106">事件追蹤函數</span><span class="sxs-lookup"><span data-stu-id="ce512-106">Event Tracing Functions</span></span>](/windows/desktop/api/_etw/#functions)
-   [<span data-ttu-id="ce512-107">事件追蹤介面</span><span class="sxs-lookup"><span data-stu-id="ce512-107">Event Tracing Interfaces</span></span>](/windows/desktop/api/_etw/#interfaces)
-   [<span data-ttu-id="ce512-108">事件追蹤結構</span><span class="sxs-lookup"><span data-stu-id="ce512-108">Event Tracing Structures</span></span>](/windows/desktop/api/_etw/#structures)
-   [<span data-ttu-id="ce512-109">事件追蹤常數</span><span class="sxs-lookup"><span data-stu-id="ce512-109">Event Tracing Constants</span></span>](event-tracing-constants.md)

<span data-ttu-id="ce512-110">如需使用這些程式設計項目的範例詳細資訊，請參閱 [事件追蹤範例](event-tracing-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="ce512-110">For details on samples that use these programming elements, see [Event Tracing Samples](event-tracing-samples.md).</span></span>

<span data-ttu-id="ce512-111">本節也包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="ce512-111">This section also contains information on:</span></span>

-   <span data-ttu-id="ce512-112">ETW 提供的[工具](event-tracing-tools.md)</span><span class="sxs-lookup"><span data-stu-id="ce512-112">[Tools](event-tracing-tools.md) that ETW provides</span></span>
-   <span data-ttu-id="ce512-113">核心事件的[MOF 類別定義](event-tracing-mof-classes.md)</span><span class="sxs-lookup"><span data-stu-id="ce512-113">[MOF class definitions](event-tracing-mof-classes.md) for kernel events</span></span>
-   <span data-ttu-id="ce512-114">定義事件類別時使用的[MOF 類別限定詞](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ce512-114">[MOF class qualifiers](event-tracing-mof-qualifiers.md) used when defining your event classes</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="ce512-115">在 .NET 程式碼中處理 ETW 追蹤</span><span class="sxs-lookup"><span data-stu-id="ce512-115">Process ETW traces in .NET code</span></span>

<span data-ttu-id="ce512-116">您也可以使用 [.Net TRACEPROCESSING API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) 來分析應用程式和其他軟體元件的 ETW 追蹤。</span><span class="sxs-lookup"><span data-stu-id="ce512-116">You can also use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="ce512-117">Microsoft 內部使用此 API 來分析產生 Windows 工程系統的 ETW 資料，而且它也可用來為 [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer)中的多個資料表加上電源。</span><span class="sxs-lookup"><span data-stu-id="ce512-117">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="ce512-118">此 API 會以 NuGet 套件的形式提供。</span><span class="sxs-lookup"><span data-stu-id="ce512-118">This API is available as a NuGet package.</span></span>

<span data-ttu-id="ce512-119">如需詳細資訊，請參閱[這篇文章](/windows/apps/trace-processing/overview)。</span><span class="sxs-lookup"><span data-stu-id="ce512-119">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>
