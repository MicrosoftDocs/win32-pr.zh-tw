---
description: 作為與實例相關之所有內建事件的基類。
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: __InstanceOperationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975272"
---
# <a name="__instanceoperationevent-class"></a><span data-ttu-id="6758e-103">\_\_InstanceOperationEvent 類別</span><span class="sxs-lookup"><span data-stu-id="6758e-103">\_\_InstanceOperationEvent class</span></span>

<span data-ttu-id="6758e-104">**\_ \_ InstanceOperationEvent** 系統類別可做為與實例相關之所有內部事件的基類。</span><span class="sxs-lookup"><span data-stu-id="6758e-104">The **\_\_InstanceOperationEvent** system class serves as a base class for all intrinsic events that relate to an instance.</span></span>

<span data-ttu-id="6758e-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6758e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6758e-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="6758e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6758e-107">語法</span><span class="sxs-lookup"><span data-stu-id="6758e-107">Syntax</span></span>

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="6758e-108">成員</span><span class="sxs-lookup"><span data-stu-id="6758e-108">Members</span></span>

<span data-ttu-id="6758e-109">**\_ \_ InstanceOperationEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6758e-109">The **\_\_InstanceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="6758e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6758e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6758e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6758e-111">Properties</span></span>

<span data-ttu-id="6758e-112">**\_ \_ InstanceOperationEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6758e-112">The **\_\_InstanceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6758e-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="6758e-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6758e-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="6758e-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6758e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6758e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6758e-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="6758e-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="6758e-117">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="6758e-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="6758e-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="6758e-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6758e-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="6758e-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="6758e-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6758e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6758e-121">受事件影響的實例。</span><span class="sxs-lookup"><span data-stu-id="6758e-121">Instance affected by the event.</span></span> <span data-ttu-id="6758e-122">針對建立事件，這是新建立的實例。</span><span class="sxs-lookup"><span data-stu-id="6758e-122">For creation events, this is the newly created instance.</span></span> <span data-ttu-id="6758e-123">針對修改事件，這是已變更之實例的新版本。</span><span class="sxs-lookup"><span data-stu-id="6758e-123">For modification events, this is the new version of the changed instance.</span></span> <span data-ttu-id="6758e-124">如果是刪除事件，這就是已刪除的實例。</span><span class="sxs-lookup"><span data-stu-id="6758e-124">For deletion events, this is the deleted instance.</span></span>

</dd> <dt>

<span data-ttu-id="6758e-125">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="6758e-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6758e-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="6758e-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6758e-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6758e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6758e-128">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="6758e-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="6758e-129">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="6758e-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="6758e-130">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="6758e-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="6758e-131">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="6758e-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="6758e-132">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="6758e-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6758e-133">備註</span><span class="sxs-lookup"><span data-stu-id="6758e-133">Remarks</span></span>

