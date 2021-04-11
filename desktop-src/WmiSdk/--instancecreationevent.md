---
description: 報告實例建立事件，這是在新的實例新增至命名空間時所產生的內建事件種類。
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: __InstanceCreationEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194719"
---
# <a name="__instancecreationevent-class"></a><span data-ttu-id="dcdb1-103">\_\_InstanceCreationEvent 類別</span><span class="sxs-lookup"><span data-stu-id="dcdb1-103">\_\_InstanceCreationEvent class</span></span>

<span data-ttu-id="dcdb1-104">**\_ \_ InstanceCreationEvent** 系統類別會報告實例建立事件，這是在新的實例新增至命名空間時所產生的內建 [事件](determining-the-type-of-event-to-receive.md)類型。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-104">The **\_\_InstanceCreationEvent** system class reports an instance creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a new instance is added to the namespace.</span></span>

<span data-ttu-id="dcdb1-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dcdb1-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcdb1-107">語法</span><span class="sxs-lookup"><span data-stu-id="dcdb1-107">Syntax</span></span>

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="dcdb1-108">成員</span><span class="sxs-lookup"><span data-stu-id="dcdb1-108">Members</span></span>

<span data-ttu-id="dcdb1-109">**\_ \_ InstanceCreationEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dcdb1-109">The **\_\_InstanceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="dcdb1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="dcdb1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dcdb1-111">屬性</span><span class="sxs-lookup"><span data-stu-id="dcdb1-111">Properties</span></span>

<span data-ttu-id="dcdb1-112">**\_ \_ InstanceCreationEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-112">The **\_\_InstanceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dcdb1-113">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="dcdb1-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdb1-114">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="dcdb1-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dcdb1-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dcdb1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdb1-116">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="dcdb1-117">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcdb1-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="dcdb1-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdb1-119">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="dcdb1-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="dcdb1-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dcdb1-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdb1-121">所建立之實例的複本。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-121">Copy of the instance that was created.</span></span> <span data-ttu-id="dcdb1-122">這個屬性繼承自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcdb1-123">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="dcdb1-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcdb1-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="dcdb1-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dcdb1-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dcdb1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcdb1-126">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="dcdb1-127">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="dcdb1-128">這項資訊是 (UTC) 格式的國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="dcdb1-129">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="dcdb1-130">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcdb1-131">備註</span><span class="sxs-lookup"><span data-stu-id="dcdb1-131">Remarks</span></span>

<span data-ttu-id="dcdb1-132">**\_ \_ InstanceCreationEvent** 類別衍生自 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md)。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-132">The **\_\_InstanceCreationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="dcdb1-133">**建立資源： \_ \_ InstanceCreationEvent**</span><span class="sxs-lookup"><span data-stu-id="dcdb1-133">**Creation of a resource: \_\_InstanceCreationEvent**</span></span>

<span data-ttu-id="dcdb1-134">假設您想要在特定電腦上執行「記事本」時收到通知。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-134">Suppose you are interested in receiving a notification if Notepad is run on a certain computer.</span></span> <span data-ttu-id="dcdb1-135">當「記事本」執行時，會建立對應的進程。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-135">When Notepad runs, a corresponding process is created.</span></span> <span data-ttu-id="dcdb1-136">您可以使用 WMI 來管理處理程式，並以 Win32 \_ 進程類別來表示。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-136">Processes can be managed by using WMI and are represented by the Win32\_Process class.</span></span> <span data-ttu-id="dcdb1-137">當「記事本」開始執行時，Win32 進程類別的對應實例 \_ 會變成可透過 WMI 使用。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-137">When Notepad starts running, a corresponding instance of the Win32\_Process class becomes available through WMI.</span></span> <span data-ttu-id="dcdb1-138">如果您已在此事件 (註冊適當的事件通知查詢) ，此實例的可用性會導致建立 **\_ \_ InstanceCreationEvent** 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-138">If you have registered your interest in this event (by issuing the appropriate event notification query), the availability of this instance results in the creation of an instance of the **\_\_InstanceCreationEvent** class.</span></span>

<span data-ttu-id="dcdb1-139">要求建立資源和使用內建事件之通知的通知查詢，全都使用類似下面的語法：</span><span class="sxs-lookup"><span data-stu-id="dcdb1-139">Notification queries that request notification of the creation of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

<span data-ttu-id="dcdb1-140">如需使用 **\_ \_ InstanceCreationEvent** 作為監視檔案系統之方法的更大討論，請參閱 CodeProject 上的 [WMI 和檔案系統監視](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring)。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-140">For a larger discussion of using **\_\_InstanceCreationEvent** as a way to monitor file systems, see [WMI and File System Monitoring](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) on CodeProject.</span></span>

## <a name="examples"></a><span data-ttu-id="dcdb1-141">範例</span><span class="sxs-lookup"><span data-stu-id="dcdb1-141">Examples</span></span>

<span data-ttu-id="dcdb1-142">在 TechNet 資源庫上 [建立永久性 wmi 事件註冊來監視](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2)檔案 PowerShell 範例使用 **\_ \_ InstanceCreationEvent** 做為複雜字集的一部分，以設定永久的 wmi 事件註冊。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-142">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a complex script to set up a permanent WMI event registration.</span></span>

<span data-ttu-id="dcdb1-143">TechNet 資源庫上的 [powershell WMI 永久事件](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262)powershell 範例會使用 **\_ \_ InstanceCreationEvent** 做為設定永久事件註冊的示範腳本的一部分。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-143">The [PowerShell WMI Permanent Events](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a demonstration script for setting up a permanent event registration.</span></span>

<span data-ttu-id="dcdb1-144">TechNet 上的 [監視器進程建立事件](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d)VBScript 範例使用 **\_ \_ InstanceCreationEvent** 來監視 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的第一個 WMI 實例建立事件。</span><span class="sxs-lookup"><span data-stu-id="dcdb1-144">The [Monitor process creation event](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) VBScript sample on TechNet uses **\_\_InstanceCreationEvent** to monitors the first WMI instance creation event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcdb1-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcdb1-145">Requirements</span></span>



| <span data-ttu-id="dcdb1-146">需求</span><span class="sxs-lookup"><span data-stu-id="dcdb1-146">Requirement</span></span> | <span data-ttu-id="dcdb1-147">值</span><span class="sxs-lookup"><span data-stu-id="dcdb1-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="dcdb1-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dcdb1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="dcdb1-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dcdb1-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="dcdb1-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dcdb1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="dcdb1-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcdb1-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="dcdb1-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="dcdb1-152">Namespace</span></span><br/>                | <span data-ttu-id="dcdb1-153">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="dcdb1-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="dcdb1-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcdb1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcdb1-155">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="dcdb1-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="dcdb1-156">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="dcdb1-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

