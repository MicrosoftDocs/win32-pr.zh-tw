---
description: 代表已規劃的虛擬機器。
ms.assetid: 4ce6d34c-66fb-4f4f-bf52-26d19bab6d4a
title: Msvm_PlannedComputerSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem
- Msvm_PlannedComputerSystem.SetPowerState
- Msvm_PlannedComputerSystem.InstanceID
- Msvm_PlannedComputerSystem.Caption
- Msvm_PlannedComputerSystem.Description
- Msvm_PlannedComputerSystem.ElementName
- Msvm_PlannedComputerSystem.InstallDate
- Msvm_PlannedComputerSystem.OperationalStatus
- Msvm_PlannedComputerSystem.StatusDescriptions
- Msvm_PlannedComputerSystem.Status
- Msvm_PlannedComputerSystem.HealthState
- Msvm_PlannedComputerSystem.CommunicationStatus
- Msvm_PlannedComputerSystem.DetailedStatus
- Msvm_PlannedComputerSystem.OperatingStatus
- Msvm_PlannedComputerSystem.PrimaryStatus
- Msvm_PlannedComputerSystem.EnabledState
- Msvm_PlannedComputerSystem.OtherEnabledState
- Msvm_PlannedComputerSystem.RequestedState
- Msvm_PlannedComputerSystem.EnabledDefault
- Msvm_PlannedComputerSystem.TimeOfLastStateChange
- Msvm_PlannedComputerSystem.AvailableRequestedStates
- Msvm_PlannedComputerSystem.TransitioningToState
- Msvm_PlannedComputerSystem.CreationClassName
- Msvm_PlannedComputerSystem.Name
- Msvm_PlannedComputerSystem.NameFormat
- Msvm_PlannedComputerSystem.PrimaryOwnerName
- Msvm_PlannedComputerSystem.PrimaryOwnerContact
- Msvm_PlannedComputerSystem.Roles
- Msvm_PlannedComputerSystem.OtherIdentifyingInfo
- Msvm_PlannedComputerSystem.IdentifyingDescriptions
- Msvm_PlannedComputerSystem.Dedicated
- Msvm_PlannedComputerSystem.OtherDedicatedDescriptions
- Msvm_PlannedComputerSystem.ResetCapability
- Msvm_PlannedComputerSystem.PowerManagementCapabilities
- Msvm_PlannedComputerSystem.AssignedNumaNodeList
- Msvm_PlannedComputerSystem.OnTimeInMilliseconds
- Msvm_PlannedComputerSystem.ProcessID
- Msvm_PlannedComputerSystem.TimeOfLastConfigurationChange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 54bd72567880e97ece02936348d5a091a11d8ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984244"
---
# <a name="msvm_plannedcomputersystem-class"></a><span data-ttu-id="fa8a4-103">Msvm \_ PlannedComputerSystem 類別</span><span class="sxs-lookup"><span data-stu-id="fa8a4-103">Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="fa8a4-104">代表已規劃的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-104">Represents a planned virtual machine.</span></span>

