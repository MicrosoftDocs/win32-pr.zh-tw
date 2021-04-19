---
description: 管理特定主機的所有遠端終端機連接。
ms.assetid: 7eacb8a6-cb8d-4a2a-951e-f5286cf484e7
title: Msvm_TerminalService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService
- Msvm_TerminalService.InstanceID
- Msvm_TerminalService.Caption
- Msvm_TerminalService.Description
- Msvm_TerminalService.ElementName
- Msvm_TerminalService.InstallDate
- Msvm_TerminalService.OperationalStatus
- Msvm_TerminalService.StatusDescriptions
- Msvm_TerminalService.Status
- Msvm_TerminalService.HealthState
- Msvm_TerminalService.CommunicationStatus
- Msvm_TerminalService.DetailedStatus
- Msvm_TerminalService.OperatingStatus
- Msvm_TerminalService.PrimaryStatus
- Msvm_TerminalService.EnabledState
- Msvm_TerminalService.OtherEnabledState
- Msvm_TerminalService.RequestedState
- Msvm_TerminalService.EnabledDefault
- Msvm_TerminalService.TimeOfLastStateChange
- Msvm_TerminalService.AvailableRequestedStates
- Msvm_TerminalService.TransitioningToState
- Msvm_TerminalService.SystemCreationClassName
- Msvm_TerminalService.SystemName
- Msvm_TerminalService.Name
- Msvm_TerminalService.CreationClassName
- Msvm_TerminalService.PrimaryOwnerName
- Msvm_TerminalService.PrimaryOwnerContact
- Msvm_TerminalService.StartMode
- Msvm_TerminalService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76b12bb49391909638d20df817a3693938c3222c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969230"
---
# <a name="msvm_terminalservice-class"></a><span data-ttu-id="ee08f-103">Msvm \_ TerminalService 類別</span><span class="sxs-lookup"><span data-stu-id="ee08f-103">Msvm\_TerminalService class</span></span>

<span data-ttu-id="ee08f-104">管理特定主機的所有遠端終端機連接。</span><span class="sxs-lookup"><span data-stu-id="ee08f-104">Manages all remote terminal connections to a particular host.</span></span> <span data-ttu-id="ee08f-105">服務會使用可設定的埠來起始所有的終端機連接。</span><span class="sxs-lookup"><span data-stu-id="ee08f-105">The service uses a configurable port to initiate all terminal connections.</span></span>

<span data-ttu-id="ee08f-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ee08f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee08f-107">語法</span><span class="sxs-lookup"><span data-stu-id="ee08f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Terminal Service";
  string   Description = "Microsoft Virtual Terminal Service";
  string   ElementName = "Hyper-V Terminal Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The virtual terminal connection management service is fully operational" };
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
  string   Name = "termsvc";
  string   CreationClassName = "Msvm_TerminalService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="ee08f-108">成員</span><span class="sxs-lookup"><span data-stu-id="ee08f-108">Members</span></span>

<span data-ttu-id="ee08f-109">**Msvm \_ TerminalService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ee08f-109">The **Msvm\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="ee08f-110">方法</span><span class="sxs-lookup"><span data-stu-id="ee08f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ee08f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ee08f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ee08f-112">方法</span><span class="sxs-lookup"><span data-stu-id="ee08f-112">Methods</span></span>

