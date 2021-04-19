---
description: 描述綜合3-d 的 GPU 服務。
ms.assetid: fe3d6105-3def-453a-ad81-97cd0bb4613f
title: Msvm_Synthetic3DService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService
- Msvm_Synthetic3DService.RequestStateChange
- Msvm_Synthetic3DService.StartService
- Msvm_Synthetic3DService.StopService
- Msvm_Synthetic3DService.InstanceID
- Msvm_Synthetic3DService.Caption
- Msvm_Synthetic3DService.Description
- Msvm_Synthetic3DService.ElementName
- Msvm_Synthetic3DService.InstallDate
- Msvm_Synthetic3DService.OperationalStatus
- Msvm_Synthetic3DService.StatusDescriptions
- Msvm_Synthetic3DService.Status
- Msvm_Synthetic3DService.HealthState
- Msvm_Synthetic3DService.CommunicationStatus
- Msvm_Synthetic3DService.DetailedStatus
- Msvm_Synthetic3DService.OperatingStatus
- Msvm_Synthetic3DService.PrimaryStatus
- Msvm_Synthetic3DService.EnabledState
- Msvm_Synthetic3DService.OtherEnabledState
- Msvm_Synthetic3DService.RequestedState
- Msvm_Synthetic3DService.EnabledDefault
- Msvm_Synthetic3DService.TimeOfLastStateChange
- Msvm_Synthetic3DService.AvailableRequestedStates
- Msvm_Synthetic3DService.TransitioningToState
- Msvm_Synthetic3DService.SystemCreationClassName
- Msvm_Synthetic3DService.SystemName
- Msvm_Synthetic3DService.Name
- Msvm_Synthetic3DService.CreationClassName
- Msvm_Synthetic3DService.PrimaryOwnerName
- Msvm_Synthetic3DService.PrimaryOwnerContact
- Msvm_Synthetic3DService.StartMode
- Msvm_Synthetic3DService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e5bdacb764051f4bee2c9a646a00b09615ee5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982294"
---
# <a name="msvm_synthetic3dservice-class"></a><span data-ttu-id="8e392-103">Msvm \_ Synthetic3DService 類別</span><span class="sxs-lookup"><span data-stu-id="8e392-103">Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="8e392-104">描述綜合3-d 的 GPU 服務。</span><span class="sxs-lookup"><span data-stu-id="8e392-104">Describes the synthetic 3-D GPU service.</span></span>

> [!Note]  
> <span data-ttu-id="8e392-105">第2代虛擬機器無法使用此類別。</span><span class="sxs-lookup"><span data-stu-id="8e392-105">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="8e392-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8e392-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e392-107">語法</span><span class="sxs-lookup"><span data-stu-id="8e392-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Synthetic3D Service";
  string   Description = "Microsoft Synthetic3D Service";
  string   ElementName = "Synthetic3D Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The Synthetic 3D service is fully operational." };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "synth3d";
  string   CreationClassName = "Msvm_Synthetic3DService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="8e392-108">成員</span><span class="sxs-lookup"><span data-stu-id="8e392-108">Members</span></span>

<span data-ttu-id="8e392-109">**Msvm \_ Synthetic3DService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8e392-109">The **Msvm\_Synthetic3DService** class has these types of members:</span></span>

