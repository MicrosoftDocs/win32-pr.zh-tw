---
description: 描述事件查詢之 SELECT 語句的基本語法。
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: 事件查詢的 SELECT 語句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194700"
---
# <a name="select-statement-for-event-queries"></a><span data-ttu-id="9c9cf-103">事件查詢的 SELECT 語句</span><span class="sxs-lookup"><span data-stu-id="9c9cf-103">SELECT Statement for Event Queries</span></span>

<span data-ttu-id="9c9cf-104">您可以使用各種 SELECT 語句來查詢事件資訊。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-104">You can use a variety of SELECT statements to query for event information.</span></span> <span data-ttu-id="9c9cf-105">語句可以是基本語句，也可以更嚴格地縮減查詢所傳回的結果集。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="9c9cf-106">下列範例是用來查詢事件資訊的基本 SELECT 語句。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-106">The following example is a basic SELECT statement that is used to query for event information.</span></span>


```sql
SELECT * FROM EventClass
```



<span data-ttu-id="9c9cf-107">當取用者提交查詢時，會要求收到 **EventClass** 所代表事件的所有出現次數。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-107">When a consumer submits a query, it is a request to be notified of all occurrences of the event represented by **EventClass**.</span></span> <span data-ttu-id="9c9cf-108">此要求包含有關所有事件系統和非系統屬性的通知要求。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-108">This request includes a request for notification about all of the event system and nonsystem properties.</span></span> <span data-ttu-id="9c9cf-109">當事件提供者提交查詢時，它會在 **EventClass** 所代表的事件發生時，註冊產生通知的支援。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-109">When an event provider submits a query, it registers support for generating notifications when an event represented by **EventClass** occurs.</span></span>

<span data-ttu-id="9c9cf-110">取用者可以在 SELECT 語句中指定個別屬性，而不是星號 (\*) 。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-110">Consumers can specify individual properties instead of the asterisk (\*) in the SELECT statement.</span></span>

<span data-ttu-id="9c9cf-111">下列範例示範如何查詢特定屬性。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-111">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



<span data-ttu-id="9c9cf-112">但是，即使查詢指定内嵌物件屬性，也會傳回内嵌物件的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-112">However, all of the properties of an embedded object are returned, even if the query specifies embedded object properties.</span></span>

<span data-ttu-id="9c9cf-113">下列範例顯示兩個傳回相同資料的查詢。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-113">The following example shows two queries that return the same data.</span></span>


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



<span data-ttu-id="9c9cf-114">如果系統屬性與特定查詢無關，則會包含 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-114">If a system property is not relevant for a specific query, it contains **NULL**.</span></span> <span data-ttu-id="9c9cf-115">例如，所有事件查詢的 **\_ \_ RELPATH** 系統屬性值都是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-115">For example, the value of the **\_\_RELPATH** system property is **NULL** for all event queries.</span></span>

<span data-ttu-id="9c9cf-116">下列系統屬性包含事件查詢的 **Null** ：</span><span class="sxs-lookup"><span data-stu-id="9c9cf-116">The following system properties contain **NULL** for event queries:</span></span>

<dl> <span data-ttu-id="9c9cf-117">\_\_命名 空間</span><span class="sxs-lookup"><span data-stu-id="9c9cf-117">\_\_Namespace</span></span>  
<span data-ttu-id="9c9cf-118">\_\_路徑</span><span class="sxs-lookup"><span data-stu-id="9c9cf-118">\_\_Path</span></span>  
<span data-ttu-id="9c9cf-119">\_\_RelPath</span><span class="sxs-lookup"><span data-stu-id="9c9cf-119">\_\_RelPath</span></span>  
<span data-ttu-id="9c9cf-120">\_\_伺服器</span><span class="sxs-lookup"><span data-stu-id="9c9cf-120">\_\_Server</span></span>  
</dl>

<span data-ttu-id="9c9cf-121">如需詳細資訊，請參閱 [WMI 系統屬性參考](wmi-system-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-121">For more information, see [WMI System Property Reference](wmi-system-properties.md).</span></span>

<span data-ttu-id="9c9cf-122">所有事件查詢都可以包含選擇性 [的 WHERE 子句](where-clause.md)，但 where 子句主要是供取用者用來指定其他篩選。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-122">All event queries can include an optional [WHERE clause](where-clause.md), but WHERE clauses are primarily used by consumers to specify additional filtering.</span></span> <span data-ttu-id="9c9cf-123">強烈建議取用者一律指定 WHERE 子句。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-123">It is strongly recommended that consumers always specify a WHERE clause.</span></span> <span data-ttu-id="9c9cf-124">相較于傳遞和處理不必要通知的成本，複雜查詢的成本很低。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-124">The cost of a complex query is minimal compared to the cost of delivering and processing unneeded notifications.</span></span>

<span data-ttu-id="9c9cf-125">下列範例顯示的查詢會要求所有會影響假想類別 **EmailEvent** 的實例修改事件的通知。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-125">The following example shows a query that requests notifications of all instance modification events that affect the hypothetical class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent
```



<span data-ttu-id="9c9cf-126">如果經常發生與 **EmailEvent** 相關聯的事件，取用者會產生事件。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-126">If events associated with **EmailEvent** occur frequently, the consumer is flooded with events.</span></span> <span data-ttu-id="9c9cf-127">只有當特定條件使用指定之類別的屬性（例如重要性層級很高）時，更好的查詢才會要求事件。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-127">A better query requests events only when specific conditions use properties of the class specified, such as when the importance level is high.</span></span>

<span data-ttu-id="9c9cf-128">下列範例顯示當 **EmailImportance** 是 **EmailEvent** 類別的屬性時，您可以使用的查詢。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-128">The following example shows the query you can use if **EmailImportance** is a property of the class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



<span data-ttu-id="9c9cf-129">請注意，WMI 可能會因為許多原因而拒絕查詢。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-129">Note that WMI can reject a query for a number of reasons.</span></span> <span data-ttu-id="9c9cf-130">例如，查詢可能太複雜或需要大量資源才能進行評估。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-130">For example, the query can be too complex or resource-intensive for evaluation.</span></span> <span data-ttu-id="9c9cf-131">發生這種情況時，WMI 會傳回特定的錯誤碼，例如 **WBEM \_ E \_ 無效 \_ 查詢**。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-131">When this occurs, WMI returns specific error codes, such as **WBEM\_E\_INVALID\_QUERY**.</span></span>

<span data-ttu-id="9c9cf-132">内嵌物件的屬性可以在 WHERE 子句中使用。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-132">Properties of embedded objects can be used in the WHERE clause.</span></span>

<span data-ttu-id="9c9cf-133">下列範例示範如何查詢物件，其中 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)系統類別的 **TargetInstance** 屬性是內嵌的 [**win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)物件，而可 **空間** 是 **Win32 \_ LogicalDisk** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-133">The following example shows how to query for objects where the **TargetInstance** property of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system class is an embedded [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) object and **FreeSpace** is a property of **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a><span data-ttu-id="9c9cf-134">範例</span><span class="sxs-lookup"><span data-stu-id="9c9cf-134">Examples</span></span>

<span data-ttu-id="9c9cf-135">TechNet 上 [特定進程名稱 VBScript 範例的監視器建立事件](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) 會使用 SELECT 語句來監視 Win32 進程的 WMI 實例建立事件 \_ ，並篩選特定的進程名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9cf-135">The [Monitor creation event for specific process name](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript sample on TechNet uses the SELECT statement to monitor WMI instance creation events for Win32\_Process, filtering for a specific process name.</span></span>

 

 
