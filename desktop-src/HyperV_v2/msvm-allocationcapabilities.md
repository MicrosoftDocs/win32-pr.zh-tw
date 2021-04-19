---
description: 定義用戶端可以探索虛擬資源預設設定之有效範圍的方法。
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Msvm_AllocationCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7642d1b590affcb3704f7d854d65edb5481c2285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998333"
---
# <a name="msvm_allocationcapabilities-class"></a><span data-ttu-id="4503c-103">Msvm \_ AllocationCapabilities 類別</span><span class="sxs-lookup"><span data-stu-id="4503c-103">Msvm\_AllocationCapabilities class</span></span>

<span data-ttu-id="4503c-104">定義用戶端可以探索虛擬資源預設設定之有效範圍的方法。</span><span class="sxs-lookup"><span data-stu-id="4503c-104">Defines the means by which a client can discover the valid range of default settings for a virtual resource.</span></span> <span data-ttu-id="4503c-105">**Msvm \_ AllocationCapabilities** 物件與每個資源集區相關聯。</span><span class="sxs-lookup"><span data-stu-id="4503c-105">A **Msvm\_AllocationCapabilities** object is associated with each resource pool.</span></span> <span data-ttu-id="4503c-106">四個 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 物件與 **Msvm \_ AllocationCapabilities** 物件相關聯，以描述指定資源配置的最小值、最大值、預設值和累加值。</span><span class="sxs-lookup"><span data-stu-id="4503c-106">Four [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) objects are associated with the **Msvm\_AllocationCapabilities** object to describe the minimum, maximum, default, and incremental values for the given resource's allocation.</span></span> <span data-ttu-id="4503c-107">這些類別一起描述支援功能的整體範圍。</span><span class="sxs-lookup"><span data-stu-id="4503c-107">Together, these classes describe the overall range of supported capabilities.</span></span>

<span data-ttu-id="4503c-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4503c-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4503c-109">語法</span><span class="sxs-lookup"><span data-stu-id="4503c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="4503c-110">成員</span><span class="sxs-lookup"><span data-stu-id="4503c-110">Members</span></span>

<span data-ttu-id="4503c-111">**Msvm \_ AllocationCapabilities** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4503c-111">The **Msvm\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="4503c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="4503c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4503c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4503c-113">Properties</span></span>

