---
description: 匯總可能配置給虛擬機器的處理器資源。
ms.assetid: 73424568-fa6c-4ed8-9640-a67a6d2829f0
title: Msvm_ProcessorPool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool
- Msvm_ProcessorPool.InstanceID
- Msvm_ProcessorPool.Caption
- Msvm_ProcessorPool.Description
- Msvm_ProcessorPool.ElementName
- Msvm_ProcessorPool.InstallDate
- Msvm_ProcessorPool.Name
- Msvm_ProcessorPool.OperationalStatus
- Msvm_ProcessorPool.StatusDescriptions
- Msvm_ProcessorPool.Status
- Msvm_ProcessorPool.HealthState
- Msvm_ProcessorPool.CommunicationStatus
- Msvm_ProcessorPool.DetailedStatus
- Msvm_ProcessorPool.OperatingStatus
- Msvm_ProcessorPool.PrimaryStatus
- Msvm_ProcessorPool.PoolID
- Msvm_ProcessorPool.Primordial
- Msvm_ProcessorPool.Capacity
- Msvm_ProcessorPool.Reserved
- Msvm_ProcessorPool.ResourceType
- Msvm_ProcessorPool.OtherResourceType
- Msvm_ProcessorPool.ResourceSubType
- Msvm_ProcessorPool.AllocationUnits
- Msvm_ProcessorPool.ConsumedResourceUnits
- Msvm_ProcessorPool.CurrentlyConsumedResource
- Msvm_ProcessorPool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 93927483c23147fd387e24cdc5a550a1771457cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981598"
---
# <a name="msvm_processorpool-class"></a><span data-ttu-id="06109-103">Msvm \_ ProcessorPool 類別</span><span class="sxs-lookup"><span data-stu-id="06109-103">Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="06109-104">匯總可能配置給虛擬機器的處理器資源。</span><span class="sxs-lookup"><span data-stu-id="06109-104">Aggregates the processor resources that may be allocated to a virtual machine.</span></span>

<span data-ttu-id="06109-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="06109-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06109-106">語法</span><span class="sxs-lookup"><span data-stu-id="06109-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID = "Microsoft:GUID\Root";
  boolean  Primordial = False;
  uint64   Capacity;
  uint64   Reserved;
  uint16   ResourceType = 4;
  string   OtherResourceType;
  string   ResourceSubType;
  string   AllocationUnits = "Megabyte";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="06109-107">成員</span><span class="sxs-lookup"><span data-stu-id="06109-107">Members</span></span>

<span data-ttu-id="06109-108">**Msvm \_ ProcessorPool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06109-108">The **Msvm\_ProcessorPool** class has these types of members:</span></span>

-   [<span data-ttu-id="06109-109">方法</span><span class="sxs-lookup"><span data-stu-id="06109-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="06109-110">屬性</span><span class="sxs-lookup"><span data-stu-id="06109-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06109-111">方法</span><span class="sxs-lookup"><span data-stu-id="06109-111">Methods</span></span>

<span data-ttu-id="06109-112">**Msvm \_ ProcessorPool** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="06109-112">The **Msvm\_ProcessorPool** class has these methods.</span></span>



| <span data-ttu-id="06109-113">方法</span><span class="sxs-lookup"><span data-stu-id="06109-113">Method</span></span>                                                                          | <span data-ttu-id="06109-114">描述</span><span class="sxs-lookup"><span data-stu-id="06109-114">Description</span></span>                                           |
|:--------------------------------------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="06109-115">**CalculatePossibleReserve**</span><span class="sxs-lookup"><span data-stu-id="06109-115">**CalculatePossibleReserve**</span></span>](calculatepossiblereserve-msvm-processorpool.md) | <span data-ttu-id="06109-116">用來尋找實際的處理器保留。</span><span class="sxs-lookup"><span data-stu-id="06109-116">Used to find the actual processor reserve.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="06109-117">屬性</span><span class="sxs-lookup"><span data-stu-id="06109-117">Properties</span></span>

