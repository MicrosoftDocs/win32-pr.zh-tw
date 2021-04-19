---
description: 報告實例刪除事件，這是從命名空間中刪除實例時所產生的內建事件種類。
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: __InstanceDeletionEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975801"
---
# <a name="__instancedeletionevent-class"></a><span data-ttu-id="3ecc7-103">\_\_InstanceDeletionEvent 類別</span><span class="sxs-lookup"><span data-stu-id="3ecc7-103">\_\_InstanceDeletionEvent class</span></span>

<span data-ttu-id="3ecc7-104">**\_ \_ InstanceDeletionEvent** 系統類別會報告實例刪除事件，這是從命名空間中刪除實例時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-104">The **\_\_InstanceDeletionEvent** system class reports an instance deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance is deleted from the namespace.</span></span>

<span data-ttu-id="3ecc7-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3ecc7-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ecc7-107">語法</span><span class="sxs-lookup"><span data-stu-id="3ecc7-107">Syntax</span></span>

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="3ecc7-108">成員</span><span class="sxs-lookup"><span data-stu-id="3ecc7-108">Members</span></span>

<span data-ttu-id="3ecc7-109">**\_ \_ InstanceDeletionEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3ecc7-109">The **\_\_InstanceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="3ecc7-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3ecc7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ecc7-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3ecc7-111">Properties</span></span>

<span data-ttu-id="3ecc7-112">**\_ \_ InstanceDeletionEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-112">The **\_\_InstanceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ecc7-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="3ecc7-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ecc7-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="3ecc7-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3ecc7-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ecc7-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ecc7-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="3ecc7-117">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ecc7-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="3ecc7-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ecc7-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="3ecc7-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="3ecc7-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ecc7-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ecc7-121">已刪除之實例的複本。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-121">Copy of the instance that was deleted.</span></span> <span data-ttu-id="3ecc7-122">這個屬性繼承自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ecc7-123">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="3ecc7-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ecc7-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="3ecc7-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ecc7-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3ecc7-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ecc7-126">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="3ecc7-127">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="3ecc7-128">這項資訊是 (UTC) 格式的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="3ecc7-129">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="3ecc7-130">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ecc7-131">備註</span><span class="sxs-lookup"><span data-stu-id="3ecc7-131">Remarks</span></span>

<span data-ttu-id="3ecc7-132">**\_ \_ InstanceDeletionEvent** 類別衍生自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-132">The **\_\_InstanceDeletionEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="3ecc7-133">**刪除資源： \_ \_ InstanceDeletionEvent**</span><span class="sxs-lookup"><span data-stu-id="3ecc7-133">**Deletion of a resource: \_\_InstanceDeletionEvent**</span></span>

<span data-ttu-id="3ecc7-134">如果您想要確保特定的防毒程式會繼續在電腦上執行，您可以撰寫腳本來監視電腦上的處理常式，以判斷是否有任何停止。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-134">If you want to ensure that a particular antivirus scanner program continues to run on a computer, you can write a script that monitors the processes on the computer to determine whether any of them stop.</span></span>

<span data-ttu-id="3ecc7-135">要求刪除資源和使用內建事件之通知的通知查詢，全都使用類似下面的語法：</span><span class="sxs-lookup"><span data-stu-id="3ecc7-135">Notification queries that request notification of the deletion of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a><span data-ttu-id="3ecc7-136">範例</span><span class="sxs-lookup"><span data-stu-id="3ecc7-136">Examples</span></span>

<span data-ttu-id="3ecc7-137">TechNet 資源庫上的 [監視器進程刪除事件](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38)VBScript 程式碼範例會使用 **\_ \_ InstanceDeletionEvent** 來監視 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)第一次出現的 WMI 實例刪除事件。</span><span class="sxs-lookup"><span data-stu-id="3ecc7-137">The [Monitor process deletion event](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript code sample on TechNet Gallery uses **\_\_InstanceDeletionEvent** to monitor the first occurrence of a WMI instance deletion event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecc7-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ecc7-138">Requirements</span></span>



| <span data-ttu-id="3ecc7-139">需求</span><span class="sxs-lookup"><span data-stu-id="3ecc7-139">Requirement</span></span> | <span data-ttu-id="3ecc7-140">值</span><span class="sxs-lookup"><span data-stu-id="3ecc7-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3ecc7-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ecc7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3ecc7-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ecc7-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3ecc7-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ecc7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3ecc7-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ecc7-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3ecc7-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="3ecc7-145">Namespace</span></span><br/>                | <span data-ttu-id="3ecc7-146">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="3ecc7-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3ecc7-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ecc7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecc7-148">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="3ecc7-148">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="3ecc7-149">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="3ecc7-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

