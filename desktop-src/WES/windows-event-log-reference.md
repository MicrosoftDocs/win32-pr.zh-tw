---
title: Windows 事件記錄檔參考
description: 以下是您用來建立檢測資訊清單、從提供者使用的資訊清單建立資源、在執行時間取得檢測中繼資料，以及從通道和記錄檔查詢事件的程式設計項目
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025853"
---
# <a name="windows-event-log-reference"></a><span data-ttu-id="2b105-103">Windows 事件記錄檔參考</span><span class="sxs-lookup"><span data-stu-id="2b105-103">Windows Event Log Reference</span></span>

<span data-ttu-id="2b105-104">以下是您用來建立檢測資訊清單、從提供者使用的資訊清單建立資源、在執行時間取得檢測中繼資料，以及從通道和記錄檔查詢事件的程式設計項目：</span><span class="sxs-lookup"><span data-stu-id="2b105-104">The following are the programming elements that you use to create an instrumentation manifest, create resources from the manifest that your provider uses, get instrumentation metadata at run time, and query events from channels and log files:</span></span>

-   [<span data-ttu-id="2b105-105">EventManifest 架構</span><span class="sxs-lookup"><span data-stu-id="2b105-105">EventManifest Schema</span></span>](eventmanifestschema-schema.md)
-   [<span data-ttu-id="2b105-106">事件架構</span><span class="sxs-lookup"><span data-stu-id="2b105-106">Event Schema</span></span>](eventschema-schema.md)
-   [<span data-ttu-id="2b105-107">查詢架構</span><span class="sxs-lookup"><span data-stu-id="2b105-107">Query Schema</span></span>](queryschema-schema.md)
-   [<span data-ttu-id="2b105-108">Windows 事件記錄檔常數</span><span class="sxs-lookup"><span data-stu-id="2b105-108">Windows Event Log Constants</span></span>](windows-event-log-constants.md)
-   [<span data-ttu-id="2b105-109">Windows 事件記錄檔資料類型</span><span class="sxs-lookup"><span data-stu-id="2b105-109">Windows Event Log Data Types</span></span>](windows-event-log-data-types.md)
-   [<span data-ttu-id="2b105-110">Windows 事件記錄檔列舉</span><span class="sxs-lookup"><span data-stu-id="2b105-110">Windows Event Log Enumerations</span></span>](windows-event-log-enumerations.md)
-   [<span data-ttu-id="2b105-111">Windows 事件記錄檔函數</span><span class="sxs-lookup"><span data-stu-id="2b105-111">Windows Event Log Functions</span></span>](windows-event-log-functions.md)
-   [<span data-ttu-id="2b105-112">Windows 事件記錄檔結構</span><span class="sxs-lookup"><span data-stu-id="2b105-112">Windows Event Log Structures</span></span>](windows-event-log-structures.md)
-   [<span data-ttu-id="2b105-113">Windows 事件記錄檔工具</span><span class="sxs-lookup"><span data-stu-id="2b105-113">Windows Event Log Tools</span></span>](windows-event-log-tools.md)

<span data-ttu-id="2b105-114">針對使用 .NET 語言（例如 c # 或 Visual Basic）撰寫的應用程式，請參閱下列命名空間：</span><span class="sxs-lookup"><span data-stu-id="2b105-114">For applications written using a .NET language, such as C# or Visual Basic, see the following namespaces:</span></span>

-   <span data-ttu-id="2b105-115">若要寫入事件，請 [使用在 system.string 命名空間](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) 中定義的類別和方法。</span><span class="sxs-lookup"><span data-stu-id="2b105-115">To write events, use the classes and methods defined in the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace.</span></span>
-   <span data-ttu-id="2b105-116">若要使用 Windows 事件記錄檔通道或記錄檔中的事件，請使用在中定義 [的類別](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) 和方法。</span><span class="sxs-lookup"><span data-stu-id="2b105-116">To consume events from a Windows Event Log channel or log, use the classes and methods defined in the [System.Diagnostics.Eventing.Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.</span></span>

<span data-ttu-id="2b105-117">除了使用 [system.servicemodel 命名空間](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) 來寫入事件之外，您還可以使用 **-cs** 或 **-css** 引數，讓訊息編譯器產生程式碼來寫入事件。</span><span class="sxs-lookup"><span data-stu-id="2b105-117">As an alternative to using the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace to write events, you can use the **-cs** or **-css** argument to have the message compiler generate the code to write the events.</span></span> <span data-ttu-id="2b105-118">如需詳細資訊，請參閱 [**訊息編譯器**](message-compiler--mc-exe-.md)。</span><span class="sxs-lookup"><span data-stu-id="2b105-118">For details, see [**Message Compiler**](message-compiler--mc-exe-.md).</span></span>
