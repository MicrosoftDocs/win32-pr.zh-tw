---
description: 代表虛擬機器的記憶體設定狀態。
ms.assetid: 4B6FEE50-1C5F-4F41-B14A-E10B40400A1B
title: Msvm_MemorySettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MemorySettingData
- Msvm_MemorySettingData.InstanceID
- Msvm_MemorySettingData.Caption
- Msvm_MemorySettingData.Description
- Msvm_MemorySettingData.ElementName
- Msvm_MemorySettingData.ResourceType
- Msvm_MemorySettingData.OtherResourceType
- Msvm_MemorySettingData.ResourceSubType
- Msvm_MemorySettingData.PoolID
- Msvm_MemorySettingData.ConsumerVisibility
- Msvm_MemorySettingData.HostResource
- Msvm_MemorySettingData.HugePagesEnabled
- Msvm_MemorySettingData.AllocationUnits
- Msvm_MemorySettingData.VirtualQuantity
- Msvm_MemorySettingData.Reservation
- Msvm_MemorySettingData.Limit
- Msvm_MemorySettingData.Weight
- Msvm_MemorySettingData.AutomaticAllocation
- Msvm_MemorySettingData.AutomaticDeallocation
- Msvm_MemorySettingData.Parent
- Msvm_MemorySettingData.Connection
- Msvm_MemorySettingData.Address
- Msvm_MemorySettingData.MappingBehavior
- Msvm_MemorySettingData.AddressOnParent
- Msvm_MemorySettingData.VirtualQuantityUnits
- Msvm_MemorySettingData.DynamicMemoryEnabled
- Msvm_MemorySettingData.TargetMemoryBuffer
- Msvm_MemorySettingData.IsVirtualized
- Msvm_MemorySettingData.SwapFilesInUse
- Msvm_MemorySettingData.MaxMemoryBlocksPerNumaNode
- Msvm_MemorySettingData.SgxSize
- Msvm_MemorySettingData.SgxEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47309fead7ee45936f34e1e4286ee94437823df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944172"
---
# <a name="msvm_memorysettingdata-class"></a><span data-ttu-id="ef442-103">Msvm \_ MemorySettingData 類別</span><span class="sxs-lookup"><span data-stu-id="ef442-103">Msvm\_MemorySettingData class</span></span>

<span data-ttu-id="ef442-104">代表虛擬機器的記憶體設定狀態。</span><span class="sxs-lookup"><span data-stu-id="ef442-104">Represents the configured state of the memory for a virtual machine.</span></span>

