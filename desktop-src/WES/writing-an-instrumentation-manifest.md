---
title: 撰寫檢測資訊清單
description: 應用程式和 Dll 會使用檢測資訊清單來識別其檢測提供者和提供者寫入的事件。
ms.assetid: eec9d129-acde-4302-9121-634b3fad8455
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdad802526ad177eb5daa8846535c434fff32eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375389"
---
# <a name="writing-an-instrumentation-manifest"></a><span data-ttu-id="6ee80-103">撰寫檢測資訊清單</span><span class="sxs-lookup"><span data-stu-id="6ee80-103">Writing an Instrumentation Manifest</span></span>

<span data-ttu-id="6ee80-104">應用程式和 Dll 會使用檢測資訊清單來識別其檢測提供者和提供者寫入的事件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-104">Applications and DLLs use an instrumentation manifest to identify their instrumentation providers and the events that the providers write.</span></span> <span data-ttu-id="6ee80-105">資訊清單是 XML 檔案，其中包含識別提供者的元素。</span><span class="sxs-lookup"><span data-stu-id="6ee80-105">A manifest is an XML file that contains the elements that identify your provider.</span></span> <span data-ttu-id="6ee80-106">慣例是使用. man 做為您的資訊清單的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="6ee80-106">The convention is to use .man as the extension for your manifest.</span></span> <span data-ttu-id="6ee80-107">資訊清單必須符合事件資訊清單 XSD。</span><span class="sxs-lookup"><span data-stu-id="6ee80-107">The manifest must conform to the event manifest XSD.</span></span> <span data-ttu-id="6ee80-108">如需架構的詳細資訊，請參閱 [EventManifest 架構](eventmanifestschema-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="6ee80-108">For details on the schema, see [EventManifest Schema](eventmanifestschema-schema.md).</span></span>

<span data-ttu-id="6ee80-109">檢測提供者是呼叫 [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)、 [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring)或 [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) 函數的任何應用程式或 DLL，以將事件寫入 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) 追蹤會話或事件記錄檔通道。</span><span class="sxs-lookup"><span data-stu-id="6ee80-109">An instrumentation provider is any application or DLL that calls the [**EventWriteEx**](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex), [**EventWriteString**](/windows/desktop/api/evntprov/nf-evntprov-eventwritestring), or [**EventWriteTransfer**](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer) functions to write events to an [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) tracing session or an Event Log channel.</span></span> <span data-ttu-id="6ee80-110">應用程式可以定義單一檢測提供者來涵蓋它寫入的所有事件，或是定義應用程式的提供者，以及其每個 Dll 的提供者。</span><span class="sxs-lookup"><span data-stu-id="6ee80-110">An application can define a single instrumentation provider that covers all events that it writes or it can define a provider for the application and a provider for each of its DLLs.</span></span> <span data-ttu-id="6ee80-111">應用程式在資訊清單中定義的提供者數目，完全取決於應用程式要如何組織其所寫入的事件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-111">The number of providers that the application defines in the manifest depends solely on how the application wants to organize the events that it writes.</span></span>

<span data-ttu-id="6ee80-112">為每個 DLL 指定提供者的優點是，您接著可以啟用和停用個別提供者，以及它們所產生的事件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-112">The advantage of specifying a provider for each DLL is that you can then enable and disable the individual providers and thus the events that they generate.</span></span> <span data-ttu-id="6ee80-113">只有當 ETW 追蹤會話啟用提供者時，才適用這項優點。</span><span class="sxs-lookup"><span data-stu-id="6ee80-113">This advantage applies only if the provider is enabled by an ETW tracing session.</span></span> <span data-ttu-id="6ee80-114">指定事件記錄檔通道的任何事件一律會寫入至該通道。</span><span class="sxs-lookup"><span data-stu-id="6ee80-114">Any events that specify an event log channel are always written to that channel.</span></span>