-   [<span data-ttu-id="8e392-110">方法</span><span class="sxs-lookup"><span data-stu-id="8e392-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8e392-111">屬性</span><span class="sxs-lookup"><span data-stu-id="8e392-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8e392-112">方法</span><span class="sxs-lookup"><span data-stu-id="8e392-112">Methods</span></span>

<span data-ttu-id="8e392-113">**Msvm \_ Synthetic3DService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8e392-113">The **Msvm\_Synthetic3DService** class has these methods.</span></span>



| <span data-ttu-id="8e392-114">方法</span><span class="sxs-lookup"><span data-stu-id="8e392-114">Method</span></span>                                                                                     | <span data-ttu-id="8e392-115">描述</span><span class="sxs-lookup"><span data-stu-id="8e392-115">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="8e392-116">**DisableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="8e392-116">**DisableGPUForVirtualization**</span></span>](disablegpuforvirtualization-msvm-synthetic3dservice.md) | <span data-ttu-id="8e392-117">停用實體 GPU 以進行虛擬化。</span><span class="sxs-lookup"><span data-stu-id="8e392-117">Disables a physical GPU for virtualization.</span></span><br/>              |
| [<span data-ttu-id="8e392-118">**EnableGPUForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="8e392-118">**EnableGPUForVirtualization**</span></span>](enablegpuforvirtualization-msvm-synthetic3dservice.md)   | <span data-ttu-id="8e392-119">啟用實體 GPU 以進行虛擬化。</span><span class="sxs-lookup"><span data-stu-id="8e392-119">Enables a physical GPU for virtualization.</span></span><br/>               |
| [<span data-ttu-id="8e392-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="8e392-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-synthetic3dservice.md)             | <span data-ttu-id="8e392-121">修改綜合3-d 服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="8e392-121">Modifies the setting data for the synthetic 3-D service.</span></span><br/> |
| <span data-ttu-id="8e392-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8e392-122">**RequestStateChange**</span></span>                                                                     | <span data-ttu-id="8e392-123">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="8e392-123">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="8e392-124">**StartService**</span><span class="sxs-lookup"><span data-stu-id="8e392-124">**StartService**</span></span>                                                                           | <span data-ttu-id="8e392-125">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="8e392-125">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="8e392-126">**StopService**</span><span class="sxs-lookup"><span data-stu-id="8e392-126">**StopService**</span></span>                                                                            | <span data-ttu-id="8e392-127">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="8e392-127">This method is not supported.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="8e392-128">屬性</span><span class="sxs-lookup"><span data-stu-id="8e392-128">Properties</span></span>