<span data-ttu-id="ef442-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ef442-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef442-106">語法</span><span class="sxs-lookup"><span data-stu-id="ef442-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MemorySettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Memory Default Settings";
  string  Description = "Describes the default settings for the memory resources.";
  string  ElementName;
  uint16  ResourceType = 4;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Memory";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  boolean HugePagesEnabled;
  string  AllocationUnits = "byte * 2^20";
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "byte * 2^20";
  boolean DynamicMemoryEnabled;
  uint32  TargetMemoryBuffer;
  boolean IsVirtualized = True;
  boolean SwapFilesInUse;
  uint64  MaxMemoryBlocksPerNumaNode;
  uint64  SgxSize;
  boolean SgxEnabled;
};
```

## <a name="members"></a><span data-ttu-id="ef442-107">成員</span><span class="sxs-lookup"><span data-stu-id="ef442-107">Members</span></span>

<span data-ttu-id="ef442-108">**Msvm \_ MemorySettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ef442-108">The **Msvm\_MemorySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ef442-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ef442-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef442-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ef442-110">Properties</span></span>

<span data-ttu-id="ef442-111">**Msvm \_ MemorySettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ef442-111">The **Msvm\_MemorySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef442-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="ef442-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="ef442-115">The address of the resource.</span></span> <span data-ttu-id="ef442-116">例如，乙太網路埠的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="ef442-116">For example, the MAC address of an Ethernet port.</span></span> <span data-ttu-id="ef442-117">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="ef442-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-121">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="ef442-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="ef442-122">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="ef442-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="ef442-123">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="ef442-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-127">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="ef442-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="ef442-128">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="ef442-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef442-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-132">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ef442-133">例如，當這個屬性設定為 **True** 且取用中的虛擬機器開啟時，就會配置此資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-133">For example, when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="ef442-134">值為 **False** 表示必須明確配置資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-134">A value of **False** indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="ef442-135">例如，此設定可能代表卸載式媒體 (例如 cd-rom 或磁片) ，而在啟動時，不會顯示媒體。</span><span class="sxs-lookup"><span data-stu-id="ef442-135">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="ef442-136">需要明確操作才能配置資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-136">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="ef442-137">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-138">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="ef442-138">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef442-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-141">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-141">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ef442-142">例如，當這個屬性設定為 **True** 且取用的虛擬機器開啟時，就會配置此資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-142">For example when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="ef442-143">當此屬性為 **False** 時，必須明確配置資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-143">When this property is **False**, the resource must be explicitly allocated.</span></span> <span data-ttu-id="ef442-144">例如，此設定可能代表卸載式媒體 (例如 cd-rom 或磁片) ，而在啟動時，不會顯示媒體。</span><span class="sxs-lookup"><span data-stu-id="ef442-144">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="ef442-145">需要明確操作才能配置資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-145">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="ef442-146">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-147">**標題**</span><span class="sxs-lookup"><span data-stu-id="ef442-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef442-150">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="ef442-150">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ef442-151">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="ef442-151">A short description of the object.</span></span> <span data-ttu-id="ef442-152">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ef442-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-153">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="ef442-153">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-154">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ef442-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef442-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-156">此資源所連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="ef442-156">The device to which this resource is connected.</span></span> <span data-ttu-id="ef442-157">例如，名為網路或交換器埠。</span><span class="sxs-lookup"><span data-stu-id="ef442-157">For example, a named network or switch port.</span></span> <span data-ttu-id="ef442-158">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-158">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="ef442-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-160">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ef442-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-162">描述已配置資源的取用者可見度。</span><span class="sxs-lookup"><span data-stu-id="ef442-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="ef442-163">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-164">**說明**</span><span class="sxs-lookup"><span data-stu-id="ef442-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-167">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="ef442-167">A description of the object.</span></span> <span data-ttu-id="ef442-168">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ef442-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-169">**DynamicMemoryEnabled**</span><span class="sxs-lookup"><span data-stu-id="ef442-169">**DynamicMemoryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-170">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef442-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-172">指出是否已啟用虛擬機器的動態記憶體。</span><span class="sxs-lookup"><span data-stu-id="ef442-172">Indicates whether dynamic memory is enabled for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="ef442-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ef442-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-176">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ef442-176">A display name for the object.</span></span> <span data-ttu-id="ef442-177">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ef442-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-178">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="ef442-178">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-179">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ef442-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef442-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-181">這個陣列的第一個元素包含要指派之基礎主機資源的參考。</span><span class="sxs-lookup"><span data-stu-id="ef442-181">The first element of this array contains a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="ef442-182">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ef442-182">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but it is not used.</span></span>

</dd> <dt>
  
<span data-ttu-id="ef442-183">**HugePagesEnabled**</span><span class="sxs-lookup"><span data-stu-id="ef442-183">**HugePagesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef442-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-186">記憶體是否由1GB 頁面支援。</span><span class="sxs-lookup"><span data-stu-id="ef442-186">Whether the memory is backed by 1GB pages or not.</span></span>

</dd> <dt>

<span data-ttu-id="ef442-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ef442-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef442-190">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="ef442-190">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ef442-191">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ef442-191">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ef442-192">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ef442-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-193">**IsVirtualized**</span><span class="sxs-lookup"><span data-stu-id="ef442-193">**IsVirtualized**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-194">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef442-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-196">指出此裝置是否已虛擬化或傳遞。</span><span class="sxs-lookup"><span data-stu-id="ef442-196">Indicates whether this device is virtualized or passed through.</span></span> <span data-ttu-id="ef442-197">當設定為 **False** 時，就會使用基礎或主機資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-197">When set to **False**, the underlying or host resource is used.</span></span> <span data-ttu-id="ef442-198">**DeviceID** 屬性中至少要有一個專案。</span><span class="sxs-lookup"><span data-stu-id="ef442-198">At least one item should be present in the **DeviceID** property.</span></span> <span data-ttu-id="ef442-199">當設定為 **True** 時，資源會虛擬化，而且可能不會直接對應至基礎/主機資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-199">When set to **True**, the resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="ef442-200">某些實現可能會支援虛擬資源的特定指派，在這種情況下，會使用 **DeviceID** 屬性來公開主機資源。</span><span class="sxs-lookup"><span data-stu-id="ef442-200">Some implementations may support specific assignment for virtualized resources, in which case the host resources are exposed by using the **DeviceID** property.</span></span> <span data-ttu-id="ef442-201">此屬性一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="ef442-201">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="ef442-202">**限制**</span><span class="sxs-lookup"><span data-stu-id="ef442-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-203">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ef442-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-205">虛擬機器可能耗用的最大記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="ef442-205">The maximum amount of memory that may be consumed by the virtual machine.</span></span> <span data-ttu-id="ef442-206">針對已啟用動態記憶體的虛擬機器，這代表最大記憶體設定。</span><span class="sxs-lookup"><span data-stu-id="ef442-206">For a virtual machine with dynamic memory enabled, this represents the maximum memory setting.</span></span> <span data-ttu-id="ef442-207">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="ef442-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-209">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ef442-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-211">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="ef442-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="ef442-212">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-213">**MaxMemoryBlocksPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="ef442-213">**MaxMemoryBlocksPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-214">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ef442-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-216">可在虛擬機器中觀察到屬於單一 NUMA 節點的最大記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="ef442-216">The maximum amount of memory that can be observed within the virtual machine as belonging to a single NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="ef442-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="ef442-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-220">當定義完善的值無法使用且 **ResourceType** 的值為 "Other" 時，描述資源類型的字串。</span><span class="sxs-lookup"><span data-stu-id="ef442-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="ef442-221">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-222">**父系**</span><span class="sxs-lookup"><span data-stu-id="ef442-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-225">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="ef442-225">The parent of the resource.</span></span> <span data-ttu-id="ef442-226">例如，目前配置的控制器。</span><span class="sxs-lookup"><span data-stu-id="ef442-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="ef442-227">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-228">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="ef442-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-231">配置此資源的來源資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef442-231">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="ef442-232">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-233">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="ef442-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-234">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ef442-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-236">指定保證可供此虛擬機器使用的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="ef442-236">Specifies the amount of memory guaranteed to be available for this virtual machine.</span></span> <span data-ttu-id="ef442-237">針對已啟用動態記憶體的虛擬機器，這代表最小記憶體設定。</span><span class="sxs-lookup"><span data-stu-id="ef442-237">For a virtual machine with dynamic memory enabled, this represents the minimum memory setting.</span></span> <span data-ttu-id="ef442-238">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ef442-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-242">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="ef442-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="ef442-243">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="ef442-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="ef442-244">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ef442-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-246">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ef442-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-248">此配置設定所表示的資源類型。</span><span class="sxs-lookup"><span data-stu-id="ef442-248">The type of resource that this allocation setting represents.</span></span> <span data-ttu-id="ef442-249">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為 4 (記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="ef442-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 4 (Memory).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-250">**SgxEnabled**</span><span class="sxs-lookup"><span data-stu-id="ef442-250">**SgxEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-251">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef442-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-253">指出是否已啟用 SGX。</span><span class="sxs-lookup"><span data-stu-id="ef442-253">Indicates if SGX is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="ef442-254">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="ef442-254">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ef442-255">**SgxSize**</span><span class="sxs-lookup"><span data-stu-id="ef442-255">**SgxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-256">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ef442-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-258">要配置給 VM 的 SGX 記憶體數量（以 MB 為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef442-258">The amount of SGX memory to allocate for the VM, in MB.</span></span>

> [!Note]  
> <span data-ttu-id="ef442-259">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="ef442-259">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="ef442-260">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="ef442-260">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-261">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ef442-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-263">如果第二層分頁為使用中，則 **為 True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="ef442-263">**True** if second level paging is active; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="ef442-264">**TargetMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="ef442-264">**TargetMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-265">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef442-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-267">定義在執行時間應該為虛擬機器保留的額外記憶體數量，以虛擬機器所需的總記憶體百分比為單位。</span><span class="sxs-lookup"><span data-stu-id="ef442-267">Defines the amount of extra memory that should be reserved for a virtual machine at runtime, as a percentage of the total memory that the virtual machine is thought to need.</span></span> <span data-ttu-id="ef442-268">這僅適用于已啟用動態記憶體的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ef442-268">This only applies to virtual machines with dynamic memory enabled.</span></span>

<span data-ttu-id="ef442-269">這個屬性可以在5到2000的範圍內。</span><span class="sxs-lookup"><span data-stu-id="ef442-269">This property can be in the range of 5 to 2000.</span></span>

</dd> <dt>

<span data-ttu-id="ef442-270">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="ef442-270">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-271">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ef442-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-273">虛擬機器中的 RAM 總容量，如同客體作業系統所見。</span><span class="sxs-lookup"><span data-stu-id="ef442-273">The total amount of RAM in the virtual machine, as seen by the guest operating system.</span></span> <span data-ttu-id="ef442-274">針對已啟用動態記憶體的虛擬機器，這代表啟動時可用的初始記憶體。</span><span class="sxs-lookup"><span data-stu-id="ef442-274">For a virtual machine with dynamic memory enabled, this represents the initial memory available at startup.</span></span> <span data-ttu-id="ef442-275">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-276">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="ef442-276">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-277">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ef442-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-279">指定此資源配置的度量單位。</span><span class="sxs-lookup"><span data-stu-id="ef442-279">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="ef442-280">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="ef442-280">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="ef442-281">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ef442-282">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ef442-282">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef442-283">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ef442-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef442-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ef442-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef442-285">定義每部虛擬機器的記憶體配置加權值。</span><span class="sxs-lookup"><span data-stu-id="ef442-285">Defines the memory allocation weighting value for each virtual machine.</span></span> <span data-ttu-id="ef442-286">符合所有保留之後，裝載平臺的剩餘記憶體會根據其相對權數配置至虛擬機器， (不超過 **Limit** 屬性) 所指定的值。</span><span class="sxs-lookup"><span data-stu-id="ef442-286">After all reserves have been met, the remaining memory of the hosting platform will be allocated to virtual machines based on their relative weights (not to exceed the value specified by the **Limit** property).</span></span> <span data-ttu-id="ef442-287">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="ef442-287">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef442-288">備註</span><span class="sxs-lookup"><span data-stu-id="ef442-288">Remarks</span></span>

<span data-ttu-id="ef442-289">存取 **Msvm \_ MemorySettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="ef442-289">Access to the **Msvm\_MemorySettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ef442-290">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="ef442-290">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ef442-291">範例</span><span class="sxs-lookup"><span data-stu-id="ef442-291">Examples</span></span>

```powershell
function WaitForResult
{
  param($result)
  if ($result.ReturnValue -eq 4096)
  {
    while($true)
    {
      $result.Job
      if ($result.Job -ne $null)
      {
        if ($result.Job.JobState -gt 4)
        {
          return $result.Job.ErrorCode
        }
      }
      start-sleep 1
    }
  }
  else
  {
    return $result.ReturnValue
  }
}

