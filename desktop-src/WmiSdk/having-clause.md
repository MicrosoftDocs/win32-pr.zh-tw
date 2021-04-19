---
description: HAVING 子句可用來篩選在 in 子句中指定的分組間隔期間所收到的事件。
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: HAVING 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f93fbe082fb2f655dfad59d7642e1d0ff9a33e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989989"
---
# <a name="having-clause"></a><span data-ttu-id="a8f3f-103">HAVING 子句</span><span class="sxs-lookup"><span data-stu-id="a8f3f-103">HAVING Clause</span></span>

<span data-ttu-id="a8f3f-104">HAVING 子句可用來篩選在 in [子句](within-clause.md)中指定的分組間隔期間所收到的事件。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-104">The HAVING clause is used to filter the events that are received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="a8f3f-105">例如，您可以建立一個 SELECT 語句，讓它不會傳回任何內容，除非過去30秒的間隔內至少有5個事件。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-105">For example, a SELECT statement could be constructed so that it returns nothing unless there HAVE been at least 5 events within the past 30 second INTERVAL.</span></span>

<span data-ttu-id="a8f3f-106">In 子句緊接在[group](group-clause.md)子句之後的[SELECT 語句](select-statement-for-event-queries.md)中。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-106">The WITHIN clause follows immediately in the [SELECT statement](select-statement-for-event-queries.md) after the [GROUP](group-clause.md) clause.</span></span> <span data-ttu-id="a8f3f-107">HAVING 子句會在 [**\_ \_ AggregateEvent**](--aggregateevent.md)系統類別的 **NumberOfEvents** 屬性上運作，而 group 子句所建立的群組是成員。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-107">The HAVING clause operates on the **NumberOfEvents** property of the [**\_\_AggregateEvent**](--aggregateevent.md) system class, of which the group created by the GROUP clause is a member.</span></span> <span data-ttu-id="a8f3f-108">HAVING 子句可以使用所有標準關係運算子。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-108">The HAVING clause can use all of the standard relational operators.</span></span>

<span data-ttu-id="a8f3f-109">語法如下：</span><span class="sxs-lookup"><span data-stu-id="a8f3f-109">The syntax is as follows:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

<span data-ttu-id="a8f3f-110">*EventClass* 值是事件所屬的事件類別，而 *值* 則是需要通知之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-110">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="a8f3f-111">間隔是一種不帶正負號的整數，表示在接收到第一個事件之後 (的分組間隔（以秒) 為單位）。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-111">The interval is an unsigned integer that represents the grouping interval (in seconds) after receiving the first event.</span></span> <span data-ttu-id="a8f3f-112">屬性清單是事件類別中包含的一或多個屬性的逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-112">The property list is a comma-delimited list of one or more properties that are included in the event class.</span></span> <span data-ttu-id="a8f3f-113">運算子是任何關係運算子。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-113">The operator is any relational operator.</span></span> <span data-ttu-id="a8f3f-114">常數值是任何不帶正負號的32位整數，表示用於篩選的事件數目。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-114">The constant value is any unsigned 32-bit integer indicating the number of events used for filtering.</span></span>

<span data-ttu-id="a8f3f-115">使用 HAVING 子句時，WHERE 和 BY 子句是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-115">When using the HAVING clause, the WHERE and BY clauses are optional.</span></span>

<span data-ttu-id="a8f3f-116">下列事件查詢要求 **EmailEvent** 類別的通知會在 WMI 收到的第一個事件之後分組為一個事件300秒。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-116">The following event query requests that notifications of the **EmailEvent** class be grouped into one event 300 seconds after the first event that WMI receives.</span></span> <span data-ttu-id="a8f3f-117">此外，只有當 WMI 在300秒內收到五個以上的電子郵件事件時，查詢才會要求 [**\_ \_ AggregateEvent**](--aggregateevent.md)實例傳遞。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-117">Also, the query requests the [**\_\_AggregateEvent**](--aggregateevent.md) instance should be delivered only if WMI receives more than five email events in that 300 seconds.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



<span data-ttu-id="a8f3f-118">下列範例會將600秒內收到的所有事件分組 (也就是 **TargetInstance**) 10 分鐘。未通過 **的屬性。**</span><span class="sxs-lookup"><span data-stu-id="a8f3f-118">The following example groups all events received in 600 seconds (that is, 10 minutes) by the **TargetInstance**.**SourceName** property.</span></span> <span data-ttu-id="a8f3f-119">在此範例中，只有在從相同來源收到的 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) 事件數目超過25時，才會傳遞匯總事件。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-119">In this example, aggregate events are delivered only if the number of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) events received from the same source exceeds 25.</span></span> <span data-ttu-id="a8f3f-120">請記住，ISA 運算子會讓 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)系統類別的 **TargetInstance** 屬性代表 **Win32 \_ NTLogEvent** 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a8f3f-120">Keep in mind that the ISA operator causes the **TargetInstance** property of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) system class to represent an instance of the **Win32\_NTLogEvent** class.</span></span>


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
