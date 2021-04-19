---
description: 代表來賓服務介面元件的設定狀態。
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Msvm_GuestServiceInterfaceComponentSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972818"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a><span data-ttu-id="fe844-103">Msvm \_ GuestServiceInterfaceComponentSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="fe844-103">Msvm\_GuestServiceInterfaceComponentSettingData class</span></span>

<span data-ttu-id="fe844-104">代表來賓服務介面元件的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="fe844-104">Represents the configured state of the guest service interface component.</span></span> <span data-ttu-id="fe844-105">此類別衍生自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 類別。</span><span class="sxs-lookup"><span data-stu-id="fe844-105">This class derives from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class.</span></span>

<span data-ttu-id="fe844-106">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fe844-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe844-107">語法</span><span class="sxs-lookup"><span data-stu-id="fe844-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a><span data-ttu-id="fe844-108">成員</span><span class="sxs-lookup"><span data-stu-id="fe844-108">Members</span></span>

<span data-ttu-id="fe844-109">**Msvm \_ GuestServiceInterfaceComponentSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fe844-109">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fe844-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fe844-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe844-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fe844-111">Properties</span></span>

<span data-ttu-id="fe844-112">**Msvm \_ GuestServiceInterfaceComponentSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fe844-112">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe844-113">**位址**</span><span class="sxs-lookup"><span data-stu-id="fe844-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe844-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-116">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="fe844-116">The address of the resource.</span></span> <span data-ttu-id="fe844-117">例如，乙太網路埠的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="fe844-117">For example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-118">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="fe844-118">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe844-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-121">這個屬性會指定保留和限制屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="fe844-121">This property specifies the units of allocation used by the Reservation and Limit properties.</span></span> <span data-ttu-id="fe844-122">例如，當 ResourceType = Processor 時，AllocationUnits 可設定為 MHz。</span><span class="sxs-lookup"><span data-stu-id="fe844-122">For example, when ResourceType=Processor, AllocationUnits may be set to MHz.</span></span> <span data-ttu-id="fe844-123">當 ResourceType = Memory 時，AllocationUnits 可設定為 MB</span><span class="sxs-lookup"><span data-stu-id="fe844-123">When ResourceType=Memory, AllocationUnits may be set to MB</span></span>

</dd> <dt>

<span data-ttu-id="fe844-124">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="fe844-124">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-125">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe844-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-127">這個屬性會指定是否要自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="fe844-127">This property specifies if the resource will be automatically allocated.</span></span> <span data-ttu-id="fe844-128">例如，設定為 true 時，當取用的虛擬電腦系統開機時，會配置此資源。</span><span class="sxs-lookup"><span data-stu-id="fe844-128">For example when set to true, when the consuming virtual computer system is powered on, this resource would be allocated.</span></span> <span data-ttu-id="fe844-129">值為 false 表示必須明確配置資源。</span><span class="sxs-lookup"><span data-stu-id="fe844-129">A value of false indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="fe844-130">例如，此設定可能代表卸載式媒體 (也就是 cdrom 或磁片) 在當時的電源上，媒體不存在。</span><span class="sxs-lookup"><span data-stu-id="fe844-130">For example, the setting may represent removable media (that is, cdrom or floppy) where at power on time, the media is not present.</span></span> <span data-ttu-id="fe844-131">需要明確操作才能配置資源。</span><span class="sxs-lookup"><span data-stu-id="fe844-131">An explicit operation is required to allocate the resource.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-132">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="fe844-132">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-133">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fe844-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-135">這個屬性會指定是否要自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="fe844-135">This property specifies if the resource will be automatically deallocated.</span></span> <span data-ttu-id="fe844-136">例如，設定為 true 時，當取用的虛擬電腦系統電源關閉時，就會解除配置此資源。</span><span class="sxs-lookup"><span data-stu-id="fe844-136">For example, when set to true, when the consuming virtual computer system is powered off, this resource would be deallocated.</span></span> <span data-ttu-id="fe844-137">當設定為 false 時，資源仍會保持配置，且必須明確解除配置。</span><span class="sxs-lookup"><span data-stu-id="fe844-137">When set to false, the resource will remain allocated and must be explicitly deallocated.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-138">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="fe844-138">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-139">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fe844-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fe844-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-141">此資源所連接的目標。</span><span class="sxs-lookup"><span data-stu-id="fe844-141">The thing to which this resource is connected.</span></span> <span data-ttu-id="fe844-142">例如，名為網路或交換器埠。</span><span class="sxs-lookup"><span data-stu-id="fe844-142">For example, a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-143">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="fe844-143">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fe844-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-146">描述已配置資源的取用者可見度。</span><span class="sxs-lookup"><span data-stu-id="fe844-146">Describes the consumers visibility to the allocated resource.</span></span>



