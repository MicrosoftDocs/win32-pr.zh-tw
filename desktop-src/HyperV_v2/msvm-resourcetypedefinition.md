---
description: 定義資源類型與其實類別的對應。
ms.assetid: 0911454D-2494-49D5-8480-212E9ADD1B45
title: Msvm_ResourceTypeDefinition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceTypeDefinition
- Msvm_ResourceTypeDefinition.ResourceType
- Msvm_ResourceTypeDefinition.OtherResourceType
- Msvm_ResourceTypeDefinition.ResourceSubType
- Msvm_ResourceTypeDefinition.LogicalDeviceClassName
- Msvm_ResourceTypeDefinition.SettingDataClassName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: edfbf2ec9772fa710df5fc0d024abfcad6d826d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983771"
---
# <a name="msvm_resourcetypedefinition-class"></a><span data-ttu-id="70ffb-103">Msvm \_ ResourceTypeDefinition 類別</span><span class="sxs-lookup"><span data-stu-id="70ffb-103">Msvm\_ResourceTypeDefinition class</span></span>

<span data-ttu-id="70ffb-104">定義資源類型與其實類別的對應。</span><span class="sxs-lookup"><span data-stu-id="70ffb-104">Defines a mapping of a resource type to its implementation classes.</span></span>

<span data-ttu-id="70ffb-105">下列語法已簡化受控物件格式 (MOF) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="70ffb-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ffb-106">語法</span><span class="sxs-lookup"><span data-stu-id="70ffb-106">Syntax</span></span>

``` syntax
class Msvm_ResourceTypeDefinition
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  string LogicalDeviceClassName;
  string SettingDataClassName;
};
```

## <a name="members"></a><span data-ttu-id="70ffb-107">成員</span><span class="sxs-lookup"><span data-stu-id="70ffb-107">Members</span></span>

<span data-ttu-id="70ffb-108">**Msvm \_ ResourceTypeDefinition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="70ffb-108">The **Msvm\_ResourceTypeDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="70ffb-109">屬性</span><span class="sxs-lookup"><span data-stu-id="70ffb-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70ffb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="70ffb-110">Properties</span></span>

<span data-ttu-id="70ffb-111">**Msvm \_ ResourceTypeDefinition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="70ffb-111">The **Msvm\_ResourceTypeDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70ffb-112">**LogicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="70ffb-112">**LogicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ffb-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="70ffb-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="70ffb-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70ffb-115">衍生自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 的類別名稱，這個類別會針對此資源類型執行邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="70ffb-115">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the logical device for this resource type.</span></span>

</dd> <dt>

<span data-ttu-id="70ffb-116">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="70ffb-116">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ffb-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="70ffb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="70ffb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-119">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="70ffb-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="70ffb-120">描述資源類型的字串，當定義完善的值無法使用且 **ResourceType** 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="70ffb-120">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="70ffb-121">與 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)的 **OtherResourceType** 屬性有對應關係。</span><span class="sxs-lookup"><span data-stu-id="70ffb-121">There is a correspondence with the **OtherResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="70ffb-122">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="70ffb-122">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ffb-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="70ffb-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="70ffb-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-125">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="70ffb-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="70ffb-126">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="70ffb-126">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="70ffb-127">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="70ffb-127">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="70ffb-128">與 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)的 **ResourceSubType** 屬性有對應關係。</span><span class="sxs-lookup"><span data-stu-id="70ffb-128">There is a correspondence with the **ResourceSubType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="70ffb-129">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="70ffb-129">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ffb-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="70ffb-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="70ffb-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-132">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="70ffb-132">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="70ffb-133">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="70ffb-133">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="70ffb-134">與 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)的 **ResourceType** 屬性有對應關係。</span><span class="sxs-lookup"><span data-stu-id="70ffb-134">There is a correspondence with the **ResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="70ffb-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="70ffb-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="70ffb-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="70ffb-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="70ffb-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="70ffb-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="70ffb-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="70ffb-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="70ffb-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="70ffb-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="70ffb-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="70ffb-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="70ffb-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="70ffb-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="70ffb-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="70ffb-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="70ffb-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**序列埠** (17) </span><span class="sxs-lookup"><span data-stu-id="70ffb-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**平行埠** (18) </span><span class="sxs-lookup"><span data-stu-id="70ffb-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB 控制器** (19) </span><span class="sxs-lookup"><span data-stu-id="70ffb-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**圖形控制器** (20) </span><span class="sxs-lookup"><span data-stu-id="70ffb-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**儲存體範圍** (21) </span><span class="sxs-lookup"><span data-stu-id="70ffb-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**磁片** (22) </span><span class="sxs-lookup"><span data-stu-id="70ffb-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**磁帶** (23) </span><span class="sxs-lookup"><span data-stu-id="70ffb-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**其他存放裝置** (24) </span><span class="sxs-lookup"><span data-stu-id="70ffb-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="70ffb-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="70ffb-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="70ffb-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**電源供應** 器 (28) </span><span class="sxs-lookup"><span data-stu-id="70ffb-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**冷卻裝置** (29) </span><span class="sxs-lookup"><span data-stu-id="70ffb-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (30 32767) </span><span class="sxs-lookup"><span data-stu-id="70ffb-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768 65535) </span><span class="sxs-lookup"><span data-stu-id="70ffb-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70ffb-166">**SettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="70ffb-166">**SettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70ffb-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="70ffb-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70ffb-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="70ffb-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70ffb-169">衍生自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 的類別名稱，這個類別會執行此資源類型的設定。</span><span class="sxs-lookup"><span data-stu-id="70ffb-169">The name of the class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) that implements the settings for this resource type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70ffb-170">備註</span><span class="sxs-lookup"><span data-stu-id="70ffb-170">Remarks</span></span>

<span data-ttu-id="70ffb-171">存取 **Msvm \_ ResourceTypeDefinition** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="70ffb-171">Access to the **Msvm\_ResourceTypeDefinition** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="70ffb-172">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="70ffb-172">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="70ffb-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="70ffb-173">Requirements</span></span>



| <span data-ttu-id="70ffb-174">需求</span><span class="sxs-lookup"><span data-stu-id="70ffb-174">Requirement</span></span> | <span data-ttu-id="70ffb-175">值</span><span class="sxs-lookup"><span data-stu-id="70ffb-175">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ffb-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70ffb-176">Minimum supported client</span></span><br/> | <span data-ttu-id="70ffb-177">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70ffb-177">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="70ffb-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70ffb-178">Minimum supported server</span></span><br/> | <span data-ttu-id="70ffb-179">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70ffb-179">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70ffb-180">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="70ffb-180">End of client support</span></span><br/>    | <span data-ttu-id="70ffb-181">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="70ffb-181">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="70ffb-182">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="70ffb-182">End of server support</span></span><br/>    | <span data-ttu-id="70ffb-183">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="70ffb-183">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="70ffb-184">命名空間</span><span class="sxs-lookup"><span data-stu-id="70ffb-184">Namespace</span></span><br/>                | <span data-ttu-id="70ffb-185">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="70ffb-185">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="70ffb-186">MOF</span><span class="sxs-lookup"><span data-stu-id="70ffb-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70ffb-187"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="70ffb-187"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70ffb-188">DLL</span><span class="sxs-lookup"><span data-stu-id="70ffb-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70ffb-189"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70ffb-189"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

