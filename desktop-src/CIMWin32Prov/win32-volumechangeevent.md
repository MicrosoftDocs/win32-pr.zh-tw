---
description: Win32 \_ VolumeChangeEvent 代表在電腦系統上加入磁碟機號或已載入的磁片磁碟機所產生的本機磁片磁碟機事件。
ms.assetid: 38595319-d7a1-4dcd-9ad8-a27cc484b699
ms.tgt_platform: multiple
title: Win32_VolumeChangeEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VolumeChangeEvent
- Win32_VolumeChangeEvent.SECURITY_DESCRIPTOR
- Win32_VolumeChangeEvent.TIME_CREATED
- Win32_VolumeChangeEvent.EventType
- Win32_VolumeChangeEvent.DriveName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7610cae8d0cc746774b99a101e3c6aaf1f8a64d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110217"
---
# <a name="win32_volumechangeevent-class"></a><span data-ttu-id="b8239-103">Win32 \_ VolumeChangeEvent 類別</span><span class="sxs-lookup"><span data-stu-id="b8239-103">Win32\_VolumeChangeEvent class</span></span>

<span data-ttu-id="b8239-104">**Win32 \_ VolumeChangeEvent** [WMI 類別](../wmisdk/retrieving-a-class.md)代表在電腦系統上新增磁碟機號或掛接的磁片磁碟機所產生的本機磁片磁碟機事件。</span><span class="sxs-lookup"><span data-stu-id="b8239-104">The **Win32\_VolumeChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents a local drive event that results from the addition of a drive letter or mounted drive on the computer system.</span></span> <span data-ttu-id="b8239-105">目前不支援網路磁碟機機。</span><span class="sxs-lookup"><span data-stu-id="b8239-105">Network drives are not currently supported.</span></span>

<span data-ttu-id="b8239-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b8239-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b8239-107">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="b8239-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8239-108">語法</span><span class="sxs-lookup"><span data-stu-id="b8239-108">Syntax</span></span>

``` syntax
[UUID("455CE053-2552-4051-A3E4-C4200DC31B7"), AMENDMENT]
class Win32_VolumeChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  string DriveName;
};
```

## <a name="members"></a><span data-ttu-id="b8239-109">成員</span><span class="sxs-lookup"><span data-stu-id="b8239-109">Members</span></span>

<span data-ttu-id="b8239-110">**Win32 \_ VolumeChangeEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b8239-110">The **Win32\_VolumeChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b8239-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b8239-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8239-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b8239-112">Properties</span></span>

<span data-ttu-id="b8239-113">**Win32 \_ VolumeChangeEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b8239-113">The **Win32\_VolumeChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8239-114">**DriveName**</span><span class="sxs-lookup"><span data-stu-id="b8239-114">**DriveName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8239-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8239-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8239-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8239-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8239-117">已從系統新增或移除的磁片磁碟機名稱 (字母) 。</span><span class="sxs-lookup"><span data-stu-id="b8239-117">Drive name (letter) that has been added or removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b8239-118">**EventType**</span><span class="sxs-lookup"><span data-stu-id="b8239-118">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8239-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b8239-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8239-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8239-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8239-121">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32APIDevice management messages \| wm \_ DEVICECHANGE \| WParam"，"Win32APIDevice management messages \| wm \_ SETTINGCHANGE" ) </span><span class="sxs-lookup"><span data-stu-id="b8239-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="b8239-122">已發生的事件變更通知類型。</span><span class="sxs-lookup"><span data-stu-id="b8239-122">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="b8239-123">這個屬性繼承自 [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)。</span><span class="sxs-lookup"><span data-stu-id="b8239-123">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="b8239-124">設定 **已變更** (1) </span><span class="sxs-lookup"><span data-stu-id="b8239-124">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="b8239-125">**裝置抵達** (2) </span><span class="sxs-lookup"><span data-stu-id="b8239-125">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="b8239-126">**移除裝置** (3) </span><span class="sxs-lookup"><span data-stu-id="b8239-126">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="b8239-127">**銜接** (4) </span><span class="sxs-lookup"><span data-stu-id="b8239-127">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8239-128">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="b8239-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8239-129">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="b8239-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b8239-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8239-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8239-131">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="b8239-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="b8239-132">這個屬性繼承自 [**\_ \_ 事件**](../wmisdk/--event.md)。</span><span class="sxs-lookup"><span data-stu-id="b8239-132">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="b8239-133">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](../wmisdk/wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="b8239-133">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8239-134">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="b8239-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8239-135">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b8239-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8239-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b8239-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8239-137">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="b8239-137">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="b8239-138">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="b8239-138">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="b8239-139">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="b8239-139">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="b8239-140">這個屬性繼承自 [**\_ \_ 事件**](../wmisdk/--event.md)。</span><span class="sxs-lookup"><span data-stu-id="b8239-140">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="b8239-141">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="b8239-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8239-142">備註</span><span class="sxs-lookup"><span data-stu-id="b8239-142">Remarks</span></span>

<span data-ttu-id="b8239-143">**Win32 \_ VolumeChangeEvent** 類別衍生自 [**win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)。</span><span class="sxs-lookup"><span data-stu-id="b8239-143">The **Win32\_VolumeChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8239-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8239-144">Requirements</span></span>



| <span data-ttu-id="b8239-145">需求</span><span class="sxs-lookup"><span data-stu-id="b8239-145">Requirement</span></span> | <span data-ttu-id="b8239-146">值</span><span class="sxs-lookup"><span data-stu-id="b8239-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8239-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8239-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b8239-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8239-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8239-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8239-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b8239-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8239-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8239-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8239-151">Namespace</span></span><br/>                | <span data-ttu-id="b8239-152">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b8239-152">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8239-153">MOF</span><span class="sxs-lookup"><span data-stu-id="b8239-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8239-154"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8239-154"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8239-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b8239-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8239-156"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8239-156"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8239-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8239-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8239-158">**Win32 \_ DeviceChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="b8239-158">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="b8239-159">作業系統類別</span><span class="sxs-lookup"><span data-stu-id="b8239-159">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
