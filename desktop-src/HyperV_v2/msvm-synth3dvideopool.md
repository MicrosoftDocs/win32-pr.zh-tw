---
description: 包含主機系統上的綜合 3-d video 圖形處理器 (Gpu) 可用的相關資訊。
ms.assetid: 771A42C3-4888-49DF-A389-161A2D0E3DBD
title: Msvm_Synth3dVideoPool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool
- Msvm_Synth3dVideoPool.InstanceID
- Msvm_Synth3dVideoPool.Caption
- Msvm_Synth3dVideoPool.Description
- Msvm_Synth3dVideoPool.ElementName
- Msvm_Synth3dVideoPool.InstallDate
- Msvm_Synth3dVideoPool.Name
- Msvm_Synth3dVideoPool.OperationalStatus
- Msvm_Synth3dVideoPool.StatusDescriptions
- Msvm_Synth3dVideoPool.Status
- Msvm_Synth3dVideoPool.HealthState
- Msvm_Synth3dVideoPool.CommunicationStatus
- Msvm_Synth3dVideoPool.DetailedStatus
- Msvm_Synth3dVideoPool.OperatingStatus
- Msvm_Synth3dVideoPool.PrimaryStatus
- Msvm_Synth3dVideoPool.PoolID
- Msvm_Synth3dVideoPool.Primordial
- Msvm_Synth3dVideoPool.Capacity
- Msvm_Synth3dVideoPool.Reserved
- Msvm_Synth3dVideoPool.ResourceType
- Msvm_Synth3dVideoPool.OtherResourceType
- Msvm_Synth3dVideoPool.ResourceSubType
- Msvm_Synth3dVideoPool.AllocationUnits
- Msvm_Synth3dVideoPool.ConsumedResourceUnits
- Msvm_Synth3dVideoPool.CurrentlyConsumedResource
- Msvm_Synth3dVideoPool.MaxConsumableResource
- Msvm_Synth3dVideoPool.Is3dVideoSupported
- Msvm_Synth3dVideoPool.IsSLATCapable
- Msvm_Synth3dVideoPool.IsGPUCapable
- Msvm_Synth3dVideoPool.DirectXVersion
- Msvm_Synth3dVideoPool.RequiredMinimumDirectXVersion
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1afad0f1b2e80a747bb518cb3eafc75d494de62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943895"
---
# <a name="msvm_synth3dvideopool-class"></a><span data-ttu-id="8da9b-103">Msvm \_ Synth3dVideoPool 類別</span><span class="sxs-lookup"><span data-stu-id="8da9b-103">Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="8da9b-104">包含主機系統上的綜合 3-d video 圖形處理器 (Gpu) 可用的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8da9b-104">Contains information about the synthetic 3-D video graphics processing units (GPUs) available on the host system.</span></span> <span data-ttu-id="8da9b-105">這個類別只會與支援 RemoteFX 的主機系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8da9b-105">This class is only used with host systems that support RemoteFX.</span></span>

