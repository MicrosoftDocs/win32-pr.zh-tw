---
description: 表示虛擬系統 (NUMA) 節點的非統一記憶體存取。
ms.assetid: a2e9aa74-15e5-4a78-b7f8-ffe2883a31d0
title: Msvm_NumaNode 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NumaNode
- Msvm_NumaNode.RequestStateChange
- Msvm_NumaNode.InstanceID
- Msvm_NumaNode.Caption
- Msvm_NumaNode.Description
- Msvm_NumaNode.ElementName
- Msvm_NumaNode.InstallDate
- Msvm_NumaNode.Name
- Msvm_NumaNode.OperationalStatus
- Msvm_NumaNode.StatusDescriptions
- Msvm_NumaNode.Status
- Msvm_NumaNode.HealthState
- Msvm_NumaNode.CommunicationStatus
- Msvm_NumaNode.DetailedStatus
- Msvm_NumaNode.OperatingStatus
- Msvm_NumaNode.PrimaryStatus
- Msvm_NumaNode.EnabledState
- Msvm_NumaNode.OtherEnabledState
- Msvm_NumaNode.RequestedState
- Msvm_NumaNode.EnabledDefault
- Msvm_NumaNode.TimeOfLastStateChange
- Msvm_NumaNode.AvailableRequestedStates
- Msvm_NumaNode.TransitioningToState
- Msvm_NumaNode.SystemCreationClassName
- Msvm_NumaNode.SystemName
- Msvm_NumaNode.CreationClassName
- Msvm_NumaNode.NodeID
- Msvm_NumaNode.NumberOfProcessorCores
- Msvm_NumaNode.NumberOfLogicalProcessors
- Msvm_NumaNode.CurrentlyConsumableMemoryBlocks
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4bdbd600cd4a78f66376f21ee264b2dfe9854147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995869"
---
# <a name="msvm_numanode-class"></a><span data-ttu-id="a7cac-103">Msvm \_ NumaNode 類別</span><span class="sxs-lookup"><span data-stu-id="a7cac-103">Msvm\_NumaNode class</span></span>

<span data-ttu-id="a7cac-104">表示虛擬系統 (NUMA) 節點的非統一記憶體存取。</span><span class="sxs-lookup"><span data-stu-id="a7cac-104">Represents a Non-Uniform Memory Access (NUMA) node of a virtual system.</span></span>

