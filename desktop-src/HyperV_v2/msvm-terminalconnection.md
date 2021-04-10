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
# <a name="msvm_terminalconnection-class"></a><span data-ttu-id="22d40-103">Msvm \_ TerminalConnection 類別</span><span class="sxs-lookup"><span data-stu-id="22d40-103">Msvm\_TerminalConnection class</span></span>

<span data-ttu-id="22d40-104">表示與虛擬機器互動之作用中遠端會話的狀態。</span><span class="sxs-lookup"><span data-stu-id="22d40-104">Indicates the state of an active remote session interacting with a virtual machine.</span></span> <span data-ttu-id="22d40-105">一次只能有一個連接。</span><span class="sxs-lookup"><span data-stu-id="22d40-105">There can only be one connection at a time.</span></span>

<span data-ttu-id="22d40-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="22d40-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d40-107">語法</span><span class="sxs-lookup"><span data-stu-id="22d40-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="22d40-108">成員</span><span class="sxs-lookup"><span data-stu-id="22d40-108">Members</span></span>

<span data-ttu-id="22d40-109">**Msvm \_ TerminalConnection** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="22d40-109">The **Msvm\_TerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="22d40-110">方法</span><span class="sxs-lookup"><span data-stu-id="22d40-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="22d40-111">屬性</span><span class="sxs-lookup"><span data-stu-id="22d40-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22d40-112">方法</span><span class="sxs-lookup"><span data-stu-id="22d40-112">Methods</span></span>

<span data-ttu-id="22d40-113">**Msvm \_ TerminalConnection** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="22d40-113">The **Msvm\_TerminalConnection** class has these methods.</span></span>



| <span data-ttu-id="22d40-114">方法</span><span class="sxs-lookup"><span data-stu-id="22d40-114">Method</span></span>                                                                   | <span data-ttu-id="22d40-115">描述</span><span class="sxs-lookup"><span data-stu-id="22d40-115">Description</span></span>                         |
|:-------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="22d40-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="22d40-116">**RequestStateChange**</span></span>](msvm-terminalconnection-requeststatechange.md) | <span data-ttu-id="22d40-117">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="22d40-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="22d40-118">屬性</span><span class="sxs-lookup"><span data-stu-id="22d40-118">Properties</span></span>

<span data-ttu-id="22d40-119">**Msvm \_ TerminalConnection** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="22d40-119">The **Msvm\_TerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22d40-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="22d40-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-121">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="22d40-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22d40-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-123">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="22d40-123">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="22d40-124">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="22d40-124">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22d40-125">**標題**</span><span class="sxs-lookup"><span data-stu-id="22d40-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22d40-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-128">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="22d40-128">A short description of the object.</span></span> <span data-ttu-id="22d40-129">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22d40-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="22d40-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22d40-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-133">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="22d40-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="22d40-134">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="22d40-134">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22d40-135">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-135">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22d40-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="22d40-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="22d40-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="22d40-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="22d40-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="22d40-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="22d40-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="22d40-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22d40-143">)</span><span class="sxs-lookup"><span data-stu-id="22d40-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22d40-144">**ConnectionID**</span><span class="sxs-lookup"><span data-stu-id="22d40-144">**ConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22d40-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22d40-147">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="22d40-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="22d40-148">終端連線物件實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="22d40-148">The unique identifier for an instance of the terminal connection object.</span></span> <span data-ttu-id="22d40-149">識別碼的格式為 "Microsoft：*VMID* \\ *Index*"。</span><span class="sxs-lookup"><span data-stu-id="22d40-149">The identifier is of the form "Microsoft:*VMID*\\*Index*".</span></span> <span data-ttu-id="22d40-150">例如「Microsoft： 67A5D397-A02D-11DB-AC13-001676AA34F0 0」 \\ 。</span><span class="sxs-lookup"><span data-stu-id="22d40-150">For example, "Microsoft:67A5D397-A02D-11DB-AC13-001676AA34F0\\0".</span></span>

</dd> <dt>

