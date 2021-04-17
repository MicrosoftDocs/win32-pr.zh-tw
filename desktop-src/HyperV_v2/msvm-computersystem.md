---
description: 代表實體電腦系統或虛擬機器。
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Msvm_ComputerSystem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557092"
---
# <a name="msvm_computersystem-class"></a><span data-ttu-id="85137-103">Msvm 的 it \_ 類別</span><span class="sxs-lookup"><span data-stu-id="85137-103">Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="85137-104">代表實體電腦系統或虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85137-104">Represents a physical computer system or virtual machine.</span></span>

<span data-ttu-id="85137-105">若要取得 VMMS 的資訊，請使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="85137-105">To retrieve information for the VMMS, use the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="85137-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="85137-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="85137-107">語法</span><span class="sxs-lookup"><span data-stu-id="85137-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
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
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a><span data-ttu-id="85137-108">成員</span><span class="sxs-lookup"><span data-stu-id="85137-108">Members</span></span>

<span data-ttu-id="85137-109">**Msvm 的 \_** 非程式類別有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="85137-109">The **Msvm\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="85137-110">方法</span><span class="sxs-lookup"><span data-stu-id="85137-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="85137-111">屬性</span><span class="sxs-lookup"><span data-stu-id="85137-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="85137-112">方法</span><span class="sxs-lookup"><span data-stu-id="85137-112">Methods</span></span>

<span data-ttu-id="85137-113">**Msvm 的 \_** it 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="85137-113">The **Msvm\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="85137-114">方法</span><span class="sxs-lookup"><span data-stu-id="85137-114">Method</span></span>                                                                                         | <span data-ttu-id="85137-115">描述</span><span class="sxs-lookup"><span data-stu-id="85137-115">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85137-116">**InjectNonMaskableInterrupt**</span><span class="sxs-lookup"><span data-stu-id="85137-116">**InjectNonMaskableInterrupt**</span></span>](injectnonmaskableinterrupt-msvm-computersystem.md)           | <span data-ttu-id="85137-117">將非遮罩式插斷插入虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="85137-117">Injects a non-maskable interrupt into the virtual machine.</span></span> <span data-ttu-id="85137-118">只有代表虛擬機器的 Msvm 同機類別 **\_** 實例才支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="85137-118">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="85137-119">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="85137-119">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                    |
| [<span data-ttu-id="85137-120">**RequestReplicationStateChange**</span><span class="sxs-lookup"><span data-stu-id="85137-120">**RequestReplicationStateChange**</span></span>](msvm-computersystem-requestreplicationstatechange.md)     | <span data-ttu-id="85137-121">要求將虛擬機器的複寫狀態變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="85137-121">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="85137-122">只有代表虛擬機器的 Msvm 同機類別 **\_** 實例才支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="85137-122">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="85137-123">**RequestReplicationStateChangeEx**</span><span class="sxs-lookup"><span data-stu-id="85137-123">**RequestReplicationStateChangeEx**</span></span>](msvm-requestreplicationstatechangeex-computersystem.md) | <span data-ttu-id="85137-124">要求將虛擬機器的複寫狀態變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="85137-124">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="85137-125">只有代表虛擬機器的 Msvm 同機類別 **\_** 實例才支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="85137-125">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="85137-126">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="85137-126">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="85137-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="85137-127">**RequestStateChange**</span></span>](requeststatechange-msvm-computersystem.md)                           | <span data-ttu-id="85137-128">要求變更虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-128">Requests that the state of the virtual machine be changed.</span></span> <span data-ttu-id="85137-129">只有代表虛擬機器的 Msvm 同機類別 **\_** 實例才支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="85137-129">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="85137-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="85137-130">**SetPowerState**</span></span>                                                                              | <span data-ttu-id="85137-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="85137-131">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="85137-132">屬性</span><span class="sxs-lookup"><span data-stu-id="85137-132">Properties</span></span>

<span data-ttu-id="85137-133">**Msvm 的 \_** it 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="85137-133">The **Msvm\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85137-134">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="85137-134">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-135">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="85137-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85137-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-137">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="85137-137">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="85137-138">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="85137-138">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="85137-139">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="85137-139">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="85137-140">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="85137-140">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="85137-141">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="85137-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="85137-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="85137-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85137-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="85137-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85137-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="85137-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85137-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="85137-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="85137-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="85137-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="85137-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="85137-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="85137-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="85137-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="85137-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="85137-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="85137-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="85137-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="85137-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="85137-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="85137-152">)</span><span class="sxs-lookup"><span data-stu-id="85137-152">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85137-153">**標題**</span><span class="sxs-lookup"><span data-stu-id="85137-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-156">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="85137-156">A short description of the object.</span></span> <span data-ttu-id="85137-157">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 類別，而且它將包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="85137-157">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it will contain one of the following values.</span></span>



