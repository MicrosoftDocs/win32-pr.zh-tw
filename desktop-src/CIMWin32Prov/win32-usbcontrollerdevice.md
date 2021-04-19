---
description: Win32 \_ USBControllerDevice 關聯 WMI 類別會建立通用序列匯流排 (USB) 控制器和與其連接的 CIM \_ LogicalDevice 實例的關聯。
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Win32_USBControllerDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bf72c92a4ae23ac7750cdd52914e86f5dbcdd01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999830"
---
# <a name="win32_usbcontrollerdevice-class"></a><span data-ttu-id="20248-103">Win32 \_ USBControllerDevice 類別</span><span class="sxs-lookup"><span data-stu-id="20248-103">Win32\_USBControllerDevice class</span></span>

<span data-ttu-id="20248-104">**Win32 \_ USBControllerDevice** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立通用序列匯流排 (USB) 控制器和與其連接的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)實例的關聯。</span><span class="sxs-lookup"><span data-stu-id="20248-104">The **Win32\_USBControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a universal serial bus (USB) controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span>

<span data-ttu-id="20248-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="20248-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="20248-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="20248-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="20248-107">語法</span><span class="sxs-lookup"><span data-stu-id="20248-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="20248-108">成員</span><span class="sxs-lookup"><span data-stu-id="20248-108">Members</span></span>

<span data-ttu-id="20248-109">**Win32 \_ USBControllerDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="20248-109">The **Win32\_USBControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="20248-110">屬性</span><span class="sxs-lookup"><span data-stu-id="20248-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20248-111">屬性</span><span class="sxs-lookup"><span data-stu-id="20248-111">Properties</span></span>

<span data-ttu-id="20248-112">**Win32 \_ USBControllerDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="20248-112">The **Win32\_USBControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20248-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="20248-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20248-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="20248-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20248-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20248-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20248-116">指出控制器是否正在主動命令或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="20248-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="20248-117">當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="20248-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="20248-118">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="20248-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20248-119">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="20248-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="20248-120">**Active** (1) </span><span class="sxs-lookup"><span data-stu-id="20248-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="20248-121">**非** 使用中 (2) </span><span class="sxs-lookup"><span data-stu-id="20248-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20248-122">**先行**</span><span class="sxs-lookup"><span data-stu-id="20248-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20248-123">資料類型： **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="20248-123">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="20248-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20248-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20248-125">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "cim \| CIM \_ USBController" ) </span><span class="sxs-lookup"><span data-stu-id="20248-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_USBController")</span></span>
</dt> </dl>

<span data-ttu-id="20248-126">[**CIM \_ USBController**](cim-usbcontroller.md) ，表示與此裝置相關聯的通用序列匯流排 (USB) 控制器。</span><span class="sxs-lookup"><span data-stu-id="20248-126">A [**CIM\_USBController**](cim-usbcontroller.md) representing the Universal Serial Bus (USB) controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="20248-127">**依賴**</span><span class="sxs-lookup"><span data-stu-id="20248-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20248-128">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="20248-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="20248-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20248-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20248-130">限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「cim \| CIM \_ LogicalDevice」 ) </span><span class="sxs-lookup"><span data-stu-id="20248-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="20248-131">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述連線到通用序列匯流排 (USB) 控制器的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="20248-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) describing the logical device connected to the Universal Serial Bus (USB) controller.</span></span>

</dd> <dt>

<span data-ttu-id="20248-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="20248-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20248-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="20248-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20248-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20248-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20248-135">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="20248-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="20248-136">當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="20248-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="20248-137">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="20248-137">Data width is specified in bits.</span></span> <span data-ttu-id="20248-138">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="20248-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="20248-139">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="20248-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="20248-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="20248-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20248-141">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="20248-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20248-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20248-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20248-143">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="20248-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="20248-144">當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。</span><span class="sxs-lookup"><span data-stu-id="20248-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="20248-145">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="20248-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="20248-146">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="20248-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="20248-147">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="20248-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="20248-148">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="20248-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="20248-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="20248-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20248-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="20248-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20248-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20248-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20248-152">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="20248-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="20248-153">硬重設會將裝置傳回到其初始化或啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="20248-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="20248-154">所有內部裝置狀態資訊和資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="20248-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="20248-155">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="20248-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="20248-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="20248-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20248-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="20248-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20248-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="20248-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20248-159">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="20248-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="20248-160">軟重設並不會完全清除目前的裝置狀態和資料。</span><span class="sxs-lookup"><span data-stu-id="20248-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="20248-161">確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。</span><span class="sxs-lookup"><span data-stu-id="20248-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="20248-162">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="20248-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20248-163">備註</span><span class="sxs-lookup"><span data-stu-id="20248-163">Remarks</span></span>

<span data-ttu-id="20248-164">**Win32 \_ USBControllerDevice** 類別衍生自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="20248-164">The **Win32\_USBControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="20248-165">如需使用的相關討論，請參閱 [使用 WMI blog 的顯示 USB 裝置](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) 一文。</span><span class="sxs-lookup"><span data-stu-id="20248-165">For a discussion on using, see the [Displaying USB Devices using WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) blog article.</span></span> <span data-ttu-id="20248-166">如需使用關聯類別的討論，請參閱 [PowerShell 文章中的「取得 USB-使用 WMI 關聯類別](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) 」。</span><span class="sxs-lookup"><span data-stu-id="20248-166">For a discussion of using association classes, see the [Get-USB – Using WMI Association Classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) article.</span></span>

## <a name="examples"></a><span data-ttu-id="20248-167">範例</span><span class="sxs-lookup"><span data-stu-id="20248-167">Examples</span></span>

<span data-ttu-id="20248-168">下列 PowerShell 範例會抓取相依的邏輯裝置，並顯示相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="20248-168">The following PowerShell example retrieves the dependent logical device and displays the relevant information.</span></span>


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
```



## <a name="requirements"></a><span data-ttu-id="20248-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="20248-169">Requirements</span></span>



| <span data-ttu-id="20248-170">需求</span><span class="sxs-lookup"><span data-stu-id="20248-170">Requirement</span></span> | <span data-ttu-id="20248-171">值</span><span class="sxs-lookup"><span data-stu-id="20248-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20248-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20248-172">Minimum supported client</span></span><br/> | <span data-ttu-id="20248-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20248-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20248-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20248-174">Minimum supported server</span></span><br/> | <span data-ttu-id="20248-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20248-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20248-176">命名空間</span><span class="sxs-lookup"><span data-stu-id="20248-176">Namespace</span></span><br/>                | <span data-ttu-id="20248-177">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="20248-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20248-178">MOF</span><span class="sxs-lookup"><span data-stu-id="20248-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20248-179"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="20248-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20248-180">DLL</span><span class="sxs-lookup"><span data-stu-id="20248-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20248-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20248-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20248-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20248-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20248-183">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="20248-183">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="20248-184">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="20248-184">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
