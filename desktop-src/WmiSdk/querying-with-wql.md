---
description: WMI 查詢語言 (WQL) 是標準美國國家標準局結構化查詢語言 (SQL)  (ANSI SQL) 的子集，其中包含支援 WMI 的次要語義變更。
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: 使用 WQL 查詢
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971719"
---
# <a name="querying-with-wql"></a><span data-ttu-id="c0ece-103">使用 WQL 查詢</span><span class="sxs-lookup"><span data-stu-id="c0ece-103">Querying with WQL</span></span>

<span data-ttu-id="c0ece-104">WMI 查詢語言 (WQL) 是標準美國國家標準局結構化查詢語言 (SQL)  (ANSI SQL) 的子集，其中包含支援 WMI 的次要語義變更。</span><span class="sxs-lookup"><span data-stu-id="c0ece-104">The WMI Query Language (WQL) is a subset of standard American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes to support WMI.</span></span>

<span data-ttu-id="c0ece-105">如需支援的 WQL 關鍵字完整清單，請參閱 [wql (適用于 WMI 的 SQL) ](wql-sql-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="c0ece-105">For a complete list of supported WQL keywords, see [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span> <span data-ttu-id="c0ece-106">針對物件或屬性名稱使用 SQL 關鍵字可能會限制無法剖析查詢。</span><span class="sxs-lookup"><span data-stu-id="c0ece-106">Using SQL keywords for object or property names may restrict a query from being parsed.</span></span> <span data-ttu-id="c0ece-107">下列 SQL 關鍵字受到限制： **Null**、 **TRUE** 和 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c0ece-107">The following SQL keywords are restricted: **NULL**, **TRUE**, and **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="c0ece-108">WQL 查詢中可使用的和和或關鍵字數目有一些限制。</span><span class="sxs-lookup"><span data-stu-id="c0ece-108">There are limits to the number of AND and OR keywords that can be used in WQL queries.</span></span> <span data-ttu-id="c0ece-109">複雜查詢中使用的大量 WQL 關鍵字可能會導致 WMI 將 **WBEM \_ E \_ 配額 \_ 違規** 錯誤碼傳回為 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c0ece-109">Large numbers of WQL keywords used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="c0ece-110">WQL 關鍵字的限制取決於查詢的複雜程度。</span><span class="sxs-lookup"><span data-stu-id="c0ece-110">The limit of WQL keywords depends on how complex the query is.</span></span>

 

<span data-ttu-id="c0ece-111">查詢可以使用 **WHERE** 子句進行擴充和自訂，但不是必要的。</span><span class="sxs-lookup"><span data-stu-id="c0ece-111">Queries can use the **WHERE** clause for extension and customization, although it is not required.</span></span> <span data-ttu-id="c0ece-112">**WHERE** 子句是由屬性或關鍵字、運算子和常數所組成。</span><span class="sxs-lookup"><span data-stu-id="c0ece-112">The **WHERE** clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="c0ece-113">所有 **WHERE** 子句都必須指定 WQL 中包含的其中一個預先定義的運算子。</span><span class="sxs-lookup"><span data-stu-id="c0ece-113">All **WHERE** clauses must specify one of the predefined operators that are included in WQL.</span></span> <span data-ttu-id="c0ece-114">如需語法的詳細資訊，請參閱 [WHERE 子句](where-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="c0ece-114">For more information about syntax, see [WHERE Clause](where-clause.md).</span></span> <span data-ttu-id="c0ece-115">如需有效 WQL 運算子的詳細資訊，請參閱 [Wql 運算子](wql-operators.md)。</span><span class="sxs-lookup"><span data-stu-id="c0ece-115">For more information about valid WQL operators, see [WQL Operators](wql-operators.md).</span></span>

<span data-ttu-id="c0ece-116">如同其他 SQL 查詢字串，您可以對查詢進行 escape。</span><span class="sxs-lookup"><span data-stu-id="c0ece-116">As with other SQL query strings, you can escape your queries.</span></span>

> [!Note]  
> <span data-ttu-id="c0ece-117">WQL 不支援跨命名空間的查詢或關聯。</span><span class="sxs-lookup"><span data-stu-id="c0ece-117">WQL does not support cross-namespace queries or associations.</span></span> <span data-ttu-id="c0ece-118">您無法在目的電腦上的所有命名空間中查詢指定類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="c0ece-118">You cannot query for all instances of a specified class residing in all of the namespaces on the target computer.</span></span>

 

<span data-ttu-id="c0ece-119">WQL 支援下列類型的查詢：</span><span class="sxs-lookup"><span data-stu-id="c0ece-119">WQL supports the following types of queries:</span></span>

-   <span data-ttu-id="c0ece-120">資料查詢</span><span class="sxs-lookup"><span data-stu-id="c0ece-120">Data queries</span></span>

    <span data-ttu-id="c0ece-121">資料查詢是用來取出類別實例和資料關聯。</span><span class="sxs-lookup"><span data-stu-id="c0ece-121">Data queries are used to retrieve class instances and data associations.</span></span> <span data-ttu-id="c0ece-122">它們是 WMI 腳本和應用程式中最常使用的查詢類型。</span><span class="sxs-lookup"><span data-stu-id="c0ece-122">They are the most commonly used type of query in WMI scripts and applications.</span></span> <span data-ttu-id="c0ece-123">如需資料查詢語法的詳細資訊，請參閱 [要求類別實例資料](requesting-class-instance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="c0ece-123">For more information about the syntax of data queries, see [Requesting Class Instance Data](requesting-class-instance-data.md).</span></span> <span data-ttu-id="c0ece-124">如需關聯的詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。</span><span class="sxs-lookup"><span data-stu-id="c0ece-124">For more information about associations, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="c0ece-125">WQL 不支援陣列資料類型的查詢。</span><span class="sxs-lookup"><span data-stu-id="c0ece-125">WQL does not support queries of array datatypes.</span></span>

     

    <span data-ttu-id="c0ece-126">下列資料查詢範例會從所有 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)實例要求名為 "Application" 的事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c0ece-126">The following data query example requests the event log file named "Application" from all instances of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   <span data-ttu-id="c0ece-127">事件查詢</span><span class="sxs-lookup"><span data-stu-id="c0ece-127">Event queries</span></span>

    <span data-ttu-id="c0ece-128">取用者會使用事件查詢來註冊，以接收事件的通知。</span><span class="sxs-lookup"><span data-stu-id="c0ece-128">Consumers use event queries to register to receive notification of events.</span></span> <span data-ttu-id="c0ece-129">事件提供者會使用事件查詢來註冊，以支援一或多個事件。</span><span class="sxs-lookup"><span data-stu-id="c0ece-129">Event providers use event queries to register to support one or more events.</span></span> <span data-ttu-id="c0ece-130">如需事件查詢的詳細資訊，請參閱 [接收事件通知](receiving-event-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="c0ece-130">For more information about event queries, see [Receiving Event Notifications](receiving-event-notifications.md).</span></span>

    <span data-ttu-id="c0ece-131">當衍生自 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) 之類別的新實例建立時，暫存事件取用者會使用下列範例事件查詢來要求通知。</span><span class="sxs-lookup"><span data-stu-id="c0ece-131">The following example event query by a temporary event consumer requests notification when a new instance of a class derived from [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) is created.</span></span>

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   <span data-ttu-id="c0ece-132">架構查詢</span><span class="sxs-lookup"><span data-stu-id="c0ece-132">Schema queries</span></span>

    <span data-ttu-id="c0ece-133">架構查詢是用來取出類別定義 (而非) 和架構關聯的類別實例。</span><span class="sxs-lookup"><span data-stu-id="c0ece-133">Schema queries are used to retrieve class definitions (rather than class instances) and schema associations.</span></span> <span data-ttu-id="c0ece-134">類別提供者會使用架構查詢來指定它們在註冊時所支援的類別。</span><span class="sxs-lookup"><span data-stu-id="c0ece-134">Class providers use schema queries to specify the classes that they support when they register.</span></span> <span data-ttu-id="c0ece-135">如需架構查詢的詳細資訊，請參閱 [取出類別定義](retrieving-class-definitions.md)。</span><span class="sxs-lookup"><span data-stu-id="c0ece-135">For more information about schema queries, see [Retrieving Class Definitions](retrieving-class-definitions.md).</span></span>

    <span data-ttu-id="c0ece-136">下列範例架構查詢會顯示特殊語法。</span><span class="sxs-lookup"><span data-stu-id="c0ece-136">The following example schema query shows the special syntax.</span></span>

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="c0ece-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="c0ece-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0ece-138">WMI 日期和時間格式</span><span class="sxs-lookup"><span data-stu-id="c0ece-138">WMI Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 