| <span data-ttu-id="85137-158">值</span><span class="sxs-lookup"><span data-stu-id="85137-158">Value</span></span>                                                                                                | <span data-ttu-id="85137-159">意義</span><span class="sxs-lookup"><span data-stu-id="85137-159">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="85137-160"><dt>「虛擬機器」</dt></span><span class="sxs-lookup"><span data-stu-id="85137-160"><dt>"Virtual Machine"</dt></span></span> </dl>         | <span data-ttu-id="85137-161">實例代表虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85137-161">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="85137-162"><dt>「主控電腦系統」</dt></span><span class="sxs-lookup"><span data-stu-id="85137-162"><dt>"Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="85137-163">實例代表主控電腦。</span><span class="sxs-lookup"><span data-stu-id="85137-163">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="85137-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="85137-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-167">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="85137-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="85137-168">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="85137-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85137-169">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="85137-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85137-170">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="85137-170">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-173">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="85137-173">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="85137-174">這個屬性會繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為「Msvm 的系統組態」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="85137-174">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="85137-175">**專用**</span><span class="sxs-lookup"><span data-stu-id="85137-175">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-176">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="85137-176">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85137-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-178">指出電腦系統是否為特殊用途的系統 (專用於特定用途) ，而不是一般用途的系統。</span><span class="sxs-lookup"><span data-stu-id="85137-178">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="85137-179">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 0 (並非專用) 。</span><span class="sxs-lookup"><span data-stu-id="85137-179">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="85137-180">**說明**</span><span class="sxs-lookup"><span data-stu-id="85137-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-183">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="85137-183">A description of the object.</span></span> <span data-ttu-id="85137-184">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，它會包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="85137-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it will contain one of the following values.</span></span>



| <span data-ttu-id="85137-185">值</span><span class="sxs-lookup"><span data-stu-id="85137-185">Value</span></span>                                                                                                          | <span data-ttu-id="85137-186">意義</span><span class="sxs-lookup"><span data-stu-id="85137-186">Meaning</span></span>                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="85137-187"><dt>「Microsoft 虛擬電腦系統」</dt></span><span class="sxs-lookup"><span data-stu-id="85137-187"><dt>"Microsoft Virtual Computer System"</dt></span></span> </dl> | <span data-ttu-id="85137-188">實例代表虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85137-188">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="85137-189"><dt>「Microsoft 主控電腦系統」</dt></span><span class="sxs-lookup"><span data-stu-id="85137-189"><dt>"Microsoft Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="85137-190">實例代表主控電腦。</span><span class="sxs-lookup"><span data-stu-id="85137-190">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="85137-191">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="85137-191">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-192">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-194">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="85137-194">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="85137-195">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="85137-195">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85137-196">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="85137-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85137-197">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="85137-197">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-200">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="85137-200">A display name for the object.</span></span> <span data-ttu-id="85137-201">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為虛擬機器的電腦顯示名稱或管理作業系統的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="85137-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to the display name of the computer for a virtual machine or the NetBIOS name of the management operating system.</span></span>

</dd> <dt>

<span data-ttu-id="85137-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="85137-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-203">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-205">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="85137-206">這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="85137-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="85137-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="85137-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85137-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="85137-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85137-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="85137-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="85137-210">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="85137-210">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-211">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-213">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-213">The enabled and disabled states of an element.</span></span> <span data-ttu-id="85137-214">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="85137-214">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="85137-215">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 類別，它會設定為 2 (針對實體電腦啟用) ，或針對虛擬機器使用下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="85137-215">This property is inherited from the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class, and it is set to 2 (Enabled) for a physical computer or one of the following values for a virtual machine.</span></span> <span data-ttu-id="85137-216">如需這些狀態的圖形化視圖，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="85137-216">For a graphical view of these states, see Remarks.</span></span>



| <span data-ttu-id="85137-217">值</span><span class="sxs-lookup"><span data-stu-id="85137-217">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="85137-218">意義</span><span class="sxs-lookup"><span data-stu-id="85137-218">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="85137-219"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="85137-219"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="85137-220">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-220">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="85137-221"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="85137-221"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="85137-222"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="85137-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="85137-223">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="85137-223">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="85137-224"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="85137-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="85137-225">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="85137-225">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="85137-226">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="85137-226"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="85137-227">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="85137-227">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="85137-228"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="85137-228"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="85137-229">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="85137-229">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="85137-230"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="85137-230"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="85137-231">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="85137-231">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="85137-232"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="85137-232"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="85137-233">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-233">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="85137-234"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="85137-234"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="85137-235">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="85137-235">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="85137-236"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="85137-236"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="85137-237">元素已啟用但處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="85137-237">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="85137-238">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="85137-238">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="85137-239">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="85137-239">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="85137-240"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="85137-240"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="85137-241">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="85137-241">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="85137-242">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="85137-242">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="85137-243">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="85137-243">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-244">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-246">指定虛擬機器上增強型會話模式的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-246">Specifies the current state of enhanced session mode on the virtual machine.</span></span>

