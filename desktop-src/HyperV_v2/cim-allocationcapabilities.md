---
description: 表示特定資源類型之 managed 元素的資源配置設定。
ms.assetid: f27910c7-a88a-4694-80fe-7761945782e0
title: CIM_AllocationCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocationCapabilities
- CIM_AllocationCapabilities.ResourceType
- CIM_AllocationCapabilities.OtherResourceType
- CIM_AllocationCapabilities.ResourceSubType
- CIM_AllocationCapabilities.RequestTypesSupported
- CIM_AllocationCapabilities.SharingMode
- CIM_AllocationCapabilities.SupportedAddStates
- CIM_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d022023142b38905067e30a4c1be3b133e49a86f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973999"
---
# <a name="cim_allocationcapabilities-class"></a><span data-ttu-id="f72b7-103">CIM \_ AllocationCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="f72b7-103">CIM\_AllocationCapabilities class</span></span>

<span data-ttu-id="f72b7-104">表示特定資源類型之 managed 元素的資源配置設定。</span><span class="sxs-lookup"><span data-stu-id="f72b7-104">Represents the resource allocation settings of a managed element for a specific resource type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72b7-105">語法</span><span class="sxs-lookup"><span data-stu-id="f72b7-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_AllocationCapabilities : CIM_Capabilities
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="f72b7-106">成員</span><span class="sxs-lookup"><span data-stu-id="f72b7-106">Members</span></span>

<span data-ttu-id="f72b7-107">**CIM \_ AllocationCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f72b7-107">The **CIM\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="f72b7-108">屬性</span><span class="sxs-lookup"><span data-stu-id="f72b7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f72b7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="f72b7-109">Properties</span></span>

<span data-ttu-id="f72b7-110">**CIM \_ AllocationCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f72b7-110">The **CIM\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f72b7-111">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="f72b7-111">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f72b7-112">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f72b7-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f72b7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-114">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**") </span><span class="sxs-lookup"><span data-stu-id="f72b7-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="f72b7-115">當 **ResourceType** 屬性設為 "1" (其他) 時，此配置設定的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f72b7-115">The resource type for this allocation setting when the **ResourceType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="f72b7-116">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="f72b7-116">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f72b7-117">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f72b7-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f72b7-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f72b7-119">指出是否支援要求特定的資源。</span><span class="sxs-lookup"><span data-stu-id="f72b7-119">Indicates whether requesting a specific resource is supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f72b7-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f72b7-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>

<span data-ttu-id="f72b7-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**特定** (2) </span><span class="sxs-lookup"><span data-stu-id="f72b7-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Specific** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f72b7-122">要求可以包含特定資源的要求。</span><span class="sxs-lookup"><span data-stu-id="f72b7-122">Request can include a request for specific resource.</span></span>

</dd> <dt>

<span id="General"></span><span id="general"></span><span id="GENERAL"></span>

<span data-ttu-id="f72b7-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**一般** (3) </span><span class="sxs-lookup"><span data-stu-id="f72b7-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**General** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f72b7-124">要求不包含特定的資源。</span><span class="sxs-lookup"><span data-stu-id="f72b7-124">Request does not include specific resource.</span></span>

</dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="f72b7-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**(4**) </span><span class="sxs-lookup"><span data-stu-id="f72b7-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Both** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f72b7-126">支援特定和一般要求。</span><span class="sxs-lookup"><span data-stu-id="f72b7-126">Both specific and general requests are supported.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f72b7-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f72b7-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f72b7-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="f72b7-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f72b7-129">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="f72b7-129">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f72b7-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f72b7-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f72b7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f72b7-132">此資源之執行特定子類型的描述。</span><span class="sxs-lookup"><span data-stu-id="f72b7-132">A description of an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="f72b7-133">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="f72b7-133">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="f72b7-134">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="f72b7-134">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f72b7-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f72b7-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f72b7-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-137">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AllocationCapabilities**.**OtherResourceType**"，"[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**") </span><span class="sxs-lookup"><span data-stu-id="f72b7-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AllocationCapabilities**.**OtherResourceType**", "[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="f72b7-138">指派給此配置設定的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f72b7-138">The type of resource that is assigned to this allocation setting.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f72b7-139">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f72b7-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="f72b7-140">**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="f72b7-140">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="f72b7-141">**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="f72b7-141">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="f72b7-142">**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="f72b7-142">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="f72b7-143">**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="f72b7-143">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="f72b7-144">**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="f72b7-144">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="f72b7-145">**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="f72b7-145">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="f72b7-146">**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="f72b7-146">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="f72b7-147">**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="f72b7-147">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="f72b7-148">**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="f72b7-148">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="f72b7-149">**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="f72b7-149">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="f72b7-150">**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="f72b7-150">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="f72b7-151"> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="f72b7-151">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="f72b7-152">**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="f72b7-152">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="f72b7-153">**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="f72b7-153">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="f72b7-154">**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="f72b7-154">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="f72b7-155">**磁片磁碟機** (17) </span><span class="sxs-lookup"><span data-stu-id="f72b7-155">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="f72b7-156">**磁帶機** (18) </span><span class="sxs-lookup"><span data-stu-id="f72b7-156">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="f72b7-157">**儲存體範圍** (19) </span><span class="sxs-lookup"><span data-stu-id="f72b7-157">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="f72b7-158">**其他存放裝置** (20) </span><span class="sxs-lookup"><span data-stu-id="f72b7-158">**Other Storage Device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="f72b7-159">**序列埠** (21) </span><span class="sxs-lookup"><span data-stu-id="f72b7-159">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="f72b7-160">**平行埠** (22) </span><span class="sxs-lookup"><span data-stu-id="f72b7-160">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="f72b7-161">**USB 控制器** (23) </span><span class="sxs-lookup"><span data-stu-id="f72b7-161">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="f72b7-162">**圖形控制器** (24) </span><span class="sxs-lookup"><span data-stu-id="f72b7-162">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="f72b7-163">**IEEE 1394 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="f72b7-163">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="f72b7-164">**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="f72b7-164">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="f72b7-165">**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="f72b7-165">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="f72b7-166">**Power** (28) </span><span class="sxs-lookup"><span data-stu-id="f72b7-166">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="f72b7-167">**冷卻容量** (29) </span><span class="sxs-lookup"><span data-stu-id="f72b7-167">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="f72b7-168">**乙太網路交換器埠** (30) </span><span class="sxs-lookup"><span data-stu-id="f72b7-168">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="f72b7-169">**邏輯磁片** (31) </span><span class="sxs-lookup"><span data-stu-id="f72b7-169">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="f72b7-170">**存放磁片區** (32) </span><span class="sxs-lookup"><span data-stu-id="f72b7-170">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="f72b7-171">**Ethernet 連接** (33) </span><span class="sxs-lookup"><span data-stu-id="f72b7-171">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f72b7-172">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f72b7-172">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f72b7-173">**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="f72b7-173">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f72b7-174">**SharingMode**</span><span class="sxs-lookup"><span data-stu-id="f72b7-174">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f72b7-175">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f72b7-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f72b7-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f72b7-177">指出如何授與基礎資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="f72b7-177">Indicates how access to the underlying resource is granted.</span></span>

<span data-ttu-id="f72b7-178">實際數量是由最小、最大大小、權數等來控制。</span><span class="sxs-lookup"><span data-stu-id="f72b7-178">Actual quantity is controlled by min, max size, weights, etc.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f72b7-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f72b7-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="f72b7-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (2) </span><span class="sxs-lookup"><span data-stu-id="f72b7-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f72b7-181">基礎資源的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="f72b7-181">Exclusive access to underlying resource.</span></span>

</dd> <dt>

<span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>