<span data-ttu-id="4503c-114">**Msvm \_ AllocationCapabilities** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4503c-114">The **Msvm\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4503c-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="4503c-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4503c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4503c-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4503c-118">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="4503c-118">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4503c-119">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="4503c-119">A short description of the object.</span></span> <span data-ttu-id="4503c-120">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4503c-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4503c-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="4503c-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4503c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4503c-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-124">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4503c-124">A description of the object.</span></span> <span data-ttu-id="4503c-125">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4503c-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4503c-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4503c-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4503c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4503c-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-129">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4503c-129">A display name for the object.</span></span> <span data-ttu-id="4503c-130">除了索引鍵屬性、身分識別資料和描述資訊之外，此屬性還可讓每個實例定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4503c-130">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="4503c-131">**CIM \_ ManagedSystemElement** 類別的 [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)屬性也會定義為顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4503c-131">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="4503c-132">但是，它通常是一個重要的子類別。</span><span class="sxs-lookup"><span data-stu-id="4503c-132">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="4503c-133">相同的屬性可以同時傳達身分識別和顯示名稱，而不會有不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="4503c-133">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="4503c-134">如果 [**名稱**](msvm-keyboard.md) 存在，而且不是索引鍵 (例如) 邏輯裝置的實例，則 **名稱** 和 **ElementName** 屬性中都可以同時存在相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="4503c-134">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of a logical device), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="4503c-135">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4503c-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4503c-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4503c-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4503c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4503c-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-139">此資源集區的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4503c-139">A unique identifier for this resource pool.</span></span> <span data-ttu-id="4503c-140">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="4503c-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4503c-141">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="4503c-141">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4503c-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4503c-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-144">當定義完善的值無法使用且 **ResourceType** 的值為 "Other" 時，描述資源類型的字串。</span><span class="sxs-lookup"><span data-stu-id="4503c-144">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="4503c-145">這個屬性繼承自 [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="4503c-145">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="4503c-146">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="4503c-146">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-147">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4503c-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4503c-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-149">指出是否支援要求特定的資源。</span><span class="sxs-lookup"><span data-stu-id="4503c-149">Indicates whether requesting a specific resource is supported.</span></span> <span data-ttu-id="4503c-150">這個屬性繼承自 [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="4503c-150">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="4503c-151">值</span><span class="sxs-lookup"><span data-stu-id="4503c-151">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="4503c-152">意義</span><span class="sxs-lookup"><span data-stu-id="4503c-152">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="4503c-153"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4503c-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="4503c-154">Unknown</span><span class="sxs-lookup"><span data-stu-id="4503c-154">Unknown</span></span><br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <span data-ttu-id="4503c-155"><dt>**特定**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4503c-155"><dt>**Specific**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="4503c-156">要求可以包含特定資源的要求。</span><span class="sxs-lookup"><span data-stu-id="4503c-156">The request can include a request for a specific resource.</span></span><br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <span data-ttu-id="4503c-157"><dt>**一般**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4503c-157"><dt>**General**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="4503c-158">要求不包含特定資源的要求。</span><span class="sxs-lookup"><span data-stu-id="4503c-158">The request does not include a request for a specific resource.</span></span><br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <span data-ttu-id="4503c-159"><dt>**兩者都**</dt>是 <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4503c-159"><dt>**Both**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="4503c-160">支援特定和一般要求。</span><span class="sxs-lookup"><span data-stu-id="4503c-160">Both specific and general requests are supported.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="4503c-161">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="4503c-161">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4503c-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4503c-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-164">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="4503c-164">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="4503c-165">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="4503c-165">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="4503c-166">這個屬性繼承自 [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="4503c-166">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="4503c-167">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="4503c-167">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4503c-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4503c-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-170">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="4503c-170">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="4503c-171">這個屬性繼承自 [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="4503c-171">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="4503c-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4503c-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="4503c-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="4503c-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="4503c-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="4503c-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="4503c-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="4503c-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="4503c-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="4503c-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="4503c-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="4503c-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="4503c-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="4503c-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="4503c-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="4503c-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="4503c-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**磁片磁碟機** (17) </span><span class="sxs-lookup"><span data-stu-id="4503c-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**磁帶機** (18) </span><span class="sxs-lookup"><span data-stu-id="4503c-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**儲存體範圍** (19) </span><span class="sxs-lookup"><span data-stu-id="4503c-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**其他存放裝置** (20) </span><span class="sxs-lookup"><span data-stu-id="4503c-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**序列埠** (21) </span><span class="sxs-lookup"><span data-stu-id="4503c-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**平行埠** (22) </span><span class="sxs-lookup"><span data-stu-id="4503c-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB 控制器** (23) </span><span class="sxs-lookup"><span data-stu-id="4503c-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**圖形控制器** (24) </span><span class="sxs-lookup"><span data-stu-id="4503c-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="4503c-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="4503c-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="4503c-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28) </span><span class="sxs-lookup"><span data-stu-id="4503c-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**冷卻容量** (29) </span><span class="sxs-lookup"><span data-stu-id="4503c-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**乙太網路交換器埠** (30) </span><span class="sxs-lookup"><span data-stu-id="4503c-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**邏輯磁片** (31) </span><span class="sxs-lookup"><span data-stu-id="4503c-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**存放磁片區** (32) </span><span class="sxs-lookup"><span data-stu-id="4503c-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet 連接** (33) </span><span class="sxs-lookup"><span data-stu-id="4503c-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="4503c-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。0xFFFF ) </span><span class="sxs-lookup"><span data-stu-id="4503c-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4503c-207">**SharingMode**</span><span class="sxs-lookup"><span data-stu-id="4503c-207">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4503c-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4503c-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-210">指出如何授與基礎資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="4503c-210">Indicates how access to an underlying resource is granted.</span></span> <span data-ttu-id="4503c-211">這個屬性繼承自 [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="4503c-211">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="4503c-212">值</span><span class="sxs-lookup"><span data-stu-id="4503c-212">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="4503c-213">意義</span><span class="sxs-lookup"><span data-stu-id="4503c-213">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="4503c-214"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4503c-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="4503c-215">Unknown</span><span class="sxs-lookup"><span data-stu-id="4503c-215">Unknown</span></span><br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <span data-ttu-id="4503c-216"><dt>**專用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4503c-216"><dt>**Dedicated**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="4503c-217">基礎資源的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="4503c-217">Exclusive access to an underlying resource.</span></span><br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <span data-ttu-id="4503c-218"><dt>**共用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4503c-218"><dt>**Shared**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="4503c-219">共用基礎資源的使用。</span><span class="sxs-lookup"><span data-stu-id="4503c-219">Shared use of an underlying resource.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="4503c-220">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="4503c-220">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-221">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4503c-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4503c-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-223">指出建立新資源時，與資源相關聯的系統可位於的狀態。</span><span class="sxs-lookup"><span data-stu-id="4503c-223">Indicates the states that the system to which the resource will be associated can be in when a new resource is created.</span></span> <span data-ttu-id="4503c-224">這個屬性繼承自 [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="4503c-224">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="4503c-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4503c-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="4503c-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="4503c-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (4) </span><span class="sxs-lookup"><span data-stu-id="4503c-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="4503c-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="4503c-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (7) </span><span class="sxs-lookup"><span data-stu-id="4503c-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**延** 後的 (8) </span><span class="sxs-lookup"><span data-stu-id="4503c-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="4503c-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (10) </span><span class="sxs-lookup"><span data-stu-id="4503c-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (11) </span><span class="sxs-lookup"><span data-stu-id="4503c-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>已 **暫** 止 (12) </span><span class="sxs-lookup"><span data-stu-id="4503c-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="4503c-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。0xFFFF ) </span><span class="sxs-lookup"><span data-stu-id="4503c-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4503c-239">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="4503c-239">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4503c-240">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4503c-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4503c-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4503c-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4503c-242">指出當移除資源時，與資源相關聯的系統可處於的狀態。</span><span class="sxs-lookup"><span data-stu-id="4503c-242">Indicates the states that the system to which the resource is associated can be in when the resource is removed.</span></span> <span data-ttu-id="4503c-243">這個屬性繼承自 [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)。</span><span class="sxs-lookup"><span data-stu-id="4503c-243">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="4503c-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4503c-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="4503c-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="4503c-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (4) </span><span class="sxs-lookup"><span data-stu-id="4503c-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="4503c-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="4503c-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (7) </span><span class="sxs-lookup"><span data-stu-id="4503c-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**延** 後的 (8) </span><span class="sxs-lookup"><span data-stu-id="4503c-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="4503c-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (10) </span><span class="sxs-lookup"><span data-stu-id="4503c-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (11) </span><span class="sxs-lookup"><span data-stu-id="4503c-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>已 **暫** 止 (12) </span><span class="sxs-lookup"><span data-stu-id="4503c-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="4503c-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4503c-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。0xFFFF ) </span><span class="sxs-lookup"><span data-stu-id="4503c-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4503c-258">備註</span><span class="sxs-lookup"><span data-stu-id="4503c-258">Remarks</span></span>

<span data-ttu-id="4503c-259">存取 **Msvm \_ AllocationCapabilities** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="4503c-259">Access to the **Msvm\_AllocationCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4503c-260">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="4503c-260">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4503c-261">規格需求</span><span class="sxs-lookup"><span data-stu-id="4503c-261">Requirements</span></span>



| <span data-ttu-id="4503c-262">需求</span><span class="sxs-lookup"><span data-stu-id="4503c-262">Requirement</span></span> | <span data-ttu-id="4503c-263">值</span><span class="sxs-lookup"><span data-stu-id="4503c-263">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4503c-264">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4503c-264">Minimum supported client</span></span><br/> | <span data-ttu-id="4503c-265">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4503c-265">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4503c-266">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4503c-266">Minimum supported server</span></span><br/> | <span data-ttu-id="4503c-267">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4503c-267">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4503c-268">命名空間</span><span class="sxs-lookup"><span data-stu-id="4503c-268">Namespace</span></span><br/>                | <span data-ttu-id="4503c-269">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="4503c-269">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4503c-270">MOF</span><span class="sxs-lookup"><span data-stu-id="4503c-270">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4503c-271"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="4503c-271"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4503c-272">DLL</span><span class="sxs-lookup"><span data-stu-id="4503c-272">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4503c-273"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4503c-273"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4503c-274">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4503c-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4503c-275">**CIM \_ AllocationCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4503c-275">**CIM\_AllocationCapabilities**</span></span>](cim-allocationcapabilities.md)
</dt> <dt>

[<span data-ttu-id="4503c-276">**CIM \_ AllocationCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4503c-276">**CIM\_AllocationCapabilities**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="4503c-277">**Msvm \_ AllocationCapabilities (V1)**</span><span class="sxs-lookup"><span data-stu-id="4503c-277">**Msvm\_AllocationCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="4503c-278">資源管理類別</span><span class="sxs-lookup"><span data-stu-id="4503c-278">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

