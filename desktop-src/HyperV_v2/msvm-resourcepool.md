---
description: 描述可在虛擬機器中使用的虛擬資源類型。
ms.assetid: A93D990E-D921-4113-8D88-218D0F84EFA0
title: Msvm_ResourcePool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePool
- Msvm_ResourcePool.InstanceID
- Msvm_ResourcePool.Caption
- Msvm_ResourcePool.Description
- Msvm_ResourcePool.ElementName
- Msvm_ResourcePool.InstallDate
- Msvm_ResourcePool.Name
- Msvm_ResourcePool.OperationalStatus
- Msvm_ResourcePool.StatusDescriptions
- Msvm_ResourcePool.Status
- Msvm_ResourcePool.HealthState
- Msvm_ResourcePool.CommunicationStatus
- Msvm_ResourcePool.DetailedStatus
- Msvm_ResourcePool.OperatingStatus
- Msvm_ResourcePool.PrimaryStatus
- Msvm_ResourcePool.PoolID
- Msvm_ResourcePool.Primordial
- Msvm_ResourcePool.Capacity
- Msvm_ResourcePool.Reserved
- Msvm_ResourcePool.ResourceType
- Msvm_ResourcePool.OtherResourceType
- Msvm_ResourcePool.ResourceSubType
- Msvm_ResourcePool.AllocationUnits
- Msvm_ResourcePool.ConsumedResourceUnits
- Msvm_ResourcePool.CurrentlyConsumedResource
- Msvm_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c45f67a3e1b7c2b4b5291b24beddcdd4cf5e964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193318"
---
# <a name="msvm_resourcepool-class"></a><span data-ttu-id="0decf-103">Msvm \_ ResourcePool 類別</span><span class="sxs-lookup"><span data-stu-id="0decf-103">Msvm\_ResourcePool class</span></span>

<span data-ttu-id="0decf-104">描述可在虛擬機器中使用的虛擬資源類型。</span><span class="sxs-lookup"><span data-stu-id="0decf-104">Describes a type of virtual resource available for use in virtual machines.</span></span> <span data-ttu-id="0decf-105">資源集區會匯總實體資源，並且用來將資源配置給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0decf-105">The resource pool aggregates physical resources and is used to allocate resources to virtual machines.</span></span> <span data-ttu-id="0decf-106">在 Hyper-v 中，所有資源集區都是原始的，而且每個特定類型的資源正好有一個集區可配置給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0decf-106">In Hyper-V, all resource pools are primordial, and there is exactly one pool for each specific type of resource which may be allocated to a virtual machine.</span></span>

<span data-ttu-id="0decf-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0decf-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0decf-108">語法</span><span class="sxs-lookup"><span data-stu-id="0decf-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePool : CIM_ResourcePool
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

## <a name="members"></a><span data-ttu-id="0decf-109">成員</span><span class="sxs-lookup"><span data-stu-id="0decf-109">Members</span></span>

<span data-ttu-id="0decf-110">**Msvm \_ ResourcePool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0decf-110">The **Msvm\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="0decf-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0decf-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0decf-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0decf-112">Properties</span></span>

<span data-ttu-id="0decf-113">**Msvm \_ ResourcePool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0decf-113">The **Msvm\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0decf-114">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="0decf-114">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-117">資源集區所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="0decf-117">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="0decf-118">這個屬性會繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，而且會設定為「mb」。</span><span class="sxs-lookup"><span data-stu-id="0decf-118">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="0decf-119">**容量**</span><span class="sxs-lookup"><span data-stu-id="0decf-119">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-120">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0decf-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-122">資源集區可支援的有效保留 (的最大數量單位為 **AllocationUnits**) 。</span><span class="sxs-lookup"><span data-stu-id="0decf-122">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="0decf-123">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0decf-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="0decf-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-127">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="0decf-127">A short description of the object.</span></span> <span data-ttu-id="0decf-128">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0decf-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0decf-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-132">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="0decf-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0decf-133">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0decf-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0decf-134">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0decf-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0decf-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="0decf-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="0decf-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="0decf-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="0decf-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0decf-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0decf-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0decf-142">)</span><span class="sxs-lookup"><span data-stu-id="0decf-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0decf-143">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="0decf-143">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-146">指定 **MaxConsumableResource** 和 **CurrentlyConsumedResource** 屬性的單位。</span><span class="sxs-lookup"><span data-stu-id="0decf-146">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span>

</dd> <dt>