<span data-ttu-id="85137-247">Hyper-v WMI 提供者會在每次 **Msvm \_** 系統類型的 **EnhancedSessionModeState** 變更時引發 [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) 。</span><span class="sxs-lookup"><span data-stu-id="85137-247">The Hyper-V WMI provider raises an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) each time the **EnhancedSessionModeState** of the **Msvm\_ComputerSystem** class changes.</span></span> <span data-ttu-id="85137-248">如果使用中的 vmconnection 會話收到 **\_ \_ InstanceModificationEvent**，則會在使用者啟用該設定時，嘗試切換至增強的會話模式。</span><span class="sxs-lookup"><span data-stu-id="85137-248">If an active vmconnection session receives an **\_\_InstanceModificationEvent**, it attempts to switch to enhanced session mode if the user enabled that setting.</span></span>

<span data-ttu-id="85137-249">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="85137-249">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="85137-250">**EnhancedSessionModeState** 可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="85137-250">**EnhancedSessionModeState** can be one of these values:</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="85137-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**允許和可用** (2) </span><span class="sxs-lookup"><span data-stu-id="85137-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Allowed and available** (2)</span></span>


</dt> <dd>

<span data-ttu-id="85137-252">虛擬機器允許並提供增強模式。</span><span class="sxs-lookup"><span data-stu-id="85137-252">Enhanced mode is allowed and available on the virtual machine.</span></span>

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="85137-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**不允許** (3) </span><span class="sxs-lookup"><span data-stu-id="85137-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not allowed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="85137-254">虛擬機器上不允許增強模式。</span><span class="sxs-lookup"><span data-stu-id="85137-254">Enhanced mode is not allowed on the virtual machine.</span></span>

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="85137-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**允許但無法使用** (6) </span><span class="sxs-lookup"><span data-stu-id="85137-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Allowed but not available** (6)</span></span>


</dt> <dd>

<span data-ttu-id="85137-256">允許使用增強模式，但目前無法在虛擬機器上使用。</span><span class="sxs-lookup"><span data-stu-id="85137-256">Enhanced mode is allowed and but not currently available on the virtual machine.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="85137-257">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="85137-257">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-258">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85137-260">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**") </span><span class="sxs-lookup"><span data-stu-id="85137-260">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="85137-261">在容錯移轉操作期間套用的復原資料點類型。</span><span class="sxs-lookup"><span data-stu-id="85137-261">The type of recovery data point that was applied during the failover operation.</span></span>

> [!Note]  
> <span data-ttu-id="85137-262">從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。</span><span class="sxs-lookup"><span data-stu-id="85137-262">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="85137-263">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="85137-263">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="85137-264">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="85137-264">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="85137-265">**一般** (1) </span><span class="sxs-lookup"><span data-stu-id="85137-265">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="85137-266">**應用程式一致** (2) </span><span class="sxs-lookup"><span data-stu-id="85137-266">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="85137-267">**規劃** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="85137-267">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85137-268">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="85137-268">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-269">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-271">指定元素目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="85137-271">Specifies the current health of the element.</span></span> <span data-ttu-id="85137-272">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="85137-272">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="85137-273">發生重大錯誤時，請檢查事件記錄檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="85137-273">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="85137-274">**EnabledState** 屬性也可以包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="85137-274">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="85137-275">例如，當磁碟空間不足時， **HealthState** 會設定為25、虛擬機器暫停，而 **EnabledState** 設定為 32768 (暫停) 。</span><span class="sxs-lookup"><span data-stu-id="85137-275">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="85137-276">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="85137-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="85137-277">值</span><span class="sxs-lookup"><span data-stu-id="85137-277">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="85137-278">意義</span><span class="sxs-lookup"><span data-stu-id="85137-278">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="85137-279"><dt>**確定**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="85137-279"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="85137-280">虛擬機器完全正常運作，且在正常指令引數內運作，而且沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="85137-280">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="85137-281"><dt>**重大失敗**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="85137-281"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="85137-282">虛擬機器發生重大故障。</span><span class="sxs-lookup"><span data-stu-id="85137-282">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="85137-283">當包含虛擬機器 Vhd 的一或多個磁片的磁碟空間不足，且虛擬機器已暫停時，就會使用此值。</span><span class="sxs-lookup"><span data-stu-id="85137-283">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="85137-284"><dt>**重大失敗**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="85137-284"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="85137-285">元素沒有作用，而且可能無法復原。</span><span class="sxs-lookup"><span data-stu-id="85137-285">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="85137-286">這可能表示虛擬機器 (Vmwp.exe) 的工作者進程沒有回應控制或資訊要求，或是包含虛擬機器 Vhd 的一或多個磁片磁碟空間不足。</span><span class="sxs-lookup"><span data-stu-id="85137-286">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="85137-287">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="85137-287">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-288">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="85137-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85137-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-290">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-290">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85137-291">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="85137-291">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-292">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="85137-292">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85137-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-294">虛擬機器設定為虛擬機器建立的日期和時間，或針對管理作業系統的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-294">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="85137-295">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="85137-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85137-296">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="85137-296">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85137-299">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="85137-299">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="85137-300">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="85137-300">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="85137-301">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="85137-301">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="85137-302">在 Windows 8 中，每個電腦系統或虛擬機器都有單一的 [**ReplicationSettingData**](msvm-replicationsettingdata.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="85137-302">In Windows 8, there is a single instance of [**ReplicationSettingData**](msvm-replicationsettingdata.md) for every computer system or virtual machine.</span></span> <span data-ttu-id="85137-303">針對 Windows 8.1，復原虛擬機器有兩個 **ReplicationSettingData** 實例。</span><span class="sxs-lookup"><span data-stu-id="85137-303">For Windows 8.1, a recovery virtual machine has two instances of **ReplicationSettingData**.</span></span> <span data-ttu-id="85137-304">這種變更會區分設定資料與複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="85137-304">This change differentiates and associates setting data with replication relationship.</span></span>



