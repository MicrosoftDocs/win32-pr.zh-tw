---
description: Win32 \_ 1394ControllerDevice 關聯 WMI 類別會建立高速串列匯流排 (IEEE 1394 Firewire) 控制器以及 \_ 與其連接的 CIM LogicalDevice 實例的關聯。
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Win32_1394ControllerDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: af3a54db81a388184da148cd411895ebb910de7d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847529"
---
# <a name="win32_1394controllerdevice-class"></a><span data-ttu-id="5d853-103">Win32 \_ 1394ControllerDevice 類別</span><span class="sxs-lookup"><span data-stu-id="5d853-103">Win32\_1394ControllerDevice class</span></span>

<span data-ttu-id="5d853-104">**Win32 \_ 1394ControllerDevice** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會建立高速串列匯流排 (IEEE 1394 Firewire) 控制器以及與其連接的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)實例的關聯。</span><span class="sxs-lookup"><span data-stu-id="5d853-104">The **Win32\_1394ControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the high-speed serial bus (IEEE 1394 Firewire) Controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span> <span data-ttu-id="5d853-105">此序列匯流排為各式各樣的裝置提供增強的連線能力，包括消費者音訊或影片元件、存放裝置週邊設備、其他電腦和可攜式裝置。</span><span class="sxs-lookup"><span data-stu-id="5d853-105">This serial bus provides enhanced connectivity for a wide range of devices, including consumer audio or video components, storage peripherals, other computers, and portable devices.</span></span> <span data-ttu-id="5d853-106">消費者電子產業採用了 IEEE 1394，並提供隨插即用相容的擴充介面。</span><span class="sxs-lookup"><span data-stu-id="5d853-106">IEEE 1394 has been adopted by the consumer electronics industry and provides a Plug and Play-compatible expansion interface.</span></span>

<span data-ttu-id="5d853-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5d853-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5d853-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5d853-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d853-109">語法</span><span class="sxs-lookup"><span data-stu-id="5d853-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5d853-110">成員</span><span class="sxs-lookup"><span data-stu-id="5d853-110">Members</span></span>

<span data-ttu-id="5d853-111">**Win32 \_ 1394ControllerDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5d853-111">The **Win32\_1394ControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="5d853-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5d853-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d853-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5d853-113">Properties</span></span>

<span data-ttu-id="5d853-114">**Win32 \_ 1394ControllerDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5d853-114">The **Win32\_1394ControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d853-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="5d853-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d853-116">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5d853-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d853-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d853-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d853-118">指出控制器是否正在主動命令或存取裝置。</span><span class="sxs-lookup"><span data-stu-id="5d853-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="5d853-119">當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。</span><span class="sxs-lookup"><span data-stu-id="5d853-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="5d853-120">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="5d853-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5d853-121">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5d853-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="5d853-122">**Active** (1) </span><span class="sxs-lookup"><span data-stu-id="5d853-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="5d853-123">**非** 使用中 (2) </span><span class="sxs-lookup"><span data-stu-id="5d853-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d853-124">**先行**</span><span class="sxs-lookup"><span data-stu-id="5d853-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d853-125">資料類型： **Win32 \_ 1394Controller**</span><span class="sxs-lookup"><span data-stu-id="5d853-125">Data type: **Win32\_1394Controller**</span></span>
</dt> <dt>

<span data-ttu-id="5d853-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d853-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d853-127">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ 1394Controller" ) </span><span class="sxs-lookup"><span data-stu-id="5d853-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_1394Controller")</span></span>
</dt> </dl>

<span data-ttu-id="5d853-128">Win32 \_ 1394Controller antecedent 參考代表與此裝置相關聯的1394控制器。</span><span class="sxs-lookup"><span data-stu-id="5d853-128">The Win32\_1394Controller antecedent reference represents the 1394 controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="5d853-129">**依賴**</span><span class="sxs-lookup"><span data-stu-id="5d853-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d853-130">資料類型： **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="5d853-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5d853-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d853-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d853-132">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「cim \| CIM \_ LogicalDevice」 ) </span><span class="sxs-lookup"><span data-stu-id="5d853-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="5d853-133">CIM \_ LogicalDevice 相依參考代表 \_ 連接至1394控制器的 cim LogicalDevice。</span><span class="sxs-lookup"><span data-stu-id="5d853-133">The CIM\_LogicalDevice dependent reference represents the CIM\_LogicalDevice connected to the 1394 controller.</span></span>

