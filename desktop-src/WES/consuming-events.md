---
title: '使用事件 (Windows 事件記錄檔) '
description: 您可以使用通道或記錄檔中的事件。
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb3fb1b36a0cd4ecf836a8893bc1abc14e46451
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106976349"
---
# <a name="consuming-events-windows-event-log"></a><span data-ttu-id="1251e-103">使用事件 (Windows 事件記錄檔) </span><span class="sxs-lookup"><span data-stu-id="1251e-103">Consuming Events (Windows Event Log)</span></span>

<span data-ttu-id="1251e-104">您可以使用通道或記錄檔中的事件。</span><span class="sxs-lookup"><span data-stu-id="1251e-104">You can consume events from channels or from log files.</span></span> <span data-ttu-id="1251e-105">若要取用事件，您可以使用所有事件，也可以指定 XPath 運算式來識別您想要取用的事件。</span><span class="sxs-lookup"><span data-stu-id="1251e-105">To consume events, you can consume all events or you can specify an XPath expression that identifies the events that you want to consume.</span></span> <span data-ttu-id="1251e-106">若要判斷您可以在 XPath 運算式中使用之事件的元素和屬性，請參閱 [事件架構](eventschema-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="1251e-106">To determine the elements and attributes of an event that you can use in your XPath expression, see [Event Schema](eventschema-schema.md).</span></span>

<span data-ttu-id="1251e-107">Windows 事件記錄檔支援 XPath 1.0 的子集。</span><span class="sxs-lookup"><span data-stu-id="1251e-107">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="1251e-108">如需限制的詳細資訊，請參閱 [XPath 1.0 限制](#xpath-10-limitations)。</span><span class="sxs-lookup"><span data-stu-id="1251e-108">For details on the limitations, see [XPath 1.0 limitations](#xpath-10-limitations).</span></span>

<span data-ttu-id="1251e-109">下列範例顯示簡單的 XPath 運算式。</span><span class="sxs-lookup"><span data-stu-id="1251e-109">The following examples show simple XPath expressions.</span></span>


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



<span data-ttu-id="1251e-110">您可以直接在呼叫 [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) 或 [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) 函數時使用 XPath 運算式，也可以使用包含 XPath 運算式的結構化 XML 查詢。</span><span class="sxs-lookup"><span data-stu-id="1251e-110">You can use the XPath expressions directly when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions or you can use a structured XML query that contains the XPath expression.</span></span> <span data-ttu-id="1251e-111">針對從單一來源查詢事件的簡單查詢，使用 XPath 運算式是正常的。</span><span class="sxs-lookup"><span data-stu-id="1251e-111">For simple queries that query events from a single source, using an XPath expression is fine.</span></span> <span data-ttu-id="1251e-112">如果 XPath 運算式是包含20個以上運算式的複合運算式，或您要查詢來自多個來源的事件，則您必須使用結構化 XML 查詢。</span><span class="sxs-lookup"><span data-stu-id="1251e-112">If the XPath expression is a compound expression that contains more than 20 expressions or you are querying for events from multiple sources, then you must use a structured XML query.</span></span> <span data-ttu-id="1251e-113">如需結構化 XML 查詢之元素的詳細資訊，請參閱 [查詢架構](queryschema-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="1251e-113">For details on the elements of a structured XML query, see [Query Schema](queryschema-schema.md).</span></span>

<span data-ttu-id="1251e-114">結構化查詢會識別事件的來源，以及一或多個選取器或 suppressors。</span><span class="sxs-lookup"><span data-stu-id="1251e-114">A structured query identifies the source of the events and one or more selectors or suppressors.</span></span> <span data-ttu-id="1251e-115">選取器包含從來源選取事件的 XPath 運算式，而抑制器包含可防止選取事件的 XPath 運算式。</span><span class="sxs-lookup"><span data-stu-id="1251e-115">A selector contains an XPath expressions that selects events from the source and a suppressor contains an XPath expression that prevents events from being selected.</span></span> <span data-ttu-id="1251e-116">您可以從一個以上的來源選取事件。</span><span class="sxs-lookup"><span data-stu-id="1251e-116">You can select events from more than one source.</span></span> <span data-ttu-id="1251e-117">如果選取器和抑制器識別相同的事件，則事件不會包含在結果中。</span><span class="sxs-lookup"><span data-stu-id="1251e-117">If a selector and suppressor identify the same event, the event is not included in the result.</span></span>

<span data-ttu-id="1251e-118">下圖顯示指定一組選取器和 suppressors 的結構化 XML 查詢。</span><span class="sxs-lookup"><span data-stu-id="1251e-118">The following shows a structured XML query that specifies a set of selectors and suppressors.</span></span>


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



<span data-ttu-id="1251e-119">查詢的結果集不包含查詢時的事件快照集。</span><span class="sxs-lookup"><span data-stu-id="1251e-119">The result set from the query does not contain a snapshot of the events at the time of the query.</span></span> <span data-ttu-id="1251e-120">相反地，結果集會包含在查詢時所產生的事件，而且也會包含在您列舉結果時所引發符合查詢準則的所有新事件。</span><span class="sxs-lookup"><span data-stu-id="1251e-120">Instead, the result set includes the events at the time of the query and will also contain all new events that are raised that match the query criteria while you are enumerating the results.</span></span>

> [!Note]  
> <span data-ttu-id="1251e-121">事件的順序會保留給相同執行緒所寫入的事件。</span><span class="sxs-lookup"><span data-stu-id="1251e-121">The order of the events is preserved for events that are written by the same thread.</span></span> <span data-ttu-id="1251e-122">不過，在多處理器電腦的不同處理器上，由個別執行緒所撰寫的事件可能不會出現順序。</span><span class="sxs-lookup"><span data-stu-id="1251e-122">However, it is possible for events written by separate threads on different processors of a multiple processor computer to appear out of order.</span></span>

 

<span data-ttu-id="1251e-123">如需使用事件的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="1251e-123">For details on consuming events, see the following topics:</span></span>

-   [<span data-ttu-id="1251e-124">查詢事件</span><span class="sxs-lookup"><span data-stu-id="1251e-124">Querying for Events</span></span>](querying-for-events.md)
-   [<span data-ttu-id="1251e-125">訂閱事件</span><span class="sxs-lookup"><span data-stu-id="1251e-125">Subscribing to Events</span></span>](subscribing-to-events.md)
-   [<span data-ttu-id="1251e-126">轉譯事件</span><span class="sxs-lookup"><span data-stu-id="1251e-126">Rendering Events</span></span>](rendering-events.md)
-   [<span data-ttu-id="1251e-127">格式化事件訊息</span><span class="sxs-lookup"><span data-stu-id="1251e-127">Formatting Event Messages</span></span>](formatting-event-messages.md)
-   [<span data-ttu-id="1251e-128">將事件加上書簽</span><span class="sxs-lookup"><span data-stu-id="1251e-128">Bookmarking Events</span></span>](bookmarking-events.md)

<span data-ttu-id="1251e-129">使用事件的標準終端使用者工具組括：</span><span class="sxs-lookup"><span data-stu-id="1251e-129">The standard end user tools for consuming event are:</span></span>

-   <span data-ttu-id="1251e-130">[事件檢視器](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="1251e-130">[Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))</span></span>
-   <span data-ttu-id="1251e-131">Windows PowerShell [new-winevent](/previous-versions//dd367894(v=technet.10)) 指令 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1251e-131">The Windows PowerShell [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) cmdlet</span></span>
-   [<span data-ttu-id="1251e-132">**WevtUtil**</span><span class="sxs-lookup"><span data-stu-id="1251e-132">**WevtUtil**</span></span>](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a><span data-ttu-id="1251e-133">XPath 1.0 限制</span><span class="sxs-lookup"><span data-stu-id="1251e-133">XPath 1.0 limitations</span></span>

<span data-ttu-id="1251e-134">Windows 事件記錄檔支援 XPath 1.0 的子集。</span><span class="sxs-lookup"><span data-stu-id="1251e-134">Windows Event Log supports a subset of XPath 1.0.</span></span> <span data-ttu-id="1251e-135">主要限制是，事件選取器只可以選取代表事件的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="1251e-135">The primary restriction is that only XML elements that represent events can be selected by an event selector.</span></span> <span data-ttu-id="1251e-136">未選取事件的 XPath 查詢無效。</span><span class="sxs-lookup"><span data-stu-id="1251e-136">An XPath query that does not select an event is not valid.</span></span> <span data-ttu-id="1251e-137">所有有效的選取器路徑都以 \* 或 "Event" 開頭。</span><span class="sxs-lookup"><span data-stu-id="1251e-137">All valid selector paths start with \* or "Event".</span></span> <span data-ttu-id="1251e-138">所有位置路徑都是在事件節點上運作，並且由一系列步驟組成。</span><span class="sxs-lookup"><span data-stu-id="1251e-138">All location paths operate on the event nodes and are composed of a series of steps.</span></span> <span data-ttu-id="1251e-139">每個步驟都是三個部分的結構：軸、節點測試與述詞。</span><span class="sxs-lookup"><span data-stu-id="1251e-139">Each step is a structure of three parts: the axis, node test, and predicate.</span></span> <span data-ttu-id="1251e-140">如需有關這些元件以及 XPath 1.0 的詳細資訊，請參閱 [XML 路徑語言 (XPath) ](https://www.w3.org/TR/xpath)。</span><span class="sxs-lookup"><span data-stu-id="1251e-140">For more information about these parts and about XPath 1.0, see [XML Path Language (XPath)](https://www.w3.org/TR/xpath).</span></span> <span data-ttu-id="1251e-141">Windows 事件記錄檔會在運算式上放置下列限制：</span><span class="sxs-lookup"><span data-stu-id="1251e-141">Windows Event Log places the following restrictions on the expression:</span></span>

-   <span data-ttu-id="1251e-142">軸：僅支援子 (預設) 和屬性 (以及其速記 "@" ) 軸。</span><span class="sxs-lookup"><span data-stu-id="1251e-142">Axis: Only the Child (default) and Attribute (and its shorthand "@") axis are supported.</span></span>
-   <span data-ttu-id="1251e-143">節點測試：僅支援節點名稱和 NCName 測試。</span><span class="sxs-lookup"><span data-stu-id="1251e-143">Node Tests: Only node names and NCName tests are supported.</span></span> <span data-ttu-id="1251e-144">支援 " \* " 字元（可選取任何字元）。</span><span class="sxs-lookup"><span data-stu-id="1251e-144">The "\*" character, which selects any character, is supported.</span></span>
-   <span data-ttu-id="1251e-145">述詞：如果位置路徑符合下列限制，則可接受任何有效的 XPath 運算式：</span><span class="sxs-lookup"><span data-stu-id="1251e-145">Predicates: Any valid XPath expression is acceptable if the location paths conform to the following restrictions:</span></span>
    -   <span data-ttu-id="1251e-146">支援標準運算子 **或**、 **AND**、=、！ =、<=、<、>=、> 和括弧。</span><span class="sxs-lookup"><span data-stu-id="1251e-146">Standard operators **OR**, **AND**, =, !=, <=, <, >=, >, and parentheses are supported.</span></span>
    -   <span data-ttu-id="1251e-147">不支援產生節點名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="1251e-147">Generating a string value for a node name is not supported.</span></span>
    -   <span data-ttu-id="1251e-148">不支援以反向順序進行評估。</span><span class="sxs-lookup"><span data-stu-id="1251e-148">Evaluation in reverse order is not supported.</span></span>
    -   <span data-ttu-id="1251e-149">不支援節點集。</span><span class="sxs-lookup"><span data-stu-id="1251e-149">Node sets are not supported.</span></span>
    -   <span data-ttu-id="1251e-150">不支援命名空間範圍設定。</span><span class="sxs-lookup"><span data-stu-id="1251e-150">Namespace scoping is not supported.</span></span>
    -   <span data-ttu-id="1251e-151">不支援命名空間、處理和批註節點。</span><span class="sxs-lookup"><span data-stu-id="1251e-151">Namespace, processing, and comment nodes are not supported.</span></span>
    -   <span data-ttu-id="1251e-152">不支援內容大小。</span><span class="sxs-lookup"><span data-stu-id="1251e-152">Context size is not supported.</span></span>
    -   <span data-ttu-id="1251e-153">不支援變數系結。</span><span class="sxs-lookup"><span data-stu-id="1251e-153">Variable bindings are not supported.</span></span>
    -   <span data-ttu-id="1251e-154">只有) 才支援 position 函式和其速記陣列參考 (于分葉節點上。</span><span class="sxs-lookup"><span data-stu-id="1251e-154">The position function, and its shorthand array reference, is supported (on leaf nodes only).</span></span>
    -   <span data-ttu-id="1251e-155">支援頻外函數。</span><span class="sxs-lookup"><span data-stu-id="1251e-155">The Band function is supported.</span></span> <span data-ttu-id="1251e-156">函數會針對兩個整數數位引數執行位 AND。</span><span class="sxs-lookup"><span data-stu-id="1251e-156">The function performs a bitwise AND for two integer number arguments.</span></span> <span data-ttu-id="1251e-157">如果位 AND 的結果為非零值，則函數會評估為 true;否則，函數會評估為 false。</span><span class="sxs-lookup"><span data-stu-id="1251e-157">If the result of the bitwise AND is nonzero, the function evaluates to true; otherwise, the function evaluates to false.</span></span>
    -   <span data-ttu-id="1251e-158">支援 timediff 函數。</span><span class="sxs-lookup"><span data-stu-id="1251e-158">The timediff function is supported.</span></span> <span data-ttu-id="1251e-159">函數會計算第二個引數與第一個引數之間的差異。</span><span class="sxs-lookup"><span data-stu-id="1251e-159">The function computes the difference between the second argument and the first argument.</span></span> <span data-ttu-id="1251e-160">其中一個引數必須是常值。</span><span class="sxs-lookup"><span data-stu-id="1251e-160">One of the arguments must be a literal number.</span></span> <span data-ttu-id="1251e-161">引數必須使用 FILETIME 標記法。</span><span class="sxs-lookup"><span data-stu-id="1251e-161">The arguments must use FILETIME representation.</span></span> <span data-ttu-id="1251e-162">結果是兩次之間的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="1251e-162">The result is the number of milliseconds between the two times.</span></span> <span data-ttu-id="1251e-163">如果第二個引數代表較晚的時間，則結果為正數;否則，它會是負數。</span><span class="sxs-lookup"><span data-stu-id="1251e-163">The result is positive if the second argument represents a later time; otherwise, it is negative.</span></span> <span data-ttu-id="1251e-164">如果未提供第二個引數，則會使用目前的系統時間。</span><span class="sxs-lookup"><span data-stu-id="1251e-164">When the second argument is not provided, the current system time is used.</span></span>

 

 