| <span data-ttu-id="85137-305">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="85137-305">Property name</span></span>  | <span data-ttu-id="85137-306">Windows 8 值</span><span class="sxs-lookup"><span data-stu-id="85137-306">Windows 8 value</span></span>               | <span data-ttu-id="85137-307">Windows 8.1 值</span><span class="sxs-lookup"><span data-stu-id="85137-307">Windows 8.1 value</span></span>                          |
|----------------|-------------------------------|--------------------------------------------|
| <span data-ttu-id="85137-308">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="85137-308">**InstanceID**</span></span> | <span data-ttu-id="85137-309">Microsoft： <vmguid> \\ HVR</span><span class="sxs-lookup"><span data-stu-id="85137-309">Microsoft:<vmguid>\\HVR</span></span> | <span data-ttu-id="85137-310">Microsoft： <vmguid> \\ HVR \\<0/1></span><span class="sxs-lookup"><span data-stu-id="85137-310">Microsoft:<vmguid>\\HVR\\<0/1></span></span> |



 

<span data-ttu-id="85137-311">在 Windows 8.1 值中，0表示 primary，1表示擴充複寫。</span><span class="sxs-lookup"><span data-stu-id="85137-311">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="85137-312">如需擴充複寫的詳細資訊，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)。</span><span class="sxs-lookup"><span data-stu-id="85137-312">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="85137-313">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="85137-313">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-314">資料類型： **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85137-314">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="85137-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85137-316">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**") </span><span class="sxs-lookup"><span data-stu-id="85137-316">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="85137-317">為虛擬機器收到最後一個應用程式一致複寫的時間。</span><span class="sxs-lookup"><span data-stu-id="85137-317">The time at which the last application-consistent replication was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="85137-318">從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。</span><span class="sxs-lookup"><span data-stu-id="85137-318">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="85137-319">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="85137-319">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-320">資料類型： **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85137-320">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="85137-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85137-322">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**") </span><span class="sxs-lookup"><span data-stu-id="85137-322">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="85137-323">復原虛擬機器時，收到最後一次複寫的時間。</span><span class="sxs-lookup"><span data-stu-id="85137-323">The time at which the last replication is received on recovery for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="85137-324">從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。</span><span class="sxs-lookup"><span data-stu-id="85137-324">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="85137-325">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="85137-325">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-326">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85137-328">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**") </span><span class="sxs-lookup"><span data-stu-id="85137-328">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="85137-329">針對虛擬機器所收到的最後一個複寫類型。</span><span class="sxs-lookup"><span data-stu-id="85137-329">The type of the last replication that was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="85137-330">從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。</span><span class="sxs-lookup"><span data-stu-id="85137-330">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="85137-331">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="85137-331">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="85137-332">**無** (0) </span><span class="sxs-lookup"><span data-stu-id="85137-332">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="85137-333">**一般** (1) </span><span class="sxs-lookup"><span data-stu-id="85137-333">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="85137-334">**應用程式一致** (2) </span><span class="sxs-lookup"><span data-stu-id="85137-334">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="85137-335">**規劃** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="85137-335">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85137-336">**LastSuccessfulBackupTime**</span><span class="sxs-lookup"><span data-stu-id="85137-336">**LastSuccessfulBackupTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-337">資料類型： **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85137-337">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="85137-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-339">虛擬機器上一次成功備份的完成時間。</span><span class="sxs-lookup"><span data-stu-id="85137-339">The time at which the last successful backup has completed for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="85137-340">**名稱**</span><span class="sxs-lookup"><span data-stu-id="85137-340">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-341">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-343">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="85137-343">The label by which the object is known.</span></span> <span data-ttu-id="85137-344">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 "*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="85137-344">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="85137-345">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="85137-345">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-348">識別如何產生系統名稱的字串，使用子類別的啟發式法。</span><span class="sxs-lookup"><span data-stu-id="85137-348">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="85137-349">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-349">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85137-350">**NumberOfNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="85137-350">**NumberOfNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-351">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-353">電腦系統 (NUMA) 節點的非統一記憶體存取數量。</span><span class="sxs-lookup"><span data-stu-id="85137-353">The number of nonuniform memory access (NUMA) nodes of the computer system.</span></span> <span data-ttu-id="85137-354">當 **Msvm \_** 的電腦代表主控電腦系統時，此屬性會包含實體 NUMA 節點的計數。</span><span class="sxs-lookup"><span data-stu-id="85137-354">When **Msvm\_ComputerSystem** represents the hosting computer system, this property contains the count of physical NUMA nodes.</span></span> <span data-ttu-id="85137-355">當 **Msvm \_** 的電腦代表虛擬機器時，此屬性包含虛擬 NUMA 節點的數目，這些節點會透過 ACPI 系統資源親和性表格 (SRAT) 呈現給客體作業系統。</span><span class="sxs-lookup"><span data-stu-id="85137-355">When **Msvm\_ComputerSystem** represents a virtual machine, this property contains the number of virtual NUMA nodes that are presented to the guest operating system through the ACPI System Resource Affinity Table (SRAT).</span></span>