<span data-ttu-id="6ee80-115">資訊清單必須識別提供者和它所寫入的事件，但其他中繼資料（例如通道、層級和關鍵字）是選擇性的;您是否要定義選擇性的中繼資料，取決於將取用事件的物件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-115">The manifest must identify the provider and the events that it writes but the other metadata such as channels, levels, and keywords are optional; whether you define the optional metadata depends on who will be consuming the events.</span></span> <span data-ttu-id="6ee80-116">例如，如果系統管理員或支援人員使用從事件記錄通道讀取事件的 Windows 事件檢視器之類的工具來取用事件，則您必須定義要寫入事件的通道。</span><span class="sxs-lookup"><span data-stu-id="6ee80-116">For example, if administrators or support personnel consume the events using a tool like the Windows Event Viewer that reads events from event log channels, then you must define the channels to which the events are written.</span></span> <span data-ttu-id="6ee80-117">不過，如果提供者只會由 ETW 追蹤會話啟用，則您不需要定義通道。</span><span class="sxs-lookup"><span data-stu-id="6ee80-117">However, if the provider will only be enabled by an ETW tracing session, then you do not need to define channels.</span></span>

<span data-ttu-id="6ee80-118">雖然層級、工作、opcode 和關鍵字中繼資料都是選擇性的，但您應該使用它們來以邏輯方式分組或區出事件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-118">Although the levels, tasks, opcodes, and keywords metadata are optional, you should use them to logically group or bucket the events.</span></span> <span data-ttu-id="6ee80-119">分組事件可協助取用者只取用感興趣的事件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-119">Grouping the events helps the consumers consume only those events that are of interest.</span></span> <span data-ttu-id="6ee80-120">例如，取用者可以查詢層級為「重大」且關鍵字為「寫入」的所有事件，或查詢特定工作所寫入的所有事件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-120">For example, the consumer could query for all events where level is "critical" and keyword is "write", or query for all events written by a specific task.</span></span>

<span data-ttu-id="6ee80-121">除了使用 level 和關鍵字來取用特定類型事件的取用者之外，ETW 追蹤會話還可以使用層級和關鍵字中繼資料來告訴 ETW，以限制寫入事件追蹤記錄檔的事件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-121">In addition to consumers using level and keywords to consume specific types of events, an ETW tracing session can use the level and keyword metadata to tell ETW to limit the events that are written to the event tracing log.</span></span> <span data-ttu-id="6ee80-122">例如，會話可能會將事件限制為只有層級為 "error" 或 "critical" 且關鍵字為 "read" 的事件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-122">For example, the session could limit the events to only events where level is "error" or "critical" and keyword is "read".</span></span>

<span data-ttu-id="6ee80-123">提供者可以定義篩選器，讓會話用來根據事件資料篩選事件。</span><span class="sxs-lookup"><span data-stu-id="6ee80-123">A provider can define filters that a session uses to filter the events based on event data.</span></span> <span data-ttu-id="6ee80-124">使用層級和關鍵字時，ETW 會判斷是否將事件寫入記錄檔，但使用篩選準則，提供者會使用篩選資料準則來判斷它是否會將事件寫入該會話。</span><span class="sxs-lookup"><span data-stu-id="6ee80-124">With level and keywords, ETW determines whether the event is written to the log but with filters, the provider uses the filter data criteria to determine whether it writes the event to that session.</span></span> <span data-ttu-id="6ee80-125">只有當 ETW 追蹤會話啟用您的提供者時，篩選才適用。</span><span class="sxs-lookup"><span data-stu-id="6ee80-125">The filters are applicable only when an ETW tracing session enables your provider.</span></span>

<span data-ttu-id="6ee80-126">下列各節說明如何定義資訊清單的元件：</span><span class="sxs-lookup"><span data-stu-id="6ee80-126">The following sections show how to define the components of the manifest:</span></span>

