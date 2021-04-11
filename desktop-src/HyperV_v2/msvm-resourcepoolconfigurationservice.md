---
description: 提供資源集區的主動管理。
ms.assetid: 34ee3189-cb89-4d36-b12f-333449103968
title: Msvm_ResourcePoolConfigurationService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService
- Msvm_ResourcePoolConfigurationService.RequestStateChange
- Msvm_ResourcePoolConfigurationService.StartService
- Msvm_ResourcePoolConfigurationService.StopService
- Msvm_ResourcePoolConfigurationService.InstanceID
- Msvm_ResourcePoolConfigurationService.Caption
- Msvm_ResourcePoolConfigurationService.Description
- Msvm_ResourcePoolConfigurationService.ElementName
- Msvm_ResourcePoolConfigurationService.InstallDate
- Msvm_ResourcePoolConfigurationService.Name
- Msvm_ResourcePoolConfigurationService.OperationalStatus
- Msvm_ResourcePoolConfigurationService.StatusDescriptions
- Msvm_ResourcePoolConfigurationService.Status
- Msvm_ResourcePoolConfigurationService.HealthState
- Msvm_ResourcePoolConfigurationService.CommunicationStatus
- Msvm_ResourcePoolConfigurationService.DetailedStatus
- Msvm_ResourcePoolConfigurationService.OperatingStatus
- Msvm_ResourcePoolConfigurationService.PrimaryStatus
- Msvm_ResourcePoolConfigurationService.EnabledState
- Msvm_ResourcePoolConfigurationService.OtherEnabledState
- Msvm_ResourcePoolConfigurationService.RequestedState
- Msvm_ResourcePoolConfigurationService.EnabledDefault
- Msvm_ResourcePoolConfigurationService.TimeOfLastStateChange
- Msvm_ResourcePoolConfigurationService.AvailableRequestedStates
- Msvm_ResourcePoolConfigurationService.TransitioningToState
- Msvm_ResourcePoolConfigurationService.SystemCreationClassName
- Msvm_ResourcePoolConfigurationService.SystemName
- Msvm_ResourcePoolConfigurationService.CreationClassName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerContact
- Msvm_ResourcePoolConfigurationService.StartMode
- Msvm_ResourcePoolConfigurationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3160e8ac9ba011db70a5d7118e4d1f72733ff23f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852375"
---
# <a name="msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="186f6-103">Msvm \_ ResourcePoolConfigurationService 類別</span><span class="sxs-lookup"><span data-stu-id="186f6-103">Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="186f6-104">提供資源集區的主動管理。</span><span class="sxs-lookup"><span data-stu-id="186f6-104">Provides for active management of resource pools.</span></span>

<span data-ttu-id="186f6-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="186f6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="186f6-106">語法</span><span class="sxs-lookup"><span data-stu-id="186f6-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationService : CIM_Service
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="186f6-107">成員</span><span class="sxs-lookup"><span data-stu-id="186f6-107">Members</span></span>

<span data-ttu-id="186f6-108">**Msvm \_ ResourcePoolConfigurationService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="186f6-108">The **Msvm\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="186f6-109">方法</span><span class="sxs-lookup"><span data-stu-id="186f6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="186f6-110">屬性</span><span class="sxs-lookup"><span data-stu-id="186f6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="186f6-111">方法</span><span class="sxs-lookup"><span data-stu-id="186f6-111">Methods</span></span>