<span data-ttu-id="6758e-134">**\_ \_ InstanceOperationEvent** 類別衍生自 [**\_ \_ Event**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="6758e-134">The **\_\_InstanceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="6758e-135">不會建立 **\_ \_ InstanceOperationEvent** 的實例，只會建立其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="6758e-135">Instances of **\_\_InstanceOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="6758e-136">下列類別衍生自 **\_ \_ InstanceOperationEvent**：</span><span class="sxs-lookup"><span data-stu-id="6758e-136">The following classes derive from **\_\_InstanceOperationEvent**:</span></span>

[<span data-ttu-id="6758e-137">**\_\_InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="6758e-137">**\_\_InstanceCreationEvent**</span></span>](--instancecreationevent.md)

[<span data-ttu-id="6758e-138">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="6758e-138">**\_\_InstanceModificationEvent**</span></span>](--instancemodificationevent.md)

[<span data-ttu-id="6758e-139">**\_\_InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="6758e-139">**\_\_InstanceDeletionEvent**</span></span>](--instancedeletionevent.md)

<span data-ttu-id="6758e-140">**概觀**</span><span class="sxs-lookup"><span data-stu-id="6758e-140">**Overview**</span></span>

<span data-ttu-id="6758e-141">就像 WMI 類別一樣，它代表可使用 WMI 管理的每種系統資源類型，有一個 WMI 類別代表每個 WMI 事件種類。</span><span class="sxs-lookup"><span data-stu-id="6758e-141">Just as there is a WMI class that represents each type of system resource that can be managed using WMI, there is a WMI class that represents each type of WMI event.</span></span> <span data-ttu-id="6758e-142">當 WMI 可以監視的事件發生時，就會建立對應 WMI 事件類別的實例。</span><span class="sxs-lookup"><span data-stu-id="6758e-142">When an event that can be monitored by WMI occurs, an instance of the corresponding WMI event class is created.</span></span> <span data-ttu-id="6758e-143">建立實例時，就會發生 WMI 事件。</span><span class="sxs-lookup"><span data-stu-id="6758e-143">A WMI event occurs when that instance is created.</span></span>

<span data-ttu-id="6758e-144">Wmi 事件類別共有三種主要類型，這些類別都是衍生自 [**\_ \_ 事件**](--event.md)WMI 類別：內部事件、外建事件和計時器事件。</span><span class="sxs-lookup"><span data-stu-id="6758e-144">There are three major types of WMI event classes, all of which are derived from the [**\_\_Event**](--event.md) WMI class: Intrinsic Events, Extrinsic Events, and Timer Events.</span></span> <span data-ttu-id="6758e-145">內建事件接著會以三個衍生自 **\_ \_ 事件** 類別的不同類別來表示： [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md)、 **\_ \_ InstanceOperationEvent** 和 [**\_ \_ ClassOperationEvent**](--classoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="6758e-145">Intrinsic Events, in turn, are represented by three distinct classes derived from the **\_\_Event** class: [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md), **\_\_InstanceOperationEvent**, and [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="6758e-146">內建事件</span><span class="sxs-lookup"><span data-stu-id="6758e-146">Intrinsic Events</span></span>

<span data-ttu-id="6758e-147">內建事件是用來監視 CIM 存放庫中的類別所代表的資源。</span><span class="sxs-lookup"><span data-stu-id="6758e-147">Intrinsic events are used to monitor a resource represented by a class in the CIM repository.</span></span> <span data-ttu-id="6758e-148">每個資源都會以類別的實例來表示。</span><span class="sxs-lookup"><span data-stu-id="6758e-148">Each resource is represented by an instance of a class.</span></span> <span data-ttu-id="6758e-149">這表示使用 WMI 監視資源其實牽涉到監視對應至資源的實例。</span><span class="sxs-lookup"><span data-stu-id="6758e-149">This means that monitoring a resource using WMI actually involves monitoring the instances that correspond to the resource.</span></span>

<span data-ttu-id="6758e-150">內建事件也可以用來監視儲存機制中的命名空間或類別的變更。</span><span class="sxs-lookup"><span data-stu-id="6758e-150">Intrinsic events can also be used to monitor changes to a namespace or class in the repository.</span></span> <span data-ttu-id="6758e-151">不過，監視命名空間或類別的變更對於系統管理員而言的價值有限。</span><span class="sxs-lookup"><span data-stu-id="6758e-151">However, monitoring changes to namespaces or classes is of limited value to system administrators.</span></span>

<span data-ttu-id="6758e-152">內建事件是以衍生自 \_ \_ InstanceOperationEvent、 \_ \_ NamespaceOperationEvent 或 \_ \_ ClassOperationEvent 之類別的實例來表示。</span><span class="sxs-lookup"><span data-stu-id="6758e-152">An intrinsic event is represented by an instance of a class derived from \_\_InstanceOperationEvent, \_\_NamespaceOperationEvent, or \_\_ClassOperationEvent.</span></span> <span data-ttu-id="6758e-153">對 WMI 中的實例所做的任何變更，都會以 \_ \_ InstanceOperationEvent 類別和衍生自它的類別來表示： \_ \_ InstanceCreationEvent、 \_ \_ InstanceModificationEvent 和 \_ \_ InstanceDeletionEvent。</span><span class="sxs-lookup"><span data-stu-id="6758e-153">Any changes to instances in WMI are represented by the \_\_InstanceOperationEvent class and the classes derived from it: \_\_InstanceCreationEvent, \_\_InstanceModificationEvent, and \_\_InstanceDeletionEvent.</span></span>

<span data-ttu-id="6758e-154">使用 WMI 監視資源涉及監視實例，而實例的所有變更都會以 \_ \_ InstanceOperationEvent 和衍生自它的類別來表示。</span><span class="sxs-lookup"><span data-stu-id="6758e-154">Monitoring resources using WMI involves monitoring instances and all changes to instances are represented by \_\_InstanceOperationEvent and the classes derived from it.</span></span> <span data-ttu-id="6758e-155">這表示監視資源最後牽涉到監視 \_ \_ InstanceOperationEvent 衍生類別的實例。</span><span class="sxs-lookup"><span data-stu-id="6758e-155">This means that monitoring resources ultimately involves monitoring instances of \_\_InstanceOperationEvent-derived classes.</span></span>

<span data-ttu-id="6758e-156">您可以發出以 WQL 表示的通知查詢，在其中一個類別的實例中註冊感興趣的人。</span><span class="sxs-lookup"><span data-stu-id="6758e-156">You register interest in instances of one of these classes by issuing a notification query expressed in WQL.</span></span> <span data-ttu-id="6758e-157">查詢使用類似下面的語法：</span><span class="sxs-lookup"><span data-stu-id="6758e-157">The query uses syntax similar to the following:</span></span>

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

<span data-ttu-id="6758e-158">如需使用 WMI 實例事件來監視電腦活動的更長討論，請參閱 [如何使用單一腳本來監視不同類型的事件？](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span><span class="sxs-lookup"><span data-stu-id="6758e-158">For a longer discussion of using the WMI instance events to monitor computer activity, see [How Can I Monitor for Different Types of Events With Just One Script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="6758e-159">範例</span><span class="sxs-lookup"><span data-stu-id="6758e-159">Examples</span></span>

<span data-ttu-id="6758e-160">TechNet 資源庫上的 [監視器進程事件](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f)VBScript 程式碼範例會使用 **\_ \_ InstanceOperationEvent** 來監視 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的第一個 WMI 實例事件。</span><span class="sxs-lookup"><span data-stu-id="6758e-160">The [Monitor process event](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript code sample on TechNet Gallery uses **\_\_InstanceOperationEvent** to monitors the first WMI instance event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="6758e-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="6758e-161">Requirements</span></span>



| <span data-ttu-id="6758e-162">需求</span><span class="sxs-lookup"><span data-stu-id="6758e-162">Requirement</span></span> | <span data-ttu-id="6758e-163">值</span><span class="sxs-lookup"><span data-stu-id="6758e-163">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6758e-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6758e-164">Minimum supported client</span></span><br/> | <span data-ttu-id="6758e-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6758e-165">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6758e-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6758e-166">Minimum supported server</span></span><br/> | <span data-ttu-id="6758e-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6758e-167">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6758e-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="6758e-168">Namespace</span></span><br/>                | <span data-ttu-id="6758e-169">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="6758e-169">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6758e-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6758e-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6758e-171">**\_\_事件**</span><span class="sxs-lookup"><span data-stu-id="6758e-171">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="6758e-172">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="6758e-172">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="6758e-173">判斷要接收的事件種類</span><span class="sxs-lookup"><span data-stu-id="6758e-173">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="6758e-174">根據事件寫入記錄檔</span><span class="sxs-lookup"><span data-stu-id="6758e-174">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

