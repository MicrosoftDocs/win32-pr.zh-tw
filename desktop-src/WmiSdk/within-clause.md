---
description: 在事件查詢中使用內子句來指定輪詢間隔或群組間隔。
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: 在子句內
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d863e2e71d52fe60aeed7697feeb1231164c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115036"
---
# <a name="within-clause"></a><span data-ttu-id="a457f-103">在子句內</span><span class="sxs-lookup"><span data-stu-id="a457f-103">WITHIN Clause</span></span>

<span data-ttu-id="a457f-104">事件取用者會在事件查詢中使用 in 子句來指定 *輪詢間隔* 或 *群組間隔*。</span><span class="sxs-lookup"><span data-stu-id="a457f-104">Event consumers use the WITHIN clause in event queries to specify a *polling interval* or a *grouping interval*.</span></span>

<span data-ttu-id="a457f-105">輪詢間隔是 Windows Management Instrumentation (WMI) 用來輪詢 [內部事件](determining-the-type-of-event-to-receive.md)之類別的資料提供者的間隔，而查詢的事件則是成員。</span><span class="sxs-lookup"><span data-stu-id="a457f-105">A polling interval is the interval that Windows Management Instrumentation (WMI) uses to poll the data provider responsible for the class for [intrinsic events](determining-the-type-of-event-to-receive.md), of which the event queried is a member.</span></span> <span data-ttu-id="a457f-106">這個間隔是事件告知必須傳遞之前所能夠等待的最長時間。</span><span class="sxs-lookup"><span data-stu-id="a457f-106">This interval is the maximum amount of time that can pass before notification of an event must be delivered.</span></span> <span data-ttu-id="a457f-107">當取用者需要對類別進行變更的通知，且事件提供者無法使用時，取用者會在內建子句中使用輪詢間隔。</span><span class="sxs-lookup"><span data-stu-id="a457f-107">A consumer uses a polling interval in a WITHIN clause when the consumer requires notification of changes to a class, and an event provider is unavailable.</span></span> <span data-ttu-id="a457f-108">取用者會註冊內部事件並包含輪詢間隔。</span><span class="sxs-lookup"><span data-stu-id="a457f-108">The consumer registers for an intrinsic event and includes the polling interval.</span></span>

<span data-ttu-id="a457f-109">若要指定輪詢間隔，請在 WHERE 子句之前放置內的子句，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a457f-109">To specify a polling interval, place the WITHIN clause immediately before the WHERE clause, as shown following:</span></span>


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



<span data-ttu-id="a457f-110">IntrinsicEventClass 是內部事件類別，其事件為成員、間隔是輪詢間隔，而值則是取用者需要通知的屬性值。</span><span class="sxs-lookup"><span data-stu-id="a457f-110">IntrinsicEventClass is the intrinsic event class of which the event is a member, interval is the polling interval, and value is the value for the property on which the consumer requires notification.</span></span>

<span data-ttu-id="a457f-111">輪詢間隔是浮點數，而且可以是小數以接受小於1秒的值。</span><span class="sxs-lookup"><span data-stu-id="a457f-111">The polling interval is a floating-point number, and can be fractional to accept values smaller than 1 second.</span></span> <span data-ttu-id="a457f-112">不過，間隔應代表幾秒鐘的時間，而不是非常小的值（例如0.001），因為指定太小的值可能會導致 WMI 拒絕不正確語句，因為輪詢的資源密集性質。</span><span class="sxs-lookup"><span data-stu-id="a457f-112">However, the interval should represent a number of seconds rather than an extremely small value such as 0.001, because specifying a value that is too small can cause WMI to reject the statement as not valid—due to the resource-intensive nature of polling.</span></span> <span data-ttu-id="a457f-113">因為大部分的事件取用者不需要立即通知，所以建議使用超過5分鐘的間隔。</span><span class="sxs-lookup"><span data-stu-id="a457f-113">Because most event consumers do not require immediate notification, it is recommended that they use an interval that is greater than 5 minutes.</span></span>