<span data-ttu-id="22d40-151">**說明**</span><span class="sxs-lookup"><span data-stu-id="22d40-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22d40-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-154">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="22d40-154">A description of the object.</span></span> <span data-ttu-id="22d40-155">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22d40-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="22d40-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-157">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22d40-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-159">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="22d40-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="22d40-160">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="22d40-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22d40-161">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22d40-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="22d40-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="22d40-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="22d40-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="22d40-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="22d40-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="22d40-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="22d40-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="22d40-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22d40-170">)</span><span class="sxs-lookup"><span data-stu-id="22d40-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22d40-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="22d40-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22d40-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-174">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="22d40-174">A display name for the object.</span></span> <span data-ttu-id="22d40-175">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22d40-176">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="22d40-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-177">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22d40-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-179">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="22d40-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="22d40-180">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22d40-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="22d40-181">值</span><span class="sxs-lookup"><span data-stu-id="22d40-181">Value</span></span>                                                                        | <span data-ttu-id="22d40-182">意義</span><span class="sxs-lookup"><span data-stu-id="22d40-182">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="22d40-183"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="22d40-183"><dt>2</dt></span></span> </dl> | <span data-ttu-id="22d40-184">已啟用</span><span class="sxs-lookup"><span data-stu-id="22d40-184">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="22d40-185"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="22d40-185"><dt>3</dt></span></span> </dl> | <span data-ttu-id="22d40-186">Disabled</span><span class="sxs-lookup"><span data-stu-id="22d40-186">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="22d40-187">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="22d40-187">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-188">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22d40-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-190">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="22d40-190">The enabled and disabled states of an element.</span></span> <span data-ttu-id="22d40-191">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="22d40-191">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="22d40-192">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22d40-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="22d40-193">值</span><span class="sxs-lookup"><span data-stu-id="22d40-193">Value</span></span>                                                                        | <span data-ttu-id="22d40-194">意義</span><span class="sxs-lookup"><span data-stu-id="22d40-194">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="22d40-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="22d40-195"><dt>2</dt></span></span> </dl> | <span data-ttu-id="22d40-196">已啟用</span><span class="sxs-lookup"><span data-stu-id="22d40-196">Enabled</span></span><br/>        |
| <dl> <span data-ttu-id="22d40-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="22d40-197"><dt>3</dt></span></span> </dl> | <span data-ttu-id="22d40-198">Disabled</span><span class="sxs-lookup"><span data-stu-id="22d40-198">Disabled</span></span><br/>       |
| <dl> <span data-ttu-id="22d40-199"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="22d40-199"><dt>5</dt></span></span> </dl> | <span data-ttu-id="22d40-200">不適用</span><span class="sxs-lookup"><span data-stu-id="22d40-200">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="22d40-201">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="22d40-201">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-202">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22d40-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-204">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="22d40-204">The current health of the element.</span></span> <span data-ttu-id="22d40-205">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="22d40-205">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="22d40-206">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="22d40-206">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="22d40-207">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="22d40-207">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="22d40-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="22d40-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-209">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="22d40-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-211">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="22d40-211">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="22d40-212">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22d40-213">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="22d40-213">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22d40-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22d40-216">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="22d40-216">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="22d40-217">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="22d40-217">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="22d40-218">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22d40-219">**名稱**</span><span class="sxs-lookup"><span data-stu-id="22d40-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-220">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22d40-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-222">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="22d40-222">The label by which the object is known.</span></span> <span data-ttu-id="22d40-223">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="22d40-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="22d40-224">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="22d40-224">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-225">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22d40-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-227">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="22d40-227">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="22d40-228">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="22d40-228">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22d40-229">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22d40-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="22d40-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="22d40-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="22d40-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="22d40-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="22d40-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="22d40-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="22d40-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="22d40-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="22d40-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="22d40-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="22d40-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="22d40-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="22d40-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="22d40-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="22d40-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="22d40-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="22d40-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="22d40-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="22d40-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22d40-249">)</span><span class="sxs-lookup"><span data-stu-id="22d40-249">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22d40-250">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="22d40-250">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-251">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="22d40-251">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22d40-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-253">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="22d40-253">The current statuses of the object.</span></span> <span data-ttu-id="22d40-254">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22d40-255">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="22d40-255">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-256">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22d40-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-258">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="22d40-258">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="22d40-259">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="22d40-259">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="22d40-260">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="22d40-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22d40-261">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="22d40-261">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-262">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22d40-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-264">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="22d40-264">Provides high level status information.</span></span> <span data-ttu-id="22d40-265">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="22d40-265">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="22d40-266">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="22d40-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22d40-267">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="22d40-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="22d40-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-269"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="22d40-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="22d40-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="22d40-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="22d40-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="22d40-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="22d40-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="22d40-274">)</span><span class="sxs-lookup"><span data-stu-id="22d40-274">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22d40-275">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="22d40-275">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-276">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22d40-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-278">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="22d40-278">The last requested or desired state for the element.</span></span> <span data-ttu-id="22d40-279">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="22d40-279">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="22d40-280">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="22d40-280">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="22d40-281">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange**。</span><span class="sxs-lookup"><span data-stu-id="22d40-281">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="22d40-282">如果發生這種情況，則會使用值12。</span><span class="sxs-lookup"><span data-stu-id="22d40-282">If this occurs, the value 12 is used.</span></span> <span data-ttu-id="22d40-283">這個屬性繼承自 **CIM \_ EnabledLogicalElement**。</span><span class="sxs-lookup"><span data-stu-id="22d40-283">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>



