---
description: 永久事件取用者的註冊需要 \_ \_ >eventfilter 系統類別的實例。
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: __EventFilter 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983724"
---
# <a name="__eventfilter-class"></a><span data-ttu-id="14c5b-103">\_\_>eventfilter 類別</span><span class="sxs-lookup"><span data-stu-id="14c5b-103">\_\_EventFilter class</span></span>

<span data-ttu-id="14c5b-104">永久事件取用者的註冊需要 **\_ \_ >eventfilter** 系統類別的實例。</span><span class="sxs-lookup"><span data-stu-id="14c5b-104">The registration of a permanent event consumer requires an instance of the **\_\_EventFilter** system class.</span></span>

<span data-ttu-id="14c5b-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="14c5b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="14c5b-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="14c5b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c5b-107">語法</span><span class="sxs-lookup"><span data-stu-id="14c5b-107">Syntax</span></span>

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a><span data-ttu-id="14c5b-108">成員</span><span class="sxs-lookup"><span data-stu-id="14c5b-108">Members</span></span>

<span data-ttu-id="14c5b-109">**\_ \_ >eventfilter** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="14c5b-109">The **\_\_EventFilter** class has these types of members:</span></span>

-   [<span data-ttu-id="14c5b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="14c5b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14c5b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="14c5b-111">Properties</span></span>

<span data-ttu-id="14c5b-112">**\_ \_ >eventfilter** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="14c5b-112">The **\_\_EventFilter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14c5b-113">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="14c5b-113">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c5b-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="14c5b-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="14c5b-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="14c5b-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="14c5b-116">安全識別碼 (SID) ，可唯一識別建立此篩選器的使用者。</span><span class="sxs-lookup"><span data-stu-id="14c5b-116">Security identifier (SID) that uniquely identifies the user who creates this filter.</span></span> <span data-ttu-id="14c5b-117">Windows Management Instrumentation (WMI) 會將建立 **\_ \_ >eventfilter** 實例的使用者 sid，或系統管理員 sid 儲存在不同的作業系統上。</span><span class="sxs-lookup"><span data-stu-id="14c5b-117">Windows Management Instrumentation (WMI) stores the SID of the user that creates an instance of **\_\_EventFilter** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="14c5b-118">如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="14c5b-118">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="14c5b-119">**EventAccess**</span><span class="sxs-lookup"><span data-stu-id="14c5b-119">**EventAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c5b-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="14c5b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c5b-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="14c5b-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="14c5b-122">安全描述項定義語言中的安全描述項 (SD)  (SDDL) ，可控制傳遞至篩選之事件的存取權。</span><span class="sxs-lookup"><span data-stu-id="14c5b-122">Security descriptor (SD) in Security Descriptor Definition Language (SDDL) that controls access for events delivered to the filter.</span></span> <span data-ttu-id="14c5b-123">您可以使用這個屬性來指定只能將特定帳戶之安全性內容中的事件傳遞給此篩選器。</span><span class="sxs-lookup"><span data-stu-id="14c5b-123">Use this property to specify that only events in the security context of specific accounts can be delivered to this filter.</span></span> <span data-ttu-id="14c5b-124">例如，當特定使用者產生特定事件時，永久事件取用者可能會清除安全性記錄。</span><span class="sxs-lookup"><span data-stu-id="14c5b-124">For example, a permanent event consumer may clear the security logs only when a specific event is generated by a specific user.</span></span> <span data-ttu-id="14c5b-125">若要指定可以將事件發佈到此篩選器的使用者，請在 [[**安全 \_ 描述項**](--event.md)] 屬性的 [存取控制] 專案中，使用 [ **WBEM] 右邊的 \_ \_ 發佈** 遮罩 (ACE) 。</span><span class="sxs-lookup"><span data-stu-id="14c5b-125">To specify who can publish events to this filter, use the **WBEM\_RIGHT\_PUBLISH** mask in the Access Control Entry (ACE) for the [**SECURITY\_DESCRIPTOR**](--event.md) property.</span></span> <span data-ttu-id="14c5b-126">如需詳細資訊，請參閱 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language)。</span><span class="sxs-lookup"><span data-stu-id="14c5b-126">For more information, see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span> <span data-ttu-id="14c5b-127">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="14c5b-127">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span> <span data-ttu-id="14c5b-128">如需詳細資訊和範例，請參閱取代：[安全地接收事件](receiving-events-securely.md)。</span><span class="sxs-lookup"><span data-stu-id="14c5b-128">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="14c5b-129">您可以設定事件存取安全描述項，只允許在本機系統帳戶產生事件時傳遞事件。</span><span class="sxs-lookup"><span data-stu-id="14c5b-129">You can configure an event access security descriptor to allow an event to be delivered only when the local system account generates the event.</span></span> <span data-ttu-id="14c5b-130">如需建立安全描述項及授權存取的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="14c5b-130">For more information about creating security descriptor and authorizing access, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="14c5b-131">範例：下列 SDDL 字串只允許系統管理員將事件提供給篩選準則。</span><span class="sxs-lookup"><span data-stu-id="14c5b-131">Example: The following SDDL string allows only administrators to provide events to the filter.</span></span> <span data-ttu-id="14c5b-132">提供事件所需的正確之處是 (x80) 的 **WBEM \_ 正確 \_ 發佈** 。</span><span class="sxs-lookup"><span data-stu-id="14c5b-132">The right required to provide events is **WBEM\_RIGHT\_PUBLISH** (x80).</span></span>


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

