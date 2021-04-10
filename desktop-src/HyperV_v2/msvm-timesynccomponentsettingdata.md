---
description: 表示時間同步處理服務的設定狀態。
ms.assetid: AACEDE11-3F5B-42AB-A16F-0474FA98D3FD
title: Msvm_TimeSyncComponentSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponentSettingData
- Msvm_TimeSyncComponentSettingData.InstanceID
- Msvm_TimeSyncComponentSettingData.Caption
- Msvm_TimeSyncComponentSettingData.Description
- Msvm_TimeSyncComponentSettingData.ElementName
- Msvm_TimeSyncComponentSettingData.ResourceType
- Msvm_TimeSyncComponentSettingData.OtherResourceType
- Msvm_TimeSyncComponentSettingData.ResourceSubType
- Msvm_TimeSyncComponentSettingData.PoolID
- Msvm_TimeSyncComponentSettingData.ConsumerVisibility
- Msvm_TimeSyncComponentSettingData.HostResource
- Msvm_TimeSyncComponentSettingData.AllocationUnits
- Msvm_TimeSyncComponentSettingData.VirtualQuantity
- Msvm_TimeSyncComponentSettingData.Reservation
- Msvm_TimeSyncComponentSettingData.Limit
- Msvm_TimeSyncComponentSettingData.Weight
- Msvm_TimeSyncComponentSettingData.AutomaticAllocation
- Msvm_TimeSyncComponentSettingData.AutomaticDeallocation
- Msvm_TimeSyncComponentSettingData.Parent
- Msvm_TimeSyncComponentSettingData.Connection
- Msvm_TimeSyncComponentSettingData.Address
- Msvm_TimeSyncComponentSettingData.MappingBehavior
- Msvm_TimeSyncComponentSettingData.AddressOnParent
- Msvm_TimeSyncComponentSettingData.VirtualQuantityUnits
- Msvm_TimeSyncComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 063c0f7904976d50d7c1914f810e71ff84f740b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943685"
---
# <a name="msvm_timesynccomponentsettingdata-class"></a><span data-ttu-id="751a9-103">Msvm \_ TimeSyncComponentSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="751a9-103">Msvm\_TimeSyncComponentSettingData class</span></span>

<span data-ttu-id="751a9-104">表示時間同步處理服務的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="751a9-104">Represents the configured state of the time synchronization service.</span></span>