-   [<span data-ttu-id="6ee80-127">識別提供者</span><span class="sxs-lookup"><span data-stu-id="6ee80-127">Identifying the provider</span></span>](identifying-the-provider.md)
-   [<span data-ttu-id="6ee80-128">定義寫入事件的通道</span><span class="sxs-lookup"><span data-stu-id="6ee80-128">Defining the channels to where the events are written</span></span>](defining-channels.md)
-   [<span data-ttu-id="6ee80-129">定義提供者所寫入事件的嚴重性層級</span><span class="sxs-lookup"><span data-stu-id="6ee80-129">Defining the severity levels of events that the provider writes</span></span>](defining-severity-levels.md)
-   [<span data-ttu-id="6ee80-130">定義您的提供者所執行的工作和作業</span><span class="sxs-lookup"><span data-stu-id="6ee80-130">Defining the tasks and operations that your provider performs</span></span>](defining-tasks-and-opcodes.md)
-   [<span data-ttu-id="6ee80-131">定義分類提供者所寫入之事件的關鍵字</span><span class="sxs-lookup"><span data-stu-id="6ee80-131">Defining the keywords that classify the events that the provider writes</span></span>](defining-keywords-used-to-classify-types-of-events.md)
-   [<span data-ttu-id="6ee80-132">定義提供者用來篩選所寫入之事件的篩選準則</span><span class="sxs-lookup"><span data-stu-id="6ee80-132">Defining the filters that the provider uses to filter the events that it writes</span></span>](defining-filters.md)
-   [<span data-ttu-id="6ee80-133">定義您的範本資料參考的名稱/值對應</span><span class="sxs-lookup"><span data-stu-id="6ee80-133">Defining the name/value maps that your template data references</span></span>](defining-name-value-mappings.md)
-   [<span data-ttu-id="6ee80-134">定義定義事件特定資料的範本</span><span class="sxs-lookup"><span data-stu-id="6ee80-134">Defining the templates that define the event-specific data</span></span>](defining-event-data-templates.md)
-   [<span data-ttu-id="6ee80-135">定義提供者寫入的事件</span><span class="sxs-lookup"><span data-stu-id="6ee80-135">Defining the events that the provider writes</span></span>](defining-events.md)

<span data-ttu-id="6ee80-136">雖然您可以手動撰寫檢測資訊清單，但您應該考慮使用 Windows SDK Bin 資料夾中包含的 ECManGen.exe 工具 \\ 。</span><span class="sxs-lookup"><span data-stu-id="6ee80-136">Although you can author an instrumentation manifest manually, you should consider using the ECManGen.exe tool that is included in the \\Bin folder of the Windows SDK.</span></span> <span data-ttu-id="6ee80-137">ECManGen.exe 工具會使用 GUI，引導您從頭開始建立資訊清單，而不需要使用 XML 標記。</span><span class="sxs-lookup"><span data-stu-id="6ee80-137">The ECManGen.exe tool uses a GUI that guides you through creating a manifest from scratch without ever having to use XML tags.</span></span> <span data-ttu-id="6ee80-138">在使用此工具時，知道本節和 [EventManifest 架構](eventmanifestschema-schema.md) 區段中的資訊將有所説明。</span><span class="sxs-lookup"><span data-stu-id="6ee80-138">Having knowledge of the information in this section and in the [EventManifest Schema](eventmanifestschema-schema.md) section will help when using the tool.</span></span>

<span data-ttu-id="6ee80-139">如果您使用 Visual Studio 做為 XML 編輯器，則可以將 [EventManifest](eventmanifestschema-schema.md) 架構加入至專案 (請參閱 XML 功能表) 以利用 Intellisense、內嵌架構驗證及其他功能，讓您更輕鬆且精確地撰寫資訊清單。</span><span class="sxs-lookup"><span data-stu-id="6ee80-139">If you use Visual Studio as your XML editor, you can add the [EventManifest](eventmanifestschema-schema.md) schema to the project (see the XML menu) to take advantage of Intellisense, inline schema validation, and other features to make writing the manifest easy and accurate.</span></span>

<span data-ttu-id="6ee80-140">寫入資訊清單之後，請使用訊息編譯器來驗證資訊清單，並產生您在提供者中包含的資源和標頭檔。</span><span class="sxs-lookup"><span data-stu-id="6ee80-140">After writing your manifest, use the message compiler to validate the manifest and generate the resource and header files that you include in your provider.</span></span> <span data-ttu-id="6ee80-141">如需詳細資訊，請參閱 [編譯檢測資訊清單](compiling-an-instrumentation-manifest.md)。</span><span class="sxs-lookup"><span data-stu-id="6ee80-141">For more information, see [Compiling an Instrumentation Manifest](compiling-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="6ee80-142">下列範例顯示完整定義之事件資訊清單的基本架構。</span><span class="sxs-lookup"><span data-stu-id="6ee80-142">The following example shows the skeleton of a fully defined event manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChannel .../>
                    <channel .../>
                </channels>
                <levels>
                    <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



 

 