<span data-ttu-id="8e392-129">**Msvm \_ Synthetic3DService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8e392-129">The **Msvm\_Synthetic3DService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e392-130">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8e392-130">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-131">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8e392-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e392-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-133">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="8e392-133">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="8e392-134">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8e392-134">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-135">**標題**</span><span class="sxs-lookup"><span data-stu-id="8e392-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-138">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="8e392-138">A short description of the object.</span></span> <span data-ttu-id="8e392-139">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8e392-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-141">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8e392-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-143">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="8e392-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8e392-144">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="8e392-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8e392-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8e392-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8e392-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="8e392-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="8e392-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="8e392-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="8e392-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8e392-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="8e392-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8e392-153">)</span><span class="sxs-lookup"><span data-stu-id="8e392-153">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8e392-154">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e392-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-157">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e392-157">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8e392-158">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="8e392-158">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-159">**說明**</span><span class="sxs-lookup"><span data-stu-id="8e392-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-162">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8e392-162">A description of the object.</span></span> <span data-ttu-id="8e392-163">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8e392-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8e392-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-167">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e392-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8e392-168">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="8e392-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8e392-169">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8e392-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="8e392-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="8e392-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="8e392-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="8e392-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="8e392-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="8e392-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8e392-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="8e392-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8e392-178">)</span><span class="sxs-lookup"><span data-stu-id="8e392-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8e392-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8e392-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-182">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8e392-182">A display name for the object.</span></span> <span data-ttu-id="8e392-183">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-184">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8e392-184">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-185">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8e392-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-187">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="8e392-187">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8e392-188">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8e392-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-189">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8e392-189">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-192">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="8e392-192">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8e392-193">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="8e392-193">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="8e392-194">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8e392-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8e392-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8e392-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-198">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="8e392-198">The current health of the element.</span></span> <span data-ttu-id="8e392-199">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="8e392-199">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8e392-200">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="8e392-200">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8e392-201">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-201">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e392-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-203">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8e392-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-205">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8e392-205">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="8e392-206">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-207">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8e392-207">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e392-210">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="8e392-210">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8e392-211">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8e392-211">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8e392-212">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8e392-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8e392-213">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8e392-213">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-216">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="8e392-216">The label by which the object is known.</span></span> <span data-ttu-id="8e392-217">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="8e392-217">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-218">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8e392-218">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-219">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8e392-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-221">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e392-221">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8e392-222">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="8e392-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8e392-223">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8e392-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8e392-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="8e392-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="8e392-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="8e392-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="8e392-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="8e392-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="8e392-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="8e392-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="8e392-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="8e392-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="8e392-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="8e392-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="8e392-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="8e392-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="8e392-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="8e392-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="8e392-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8e392-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="8e392-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8e392-243">)</span><span class="sxs-lookup"><span data-stu-id="8e392-243">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8e392-244">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8e392-244">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-245">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8e392-245">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e392-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-247">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8e392-247">The current statuses of the object.</span></span> <span data-ttu-id="8e392-248">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-249">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8e392-249">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-250">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-252">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="8e392-252">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8e392-253">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8e392-253">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8e392-254">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8e392-254">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-255">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="8e392-255">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-256">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-258">值，提供有關如何聯繫服務主要擁有者的資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="8e392-258">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="8e392-259">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="8e392-259">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-260">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="8e392-260">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-263">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="8e392-263">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="8e392-264">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="8e392-264">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="8e392-265">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="8e392-265">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8e392-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-267">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8e392-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-269">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="8e392-269">Provides high level status information.</span></span> <span data-ttu-id="8e392-270">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="8e392-270">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8e392-271">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="8e392-271">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8e392-272">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8e392-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8e392-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-274"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="8e392-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="8e392-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="8e392-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8e392-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8e392-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="8e392-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8e392-279">)</span><span class="sxs-lookup"><span data-stu-id="8e392-279">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8e392-280">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8e392-280">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-281">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8e392-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-283">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="8e392-283">The last requested or desired state for the element.</span></span> <span data-ttu-id="8e392-284">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="8e392-284">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="8e392-285">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e392-285">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="8e392-286">[**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))類別的特定實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="8e392-286">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="8e392-287">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="8e392-287">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="8e392-288">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="8e392-288">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="8e392-289">**已開始**</span><span class="sxs-lookup"><span data-stu-id="8e392-289">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-290">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8e392-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-292">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="8e392-292">Indicates whether the service is currently running.</span></span> <span data-ttu-id="8e392-293">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="8e392-293">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-294">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="8e392-294">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-295">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-297">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="8e392-297">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="8e392-298">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="8e392-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-299">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8e392-299">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-302">元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="8e392-302">The status of the element.</span></span> <span data-ttu-id="8e392-303">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-304">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8e392-304">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-305">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8e392-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8e392-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-307">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="8e392-307">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8e392-308">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="8e392-308">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-309">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e392-309">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-312">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="8e392-312">The scoping system's creation class name.</span></span> <span data-ttu-id="8e392-313">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="8e392-313">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-314">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8e392-314">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-315">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8e392-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-317">主控電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e392-317">The name of the hosting computer system.</span></span> <span data-ttu-id="8e392-318">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="8e392-318">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-319">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8e392-319">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-320">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8e392-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-322">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="8e392-322">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8e392-323">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8e392-323">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8e392-324">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8e392-324">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e392-325">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8e392-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e392-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8e392-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e392-327">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="8e392-327">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8e392-328">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8e392-328">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e392-329">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e392-329">Requirements</span></span>



| <span data-ttu-id="8e392-330">需求</span><span class="sxs-lookup"><span data-stu-id="8e392-330">Requirement</span></span> | <span data-ttu-id="8e392-331">值</span><span class="sxs-lookup"><span data-stu-id="8e392-331">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e392-332">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e392-332">Minimum supported client</span></span><br/> | <span data-ttu-id="8e392-333">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e392-333">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8e392-334">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e392-334">Minimum supported server</span></span><br/> | <span data-ttu-id="8e392-335">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e392-335">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e392-336">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e392-336">Namespace</span></span><br/>                | <span data-ttu-id="8e392-337">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="8e392-337">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8e392-338">MOF</span><span class="sxs-lookup"><span data-stu-id="8e392-338">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e392-339"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8e392-339"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e392-340">DLL</span><span class="sxs-lookup"><span data-stu-id="8e392-340">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e392-341"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e392-341"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

