---
description: Win32 \_ IDEControllerDevice 關聯 WMI 類別 (IDE) 控制器和連接到的邏輯裝置（例如，磁片磁碟機），建立整合的磁片磁碟機。
ms.assetid: 1b0a551c-d836-4147-91ed-a0a7d97f4a5b
ms.tgt_platform: multiple
title: Win32_IDEControllerDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IDEControllerDevice
- Win32_IDEControllerDevice.NegotiatedDataWidth
- Win32_IDEControllerDevice.NegotiatedSpeed
- Win32_IDEControllerDevice.AccessState
- Win32_IDEControllerDevice.NumberOfHardResets
- Win32_IDEControllerDevice.NumberOfSoftResets
- Win32_IDEControllerDevice.Antecedent
- Win32_IDEControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc690aadd442d656132b2d9e4539cc27961c3ef9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385994"
---
# <a name="win32_idecontrollerdevice-class"></a><span data-ttu-id="4ef5e-103">Win32 \_ IDEControllerDevice 類別</span><span class="sxs-lookup"><span data-stu-id="4ef5e-103">Win32\_IDEControllerDevice class</span></span>

<span data-ttu-id="4ef5e-104">**Win32 \_ IDEControllerDevice** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class) (IDE) 控制器和連接到的邏輯裝置（例如，磁片磁碟機），建立整合的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-104">The **Win32\_IDEControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an Integrated Drive Electronics (IDE) controller and the logical device connected to, for example, a disk drive.</span></span>

<span data-ttu-id="4ef5e-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4ef5e-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef5e-107">語法</span><span class="sxs-lookup"><span data-stu-id="4ef5e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{5BC42B62-C7A1-11d2-911D-0060081A46FD}"), AMENDMENT]
class Win32_IDEControllerDevice : CIM_ControlledBy
{
  uint32                  NegotiatedDataWidth;
  uint64                  NegotiatedSpeed;
  uint16                  AccessState;
  uint32                  NumberOfHardResets;
  uint32                  NumberOfSoftResets;
  Win32_IDEController REF Antecedent;
  CIM_LogicalDevice   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4ef5e-108">成員</span><span class="sxs-lookup"><span data-stu-id="4ef5e-108">Members</span></span>

<span data-ttu-id="4ef5e-109">**Win32 \_ IDEControllerDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4ef5e-109">The **Win32\_IDEControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="4ef5e-110">屬性</span><span class="sxs-lookup"><span data-stu-id="4ef5e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ef5e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4ef5e-111">Properties</span></span>

<span data-ttu-id="4ef5e-112">**Win32 \_ IDEControllerDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-112">The **Win32\_IDEControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ef5e-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ef5e-114">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ef5e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ef5e-116">指出控制器是否正在主動命令或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="4ef5e-117">當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="4ef5e-118">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4ef5e-119">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4ef5e-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="4ef5e-120">**Active** (1) </span><span class="sxs-lookup"><span data-stu-id="4ef5e-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="4ef5e-121">**非** 使用中 (2) </span><span class="sxs-lookup"><span data-stu-id="4ef5e-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4ef5e-122">**先行**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ef5e-123">資料類型： **Win32 \_ IDEController**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-123">Data type: **Win32\_IDEController**</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ef5e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-125">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \| Win32 \_ IDEController" ) </span><span class="sxs-lookup"><span data-stu-id="4ef5e-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|Win32\_IDEController")</span></span>
</dt> </dl>

<span data-ttu-id="4ef5e-126">[**Win32 \_ IDEController**](win32-idecontroller.md) ，表示與此裝置相關聯的 IDE 控制器。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-126">A [**Win32\_IDEController**](win32-idecontroller.md) that represents the IDE controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="4ef5e-127">**依賴**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ef5e-128">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ef5e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-130">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| CIM \_ LogicalDevice」 ) </span><span class="sxs-lookup"><span data-stu-id="4ef5e-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="4ef5e-131">[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，表示連接到 IDE 控制器的邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the logical device connected to the IDE controller.</span></span>

</dd> <dt>

<span data-ttu-id="4ef5e-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ef5e-133">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ef5e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-135">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="4ef5e-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="4ef5e-136">當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="4ef5e-137">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-137">Data width is specified in bits.</span></span> <span data-ttu-id="4ef5e-138">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="4ef5e-139">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ef5e-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ef5e-141">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ef5e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-143">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="4ef5e-143">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="4ef5e-144">當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="4ef5e-145">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="4ef5e-146">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="4ef5e-147">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="4ef5e-148">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ef5e-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ef5e-150">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ef5e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ef5e-152">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="4ef5e-153">硬重設會將裝置傳回到其初始化或啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="4ef5e-154">所有內部裝置狀態資訊和資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="4ef5e-155">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ef5e-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ef5e-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ef5e-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4ef5e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ef5e-159">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="4ef5e-160">軟重設並不會完全清除目前的裝置狀態和資料。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="4ef5e-161">確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="4ef5e-162">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ef5e-163">備註</span><span class="sxs-lookup"><span data-stu-id="4ef5e-163">Remarks</span></span>

<span data-ttu-id="4ef5e-164">**Win32 \_ IDEControllerDevice** 類別衍生自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="4ef5e-164">The **Win32\_IDEControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ef5e-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ef5e-165">Requirements</span></span>



| <span data-ttu-id="4ef5e-166">需求</span><span class="sxs-lookup"><span data-stu-id="4ef5e-166">Requirement</span></span> | <span data-ttu-id="4ef5e-167">值</span><span class="sxs-lookup"><span data-stu-id="4ef5e-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef5e-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ef5e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="4ef5e-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ef5e-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ef5e-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ef5e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="4ef5e-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ef5e-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ef5e-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="4ef5e-172">Namespace</span></span><br/>                | <span data-ttu-id="4ef5e-173">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4ef5e-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4ef5e-174">MOF</span><span class="sxs-lookup"><span data-stu-id="4ef5e-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ef5e-175"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ef5e-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ef5e-176">DLL</span><span class="sxs-lookup"><span data-stu-id="4ef5e-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ef5e-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ef5e-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ef5e-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ef5e-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ef5e-179">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="4ef5e-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="4ef5e-180">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4ef5e-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