</dd> <dt>

<span data-ttu-id="85137-356">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="85137-356">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-357">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="85137-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="85137-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85137-359">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="85137-359">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="85137-360">若為虛擬機器，此屬性會指出電腦上次開啟、重設或還原後的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="85137-360">For the virtual machine, this property indicates the time, in milliseconds, since the machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="85137-361">這次會排除虛擬機器處於暫停狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="85137-361">This time excludes the time the virtual machine was in the paused state.</span></span> <span data-ttu-id="85137-362">若為管理作業系統，這個屬性會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-362">For the management operating system, this property is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85137-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="85137-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-364">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-366">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="85137-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="85137-367">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="85137-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85137-368">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="85137-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85137-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="85137-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-370">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="85137-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85137-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-372">陣列，其中包含物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-372">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="85137-373">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="85137-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="85137-374">位於索引零 (0) 的值是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="85137-374">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="85137-375">值</span><span class="sxs-lookup"><span data-stu-id="85137-375">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="85137-376">意義</span><span class="sxs-lookup"><span data-stu-id="85137-376">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="85137-377"><dt>**確定**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="85137-377"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="85137-378">虛擬機器正常運作，且正常運作。</span><span class="sxs-lookup"><span data-stu-id="85137-378">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="85137-379"><dt>**降級**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="85137-379"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="85137-380">虛擬機器只能部分運作。</span><span class="sxs-lookup"><span data-stu-id="85137-380">The virtual machine is only partially functional.</span></span> <span data-ttu-id="85137-381">這表示無法存取包含設定的儲存體。</span><span class="sxs-lookup"><span data-stu-id="85137-381">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="85137-382">處於此狀態的虛擬機器只能關閉或刪除。</span><span class="sxs-lookup"><span data-stu-id="85137-382">A virtual machine in this state can only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="85137-383"><dt>**預測性失敗**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="85137-383"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="85137-384">虛擬機器可正常運作，但未來可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="85137-384">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="85137-385">這表示包含虛擬機器虛擬硬碟的存放裝置可用空間不足。</span><span class="sxs-lookup"><span data-stu-id="85137-385">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="85137-386">如果沒有可用的磁碟空間，將會暫停虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85137-386">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="85137-387"><dt>**已停止**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="85137-387"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="85137-388">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="85137-388">This value is not supported.</span></span> <span data-ttu-id="85137-389">如果虛擬機器已停止，則 [ **EnabledState** ] 屬性的值會是3， ([已停用]) 。</span><span class="sxs-lookup"><span data-stu-id="85137-389">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="85137-390"><dt>**在服務**</dt> <dt>11</dt>中</span><span class="sxs-lookup"><span data-stu-id="85137-390"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="85137-391">虛擬機器正在處理要求。</span><span class="sxs-lookup"><span data-stu-id="85137-391">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="85137-392"><dt>**休眠**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="85137-392"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="85137-393">不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="85137-393">This value is not supported.</span></span> <span data-ttu-id="85137-394">如果虛擬機器已暫停或暫停，則 [ **EnabledState** ] 屬性的值會是 32769 ([已暫停]) 或 32768 (暫停) 。</span><span class="sxs-lookup"><span data-stu-id="85137-394">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="85137-395">位於索引 1 (1) 的值是選擇性的，並包含次要狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="85137-395">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="85137-396">用戶端應該使用索引零 (0) 的主要狀態，以判斷是否可以將新的要求發行至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85137-396">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="85137-397">如果 **operationalstatus** \[ 0 \] 是 2 (確定) ，則由 **OperationalStatus** 1 指出的作業 \[ \] 可能會中斷。</span><span class="sxs-lookup"><span data-stu-id="85137-397">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="85137-398">在 **OperationalStatus** \[ 1 的值 \] 是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="85137-398">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="85137-399">值</span><span class="sxs-lookup"><span data-stu-id="85137-399">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="85137-400">意義</span><span class="sxs-lookup"><span data-stu-id="85137-400">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="85137-401"><dt>**正在建立快照**</dt>集 <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="85137-401"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="85137-402">正在為虛擬機器建立快照集。</span><span class="sxs-lookup"><span data-stu-id="85137-402">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="85137-403">正在套用 <dt>**快照**</dt>集 <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="85137-403"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="85137-404">正在將快照集套用到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85137-404">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="85137-405"><dt>**正在刪除快照**</dt>集 <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="85137-405"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="85137-406">正在從虛擬機器刪除快照集。</span><span class="sxs-lookup"><span data-stu-id="85137-406">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="85137-407"><dt>**正在等候開始**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="85137-407"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="85137-408">虛擬機器將會在自動啟動延遲經過之後啟動。</span><span class="sxs-lookup"><span data-stu-id="85137-408">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="85137-409"><dt>**合併磁片**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="85137-409"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="85137-410">先前已刪除之快照集的虛擬硬碟正在合併。</span><span class="sxs-lookup"><span data-stu-id="85137-410">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="85137-411"><dt>**正在匯出虛擬機器**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="85137-411"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="85137-412">正在匯出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="85137-412">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="85137-413">正在 <dt>**遷移虛擬機器**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="85137-413"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="85137-414">虛擬機器正在從一部實體電腦即時移轉至另一部電腦。</span><span class="sxs-lookup"><span data-stu-id="85137-414">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="85137-415">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="85137-415">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-416">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="85137-416">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85137-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-418">描述當 **專用** 陣列包含值 2 (其他) 時，如何或為何專用系統的字串。</span><span class="sxs-lookup"><span data-stu-id="85137-418">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="85137-419">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-419">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85137-420">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="85137-420">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-423">當 **EnabledState** 屬性設定為 1 (其他) 時，已啟用或停用虛擬機器的狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-423">The enabled or disabled state of the virtual machine when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="85137-424">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="85137-424">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="85137-425">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-425">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85137-426">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="85137-426">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-427">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="85137-427">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85137-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-429">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-429">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85137-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="85137-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-431">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="85137-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="85137-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-433">這個屬性繼承自 [**CIM 的 \_ 程式**](/windows/desktop/CIMWin32Prov/cim-computersystem)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="85137-433">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85137-434">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="85137-434">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-435">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-435">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-437">指出如何達到主要系統擁有者 (的字串，例如電話號碼或電子郵件地址) 。</span><span class="sxs-lookup"><span data-stu-id="85137-437">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="85137-438">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-438">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85137-439">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="85137-439">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-440">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-442">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="85137-442">The name of the primary system owner.</span></span> <span data-ttu-id="85137-443">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-443">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85137-444">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="85137-444">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-445">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-445">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-447">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="85137-447">Provides high level status information.</span></span> <span data-ttu-id="85137-448">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="85137-448">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="85137-449">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="85137-449">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="85137-450">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="85137-450">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85137-451">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="85137-451">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-452">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="85137-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="85137-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-454">執行此虛擬機器的進程識別碼。</span><span class="sxs-lookup"><span data-stu-id="85137-454">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="85137-455">此值可用來唯一識別正在執行虛擬機器之系統上的 Vmwp.exe 實例。</span><span class="sxs-lookup"><span data-stu-id="85137-455">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="85137-456">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="85137-456">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-457">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-458">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85137-459">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**") </span><span class="sxs-lookup"><span data-stu-id="85137-459">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span></span>
</dt> </dl>