<span data-ttu-id="ee08f-113">**Msvm \_ TerminalService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ee08f-113">The **Msvm\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="ee08f-114">方法</span><span class="sxs-lookup"><span data-stu-id="ee08f-114">Method</span></span>                                                                                        | <span data-ttu-id="ee08f-115">描述</span><span class="sxs-lookup"><span data-stu-id="ee08f-115">Description</span></span>                                                                                                      |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee08f-116">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="ee08f-116">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)             | <span data-ttu-id="ee08f-117">抓取目前的 DACL，以控制對虛擬機器的互動式會話的存取。</span><span class="sxs-lookup"><span data-stu-id="ee08f-117">Retrieves the current DACL that controls access to the interactive session of a virtual machine.</span></span><br/>      |
| [<span data-ttu-id="ee08f-118">**GrantInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="ee08f-118">**GrantInteractiveSessionAccess**</span></span>](grantinteractivesessionaccess-msvm-terminalservice.md)   | <span data-ttu-id="ee08f-119">將虛擬機器的互動式會話存取權授與指定的受信者清單。</span><span class="sxs-lookup"><span data-stu-id="ee08f-119">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span><br/>    |
| [<span data-ttu-id="ee08f-120">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="ee08f-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-terminalservice.md)                   | <span data-ttu-id="ee08f-121">修改服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="ee08f-121">Modifies the setting data for the service.</span></span><br/>                                                            |
| [<span data-ttu-id="ee08f-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ee08f-122">**RequestStateChange**</span></span>](msvm-terminalservice-requeststatechange.md)                         | <span data-ttu-id="ee08f-123">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="ee08f-123">Requests a state change.</span></span><br/>                                                                              |
| [<span data-ttu-id="ee08f-124">**RevokeInteractiveSessionAccess**</span><span class="sxs-lookup"><span data-stu-id="ee08f-124">**RevokeInteractiveSessionAccess**</span></span>](revokeinteractivesessionaccess-msvm-terminalservice.md) | <span data-ttu-id="ee08f-125">從指定的受信者清單撤銷虛擬機器的互動式會話存取權。</span><span class="sxs-lookup"><span data-stu-id="ee08f-125">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span><br/> |
| [<span data-ttu-id="ee08f-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="ee08f-126">**StartService**</span></span>](msvm-terminalservice-startservice.md)                                     | <span data-ttu-id="ee08f-127">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="ee08f-127">Starts the service.</span></span><br/>                                                                                   |
| [<span data-ttu-id="ee08f-128">**StopService**</span><span class="sxs-lookup"><span data-stu-id="ee08f-128">**StopService**</span></span>](msvm-terminalservice-stopservice.md)                                       | <span data-ttu-id="ee08f-129">停止服務。</span><span class="sxs-lookup"><span data-stu-id="ee08f-129">Stops the service.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="ee08f-130">屬性</span><span class="sxs-lookup"><span data-stu-id="ee08f-130">Properties</span></span>

<span data-ttu-id="ee08f-131">**Msvm \_ TerminalService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ee08f-131">The **Msvm\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee08f-132">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="ee08f-132">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-133">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ee08f-133">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-135">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="ee08f-135">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="ee08f-136">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ee08f-136">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-137">**標題**</span><span class="sxs-lookup"><span data-stu-id="ee08f-137">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-140">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="ee08f-140">A short description of the object.</span></span> <span data-ttu-id="ee08f-141">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-142">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ee08f-142">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ee08f-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-145">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="ee08f-145">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ee08f-146">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="ee08f-146">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ee08f-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ee08f-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ee08f-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="ee08f-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="ee08f-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="ee08f-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="ee08f-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="ee08f-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="ee08f-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ee08f-155">)</span><span class="sxs-lookup"><span data-stu-id="ee08f-155">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee08f-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ee08f-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-159">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee08f-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ee08f-160">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-161">**說明**</span><span class="sxs-lookup"><span data-stu-id="ee08f-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-164">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="ee08f-164">A description of the object.</span></span> <span data-ttu-id="ee08f-165">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ee08f-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ee08f-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-169">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ee08f-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ee08f-170">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="ee08f-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ee08f-171">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ee08f-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="ee08f-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="ee08f-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="ee08f-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="ee08f-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="ee08f-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="ee08f-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="ee08f-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="ee08f-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ee08f-180">)</span><span class="sxs-lookup"><span data-stu-id="ee08f-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee08f-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ee08f-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-184">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ee08f-184">A display name for the object.</span></span> <span data-ttu-id="ee08f-185">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-186">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="ee08f-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-187">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ee08f-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-189">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="ee08f-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ee08f-190">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ee08f-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-191">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ee08f-191">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-194">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="ee08f-194">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ee08f-195">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="ee08f-195">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="ee08f-196">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ee08f-196">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-197">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ee08f-197">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-198">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ee08f-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-200">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="ee08f-200">The current health of the element.</span></span> <span data-ttu-id="ee08f-201">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="ee08f-201">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="ee08f-202">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="ee08f-202">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="ee08f-203">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ee08f-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-205">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ee08f-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-207">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ee08f-207">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="ee08f-208">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-209">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ee08f-209">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-212">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="ee08f-212">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-213">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ee08f-213">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ee08f-214">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ee08f-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-215">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ee08f-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-218">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="ee08f-218">The label by which the object is known.</span></span> <span data-ttu-id="ee08f-219">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-219">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-220">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ee08f-220">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-221">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ee08f-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-223">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ee08f-223">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ee08f-224">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="ee08f-224">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ee08f-225">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ee08f-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ee08f-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="ee08f-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="ee08f-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="ee08f-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="ee08f-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="ee08f-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="ee08f-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="ee08f-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="ee08f-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="ee08f-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="ee08f-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="ee08f-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="ee08f-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="ee08f-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="ee08f-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="ee08f-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="ee08f-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="ee08f-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="ee08f-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ee08f-245">)</span><span class="sxs-lookup"><span data-stu-id="ee08f-245">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee08f-246">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ee08f-246">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-247">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ee08f-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-249">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ee08f-249">The current statuses of the object.</span></span> <span data-ttu-id="ee08f-250">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-250">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-251">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="ee08f-251">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-254">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="ee08f-254">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ee08f-255">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ee08f-255">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="ee08f-256">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ee08f-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-257">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="ee08f-257">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-260">值，提供有關如何聯繫服務主要擁有者的資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="ee08f-260">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="ee08f-261">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-261">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-262">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="ee08f-262">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-263">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-265">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="ee08f-265">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="ee08f-266">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="ee08f-266">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="ee08f-267">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-267">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-268">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ee08f-268">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-269">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ee08f-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-271">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="ee08f-271">Provides high level status information.</span></span> <span data-ttu-id="ee08f-272">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="ee08f-272">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="ee08f-273">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="ee08f-273">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ee08f-274">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-274">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ee08f-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ee08f-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-276"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="ee08f-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="ee08f-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="ee08f-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="ee08f-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="ee08f-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ee08f-281">)</span><span class="sxs-lookup"><span data-stu-id="ee08f-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ee08f-282">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ee08f-282">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-283">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ee08f-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-285">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="ee08f-285">The last requested or desired state for the element.</span></span> <span data-ttu-id="ee08f-286">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="ee08f-286">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="ee08f-287">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="ee08f-287">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="ee08f-288">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="ee08f-288">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="ee08f-289">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="ee08f-289">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="ee08f-290">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="ee08f-290">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-291">**已開始**</span><span class="sxs-lookup"><span data-stu-id="ee08f-291">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-292">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ee08f-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-294">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="ee08f-294">Indicates whether the service is currently running.</span></span> <span data-ttu-id="ee08f-295">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-295">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-296">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="ee08f-296">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-299">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="ee08f-299">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="ee08f-300">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-301">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ee08f-301">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-302">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-304">元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="ee08f-304">The status of the element.</span></span> <span data-ttu-id="ee08f-305">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-306">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ee08f-306">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-307">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ee08f-307">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-309">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="ee08f-309">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ee08f-310">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-311">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ee08f-311">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-312">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-314">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="ee08f-314">The scoping system's creation class name.</span></span> <span data-ttu-id="ee08f-315">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-316">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ee08f-316">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ee08f-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-319">主控電腦系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee08f-319">The name of the hosting computer system.</span></span> <span data-ttu-id="ee08f-320">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-321">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="ee08f-321">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-322">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ee08f-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-324">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="ee08f-324">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ee08f-325">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ee08f-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ee08f-326">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="ee08f-326">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee08f-327">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ee08f-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ee08f-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ee08f-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ee08f-329">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="ee08f-329">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ee08f-330">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ee08f-330">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee08f-331">備註</span><span class="sxs-lookup"><span data-stu-id="ee08f-331">Remarks</span></span>

<span data-ttu-id="ee08f-332">存取 **Msvm \_ TerminalService** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="ee08f-332">Access to the **Msvm\_TerminalService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ee08f-333">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="ee08f-333">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee08f-334">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee08f-334">Requirements</span></span>



| <span data-ttu-id="ee08f-335">需求</span><span class="sxs-lookup"><span data-stu-id="ee08f-335">Requirement</span></span> | <span data-ttu-id="ee08f-336">值</span><span class="sxs-lookup"><span data-stu-id="ee08f-336">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee08f-337">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee08f-337">Minimum supported client</span></span><br/> | <span data-ttu-id="ee08f-338">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee08f-338">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ee08f-339">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee08f-339">Minimum supported server</span></span><br/> | <span data-ttu-id="ee08f-340">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee08f-340">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee08f-341">命名空間</span><span class="sxs-lookup"><span data-stu-id="ee08f-341">Namespace</span></span><br/>                | <span data-ttu-id="ee08f-342">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="ee08f-342">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ee08f-343">MOF</span><span class="sxs-lookup"><span data-stu-id="ee08f-343">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee08f-344"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ee08f-344"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee08f-345">DLL</span><span class="sxs-lookup"><span data-stu-id="ee08f-345">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee08f-346"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ee08f-346"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ee08f-347">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee08f-347">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee08f-348">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="ee08f-348">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

