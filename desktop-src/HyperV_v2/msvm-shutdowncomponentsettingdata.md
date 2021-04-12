---
description: 代表關機服務的設定狀態。
ms.assetid: 434DE26A-E78A-403A-AFAB-2F9272426A16
title: Msvm_ShutdownComponentSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponentSettingData
- Msvm_ShutdownComponentSettingData.InstanceID
- Msvm_ShutdownComponentSettingData.Caption
- Msvm_ShutdownComponentSettingData.Description
- Msvm_ShutdownComponentSettingData.ElementName
- Msvm_ShutdownComponentSettingData.ResourceType
- Msvm_ShutdownComponentSettingData.OtherResourceType
- Msvm_ShutdownComponentSettingData.ResourceSubType
- Msvm_ShutdownComponentSettingData.PoolID
- Msvm_ShutdownComponentSettingData.ConsumerVisibility
- Msvm_ShutdownComponentSettingData.HostResource
- Msvm_ShutdownComponentSettingData.AllocationUnits
- Msvm_ShutdownComponentSettingData.VirtualQuantity
- Msvm_ShutdownComponentSettingData.Reservation
- Msvm_ShutdownComponentSettingData.Limit
- Msvm_ShutdownComponentSettingData.Weight
- Msvm_ShutdownComponentSettingData.AutomaticAllocation
- Msvm_ShutdownComponentSettingData.AutomaticDeallocation
- Msvm_ShutdownComponentSettingData.Parent
- Msvm_ShutdownComponentSettingData.Connection
- Msvm_ShutdownComponentSettingData.Address
- Msvm_ShutdownComponentSettingData.MappingBehavior
- Msvm_ShutdownComponentSettingData.AddressOnParent
- Msvm_ShutdownComponentSettingData.VirtualQuantityUnits
- Msvm_ShutdownComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8ee2fcb910dc788b01a58544bbfe6a06ba215585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191874"
---
# <a name="msvm_shutdowncomponentsettingdata-class"></a><span data-ttu-id="5cc18-103">Msvm \_ ShutdownComponentSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="5cc18-103">Msvm\_ShutdownComponentSettingData class</span></span>

<span data-ttu-id="5cc18-104">代表關機服務的設定狀態。</span><span class="sxs-lookup"><span data-stu-id="5cc18-104">Represents the configured state of the shutdown service.</span></span>

<span data-ttu-id="5cc18-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5cc18-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cc18-106">語法</span><span class="sxs-lookup"><span data-stu-id="5cc18-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Shutdown";
  string  Description = "Microsoft Shutdown Service Setting Data";
  string  ElementName = "Shutdown";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Shutdown Component";
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

## <a name="members"></a><span data-ttu-id="5cc18-107">成員</span><span class="sxs-lookup"><span data-stu-id="5cc18-107">Members</span></span>

<span data-ttu-id="5cc18-108">**Msvm \_ ShutdownComponentSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5cc18-108">The **Msvm\_ShutdownComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5cc18-109">屬性</span><span class="sxs-lookup"><span data-stu-id="5cc18-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5cc18-110">屬性</span><span class="sxs-lookup"><span data-stu-id="5cc18-110">Properties</span></span>

