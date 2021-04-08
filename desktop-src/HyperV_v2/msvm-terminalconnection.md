---
description: 表示與虛擬機器互動之作用中遠端會話的狀態。
ms.assetid: EAE6082F-A0CB-4E75-8029-51E20649C0A8
title: Msvm_TerminalConnection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalConnection
- Msvm_TerminalConnection.InstanceID
- Msvm_TerminalConnection.Caption
- Msvm_TerminalConnection.Description
- Msvm_TerminalConnection.ElementName
- Msvm_TerminalConnection.InstallDate
- Msvm_TerminalConnection.Name
- Msvm_TerminalConnection.OperationalStatus
- Msvm_TerminalConnection.StatusDescriptions
- Msvm_TerminalConnection.Status
- Msvm_TerminalConnection.HealthState
- Msvm_TerminalConnection.CommunicationStatus
- Msvm_TerminalConnection.DetailedStatus
- Msvm_TerminalConnection.OperatingStatus
- Msvm_TerminalConnection.PrimaryStatus
- Msvm_TerminalConnection.EnabledState
- Msvm_TerminalConnection.OtherEnabledState
- Msvm_TerminalConnection.RequestedState
- Msvm_TerminalConnection.EnabledDefault
- Msvm_TerminalConnection.TimeOfLastStateChange
- Msvm_TerminalConnection.AvailableRequestedStates
- Msvm_TerminalConnection.TransitioningToState
- Msvm_TerminalConnection.ConnectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66be5000fb7fdd4404e07c87673e3359065af6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694676"
---
# <a name="msvm_terminalconnection-class"></a><span data-ttu-id="dae5b-103">Msvm \_ TerminalConnection 類別</span><span class="sxs-lookup"><span data-stu-id="dae5b-103">Msvm\_TerminalConnection class</span></span>

<span data-ttu-id="dae5b-104">表示與虛擬機器互動之作用中遠端會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="dae5b-104">Indicates the state of an active remote session interacting with a virtual machine.</span></span> <span data-ttu-id="dae5b-105">一次只能有一個連接。</span><span class="sxs-lookup"><span data-stu-id="dae5b-105">There can only be one connection at a time.</span></span>