<span data-ttu-id="0decf-147">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="0decf-147">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-148">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0decf-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-150">指定資源集區目前向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="0decf-150">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="0decf-151">這個屬性與 **保留** 的屬性不同，因為它會描述資源的取用者觀點，而 **保留** 的屬性則會描述資源的產生者觀點。</span><span class="sxs-lookup"><span data-stu-id="0decf-151">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="0decf-152">**說明**</span><span class="sxs-lookup"><span data-stu-id="0decf-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-155">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="0decf-155">A description of the object.</span></span> <span data-ttu-id="0decf-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0decf-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-158">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0decf-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-160">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0decf-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0decf-161">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0decf-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0decf-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0decf-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="0decf-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="0decf-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="0decf-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="0decf-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="0decf-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="0decf-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0decf-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0decf-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0decf-171">)</span><span class="sxs-lookup"><span data-stu-id="0decf-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0decf-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0decf-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-175">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0decf-175">A display name for the object.</span></span> <span data-ttu-id="0decf-176">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-177">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0decf-177">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-178">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0decf-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-180">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="0decf-180">The current health of the element.</span></span> <span data-ttu-id="0decf-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-182">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0decf-182">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-183">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0decf-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-185">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0decf-185">The date and time when the object was installed.</span></span> <span data-ttu-id="0decf-186">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="0decf-186">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="0decf-187">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-188">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0decf-188">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0decf-191">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="0decf-191">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0decf-192">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="0decf-192">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0decf-193">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-194">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="0decf-194">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-195">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0decf-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-197">指定資源集區可向取用者呈現的可耗用資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="0decf-197">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="0decf-198">這個屬性與 [ **容量** ] 屬性不同的是，它會描述資源的取用者觀點，而 [ **容量** ] 屬性則是描述資源的生產者視圖。</span><span class="sxs-lookup"><span data-stu-id="0decf-198">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="0decf-199">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0decf-199">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-202">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0decf-202">The label by which the object is known.</span></span> <span data-ttu-id="0decf-203">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-204">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0decf-204">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-205">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0decf-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-207">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0decf-207">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0decf-208">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0decf-208">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0decf-209">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0decf-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0decf-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="0decf-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="0decf-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="0decf-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="0decf-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="0decf-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="0decf-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="0decf-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="0decf-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="0decf-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="0decf-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="0decf-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="0decf-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="0decf-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="0decf-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="0decf-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="0decf-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0decf-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0decf-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0decf-229">)</span><span class="sxs-lookup"><span data-stu-id="0decf-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0decf-230">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0decf-230">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-231">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0decf-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0decf-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0decf-233">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "OperationalStatus" ) ， [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) </span><span class="sxs-lookup"><span data-stu-id="0decf-233">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0decf-234">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0decf-234">The current statuses of the object.</span></span> <span data-ttu-id="0decf-235">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="0decf-236">如果未偵測到任何 QoS 相關的狀況，則會將主要狀態 (OperationalStatus \[ 0 \]) 設定為 [確定] (2) 。</span><span class="sxs-lookup"><span data-stu-id="0decf-236">If no QoS related conditions have been detected, the primary status (OperationalStatus\[0\]) is set to OK (2).</span></span> <span data-ttu-id="0decf-237">否則，主要狀態會設定為 [降級 (3) ]，並在陣列中填入一個或多個次要狀態值（從索引1開始），此值會根據此資料表來報告更具體的條件。</span><span class="sxs-lookup"><span data-stu-id="0decf-237">Otherwise, the primary status is set to Degraded (3), and one or more secondary status values is filled in the array, starting at index 1, which report more specific conditions, according to this table.</span></span>



| <span data-ttu-id="0decf-238">值</span><span class="sxs-lookup"><span data-stu-id="0decf-238">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="0decf-239">描述</span><span class="sxs-lookup"><span data-stu-id="0decf-239">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0decf-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> 輸送量不足 (32788) </span><span class="sxs-lookup"><span data-stu-id="0decf-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="0decf-241">至少有一個從集區配置的虛擬磁片目前回報的輸送量狀態不足。</span><span class="sxs-lookup"><span data-stu-id="0decf-241">At least one of the virtual disks allocated from the pool is currently reporting an  Insufficient Throughput  status.</span></span><br/> |



 

