---
description: 是用來註冊永久事件取用者的抽象基類。
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: __EventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945392"
---
# <a name="__eventconsumer-class"></a><span data-ttu-id="20ac0-103">\_\_EventConsumer 類別</span><span class="sxs-lookup"><span data-stu-id="20ac0-103">\_\_EventConsumer class</span></span>

<span data-ttu-id="20ac0-104">**\_ \_ EventConsumer** 系統類別是用來註冊永久事件取用者的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="20ac0-104">The **\_\_EventConsumer** system class is an abstract base class that is used in the registration of a permanent event consumer.</span></span> <span data-ttu-id="20ac0-105">您可以從 **\_ \_ EventConsumer** 衍生新的事件取用者類別。</span><span class="sxs-lookup"><span data-stu-id="20ac0-105">You can derive a new event consumer class from **\_\_EventConsumer**.</span></span>

<span data-ttu-id="20ac0-106">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="20ac0-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="20ac0-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="20ac0-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ac0-108">語法</span><span class="sxs-lookup"><span data-stu-id="20ac0-108">Syntax</span></span>

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a><span data-ttu-id="20ac0-109">成員</span><span class="sxs-lookup"><span data-stu-id="20ac0-109">Members</span></span>

<span data-ttu-id="20ac0-110">**\_ \_ EventConsumer** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="20ac0-110">The **\_\_EventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="20ac0-111">屬性</span><span class="sxs-lookup"><span data-stu-id="20ac0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20ac0-112">屬性</span><span class="sxs-lookup"><span data-stu-id="20ac0-112">Properties</span></span>

<span data-ttu-id="20ac0-113">**\_ \_ EventConsumer** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="20ac0-113">The **\_\_EventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20ac0-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="20ac0-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac0-115">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="20ac0-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="20ac0-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20ac0-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac0-117">安全識別碼 (SID) ，可唯一識別建立篩選的使用者。</span><span class="sxs-lookup"><span data-stu-id="20ac0-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="20ac0-118">根據作業系統而定，WMI 會儲存建立 **\_ \_ EventConsumer** 實例或系統管理員 SID 之使用者的 SID。</span><span class="sxs-lookup"><span data-stu-id="20ac0-118">WMI stores the SID of the user who creates an instance of **\_\_EventConsumer** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="20ac0-119">如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="20ac0-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac0-120">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="20ac0-120">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac0-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="20ac0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac0-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20ac0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac0-123">Windows Management Instrumentation (WMI) 傳送事件的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="20ac0-123">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

</dd> <dt>

<span data-ttu-id="20ac0-124">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="20ac0-124">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac0-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="20ac0-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20ac0-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20ac0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac0-127">特定取用者的佇列上限，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="20ac0-127">Maximum queue for a specific consumer, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20ac0-128">備註</span><span class="sxs-lookup"><span data-stu-id="20ac0-128">Remarks</span></span>

<span data-ttu-id="20ac0-129">**\_ \_ EventConsumer** 類別衍生自 [**\_ \_ IndicationRelated**](--indicationrelated.md)，但沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="20ac0-129">The **\_\_EventConsumer** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which does not have properties.</span></span>

<span data-ttu-id="20ac0-130">永久取用者會定義新的取用者類別，以描述取用者接收事件通知時要採取的動作以及要處理的資料。</span><span class="sxs-lookup"><span data-stu-id="20ac0-130">Permanent consumers define new consumer classes to describe an action to take and data to be processed when consumers receive event notifications.</span></span> <span data-ttu-id="20ac0-131">永久取用者有特殊的安全性考慮。</span><span class="sxs-lookup"><span data-stu-id="20ac0-131">Permanent consumers have special security concerns.</span></span> <span data-ttu-id="20ac0-132">如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="20ac0-132">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20ac0-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="20ac0-133">Requirements</span></span>



| <span data-ttu-id="20ac0-134">需求</span><span class="sxs-lookup"><span data-stu-id="20ac0-134">Requirement</span></span> | <span data-ttu-id="20ac0-135">值</span><span class="sxs-lookup"><span data-stu-id="20ac0-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="20ac0-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20ac0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="20ac0-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20ac0-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="20ac0-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20ac0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="20ac0-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20ac0-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="20ac0-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="20ac0-140">Namespace</span></span><br/>                | <span data-ttu-id="20ac0-141">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="20ac0-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="20ac0-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20ac0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ac0-143">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="20ac0-143">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="20ac0-144">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="20ac0-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="20ac0-145">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="20ac0-145">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="20ac0-146">建立新的永久事件取用者類別</span><span class="sxs-lookup"><span data-stu-id="20ac0-146">Creating a New Permanent Event Consumer Class</span></span>](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[<span data-ttu-id="20ac0-147">建立邏輯取用者</span><span class="sxs-lookup"><span data-stu-id="20ac0-147">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="20ac0-148">保護 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="20ac0-148">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

