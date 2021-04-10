---
description: Win32 \_ SystemConfigurationChangeEvent&\# 8194;WMI 類別指出系統上的裝置清單已重新整理， (已新增或移除裝置，或設定) 變更。
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Win32_SystemConfigurationChangeEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0bc479d3415906a6536c6df1d163056e94e2af76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111328"
---
# <a name="win32_systemconfigurationchangeevent-class"></a><span data-ttu-id="844f2-103">Win32 \_ SystemConfigurationChangeEvent 類別</span><span class="sxs-lookup"><span data-stu-id="844f2-103">Win32\_SystemConfigurationChangeEvent class</span></span>

<span data-ttu-id="844f2-104">**Win32 \_ SystemConfigurationChangeEvent** [WMI 類別](../wmisdk/retrieving-a-class.md)指出系統上的裝置清單已重新整理， (已新增或移除裝置，或設定) 變更。</span><span class="sxs-lookup"><span data-stu-id="844f2-104">The **Win32\_SystemConfigurationChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) indicates that the device list on the system has been refreshed (a device has been added or removed, or the configuration changed).</span></span> <span data-ttu-id="844f2-105">當傳送 "DevMgrRefreshOn<*ComputerName*>" 訊息時，就會引發事件，並建立此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="844f2-105">An event is fired and an instance of this is class created when the "DevMgrRefreshOn<*ComputerName*>" message is sent.</span></span> <span data-ttu-id="844f2-106">裝置清單的確切變更不包含在訊息中，因此需要重新整理裝置才能取得目前的系統設定。</span><span class="sxs-lookup"><span data-stu-id="844f2-106">The exact change to the device list is not contained in the message, so a device refresh is required to obtain the current system settings.</span></span> <span data-ttu-id="844f2-107">受影響的設定變更範例包括 IRQ 設定、COM 埠和 BIOS 版本。</span><span class="sxs-lookup"><span data-stu-id="844f2-107">Examples of configuration changes affected are IRQ settings, COM ports, and BIOS versions.</span></span>

<span data-ttu-id="844f2-108">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="844f2-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="844f2-109">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="844f2-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="844f2-110">語法</span><span class="sxs-lookup"><span data-stu-id="844f2-110">Syntax</span></span>

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="844f2-111">成員</span><span class="sxs-lookup"><span data-stu-id="844f2-111">Members</span></span>

<span data-ttu-id="844f2-112">**Win32 \_ SystemConfigurationChangeEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="844f2-112">The **Win32\_SystemConfigurationChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="844f2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="844f2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="844f2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="844f2-114">Properties</span></span>

<span data-ttu-id="844f2-115">**Win32 \_ SystemConfigurationChangeEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="844f2-115">The **Win32\_SystemConfigurationChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="844f2-116">**EventType**</span><span class="sxs-lookup"><span data-stu-id="844f2-116">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844f2-117">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="844f2-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="844f2-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="844f2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="844f2-119">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32APIDevice management messages \| wm \_ DEVICECHANGE \| WParam"，"Win32APIDevice management messages \| wm \_ SETTINGCHANGE" ) </span><span class="sxs-lookup"><span data-stu-id="844f2-119">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="844f2-120">已發生的事件變更通知類型。</span><span class="sxs-lookup"><span data-stu-id="844f2-120">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="844f2-121">這個屬性繼承自 [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)。</span><span class="sxs-lookup"><span data-stu-id="844f2-121">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="844f2-122">設定 **已變更** (1) </span><span class="sxs-lookup"><span data-stu-id="844f2-122">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="844f2-123">**裝置抵達** (2) </span><span class="sxs-lookup"><span data-stu-id="844f2-123">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="844f2-124">**移除裝置** (3) </span><span class="sxs-lookup"><span data-stu-id="844f2-124">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="844f2-125">**銜接** (4) </span><span class="sxs-lookup"><span data-stu-id="844f2-125">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="844f2-126">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="844f2-126">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844f2-127">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="844f2-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="844f2-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="844f2-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844f2-129">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="844f2-129">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="844f2-130">這個屬性繼承自 [**\_ \_ 事件**](../wmisdk/--event.md)。</span><span class="sxs-lookup"><span data-stu-id="844f2-130">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="844f2-131">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](../wmisdk/wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="844f2-131">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="844f2-132">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="844f2-132">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="844f2-133">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="844f2-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="844f2-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="844f2-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="844f2-135">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="844f2-135">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="844f2-136">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="844f2-136">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="844f2-137">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="844f2-137">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="844f2-138">這個屬性繼承自 [**\_ \_ 事件**](../wmisdk/--event.md)。</span><span class="sxs-lookup"><span data-stu-id="844f2-138">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="844f2-139">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="844f2-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="844f2-140">備註</span><span class="sxs-lookup"><span data-stu-id="844f2-140">Remarks</span></span>

<span data-ttu-id="844f2-141">**Win32 \_ SystemConfigurationChangeEvent** 類別衍生自 [**win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)。</span><span class="sxs-lookup"><span data-stu-id="844f2-141">The **Win32\_SystemConfigurationChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="844f2-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="844f2-142">Requirements</span></span>



| <span data-ttu-id="844f2-143">需求</span><span class="sxs-lookup"><span data-stu-id="844f2-143">Requirement</span></span> | <span data-ttu-id="844f2-144">值</span><span class="sxs-lookup"><span data-stu-id="844f2-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="844f2-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="844f2-145">Minimum supported client</span></span><br/> | <span data-ttu-id="844f2-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="844f2-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="844f2-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="844f2-147">Minimum supported server</span></span><br/> | <span data-ttu-id="844f2-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="844f2-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="844f2-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="844f2-149">Namespace</span></span><br/>                | <span data-ttu-id="844f2-150">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="844f2-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="844f2-151">MOF</span><span class="sxs-lookup"><span data-stu-id="844f2-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="844f2-152"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="844f2-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="844f2-153">DLL</span><span class="sxs-lookup"><span data-stu-id="844f2-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="844f2-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="844f2-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="844f2-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="844f2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="844f2-156">**Win32 \_ DeviceChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="844f2-156">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="844f2-157">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="844f2-157">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