<span data-ttu-id="85137-460">虛擬機器的複寫健全狀況。</span><span class="sxs-lookup"><span data-stu-id="85137-460">The replication health for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="85137-461">從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。</span><span class="sxs-lookup"><span data-stu-id="85137-461">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="85137-462">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="85137-462">Possible values are:</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="85137-463">**不適用** (0) </span><span class="sxs-lookup"><span data-stu-id="85137-463">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="85137-464">**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="85137-464">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="85137-465">**警告** (2) </span><span class="sxs-lookup"><span data-stu-id="85137-465">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="85137-466">**重大** (3) </span><span class="sxs-lookup"><span data-stu-id="85137-466">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85137-467">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="85137-467">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-468">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-468">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-469">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-470">指定虛擬機器的複寫模式。</span><span class="sxs-lookup"><span data-stu-id="85137-470">Specifies the replication mode for the virtual machine.</span></span> <span data-ttu-id="85137-471">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="85137-471">This will be one of the following values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="85137-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (0) </span><span class="sxs-lookup"><span data-stu-id="85137-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="85137-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**主要** (1) </span><span class="sxs-lookup"><span data-stu-id="85137-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="85137-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**複本** (2) </span><span class="sxs-lookup"><span data-stu-id="85137-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replica** (2)</span></span>


