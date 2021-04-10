---
description: Win32 \_ DeviceChangeEvent ABSTRACT WMI 類別代表在電腦系統上新增、移除或修改裝置所產生的裝置變更事件。
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Win32_DeviceChangeEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceChangeEvent
- Win32_DeviceChangeEvent.SECURITY_DESCRIPTOR
- Win32_DeviceChangeEvent.TIME_CREATED
- Win32_DeviceChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f97ab262d95b70a69b06e15202a78d5c1364f90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689192"
---
# <a name="win32_devicechangeevent-class"></a><span data-ttu-id="44fac-103">Win32 \_ DeviceChangeEvent 類別</span><span class="sxs-lookup"><span data-stu-id="44fac-103">Win32\_DeviceChangeEvent class</span></span>

<span data-ttu-id="44fac-104">**Win32 \_ DeviceChangeEvent** abstract [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表在電腦系統上新增、移除或修改裝置所產生的裝置變更事件。</span><span class="sxs-lookup"><span data-stu-id="44fac-104">The **Win32\_DeviceChangeEvent** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents device change events that result from the addition, removal, or modification of devices on the computer system.</span></span> <span data-ttu-id="44fac-105">這包括硬體設定 (銜接和移除) 、硬體狀態或新對應的裝置 (對應網路磁碟機機) 的變更。</span><span class="sxs-lookup"><span data-stu-id="44fac-105">This includes changes in the hardware configuration (docking and undocking), the hardware state, or newly mapped devices (mapping of a network drive).</span></span> <span data-ttu-id="44fac-106">例如，在傳送 WM DEVICECHANGE 訊息時，裝置已變更 \_ 。</span><span class="sxs-lookup"><span data-stu-id="44fac-106">For example, a device has changed when a WM\_DEVICECHANGE message is sent.</span></span>

<span data-ttu-id="44fac-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="44fac-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="44fac-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="44fac-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fac-109">語法</span><span class="sxs-lookup"><span data-stu-id="44fac-109">Syntax</span></span>

``` syntax
[UUID("0DE6AAF8-49F1-4868-B3D4-61CB69BA4322"), AMENDMENT]
class Win32_DeviceChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="44fac-110">成員</span><span class="sxs-lookup"><span data-stu-id="44fac-110">Members</span></span>

<span data-ttu-id="44fac-111">**Win32 \_ DeviceChangeEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="44fac-111">The **Win32\_DeviceChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="44fac-112">屬性</span><span class="sxs-lookup"><span data-stu-id="44fac-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44fac-113">屬性</span><span class="sxs-lookup"><span data-stu-id="44fac-113">Properties</span></span>

<span data-ttu-id="44fac-114">**Win32 \_ DeviceChangeEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="44fac-114">The **Win32\_DeviceChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44fac-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="44fac-115">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44fac-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="44fac-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44fac-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44fac-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44fac-118">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32APIDevice management messages \| wm \_ DEVICECHANGE \| WParam"，"Win32APIDevice management messages \| wm \_ SETTINGCHANGE" ) </span><span class="sxs-lookup"><span data-stu-id="44fac-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="44fac-119">已發生的事件變更通知類型。</span><span class="sxs-lookup"><span data-stu-id="44fac-119">Type of event change notification that has occurred.</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="44fac-120">設定 **已變更** (1) </span><span class="sxs-lookup"><span data-stu-id="44fac-120">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="44fac-121">**裝置抵達** (2) </span><span class="sxs-lookup"><span data-stu-id="44fac-121">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="44fac-122">**移除裝置** (3) </span><span class="sxs-lookup"><span data-stu-id="44fac-122">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="44fac-123">**銜接** (4) </span><span class="sxs-lookup"><span data-stu-id="44fac-123">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44fac-124">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="44fac-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44fac-125">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="44fac-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="44fac-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44fac-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44fac-127">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="44fac-127">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="44fac-128">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="44fac-128">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="44fac-129">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](/windows/desktop/WmiSdk/wmi-security-constants)。</span><span class="sxs-lookup"><span data-stu-id="44fac-129">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="44fac-130">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="44fac-130">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44fac-131">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="44fac-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44fac-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="44fac-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44fac-133">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="44fac-133">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="44fac-134">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="44fac-134">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="44fac-135">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="44fac-135">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="44fac-136">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="44fac-136">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="44fac-137">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="44fac-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44fac-138">備註</span><span class="sxs-lookup"><span data-stu-id="44fac-138">Remarks</span></span>

<span data-ttu-id="44fac-139">**Win32 \_ DeviceChangeEvent** 是衍生自 [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)的抽象類別。</span><span class="sxs-lookup"><span data-stu-id="44fac-139">The **Win32\_DeviceChangeEvent** is an abstract class derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="44fac-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="44fac-140">Requirements</span></span>



| <span data-ttu-id="44fac-141">需求</span><span class="sxs-lookup"><span data-stu-id="44fac-141">Requirement</span></span> | <span data-ttu-id="44fac-142">值</span><span class="sxs-lookup"><span data-stu-id="44fac-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44fac-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44fac-143">Minimum supported client</span></span><br/> | <span data-ttu-id="44fac-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44fac-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44fac-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44fac-145">Minimum supported server</span></span><br/> | <span data-ttu-id="44fac-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44fac-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44fac-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="44fac-147">Namespace</span></span><br/>                | <span data-ttu-id="44fac-148">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="44fac-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44fac-149">MOF</span><span class="sxs-lookup"><span data-stu-id="44fac-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44fac-150"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="44fac-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44fac-151">DLL</span><span class="sxs-lookup"><span data-stu-id="44fac-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44fac-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44fac-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44fac-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44fac-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fac-154">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="44fac-154">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

<span data-ttu-id="44fac-155">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="44fac-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

