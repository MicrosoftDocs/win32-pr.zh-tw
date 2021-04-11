---
description: 報告實例修改事件，這是在命名空間中的實例變更時所產生的內建事件種類。
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: __InstanceModificationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850788"
---
# <a name="__instancemodificationevent-class"></a><span data-ttu-id="ec65f-103">\_\_InstanceModificationEvent 類別</span><span class="sxs-lookup"><span data-stu-id="ec65f-103">\_\_InstanceModificationEvent class</span></span>

<span data-ttu-id="ec65f-104">**\_ \_ InstanceModificationEvent** 系統類別會報告實例修改事件，這是在命名空間中的實例變更時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。</span><span class="sxs-lookup"><span data-stu-id="ec65f-104">The **\_\_InstanceModificationEvent** system class reports an instance modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance changes in the namespace.</span></span>

<span data-ttu-id="ec65f-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ec65f-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ec65f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec65f-107">語法</span><span class="sxs-lookup"><span data-stu-id="ec65f-107">Syntax</span></span>

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="ec65f-108">成員</span><span class="sxs-lookup"><span data-stu-id="ec65f-108">Members</span></span>

<span data-ttu-id="ec65f-109">**\_ \_ InstanceModificationEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ec65f-109">The **\_\_InstanceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ec65f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ec65f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec65f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ec65f-111">Properties</span></span>

<span data-ttu-id="ec65f-112">**\_ \_ InstanceModificationEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ec65f-112">The **\_\_InstanceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec65f-113">**PreviousInstance**</span><span class="sxs-lookup"><span data-stu-id="ec65f-113">**PreviousInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec65f-114">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="ec65f-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ec65f-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec65f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec65f-116">修改之前的實例複本。</span><span class="sxs-lookup"><span data-stu-id="ec65f-116">Copy of the instance prior to modification.</span></span>

</dd> <dt>

<span data-ttu-id="ec65f-117">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="ec65f-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec65f-118">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="ec65f-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ec65f-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec65f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec65f-120">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="ec65f-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="ec65f-121">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="ec65f-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec65f-122">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="ec65f-122">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec65f-123">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="ec65f-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ec65f-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec65f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec65f-125">已變更之實例的新版本。</span><span class="sxs-lookup"><span data-stu-id="ec65f-125">New version of the changed instance.</span></span> <span data-ttu-id="ec65f-126">這個屬性繼承自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="ec65f-126">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec65f-127">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="ec65f-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec65f-128">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ec65f-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ec65f-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec65f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec65f-130">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="ec65f-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="ec65f-131">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="ec65f-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ec65f-132">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="ec65f-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="ec65f-133">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="ec65f-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="ec65f-134">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="ec65f-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec65f-135">備註</span><span class="sxs-lookup"><span data-stu-id="ec65f-135">Remarks</span></span>

<span data-ttu-id="ec65f-136">**\_ \_ InstanceModificationEvent** 類別衍生自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="ec65f-136">The **\_\_InstanceModificationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="ec65f-137">**修改資源： \_ \_ InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="ec65f-137">**Modification of a resource: \_\_InstanceModificationEvent**</span></span>

<span data-ttu-id="ec65f-138">假設您懷疑正在使用的管理應用程式，在您的其中一部伺服器上錯誤地變更服務的啟動類型。</span><span class="sxs-lookup"><span data-stu-id="ec65f-138">Suppose you suspect that a management application you are using is erroneously changing the startup type of a service on one of your servers.</span></span> <span data-ttu-id="ec65f-139">您想要撰寫 WMI 腳本來監視對服務的設定所做的任何修改。</span><span class="sxs-lookup"><span data-stu-id="ec65f-139">You want to write a WMI script to monitor any modifications made to the configuration of the service.</span></span> <span data-ttu-id="ec65f-140">一旦對服務進行修改，其對應的 TargetInstance 就會反映修改。</span><span class="sxs-lookup"><span data-stu-id="ec65f-140">As soon as a modification is made to a service, its corresponding TargetInstance reflects the modification.</span></span>

<span data-ttu-id="ec65f-141">如果您在此活動中註冊您的興趣，則修改服務的設定會導致建立 **\_ \_ InstanceModificationEvent** 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ec65f-141">If you register your interest in this event, a modification to the configuration of the service results in the creation of an instance of the **\_\_InstanceModificationEvent** class.</span></span>

<span data-ttu-id="ec65f-142">要求修改資源和使用內建事件的通知查詢，全都使用類似下面的語法：</span><span class="sxs-lookup"><span data-stu-id="ec65f-142">Notification queries that request notification of the modification of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a><span data-ttu-id="ec65f-143">範例</span><span class="sxs-lookup"><span data-stu-id="ec65f-143">Examples</span></span>

<span data-ttu-id="ec65f-144">TechNet 資源庫上的 [監視器進程修改事件](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079)VBScript 範例會使用 **\_ \_ InstanceModificationEvent** 來監視 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)第一次出現的 WMI 實例修改事件。</span><span class="sxs-lookup"><span data-stu-id="ec65f-144">The [Monitor process modification event](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript sample on TechNet Gallery uses **\_\_InstanceModificationEvent** to monitor the first occurrence of a WMI instance modification event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec65f-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec65f-145">Requirements</span></span>



| <span data-ttu-id="ec65f-146">需求</span><span class="sxs-lookup"><span data-stu-id="ec65f-146">Requirement</span></span> | <span data-ttu-id="ec65f-147">值</span><span class="sxs-lookup"><span data-stu-id="ec65f-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ec65f-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec65f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ec65f-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec65f-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ec65f-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec65f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ec65f-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec65f-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ec65f-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec65f-152">Namespace</span></span><br/>                | <span data-ttu-id="ec65f-153">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="ec65f-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ec65f-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec65f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec65f-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="ec65f-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="ec65f-156">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="ec65f-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

