---
description: 代表磁碟區陰影複製服務 (VSS) 服務的設定狀態。
ms.assetid: FAE8E8F7-525A-4E5A-91B3-B73343337352
title: Msvm_VssComponentSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponentSettingData
- Msvm_VssComponentSettingData.InstanceID
- Msvm_VssComponentSettingData.Caption
- Msvm_VssComponentSettingData.Description
- Msvm_VssComponentSettingData.ElementName
- Msvm_VssComponentSettingData.ResourceType
- Msvm_VssComponentSettingData.OtherResourceType
- Msvm_VssComponentSettingData.ResourceSubType
- Msvm_VssComponentSettingData.PoolID
- Msvm_VssComponentSettingData.ConsumerVisibility
- Msvm_VssComponentSettingData.HostResource
- Msvm_VssComponentSettingData.AllocationUnits
- Msvm_VssComponentSettingData.VirtualQuantity
- Msvm_VssComponentSettingData.Reservation
- Msvm_VssComponentSettingData.Limit
- Msvm_VssComponentSettingData.Weight
- Msvm_VssComponentSettingData.AutomaticAllocation
- Msvm_VssComponentSettingData.AutomaticDeallocation
- Msvm_VssComponentSettingData.Parent
- Msvm_VssComponentSettingData.Connection
- Msvm_VssComponentSettingData.Address
- Msvm_VssComponentSettingData.MappingBehavior
- Msvm_VssComponentSettingData.AddressOnParent
- Msvm_VssComponentSettingData.VirtualQuantityUnits
- Msvm_VssComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d37f46c10cc702c66a30fb484553a8c5da03d8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973608"
---
# <a name="msvm_vsscomponentsettingdata-class"></a><span data-ttu-id="8ea8d-103">Msvm \_ VssComponentSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="8ea8d-103">Msvm\_VssComponentSettingData class</span></span>

<span data-ttu-id="8ea8d-104">代表磁碟區陰影複製服務 (VSS) 服務的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-104">Represents the configured state of the Volume Shadow Copy Service (VSS) service.</span></span>

<span data-ttu-id="8ea8d-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea8d-106">語法</span><span class="sxs-lookup"><span data-stu-id="8ea8d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "VSS";
  string  Description = "Microsoft VSS Service Setting Data";
  string  ElementName = "VSS";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:VSS Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource;
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

## <a name="members"></a><span data-ttu-id="8ea8d-107">成員</span><span class="sxs-lookup"><span data-stu-id="8ea8d-107">Members</span></span>

<span data-ttu-id="8ea8d-108">**Msvm \_ VssComponentSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8ea8d-108">The **Msvm\_VssComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="8ea8d-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8ea8d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ea8d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="8ea8d-110">Properties</span></span>

<span data-ttu-id="8ea8d-111">**Msvm \_ VssComponentSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-111">The **Msvm\_VssComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ea8d-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-115">The address of the resource.</span></span> <span data-ttu-id="8ea8d-116">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-120">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="8ea8d-121">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="8ea8d-122">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-126">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="8ea8d-127">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-131">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="8ea8d-132">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-136">指出是否會自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="8ea8d-137">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-141">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-141">A short description of the object.</span></span> <span data-ttu-id="8ea8d-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-143">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-144">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8ea8d-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-146">此資源所連接的目標。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="8ea8d-147">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-151">取用者會看到已配置的資源。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="8ea8d-152">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="8ea8d-153">值</span><span class="sxs-lookup"><span data-stu-id="8ea8d-153">Value</span></span>                                                                        | <span data-ttu-id="8ea8d-154">意義</span><span class="sxs-lookup"><span data-stu-id="8ea8d-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="8ea8d-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8ea8d-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="8ea8d-156">虛擬</span><span class="sxs-lookup"><span data-stu-id="8ea8d-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ea8d-157">**說明**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-160">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-160">A description of the object.</span></span> <span data-ttu-id="8ea8d-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-165">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-165">A display name for the object.</span></span> <span data-ttu-id="8ea8d-166">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-170">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8ea8d-171">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，預設值為 2 (已啟用) 。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and has a default value of 2 (Enabled).</span></span>

