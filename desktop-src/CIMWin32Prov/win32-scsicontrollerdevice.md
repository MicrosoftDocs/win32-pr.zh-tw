---
description: Win32 \_ SCSIControllerDevice 關聯 WMI 類別會將小型電腦系統介面與 (SCSI) 控制器以及邏輯裝置 (磁片磁碟機) 連接。
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Win32_SCSIControllerDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a3189f9d9b75321df7c69214e68779864953f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510726"
---
# <a name="win32_scsicontrollerdevice-class"></a><span data-ttu-id="efb30-103">Win32 \_ SCSIControllerDevice 類別</span><span class="sxs-lookup"><span data-stu-id="efb30-103">Win32\_SCSIControllerDevice class</span></span>

<span data-ttu-id="efb30-104">**Win32 \_ SCSIControllerDevice** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將小型電腦系統介面與 (SCSI) 控制器以及邏輯裝置 (磁片磁碟機) 連接。</span><span class="sxs-lookup"><span data-stu-id="efb30-104">The **Win32\_SCSIControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a small computer system interface (SCSI) controller and the logical device (disk drive) connected to it.</span></span>

<span data-ttu-id="efb30-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="efb30-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="efb30-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="efb30-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb30-107">語法</span><span class="sxs-lookup"><span data-stu-id="efb30-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="efb30-108">成員</span><span class="sxs-lookup"><span data-stu-id="efb30-108">Members</span></span>

<span data-ttu-id="efb30-109">**Win32 \_ SCSIControllerDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="efb30-109">The **Win32\_SCSIControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="efb30-110">屬性</span><span class="sxs-lookup"><span data-stu-id="efb30-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efb30-111">屬性</span><span class="sxs-lookup"><span data-stu-id="efb30-111">Properties</span></span>

<span data-ttu-id="efb30-112">**Win32 \_ SCSIControllerDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="efb30-112">The **Win32\_SCSIControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efb30-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="efb30-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efb30-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="efb30-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efb30-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="efb30-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efb30-116">指出控制器是否正在主動命令或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="efb30-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="efb30-117">當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="efb30-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="efb30-118">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="efb30-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efb30-119">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="efb30-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="efb30-120">**Active** (1) </span><span class="sxs-lookup"><span data-stu-id="efb30-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="efb30-121">**非** 使用中 (2) </span><span class="sxs-lookup"><span data-stu-id="efb30-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efb30-122">**先行**</span><span class="sxs-lookup"><span data-stu-id="efb30-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efb30-123">資料類型： **Win32 \_ microsoft.hyperv.powershell.scsicontroller**</span><span class="sxs-lookup"><span data-stu-id="efb30-123">Data type: **Win32\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="efb30-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="efb30-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efb30-125">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Antecedent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "CIM \| Win32 \_ microsoft.hyperv.powershell.scsicontroller" ) </span><span class="sxs-lookup"><span data-stu-id="efb30-125">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|Win32\_SCSIController")</span></span>
</dt> </dl>

<span data-ttu-id="efb30-126">[**Win32 \_ microsoft.hyperv.powershell.scsicontroller**](win32-scsicontroller.md) antecedent 參考代表與此裝置相關聯的 SCSI 控制器。</span><span class="sxs-lookup"><span data-stu-id="efb30-126">The [**Win32\_SCSIController**](win32-scsicontroller.md) antecedent reference represents the SCSI controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="efb30-127">**依賴**</span><span class="sxs-lookup"><span data-stu-id="efb30-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efb30-128">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="efb30-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="efb30-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="efb30-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efb30-130">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( 「相依」 ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「cim \| CIM \_ LogicalDevice」 ) </span><span class="sxs-lookup"><span data-stu-id="efb30-130">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="efb30-131">[**CIM \_ LogicalDevice**](cim-logicaldevice.md)相依參考代表連接至 SCSI 控制器的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="efb30-131">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) dependent reference represents the logical device connected to the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="efb30-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="efb30-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efb30-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="efb30-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efb30-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="efb30-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efb30-135">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="efb30-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="efb30-136">當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="efb30-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="efb30-137">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="efb30-137">Data width is specified in bits.</span></span> <span data-ttu-id="efb30-138">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="efb30-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="efb30-139">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="efb30-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="efb30-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="efb30-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efb30-141">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="efb30-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="efb30-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="efb30-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efb30-143">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="efb30-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="efb30-144">當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。</span><span class="sxs-lookup"><span data-stu-id="efb30-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="efb30-145">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="efb30-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="efb30-146">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="efb30-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="efb30-147">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="efb30-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="efb30-148">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="efb30-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="efb30-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="efb30-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efb30-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="efb30-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efb30-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="efb30-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efb30-152">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="efb30-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="efb30-153">硬重設會將裝置傳回到其初始化或啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="efb30-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="efb30-154">所有內部裝置狀態資訊和資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="efb30-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="efb30-155">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="efb30-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="efb30-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="efb30-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efb30-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="efb30-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efb30-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="efb30-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efb30-159">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="efb30-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="efb30-160">軟重設並不會完全清除目前的裝置狀態和資料。</span><span class="sxs-lookup"><span data-stu-id="efb30-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="efb30-161">確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。</span><span class="sxs-lookup"><span data-stu-id="efb30-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="efb30-162">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="efb30-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efb30-163">備註</span><span class="sxs-lookup"><span data-stu-id="efb30-163">Remarks</span></span>

<span data-ttu-id="efb30-164">**Win32 \_ SCSIControllerDevice** 類別衍生自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="efb30-164">The **Win32\_SCSIControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="efb30-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="efb30-165">Requirements</span></span>



| <span data-ttu-id="efb30-166">需求</span><span class="sxs-lookup"><span data-stu-id="efb30-166">Requirement</span></span> | <span data-ttu-id="efb30-167">值</span><span class="sxs-lookup"><span data-stu-id="efb30-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efb30-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="efb30-168">Minimum supported client</span></span><br/> | <span data-ttu-id="efb30-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efb30-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="efb30-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="efb30-170">Minimum supported server</span></span><br/> | <span data-ttu-id="efb30-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efb30-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="efb30-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="efb30-172">Namespace</span></span><br/>                | <span data-ttu-id="efb30-173">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="efb30-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="efb30-174">MOF</span><span class="sxs-lookup"><span data-stu-id="efb30-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efb30-175"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="efb30-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="efb30-176">DLL</span><span class="sxs-lookup"><span data-stu-id="efb30-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efb30-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efb30-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb30-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="efb30-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb30-179">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="efb30-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="efb30-180">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="efb30-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
