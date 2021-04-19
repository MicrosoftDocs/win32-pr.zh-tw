---
description: 代表虛擬機器的虛擬處理器設定。
ms.assetid: 2B299793-E1CD-49D4-898C-AE60B49F44F5
title: Msvm_ProcessorSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorSettingData
- Msvm_ProcessorSettingData.InstanceID
- Msvm_ProcessorSettingData.Caption
- Msvm_ProcessorSettingData.Description
- Msvm_ProcessorSettingData.ElementName
- Msvm_ProcessorSettingData.ResourceType
- Msvm_ProcessorSettingData.OtherResourceType
- Msvm_ProcessorSettingData.ResourceSubType
- Msvm_ProcessorSettingData.PoolID
- Msvm_ProcessorSettingData.ConsumerVisibility
- Msvm_ProcessorSettingData.HostResource
- Msvm_ProcessorSettingData.AllocationUnits
- Msvm_ProcessorSettingData.VirtualQuantity
- Msvm_ProcessorSettingData.Reservation
- Msvm_ProcessorSettingData.Limit
- Msvm_ProcessorSettingData.Weight
- Msvm_ProcessorSettingData.AutomaticAllocation
- Msvm_ProcessorSettingData.AutomaticDeallocation
- Msvm_ProcessorSettingData.Parent
- Msvm_ProcessorSettingData.Connection
- Msvm_ProcessorSettingData.Address
- Msvm_ProcessorSettingData.MappingBehavior
- Msvm_ProcessorSettingData.AddressOnParent
- Msvm_ProcessorSettingData.VirtualQuantityUnits
- Msvm_ProcessorSettingData.LimitCPUID
- Msvm_ProcessorSettingData.HwThreadsPerCore
- Msvm_ProcessorSettingData.LimitProcessorFeatures
- Msvm_ProcessorSettingData.MaxProcessorsPerNumaNode
- Msvm_ProcessorSettingData.MaxNumaNodesPerSocket
- Msvm_ProcessorSettingData.EnableHostResourceProtection
- Msvm_ProcessorSettingData.CpuGroupId
- Msvm_ProcessorSettingData.HideHypervisorPresent
- Msvm_ProcessorSettingData.ExposeVirtualizationExtensions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5154105c4deab13f93bb65078a5c9527283620e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993172"
---
# <a name="msvm_processorsettingdata-class"></a><span data-ttu-id="9e439-103">Msvm \_ ProcessorSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="9e439-103">Msvm\_ProcessorSettingData class</span></span>

<span data-ttu-id="9e439-104">代表虛擬機器的虛擬處理器設定。</span><span class="sxs-lookup"><span data-stu-id="9e439-104">Represents the virtual processor settings for a virtual machine.</span></span>