<span data-ttu-id="06109-118">**Msvm \_ ProcessorPool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="06109-118">The **Msvm\_ProcessorPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06109-119">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="06109-119">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-122">資源集區所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="06109-122">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="06109-123">這個屬性會繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，而且會設定為「mb」。</span><span class="sxs-lookup"><span data-stu-id="06109-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="06109-124">**容量**</span><span class="sxs-lookup"><span data-stu-id="06109-124">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-125">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06109-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06109-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-127">資源集區可支援的有效保留 (的最大數量單位為 **AllocationUnits**) 。</span><span class="sxs-lookup"><span data-stu-id="06109-127">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="06109-128">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06109-128">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06109-129">**標題**</span><span class="sxs-lookup"><span data-stu-id="06109-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-130">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-132">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="06109-132">A short description of the object.</span></span> <span data-ttu-id="06109-133">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06109-134">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="06109-134">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-135">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06109-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06109-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-137">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="06109-137">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="06109-138">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="06109-138">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06109-139">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="06109-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06109-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06109-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="06109-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06109-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="06109-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06109-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="06109-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06109-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="06109-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="06109-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06109-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="06109-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="06109-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="06109-147">)</span><span class="sxs-lookup"><span data-stu-id="06109-147">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06109-148">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="06109-148">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-151">指定 **MaxConsumableResource** 和 **CurrentlyConsumedResource** 屬性的單位。</span><span class="sxs-lookup"><span data-stu-id="06109-151">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="06109-152">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06109-152">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06109-153">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="06109-153">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-154">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06109-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06109-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-156">指定資源集區目前向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="06109-156">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="06109-157">這個屬性與 **保留** 的屬性不同，因為它會描述資源的取用者觀點，而 **保留** 的屬性則會描述資源的產生者觀點。</span><span class="sxs-lookup"><span data-stu-id="06109-157">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="06109-158">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06109-158">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06109-159">**說明**</span><span class="sxs-lookup"><span data-stu-id="06109-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-162">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="06109-162">A description of the object.</span></span> <span data-ttu-id="06109-163">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06109-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="06109-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06109-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06109-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-167">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="06109-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="06109-168">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="06109-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06109-169">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="06109-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="06109-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06109-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="06109-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06109-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="06109-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06109-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="06109-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06109-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="06109-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="06109-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="06109-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="06109-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06109-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="06109-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="06109-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="06109-178">)</span><span class="sxs-lookup"><span data-stu-id="06109-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06109-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="06109-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-182">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="06109-182">A display name for the object.</span></span> <span data-ttu-id="06109-183">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06109-184">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="06109-184">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-185">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06109-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06109-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-187">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="06109-187">The current health of the element.</span></span> <span data-ttu-id="06109-188">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06109-189">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="06109-189">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-190">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="06109-190">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="06109-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-192">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="06109-192">The date and time when the object was installed.</span></span> <span data-ttu-id="06109-193">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="06109-193">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="06109-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06109-195">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="06109-195">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06109-198">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="06109-198">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="06109-199">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="06109-199">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="06109-200">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="06109-201">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="06109-201">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-202">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06109-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06109-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-204">指定資源集區可向取用者呈現的可耗用資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="06109-204">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="06109-205">這個屬性與 [ **容量** ] 屬性不同的是，它會描述資源的取用者觀點，而 [ **容量** ] 屬性則是描述資源的生產者視圖。</span><span class="sxs-lookup"><span data-stu-id="06109-205">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="06109-206">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06109-206">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06109-207">**名稱**</span><span class="sxs-lookup"><span data-stu-id="06109-207">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-210">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="06109-210">The label by which the object is known.</span></span> <span data-ttu-id="06109-211">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06109-212">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="06109-212">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-213">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06109-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06109-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-215">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="06109-215">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="06109-216">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="06109-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06109-217">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="06109-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06109-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06109-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="06109-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06109-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="06109-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06109-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="06109-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06109-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="06109-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="06109-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="06109-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="06109-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="06109-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="06109-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="06109-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="06109-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="06109-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="06109-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="06109-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="06109-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="06109-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="06109-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="06109-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="06109-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="06109-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="06109-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="06109-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="06109-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="06109-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="06109-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="06109-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="06109-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="06109-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="06109-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06109-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="06109-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="06109-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="06109-237">)</span><span class="sxs-lookup"><span data-stu-id="06109-237">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06109-238">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="06109-238">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-239">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="06109-239">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="06109-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-241">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="06109-241">The current statuses of the object.</span></span> <span data-ttu-id="06109-242">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-242">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="06109-243">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="06109-243">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-244">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-246">描述資源類型的字串，當無法使用定義完善的值，並將 **ResourceType** 設定為 0 ( "Other" ) 。</span><span class="sxs-lookup"><span data-stu-id="06109-246">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to 0 ("Other").</span></span> <span data-ttu-id="06109-247">這個屬性會繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="06109-247">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="06109-248">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="06109-248">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-250">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-251">從這個集區配置的 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 實例會參考此值。</span><span class="sxs-lookup"><span data-stu-id="06109-251">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="06109-252">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，而且一律設定為 "Microsoft：*GUID* \\ Root"。</span><span class="sxs-lookup"><span data-stu-id="06109-252">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="06109-253">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="06109-253">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-254">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06109-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06109-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-256">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="06109-256">Provides high level status information.</span></span> <span data-ttu-id="06109-257">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="06109-257">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="06109-258">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="06109-258">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="06109-259">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="06109-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="06109-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06109-261"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="06109-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06109-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="06109-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06109-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="06109-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06109-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="06109-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="06109-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="06109-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="06109-266">)</span><span class="sxs-lookup"><span data-stu-id="06109-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06109-267">**原始**</span><span class="sxs-lookup"><span data-stu-id="06109-267">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-268">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="06109-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06109-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-270">如果此資源集區是資源管理活動中用來繪製和傳回資源的基礎，則為 **True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="06109-270">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="06109-271">原始的意思是，此模型的取用者無法建立或刪除此資源集區。</span><span class="sxs-lookup"><span data-stu-id="06109-271">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="06109-272">不過，其他執行模型化的動作可能會影響原始資源集區的特性或大小。</span><span class="sxs-lookup"><span data-stu-id="06109-272">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="06109-273">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06109-273">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06109-274">**已保留**</span><span class="sxs-lookup"><span data-stu-id="06109-274">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-275">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="06109-275">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06109-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-277">目前的保留 (單位為 **AllocationUnits**) 分散到此集區的所有作用中配置。</span><span class="sxs-lookup"><span data-stu-id="06109-277">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="06109-278">在階層式設定中，這代表所有子系資源集區目前保留的總和。</span><span class="sxs-lookup"><span data-stu-id="06109-278">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="06109-279">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06109-279">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06109-280">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="06109-280">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-281">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-283">字串，描述這個集區的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="06109-283">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="06109-284">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="06109-284">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="06109-285">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="06109-285">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06109-286">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="06109-286">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-287">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="06109-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06109-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-289">此資源集區可能配置的資源類型。</span><span class="sxs-lookup"><span data-stu-id="06109-289">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="06109-290">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，它會設定為 4 ( 「記憶體」 ) 。</span><span class="sxs-lookup"><span data-stu-id="06109-290">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="06109-291">**狀態**</span><span class="sxs-lookup"><span data-stu-id="06109-291">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="06109-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06109-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-294">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="06109-294">The current status of the object.</span></span> <span data-ttu-id="06109-295">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="06109-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="06109-296">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="06109-296">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06109-297">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="06109-297">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06109-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="06109-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06109-299">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="06109-299">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="06109-300">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="06109-300">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06109-301">備註</span><span class="sxs-lookup"><span data-stu-id="06109-301">Remarks</span></span>

