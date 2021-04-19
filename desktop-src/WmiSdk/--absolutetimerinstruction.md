---
description: 導致在特定時間于特定日期產生事件。
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: __AbsoluteTimerInstruction 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988071"
---
# <a name="__absolutetimerinstruction-class"></a><span data-ttu-id="5456a-103">\_\_AbsoluteTimerInstruction 類別</span><span class="sxs-lookup"><span data-stu-id="5456a-103">\_\_AbsoluteTimerInstruction class</span></span>

<span data-ttu-id="5456a-104">**\_ \_ AbsoluteTimerInstruction** 系統類別會在特定時間產生特定日期的事件。</span><span class="sxs-lookup"><span data-stu-id="5456a-104">The **\_\_AbsoluteTimerInstruction** system class causes an event to be generated on a specific date at a specific time.</span></span> <span data-ttu-id="5456a-105">事件取用者會藉由建立此類別的實例，註冊以接收絕對計時器事件。</span><span class="sxs-lookup"><span data-stu-id="5456a-105">An event consumer registers to receive an absolute timer event by creating an instance of this class.</span></span> <span data-ttu-id="5456a-106">事件會產生一次。</span><span class="sxs-lookup"><span data-stu-id="5456a-106">The event is generated one time.</span></span>

<span data-ttu-id="5456a-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5456a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5456a-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5456a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5456a-109">語法</span><span class="sxs-lookup"><span data-stu-id="5456a-109">Syntax</span></span>

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a><span data-ttu-id="5456a-110">成員</span><span class="sxs-lookup"><span data-stu-id="5456a-110">Members</span></span>

<span data-ttu-id="5456a-111">**\_ \_ AbsoluteTimerInstruction** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5456a-111">The **\_\_AbsoluteTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="5456a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5456a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5456a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5456a-113">Properties</span></span>

<span data-ttu-id="5456a-114">**\_ \_ AbsoluteTimerInstruction** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5456a-114">The **\_\_AbsoluteTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5456a-115">**EventDateTime**</span><span class="sxs-lookup"><span data-stu-id="5456a-115">**EventDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5456a-116">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5456a-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5456a-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5456a-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5456a-118">採用 [DMTF 格式](date-and-time-format.md) 的固定長度字串，可指定計時器引發的時間。</span><span class="sxs-lookup"><span data-stu-id="5456a-118">Fixed-length string in [DMTF format](date-and-time-format.md) that specifies when the timer fires.</span></span>

</dd> <dt>

<span data-ttu-id="5456a-119">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="5456a-119">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5456a-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5456a-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5456a-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5456a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5456a-122">若 **為 TRUE**，則如果 WMI 無法在正確的時間間隔內產生計時器事件，或要求接收事件的取用者無法使用，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="5456a-122">If **TRUE**, the timer event occurs if WMI cannot generate it at the correct time interval, or the consumer requesting to receive the event is unavailable.</span></span> <span data-ttu-id="5456a-123">若 **為 TRUE**，將不會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="5456a-123">If **TRUE**, the event will not occur.</span></span> <span data-ttu-id="5456a-124">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5456a-124">The default is **FALSE**.</span></span> <span data-ttu-id="5456a-125">當 WMI 或取用者變成可用時，就會產生並接收通知事件。</span><span class="sxs-lookup"><span data-stu-id="5456a-125">When WMI or the consumer becomes available, a notification event is generated and received.</span></span> <span data-ttu-id="5456a-126">這個屬性繼承自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。</span><span class="sxs-lookup"><span data-stu-id="5456a-126">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="5456a-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="5456a-127">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="5456a-128">當 WMI 或取用者再次變成可用時，將會產生並接收通知事件。</span><span class="sxs-lookup"><span data-stu-id="5456a-128">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="5456a-129">true</span><span class="sxs-lookup"><span data-stu-id="5456a-129">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="5456a-130">如果 WMI 無法在適當的時間間隔內產生，或要求接收事件的取用者無法使用，就不會發生計時器事件。</span><span class="sxs-lookup"><span data-stu-id="5456a-130">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5456a-131">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="5456a-131">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5456a-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5456a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5456a-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5456a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5456a-134">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5456a-134">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5456a-135">識別特定計時器事件的唯一使用者指派字串。</span><span class="sxs-lookup"><span data-stu-id="5456a-135">Unique user-assigned string that identifies a specific timer event.</span></span> <span data-ttu-id="5456a-136">為了避免與其他計時器識別碼發生名稱衝突，可以使用分散式運算機環境樣式 GUID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="5456a-136">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment style GUID can be used.</span></span> <span data-ttu-id="5456a-137">這個屬性繼承自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。</span><span class="sxs-lookup"><span data-stu-id="5456a-137">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5456a-138">備註</span><span class="sxs-lookup"><span data-stu-id="5456a-138">Remarks</span></span>

<span data-ttu-id="5456a-139">**\_ \_ AbsoluteTimerInstruction** 類別衍生自 [**\_ \_ TimerInstruction**](--timerinstruction.md)。</span><span class="sxs-lookup"><span data-stu-id="5456a-139">The **\_\_AbsoluteTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="5456a-140">WMI 藉由建立 [**\_ \_ TimerEvent**](--timerevent.md)類別的實例來產生絕對計時器事件。</span><span class="sxs-lookup"><span data-stu-id="5456a-140">WMI generates the absolute timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="5456a-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="5456a-141">Requirements</span></span>



| <span data-ttu-id="5456a-142">需求</span><span class="sxs-lookup"><span data-stu-id="5456a-142">Requirement</span></span> | <span data-ttu-id="5456a-143">值</span><span class="sxs-lookup"><span data-stu-id="5456a-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5456a-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5456a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5456a-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5456a-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5456a-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5456a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5456a-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5456a-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5456a-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="5456a-148">Namespace</span></span><br/>                | <span data-ttu-id="5456a-149">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="5456a-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5456a-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5456a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5456a-151">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="5456a-151">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="5456a-152">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="5456a-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5456a-153">接收計時或重複事件</span><span class="sxs-lookup"><span data-stu-id="5456a-153">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[<span data-ttu-id="5456a-154">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="5456a-154">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="5456a-155">在您的應用程式期間接收事件</span><span class="sxs-lookup"><span data-stu-id="5456a-155">Receiving Events for the Duration of Your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