<span data-ttu-id="f72b7-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**共用** (3) </span><span class="sxs-lookup"><span data-stu-id="f72b7-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Shared** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f72b7-183">共用基礎資源的使用。</span><span class="sxs-lookup"><span data-stu-id="f72b7-183">Shared use of underlying resource.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f72b7-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f72b7-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f72b7-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="f72b7-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f72b7-186">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="f72b7-186">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f72b7-187">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f72b7-187">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f72b7-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-189">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**") </span><span class="sxs-lookup"><span data-stu-id="f72b7-189">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="f72b7-190">建立新資源時支援的系統狀態。</span><span class="sxs-lookup"><span data-stu-id="f72b7-190">The system states that are supported when a new resource is created.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f72b7-191">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f72b7-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f72b7-192">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="f72b7-192">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f72b7-193">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="f72b7-193">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="f72b7-194">正在 **關閉** (4) </span><span class="sxs-lookup"><span data-stu-id="f72b7-194">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f72b7-195">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="f72b7-195">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="f72b7-196">**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="f72b7-196">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f72b7-197">**在測試** (7) </span><span class="sxs-lookup"><span data-stu-id="f72b7-197">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="f72b7-198">**延** 後的 (8) </span><span class="sxs-lookup"><span data-stu-id="f72b7-198">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="f72b7-199">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="f72b7-199">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f72b7-200">**開始** (10) </span><span class="sxs-lookup"><span data-stu-id="f72b7-200">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f72b7-201">已 **暫停** (11) </span><span class="sxs-lookup"><span data-stu-id="f72b7-201">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="f72b7-202">已 **暫** 止 (12) </span><span class="sxs-lookup"><span data-stu-id="f72b7-202">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f72b7-203">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f72b7-203">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f72b7-204">**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="f72b7-204">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f72b7-205">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="f72b7-205">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f72b7-206">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f72b7-206">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f72b7-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f72b7-208">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**") </span><span class="sxs-lookup"><span data-stu-id="f72b7-208">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="f72b7-209">移除資源時支援的系統狀態。</span><span class="sxs-lookup"><span data-stu-id="f72b7-209">The system states that are supported when a resource is removed.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f72b7-210">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f72b7-210">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f72b7-211">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="f72b7-211">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f72b7-212">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="f72b7-212">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="f72b7-213">正在 **關閉** (4) </span><span class="sxs-lookup"><span data-stu-id="f72b7-213">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f72b7-214">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="f72b7-214">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="f72b7-215">**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="f72b7-215">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f72b7-216">**在測試** (7) </span><span class="sxs-lookup"><span data-stu-id="f72b7-216">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="f72b7-217">**延** 後的 (8) </span><span class="sxs-lookup"><span data-stu-id="f72b7-217">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="f72b7-218">**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="f72b7-218">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f72b7-219">**開始** (10) </span><span class="sxs-lookup"><span data-stu-id="f72b7-219">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f72b7-220">已 **暫停** (11) </span><span class="sxs-lookup"><span data-stu-id="f72b7-220">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="f72b7-221">已 **暫** 止 (12) </span><span class="sxs-lookup"><span data-stu-id="f72b7-221">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f72b7-222">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f72b7-222">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f72b7-223">**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="f72b7-223">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="f72b7-224"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f72b7-224"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f72b7-225">規格需求</span><span class="sxs-lookup"><span data-stu-id="f72b7-225">Requirements</span></span>



| <span data-ttu-id="f72b7-226">需求</span><span class="sxs-lookup"><span data-stu-id="f72b7-226">Requirement</span></span> | <span data-ttu-id="f72b7-227">值</span><span class="sxs-lookup"><span data-stu-id="f72b7-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72b7-228">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f72b7-228">Minimum supported client</span></span><br/> | <span data-ttu-id="f72b7-229">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f72b7-229">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f72b7-230">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f72b7-230">Minimum supported server</span></span><br/> | <span data-ttu-id="f72b7-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f72b7-231">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f72b7-232">命名空間</span><span class="sxs-lookup"><span data-stu-id="f72b7-232">Namespace</span></span><br/>                | <span data-ttu-id="f72b7-233">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f72b7-233">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f72b7-234">MOF</span><span class="sxs-lookup"><span data-stu-id="f72b7-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f72b7-235"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f72b7-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f72b7-236">DLL</span><span class="sxs-lookup"><span data-stu-id="f72b7-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f72b7-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f72b7-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f72b7-238">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f72b7-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72b7-239">**CIM \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="f72b7-239">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