<span data-ttu-id="5cc18-111">**Msvm \_ ShutdownComponentSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5cc18-111">The **Msvm\_ShutdownComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5cc18-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="5cc18-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-115">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="5cc18-115">The address of the resource.</span></span> <span data-ttu-id="5cc18-116">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="5cc18-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-120">描述此資源在父系內容中的位址。</span><span class="sxs-lookup"><span data-stu-id="5cc18-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="5cc18-121">**Parent** 和 **AddressOnParent** 屬性是用來描述控制器的關聯性，以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="5cc18-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="5cc18-122">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="5cc18-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-126">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="5cc18-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="5cc18-127">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="5cc18-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-129">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5cc18-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-131">指出是否會自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="5cc18-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="5cc18-132">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="5cc18-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-134">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5cc18-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-136">指出是否會自動解除配置資源。</span><span class="sxs-lookup"><span data-stu-id="5cc18-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="5cc18-137">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="5cc18-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-141">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="5cc18-141">A short description of the object.</span></span> <span data-ttu-id="5cc18-142">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來的，而且一律設定為「關機」。</span><span class="sxs-lookup"><span data-stu-id="5cc18-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Shutdown".</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-143">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="5cc18-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-144">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="5cc18-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-146">此資源所連接的目標。</span><span class="sxs-lookup"><span data-stu-id="5cc18-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="5cc18-147">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="5cc18-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-149">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5cc18-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-151">取用者會看到已配置的資源。</span><span class="sxs-lookup"><span data-stu-id="5cc18-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="5cc18-152">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="5cc18-153">值</span><span class="sxs-lookup"><span data-stu-id="5cc18-153">Value</span></span>                                                                        | <span data-ttu-id="5cc18-154">意義</span><span class="sxs-lookup"><span data-stu-id="5cc18-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="5cc18-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5cc18-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="5cc18-156">虛擬</span><span class="sxs-lookup"><span data-stu-id="5cc18-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5cc18-157">**說明**</span><span class="sxs-lookup"><span data-stu-id="5cc18-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-160">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5cc18-160">A description of the object.</span></span> <span data-ttu-id="5cc18-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5cc18-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-163">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-165">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5cc18-165">A display name for the object.</span></span> <span data-ttu-id="5cc18-166">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5cc18-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-168">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5cc18-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-170">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="5cc18-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="5cc18-171">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="5cc18-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5cc18-172">**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="5cc18-172">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5cc18-173">**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="5cc18-173">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5cc18-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="5cc18-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-175">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="5cc18-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-177">公開特定指派給主機或基礎資源。</span><span class="sxs-lookup"><span data-stu-id="5cc18-177">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="5cc18-178">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-178">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-179">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5cc18-179">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-182">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="5cc18-182">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-183">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="5cc18-183">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5cc18-184">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-185">**限制**</span><span class="sxs-lookup"><span data-stu-id="5cc18-185">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-186">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5cc18-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-188">此配置將授與的上限或最大資源量。</span><span class="sxs-lookup"><span data-stu-id="5cc18-188">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="5cc18-189">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-190">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="5cc18-190">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-191">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5cc18-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-193">指定此資源對應至基礎資源的方式。</span><span class="sxs-lookup"><span data-stu-id="5cc18-193">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="5cc18-194">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-195">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="5cc18-195">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-198">描述資源類型的字串，當定義完善的值無法使用且 **ResourceType** 的值為1時 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="5cc18-198">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="5cc18-199">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-200">**父系**</span><span class="sxs-lookup"><span data-stu-id="5cc18-200">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-203">資源的父系。</span><span class="sxs-lookup"><span data-stu-id="5cc18-203">The parent of the resource.</span></span> <span data-ttu-id="5cc18-204">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-205">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="5cc18-205">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-208">從中配置資源的資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="5cc18-208">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="5cc18-209">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-210">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="5cc18-210">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-211">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5cc18-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-213">保證可用於此配置的資源數量。</span><span class="sxs-lookup"><span data-stu-id="5cc18-213">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="5cc18-214">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-214">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-215">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="5cc18-215">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-218">字串，描述此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="5cc18-218">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="5cc18-219">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="5cc18-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-221">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5cc18-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-223">此配置設定所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5cc18-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="5cc18-224">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="5cc18-225">值</span><span class="sxs-lookup"><span data-stu-id="5cc18-225">Value</span></span>                                                                        | <span data-ttu-id="5cc18-226">意義</span><span class="sxs-lookup"><span data-stu-id="5cc18-226">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="5cc18-227"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5cc18-227"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5cc18-228">其他</span><span class="sxs-lookup"><span data-stu-id="5cc18-228">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5cc18-229">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="5cc18-229">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-230">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5cc18-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-232">向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="5cc18-232">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="5cc18-233">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-233">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-234">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="5cc18-234">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5cc18-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-237">指定此資源配置的度量單位。</span><span class="sxs-lookup"><span data-stu-id="5cc18-237">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="5cc18-238">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.5 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="5cc18-238">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="5cc18-239">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-239">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="5cc18-240">**Weight**</span><span class="sxs-lookup"><span data-stu-id="5cc18-240">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5cc18-241">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5cc18-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5cc18-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5cc18-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5cc18-243">相對於相同資源集區中的其他配置，此配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="5cc18-243">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="5cc18-244">這個屬性繼承自 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cc18-245">備註</span><span class="sxs-lookup"><span data-stu-id="5cc18-245">Remarks</span></span>

<span data-ttu-id="5cc18-246">存取 **Msvm \_ ShutdownComponentSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="5cc18-246">Access to the **Msvm\_ShutdownComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5cc18-247">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="5cc18-247">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cc18-248">規格需求</span><span class="sxs-lookup"><span data-stu-id="5cc18-248">Requirements</span></span>



| <span data-ttu-id="5cc18-249">需求</span><span class="sxs-lookup"><span data-stu-id="5cc18-249">Requirement</span></span> | <span data-ttu-id="5cc18-250">值</span><span class="sxs-lookup"><span data-stu-id="5cc18-250">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc18-251">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5cc18-251">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc18-252">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cc18-252">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5cc18-253">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5cc18-253">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc18-254">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5cc18-254">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5cc18-255">命名空間</span><span class="sxs-lookup"><span data-stu-id="5cc18-255">Namespace</span></span><br/>                | <span data-ttu-id="5cc18-256">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="5cc18-256">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5cc18-257">MOF</span><span class="sxs-lookup"><span data-stu-id="5cc18-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5cc18-258"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5cc18-258"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5cc18-259">DLL</span><span class="sxs-lookup"><span data-stu-id="5cc18-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cc18-260"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5cc18-260"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5cc18-261">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5cc18-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cc18-262">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="5cc18-262">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="5cc18-263">**CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="5cc18-263">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

