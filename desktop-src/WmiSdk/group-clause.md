---
description: GROUP 子句會讓 WMI 產生單一通知，以代表事件群組。
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: GROUP 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032a8e86c84c0b317b3739c0e203a249b432b0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998544"
---
# <a name="group-clause"></a><span data-ttu-id="75fa0-103">GROUP 子句</span><span class="sxs-lookup"><span data-stu-id="75fa0-103">GROUP Clause</span></span>

<span data-ttu-id="75fa0-104">GROUP 子句會讓 WMI 產生單一通知，以代表事件群組。</span><span class="sxs-lookup"><span data-stu-id="75fa0-104">The GROUP clause causes WMI to generate a single notification to represent a group of events.</span></span> <span data-ttu-id="75fa0-105">代表通知是 [**\_ \_ AggregateEvent**](--aggregateevent.md)系統類別的實例。</span><span class="sxs-lookup"><span data-stu-id="75fa0-105">The representative notification is an instance of the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span> <span data-ttu-id="75fa0-106">**\_ \_ AggregateEvent** 系統類別包含兩個屬性：**代表** 和 **NumberOfEvents**。</span><span class="sxs-lookup"><span data-stu-id="75fa0-106">The **\_\_AggregateEvent** system class contains two properties: **Representative** and **NumberOfEvents**.</span></span> <span data-ttu-id="75fa0-107">**代表** 屬性是一個内嵌物件，其中包含在 in [子句](within-clause.md)中指定的分組間隔期間所收到的其中一個實例。</span><span class="sxs-lookup"><span data-stu-id="75fa0-107">The **Representative** property is an embedded object that contains one of the instances received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="75fa0-108">例如，如果產生匯總事件以通知實例修改事件，表示 **代表** 包含一個 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="75fa0-108">For example, if an aggregate event is generated to notify of instance modification events, **Representative** contains one instance of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) class.</span></span> <span data-ttu-id="75fa0-109">**NumberOfEvents** 屬性包含在群組間隔期間收到的事件數目。</span><span class="sxs-lookup"><span data-stu-id="75fa0-109">The **NumberOfEvents** property contains the number of events received during the grouping interval.</span></span> <span data-ttu-id="75fa0-110">[群組間隔] 會指定在接收到初始事件之後，WMI 應該收集類似事件的時間週期。</span><span class="sxs-lookup"><span data-stu-id="75fa0-110">The grouping interval specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span>

<span data-ttu-id="75fa0-111">GROUP 子句必須包含內的子句來指定群組間隔，而且可以包含 BY 或 HAVING 關鍵字，或兩者都包含。</span><span class="sxs-lookup"><span data-stu-id="75fa0-111">The GROUP clause must contain a WITHIN clause to specify the grouping interval and can contain the BY or HAVING keyword, or both.</span></span> <span data-ttu-id="75fa0-112">GROUP 子句位於 WHERE 子句之後，如下所示：</span><span class="sxs-lookup"><span data-stu-id="75fa0-112">The GROUP clause is placed after the WHERE clause, as shown following:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

<span data-ttu-id="75fa0-113">*EventClass* 值是事件所屬的事件類別，而 *值* 則是需要通知之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="75fa0-113">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="75fa0-114">間隔是不帶正負號的整數，表示在接收到第一個事件之後的分組間隔。</span><span class="sxs-lookup"><span data-stu-id="75fa0-114">The interval is an unsigned integer that represents the grouping interval after receiving the first event.</span></span> <span data-ttu-id="75fa0-115">不帶正負號的整數是秒數。</span><span class="sxs-lookup"><span data-stu-id="75fa0-115">The unsigned integer is a number of seconds.</span></span> <span data-ttu-id="75fa0-116">屬性清單是事件類別中所包含的一或多個屬性的逗號分隔清單; *運算子* 是任何關係運算子;和 *整數* 是一個不帶正負號的32位整數，表示多個事件。</span><span class="sxs-lookup"><span data-stu-id="75fa0-116">The property list is a comma-delimited list of one or more properties that are included in the event class; *operator* is any relational operator; and *integer* is an unsigned 32-bit integer indicating a number of events.</span></span>

<span data-ttu-id="75fa0-117">使用 GROUP 子句時，WHERE、BY 和 HAVING 子句是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="75fa0-117">When using the GROUP clause, the WHERE, BY, and HAVING clauses are optional.</span></span>

<span data-ttu-id="75fa0-118">GROUP 子句的基本用法可能會在收到第一個事件時啟動的時間間隔內要求群組事件。</span><span class="sxs-lookup"><span data-stu-id="75fa0-118">A basic use of the GROUP clause might request a grouping of events within a time interval that starts when the first event is received.</span></span> <span data-ttu-id="75fa0-119">例如，下列查詢會將在5分鐘內傳送的所有電子郵件事件分組。</span><span class="sxs-lookup"><span data-stu-id="75fa0-119">For example, the following query groups all of the email events sent within 5 minutes.</span></span> <span data-ttu-id="75fa0-120">當收到新電子郵件時，永久取用者可能會使用此查詢來通知使用者，只有在過去5分鐘內收到新電子郵件時，才會將使用者分頁。</span><span class="sxs-lookup"><span data-stu-id="75fa0-120">Instead of paging a user every time a piece of new email is received, the permanent consumer might use this query to inform the user only if new email has been received within the last 5 minutes.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



<span data-ttu-id="75fa0-121">如果需要更詳細的資訊，事件可以依事件類別的一或多個屬性分組。</span><span class="sxs-lookup"><span data-stu-id="75fa0-121">If more detailed information is required, events can be grouped by one or more properties of the event class.</span></span> <span data-ttu-id="75fa0-122">下列查詢會要求電子郵件事件與 **寄件者** 屬性中具有相同值的其他事件結合：</span><span class="sxs-lookup"><span data-stu-id="75fa0-122">The following query requests that email events be combined with other events that have the same value in the **Sender** property:</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



<span data-ttu-id="75fa0-123">您可以藉由加入 WHERE 子句來達成更高的詳細程度。</span><span class="sxs-lookup"><span data-stu-id="75fa0-123">A still greater level of detail can be achieved by adding a WHERE clause.</span></span> <span data-ttu-id="75fa0-124">例如，下列查詢會通知使用者來自過去10分鐘內抵達的特定寄件者的新電子郵件，並與 [ **重要性** ] 屬性中具有相同值的其他事件結合：</span><span class="sxs-lookup"><span data-stu-id="75fa0-124">For example, the following query notifies a user of new email from a particular sender that has arrived within the last 10 minutes, combined with other events that have the same value in the **Importance** property:</span></span>


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