<span data-ttu-id="8da9b-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8da9b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da9b-107">語法</span><span class="sxs-lookup"><span data-stu-id="8da9b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synth3dVideoPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption = "3D Display Controller Resource Pool";
  string   Description = "Resource pool used to allocate synthetic 3D video controller resources to a virtual machine.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID;
  boolean  Primordial = True;
  uint64   Capacity;
  uint64   Reserved = 0;
  uint16   ResourceType;
  string   OtherResourceType;
  string   ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string   AllocationUnits = "count";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
  boolean  Is3dVideoSupported;
  boolean  IsSLATCapable;
  boolean  IsGPUCapable;
  string   DirectXVersion;
  string   RequiredMinimumDirectXVersion;
};
```

## <a name="members"></a><span data-ttu-id="8da9b-108">成員</span><span class="sxs-lookup"><span data-stu-id="8da9b-108">Members</span></span>

<span data-ttu-id="8da9b-109">**Msvm \_ Synth3dVideoPool** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8da9b-109">The **Msvm\_Synth3dVideoPool** class has these types of members:</span></span>

-   [<span data-ttu-id="8da9b-110">方法</span><span class="sxs-lookup"><span data-stu-id="8da9b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8da9b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8da9b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8da9b-112">方法</span><span class="sxs-lookup"><span data-stu-id="8da9b-112">Methods</span></span>

<span data-ttu-id="8da9b-113">**Msvm \_ Synth3dVideoPool** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8da9b-113">The **Msvm\_Synth3dVideoPool** class has these methods.</span></span>



| <span data-ttu-id="8da9b-114">方法</span><span class="sxs-lookup"><span data-stu-id="8da9b-114">Method</span></span>                                                                                             | <span data-ttu-id="8da9b-115">描述</span><span class="sxs-lookup"><span data-stu-id="8da9b-115">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8da9b-116">**CalculateVideoMemoryRequirements**</span><span class="sxs-lookup"><span data-stu-id="8da9b-116">**CalculateVideoMemoryRequirements**</span></span>](msvm-synth3dvideopool-calculatevideomemoryrequirements.md) | <span data-ttu-id="8da9b-117">計算 RemoteFX 虛擬機器所需的視訊記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="8da9b-117">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8da9b-118">屬性</span><span class="sxs-lookup"><span data-stu-id="8da9b-118">Properties</span></span>

<span data-ttu-id="8da9b-119">**Msvm \_ Synth3dVideoPool** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8da9b-119">The **Msvm\_Synth3dVideoPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8da9b-120">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="8da9b-120">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-123">資源集區所使用的配置單位。</span><span class="sxs-lookup"><span data-stu-id="8da9b-123">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="8da9b-124">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8da9b-124">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-125">**容量**</span><span class="sxs-lookup"><span data-stu-id="8da9b-125">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8da9b-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-128">資源集區可支援的有效保留 (的最大數量單位為 **AllocationUnits**) 。</span><span class="sxs-lookup"><span data-stu-id="8da9b-128">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="8da9b-129">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8da9b-129">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-130">**標題**</span><span class="sxs-lookup"><span data-stu-id="8da9b-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-133">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="8da9b-133">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-134">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="8da9b-134">A short description of the object.</span></span> <span data-ttu-id="8da9b-135">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8da9b-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-137">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8da9b-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-139">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="8da9b-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8da9b-140">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="8da9b-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8da9b-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8da9b-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8da9b-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="8da9b-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="8da9b-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="8da9b-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="8da9b-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8da9b-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="8da9b-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8da9b-149">)</span><span class="sxs-lookup"><span data-stu-id="8da9b-149">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8da9b-150">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="8da9b-150">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-153">指定 **MaxConsumableResource** 和 **CurrentlyConsumedResource** 屬性的單位。</span><span class="sxs-lookup"><span data-stu-id="8da9b-153">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="8da9b-154">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8da9b-154">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-155">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="8da9b-155">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-156">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8da9b-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-158">指定資源集區目前向取用者呈現的資源數量。</span><span class="sxs-lookup"><span data-stu-id="8da9b-158">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="8da9b-159">這個屬性與 **保留** 的屬性不同，因為它會描述資源的取用者觀點，而 **保留** 的屬性則會描述資源的產生者觀點。</span><span class="sxs-lookup"><span data-stu-id="8da9b-159">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="8da9b-160">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8da9b-160">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-161">**說明**</span><span class="sxs-lookup"><span data-stu-id="8da9b-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-164">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8da9b-164">A description of the object.</span></span> <span data-ttu-id="8da9b-165">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8da9b-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8da9b-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-169">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8da9b-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8da9b-170">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="8da9b-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8da9b-171">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8da9b-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="8da9b-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="8da9b-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="8da9b-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="8da9b-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="8da9b-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="8da9b-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8da9b-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="8da9b-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8da9b-180">)</span><span class="sxs-lookup"><span data-stu-id="8da9b-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8da9b-181">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="8da9b-181">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-184">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="8da9b-184">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-185">指定資源集區中的卡片所支援的最低 DirectX 版本。</span><span class="sxs-lookup"><span data-stu-id="8da9b-185">Specifies the lowest version of DirectX that is supported by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8da9b-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-187">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-189">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8da9b-189">A display name for the object.</span></span> <span data-ttu-id="8da9b-190">除了索引鍵屬性、身分識別資料和描述資訊之外，此屬性還可讓每個實例定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8da9b-190">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="8da9b-191">**CIM \_ ManagedSystemElement** 類別的 [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)屬性也會定義為顯示名稱，但通常是子類別化的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="8da9b-191">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name, but it is often subclassed to be a Key.</span></span> <span data-ttu-id="8da9b-192">相同的屬性可以同時傳達身分識別和顯示名稱，而不會有不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="8da9b-192">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="8da9b-193">如果 [**名稱**](msvm-keyboard.md) 存在，而且不是索引鍵 (例如針對 LogicalDevice) 的實例，則 **名稱** 和 **ElementName** 屬性都可以同時存在相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="8da9b-193">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="8da9b-194">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8da9b-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8da9b-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-198">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="8da9b-198">The current health of the element.</span></span> <span data-ttu-id="8da9b-199">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="8da9b-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8da9b-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-201">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8da9b-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-203">建立虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8da9b-203">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="8da9b-204">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-205">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8da9b-205">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-208">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="8da9b-208">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-209">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8da9b-209">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8da9b-210">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-211">**Is3dVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="8da9b-211">**Is3dVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-212">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8da9b-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-214">指定主機系統是否支援3-d 影片。</span><span class="sxs-lookup"><span data-stu-id="8da9b-214">Specifies whether 3-D video is supported by the host system.</span></span> <span data-ttu-id="8da9b-215">如果支援3-d 影片，則包含非零值，否則為零。</span><span class="sxs-lookup"><span data-stu-id="8da9b-215">Contains a nonzero value if 3-D video is supported, or zero otherwise.</span></span> <span data-ttu-id="8da9b-216">為了支援3-d 影片，RemoteFX 主機必須有第二層位址轉譯 (SLAT) 功能，而且至少有一個支援 RemoteFX 的實體 GPU。</span><span class="sxs-lookup"><span data-stu-id="8da9b-216">To support 3-D video, the RemoteFX host must have second level address translation (SLAT) capabilities and have at least one physical GPU that supports RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-217">**IsGPUCapable**</span><span class="sxs-lookup"><span data-stu-id="8da9b-217">**IsGPUCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-218">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8da9b-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-220">指定主機是否有支援 RemoteFX 的 Gpu，以及其 DirectX 版本是否符合最低需求。</span><span class="sxs-lookup"><span data-stu-id="8da9b-220">Specifies whether the host has GPUs that support RemoteFX and whether their DirectX versions meet the minimum requirement.</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-221">**IsSLATCapable**</span><span class="sxs-lookup"><span data-stu-id="8da9b-221">**IsSLATCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-222">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8da9b-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-224">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) </span><span class="sxs-lookup"><span data-stu-id="8da9b-224">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-225">指定主機是否有第二層位址轉譯 (SLAT) 可支援的 CPU。</span><span class="sxs-lookup"><span data-stu-id="8da9b-225">Specifies whether the host has a second level address translation (SLAT) capable CPU.</span></span>

> [!Note]  
> <span data-ttu-id="8da9b-226">已在 Windows 10、1703版和 Windows Server 2016 中淘汰。</span><span class="sxs-lookup"><span data-stu-id="8da9b-226">Deprecated in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="8da9b-227">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="8da9b-227">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-228">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8da9b-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-230">指定資源集區可向取用者呈現的可耗用資源數量上限。</span><span class="sxs-lookup"><span data-stu-id="8da9b-230">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="8da9b-231">這個屬性與 [ **容量** ] 屬性不同的是，它會描述資源的取用者觀點，而 [ **容量** ] 屬性則是描述資源的生產者視圖。</span><span class="sxs-lookup"><span data-stu-id="8da9b-231">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="8da9b-232">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8da9b-232">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-233">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8da9b-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-236">限定詞： **MaxLen** (1024) </span><span class="sxs-lookup"><span data-stu-id="8da9b-236">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-237">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="8da9b-237">The label by which the object is known.</span></span> <span data-ttu-id="8da9b-238">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="8da9b-238">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="8da9b-239">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-240">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8da9b-240">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-241">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8da9b-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-243">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8da9b-243">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8da9b-244">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="8da9b-244">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8da9b-245">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8da9b-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8da9b-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="8da9b-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="8da9b-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="8da9b-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="8da9b-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="8da9b-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="8da9b-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="8da9b-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="8da9b-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="8da9b-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="8da9b-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="8da9b-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="8da9b-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="8da9b-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="8da9b-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="8da9b-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="8da9b-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8da9b-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="8da9b-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8da9b-265">)</span><span class="sxs-lookup"><span data-stu-id="8da9b-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8da9b-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8da9b-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-267">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8da9b-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-269">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8da9b-269">The current status of the element.</span></span> <span data-ttu-id="8da9b-270">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="8da9b-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span> <span data-ttu-id="8da9b-271">Hyper-v 只會使用這個陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="8da9b-271">Hyper-V will only ever use the first element of this array.</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-272">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="8da9b-272">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-275">描述資源類型的字串，當無法使用定義完善的值，並將 [**ResourceType**](msvm-processorpool.md) 設定為 0 ( "Other" ) 。</span><span class="sxs-lookup"><span data-stu-id="8da9b-275">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="8da9b-276">這個屬性會繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8da9b-276">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-277">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="8da9b-277">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-280">從這個集區配置的 [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) 實例會參考此值。</span><span class="sxs-lookup"><span data-stu-id="8da9b-280">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="8da9b-281">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，而且一律設定為 "Microsoft：*GUID* \\ Root"。</span><span class="sxs-lookup"><span data-stu-id="8da9b-281">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-282">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8da9b-282">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8da9b-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-285">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="8da9b-285">Provides high level status information.</span></span> <span data-ttu-id="8da9b-286">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="8da9b-286">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8da9b-287">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="8da9b-287">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8da9b-288">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8da9b-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8da9b-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8da9b-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-290"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="8da9b-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="8da9b-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="8da9b-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8da9b-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="8da9b-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8da9b-295">)</span><span class="sxs-lookup"><span data-stu-id="8da9b-295">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8da9b-296">**原始**</span><span class="sxs-lookup"><span data-stu-id="8da9b-296">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-297">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8da9b-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-299">如果此資源集區是資源管理活動中用來繪製和傳回資源的基礎，則為 **True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="8da9b-299">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="8da9b-300">原始的意思是，此模型的取用者無法建立或刪除此資源集區。</span><span class="sxs-lookup"><span data-stu-id="8da9b-300">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="8da9b-301">不過，其他執行模型化的動作可能會影響原始資源集區的特性或大小。</span><span class="sxs-lookup"><span data-stu-id="8da9b-301">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="8da9b-302">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8da9b-302">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-303">**RequiredMinimumDirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="8da9b-303">**RequiredMinimumDirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-304">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-306">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="8da9b-306">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-307">指定資源集區中卡片所需的最低 DirectX 版本。</span><span class="sxs-lookup"><span data-stu-id="8da9b-307">Specifies the lowest version of DirectX that is required by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-308">**已保留**</span><span class="sxs-lookup"><span data-stu-id="8da9b-308">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-309">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8da9b-309">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-311">目前的保留 (單位為 **AllocationUnits**) 分散到此集區的所有作用中配置。</span><span class="sxs-lookup"><span data-stu-id="8da9b-311">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="8da9b-312">在階層式設定中，這代表所有子系資源集區目前保留的總和。</span><span class="sxs-lookup"><span data-stu-id="8da9b-312">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="8da9b-313">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8da9b-313">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-314">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="8da9b-314">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-315">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-317">描述此集區之特定執行子類型的字串。</span><span class="sxs-lookup"><span data-stu-id="8da9b-317">A string that describes an implementation specific subtype for this pool.</span></span> <span data-ttu-id="8da9b-318">例如，這可用來區分相同資源類型的不同模型。</span><span class="sxs-lookup"><span data-stu-id="8da9b-318">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="8da9b-319">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8da9b-319">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-320">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="8da9b-320">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-321">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8da9b-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-323">此資源集區可以配置的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8da9b-323">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="8da9b-324">這個屬性繼承自 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))，而且一律設定為 4 ( 「記憶體」 ) 。</span><span class="sxs-lookup"><span data-stu-id="8da9b-324">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-325">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8da9b-325">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-326">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8da9b-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-328">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="8da9b-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8da9b-329">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8da9b-329">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8da9b-330">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8da9b-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8da9b-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8da9b-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8da9b-332">描述各種 [**OperationalStatus**](msvm-bioselement.md) 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="8da9b-332">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="8da9b-333">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="8da9b-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span> <span data-ttu-id="8da9b-334">Hyper-v 只會使用這個陣列的第一個元素。</span><span class="sxs-lookup"><span data-stu-id="8da9b-334">Hyper-V will only ever use the first element of this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8da9b-335">規格需求</span><span class="sxs-lookup"><span data-stu-id="8da9b-335">Requirements</span></span>



| <span data-ttu-id="8da9b-336">需求</span><span class="sxs-lookup"><span data-stu-id="8da9b-336">Requirement</span></span> | <span data-ttu-id="8da9b-337">值</span><span class="sxs-lookup"><span data-stu-id="8da9b-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8da9b-338">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8da9b-338">Minimum supported client</span></span><br/> | <span data-ttu-id="8da9b-339">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8da9b-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8da9b-340">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8da9b-340">Minimum supported server</span></span><br/> | <span data-ttu-id="8da9b-341">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8da9b-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8da9b-342">命名空間</span><span class="sxs-lookup"><span data-stu-id="8da9b-342">Namespace</span></span><br/>                | <span data-ttu-id="8da9b-343">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="8da9b-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8da9b-344">MOF</span><span class="sxs-lookup"><span data-stu-id="8da9b-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8da9b-345"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8da9b-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8da9b-346">DLL</span><span class="sxs-lookup"><span data-stu-id="8da9b-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8da9b-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8da9b-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8da9b-348">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8da9b-348">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da9b-349">**CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="8da9b-349">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> </dl>

 