<span data-ttu-id="a457f-114">下列查詢範例會要求 WMI 每隔10秒檢查一次，以進行 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別實例的變更。</span><span class="sxs-lookup"><span data-stu-id="a457f-114">The following query example requests that WMI check every 10 seconds for changes that occur to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="a457f-115">如果在指定的輪詢間隔內修改了類別的實例，就會針對每個修改傳送一個通知事件。</span><span class="sxs-lookup"><span data-stu-id="a457f-115">If an instance of the class is modified within the specified polling interval, a notification event is sent for each modification.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="a457f-116">視查詢而定，事件提供者和 WMI 可以共用提供事件的工作。</span><span class="sxs-lookup"><span data-stu-id="a457f-116">Depending on the query, an event provider and WMI can share the task of providing events.</span></span> <span data-ttu-id="a457f-117">例如，支援 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)和 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)系統類別事件的事件提供者，而不是 [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md)系統類別的事件。</span><span class="sxs-lookup"><span data-stu-id="a457f-117">For example, an event provider that supports events of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) and [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system classes, and not events of the [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) system class.</span></span> <span data-ttu-id="a457f-118">下列查詢可讓事件提供者在事件發生時產生建立和修改事件，並在建立事件時加以傳遞。</span><span class="sxs-lookup"><span data-stu-id="a457f-118">The following query enables the event provider to generate the creation and modification events as they occur and have them delivered when they are created.</span></span> <span data-ttu-id="a457f-119">此查詢也可讓 WMI 使用輪詢機制，每 10 (10) 秒產生 **\_ \_ InstanceDeletionEvent** 事件。</span><span class="sxs-lookup"><span data-stu-id="a457f-119">The query also allows WMI to generate **\_\_InstanceDeletionEvent** events every 10 (ten) seconds using the polling mechanism.</span></span>


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



<span data-ttu-id="a457f-120">您也可以使用內子句來指定群組間隔。</span><span class="sxs-lookup"><span data-stu-id="a457f-120">You can also use the WITHIN clause to specify a grouping interval.</span></span> <span data-ttu-id="a457f-121">群組間隔是一種不帶正負號的32位整數，可指定在接收初始事件之後，WMI 應該收集類似事件的時間週期。</span><span class="sxs-lookup"><span data-stu-id="a457f-121">A grouping interval is an unsigned 32-bit integer that specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span> <span data-ttu-id="a457f-122">當這段時間過期時，WMI 會傳遞匯總事件，由所有類似的事件組成。</span><span class="sxs-lookup"><span data-stu-id="a457f-122">When this time period expires, WMI delivers the aggregate event, made up of all the similar events.</span></span> <span data-ttu-id="a457f-123">如需詳細資訊，請參閱 [Group 子句](group-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="a457f-123">For more information, see [GROUP Clause](group-clause.md).</span></span>

<span data-ttu-id="a457f-124">註冊經常發生之事件的事件取用者，會搭配使用群組間隔與內子句。</span><span class="sxs-lookup"><span data-stu-id="a457f-124">Event consumers that register for frequently occurring events use a grouping interval with the WITHIN clause.</span></span> <span data-ttu-id="a457f-125">將群組加入至事件查詢中的 WHERE 子句，會導致 WMI 傳送一個匯總事件，而不是多個事件。</span><span class="sxs-lookup"><span data-stu-id="a457f-125">Adding GROUP WITHIN to the WHERE clause in an event query results in WMI sending one aggregate event rather than many events.</span></span> <span data-ttu-id="a457f-126">匯總事件是以 [**\_ \_ AggregateEvent**](--aggregateevent.md)系統類別表示。</span><span class="sxs-lookup"><span data-stu-id="a457f-126">The aggregate event is represented by the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span>

<span data-ttu-id="a457f-127">若要指定群組間隔，請將內的子句放在 GROUP 子句之後。</span><span class="sxs-lookup"><span data-stu-id="a457f-127">To specify a grouping interval, place the WITHIN clause immediately after the GROUP clause.</span></span>


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



<span data-ttu-id="a457f-128">EventClass 是事件所屬的事件類別，值是取用者需要通知的屬性值，而間隔是群組間隔。</span><span class="sxs-lookup"><span data-stu-id="a457f-128">EventClass is the event class of which the event is a member, value is the value for the property on which the consumer requires notification, and Interval is the grouping interval.</span></span>

<span data-ttu-id="a457f-129">如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="a457f-129">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="a457f-130">只有當您具有系統管理員許可權時，才能使用輪詢查詢來建立永久事件取用者。</span><span class="sxs-lookup"><span data-stu-id="a457f-130">Permanent event consumers can be created with polling queries only if you have administrator privileges.</span></span>

 

 
