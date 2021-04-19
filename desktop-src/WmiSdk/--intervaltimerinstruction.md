---
description: 依時間間隔產生事件，類似于 \_ Windows 程式設計中的 WM 計時器訊息。
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: __IntervalTimerInstruction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985490"
---
# <a name="__intervaltimerinstruction-class"></a><span data-ttu-id="fee19-103">\_\_IntervalTimerInstruction 類別</span><span class="sxs-lookup"><span data-stu-id="fee19-103">\_\_IntervalTimerInstruction class</span></span>

<span data-ttu-id="fee19-104">**\_ \_ IntervalTimerInstruction** 系統類別會依間隔產生事件，類似于 Windows 程式 \_ 設計中的 WM 計時器訊息。</span><span class="sxs-lookup"><span data-stu-id="fee19-104">The **\_\_IntervalTimerInstruction** system class generates events at intervals, similar to a WM\_TIMER message in Windows programming.</span></span> <span data-ttu-id="fee19-105">事件取用者會藉由建立參考此類別的事件查詢，來註冊接收間隔計時器事件。</span><span class="sxs-lookup"><span data-stu-id="fee19-105">An event consumer registers to receive interval timer events by creating an event query that references this class.</span></span> <span data-ttu-id="fee19-106">由於作業系統行為的緣故，因此不保證事件會精確地以要求的間隔傳遞。</span><span class="sxs-lookup"><span data-stu-id="fee19-106">Due to operating system behavior, there are no guarantees that events will be delivered at precisely the requested interval.</span></span>

<span data-ttu-id="fee19-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fee19-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fee19-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="fee19-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fee19-109">語法</span><span class="sxs-lookup"><span data-stu-id="fee19-109">Syntax</span></span>

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="fee19-110">成員</span><span class="sxs-lookup"><span data-stu-id="fee19-110">Members</span></span>

<span data-ttu-id="fee19-111">**\_ \_ IntervalTimerInstruction** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fee19-111">The **\_\_IntervalTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="fee19-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fee19-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fee19-113">屬性</span><span class="sxs-lookup"><span data-stu-id="fee19-113">Properties</span></span>

<span data-ttu-id="fee19-114">**\_ \_ IntervalTimerInstruction** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fee19-114">The **\_\_IntervalTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fee19-115">**IntervalBetweenEvents**</span><span class="sxs-lookup"><span data-stu-id="fee19-115">**IntervalBetweenEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee19-116">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fee19-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fee19-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fee19-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee19-118">限定詞： [**單位**](standard-qualifiers.md) (毫秒) </span><span class="sxs-lookup"><span data-stu-id="fee19-118">Qualifiers: [**Units**](standard-qualifiers.md) (milliseconds)</span></span>
</dt> </dl>

<span data-ttu-id="fee19-119">事件引發之間的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="fee19-119">Number of milliseconds between event firings.</span></span>

</dd> <dt>

<span data-ttu-id="fee19-120">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="fee19-120">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee19-121">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fee19-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fee19-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fee19-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fee19-123">若 **為 TRUE**，則會略過此事件（如果已通過間隔）。</span><span class="sxs-lookup"><span data-stu-id="fee19-123">If **TRUE**, this event is to be skipped if the interval is already passed.</span></span> <span data-ttu-id="fee19-124">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fee19-124">The default is **FALSE**.</span></span> <span data-ttu-id="fee19-125">這個屬性繼承自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。</span><span class="sxs-lookup"><span data-stu-id="fee19-125">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="fee19-126">FALSE</span><span class="sxs-lookup"><span data-stu-id="fee19-126">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="fee19-127">當 WMI 或取用者再次變成可用時，將會產生並接收通知事件。</span><span class="sxs-lookup"><span data-stu-id="fee19-127">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="fee19-128">true</span><span class="sxs-lookup"><span data-stu-id="fee19-128">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="fee19-129">如果 WMI 無法在適當的時間間隔內產生，或要求接收事件的取用者無法使用，就不會發生計時器事件。</span><span class="sxs-lookup"><span data-stu-id="fee19-129">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fee19-130">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="fee19-130">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee19-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fee19-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fee19-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fee19-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee19-133">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="fee19-133">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="fee19-134">這個 **\_ \_ IntervalTimerInstruction** 物件的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fee19-134">Unique identifier for this **\_\_IntervalTimerInstruction** object.</span></span> <span data-ttu-id="fee19-135">這個屬性繼承自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。</span><span class="sxs-lookup"><span data-stu-id="fee19-135">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fee19-136">備註</span><span class="sxs-lookup"><span data-stu-id="fee19-136">Remarks</span></span>