<span data-ttu-id="8ea8d-172">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-172">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>



 <span data-ttu-id="8ea8d-173">(2)</span><span class="sxs-lookup"><span data-stu-id="8ea8d-173">(2)</span></span>


</dt> <dd>

<span data-ttu-id="8ea8d-174">已啟用</span><span class="sxs-lookup"><span data-stu-id="8ea8d-174">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-175">3</span><span class="sxs-lookup"><span data-stu-id="8ea8d-175">3</span></span>
</dt> <dd>

<span data-ttu-id="8ea8d-176">Disabled</span><span class="sxs-lookup"><span data-stu-id="8ea8d-176">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8ea8d-177">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-177">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-180">公開特定指派給主機或基礎資源。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-180">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="8ea8d-181">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-181">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-185">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-185">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-186">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-186">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8ea8d-187">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-188">**限制**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-188">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-189">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-191">此配置將授與的上限或最大資源量。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-191">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="8ea8d-192">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-193">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-193">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-194">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-196">指出此資源如何對應至基礎資源。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-196">Indicates how this resource maps to underlying resources.</span></span> <span data-ttu-id="8ea8d-197">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-197">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-198">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-198">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-201">描述資源類型的字串，當定義完善的值無法使用且 **ResourceType** 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-201">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="8ea8d-202">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-202">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-203">**父系**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-203">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-206">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-206">The parent of the resource.</span></span> <span data-ttu-id="8ea8d-207">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-208">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-208">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-211">從中配置資源的資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-211">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="8ea8d-212">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-213">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-213">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-214">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-216">保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-216">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="8ea8d-217">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-218">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-221">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-221">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="8ea8d-222">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-222">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-223">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-223">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-224">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-226">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-226">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="8ea8d-227">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ，而且一律設定為 1 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1 (Other).</span></span>



| <span data-ttu-id="8ea8d-228">值</span><span class="sxs-lookup"><span data-stu-id="8ea8d-228">Value</span></span>                                                                        | <span data-ttu-id="8ea8d-229">意義</span><span class="sxs-lookup"><span data-stu-id="8ea8d-229">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="8ea8d-230"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8ea8d-230"><dt>1</dt></span></span> </dl> | <span data-ttu-id="8ea8d-231">其他</span><span class="sxs-lookup"><span data-stu-id="8ea8d-231">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ea8d-232">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-232">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-233">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-233">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-235">向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-235">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="8ea8d-236">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-237">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-237">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-238">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-240">指定此資源配置的度量單位。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-240">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="8ea8d-241">這個屬性的值是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-241">The value of this property is a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="8ea8d-242">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="8ea8d-243">**Weight**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-243">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ea8d-244">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ea8d-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8ea8d-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ea8d-246">相對於相同資源集區中的其他配置，此配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-246">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="8ea8d-247">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-247">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ea8d-248">備註</span><span class="sxs-lookup"><span data-stu-id="8ea8d-248">Remarks</span></span>

<span data-ttu-id="8ea8d-249">存取 **Msvm \_ VssComponentSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-249">Access to the **Msvm\_VssComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8ea8d-250">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="8ea8d-250">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ea8d-251">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ea8d-251">Requirements</span></span>



| <span data-ttu-id="8ea8d-252">需求</span><span class="sxs-lookup"><span data-stu-id="8ea8d-252">Requirement</span></span> | <span data-ttu-id="8ea8d-253">值</span><span class="sxs-lookup"><span data-stu-id="8ea8d-253">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea8d-254">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ea8d-254">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea8d-255">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ea8d-255">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8ea8d-256">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ea8d-256">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea8d-257">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ea8d-257">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ea8d-258">命名空間</span><span class="sxs-lookup"><span data-stu-id="8ea8d-258">Namespace</span></span><br/>                | <span data-ttu-id="8ea8d-259">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="8ea8d-259">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8ea8d-260">MOF</span><span class="sxs-lookup"><span data-stu-id="8ea8d-260">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ea8d-261"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8ea8d-261"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ea8d-262">DLL</span><span class="sxs-lookup"><span data-stu-id="8ea8d-262">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ea8d-263"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ea8d-263"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8ea8d-264">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ea8d-264">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea8d-265">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-265">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="8ea8d-266">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="8ea8d-266">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