<span data-ttu-id="fa8a4-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8a4-106">語法</span><span class="sxs-lookup"><span data-stu-id="fa8a4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PlannedComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Planned Virtual Machine";
  string   Description = "Microsoft Planned Virtual Machine";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
  uint16   AssignedNumaNodeList[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
};
```

## <a name="members"></a><span data-ttu-id="fa8a4-107">成員</span><span class="sxs-lookup"><span data-stu-id="fa8a4-107">Members</span></span>

<span data-ttu-id="fa8a4-108">**Msvm \_ PlannedComputerSystem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fa8a4-108">The **Msvm\_PlannedComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="fa8a4-109">方法</span><span class="sxs-lookup"><span data-stu-id="fa8a4-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="fa8a4-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fa8a4-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fa8a4-111">方法</span><span class="sxs-lookup"><span data-stu-id="fa8a4-111">Methods</span></span>

<span data-ttu-id="fa8a4-112">**Msvm \_ PlannedComputerSystem** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-112">The **Msvm\_PlannedComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="fa8a4-113">方法</span><span class="sxs-lookup"><span data-stu-id="fa8a4-113">Method</span></span>                                                                      | <span data-ttu-id="fa8a4-114">描述</span><span class="sxs-lookup"><span data-stu-id="fa8a4-114">Description</span></span>                                                                                 |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa8a4-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-115">**RequestStateChange**</span></span>](requeststatechange-msvm-plannedcomputersystem.md) | <span data-ttu-id="fa8a4-116">要求已規劃的系統狀態會變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-116">Requests that the state of the planned system be changed to the value specified.</span></span><br/> |
| <span data-ttu-id="fa8a4-117">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-117">**SetPowerState**</span></span>                                                           | <span data-ttu-id="fa8a4-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-118">This method is not supported.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="fa8a4-119">屬性</span><span class="sxs-lookup"><span data-stu-id="fa8a4-119">Properties</span></span>

<span data-ttu-id="fa8a4-120">**Msvm \_ PlannedComputerSystem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-120">The **Msvm\_PlannedComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa8a4-121">**AssignedNumaNodeList**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-121">**AssignedNumaNodeList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-122">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-124">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-125">目前指派給虛擬機器 (NUMA) 節點的非統一記憶體存取陣列。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-125">An array of nonuniform memory access (NUMA) nodes that are currently assigned to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-126">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-127">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-129">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="fa8a4-130">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="fa8a4-131">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="fa8a4-132">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="fa8a4-133">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="fa8a4-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="fa8a4-144">)</span><span class="sxs-lookup"><span data-stu-id="fa8a4-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fa8a4-145">**標題**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-148">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-148">A short description of the object.</span></span> <span data-ttu-id="fa8a4-149">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「規劃的虛擬機器」。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-150">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-153">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="fa8a4-154">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fa8a4-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-159">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-160">指出建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-160">Indicates the name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="fa8a4-161">搭配這個類別的其他重要屬性使用時，此屬性可讓這個類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-161">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="fa8a4-162">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system) 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-162">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-163">**專用**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-163">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-164">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-166">值的陣列，表示已規劃系統的專用用途（如果有的話），以及所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-166">An array of values that indicate the purposes to which the planned system is dedicated, if any, and what functionality is provided.</span></span> <span data-ttu-id="fa8a4-167">例如，您可以指定系統專門用來「列印」 (值 = 11) 或作為「中樞」 (值 = 8) 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-167">For example, one could specify that the System is dedicated to "Print" (value=11) or acts as a "Hub" (value=8).</span></span> <span data-ttu-id="fa8a4-168">也可以指出多個用途。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-168">Multiple purposes can also be indicated.</span></span> <span data-ttu-id="fa8a4-169">例如，這是一般目的系統，表示「非專用」 (值 = 0) 但它也會將 "Print" (value = 11) 或 "Mobile User Device" (value = 17) 服務。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-169">For example, this is a general purpose system indicating "Not Dedicated" (value=0) but that it also hosts "Print" (value=11) or "Mobile User Device" (value=17) services.</span></span>

<span data-ttu-id="fa8a4-170">這個屬性繼承自 CIM 的 [**[ \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 的工作類型] 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-170">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="fa8a4-171">值</span><span class="sxs-lookup"><span data-stu-id="fa8a4-171">Value</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="fa8a4-172">意義</span><span class="sxs-lookup"><span data-stu-id="fa8a4-172">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span><dl> <span data-ttu-id="fa8a4-173"><dt>**非專用**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-173"><dt>**Not Dedicated**</dt> <dt>0</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fa8a4-174"><dt>**未知**</dt>的 <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-174"><dt>**Unknown**</dt> <dt>1</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="fa8a4-175"><dt>**其他**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-175"><dt>**Other**</dt> <dt>2</dt></span></span> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span><dl> <span data-ttu-id="fa8a4-176"><dt>**儲存體**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-176"><dt>**Storage**</dt> <dt>3</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Router"></span><span id="router"></span><span id="ROUTER"></span><dl> <span data-ttu-id="fa8a4-177"><dt>**路由器**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-177"><dt>**Router**</dt> <dt>4</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span><dl> <span data-ttu-id="fa8a4-178"><dt>**切換**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-178"><dt>**Switch**</dt> <dt>5</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span><dl> <span data-ttu-id="fa8a4-179"><dt>**第3層交換器**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-179"><dt>**Layer 3 Switch**</dt> <dt>6</dt></span></span> </dl>                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span><dl> <span data-ttu-id="fa8a4-180"><dt>**中央辦公室交換器**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-180"><dt>**Central Office Switch**</dt> <dt>7</dt></span></span> </dl>                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Hub"></span><span id="hub"></span><span id="HUB"></span><dl> <span data-ttu-id="fa8a4-181"><dt>**中樞**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-181"><dt>**Hub**</dt> <dt>8</dt></span></span> </dl>                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span><dl> <span data-ttu-id="fa8a4-182"><dt>**存取伺服器**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-182"><dt>**Access Server**</dt> <dt>9</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span><dl> <span data-ttu-id="fa8a4-183"><dt>**防火牆**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-183"><dt>**Firewall**</dt> <dt>10</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Print"></span><span id="print"></span><span id="PRINT"></span><dl> <span data-ttu-id="fa8a4-184"><dt>**列印**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-184"><dt>**Print**</dt> <dt>11</dt></span></span> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="I_O"></span><span id="i_o"></span><dl> <span data-ttu-id="fa8a4-185"><dt>**I/o**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-185"><dt>**I/O**</dt> <dt>12</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span><dl> <span data-ttu-id="fa8a4-186"><dt>**Web Caching**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-186"><dt>**Web Caching**</dt> <dt>13</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span><dl> <span data-ttu-id="fa8a4-187"><dt>**管理**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-187"><dt>**Management**</dt> <dt>14</dt></span></span> </dl>                                                                 | <span data-ttu-id="fa8a4-188">表示這個實例專門用來裝載系統管理軟體。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-188">Indicates this instance is dedicated to hosting system management software.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span><dl> <span data-ttu-id="fa8a4-189"><dt>**封鎖伺服器**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-189"><dt>**Block Server**</dt> <dt>15</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span><dl> <span data-ttu-id="fa8a4-190"><dt>**檔案伺服器**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-190"><dt>**File Server**</dt> <dt>16</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span><dl> <span data-ttu-id="fa8a4-191">行動 <dt>**使用者裝置**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-191"><dt>**Mobile User Device**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="fa8a4-192">專用行動使用者裝置的範例為行動電話或在商店中的條碼掃描器，可透過無線電頻率進行通訊。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-192">An example of a dedicated mobile user device is a mobile phone or a bar code scanner in a store that communicates through radio frequency.</span></span> <span data-ttu-id="fa8a4-193">這些系統在功能和可程式性方面都有很大的限制，不會被視為一般目的運算平臺。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-193">These systems are quite limited in functionality and programmability, and are not considered general purpose computing platforms.</span></span> <span data-ttu-id="fa8a4-194">或者，一般用途的行動系統範例 (也就是，不是專用的) 是一部掌上型電腦。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-194">Alternately, an example of a mobile system that is general purpose (that is, is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="fa8a4-195">雖然在其可程式性方面有所限制，但可以下載新的軟體，並由使用者擴充其功能。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-195">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span> <br/> |
| <span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span><dl> <span data-ttu-id="fa8a4-196"><dt>**中繼器**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-196"><dt>**Repeater**</dt> <dt>18</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span><dl> <span data-ttu-id="fa8a4-197"><dt>**橋接器/**</dt>擴充項 <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-197"><dt>**Bridge/Extender**</dt> <dt>19</dt></span></span> </dl>                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span><dl> <span data-ttu-id="fa8a4-198"><dt>**閘道**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-198"><dt>**Gateway**</dt> <dt>20</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span><dl> <span data-ttu-id="fa8a4-199"><dt>**儲存體 Virtualizer**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-199"><dt>**Storage Virtualizer**</dt> <dt>21</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span><dl> <span data-ttu-id="fa8a4-200"><dt>**Media Library**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-200"><dt>**Media Library**</dt> <dt>22</dt></span></span> </dl>                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span><dl> <span data-ttu-id="fa8a4-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span><dl> <span data-ttu-id="fa8a4-202"><dt>**NAS 頭**</dt> <dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-202"><dt>**NAS Head**</dt> <dt>24</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span><dl> <span data-ttu-id="fa8a4-203"><dt>**獨立的 NAS**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-203"><dt>**Self-contained NAS**</dt> <dt>25</dt></span></span> </dl>                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="UPS"></span><span id="ups"></span><dl> <span data-ttu-id="fa8a4-204"><dt>**UPS**</dt> <dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-204"><dt>**UPS**</dt> <dt>26</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span><dl> <span data-ttu-id="fa8a4-205"><dt>**IP Phone**</dt> <dt>27</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-205"><dt>**IP Phone**</dt> <dt>27</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span><dl> <span data-ttu-id="fa8a4-206"><dt>**管理控制器**</dt> <dt>28</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-206"><dt>**Management Controller**</dt> <dt>28</dt></span></span> </dl>                     | <span data-ttu-id="fa8a4-207">表示此實例代表系統管理專用的專用硬體 (也就是基礎板管理控制器 (BMC) 或服務處理器) 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-207">Indicates this instance represents specialized hardware dedicated to systems management (that is, a Baseboard Management Controller (BMC) or service processor).</span></span> <span data-ttu-id="fa8a4-208">管理控制器的管理範圍通常是包含它的單一受管理系統。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-208">The management scope of a Management Controller is typically a single managed system in which it is contained.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span><dl> <span data-ttu-id="fa8a4-209"><dt>**底座管理員**</dt> <dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-209"><dt>**Chassis Manager**</dt> <dt>29</dt></span></span> </dl>                                             | <span data-ttu-id="fa8a4-210">表示此實例代表專門用來管理 blade 底座和其內含裝置的系統。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-210">Indicates this instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="fa8a4-211">此值會用來代表貨架控制器。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-211">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="fa8a4-212">底座管理員是管理的匯總點，而且可能依賴從屬管理控制器來管理構成部分。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-212">A Chassis Manager is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span> <br/>                                                                                                                                                                                         |
| <span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span><dl> <span data-ttu-id="fa8a4-213">以 <dt>**主機為基礎的 RAID 控制器**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-213"><dt>**Host-based RAID controller**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="fa8a4-214">表示此實例代表主機電腦中包含的 RAID 存放控制器。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-214">Indicates this instance represents a RAID storage controller contained within a host computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span><dl> <span data-ttu-id="fa8a4-215"><dt>**存放裝置主機殼**</dt> <dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-215"><dt>**Storage Device Enclosure**</dt> <dt>31</dt></span></span> </dl>         | <span data-ttu-id="fa8a4-216">表示此實例代表包含存放裝置的主機殼。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-216">Indicates this instance represents an enclosure that contains storage devices.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span><dl> <span data-ttu-id="fa8a4-217"><dt>**桌面**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-217"><dt>**Desktop**</dt> <dt>32</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span><dl> <span data-ttu-id="fa8a4-218"><dt>**膝上型電腦**</dt> <dt>33</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-218"><dt>**Laptop**</dt> <dt>33</dt></span></span> </dl>                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span><dl> <span data-ttu-id="fa8a4-219"><dt>**虛擬磁帶媒體**</dt>櫃 <dt>34</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-219"><dt>**Virtual Tape Library**</dt> <dt>34</dt></span></span> </dl>                         | <span data-ttu-id="fa8a4-220">虛擬程式庫系統的磁帶媒體櫃模擬。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-220">The emulation of a tape library by a Virtual Library System.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span><dl> <span data-ttu-id="fa8a4-221"><dt>**虛擬程式庫系統**</dt> <dt>35</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-221"><dt>**Virtual Library System**</dt> <dt>35</dt></span></span> </dl>                 | <span data-ttu-id="fa8a4-222">使用磁片儲存體來模擬磁帶媒體櫃。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-222">Uses disk storage to emulate tape libraries.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span><dl> <span data-ttu-id="fa8a4-223"><dt>**網路電腦/瘦用戶端**</dt> <dt>36</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-223"><dt>**Network PC/Thin Client**</dt> <dt>36</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span><dl> <span data-ttu-id="fa8a4-224"><dt>**FC 交換器**</dt> <dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-224"><dt>**FC Switch**</dt> <dt>37</dt></span></span> </dl>                                                                     | <span data-ttu-id="fa8a4-225">表示這個實例專門用來切換第2層光纖通道框架。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-225">Indicates this instance is dedicated to switching layer 2 Fibre Channel frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span><dl> <span data-ttu-id="fa8a4-226"><dt>**乙太網路交換器**</dt> <dt>38</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-226"><dt>**Ethernet Switch**</dt> <dt>38</dt></span></span> </dl>                                             | <span data-ttu-id="fa8a4-227">指出此實例專門用來切換第2層 Ethernet 框架。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-227">Indicates this instance is dedicated to switching layer 2 Ethernet frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="fa8a4-228"><dt>**DMTF 保留**</dt>的 <dt>39. 32567</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-228"><dt>**DMTF Reserved**</dt> <dt>39..32567</dt></span></span> </dl>                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="fa8a4-229"><dt>**廠商保留**</dt> <dt>的 32568</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-229"><dt>**Vendor Reserved** </dt> <dt>32568..65535</dt></span></span> </dl>                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="fa8a4-230">**說明**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-230">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-233">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-233">A description of the object.</span></span> <span data-ttu-id="fa8a4-234">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 規劃的虛擬機器」。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-235">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-235">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-236">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-238">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-238">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="fa8a4-239">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-239">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fa8a4-240">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-241">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-241">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-244">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-244">A display name for the object.</span></span> <span data-ttu-id="fa8a4-245">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-246">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-246">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-247">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-249">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-249">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="fa8a4-250">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and can be one of the following values.</span></span>



| <span data-ttu-id="fa8a4-251">值</span><span class="sxs-lookup"><span data-stu-id="fa8a4-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="fa8a4-252">意義</span><span class="sxs-lookup"><span data-stu-id="fa8a4-252">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fa8a4-253"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-253"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="fa8a4-254">系統已關閉。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-254">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="fa8a4-255"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-255"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="fa8a4-256">系統已啟用但離線。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-256">The system is enabled, but offline.</span></span> <span data-ttu-id="fa8a4-257">將會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-257">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fa8a4-258">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-258">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-259">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-261">指定已規劃系統的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-261">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="fa8a4-262">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="fa8a4-263">值</span><span class="sxs-lookup"><span data-stu-id="fa8a4-263">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="fa8a4-264">意義</span><span class="sxs-lookup"><span data-stu-id="fa8a4-264">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fa8a4-265"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-265"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="fa8a4-266">系統已關閉。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-266">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="fa8a4-267"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-267"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="fa8a4-268">系統已啟用但離線。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-268">The system is enabled, but offline.</span></span> <span data-ttu-id="fa8a4-269">將會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-269">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fa8a4-270">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-270">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-271">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-271">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-273">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-273">The current health of the element.</span></span> <span data-ttu-id="fa8a4-274">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-274">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="fa8a4-275">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-275">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="fa8a4-276">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="fa8a4-277">值</span><span class="sxs-lookup"><span data-stu-id="fa8a4-277">Value</span></span>                                                                        | <span data-ttu-id="fa8a4-278">意義</span><span class="sxs-lookup"><span data-stu-id="fa8a4-278">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="fa8a4-279"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-279"><dt>5</dt></span></span> </dl> | <span data-ttu-id="fa8a4-280">健全狀況狀態為 [正常]。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-280">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fa8a4-281">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-281">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-282">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-282">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-284">字串陣列，提供 **OtherIdentifyingInfo** 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-284">An array of strings providing explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="fa8a4-285">這個陣列的每個專案都與 **OtherIdentifyingInfo** 中位於相同索引的專案相關。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-285">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="fa8a4-286">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system) 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-286">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-287">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-287">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-288">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-288">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-290">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-290">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="fa8a4-291">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-292">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-292">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-293">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-295">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-295">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-296">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-296">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fa8a4-297">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-297">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-298">**名稱**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-298">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-299">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-301">限定詞： **Key**、 **Override**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-301">Qualifiers: **Key**, **Override**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-302">繼承的名稱可作為企業環境中系統實例的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-302">The inherited name serves as the key of a system instance in an enterprise environment.</span></span> <span data-ttu-id="fa8a4-303">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system) 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-303">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-304">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-304">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-305">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-307">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-307">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-308">使用子類別的啟發學習法，識別產生系統名稱的方式。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-308">Identifies how the system name was generated, using the heuristic of the subclass.</span></span> <span data-ttu-id="fa8a4-309">系統物件及其衍生型為 CIM 的最上層物件。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-309">The system object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="fa8a4-310">它們提供許多元件的範圍。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-310">They provide the scope for numerous components.</span></span> <span data-ttu-id="fa8a4-311">需要有唯一的系統金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-311">Having unique system keys is required.</span></span> <span data-ttu-id="fa8a4-312">您可以在個別系統子類別中定義啟發式，以嘗試一律產生相同的系統名稱索引鍵。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-312">A heuristic can be defined in individual system subclasses to attempt to always generate the same system name key.</span></span> <span data-ttu-id="fa8a4-313">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system) 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-313">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-314">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-314">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-315">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-317">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-317">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-318">虛擬機器上次開啟、重設或還原後的總時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-318">The total time, in milliseconds, since the virtual machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="fa8a4-319">這次會排除虛擬機器處於暫停狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-319">This time excludes the time the virtual machine was in the paused state.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-321">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-323">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="fa8a4-324">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fa8a4-325">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-327">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-329">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-329">The current statuses of the object.</span></span> <span data-ttu-id="fa8a4-330">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-331">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-331">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-332">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-334">字串，描述當專用陣列包含值2（"Other"）時，系統的專用方式或原因。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-334">A string describing how or why the system is dedicated when the Dedicated array includes the value 2, "Other".</span></span> <span data-ttu-id="fa8a4-335">這個屬性繼承自 CIM 的 [**[ \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 的工作類型] 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-335">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-339">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="fa8a4-340">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-340">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="fa8a4-341">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-341">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-343">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-343">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-345">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-345">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-346">包含系統名稱資訊以外的其他資料，可用來識別非系統名稱。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-346">Contains additional data, beyond system name information, that can be used to identify a ComputerSystem.</span></span> <span data-ttu-id="fa8a4-347">其中一個範例是將光纖通道的全球名稱保存在節點 (WWN) 內。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-347">One example would be to hold the Fibre Channel World-Wide Name (WWN) of a node.</span></span> <span data-ttu-id="fa8a4-348">如果只有光纖通道名稱可供使用，而且是唯一的 (可作為系統金鑰) ，則這個屬性會是 **Null** ，而 WWN 會成為系統金鑰，其資料會放在 **name** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-348">If only the Fibre Channel name is available and is unique (able to be used as the system key), then this property would be **Null** and the WWN would become the system key, its data placed in the **Name** property.</span></span> <span data-ttu-id="fa8a4-349">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system) 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-349">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-350">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-351">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-353">這個屬性會繼承自 [**CIM 的 \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 「工作類型」類別，但不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-353">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class, but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-354">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-354">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-355">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-356">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fa8a4-356">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-357">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-357">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-358">提供如何達到主要系統擁有者的相關資訊 (例如電話號碼、電子郵件地址等) 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-358">A string that provides information on how the primary system owner can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="fa8a4-359">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system) 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-359">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-360">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-360">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-362">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fa8a4-362">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-363">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="fa8a4-363">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-364">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-364">The name of the primary system owner.</span></span> <span data-ttu-id="fa8a4-365">系統擁有者是系統的主要使用者。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-365">The system owner is the primary user of the system.</span></span> <span data-ttu-id="fa8a4-366">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system) 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-366">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-367">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-367">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-368">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-370">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-370">Provides high level status information.</span></span> <span data-ttu-id="fa8a4-371">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-371">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="fa8a4-372">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-372">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fa8a4-373">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-374">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-374">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-375">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-377">執行此虛擬機器的進程識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-377">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="fa8a4-378">此值可用來唯一識別正在執行虛擬機器之系統上的 Vmwp.exe 實例。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-378">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-379">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-379">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-380">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-382">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-382">The last requested or desired state for the element.</span></span> <span data-ttu-id="fa8a4-383">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-383">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="fa8a4-384">系統會提供這個屬性來比較專案的最後一個要求和目前狀態。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-384">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="fa8a4-385">[**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))類別的特定實例可能不支援 **RequestedState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-385">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="fa8a4-386">如果發生這種情況，則會使用值 12 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-386">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="fa8a4-387">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-387">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="fa8a4-388">值</span><span class="sxs-lookup"><span data-stu-id="fa8a4-388">Value</span></span>                                                                         | <span data-ttu-id="fa8a4-389">意義</span><span class="sxs-lookup"><span data-stu-id="fa8a4-389">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="fa8a4-390"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-390"><dt>12</dt></span></span> </dl> | <span data-ttu-id="fa8a4-391">不適用。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-391">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fa8a4-392">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-392">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-393">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-395">指定電腦系統的重設功能。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-395">Specifies the reset capabilities of the computer system.</span></span> <span data-ttu-id="fa8a4-396">這個屬性繼承自 CIM 的 [**[ \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 的工作類型] 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-396">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="fa8a4-397">值</span><span class="sxs-lookup"><span data-stu-id="fa8a4-397">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="fa8a4-398">意義</span><span class="sxs-lookup"><span data-stu-id="fa8a4-398">Meaning</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="fa8a4-399"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-399"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                              |                                                                                                            |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fa8a4-400"><dt>**未知**</dt>的 <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-400"><dt>**Unknown**</dt> <dt>2</dt></span></span> </dl>                                      |                                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fa8a4-401"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-401"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                  | <span data-ttu-id="fa8a4-402">不允許硬體重設。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-402">Hardware reset is not allowed.</span></span> <br/>                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="fa8a4-403"><dt>**已啟用**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-403"><dt>**Enabled**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="fa8a4-404">電腦系統可以使用硬體來重設 (例如，[電源] 和 [重設] 按鈕) 。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-404">The computer system can be reset by using hardware (for example, the power and reset buttons).</span></span> <br/> |
| <span id="Not_Implemented_"></span><span id="not_implemented_"></span><span id="NOT_IMPLEMENTED_"></span><dl> <span data-ttu-id="fa8a4-405"><dt>**未執行**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-405"><dt>**Not Implemented** </dt> <dt>5 </dt></span></span> </dl> |                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="fa8a4-406">**角色**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-406">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-407">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-408">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fa8a4-408">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-409">字串陣列，指定此系統在 managed 環境中扮演的系統管理員定義角色。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-409">An array of strings that specifies the administrator-defined roles this system plays in the managed environment.</span></span> <span data-ttu-id="fa8a4-410">範例可能是「建立8個列印伺服器」或「Boise 使用者目錄」。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-410">Examples might be "Building 8 print server" or "Boise user directories".</span></span> <span data-ttu-id="fa8a4-411">單一系統可能會執行多個角色。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-411">A single system may perform multiple roles.</span></span> <span data-ttu-id="fa8a4-412">系統角色的檢測視圖是藉由具現化系統的特定子類別或子類別中的屬性（或兩者）來定義。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-412">The instrumentation view of the roles of a system is defined by instantiating a specific subclass of system, or by properties in a subclass, or both.</span></span> <span data-ttu-id="fa8a4-413">例如，使用 **專屬** 的和 **OtherDedicatedDescription** 的屬性定義了非實常式序的用途。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-413">For example, the purpose of a ComputerSystem is defined using the **Dedicated** and **OtherDedicatedDescription** properties.</span></span> <span data-ttu-id="fa8a4-414">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system) 類別。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-414">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-415">**狀態**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-416">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-418">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-420">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="fa8a4-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-422">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-422">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="fa8a4-423">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為「服務正在正常執行」。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-424">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-424">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-425">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-425">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-427">上次修改虛擬機器組態檔的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-427">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="fa8a4-428">設定檔會在特定虛擬機器操作期間進行修改，以及新增、修改或移除任何虛擬機器或裝置設定時。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-428">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-429">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-429">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-430">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-430">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-432">專案的已啟用狀態上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-432">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="fa8a4-433">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不受支援。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-433">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fa8a4-434">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-434">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8a4-435">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa8a4-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa8a4-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8a4-437">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-437">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="fa8a4-438">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-438">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="fa8a4-439">值</span><span class="sxs-lookup"><span data-stu-id="fa8a4-439">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="fa8a4-440">意義</span><span class="sxs-lookup"><span data-stu-id="fa8a4-440">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fa8a4-441"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-441"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="fa8a4-442"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-442"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fa8a4-443"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-443"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="fa8a4-444"><dt>**關機**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-444"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="fa8a4-445"><dt>**無變更**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-445"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="fa8a4-446">沒有進行中的轉換。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-446">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="fa8a4-447"><dt>**離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-447"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="fa8a4-448"><dt>**測試**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-448"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="fa8a4-449"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-449"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="fa8a4-450"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-450"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="fa8a4-451"><dt>**重新開機**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-451"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="fa8a4-452"><dt>**重設**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-452"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="fa8a4-453"><dt>**不適用**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-453"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="fa8a4-454">此執行不支援表示進行中的轉換。</span><span class="sxs-lookup"><span data-stu-id="fa8a4-454">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="fa8a4-455">已 <dt>**保留 DMTF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-455"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa8a4-456">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa8a4-456">Requirements</span></span>



| <span data-ttu-id="fa8a4-457">需求</span><span class="sxs-lookup"><span data-stu-id="fa8a4-457">Requirement</span></span> | <span data-ttu-id="fa8a4-458">值</span><span class="sxs-lookup"><span data-stu-id="fa8a4-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8a4-459">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa8a4-459">Minimum supported client</span></span><br/> | <span data-ttu-id="fa8a4-460">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa8a4-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fa8a4-461">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa8a4-461">Minimum supported server</span></span><br/> | <span data-ttu-id="fa8a4-462">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa8a4-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa8a4-463">命名空間</span><span class="sxs-lookup"><span data-stu-id="fa8a4-463">Namespace</span></span><br/>                | <span data-ttu-id="fa8a4-464">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="fa8a4-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fa8a4-465">MOF</span><span class="sxs-lookup"><span data-stu-id="fa8a4-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa8a4-466"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa8a4-467">DLL</span><span class="sxs-lookup"><span data-stu-id="fa8a4-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa8a4-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa8a4-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa8a4-469">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa8a4-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa8a4-470">**CIM \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-470">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="fa8a4-471">**Msvm \_ VirtualSystemManagementService。ImportSystemDefinition 方法**</span><span class="sxs-lookup"><span data-stu-id="fa8a4-471">**Msvm\_VirtualSystemManagementService .ImportSystemDefinition method**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