<span data-ttu-id="06109-302">存取 **Msvm \_ ProcessorPool** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="06109-302">Access to the **Msvm\_ProcessorPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="06109-303">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="06109-303">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="06109-304">規格需求</span><span class="sxs-lookup"><span data-stu-id="06109-304">Requirements</span></span>



| <span data-ttu-id="06109-305">需求</span><span class="sxs-lookup"><span data-stu-id="06109-305">Requirement</span></span> | <span data-ttu-id="06109-306">值</span><span class="sxs-lookup"><span data-stu-id="06109-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06109-307">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06109-307">Minimum supported client</span></span><br/> | <span data-ttu-id="06109-308">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06109-308">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="06109-309">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06109-309">Minimum supported server</span></span><br/> | <span data-ttu-id="06109-310">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06109-310">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06109-311">命名空間</span><span class="sxs-lookup"><span data-stu-id="06109-311">Namespace</span></span><br/>                | <span data-ttu-id="06109-312">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="06109-312">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="06109-313">MOF</span><span class="sxs-lookup"><span data-stu-id="06109-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06109-314"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="06109-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06109-315">DLL</span><span class="sxs-lookup"><span data-stu-id="06109-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06109-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06109-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06109-317">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06109-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06109-318">**CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="06109-318">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="06109-319">[**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="06109-319">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="06109-320">處理器類別</span><span class="sxs-lookup"><span data-stu-id="06109-320">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