</dd> <dt>

<span data-ttu-id="5d853-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="5d853-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d853-135">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5d853-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d853-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d853-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d853-137">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="5d853-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5d853-138">當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。</span><span class="sxs-lookup"><span data-stu-id="5d853-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="5d853-139">資料寬度的指定單位為位。</span><span class="sxs-lookup"><span data-stu-id="5d853-139">Data width is specified in bits.</span></span> <span data-ttu-id="5d853-140">如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5d853-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="5d853-141">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="5d853-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d853-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="5d853-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d853-143">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5d853-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d853-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d853-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d853-145">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="5d853-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="5d853-146">當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。</span><span class="sxs-lookup"><span data-stu-id="5d853-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="5d853-147">以每秒位數指定速度。</span><span class="sxs-lookup"><span data-stu-id="5d853-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="5d853-148">如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5d853-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="5d853-149">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5d853-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5d853-150">這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="5d853-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d853-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="5d853-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d853-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5d853-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d853-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d853-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d853-154">控制器發出的硬重設數目。</span><span class="sxs-lookup"><span data-stu-id="5d853-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="5d853-155">硬重設會將裝置傳回到其初始化或啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="5d853-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="5d853-156">所有內部裝置狀態資訊和資料都會遺失。</span><span class="sxs-lookup"><span data-stu-id="5d853-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="5d853-157">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="5d853-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d853-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="5d853-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d853-159">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5d853-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d853-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5d853-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d853-161">控制器發出的軟重設數目。</span><span class="sxs-lookup"><span data-stu-id="5d853-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="5d853-162">軟重設並不會完全清除目前的裝置狀態和資料。</span><span class="sxs-lookup"><span data-stu-id="5d853-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="5d853-163">確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。</span><span class="sxs-lookup"><span data-stu-id="5d853-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="5d853-164">這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="5d853-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d853-165">備註</span><span class="sxs-lookup"><span data-stu-id="5d853-165">Remarks</span></span>

<span data-ttu-id="5d853-166">**Win32 \_ 1394ControllerDevice** 類別衍生自 [**CIM \_ ControlledBy**](cim-controlledby.md)。</span><span class="sxs-lookup"><span data-stu-id="5d853-166">The **Win32\_1394ControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5d853-167">範例</span><span class="sxs-lookup"><span data-stu-id="5d853-167">Examples</span></span>

<span data-ttu-id="5d853-168">下列 PowerShell 程式碼範例會抓取1394控制器裝置資訊。</span><span class="sxs-lookup"><span data-stu-id="5d853-168">The following PowerShell code sample retrieves 1394 controller device information.</span></span>


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



<span data-ttu-id="5d853-169">先前的程式碼範例會傳回下列資訊：</span><span class="sxs-lookup"><span data-stu-id="5d853-169">The previous code sample returns the following information:</span></span>

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
```

## <a name="requirements"></a><span data-ttu-id="5d853-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d853-170">Requirements</span></span>



| <span data-ttu-id="5d853-171">需求</span><span class="sxs-lookup"><span data-stu-id="5d853-171">Requirement</span></span> | <span data-ttu-id="5d853-172">值</span><span class="sxs-lookup"><span data-stu-id="5d853-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d853-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d853-173">Minimum supported client</span></span><br/> | <span data-ttu-id="5d853-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d853-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d853-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d853-175">Minimum supported server</span></span><br/> | <span data-ttu-id="5d853-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d853-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d853-177">命名空間</span><span class="sxs-lookup"><span data-stu-id="5d853-177">Namespace</span></span><br/>                | <span data-ttu-id="5d853-178">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5d853-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d853-179">MOF</span><span class="sxs-lookup"><span data-stu-id="5d853-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d853-180"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d853-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d853-181">DLL</span><span class="sxs-lookup"><span data-stu-id="5d853-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d853-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d853-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d853-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d853-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d853-184">**CIM \_ ControlledBy**</span><span class="sxs-lookup"><span data-stu-id="5d853-184">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="5d853-185">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="5d853-185">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

