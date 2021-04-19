---
description: 代表已配置資源的設定，此資源在通常用來代表資源本身的 CIM 類別範圍之外。
ms.assetid: 6261bab9-aa51-479e-bd6a-43c4a9b294a6
title: CIM_ResourceAllocationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationSettingData
- CIM_ResourceAllocationSettingData.ResourceType
- CIM_ResourceAllocationSettingData.OtherResourceType
- CIM_ResourceAllocationSettingData.ResourceSubType
- CIM_ResourceAllocationSettingData.PoolID
- CIM_ResourceAllocationSettingData.ConsumerVisibility
- CIM_ResourceAllocationSettingData.HostResource
- CIM_ResourceAllocationSettingData.AllocationUnits
- CIM_ResourceAllocationSettingData.VirtualQuantity
- CIM_ResourceAllocationSettingData.Reservation
- CIM_ResourceAllocationSettingData.Limit
- CIM_ResourceAllocationSettingData.Weight
- CIM_ResourceAllocationSettingData.AutomaticAllocation
- CIM_ResourceAllocationSettingData.AutomaticDeallocation
- CIM_ResourceAllocationSettingData.Parent
- CIM_ResourceAllocationSettingData.Connection
- CIM_ResourceAllocationSettingData.Address
- CIM_ResourceAllocationSettingData.MappingBehavior
- CIM_ResourceAllocationSettingData.AddressOnParent
- CIM_ResourceAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22289511f454e0d3b128d0e73d32687924c7a7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974687"
---
# <a name="cim_resourceallocationsettingdata-class"></a><span data-ttu-id="24ae7-103">CIM \_ ResourceAllocationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="24ae7-103">CIM\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="24ae7-104">代表已配置資源的設定，此資源在通常用來代表資源本身的 CIM 類別範圍之外。</span><span class="sxs-lookup"><span data-stu-id="24ae7-104">Represents settings for an allocated resource that are outside the scope of the CIM class typically used to represent the resource itself.</span></span> <span data-ttu-id="24ae7-105">這些設定包括資源取用者可能看不到之配置的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="24ae7-105">These settings include information specific to the allocation that may not be visible to the consumer of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ae7-106">語法</span><span class="sxs-lookup"><span data-stu-id="24ae7-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourceAllocationSettingData : CIM_SettingData
{
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
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
};
```

## <a name="members"></a><span data-ttu-id="24ae7-107">成員</span><span class="sxs-lookup"><span data-stu-id="24ae7-107">Members</span></span>

<span data-ttu-id="24ae7-108">**CIM \_ ResourceAllocationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="24ae7-108">The **CIM\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="24ae7-109">屬性</span><span class="sxs-lookup"><span data-stu-id="24ae7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24ae7-110">屬性</span><span class="sxs-lookup"><span data-stu-id="24ae7-110">Properties</span></span>

<span data-ttu-id="24ae7-111">**CIM \_ ResourceAllocationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="24ae7-111">The **CIM\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24ae7-112">**位址**</span><span class="sxs-lookup"><span data-stu-id="24ae7-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24ae7-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-115">資源的位址，例如，乙太網路埠的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="24ae7-115">The address of the resource, for example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-116">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="24ae7-116">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24ae7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-119">此資源的位址（來自父系的內容）。</span><span class="sxs-lookup"><span data-stu-id="24ae7-119">The address of this resource from the context of the parent.</span></span> <span data-ttu-id="24ae7-120">這個屬性是用來描述控制器關聯性以及控制器上的裝置順序。</span><span class="sxs-lookup"><span data-stu-id="24ae7-120">This property is used to describe a controller relationship and the ordering of devices on a controller.</span></span> <span data-ttu-id="24ae7-121">例如，如果父系是 PCI 控制器，則此屬性會指定此子裝置的 PCI 插槽。</span><span class="sxs-lookup"><span data-stu-id="24ae7-121">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-122">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="24ae7-122">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24ae7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-125">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourceAllocationSettingData**.**保留**"，"**CIM \_ ResourceAllocationSettingData**。**Limit**") ， **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="24ae7-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**Reservation**", "**CIM\_ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-126">**保留** 和 **限制** 屬性所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="24ae7-126">The allocation units used by the **Reservation** and **Limit** properties.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-127">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="24ae7-127">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-128">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24ae7-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-130">**true** 表示自動設定資源;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="24ae7-130">**true** to automatically allocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-131">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="24ae7-131">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-132">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24ae7-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-134">**true** 表示自動解除配置資源;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="24ae7-134">**true** to automatically deallocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-135">**[連接]**</span><span class="sxs-lookup"><span data-stu-id="24ae7-135">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-136">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="24ae7-136">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-138">陣列，指出連線到資源的物件，例如已命名的網路或交換器埠。</span><span class="sxs-lookup"><span data-stu-id="24ae7-138">An array that indicates the objects connected to the resource, such as a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-139">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="24ae7-139">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="24ae7-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-142">取用者會看到已配置的資源。</span><span class="sxs-lookup"><span data-stu-id="24ae7-142">The consumers visibility to the allocated resource.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24ae7-143">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="24ae7-143">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>

<span data-ttu-id="24ae7-144">**傳遞** (2) </span><span class="sxs-lookup"><span data-stu-id="24ae7-144">**Passed-Through** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>

<span data-ttu-id="24ae7-145">**虛擬化** (3) </span><span class="sxs-lookup"><span data-stu-id="24ae7-145">**Virtualized** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>

<span data-ttu-id="24ae7-146"> (4) **未表示**</span><span class="sxs-lookup"><span data-stu-id="24ae7-146">**Not represented** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="24ae7-147">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="24ae7-147">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="24ae7-148">**廠商保留** (32767. 65535) </span><span class="sxs-lookup"><span data-stu-id="24ae7-148">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24ae7-149">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="24ae7-149">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-150">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="24ae7-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-152">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourceAllocationSettingData**.**ConsumerVisibility**"，"**CIM \_ ResourceAllocationSettingData**.**MappingBehavior**") </span><span class="sxs-lookup"><span data-stu-id="24ae7-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ConsumerVisibility**", "**CIM\_ResourceAllocationSettingData**.**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-153">陣列，其中包含已配置資源的指派。</span><span class="sxs-lookup"><span data-stu-id="24ae7-153">An array that contains the assignment of the allocated resources.</span></span> <span data-ttu-id="24ae7-154">這個屬性的每個非 null 值都必須格式化為以 RFC3986 為基礎的 URI。</span><span class="sxs-lookup"><span data-stu-id="24ae7-154">Each non-null value of this property must be formated as an RFC3986 based URI.</span></span> <span data-ttu-id="24ae7-155">如果資源已模型化，則此值應該是 WBEM URI。</span><span class="sxs-lookup"><span data-stu-id="24ae7-155">If the resource is modeled, then the value should be a WBEM URI.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-156">**限制**</span><span class="sxs-lookup"><span data-stu-id="24ae7-156">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-157">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="24ae7-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-159">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**") </span><span class="sxs-lookup"><span data-stu-id="24ae7-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-160">要授與配置的資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="24ae7-160">The maximum amount of resource to grant to the allocation.</span></span> <span data-ttu-id="24ae7-161">這個屬性的單位類型是由 **AllocationUnits** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="24ae7-161">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-162">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="24ae7-162">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="24ae7-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-165">指出資源如何對應至基礎資源。</span><span class="sxs-lookup"><span data-stu-id="24ae7-165">Indicates how the resource maps to underlying resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24ae7-166">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="24ae7-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="24ae7-167">**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="24ae7-167">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="24ae7-168">**專用** (3) </span><span class="sxs-lookup"><span data-stu-id="24ae7-168">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="24ae7-169">**軟親和性** (4) </span><span class="sxs-lookup"><span data-stu-id="24ae7-169">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="24ae7-170">**硬性親和性** (5) </span><span class="sxs-lookup"><span data-stu-id="24ae7-170">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="24ae7-171">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="24ae7-171">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="24ae7-172">**廠商保留** (32767. 65535) </span><span class="sxs-lookup"><span data-stu-id="24ae7-172">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24ae7-173">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="24ae7-173">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24ae7-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-176">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourceAllocationSettingData**.**ResourceType**") </span><span class="sxs-lookup"><span data-stu-id="24ae7-176">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-177">當 **ResourceType** 屬性設定為1時 (其他) 的資源類型描述。</span><span class="sxs-lookup"><span data-stu-id="24ae7-177">A description of the resource type when the **ResourceType** property is set to 1 (other).</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-178">**父系**</span><span class="sxs-lookup"><span data-stu-id="24ae7-178">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24ae7-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-181">資源的父系，例如目前配置的控制器。</span><span class="sxs-lookup"><span data-stu-id="24ae7-181">The parent of the resource, for example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-182">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="24ae7-182">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24ae7-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-185">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolId**") </span><span class="sxs-lookup"><span data-stu-id="24ae7-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-186">產生資源的資源集區識別碼。</span><span class="sxs-lookup"><span data-stu-id="24ae7-186">The ID of the resource pool that generated the resource.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-187">**保留容量**</span><span class="sxs-lookup"><span data-stu-id="24ae7-187">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-188">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="24ae7-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-190">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**") </span><span class="sxs-lookup"><span data-stu-id="24ae7-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-191">保證可用於此配置的資源數目。</span><span class="sxs-lookup"><span data-stu-id="24ae7-191">The number of resource that are guaranteed to be available for this allocation.</span></span> <span data-ttu-id="24ae7-192">在支援過度使用資源的系統上，此值通常用於許可控制。</span><span class="sxs-lookup"><span data-stu-id="24ae7-192">On systems that support over-commitment of resources, this value is typically used for admission control.</span></span>

<span data-ttu-id="24ae7-193">這個屬性的單位類型是由 **AllocationUnits** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="24ae7-193">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-194">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="24ae7-194">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24ae7-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-197">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourceAllocationSettingData**.**ResourceType**") </span><span class="sxs-lookup"><span data-stu-id="24ae7-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-198">此資源的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="24ae7-198">An implementation specific sub-type for this resource.</span></span> <span data-ttu-id="24ae7-199">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="24ae7-199">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-200">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="24ae7-200">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-201">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="24ae7-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-203">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourceAllocationSettingData**.**OtherResourceType**"，"**CIM \_ ResourceAllocationSettingData**.**ResourceSubType**") </span><span class="sxs-lookup"><span data-stu-id="24ae7-203">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**OtherResourceType**", "**CIM\_ResourceAllocationSettingData**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-204">配置設定所表示的資源類型。</span><span class="sxs-lookup"><span data-stu-id="24ae7-204">The type of resource that is represented by the allocation settings.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24ae7-205">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="24ae7-205">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="24ae7-206">**電腦系統** (2) </span><span class="sxs-lookup"><span data-stu-id="24ae7-206">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="24ae7-207">**處理器** (3) </span><span class="sxs-lookup"><span data-stu-id="24ae7-207">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="24ae7-208">**記憶體** (4) </span><span class="sxs-lookup"><span data-stu-id="24ae7-208">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="24ae7-209">**IDE 控制器** (5) </span><span class="sxs-lookup"><span data-stu-id="24ae7-209">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="24ae7-210">**平行 SCSI HBA** (6) </span><span class="sxs-lookup"><span data-stu-id="24ae7-210">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="24ae7-211">**FC HBA** (7) </span><span class="sxs-lookup"><span data-stu-id="24ae7-211">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="24ae7-212">**ISCSI HBA** (8) </span><span class="sxs-lookup"><span data-stu-id="24ae7-212">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="24ae7-213">**IB HCA** (9) </span><span class="sxs-lookup"><span data-stu-id="24ae7-213">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="24ae7-214">**乙太網路介面卡** (10) </span><span class="sxs-lookup"><span data-stu-id="24ae7-214">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="24ae7-215">**其他網路介面卡** (11) </span><span class="sxs-lookup"><span data-stu-id="24ae7-215">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="24ae7-216">**I/o 插槽** (12) </span><span class="sxs-lookup"><span data-stu-id="24ae7-216">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="24ae7-217"> (13) 的 **I/o 裝置**</span><span class="sxs-lookup"><span data-stu-id="24ae7-217">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="24ae7-218">**磁片磁碟機** (14) </span><span class="sxs-lookup"><span data-stu-id="24ae7-218">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="24ae7-219">**CD 光碟機** (15) </span><span class="sxs-lookup"><span data-stu-id="24ae7-219">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="24ae7-220">**DVD 光碟機** (16) </span><span class="sxs-lookup"><span data-stu-id="24ae7-220">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="24ae7-221">**磁片磁碟機** (17) </span><span class="sxs-lookup"><span data-stu-id="24ae7-221">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="24ae7-222">**磁帶機** (18) </span><span class="sxs-lookup"><span data-stu-id="24ae7-222">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="24ae7-223">**儲存體範圍** (19) </span><span class="sxs-lookup"><span data-stu-id="24ae7-223">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="24ae7-224">**其他存放裝置** (20) </span><span class="sxs-lookup"><span data-stu-id="24ae7-224">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="24ae7-225">**序列埠** (21) </span><span class="sxs-lookup"><span data-stu-id="24ae7-225">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="24ae7-226">**平行埠** (22) </span><span class="sxs-lookup"><span data-stu-id="24ae7-226">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="24ae7-227">**USB 控制器** (23) </span><span class="sxs-lookup"><span data-stu-id="24ae7-227">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="24ae7-228">**圖形控制器** (24) </span><span class="sxs-lookup"><span data-stu-id="24ae7-228">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="24ae7-229">**IEEE 1394 控制器** (25) </span><span class="sxs-lookup"><span data-stu-id="24ae7-229">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="24ae7-230">**可分割 Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="24ae7-230">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="24ae7-231">**基底可分割單位** (27) </span><span class="sxs-lookup"><span data-stu-id="24ae7-231">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="24ae7-232">**Power** (28) </span><span class="sxs-lookup"><span data-stu-id="24ae7-232">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="24ae7-233">**冷卻容量** (29) </span><span class="sxs-lookup"><span data-stu-id="24ae7-233">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="24ae7-234">**乙太網路交換器埠** (30) </span><span class="sxs-lookup"><span data-stu-id="24ae7-234">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="24ae7-235">**邏輯磁片** (31) </span><span class="sxs-lookup"><span data-stu-id="24ae7-235">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="24ae7-236">**存放磁片區** (32) </span><span class="sxs-lookup"><span data-stu-id="24ae7-236">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="24ae7-237">**Ethernet 連接** (33) </span><span class="sxs-lookup"><span data-stu-id="24ae7-237">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="24ae7-238">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="24ae7-238">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="24ae7-239">**廠商保留** (0x8000。0xFFFF) </span><span class="sxs-lookup"><span data-stu-id="24ae7-239">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24ae7-240">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="24ae7-240">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-241">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="24ae7-241">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-243">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourceAllocationSettingData**.**VirtualQuantityUnits**") </span><span class="sxs-lookup"><span data-stu-id="24ae7-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-244">呈現給資源取用者的資源數目。</span><span class="sxs-lookup"><span data-stu-id="24ae7-244">The number of resources presented to the consumer of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-245">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="24ae7-245">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24ae7-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-248">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ ResourceAllocationSettingData**.**VirtualQuantity**") ， **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="24ae7-248">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-249">**VirtualQuantity** 屬性所使用的單位。</span><span class="sxs-lookup"><span data-stu-id="24ae7-249">The units used by the **VirtualQuantity** property.</span></span>

</dd> <dt>

<span data-ttu-id="24ae7-250">**Weight**</span><span class="sxs-lookup"><span data-stu-id="24ae7-250">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24ae7-251">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="24ae7-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24ae7-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24ae7-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24ae7-253">相對於相同資源集區中的其他配置，此配置的相對優先權。</span><span class="sxs-lookup"><span data-stu-id="24ae7-253">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24ae7-254">規格需求</span><span class="sxs-lookup"><span data-stu-id="24ae7-254">Requirements</span></span>



| <span data-ttu-id="24ae7-255">需求</span><span class="sxs-lookup"><span data-stu-id="24ae7-255">Requirement</span></span> | <span data-ttu-id="24ae7-256">值</span><span class="sxs-lookup"><span data-stu-id="24ae7-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24ae7-257">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24ae7-257">Minimum supported client</span></span><br/> | <span data-ttu-id="24ae7-258">Windows 8</span><span class="sxs-lookup"><span data-stu-id="24ae7-258">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="24ae7-259">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24ae7-259">Minimum supported server</span></span><br/> | <span data-ttu-id="24ae7-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24ae7-260">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="24ae7-261">命名空間</span><span class="sxs-lookup"><span data-stu-id="24ae7-261">Namespace</span></span><br/>                | <span data-ttu-id="24ae7-262">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="24ae7-262">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="24ae7-263">MOF</span><span class="sxs-lookup"><span data-stu-id="24ae7-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24ae7-264"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="24ae7-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24ae7-265">DLL</span><span class="sxs-lookup"><span data-stu-id="24ae7-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24ae7-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24ae7-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24ae7-267">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24ae7-267">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ae7-268">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="24ae7-268">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