| <span data-ttu-id="fe844-147">值</span><span class="sxs-lookup"><span data-stu-id="fe844-147">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="fe844-148">意義</span><span class="sxs-lookup"><span data-stu-id="fe844-148">Meaning</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fe844-149"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fe844-149"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                            | <span data-ttu-id="fe844-150">不明。</span><span class="sxs-lookup"><span data-stu-id="fe844-150">Unknown.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <span data-ttu-id="fe844-151"><dt>**傳遞至**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fe844-151"><dt>**Passed-Through**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="fe844-152">基礎或主機資源會利用並傳遞給取用者（可能是使用資料分割）。</span><span class="sxs-lookup"><span data-stu-id="fe844-152">The underlying or host resource is utilized and passed through to the consumer, possibly using partitioning.</span></span> <span data-ttu-id="fe844-153">DeviceID 屬性中至少應該有一個專案。</span><span class="sxs-lookup"><span data-stu-id="fe844-153">At least one item shall be present in the DeviceID property.</span></span><br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <span data-ttu-id="fe844-154"><dt>**虛擬化**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fe844-154"><dt>**Virtualized**</dt> <dt>3</dt></span></span> </dl>                            | <span data-ttu-id="fe844-155">資源已虛擬化，而且可能不會直接對應至基礎/主機資源。</span><span class="sxs-lookup"><span data-stu-id="fe844-155">The resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="fe844-156">某些實現可能會支援虛擬資源的特定指派，在這種情況下，會使用 DeviceID 屬性來公開主機資源 (的) 。</span><span class="sxs-lookup"><span data-stu-id="fe844-156">Some implementations may support specific assignment for virtualized resources, in which case the host resource(s) are exposed using the DeviceID property.</span></span><br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <span data-ttu-id="fe844-157"><dt>**未表示**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fe844-157"><dt>**Not represented**</dt> <dt>4</dt></span></span> </dl>            | <span data-ttu-id="fe844-158">資源取用者的內容中不存在資源的標記法。</span><span class="sxs-lookup"><span data-stu-id="fe844-158">A representation of the resource does not exist within the context of the resource consumer.</span></span><br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="fe844-159">已 <dt>**保留 DMTF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fe844-159"><dt>**DMTF reserved**</dt> <dt>..</dt></span></span> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="fe844-160"><dt>**廠商保留**</dt>的 <dt>32767-65535</dt></span><span class="sxs-lookup"><span data-stu-id="fe844-160"><dt>**Vendor Reserved**</dt> <dt>32767..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="fe844-161">**DefaultEnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="fe844-161">**DefaultEnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-162">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fe844-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-164">預設會啟用和停用來賓通訊服務的狀態。</span><span class="sxs-lookup"><span data-stu-id="fe844-164">The enabled and disabled states of guest communication services by default.</span></span>