<span data-ttu-id="14c5b-133">**EventNamespace**</span><span class="sxs-lookup"><span data-stu-id="14c5b-133">**EventNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c5b-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="14c5b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c5b-135">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="14c5b-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="14c5b-136">用於跨命名空間訂閱之事件實例的命名空間。</span><span class="sxs-lookup"><span data-stu-id="14c5b-136">Namespace of the event instance used for cross-namespace subscriptions.</span></span>

</dd> <dt>

<span data-ttu-id="14c5b-137">**名稱**</span><span class="sxs-lookup"><span data-stu-id="14c5b-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c5b-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="14c5b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c5b-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="14c5b-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="14c5b-140">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="14c5b-140">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="14c5b-141">事件篩選器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="14c5b-141">Unique identifier of an event filter.</span></span> <span data-ttu-id="14c5b-142">因為事件篩選器只會由 WMI 在內部使用，建議您將此屬性設定為全域唯一識別碼 (**GUID**) 轉換成字串。</span><span class="sxs-lookup"><span data-stu-id="14c5b-142">Because an event filter is only used internally by WMI, it is recommended that you set this property to a globally unique identifier (**GUID**) converted to a string.</span></span> <span data-ttu-id="14c5b-143">不過，取用者可以使用任何私用配置來篩選名稱，只要不會與其他篩選發生衝突。</span><span class="sxs-lookup"><span data-stu-id="14c5b-143">However, consumers can use any private scheme for a filter name as long as there is not a conflict with other filters.</span></span>

</dd> <dt>

<span data-ttu-id="14c5b-144">**查詢**</span><span class="sxs-lookup"><span data-stu-id="14c5b-144">**Query**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c5b-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="14c5b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c5b-146">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="14c5b-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="14c5b-147">Windows Management Instrumentation Query Language (WQL) 事件查詢，該查詢會指定取用者通知的事件組，以及通知的特定條件。</span><span class="sxs-lookup"><span data-stu-id="14c5b-147">Windows Management Instrumentation Query Language (WQL) event query that specifies the set of events for consumer notification, and the specific conditions for notification.</span></span>

</dd> <dt>

<span data-ttu-id="14c5b-148">**QueryLanguage**</span><span class="sxs-lookup"><span data-stu-id="14c5b-148">**QueryLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14c5b-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="14c5b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14c5b-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="14c5b-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="14c5b-151">用於查詢的語言。</span><span class="sxs-lookup"><span data-stu-id="14c5b-151">Language used for the query.</span></span> <span data-ttu-id="14c5b-152">因為 WMI 目前僅支援 WMI 查詢語言 (WQL) 作為查詢語言，所以此屬性必須設定為 "WQL"。</span><span class="sxs-lookup"><span data-stu-id="14c5b-152">Because WMI currently supports only WMI Query Language (WQL) as a query language, this property must be set to "WQL".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14c5b-153">備註</span><span class="sxs-lookup"><span data-stu-id="14c5b-153">Remarks</span></span>

<span data-ttu-id="14c5b-154">**\_ \_ >eventfilter** 類別衍生自 [**\_ \_ IndicationRelated**](--indicationrelated.md)。</span><span class="sxs-lookup"><span data-stu-id="14c5b-154">The **\_\_EventFilter** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md).</span></span>

## <a name="examples"></a><span data-ttu-id="14c5b-155">範例</span><span class="sxs-lookup"><span data-stu-id="14c5b-155">Examples</span></span>

<span data-ttu-id="14c5b-156">在 TechNet 資源庫上 [建立永久性 wmi 事件註冊來監視](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2)檔案 PowerShell 範例使用 **\_ \_ >eventfilter** 做為複雜字集的一部分，以設定永久的 wmi 事件註冊。</span><span class="sxs-lookup"><span data-stu-id="14c5b-156">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_EventFilter** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c5b-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="14c5b-157">Requirements</span></span>



| <span data-ttu-id="14c5b-158">需求</span><span class="sxs-lookup"><span data-stu-id="14c5b-158">Requirement</span></span> | <span data-ttu-id="14c5b-159">值</span><span class="sxs-lookup"><span data-stu-id="14c5b-159">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="14c5b-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14c5b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="14c5b-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14c5b-161">Windows Vista</span></span><br/>       |
| <span data-ttu-id="14c5b-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14c5b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="14c5b-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14c5b-163">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="14c5b-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="14c5b-164">Namespace</span></span><br/>                | <span data-ttu-id="14c5b-165">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="14c5b-165">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="14c5b-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14c5b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c5b-167">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="14c5b-167">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="14c5b-168">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="14c5b-168">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="14c5b-169">建立事件篩選器</span><span class="sxs-lookup"><span data-stu-id="14c5b-169">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="14c5b-170">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="14c5b-170">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="14c5b-171">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="14c5b-171">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="14c5b-172">監視事件</span><span class="sxs-lookup"><span data-stu-id="14c5b-172">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="14c5b-173">標準取用者類別</span><span class="sxs-lookup"><span data-stu-id="14c5b-173">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="14c5b-174">保護 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="14c5b-174">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