if ($($args.count) -ne 2)
{
  Write-Host "EnableHugePages.ps1 VMName SizeInMB"
  return
}

$vmName = $args[0]
$sizeInMB = $args[1]
 
$namespace = "root\virtualization\v2"
$vm = Get-WmiObject -class MSVM_ComputerSystem -filter "ElementName='$vmName'" -namespace $namespace
$settings = Get-WmiObject -query "Associators of {$vm} where ResultClass = Msvm_VirtualSystemSettingData" -namespace $namespace
$vmSettings = $settings | ? VirtualSystemType -eq "Microsoft:Hyper-V:System:Realized"
$memorySettings = Get-WmiObject -query "Associators of {$vmSettings} where ResultClass = Msvm_MemorySettingData" -namespace $namespace

$memorySettings.MaxMemoryBlocksPerNumaNode = $sizeInMB
$memorySettings.Reservation = $sizeInMB
$memorySettings.Limit = $sizeInMB
$memorySettings.VirtualQuantity = $sizeInMB
$memorySettings.HugePagesEnabled = $True

$vmSvc = Get-WmiObject -class Msvm_VirtualSystemManagementService -namespace $namespace
$res = $vmSvc.ModifyResourceSettings($memorySettings.GetText(2))
if (WaitForResult($res) -ne 0)
{
  Write-Host "Failed."
}
```

## <a name="requirements"></a><span data-ttu-id="ef442-292">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef442-292">Requirements</span></span>



| <span data-ttu-id="ef442-293">需求</span><span class="sxs-lookup"><span data-stu-id="ef442-293">Requirement</span></span> | <span data-ttu-id="ef442-294">值</span><span class="sxs-lookup"><span data-stu-id="ef442-294">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef442-295">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef442-295">Minimum supported client</span></span><br/> | <span data-ttu-id="ef442-296">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef442-296">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ef442-297">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef442-297">Minimum supported server</span></span><br/> | <span data-ttu-id="ef442-298">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef442-298">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef442-299">命名空間</span><span class="sxs-lookup"><span data-stu-id="ef442-299">Namespace</span></span><br/>                | <span data-ttu-id="ef442-300">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="ef442-300">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ef442-301">MOF</span><span class="sxs-lookup"><span data-stu-id="ef442-301">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef442-302"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ef442-302"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef442-303">DLL</span><span class="sxs-lookup"><span data-stu-id="ef442-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef442-304"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef442-304"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef442-305">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef442-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef442-306">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="ef442-306">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="ef442-307">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="ef442-307">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="ef442-308">記憶體類別</span><span class="sxs-lookup"><span data-stu-id="ef442-308">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