<span data-ttu-id="a7cac-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a7cac-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7cac-106">語法</span><span class="sxs-lookup"><span data-stu-id="a7cac-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_NumaNode : CIM_EnabledLogicalElement
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
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NodeID;
  uint32   NumberOfProcessorCores;
  uint32   NumberOfLogicalProcessors;
  uint64   CurrentlyConsumableMemoryBlocks;
};
```

## <a name="members"></a><span data-ttu-id="a7cac-107">成員</span><span class="sxs-lookup"><span data-stu-id="a7cac-107">Members</span></span>

<span data-ttu-id="a7cac-108">**Msvm \_ NumaNode** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a7cac-108">The **Msvm\_NumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="a7cac-109">方法</span><span class="sxs-lookup"><span data-stu-id="a7cac-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="a7cac-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a7cac-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a7cac-111">方法</span><span class="sxs-lookup"><span data-stu-id="a7cac-111">Methods</span></span>

<span data-ttu-id="a7cac-112">**Msvm \_ NumaNode** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a7cac-112">The **Msvm\_NumaNode** class has these methods.</span></span>



| <span data-ttu-id="a7cac-113">方法</span><span class="sxs-lookup"><span data-stu-id="a7cac-113">Method</span></span>                 | <span data-ttu-id="a7cac-114">描述</span><span class="sxs-lookup"><span data-stu-id="a7cac-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="a7cac-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="a7cac-115">**RequestStateChange**</span></span> | <span data-ttu-id="a7cac-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="a7cac-116">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a7cac-117">屬性</span><span class="sxs-lookup"><span data-stu-id="a7cac-117">Properties</span></span>

<span data-ttu-id="a7cac-118">**Msvm \_ NumaNode** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a7cac-118">The **Msvm\_NumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7cac-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="a7cac-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-120">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a7cac-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-122">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="a7cac-122">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="a7cac-123">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a7cac-123">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="a7cac-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-127">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="a7cac-127">A short description of the object.</span></span> <span data-ttu-id="a7cac-128">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a7cac-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7cac-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-132">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="a7cac-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a7cac-133">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a7cac-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a7cac-134">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a7cac-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a7cac-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="a7cac-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="a7cac-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="a7cac-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="a7cac-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a7cac-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="a7cac-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a7cac-142">)</span><span class="sxs-lookup"><span data-stu-id="a7cac-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7cac-143">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a7cac-143">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-146">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a7cac-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-147">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="a7cac-147">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-148">**CurrentlyConsumableMemoryBlocks**</span><span class="sxs-lookup"><span data-stu-id="a7cac-148">**CurrentlyConsumableMemoryBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-149">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="a7cac-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-151">虛擬機器目前可用的記憶體區塊數目。</span><span class="sxs-lookup"><span data-stu-id="a7cac-151">The number of memory blocks currently available for consumption by virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-152">**說明**</span><span class="sxs-lookup"><span data-stu-id="a7cac-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-155">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="a7cac-155">A description of the object.</span></span> <span data-ttu-id="a7cac-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a7cac-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-158">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7cac-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-160">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a7cac-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a7cac-161">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a7cac-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a7cac-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a7cac-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="a7cac-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="a7cac-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="a7cac-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="a7cac-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="a7cac-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="a7cac-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a7cac-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="a7cac-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a7cac-171">)</span><span class="sxs-lookup"><span data-stu-id="a7cac-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7cac-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a7cac-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-175">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a7cac-175">A display name for the object.</span></span> <span data-ttu-id="a7cac-176">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-177">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="a7cac-177">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-178">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7cac-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-180">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-180">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="a7cac-181">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a7cac-181">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-182">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="a7cac-182">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-183">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7cac-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-185">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-185">The enabled and disabled states of an element.</span></span> <span data-ttu-id="a7cac-186">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="a7cac-186">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="a7cac-187">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a7cac-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="a7cac-188">值</span><span class="sxs-lookup"><span data-stu-id="a7cac-188">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="a7cac-189">意義</span><span class="sxs-lookup"><span data-stu-id="a7cac-189">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a7cac-190"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-190"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="a7cac-191">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-191">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="a7cac-192"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-192"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="a7cac-193"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-193"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="a7cac-194">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="a7cac-194">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="a7cac-195"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-195"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="a7cac-196">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="a7cac-196">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="a7cac-197">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-197"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="a7cac-198">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="a7cac-198">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="a7cac-199"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="a7cac-200">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="a7cac-200">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="a7cac-201"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="a7cac-202">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="a7cac-202">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="a7cac-203"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="a7cac-203"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="a7cac-204">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-204">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="a7cac-205"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-205"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="a7cac-206">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="a7cac-206">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="a7cac-207"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-207"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="a7cac-208">已啟用元素，但它處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="a7cac-208">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="a7cac-209">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="a7cac-209">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="a7cac-210">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="a7cac-210">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="a7cac-211"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-211"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="a7cac-212">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="a7cac-212">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="a7cac-213">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="a7cac-213">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="a7cac-214">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a7cac-214">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-215">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7cac-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-217">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="a7cac-217">The current health of the element.</span></span> <span data-ttu-id="a7cac-218">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="a7cac-218">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a7cac-219">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="a7cac-219">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a7cac-220">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為5。</span><span class="sxs-lookup"><span data-stu-id="a7cac-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-221">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a7cac-221">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-222">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a7cac-222">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-224">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a7cac-224">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="a7cac-225">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-226">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a7cac-226">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-229">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="a7cac-229">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-230">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a7cac-230">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a7cac-231">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-232">**名稱**</span><span class="sxs-lookup"><span data-stu-id="a7cac-232">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-233">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-235">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="a7cac-235">The label by which the object is known.</span></span> <span data-ttu-id="a7cac-236">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-237">**NodeID**</span><span class="sxs-lookup"><span data-stu-id="a7cac-237">**NodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-238">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-240">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a7cac-240">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-241">NUMA 節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7cac-241">The NUMA node identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-242">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="a7cac-242">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-243">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7cac-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-245">此節點中的邏輯處理器核心總數。</span><span class="sxs-lookup"><span data-stu-id="a7cac-245">The total number of logical processor cores in this node.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-246">**NumberOfProcessorCores**</span><span class="sxs-lookup"><span data-stu-id="a7cac-246">**NumberOfProcessorCores**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-247">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a7cac-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-249">此 NUMA 節點中的處理器核心總數。</span><span class="sxs-lookup"><span data-stu-id="a7cac-249">The total number of processor cores in this NUMA node.</span></span> <span data-ttu-id="a7cac-250">如果每個處理器核心支援多個計算執行緒，這可能會與此節點相關聯的 [**Msvm \_ 處理器**](msvm-processor.md) 物件數目不同。</span><span class="sxs-lookup"><span data-stu-id="a7cac-250">This may differ from the number of [**Msvm\_Processor**](msvm-processor.md) objects associated to this node if each processor core supports multiple compute threads.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-251">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a7cac-251">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-252">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7cac-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-254">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a7cac-254">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a7cac-255">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a7cac-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a7cac-256">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a7cac-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a7cac-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="a7cac-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="a7cac-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="a7cac-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="a7cac-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="a7cac-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="a7cac-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="a7cac-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="a7cac-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="a7cac-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="a7cac-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="a7cac-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="a7cac-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="a7cac-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="a7cac-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="a7cac-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="a7cac-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a7cac-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="a7cac-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a7cac-276">)</span><span class="sxs-lookup"><span data-stu-id="a7cac-276">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7cac-277">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a7cac-277">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-278">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="a7cac-278">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-280">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-280">The current statuses of the object.</span></span> <span data-ttu-id="a7cac-281">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-282">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="a7cac-282">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-283">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-285">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-285">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="a7cac-286">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a7cac-286">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="a7cac-287">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a7cac-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-288">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a7cac-288">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-289">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7cac-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-291">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="a7cac-291">Provides high level status information.</span></span> <span data-ttu-id="a7cac-292">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-292">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="a7cac-293">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="a7cac-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a7cac-294">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a7cac-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="a7cac-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-296"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="a7cac-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="a7cac-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="a7cac-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a7cac-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="a7cac-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="a7cac-301">)</span><span class="sxs-lookup"><span data-stu-id="a7cac-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a7cac-302">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="a7cac-302">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-303">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7cac-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-305">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-305">The last requested or desired state for the element.</span></span> <span data-ttu-id="a7cac-306">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="a7cac-306">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="a7cac-307">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-307">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="a7cac-308">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="a7cac-308">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="a7cac-309">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="a7cac-309">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="a7cac-310">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="a7cac-310">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-311">**狀態**</span><span class="sxs-lookup"><span data-stu-id="a7cac-311">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-312">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-314">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="a7cac-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-315">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a7cac-315">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-316">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a7cac-316">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-318">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="a7cac-318">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a7cac-319">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="a7cac-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-320">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a7cac-320">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-323">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="a7cac-323">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-324">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="a7cac-324">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-325">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a7cac-325">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-326">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a7cac-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-328">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**名稱**") </span><span class="sxs-lookup"><span data-stu-id="a7cac-328">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-329">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7cac-329">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-330">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="a7cac-330">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-331">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="a7cac-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-333">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="a7cac-333">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="a7cac-334">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 "Null"。</span><span class="sxs-lookup"><span data-stu-id="a7cac-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="a7cac-335">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="a7cac-335">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7cac-336">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a7cac-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a7cac-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a7cac-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7cac-338">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="a7cac-338">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="a7cac-339">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a7cac-339">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7cac-340">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7cac-340">Requirements</span></span>



| <span data-ttu-id="a7cac-341">需求</span><span class="sxs-lookup"><span data-stu-id="a7cac-341">Requirement</span></span> | <span data-ttu-id="a7cac-342">值</span><span class="sxs-lookup"><span data-stu-id="a7cac-342">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cac-343">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7cac-343">Minimum supported client</span></span><br/> | <span data-ttu-id="a7cac-344">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7cac-344">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a7cac-345">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7cac-345">Minimum supported server</span></span><br/> | <span data-ttu-id="a7cac-346">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7cac-346">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a7cac-347">命名空間</span><span class="sxs-lookup"><span data-stu-id="a7cac-347">Namespace</span></span><br/>                | <span data-ttu-id="a7cac-348">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a7cac-348">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a7cac-349">MOF</span><span class="sxs-lookup"><span data-stu-id="a7cac-349">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7cac-350"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-350"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7cac-351">DLL</span><span class="sxs-lookup"><span data-stu-id="a7cac-351">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7cac-352"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a7cac-352"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