<span data-ttu-id="fe844-165">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="fe844-165">This is a read-only property, but it can be changed using the [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="fe844-166">已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="fe844-166">Added in Windows 10.</span></span>

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fe844-167">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="fe844-167">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fe844-168">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="fe844-168">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fe844-169">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fe844-169">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe844-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-172">此 SettingData 實例的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="fe844-172">The display name for this instance of SettingData.</span></span> <span data-ttu-id="fe844-173">此外，顯示名稱可以當做搜尋或查詢的索引屬性使用。</span><span class="sxs-lookup"><span data-stu-id="fe844-173">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="fe844-174"> (附注：名稱在命名空間中不一定是唯一的。 ) </span><span class="sxs-lookup"><span data-stu-id="fe844-174">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="fe844-175">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fe844-175">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-176">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fe844-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-178">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="fe844-178">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="fe844-179">這是唯讀屬性，但是可以使用 ModifyVirtualSystemResources 方法來變更，其方式是在 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 Windows 10 或更新版本) 中使用 [](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice)方法 (或 [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) 。</span><span class="sxs-lookup"><span data-stu-id="fe844-179">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method (or [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 or later) of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="fe844-180">有效值為：</span><span class="sxs-lookup"><span data-stu-id="fe844-180">Valid values are:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fe844-181">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="fe844-181">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fe844-182">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="fe844-182">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fe844-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="fe844-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-184">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fe844-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fe844-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-186">這個屬性會公開特定指派給主機或基礎資源。</span><span class="sxs-lookup"><span data-stu-id="fe844-186">This property exposes specific assignment to host or underlying resources.</span></span> <span data-ttu-id="fe844-187">內嵌的實例應只包含索引鍵屬性，並被視為物件路徑。</span><span class="sxs-lookup"><span data-stu-id="fe844-187">The embedded instances shall contain only key properties and be treated as Object Paths.</span></span> <span data-ttu-id="fe844-188">如果虛擬資源可以針對一些基礎資源進行排程，則此屬性應該保持 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="fe844-188">If the virtual resource may be scheduled on a number of underlying resources, this property should remain **NULL**.</span></span> <span data-ttu-id="fe844-189">在這種情況下，DeviceAllocatedFromPool 或 ResourceAllocationFromPool 關聯可以用來判斷可排程此虛擬資源的主機資源集區。</span><span class="sxs-lookup"><span data-stu-id="fe844-189">In that case, the DeviceAllocatedFromPool or ResourceAllocationFromPool associations may be used to determine the pool of host resources on which this virtual resource may be scheduled.</span></span> <span data-ttu-id="fe844-190">如果使用特定指派，此虛擬資源所使用的所有基礎資源都應列在此陣列中。</span><span class="sxs-lookup"><span data-stu-id="fe844-190">If specific assignment is utilized, all underlying resources used by this virtual resource shall be listed in this array.</span></span> <span data-ttu-id="fe844-191">陣列通常會包含一個專案，但針對匯總配置（例如多個處理器），可能會指定多個主機資源。</span><span class="sxs-lookup"><span data-stu-id="fe844-191">Typically, the array will contain one item, however for aggregate allocations, such as multiple processors, multiple host resources may be specified.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-192">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fe844-192">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe844-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe844-195">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="fe844-195">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fe844-196">在具現化命名空間的範圍內，InstanceID 會以不透明和唯一的方式識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="fe844-196">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fe844-197">若要確保命名空間中的唯一性，InstanceID 的值應使用下列「慣用」演算法來建立： *OrgID*：*LocalID* ，其中 *OrgID* 和 *LocalID* 會以冒號 (： ) ，而且 *OrgID* 必須包含受著作權、商標或其他唯一名稱，而該名稱是由建立或定義 InstanceID 的商務實體所擁有，或是由可辨識的全域授權單位指派給商務實體的註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe844-197">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="fe844-198"> (這項需求類似于架構類別名稱的 *SchemaName* \_ *ClassName* 結構。 ) 此外，為了確保唯一性， *OrgID* 不能包含冒號 (： ) 。</span><span class="sxs-lookup"><span data-stu-id="fe844-198">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="fe844-199">使用此演算法時，InstanceID 中出現的第一個冒號必須出現在 *OrgID* 和 *LocalID* 之間。</span><span class="sxs-lookup"><span data-stu-id="fe844-199">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="fe844-200">*LocalID* 由商務實體選擇，不應重複使用，以找出不同的基礎 (真實世界) 元素。</span><span class="sxs-lookup"><span data-stu-id="fe844-200">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="fe844-201">如果未使用上述的「慣用」演算法，則定義實體必須確保產生的 InstanceID 不會在這個實例的命名空間或其他提供者所產生的任何 InstanceIDs 上重複使用。</span><span class="sxs-lookup"><span data-stu-id="fe844-201">If the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="fe844-202">針對 DMTF 定義的實例，您必須使用「慣用」演算法搭配將 *OrgID* 設定為 CIM。</span><span class="sxs-lookup"><span data-stu-id="fe844-202">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-203">**限制**</span><span class="sxs-lookup"><span data-stu-id="fe844-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-204">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fe844-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-206">這個屬性會指定將為此配置授與的上限或最大資源量。</span><span class="sxs-lookup"><span data-stu-id="fe844-206">This property specifies the upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="fe844-207">例如，支援記憶體分頁的系統可能支援設定低於 VirtualQuantity 的記憶體配置限制，進而強制進行此配置的分頁。</span><span class="sxs-lookup"><span data-stu-id="fe844-207">For example, a system which supports memory paging may support setting the Limit of a Memory allocation below that of the VirtualQuantity, thus forcing paging to occur for this allocation.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="fe844-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-209">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fe844-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-211">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="fe844-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="fe844-212">如果 HostResource 陣列包含任何專案，則此屬性會反映資源對應至這些特定資源的方式。</span><span class="sxs-lookup"><span data-stu-id="fe844-212">If the HostResource array contains any entries, this property reflects how the resource maps to those specific resources.</span></span>

<dl> <dt>

<span data-ttu-id="fe844-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="fe844-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="fe844-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (2) </span><span class="sxs-lookup"><span data-stu-id="fe844-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**軟親和性** (3) </span><span class="sxs-lookup"><span data-stu-id="fe844-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span> (4) 的 **硬性親和性**</span><span class="sxs-lookup"><span data-stu-id="fe844-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="fe844-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32767. 65535) </span><span class="sxs-lookup"><span data-stu-id="fe844-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe844-220">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="fe844-220">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-221">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe844-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-223">描述資源類型的字串，當定義的值無法使用且 ResourceType 的值為 "Other" 時。</span><span class="sxs-lookup"><span data-stu-id="fe844-223">A string that describes the resource type when a well defined value is not available and ResourceType has the value "Other".</span></span>

</dd> <dt>

<span data-ttu-id="fe844-224">**父系**</span><span class="sxs-lookup"><span data-stu-id="fe844-224">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe844-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-227">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="fe844-227">The Parent of the resource.</span></span> <span data-ttu-id="fe844-228">例如，目前配置的控制器。</span><span class="sxs-lookup"><span data-stu-id="fe844-228">For example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-229">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="fe844-229">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe844-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-232">這個屬性會指定資源目前配置來源的 ResourcePool，或在配置發生時要配置資源的 ResourcePool。</span><span class="sxs-lookup"><span data-stu-id="fe844-232">This property specifies which ResourcePool the resource is currently allocated from, or which ResourcePool the resource will be allocated from when the allocation occurs.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-233">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="fe844-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-234">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fe844-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-236">這個屬性會指定保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="fe844-236">This property specifies the amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="fe844-237">在支援過度使用資源的系統上，此值通常會用於許可控制，以防止系統接受配置，進而避免資源耗盡。</span><span class="sxs-lookup"><span data-stu-id="fe844-237">On system which support over-commitment of resources, this value is typically used for admission control to prevent an an allocation from being accepted thus preventing resource depletion.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-238">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="fe844-238">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-239">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fe844-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-241">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="fe844-241">A string describing an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="fe844-242">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="fe844-242">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-243">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="fe844-243">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-244">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fe844-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-246">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="fe844-246">The type of resource this allocation setting represents.</span></span>

<dl> <dt>

<span data-ttu-id="fe844-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="fe844-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="fe844-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="fe844-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="fe844-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="fe844-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="fe844-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="fe844-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="fe844-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="fe844-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="fe844-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="fe844-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="fe844-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="fe844-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="fe844-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="fe844-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="fe844-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**序列埠** (17) </span><span class="sxs-lookup"><span data-stu-id="fe844-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**平行埠** (18) </span><span class="sxs-lookup"><span data-stu-id="fe844-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB 控制器** (19) </span><span class="sxs-lookup"><span data-stu-id="fe844-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**圖形控制器** (20) </span><span class="sxs-lookup"><span data-stu-id="fe844-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**儲存體範圍** (21) </span><span class="sxs-lookup"><span data-stu-id="fe844-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**磁片** (22) </span><span class="sxs-lookup"><span data-stu-id="fe844-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**磁帶** (23) </span><span class="sxs-lookup"><span data-stu-id="fe844-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**其他存放裝置** (24) </span><span class="sxs-lookup"><span data-stu-id="fe844-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="fe844-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="fe844-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="fe844-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**電源供應** 器 (28) </span><span class="sxs-lookup"><span data-stu-id="fe844-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**冷卻裝置** (29) </span><span class="sxs-lookup"><span data-stu-id="fe844-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="fe844-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fe844-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32767. 65535) </span><span class="sxs-lookup"><span data-stu-id="fe844-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe844-278">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="fe844-278">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-279">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fe844-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-281">這個屬性會指定向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="fe844-281">This property specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="fe844-282">例如，當 ResourceType = Processor 時，這個屬性會反映出給虛擬電腦系統的離散處理器數目。</span><span class="sxs-lookup"><span data-stu-id="fe844-282">For example, when ResourceType=Processor, this property would reflect the number of discrete Processors presented to the virtual computer system.</span></span> <span data-ttu-id="fe844-283">當 ResourceType = Memory 時，這個屬性可能會反映回報給虛擬電腦系統的 MB 數。</span><span class="sxs-lookup"><span data-stu-id="fe844-283">When ResourceType=Memory, this property could reflect the number of MB reported to the virtual computer system.</span></span>

</dd> <dt>

<span data-ttu-id="fe844-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="fe844-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe844-285">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fe844-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe844-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fe844-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe844-287">這個屬性會指定此配置相對於相同 ResourcePool 中其他配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="fe844-287">This property specifies a relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="fe844-288">這個屬性沒有測量單位，而且只與其他爭用相同主機資源的配置有關。</span><span class="sxs-lookup"><span data-stu-id="fe844-288">This property has no unit of measure, and is only relevant when compared to other allocations competing for the same host resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe844-289">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe844-289">Requirements</span></span>



| <span data-ttu-id="fe844-290">需求</span><span class="sxs-lookup"><span data-stu-id="fe844-290">Requirement</span></span> | <span data-ttu-id="fe844-291">值</span><span class="sxs-lookup"><span data-stu-id="fe844-291">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe844-292">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe844-292">Minimum supported client</span></span><br/> | <span data-ttu-id="fe844-293">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe844-293">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fe844-294">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe844-294">Minimum supported server</span></span><br/> | <span data-ttu-id="fe844-295">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe844-295">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fe844-296">命名空間</span><span class="sxs-lookup"><span data-stu-id="fe844-296">Namespace</span></span><br/>                | <span data-ttu-id="fe844-297">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="fe844-297">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fe844-298">MOF</span><span class="sxs-lookup"><span data-stu-id="fe844-298">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe844-299"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fe844-299"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe844-300">DLL</span><span class="sxs-lookup"><span data-stu-id="fe844-300">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe844-301"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe844-301"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fe844-302">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe844-302">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe844-303">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="fe844-303">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="fe844-304">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="fe844-304">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