<span data-ttu-id="9e439-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9e439-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e439-106">語法</span><span class="sxs-lookup"><span data-stu-id="9e439-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Processor";
  string  Description = "A logical processor of the hypervisor running on the host computer system.";
  string  ElementName;
  uint16  ResourceType = 3;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Processor";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits = "percent / 1000";
  uint64  VirtualQuantity = "count";
  uint64  Reservation = 0;
  uint64  Limit = 100000;
  uint32  Weight = 100;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  boolean LimitCPUID;
  uint64  HwThreadsPerCore;
  boolean LimitProcessorFeatures;
  uint64  MaxProcessorsPerNumaNode;
  uint64  MaxNumaNodesPerSocket;
  boolean EnableHostResourceProtection;
  string  CpuGroupId;
  boolean HideHypervisorPresent;
  boolean ExposeVirtualizationExtensions;
};
```

## <a name="members"></a><span data-ttu-id="9e439-107">成員</span><span class="sxs-lookup"><span data-stu-id="9e439-107">Members</span></span>

<span data-ttu-id="9e439-108">**Msvm \_ ProcessorSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9e439-108">The **Msvm\_ProcessorSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9e439-109">屬性</span><span class="sxs-lookup"><span data-stu-id="9e439-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e439-110">屬性</span><span class="sxs-lookup"><span data-stu-id="9e439-110">Properties</span></span>

<span data-ttu-id="9e439-111">**Msvm \_ ProcessorSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9e439-111">The **Msvm\_ProcessorSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e439-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="9e439-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="9e439-115">The address of the resource.</span></span> <span data-ttu-id="9e439-116">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="9e439-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-120">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="9e439-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="9e439-121">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="9e439-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="9e439-122">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="9e439-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-126">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="9e439-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="9e439-127">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="9e439-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e439-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-131">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="9e439-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="9e439-132">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="9e439-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e439-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-136">指出是否會自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="9e439-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="9e439-137">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="9e439-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e439-141">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="9e439-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="9e439-142">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="9e439-142">A short description of the object.</span></span> <span data-ttu-id="9e439-143">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9e439-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-144">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="9e439-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-145">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9e439-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9e439-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-147">此資源所連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="9e439-147">The device to which this resource is connected.</span></span> <span data-ttu-id="9e439-148">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="9e439-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-150">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9e439-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-152">描述取用者對已配置資源的可見度。</span><span class="sxs-lookup"><span data-stu-id="9e439-152">Describes the consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="9e439-153">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-154">**CpuGroupId**</span><span class="sxs-lookup"><span data-stu-id="9e439-154">**CpuGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-157">此 VM 所系結的 Cpu 群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e439-157">The Cpu Group Id this VM is bound to.</span></span> <span data-ttu-id="9e439-158">當值為0時，表示未系結至特定的 CPU 群組。</span><span class="sxs-lookup"><span data-stu-id="9e439-158">When value is 0 it means is not bound to a specific CPU group.</span></span>

> [!Note]  
> <span data-ttu-id="9e439-159">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="9e439-159">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="9e439-160">**說明**</span><span class="sxs-lookup"><span data-stu-id="9e439-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-163">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9e439-163">A description of the object.</span></span> <span data-ttu-id="9e439-164">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9e439-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-165">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9e439-165">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-168">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9e439-168">A display name for the object.</span></span> <span data-ttu-id="9e439-169">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9e439-169">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="9e439-170">變更這個屬性將會變更相關聯邏輯裝置衍生的 **ElementName** 。</span><span class="sxs-lookup"><span data-stu-id="9e439-170">Changing this property will change the **ElementName** of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="9e439-171">**EnableHostResourceProtection**</span><span class="sxs-lookup"><span data-stu-id="9e439-171">**EnableHostResourceProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-172">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e439-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-174">指出 VM 是否應啟用功能，以在 VM 中執行的工作負載增加主機資源的保護。</span><span class="sxs-lookup"><span data-stu-id="9e439-174">Indicates whether the VM should enable features that increase the protection of host resources from workload running in the VM.</span></span>

> [!Note]  
> <span data-ttu-id="9e439-175">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="9e439-175">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="9e439-176">**ExposeVirtualizationExtensions**</span><span class="sxs-lookup"><span data-stu-id="9e439-176">**ExposeVirtualizationExtensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-177">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e439-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-179">指出 Hyper-v 是否應該向 VM 公開虛擬化硬體虛擬化延伸模組。</span><span class="sxs-lookup"><span data-stu-id="9e439-179">Indicates whether Hyper-V should expose virtualized hardware virtualization extensions to the VM.</span></span>

> [!Note]  
> <span data-ttu-id="9e439-180">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="9e439-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="9e439-181">**HideHypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="9e439-181">**HideHypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-182">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e439-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-184">指出 Hyper-v 是否應回報虛擬程式存在於已嵌套的來賓中。</span><span class="sxs-lookup"><span data-stu-id="9e439-184">Indicates whether Hyper-V should report that a hypervisor is present to the nested guest.</span></span>

> [!Note]  
> <span data-ttu-id="9e439-185">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="9e439-185">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="9e439-186">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="9e439-186">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-187">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9e439-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9e439-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-189">公開特定指派給主機或基礎資源。</span><span class="sxs-lookup"><span data-stu-id="9e439-189">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="9e439-190">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9e439-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9e439-191">**HwThreadsPerCore**</span><span class="sxs-lookup"><span data-stu-id="9e439-191">**HwThreadsPerCore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-192">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9e439-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-194">指出每個核心回報給來賓的 SMT 執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="9e439-194">Indicates the number of SMT threads per core reported to the guest.</span></span> <span data-ttu-id="9e439-195">這份報告與 SMT 硬體是否存在無關。</span><span class="sxs-lookup"><span data-stu-id="9e439-195">This reporting is independent of whether the hardware for SMT is present.</span></span>

> [!Note]  
> <span data-ttu-id="9e439-196">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="9e439-196">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="9e439-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9e439-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e439-200">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="9e439-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9e439-201">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9e439-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9e439-202">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9e439-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-203">**限制**</span><span class="sxs-lookup"><span data-stu-id="9e439-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-204">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9e439-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-206">虛擬機器可能耗用的最大 CPU 資源數量。</span><span class="sxs-lookup"><span data-stu-id="9e439-206">The maximum amount of CPU resources that may be consumed by the virtual machine.</span></span> <span data-ttu-id="9e439-207">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="9e439-208">100000</span><span class="sxs-lookup"><span data-stu-id="9e439-208">100000</span></span>

<span data-ttu-id="9e439-209">範圍： 0 100000</span><span class="sxs-lookup"><span data-stu-id="9e439-209">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="9e439-210">**LimitCPUID**</span><span class="sxs-lookup"><span data-stu-id="9e439-210">**LimitCPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-211">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e439-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-213">指出虛擬機器是否應降低 CPU 識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e439-213">Indicates whether the virtual machine should lower the CPU identifier.</span></span> <span data-ttu-id="9e439-214">某些較舊的作業系統可能需要您以這種方式限制處理器功能，才能執行。</span><span class="sxs-lookup"><span data-stu-id="9e439-214">Some older operating systems may require you to limit processor functionality in this way in order to run.</span></span>

</dd> <dt>

<span data-ttu-id="9e439-215">**LimitProcessorFeatures**</span><span class="sxs-lookup"><span data-stu-id="9e439-215">**LimitProcessorFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-216">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9e439-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-218">指出虛擬機器是否應限制對作業系統公開的 CPU 功能。</span><span class="sxs-lookup"><span data-stu-id="9e439-218">Indicates whether the virtual machine should limit the CPU features exposed to the operating system.</span></span> <span data-ttu-id="9e439-219">限制處理器功能可讓虛擬機器遷移至具有不同處理器的不同主機電腦系統。</span><span class="sxs-lookup"><span data-stu-id="9e439-219">Limiting the processor features enables the virtual machine to be migrated to different host computer systems with different processors.</span></span> <span data-ttu-id="9e439-220">不支援使用不同廠商的處理器在電腦之間遷移虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9e439-220">Migrating virtual machines between computers with processors from different vendors is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9e439-221">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="9e439-221">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-222">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9e439-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-224">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="9e439-224">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="9e439-225">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-226">**MaxNumaNodesPerSocket**</span><span class="sxs-lookup"><span data-stu-id="9e439-226">**MaxNumaNodesPerSocket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-227">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9e439-227">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-229">可在虛擬機器中觀察到屬於單一處理器通訊端的 NUMA 節點數目上限。</span><span class="sxs-lookup"><span data-stu-id="9e439-229">The maximum number of NUMA nodes that can be observed within the virtual machine as belonging to a single processor socket.</span></span>

</dd> <dt>

<span data-ttu-id="9e439-230">**MaxProcessorsPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="9e439-230">**MaxProcessorsPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-231">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9e439-231">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-233">虛擬機器中可觀察到屬於單一虛擬 NUMA 節點的虛擬處理器數目上限。</span><span class="sxs-lookup"><span data-stu-id="9e439-233">The maximum number of virtual processors that can be observed within the virtual machine as belonging to a single virtual NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="9e439-234">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="9e439-234">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-237">描述資源類型的字串，當定義完善的值無法使用且 **ResourceType** 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="9e439-237">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="9e439-238">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-239">**父系**</span><span class="sxs-lookup"><span data-stu-id="9e439-239">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-242">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="9e439-242">The parent of the resource.</span></span> <span data-ttu-id="9e439-243">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-244">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="9e439-244">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-245">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-247">配置此資源的來源資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e439-247">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="9e439-248">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-249">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="9e439-249">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-250">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9e439-250">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-252">保留給虛擬機器使用的 CPU 資源數量。</span><span class="sxs-lookup"><span data-stu-id="9e439-252">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="9e439-253">這些資源保證可供虛擬機器取用。</span><span class="sxs-lookup"><span data-stu-id="9e439-253">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="9e439-254">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="9e439-255">0</span><span class="sxs-lookup"><span data-stu-id="9e439-255">0</span></span>

<span data-ttu-id="9e439-256">範圍： 0 100000</span><span class="sxs-lookup"><span data-stu-id="9e439-256">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="9e439-257">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="9e439-257">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-260">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="9e439-260">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="9e439-261">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="9e439-261">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="9e439-262">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-263">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="9e439-263">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-264">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9e439-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-266">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="9e439-266">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="9e439-267">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="9e439-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-269">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9e439-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-271">虛擬機器的核心總數。</span><span class="sxs-lookup"><span data-stu-id="9e439-271">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="9e439-272">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="9e439-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9e439-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-276">指定此資源配置的度量單位。</span><span class="sxs-lookup"><span data-stu-id="9e439-276">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="9e439-277">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="9e439-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="9e439-278">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="9e439-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="9e439-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e439-280">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9e439-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e439-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9e439-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e439-282">每個虛擬機器處理器的加權。</span><span class="sxs-lookup"><span data-stu-id="9e439-282">The weight for each virtual machine processor.</span></span> <span data-ttu-id="9e439-283">符合所有保留之後，裝載平臺的剩餘實體處理器容量將會根據其相對權數配置給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9e439-283">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="9e439-284">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="9e439-284">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="9e439-285">100</span><span class="sxs-lookup"><span data-stu-id="9e439-285">100</span></span>

<span data-ttu-id="9e439-286">範圍： 0 10000</span><span class="sxs-lookup"><span data-stu-id="9e439-286">Range: 0 10000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e439-287">備註</span><span class="sxs-lookup"><span data-stu-id="9e439-287">Remarks</span></span>

<span data-ttu-id="9e439-288">存取 **Msvm \_ ProcessorSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="9e439-288">Access to the **Msvm\_ProcessorSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9e439-289">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="9e439-289">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e439-290">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e439-290">Requirements</span></span>



| <span data-ttu-id="9e439-291">需求</span><span class="sxs-lookup"><span data-stu-id="9e439-291">Requirement</span></span> | <span data-ttu-id="9e439-292">值</span><span class="sxs-lookup"><span data-stu-id="9e439-292">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e439-293">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e439-293">Minimum supported client</span></span><br/> | <span data-ttu-id="9e439-294">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e439-294">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9e439-295">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e439-295">Minimum supported server</span></span><br/> | <span data-ttu-id="9e439-296">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e439-296">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e439-297">命名空間</span><span class="sxs-lookup"><span data-stu-id="9e439-297">Namespace</span></span><br/>                | <span data-ttu-id="9e439-298">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="9e439-298">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9e439-299">MOF</span><span class="sxs-lookup"><span data-stu-id="9e439-299">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e439-300"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9e439-300"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e439-301">DLL</span><span class="sxs-lookup"><span data-stu-id="9e439-301">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e439-302"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9e439-302"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9e439-303">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e439-303">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e439-304">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="9e439-304">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="9e439-305">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="9e439-305">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="9e439-306">處理器類別</span><span class="sxs-lookup"><span data-stu-id="9e439-306">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