<span data-ttu-id="751a9-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="751a9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="751a9-106">語法</span><span class="sxs-lookup"><span data-stu-id="751a9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Time Synchronization";
  string  Description = "Microsoft Time Synchronization Service Setting Data";
  string  ElementName = "Time Synchronization";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Time Synchronization Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
};
```

## <a name="members"></a><span data-ttu-id="751a9-107">成員</span><span class="sxs-lookup"><span data-stu-id="751a9-107">Members</span></span>

<span data-ttu-id="751a9-108">**Msvm \_ TimeSyncComponentSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="751a9-108">The **Msvm\_TimeSyncComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="751a9-109">屬性</span><span class="sxs-lookup"><span data-stu-id="751a9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="751a9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="751a9-110">Properties</span></span>

<span data-ttu-id="751a9-111">**Msvm \_ TimeSyncComponentSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="751a9-111">The **Msvm\_TimeSyncComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="751a9-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="751a9-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="751a9-115">The address of the resource.</span></span> <span data-ttu-id="751a9-116">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="751a9-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-120">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="751a9-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="751a9-121">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="751a9-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="751a9-122">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="751a9-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-126">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="751a9-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="751a9-127">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="751a9-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="751a9-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-131">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="751a9-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="751a9-132">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="751a9-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="751a9-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-136">指出是否會自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="751a9-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="751a9-137">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="751a9-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-141">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="751a9-141">A short description of the object.</span></span> <span data-ttu-id="751a9-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="751a9-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-143">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="751a9-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-144">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="751a9-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="751a9-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-146">此資源所連接的目標。</span><span class="sxs-lookup"><span data-stu-id="751a9-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="751a9-147">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="751a9-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="751a9-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-151">取用者會看到已配置的資源。</span><span class="sxs-lookup"><span data-stu-id="751a9-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="751a9-152">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="751a9-153">值</span><span class="sxs-lookup"><span data-stu-id="751a9-153">Value</span></span>                                                                        | <span data-ttu-id="751a9-154">意義</span><span class="sxs-lookup"><span data-stu-id="751a9-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="751a9-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="751a9-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="751a9-156">虛擬</span><span class="sxs-lookup"><span data-stu-id="751a9-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="751a9-157">**說明**</span><span class="sxs-lookup"><span data-stu-id="751a9-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-160">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="751a9-160">A description of the object.</span></span> <span data-ttu-id="751a9-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="751a9-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="751a9-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-165">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="751a9-165">A display name for the object.</span></span> <span data-ttu-id="751a9-166">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="751a9-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="751a9-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="751a9-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-170">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="751a9-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="751a9-171">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="751a9-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span></span>

<dt>



 <span data-ttu-id="751a9-172">(2)</span><span class="sxs-lookup"><span data-stu-id="751a9-172">(2)</span></span>


</dt> <dd>

<span data-ttu-id="751a9-173">已啟用</span><span class="sxs-lookup"><span data-stu-id="751a9-173">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="751a9-174">3</span><span class="sxs-lookup"><span data-stu-id="751a9-174">3</span></span>
</dt> <dd>

<span data-ttu-id="751a9-175">Disabled</span><span class="sxs-lookup"><span data-stu-id="751a9-175">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="751a9-176">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="751a9-176">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-177">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="751a9-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="751a9-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-179">公開特定指派給主機或基礎資源。</span><span class="sxs-lookup"><span data-stu-id="751a9-179">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="751a9-180">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="751a9-180">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="751a9-181">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="751a9-181">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="751a9-184">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="751a9-184">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="751a9-185">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="751a9-185">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="751a9-186">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="751a9-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-187">**限制**</span><span class="sxs-lookup"><span data-stu-id="751a9-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-188">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="751a9-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-190">此配置將授與的上限或最大資源量。</span><span class="sxs-lookup"><span data-stu-id="751a9-190">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="751a9-191">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-192">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="751a9-192">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-193">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="751a9-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-195">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="751a9-195">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="751a9-196">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-197">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="751a9-197">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-200">當無法使用定義完善的值，且 **ResourceType** 的值為 "Other" 時，資源類型。</span><span class="sxs-lookup"><span data-stu-id="751a9-200">The resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="751a9-201">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-202">**父系**</span><span class="sxs-lookup"><span data-stu-id="751a9-202">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-205">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="751a9-205">The parent of the resource.</span></span> <span data-ttu-id="751a9-206">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-207">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="751a9-207">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-210">從中配置資源的資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="751a9-210">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="751a9-211">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-212">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="751a9-212">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-213">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="751a9-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-215">保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="751a9-215">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="751a9-216">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-217">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="751a9-217">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-220">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="751a9-220">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="751a9-221">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="751a9-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="751a9-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="751a9-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-223">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="751a9-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-225">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="751a9-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="751a9-226">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="751a9-227">值</span><span class="sxs-lookup"><span data-stu-id="751a9-227">Value</span></span>                                                                        | <span data-ttu-id="751a9-228">意義</span><span class="sxs-lookup"><span data-stu-id="751a9-228">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="751a9-229"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="751a9-229"><dt>1</dt></span></span> </dl> | <span data-ttu-id="751a9-230">其他</span><span class="sxs-lookup"><span data-stu-id="751a9-230">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="751a9-231">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="751a9-231">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-232">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="751a9-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-234">向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="751a9-234">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="751a9-235">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-236">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="751a9-236">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="751a9-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-239">指定此資源配置的度量單位。</span><span class="sxs-lookup"><span data-stu-id="751a9-239">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="751a9-240">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="751a9-240">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="751a9-241">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="751a9-242">**Weight**</span><span class="sxs-lookup"><span data-stu-id="751a9-242">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="751a9-243">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="751a9-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="751a9-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="751a9-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="751a9-245">相對於相同資源集區中的其他配置，此配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="751a9-245">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="751a9-246">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="751a9-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="751a9-247">備註</span><span class="sxs-lookup"><span data-stu-id="751a9-247">Remarks</span></span>

<span data-ttu-id="751a9-248">存取 **Msvm \_ TimeSyncComponentSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="751a9-248">Access to the **Msvm\_TimeSyncComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="751a9-249">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="751a9-249">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="751a9-250">規格需求</span><span class="sxs-lookup"><span data-stu-id="751a9-250">Requirements</span></span>



| <span data-ttu-id="751a9-251">需求</span><span class="sxs-lookup"><span data-stu-id="751a9-251">Requirement</span></span> | <span data-ttu-id="751a9-252">值</span><span class="sxs-lookup"><span data-stu-id="751a9-252">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="751a9-253">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="751a9-253">Minimum supported client</span></span><br/> | <span data-ttu-id="751a9-254">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="751a9-254">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="751a9-255">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="751a9-255">Minimum supported server</span></span><br/> | <span data-ttu-id="751a9-256">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="751a9-256">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="751a9-257">命名空間</span><span class="sxs-lookup"><span data-stu-id="751a9-257">Namespace</span></span><br/>                | <span data-ttu-id="751a9-258">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="751a9-258">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="751a9-259">MOF</span><span class="sxs-lookup"><span data-stu-id="751a9-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="751a9-260"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="751a9-260"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="751a9-261">DLL</span><span class="sxs-lookup"><span data-stu-id="751a9-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="751a9-262"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="751a9-262"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="751a9-263">另請參閱</span><span class="sxs-lookup"><span data-stu-id="751a9-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751a9-264">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="751a9-264">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="751a9-265">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="751a9-265">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