<span data-ttu-id="0decf-242">Hyper-v WMI 提供者會在每次 **Msvm \_ ResourcePool** 類別的 OperationalStatus 變更時引發 [**Msvm \_ StorageAlert**](msvm-storagealert.md)事件。</span><span class="sxs-lookup"><span data-stu-id="0decf-242">The Hyper-V WMI provider raises an [**Msvm\_StorageAlert**](msvm-storagealert.md) event each time the OperationalStatus of the **Msvm\_ResourcePool** class changes.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0decf-243">**確定** (2) </span><span class="sxs-lookup"><span data-stu-id="0decf-243">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0decf-244"> (3) **降級**</span><span class="sxs-lookup"><span data-stu-id="0decf-244">**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="0decf-245">**無法復原的錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="0decf-245">**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0decf-246">**沒有連絡人** (12) </span><span class="sxs-lookup"><span data-stu-id="0decf-246">**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="0decf-247">**遺失通訊** (13) </span><span class="sxs-lookup"><span data-stu-id="0decf-247">**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="0decf-248">**通訊協定不相符** (32775) </span><span class="sxs-lookup"><span data-stu-id="0decf-248">**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="0decf-249">**輸送量不足** (32788) </span><span class="sxs-lookup"><span data-stu-id="0decf-249">**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0decf-250">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="0decf-250">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-253">描述資源類型的字串，當無法使用定義完善的值，並將 [**ResourceType**](msvm-processorpool.md) 設定為 0 ( "Other" ) 。</span><span class="sxs-lookup"><span data-stu-id="0decf-253">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="0decf-254">這個屬性會繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) ，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0decf-254">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0decf-255">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="0decf-255">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-256">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-258">從這個集區配置的 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 實例會參考此值。</span><span class="sxs-lookup"><span data-stu-id="0decf-258">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="0decf-259">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，而且一律設定為 "Microsoft：*GUID* \\ Root"。</span><span class="sxs-lookup"><span data-stu-id="0decf-259">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="0decf-260">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0decf-260">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-261">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0decf-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-263">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0decf-263">Provides high level status information.</span></span> <span data-ttu-id="0decf-264">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="0decf-264">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0decf-265">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0decf-265">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0decf-266">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0decf-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0decf-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-268"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="0decf-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="0decf-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="0decf-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0decf-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0decf-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0decf-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0decf-273">)</span><span class="sxs-lookup"><span data-stu-id="0decf-273">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0decf-274">**原始**</span><span class="sxs-lookup"><span data-stu-id="0decf-274">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-275">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0decf-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-277">如果此資源集區是資源管理活動中用來繪製和傳回資源的基礎，則為 **True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="0decf-277">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="0decf-278">原始的意思是，此模型的取用者無法建立或刪除此資源集區。</span><span class="sxs-lookup"><span data-stu-id="0decf-278">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="0decf-279">不過，其他執行模型化的動作可能會影響原始資源集區的特性或大小。</span><span class="sxs-lookup"><span data-stu-id="0decf-279">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="0decf-280">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0decf-280">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-281">**已保留**</span><span class="sxs-lookup"><span data-stu-id="0decf-281">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-282">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0decf-282">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-284">目前的保留 (單位為 **AllocationUnits**) 分散到此集區的所有作用中配置。</span><span class="sxs-lookup"><span data-stu-id="0decf-284">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="0decf-285">在階層式設定中，這代表所有子系資源集區目前保留的總和。</span><span class="sxs-lookup"><span data-stu-id="0decf-285">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="0decf-286">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0decf-286">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-287">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="0decf-287">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-290">字串，描述這個集區的執行特定子類型。</span><span class="sxs-lookup"><span data-stu-id="0decf-290">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="0decf-291">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="0decf-291">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="0decf-292">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0decf-292">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0decf-293">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0decf-293">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-294">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0decf-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-296">此資源集區可能配置的資源類型。</span><span class="sxs-lookup"><span data-stu-id="0decf-296">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="0decf-297">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，它會設定為 4 ( 「記憶體」 ) 。</span><span class="sxs-lookup"><span data-stu-id="0decf-297">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="0decf-298">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0decf-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-299">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0decf-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0decf-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-301">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0decf-301">The current status of the object.</span></span> <span data-ttu-id="0decf-302">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0decf-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0decf-303">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0decf-303">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0decf-304">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0decf-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0decf-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0decf-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0decf-306">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="0decf-306">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0decf-307">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0decf-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0decf-308">備註</span><span class="sxs-lookup"><span data-stu-id="0decf-308">Remarks</span></span>

<span data-ttu-id="0decf-309">存取 **Msvm \_ ResourcePool** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="0decf-309">Access to the **Msvm\_ResourcePool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0decf-310">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="0decf-310">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0decf-311">規格需求</span><span class="sxs-lookup"><span data-stu-id="0decf-311">Requirements</span></span>



| <span data-ttu-id="0decf-312">需求</span><span class="sxs-lookup"><span data-stu-id="0decf-312">Requirement</span></span> | <span data-ttu-id="0decf-313">值</span><span class="sxs-lookup"><span data-stu-id="0decf-313">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0decf-314">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0decf-314">Minimum supported client</span></span><br/> | <span data-ttu-id="0decf-315">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0decf-315">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0decf-316">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0decf-316">Minimum supported server</span></span><br/> | <span data-ttu-id="0decf-317">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0decf-317">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0decf-318">命名空間</span><span class="sxs-lookup"><span data-stu-id="0decf-318">Namespace</span></span><br/>                | <span data-ttu-id="0decf-319">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0decf-319">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0decf-320">MOF</span><span class="sxs-lookup"><span data-stu-id="0decf-320">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0decf-321"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0decf-321"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0decf-322">DLL</span><span class="sxs-lookup"><span data-stu-id="0decf-322">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0decf-323"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0decf-323"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0decf-324">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0decf-324">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0decf-325">**CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="0decf-325">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="0decf-326">[**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0decf-326">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0decf-327">**Msvm \_ ResourcePool (V1)**</span><span class="sxs-lookup"><span data-stu-id="0decf-327">**Msvm\_ResourcePool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourcepool)
</dt> <dt>

[<span data-ttu-id="0decf-328">**Msvm \_ StorageAlert**</span><span class="sxs-lookup"><span data-stu-id="0decf-328">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="0decf-329">資源管理類別</span><span class="sxs-lookup"><span data-stu-id="0decf-329">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