<span data-ttu-id="fee19-137">**\_ \_ IntervalTimerInstruction** 類別衍生自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。</span><span class="sxs-lookup"><span data-stu-id="fee19-137">The **\_\_IntervalTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="fee19-138">輸入以註冊間隔計時器事件的事件查詢，通常是以 **TimerId** 屬性為基礎。</span><span class="sxs-lookup"><span data-stu-id="fee19-138">The event query entered to register for an interval timer event is usually based on the **TimerId** property.</span></span> <span data-ttu-id="fee19-139">從間隔計時器事件產生的通知事件包含屬性 **NumFirings** ，其中包含的資料會反映無法接收事件時所引發的事件數目。</span><span class="sxs-lookup"><span data-stu-id="fee19-139">Notification events generated from an interval timer event contain the property **NumFirings** which contains data reflecting how many events fired during the time the events were unable to be received.</span></span> <span data-ttu-id="fee19-140">如果 **SkipIfPassed** 設定為 **TRUE**，則會捨棄該資訊。</span><span class="sxs-lookup"><span data-stu-id="fee19-140">If **SkipIfPassed** is set to **TRUE**, that information is discarded.</span></span>

<span data-ttu-id="fee19-141">**IntervalBetweenEvents** 屬性的值應該相當大。</span><span class="sxs-lookup"><span data-stu-id="fee19-141">The value for the **IntervalBetweenEvents** property should be reasonably large.</span></span> <span data-ttu-id="fee19-142">如果太小，WMI 可能會忽略它，而不會因為某些作業系統的限制而產生事件。</span><span class="sxs-lookup"><span data-stu-id="fee19-142">If it is too small, WMI may ignore it and not generate the event due to limitations in some operating systems.</span></span>

<span data-ttu-id="fee19-143">WMI 藉由建立 [**\_ \_ TimerEvent**](--timerevent.md)類別的實例來產生間隔計時器事件。</span><span class="sxs-lookup"><span data-stu-id="fee19-143">WMI generates the interval timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

<span data-ttu-id="fee19-144">若要在暫存事件取用者中接收這些計時器事件，請使用下列事件查詢字串來執行 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) ：</span><span class="sxs-lookup"><span data-stu-id="fee19-144">To receive these timer events in a temporary event consumer, execute [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) with the following event query string:</span></span>


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



<span data-ttu-id="fee19-145">若要在永久事件取用者中接收這些計時器事件，您必須將先前的查詢載入事件篩選器、定義邏輯取用者，以及為篩選和取用者建立篩選至取用者系結。</span><span class="sxs-lookup"><span data-stu-id="fee19-145">To receive these timer events in a permanent event consumer, you must load the previous query into an event filter, define a logical consumer, and create a filter-to-consumer binding for the filter and consumer.</span></span> <span data-ttu-id="fee19-146">如需詳細資訊，請參閱 [所有時間的接收事件](receiving-events-at-all-times.md)。</span><span class="sxs-lookup"><span data-stu-id="fee19-146">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fee19-147">範例</span><span class="sxs-lookup"><span data-stu-id="fee19-147">Examples</span></span>

<span data-ttu-id="fee19-148">下列 MOF 宣告顯示如何產生間隔計時器事件，其索引鍵屬性每10秒設定為 "MyEvent"：</span><span class="sxs-lookup"><span data-stu-id="fee19-148">The following MOF declaration shows how to generate an interval timer event with the key property set to "MyEvent" every 10 seconds:</span></span>


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a><span data-ttu-id="fee19-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="fee19-149">Requirements</span></span>



| <span data-ttu-id="fee19-150">需求</span><span class="sxs-lookup"><span data-stu-id="fee19-150">Requirement</span></span> | <span data-ttu-id="fee19-151">值</span><span class="sxs-lookup"><span data-stu-id="fee19-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fee19-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fee19-152">Minimum supported client</span></span><br/> | <span data-ttu-id="fee19-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fee19-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fee19-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fee19-154">Minimum supported server</span></span><br/> | <span data-ttu-id="fee19-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fee19-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="fee19-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="fee19-156">Namespace</span></span><br/>                | <span data-ttu-id="fee19-157">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="fee19-157">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="fee19-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fee19-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee19-159">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="fee19-159">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="fee19-160">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="fee19-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="fee19-161">接收計時或重複事件</span><span class="sxs-lookup"><span data-stu-id="fee19-161">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 