| <span data-ttu-id="22d40-284">值</span><span class="sxs-lookup"><span data-stu-id="22d40-284">Value</span></span>                                                                         | <span data-ttu-id="22d40-285">意義</span><span class="sxs-lookup"><span data-stu-id="22d40-285">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="22d40-286"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="22d40-286"><dt>12</dt></span></span> </dl> | <span data-ttu-id="22d40-287">不適用</span><span class="sxs-lookup"><span data-stu-id="22d40-287">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="22d40-288">**狀態**</span><span class="sxs-lookup"><span data-stu-id="22d40-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="22d40-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-291">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="22d40-291">The current status of the object.</span></span> <span data-ttu-id="22d40-292">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="22d40-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22d40-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="22d40-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-294">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="22d40-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22d40-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-296">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="22d40-296">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="22d40-297">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="22d40-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22d40-298">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="22d40-298">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-299">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="22d40-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-301">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="22d40-301">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="22d40-302">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="22d40-302">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22d40-303">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="22d40-303">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22d40-304">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="22d40-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22d40-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="22d40-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22d40-306">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="22d40-306">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="22d40-307">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="22d40-307">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="22d40-308">值</span><span class="sxs-lookup"><span data-stu-id="22d40-308">Value</span></span>                                                                         | <span data-ttu-id="22d40-309">意義</span><span class="sxs-lookup"><span data-stu-id="22d40-309">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="22d40-310"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="22d40-310"><dt>12</dt></span></span> </dl> | <span data-ttu-id="22d40-311">不適用</span><span class="sxs-lookup"><span data-stu-id="22d40-311">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22d40-312">備註</span><span class="sxs-lookup"><span data-stu-id="22d40-312">Remarks</span></span>

<span data-ttu-id="22d40-313">存取 **Msvm \_ TerminalConnection** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="22d40-313">Access to the **Msvm\_TerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="22d40-314">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="22d40-314">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="22d40-315">規格需求</span><span class="sxs-lookup"><span data-stu-id="22d40-315">Requirements</span></span>



| <span data-ttu-id="22d40-316">需求</span><span class="sxs-lookup"><span data-stu-id="22d40-316">Requirement</span></span> | <span data-ttu-id="22d40-317">值</span><span class="sxs-lookup"><span data-stu-id="22d40-317">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d40-318">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22d40-318">Minimum supported client</span></span><br/> | <span data-ttu-id="22d40-319">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22d40-319">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="22d40-320">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22d40-320">Minimum supported server</span></span><br/> | <span data-ttu-id="22d40-321">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22d40-321">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22d40-322">命名空間</span><span class="sxs-lookup"><span data-stu-id="22d40-322">Namespace</span></span><br/>                | <span data-ttu-id="22d40-323">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="22d40-323">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="22d40-324">MOF</span><span class="sxs-lookup"><span data-stu-id="22d40-324">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22d40-325"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="22d40-325"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22d40-326">DLL</span><span class="sxs-lookup"><span data-stu-id="22d40-326">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22d40-327"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22d40-327"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="22d40-328">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22d40-328">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d40-329">**CIM \_ EnabledLogicalElement**</span><span class="sxs-lookup"><span data-stu-id="22d40-329">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> <dt>

<span data-ttu-id="22d40-330">[**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22d40-330">[**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="22d40-331">影片類別</span><span class="sxs-lookup"><span data-stu-id="22d40-331">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