<span data-ttu-id="186f6-112">**Msvm \_ ResourcePoolConfigurationService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="186f6-112">The **Msvm\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="186f6-113">方法</span><span class="sxs-lookup"><span data-stu-id="186f6-113">Method</span></span>                                                                                   | <span data-ttu-id="186f6-114">描述</span><span class="sxs-lookup"><span data-stu-id="186f6-114">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="186f6-115">**>batchclient.pooloperations.createpool**</span><span class="sxs-lookup"><span data-stu-id="186f6-115">**CreatePool**</span></span>](createpool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="186f6-116">建立子資源集區。</span><span class="sxs-lookup"><span data-stu-id="186f6-116">Creates a child resource pool.</span></span><br/>                                                    |
| [<span data-ttu-id="186f6-117">**DeletePool**</span><span class="sxs-lookup"><span data-stu-id="186f6-117">**DeletePool**</span></span>](deletepool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="186f6-118">刪除資源集區。</span><span class="sxs-lookup"><span data-stu-id="186f6-118">Deletes a resource pool.</span></span><br/>                                                          |
| [<span data-ttu-id="186f6-119">**ModifyPoolResources**</span><span class="sxs-lookup"><span data-stu-id="186f6-119">**ModifyPoolResources**</span></span>](modifypoolresources-msvm-resourcepoolconfigurationservice.md) | <span data-ttu-id="186f6-120">變更指派給子集區之資源的父集區資源設定。</span><span class="sxs-lookup"><span data-stu-id="186f6-120">Changes the parent pool resource settings for resources assigned to a child pool.</span></span><br/> |
| [<span data-ttu-id="186f6-121">**ModifyPoolSettings**</span><span class="sxs-lookup"><span data-stu-id="186f6-121">**ModifyPoolSettings**</span></span>](modifypoolsettings-msvm-resourcepoolconfigurationservice.md)   | <span data-ttu-id="186f6-122">變更非配置相關的子集區設定。</span><span class="sxs-lookup"><span data-stu-id="186f6-122">Changes the settings of a child pool that are not allocation related.</span></span><br/>             |
| <span data-ttu-id="186f6-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="186f6-123">**RequestStateChange**</span></span>                                                                   | <span data-ttu-id="186f6-124">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="186f6-124">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="186f6-125">**StartService**</span><span class="sxs-lookup"><span data-stu-id="186f6-125">**StartService**</span></span>                                                                         | <span data-ttu-id="186f6-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="186f6-126">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="186f6-127">**StopService**</span><span class="sxs-lookup"><span data-stu-id="186f6-127">**StopService**</span></span>                                                                          | <span data-ttu-id="186f6-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="186f6-128">This method is not supported.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="186f6-129">屬性</span><span class="sxs-lookup"><span data-stu-id="186f6-129">Properties</span></span>

<span data-ttu-id="186f6-130">**Msvm \_ ResourcePoolConfigurationService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="186f6-130">The **Msvm\_ResourcePoolConfigurationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="186f6-131">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="186f6-131">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-132">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="186f6-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="186f6-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-134">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="186f6-134">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="186f6-135">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="186f6-135">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="186f6-136">**標題**</span><span class="sxs-lookup"><span data-stu-id="186f6-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-139">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="186f6-139">A short description of the object.</span></span> <span data-ttu-id="186f6-140">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-141">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="186f6-141">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-142">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="186f6-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-144">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="186f6-144">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="186f6-145">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="186f6-145">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="186f6-146">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-146">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="186f6-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="186f6-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="186f6-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="186f6-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="186f6-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="186f6-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="186f6-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="186f6-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="186f6-154">)</span><span class="sxs-lookup"><span data-stu-id="186f6-154">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="186f6-155">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="186f6-155">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186f6-158">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="186f6-158">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="186f6-159">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="186f6-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="186f6-160">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="186f6-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-161">**說明**</span><span class="sxs-lookup"><span data-stu-id="186f6-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-164">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="186f6-164">A description of the object.</span></span> <span data-ttu-id="186f6-165">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="186f6-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="186f6-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-169">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="186f6-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="186f6-170">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="186f6-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="186f6-171">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="186f6-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="186f6-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="186f6-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="186f6-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="186f6-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="186f6-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="186f6-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="186f6-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="186f6-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="186f6-180">)</span><span class="sxs-lookup"><span data-stu-id="186f6-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="186f6-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="186f6-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-184">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="186f6-184">A display name for the object.</span></span> <span data-ttu-id="186f6-185">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="186f6-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="186f6-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-189">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="186f6-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="186f6-190">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="186f6-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="186f6-191">值</span><span class="sxs-lookup"><span data-stu-id="186f6-191">Value</span></span>                                                                        | <span data-ttu-id="186f6-192">意義</span><span class="sxs-lookup"><span data-stu-id="186f6-192">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="186f6-193"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="186f6-193"><dt>2</dt></span></span> </dl> | <span data-ttu-id="186f6-194">已啟用</span><span class="sxs-lookup"><span data-stu-id="186f6-194">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="186f6-195">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="186f6-195">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="186f6-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-198">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="186f6-198">The enabled and disabled states of an element.</span></span> <span data-ttu-id="186f6-199">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="186f6-199">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="186f6-200">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="186f6-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="186f6-201">值</span><span class="sxs-lookup"><span data-stu-id="186f6-201">Value</span></span>                                                                        | <span data-ttu-id="186f6-202">意義</span><span class="sxs-lookup"><span data-stu-id="186f6-202">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="186f6-203"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="186f6-203"><dt>2</dt></span></span> </dl> | <span data-ttu-id="186f6-204">已啟用</span><span class="sxs-lookup"><span data-stu-id="186f6-204">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="186f6-205">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="186f6-205">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-206">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="186f6-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-208">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="186f6-208">The current health of the element.</span></span> <span data-ttu-id="186f6-209">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="186f6-209">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="186f6-210">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="186f6-210">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="186f6-211">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="186f6-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-213">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="186f6-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-215">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="186f6-215">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="186f6-216">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-217">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="186f6-217">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186f6-220">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="186f6-220">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="186f6-221">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="186f6-221">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="186f6-222">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-223">**名稱**</span><span class="sxs-lookup"><span data-stu-id="186f6-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186f6-226">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="186f6-226">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="186f6-227">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="186f6-227">The label by which the object is known.</span></span> <span data-ttu-id="186f6-228">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="186f6-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-230">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="186f6-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-232">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="186f6-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="186f6-233">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="186f6-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="186f6-234">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="186f6-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="186f6-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="186f6-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="186f6-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="186f6-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="186f6-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="186f6-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="186f6-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="186f6-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="186f6-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="186f6-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="186f6-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="186f6-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="186f6-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="186f6-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="186f6-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="186f6-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="186f6-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="186f6-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="186f6-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="186f6-254">)</span><span class="sxs-lookup"><span data-stu-id="186f6-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="186f6-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="186f6-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-256">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="186f6-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="186f6-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-258">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="186f6-258">The current statuses of the object.</span></span> <span data-ttu-id="186f6-259">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="186f6-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-263">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="186f6-263">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="186f6-264">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="186f6-264">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="186f6-265">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="186f6-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="186f6-266">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="186f6-266">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186f6-269">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="186f6-269">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="186f6-270">有關如何聯繫服務主要擁有者的任何資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="186f6-270">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="186f6-271">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="186f6-271">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="186f6-272">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="186f6-272">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186f6-275">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="186f6-275">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="186f6-276">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="186f6-276">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="186f6-277">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="186f6-277">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="186f6-278">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="186f6-278">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="186f6-279">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="186f6-279">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-280">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="186f6-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-282">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="186f6-282">Provides high level status information.</span></span> <span data-ttu-id="186f6-283">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="186f6-283">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="186f6-284">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="186f6-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="186f6-285">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="186f6-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="186f6-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-287"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="186f6-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="186f6-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="186f6-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="186f6-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="186f6-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="186f6-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="186f6-292">)</span><span class="sxs-lookup"><span data-stu-id="186f6-292">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="186f6-293">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="186f6-293">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-294">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="186f6-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-296">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="186f6-296">The last requested or desired state for the element.</span></span> <span data-ttu-id="186f6-297">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="186f6-297">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="186f6-298">系統會提供這個屬性來比較專案的最後一個要求和目前狀態。</span><span class="sxs-lookup"><span data-stu-id="186f6-298">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="186f6-299">[**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))類別的特定實例可能不支援 **RequestedState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="186f6-299">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="186f6-300">如果發生這種情況，則會使用值 12 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="186f6-300">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="186f6-301">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="186f6-301">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="186f6-302">值</span><span class="sxs-lookup"><span data-stu-id="186f6-302">Value</span></span>                                                                         | <span data-ttu-id="186f6-303">意義</span><span class="sxs-lookup"><span data-stu-id="186f6-303">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="186f6-304"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="186f6-304"><dt>12</dt></span></span> </dl> | <span data-ttu-id="186f6-305">不適用。</span><span class="sxs-lookup"><span data-stu-id="186f6-305">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="186f6-306">**已開始**</span><span class="sxs-lookup"><span data-stu-id="186f6-306">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-307">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="186f6-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-309">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="186f6-309">Indicates whether the service is currently running.</span></span> <span data-ttu-id="186f6-310">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="186f6-310">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-311">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="186f6-311">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-312">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186f6-314">限定詞： **MaxLen** ( 10 ) </span><span class="sxs-lookup"><span data-stu-id="186f6-314">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="186f6-315">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="186f6-315">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="186f6-316">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="186f6-316">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="186f6-317">**狀態**</span><span class="sxs-lookup"><span data-stu-id="186f6-317">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-318">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-320">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="186f6-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="186f6-321">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="186f6-321">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-322">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="186f6-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="186f6-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-324">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="186f6-324">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="186f6-325">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="186f6-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-326">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="186f6-326">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-327">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186f6-329">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="186f6-329">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="186f6-330">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="186f6-330">The scoping system's creation class name.</span></span> <span data-ttu-id="186f6-331">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="186f6-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-332">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="186f6-332">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="186f6-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="186f6-335">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="186f6-335">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="186f6-336">主控電腦系統的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="186f6-336">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="186f6-337">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="186f6-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-338">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="186f6-338">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-339">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="186f6-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-341">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="186f6-341">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="186f6-342">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="186f6-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="186f6-343">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="186f6-343">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="186f6-344">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="186f6-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="186f6-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="186f6-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="186f6-346">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="186f6-346">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="186f6-347">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="186f6-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="186f6-348">規格需求</span><span class="sxs-lookup"><span data-stu-id="186f6-348">Requirements</span></span>



| <span data-ttu-id="186f6-349">需求</span><span class="sxs-lookup"><span data-stu-id="186f6-349">Requirement</span></span> | <span data-ttu-id="186f6-350">值</span><span class="sxs-lookup"><span data-stu-id="186f6-350">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="186f6-351">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="186f6-351">Minimum supported client</span></span><br/> | <span data-ttu-id="186f6-352">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="186f6-352">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="186f6-353">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="186f6-353">Minimum supported server</span></span><br/> | <span data-ttu-id="186f6-354">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="186f6-354">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="186f6-355">命名空間</span><span class="sxs-lookup"><span data-stu-id="186f6-355">Namespace</span></span><br/>                | <span data-ttu-id="186f6-356">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="186f6-356">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="186f6-357">MOF</span><span class="sxs-lookup"><span data-stu-id="186f6-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="186f6-358"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="186f6-358"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="186f6-359">DLL</span><span class="sxs-lookup"><span data-stu-id="186f6-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="186f6-360"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="186f6-360"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