</dt> <dd>

<span data-ttu-id="85137-475">復原</span><span class="sxs-lookup"><span data-stu-id="85137-475">Recovery</span></span>

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="85137-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**測試複本** (3) </span><span class="sxs-lookup"><span data-stu-id="85137-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Test Replica** (3)</span></span>


</dt> <dd>

<span data-ttu-id="85137-477">複本</span><span class="sxs-lookup"><span data-stu-id="85137-477">Replica</span></span>

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="85137-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**擴充複本** (4) </span><span class="sxs-lookup"><span data-stu-id="85137-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85137-479">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="85137-479">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-480">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85137-482">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "[**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**") </span><span class="sxs-lookup"><span data-stu-id="85137-482">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span></span>
</dt> </dl>

<span data-ttu-id="85137-483">虛擬機器的複寫狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-483">The replication state for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="85137-484">從 Windows 8.1 開始，這個屬性已被取代。相反地，請在 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) 類別中使用相同名稱的屬性，以取得主要或擴充關聯性的值。</span><span class="sxs-lookup"><span data-stu-id="85137-484">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="85137-485">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="85137-485">Possible values are:</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="85137-486">**停用** (0) </span><span class="sxs-lookup"><span data-stu-id="85137-486">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="85137-487">**準備好** 複寫 (1) </span><span class="sxs-lookup"><span data-stu-id="85137-487">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="85137-488">**等候完成初始** 複寫 (2) </span><span class="sxs-lookup"><span data-stu-id="85137-488">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="85137-489">複寫 **(3**) </span><span class="sxs-lookup"><span data-stu-id="85137-489">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="85137-490">**同步複寫完成** (4) </span><span class="sxs-lookup"><span data-stu-id="85137-490">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="85137-491">已 **復原** (5) </span><span class="sxs-lookup"><span data-stu-id="85137-491">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="85137-492">**認可** (6) </span><span class="sxs-lookup"><span data-stu-id="85137-492">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="85137-493">已 **暫** 止 (7) </span><span class="sxs-lookup"><span data-stu-id="85137-493">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="85137-494">**重大** (8) </span><span class="sxs-lookup"><span data-stu-id="85137-494">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="85137-495">**等候啟動重新同步** (9) </span><span class="sxs-lookup"><span data-stu-id="85137-495">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="85137-496">重新 **同步** 處理 (10) </span><span class="sxs-lookup"><span data-stu-id="85137-496">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="85137-497">**重新同步** 處理已暫停 (11) </span><span class="sxs-lookup"><span data-stu-id="85137-497">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="85137-498">**正在進行容錯移轉** (12) </span><span class="sxs-lookup"><span data-stu-id="85137-498">**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="85137-499">**正在進行容錯回復** (13) </span><span class="sxs-lookup"><span data-stu-id="85137-499">**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="85137-500">容錯 **回復完成** (14) </span><span class="sxs-lookup"><span data-stu-id="85137-500">**Failback complete** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="85137-501">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="85137-501">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-502">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-503">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-504">傳遞給 [**RequestStateChange**](requeststatechange-msvm-computersystem.md) 方法的虛擬機器最後要求或預期狀態，或 12 (不適用) 如果沒有狀態變更正在進行中。</span><span class="sxs-lookup"><span data-stu-id="85137-504">The last requested or desired state for the virtual machine as passed to the [**RequestStateChange**](requeststatechange-msvm-computersystem.md) method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="85137-505">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="85137-505">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="85137-506">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-506">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="85137-507">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="85137-507">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85137-508">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="85137-508">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-509">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-510">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-511">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 1 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="85137-511">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="85137-512">**角色**</span><span class="sxs-lookup"><span data-stu-id="85137-512">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-513">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="85137-513">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85137-514">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-515">字串陣列，描述系統在資訊技術環境中扮演的角色。</span><span class="sxs-lookup"><span data-stu-id="85137-515">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="85137-516">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85137-516">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="85137-517">**狀態**</span><span class="sxs-lookup"><span data-stu-id="85137-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-518">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="85137-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="85137-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-520">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="85137-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="85137-521">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="85137-521">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-522">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="85137-522">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="85137-523">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85137-524">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="85137-524">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="85137-525">陣列，其中包含描述對應之 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="85137-525">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="85137-526">例如，如果服務) 中的 11 (是指派給 **OperationalStatus** \[ 0 的值 \] ，則 **StatusDescriptions** \[ 0 \] 可能會包含虛擬機器處理要求的原因說明。</span><span class="sxs-lookup"><span data-stu-id="85137-526">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="85137-527">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="85137-527">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="85137-528">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="85137-528">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-529">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="85137-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85137-530">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-531">上次修改虛擬機器組態檔的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="85137-531">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="85137-532">設定檔會在特定虛擬機器操作期間進行修改，以及新增、修改或移除任何虛擬機器或裝置設定時。</span><span class="sxs-lookup"><span data-stu-id="85137-532">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="85137-533">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="85137-533">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-534">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="85137-534">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85137-535">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-536">專案的已啟用狀態上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="85137-536">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="85137-537">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="85137-537">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="85137-538">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="85137-538">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85137-539">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="85137-539">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="85137-540">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="85137-540">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="85137-541">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-541">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="85137-542">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="85137-542">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85137-543">備註</span><span class="sxs-lookup"><span data-stu-id="85137-543">Remarks</span></span>

<span data-ttu-id="85137-544">下圖顯示 **EnabledState** 值。</span><span class="sxs-lookup"><span data-stu-id="85137-544">The following illustration shows the **EnabledState** values.</span></span>

![適用于 windows server 2008 r2 之 enabledstate 值的狀態圖表](images/msvm-computersystem-enabledstate-win2008r2.png)

<span data-ttu-id="85137-546">當 Msvm 的系統類型 **\_** 屬性變更時，WMI 提供者會指出描述變更的 [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent)事件。</span><span class="sxs-lookup"><span data-stu-id="85137-546">When a property of the **Msvm\_ComputerSystem** class changes, the WMI provider indicates an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) event that describes the changes.</span></span> <span data-ttu-id="85137-547">先前的狀態是包含在 **PreviousInstance** 屬性中，而新的狀態則包含在 **TargetInstance** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="85137-547">The previous state is contained in the **PreviousInstance** property, and the new state is contained in the **TargetInstance** property.</span></span> <span data-ttu-id="85137-548">這個事件是非同步;處理 **\_ \_ InstanceModificationEvent** 事件時， **TargetInstance** 屬性可能不會反映目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="85137-548">This event is asynchronous; by the time the **\_\_InstanceModificationEvent** event is processed, the **TargetInstance** property may not reflect the current state.</span></span>