<span data-ttu-id="dae5b-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dae5b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae5b-107">語法</span><span class="sxs-lookup"><span data-stu-id="dae5b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalConnection : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   ConnectionID;
};
```

## <a name="members"></a><span data-ttu-id="dae5b-108">成員</span><span class="sxs-lookup"><span data-stu-id="dae5b-108">Members</span></span>

<span data-ttu-id="dae5b-109">**Msvm \_ TerminalConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dae5b-109">The **Msvm\_TerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="dae5b-110">方法</span><span class="sxs-lookup"><span data-stu-id="dae5b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dae5b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="dae5b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dae5b-112">方法</span><span class="sxs-lookup"><span data-stu-id="dae5b-112">Methods</span></span>

<span data-ttu-id="dae5b-113">**Msvm \_ TerminalConnection** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dae5b-113">The **Msvm\_TerminalConnection** class has these methods.</span></span>



| <span data-ttu-id="dae5b-114">方法</span><span class="sxs-lookup"><span data-stu-id="dae5b-114">Method</span></span>                                                                   | <span data-ttu-id="dae5b-115">描述</span><span class="sxs-lookup"><span data-stu-id="dae5b-115">Description</span></span>                         |
|:-------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="dae5b-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="dae5b-116">**RequestStateChange**</span></span>](msvm-terminalconnection-requeststatechange.md) | <span data-ttu-id="dae5b-117">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="dae5b-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dae5b-118">屬性</span><span class="sxs-lookup"><span data-stu-id="dae5b-118">Properties</span></span>

<span data-ttu-id="dae5b-119">**Msvm \_ TerminalConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dae5b-119">The **Msvm\_TerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dae5b-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="dae5b-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-121">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="dae5b-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-123">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="dae5b-123">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="dae5b-124">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dae5b-124">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="dae5b-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dae5b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-128">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="dae5b-128">A short description of the object.</span></span> <span data-ttu-id="dae5b-129">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="dae5b-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dae5b-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-133">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="dae5b-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="dae5b-134">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="dae5b-134">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dae5b-135">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-135">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dae5b-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="dae5b-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="dae5b-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="dae5b-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="dae5b-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="dae5b-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="dae5b-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="dae5b-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dae5b-143">)</span><span class="sxs-lookup"><span data-stu-id="dae5b-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dae5b-144">**ConnectionID**</span><span class="sxs-lookup"><span data-stu-id="dae5b-144">**ConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dae5b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-147">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dae5b-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-148">終端連線物件實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="dae5b-148">The unique identifier for an instance of the terminal connection object.</span></span> <span data-ttu-id="dae5b-149">識別碼的格式為 "Microsoft：*VMID* \\ *Index*"。</span><span class="sxs-lookup"><span data-stu-id="dae5b-149">The identifier is of the form "Microsoft:*VMID*\\*Index*".</span></span> <span data-ttu-id="dae5b-150">例如「Microsoft： 67A5D397-A02D-11DB-AC13-001676AA34F0 0」 \\ 。</span><span class="sxs-lookup"><span data-stu-id="dae5b-150">For example, "Microsoft:67A5D397-A02D-11DB-AC13-001676AA34F0\\0".</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-151">**說明**</span><span class="sxs-lookup"><span data-stu-id="dae5b-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dae5b-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-154">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="dae5b-154">A description of the object.</span></span> <span data-ttu-id="dae5b-155">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="dae5b-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-157">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dae5b-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-159">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dae5b-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="dae5b-160">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="dae5b-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dae5b-161">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dae5b-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="dae5b-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="dae5b-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="dae5b-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="dae5b-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="dae5b-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="dae5b-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="dae5b-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="dae5b-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dae5b-170">)</span><span class="sxs-lookup"><span data-stu-id="dae5b-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dae5b-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dae5b-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dae5b-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-174">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="dae5b-174">A display name for the object.</span></span> <span data-ttu-id="dae5b-175">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-176">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="dae5b-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-177">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dae5b-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-179">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="dae5b-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="dae5b-180">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="dae5b-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="dae5b-181">值</span><span class="sxs-lookup"><span data-stu-id="dae5b-181">Value</span></span>                                                                        | <span data-ttu-id="dae5b-182">意義</span><span class="sxs-lookup"><span data-stu-id="dae5b-182">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="dae5b-183"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dae5b-183"><dt>2</dt></span></span> </dl> | <span data-ttu-id="dae5b-184">已啟用</span><span class="sxs-lookup"><span data-stu-id="dae5b-184">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="dae5b-185"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="dae5b-185"><dt>3</dt></span></span> </dl> | <span data-ttu-id="dae5b-186">Disabled</span><span class="sxs-lookup"><span data-stu-id="dae5b-186">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dae5b-187">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="dae5b-187">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-188">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dae5b-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-190">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="dae5b-190">The enabled and disabled states of an element.</span></span> <span data-ttu-id="dae5b-191">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="dae5b-191">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="dae5b-192">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="dae5b-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="dae5b-193">值</span><span class="sxs-lookup"><span data-stu-id="dae5b-193">Value</span></span>                                                                        | <span data-ttu-id="dae5b-194">意義</span><span class="sxs-lookup"><span data-stu-id="dae5b-194">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="dae5b-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dae5b-195"><dt>2</dt></span></span> </dl> | <span data-ttu-id="dae5b-196">已啟用</span><span class="sxs-lookup"><span data-stu-id="dae5b-196">Enabled</span></span><br/>        |
| <dl> <span data-ttu-id="dae5b-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="dae5b-197"><dt>3</dt></span></span> </dl> | <span data-ttu-id="dae5b-198">Disabled</span><span class="sxs-lookup"><span data-stu-id="dae5b-198">Disabled</span></span><br/>       |
| <dl> <span data-ttu-id="dae5b-199"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="dae5b-199"><dt>5</dt></span></span> </dl> | <span data-ttu-id="dae5b-200">不適用</span><span class="sxs-lookup"><span data-stu-id="dae5b-200">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dae5b-201">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="dae5b-201">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-202">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dae5b-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-204">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="dae5b-204">The current health of the element.</span></span> <span data-ttu-id="dae5b-205">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="dae5b-205">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="dae5b-206">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="dae5b-206">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="dae5b-207">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="dae5b-207">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dae5b-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-209">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dae5b-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-211">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="dae5b-211">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="dae5b-212">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-213">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dae5b-213">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dae5b-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-216">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="dae5b-216">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-217">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="dae5b-217">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dae5b-218">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-219">**名稱**</span><span class="sxs-lookup"><span data-stu-id="dae5b-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dae5b-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-222">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="dae5b-222">The label by which the object is known.</span></span> <span data-ttu-id="dae5b-223">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="dae5b-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-224">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="dae5b-224">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-225">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dae5b-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-227">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dae5b-227">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="dae5b-228">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="dae5b-228">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dae5b-229">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dae5b-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="dae5b-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="dae5b-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="dae5b-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="dae5b-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="dae5b-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="dae5b-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="dae5b-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="dae5b-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="dae5b-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="dae5b-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="dae5b-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="dae5b-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="dae5b-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="dae5b-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="dae5b-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="dae5b-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="dae5b-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="dae5b-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="dae5b-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dae5b-249">)</span><span class="sxs-lookup"><span data-stu-id="dae5b-249">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dae5b-250">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="dae5b-250">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-251">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="dae5b-251">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-253">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="dae5b-253">The current statuses of the object.</span></span> <span data-ttu-id="dae5b-254">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-255">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="dae5b-255">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-256">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dae5b-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-258">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="dae5b-258">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="dae5b-259">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dae5b-259">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="dae5b-260">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dae5b-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-261">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="dae5b-261">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-262">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dae5b-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-264">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="dae5b-264">Provides high level status information.</span></span> <span data-ttu-id="dae5b-265">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="dae5b-265">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="dae5b-266">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="dae5b-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dae5b-267">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dae5b-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="dae5b-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-269"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="dae5b-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="dae5b-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="dae5b-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="dae5b-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="dae5b-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dae5b-274">)</span><span class="sxs-lookup"><span data-stu-id="dae5b-274">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dae5b-275">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="dae5b-275">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-276">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dae5b-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-278">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="dae5b-278">The last requested or desired state for the element.</span></span> <span data-ttu-id="dae5b-279">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="dae5b-279">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="dae5b-280">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="dae5b-280">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="dae5b-281">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange**。</span><span class="sxs-lookup"><span data-stu-id="dae5b-281">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="dae5b-282">如果發生這種情況，則會使用值12。</span><span class="sxs-lookup"><span data-stu-id="dae5b-282">If this occurs, the value 12 is used.</span></span> <span data-ttu-id="dae5b-283">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="dae5b-283">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>



| <span data-ttu-id="dae5b-284">值</span><span class="sxs-lookup"><span data-stu-id="dae5b-284">Value</span></span>                                                                         | <span data-ttu-id="dae5b-285">意義</span><span class="sxs-lookup"><span data-stu-id="dae5b-285">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="dae5b-286"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="dae5b-286"><dt>12</dt></span></span> </dl> | <span data-ttu-id="dae5b-287">不適用</span><span class="sxs-lookup"><span data-stu-id="dae5b-287">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dae5b-288">**狀態**</span><span class="sxs-lookup"><span data-stu-id="dae5b-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dae5b-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-291">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="dae5b-291">The current status of the object.</span></span> <span data-ttu-id="dae5b-292">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="dae5b-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dae5b-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-294">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="dae5b-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-296">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="dae5b-296">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="dae5b-297">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-298">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="dae5b-298">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-299">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dae5b-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-301">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="dae5b-301">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="dae5b-302">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dae5b-302">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dae5b-303">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="dae5b-303">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dae5b-304">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dae5b-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dae5b-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dae5b-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dae5b-306">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="dae5b-306">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="dae5b-307">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="dae5b-307">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="dae5b-308">值</span><span class="sxs-lookup"><span data-stu-id="dae5b-308">Value</span></span>                                                                         | <span data-ttu-id="dae5b-309">意義</span><span class="sxs-lookup"><span data-stu-id="dae5b-309">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="dae5b-310"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="dae5b-310"><dt>12</dt></span></span> </dl> | <span data-ttu-id="dae5b-311">不適用</span><span class="sxs-lookup"><span data-stu-id="dae5b-311">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dae5b-312">備註</span><span class="sxs-lookup"><span data-stu-id="dae5b-312">Remarks</span></span>

<span data-ttu-id="dae5b-313">存取 **Msvm \_ TerminalConnection** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="dae5b-313">Access to the **Msvm\_TerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dae5b-314">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="dae5b-314">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dae5b-315">規格需求</span><span class="sxs-lookup"><span data-stu-id="dae5b-315">Requirements</span></span>



| <span data-ttu-id="dae5b-316">需求</span><span class="sxs-lookup"><span data-stu-id="dae5b-316">Requirement</span></span> | <span data-ttu-id="dae5b-317">值</span><span class="sxs-lookup"><span data-stu-id="dae5b-317">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae5b-318">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dae5b-318">Minimum supported client</span></span><br/> | <span data-ttu-id="dae5b-319">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dae5b-319">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dae5b-320">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dae5b-320">Minimum supported server</span></span><br/> | <span data-ttu-id="dae5b-321">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dae5b-321">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dae5b-322">命名空間</span><span class="sxs-lookup"><span data-stu-id="dae5b-322">Namespace</span></span><br/>                | <span data-ttu-id="dae5b-323">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="dae5b-323">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dae5b-324">MOF</span><span class="sxs-lookup"><span data-stu-id="dae5b-324">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dae5b-325"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="dae5b-325"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dae5b-326">DLL</span><span class="sxs-lookup"><span data-stu-id="dae5b-326">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dae5b-327"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dae5b-327"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dae5b-328">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dae5b-328">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae5b-329">**CIM \_ EnabledLogicalElement**</span><span class="sxs-lookup"><span data-stu-id="dae5b-329">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> <dt>

<span data-ttu-id="dae5b-330">[**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dae5b-330">[**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dae5b-331">影片類別</span><span class="sxs-lookup"><span data-stu-id="dae5b-331">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