<span data-ttu-id="85137-549">UAC 篩選可能會限制對 Msvm 的 [未使用] 類別的存取。 **\_**</span><span class="sxs-lookup"><span data-stu-id="85137-549">Access to the **Msvm\_ComputerSystem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="85137-550">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="85137-550">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="85137-551">範例</span><span class="sxs-lookup"><span data-stu-id="85137-551">Examples</span></span>

<span data-ttu-id="85137-552">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="85137-552">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85137-553">規格需求</span><span class="sxs-lookup"><span data-stu-id="85137-553">Requirements</span></span>



| <span data-ttu-id="85137-554">需求</span><span class="sxs-lookup"><span data-stu-id="85137-554">Requirement</span></span> | <span data-ttu-id="85137-555">值</span><span class="sxs-lookup"><span data-stu-id="85137-555">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85137-556">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85137-556">Minimum supported client</span></span><br/> | <span data-ttu-id="85137-557">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85137-557">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="85137-558">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85137-558">Minimum supported server</span></span><br/> | <span data-ttu-id="85137-559">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="85137-559">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85137-560">命名空間</span><span class="sxs-lookup"><span data-stu-id="85137-560">Namespace</span></span><br/>                | <span data-ttu-id="85137-561">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="85137-561">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="85137-562">MOF</span><span class="sxs-lookup"><span data-stu-id="85137-562">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85137-563"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="85137-563"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85137-564">DLL</span><span class="sxs-lookup"><span data-stu-id="85137-564">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85137-565"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85137-565"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85137-566">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85137-566">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85137-567">**CIM \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="85137-567">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="85137-568">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="85137-568">**\_\_InstanceModificationEvent**</span></span>](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[<span data-ttu-id="85137-569">**CIM \_ 未進行**</span><span class="sxs-lookup"><span data-stu-id="85137-569">**CIM\_ComputerSystem**</span></span>](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[<span data-ttu-id="85137-570">**Msvm) 的， \_ (V1**</span><span class="sxs-lookup"><span data-stu-id="85137-570">**Msvm\_ComputerSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[<span data-ttu-id="85137-571">虛擬系統類別</span><span class="sxs-lookup"><span data-stu-id="85137-571">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

