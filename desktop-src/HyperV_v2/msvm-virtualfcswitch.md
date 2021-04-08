---
description: 表示虛擬光纖通道參數。
ms.assetid: 4300747b-3ffc-4caf-8f0b-76cab6d2294e
title: Msvm_VirtualFcSwitch 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitch
- Msvm_VirtualFcSwitch.SetPowerState
- Msvm_VirtualFcSwitch.InstanceID
- Msvm_VirtualFcSwitch.Caption
- Msvm_VirtualFcSwitch.Description
- Msvm_VirtualFcSwitch.ElementName
- Msvm_VirtualFcSwitch.InstallDate
- Msvm_VirtualFcSwitch.OperationalStatus
- Msvm_VirtualFcSwitch.StatusDescriptions
- Msvm_VirtualFcSwitch.Status
- Msvm_VirtualFcSwitch.HealthState
- Msvm_VirtualFcSwitch.CommunicationStatus
- Msvm_VirtualFcSwitch.DetailedStatus
- Msvm_VirtualFcSwitch.OperatingStatus
- Msvm_VirtualFcSwitch.PrimaryStatus
- Msvm_VirtualFcSwitch.EnabledState
- Msvm_VirtualFcSwitch.OtherEnabledState
- Msvm_VirtualFcSwitch.RequestedState
- Msvm_VirtualFcSwitch.EnabledDefault
- Msvm_VirtualFcSwitch.TimeOfLastStateChange
- Msvm_VirtualFcSwitch.AvailableRequestedStates
- Msvm_VirtualFcSwitch.TransitioningToState
- Msvm_VirtualFcSwitch.CreationClassName
- Msvm_VirtualFcSwitch.Name
- Msvm_VirtualFcSwitch.PrimaryOwnerName
- Msvm_VirtualFcSwitch.PrimaryOwnerContact
- Msvm_VirtualFcSwitch.Roles
- Msvm_VirtualFcSwitch.NameFormat
- Msvm_VirtualFcSwitch.OtherIdentifyingInfo
- Msvm_VirtualFcSwitch.IdentifyingDescriptions
- Msvm_VirtualFcSwitch.Dedicated
- Msvm_VirtualFcSwitch.OtherDedicatedDescriptions
- Msvm_VirtualFcSwitch.ResetCapability
- Msvm_VirtualFcSwitch.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66c6b7a284a2751b1c9b664428a9c90db9f468a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112292"
---
# <a name="msvm_virtualfcswitch-class"></a><span data-ttu-id="833e6-103">Msvm \_ VirtualFcSwitch 類別</span><span class="sxs-lookup"><span data-stu-id="833e6-103">Msvm\_VirtualFcSwitch class</span></span>

<span data-ttu-id="833e6-104">表示虛擬光纖通道參數。</span><span class="sxs-lookup"><span data-stu-id="833e6-104">Represents a virtual Fibre Channel switch.</span></span> <span data-ttu-id="833e6-105">每個參數都與一個可連接到多個綜合光纖通道埠的實體光纖通道埠相關聯。</span><span class="sxs-lookup"><span data-stu-id="833e6-105">Each switch is associated with one physical Fibre Channel port to which many synthetic Fibre Channel ports can be connected.</span></span> <span data-ttu-id="833e6-106">參數本身並非高度可設定的，而且主要做為預留位置。</span><span class="sxs-lookup"><span data-stu-id="833e6-106">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="833e6-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="833e6-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="833e6-108">語法</span><span class="sxs-lookup"><span data-stu-id="833e6-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitch : CIM_ComputerSystem
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
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="833e6-109">成員</span><span class="sxs-lookup"><span data-stu-id="833e6-109">Members</span></span>

<span data-ttu-id="833e6-110">**Msvm \_ VirtualFcSwitch** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="833e6-110">The **Msvm\_VirtualFcSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="833e6-111">方法</span><span class="sxs-lookup"><span data-stu-id="833e6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="833e6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="833e6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="833e6-113">方法</span><span class="sxs-lookup"><span data-stu-id="833e6-113">Methods</span></span>

<span data-ttu-id="833e6-114">**Msvm \_ VirtualFcSwitch** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="833e6-114">The **Msvm\_VirtualFcSwitch** class has these methods.</span></span>



| <span data-ttu-id="833e6-115">方法</span><span class="sxs-lookup"><span data-stu-id="833e6-115">Method</span></span>                                                                | <span data-ttu-id="833e6-116">描述</span><span class="sxs-lookup"><span data-stu-id="833e6-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="833e6-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="833e6-117">**RequestStateChange**</span></span>](msvm-virtualfcswitch-requeststatechange.md) | <span data-ttu-id="833e6-118">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="833e6-118">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="833e6-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="833e6-119">**SetPowerState**</span></span>                                                     | <span data-ttu-id="833e6-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="833e6-120">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="833e6-121">屬性</span><span class="sxs-lookup"><span data-stu-id="833e6-121">Properties</span></span>

<span data-ttu-id="833e6-122">**Msvm \_ VirtualFcSwitch** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="833e6-122">The **Msvm\_VirtualFcSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="833e6-123">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="833e6-123">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-124">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="833e6-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="833e6-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-126">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="833e6-126">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="833e6-127">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="833e6-127">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="833e6-128">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="833e6-128">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="833e6-129">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="833e6-129">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="833e6-130">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="833e6-130">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="833e6-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="833e6-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="833e6-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="833e6-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="833e6-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="833e6-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="833e6-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="833e6-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="833e6-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="833e6-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="833e6-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="833e6-141">)</span><span class="sxs-lookup"><span data-stu-id="833e6-141">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="833e6-142">**標題**</span><span class="sxs-lookup"><span data-stu-id="833e6-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-145">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="833e6-145">A short description of the object.</span></span> <span data-ttu-id="833e6-146">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="833e6-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-148">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-150">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="833e6-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="833e6-151">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="833e6-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="833e6-152">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="833e6-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="833e6-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="833e6-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="833e6-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="833e6-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="833e6-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="833e6-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="833e6-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="833e6-160">)</span><span class="sxs-lookup"><span data-stu-id="833e6-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="833e6-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="833e6-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-164">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="833e6-164">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="833e6-165">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)。</span><span class="sxs-lookup"><span data-stu-id="833e6-165">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-166">**專用**</span><span class="sxs-lookup"><span data-stu-id="833e6-166">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-167">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="833e6-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="833e6-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-169">指出電腦系統是否為特殊用途的系統 (專用於特定用途) ，而不是一般用途的系統。</span><span class="sxs-lookup"><span data-stu-id="833e6-169">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="833e6-170">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 0 (並非專用) 。</span><span class="sxs-lookup"><span data-stu-id="833e6-170">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-171">**說明**</span><span class="sxs-lookup"><span data-stu-id="833e6-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-174">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="833e6-174">A description of the object.</span></span> <span data-ttu-id="833e6-175">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="833e6-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-177">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-179">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="833e6-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="833e6-180">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="833e6-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="833e6-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="833e6-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="833e6-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="833e6-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="833e6-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="833e6-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="833e6-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="833e6-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="833e6-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="833e6-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="833e6-190">)</span><span class="sxs-lookup"><span data-stu-id="833e6-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="833e6-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="833e6-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-194">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="833e6-194">A display name for the object.</span></span> <span data-ttu-id="833e6-195">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-196">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="833e6-196">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-197">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-199">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="833e6-199">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="833e6-200">這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="833e6-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="833e6-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="833e6-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="833e6-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="833e6-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="833e6-204">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="833e6-204">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-205">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-207">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="833e6-207">The enabled and disabled states of an element.</span></span> <span data-ttu-id="833e6-208">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="833e6-208">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="833e6-209">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="833e6-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-210">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="833e6-210">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-211">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-213">指定元素目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="833e6-213">Specifies the current health of the element.</span></span> <span data-ttu-id="833e6-214">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="833e6-214">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="833e6-215">發生重大錯誤時，請檢查事件記錄檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="833e6-215">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="833e6-216">**EnabledState** 屬性也可以包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="833e6-216">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="833e6-217">例如，當磁碟空間不足時， **HealthState** 會設定為25、虛擬機器暫停，而 **EnabledState** 設定為 32768 (暫停) 。</span><span class="sxs-lookup"><span data-stu-id="833e6-217">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="833e6-218">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="833e6-219">值</span><span class="sxs-lookup"><span data-stu-id="833e6-219">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="833e6-220">意義</span><span class="sxs-lookup"><span data-stu-id="833e6-220">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="833e6-221"><dt>**確定**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="833e6-221"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="833e6-222">專案完全正常運作，且在正常指令引數內運作，而且沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="833e6-222">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="833e6-223"><dt>**重大失敗**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="833e6-223"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="833e6-224">元素髮生重大失敗。</span><span class="sxs-lookup"><span data-stu-id="833e6-224">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="833e6-225"><dt>**重大失敗**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="833e6-225"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="833e6-226">元素無法正常地進行復原，因此可能無法復原。</span><span class="sxs-lookup"><span data-stu-id="833e6-226">The element is nonfunctional and recovery might not be possible.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="833e6-227">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="833e6-227">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-228">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="833e6-228">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="833e6-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-230">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="833e6-230">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="833e6-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="833e6-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-232">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="833e6-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-234">虛擬機器設定為虛擬機器建立的日期和時間，或針對管理作業系統的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="833e6-234">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="833e6-235">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-236">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="833e6-236">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="833e6-239">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="833e6-239">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="833e6-240">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="833e6-240">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="833e6-241">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-241">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-242">**名稱**</span><span class="sxs-lookup"><span data-stu-id="833e6-242">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-245">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="833e6-245">The label by which the object is known.</span></span> <span data-ttu-id="833e6-246">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)。</span><span class="sxs-lookup"><span data-stu-id="833e6-246">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-247">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="833e6-247">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-250">識別如何產生系統名稱的字串，使用子類別的啟發式法。</span><span class="sxs-lookup"><span data-stu-id="833e6-250">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="833e6-251">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="833e6-251">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="833e6-252">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="833e6-252">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-253">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-255">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="833e6-255">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="833e6-256">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="833e6-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="833e6-257">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="833e6-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="833e6-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="833e6-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="833e6-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="833e6-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="833e6-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="833e6-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="833e6-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="833e6-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="833e6-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="833e6-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="833e6-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="833e6-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="833e6-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="833e6-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="833e6-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="833e6-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="833e6-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="833e6-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="833e6-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="833e6-277">)</span><span class="sxs-lookup"><span data-stu-id="833e6-277">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="833e6-278">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="833e6-278">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-279">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="833e6-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="833e6-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-281">陣列，其中包含物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="833e6-281">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="833e6-282">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-283">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="833e6-283">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-284">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="833e6-284">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="833e6-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-286">描述當 **專用** 陣列包含值 2 (其他) 時，如何或為何專用系統的字串。</span><span class="sxs-lookup"><span data-stu-id="833e6-286">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="833e6-287">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="833e6-287">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="833e6-288">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="833e6-288">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-291">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="833e6-291">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="833e6-292">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="833e6-292">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="833e6-293">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="833e6-293">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="833e6-294">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="833e6-294">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-295">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="833e6-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="833e6-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-297">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="833e6-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="833e6-298">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="833e6-298">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-299">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="833e6-299">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="833e6-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-301">這個屬性繼承自 [**CIM 的 \_ 程式**](/windows/desktop/CIMWin32Prov/cim-computersystem)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="833e6-301">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="833e6-302">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="833e6-302">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-305">指出如何達到主要系統擁有者 (的字串，例如電話號碼或電子郵件地址) 。</span><span class="sxs-lookup"><span data-stu-id="833e6-305">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="833e6-306">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="833e6-306">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="833e6-307">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="833e6-307">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-308">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-310">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="833e6-310">The name of the primary system owner.</span></span> <span data-ttu-id="833e6-311">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="833e6-311">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="833e6-312">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="833e6-312">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-313">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-315">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="833e6-315">Provides high level status information.</span></span> <span data-ttu-id="833e6-316">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="833e6-316">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="833e6-317">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="833e6-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="833e6-318">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="833e6-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="833e6-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-320"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="833e6-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="833e6-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="833e6-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="833e6-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="833e6-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="833e6-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="833e6-325">)</span><span class="sxs-lookup"><span data-stu-id="833e6-325">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="833e6-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="833e6-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-327">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-329">傳遞給 **RequestStateChange** 方法之元素的最後要求或預期狀態，或 12 (不適用) 如果沒有狀態變更正在進行中。</span><span class="sxs-lookup"><span data-stu-id="833e6-329">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="833e6-330">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="833e6-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="833e6-331">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="833e6-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="833e6-332">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="833e6-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-333">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="833e6-333">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-334">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-336">這個屬性繼承自 [**CIM 的 \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)程式。</span><span class="sxs-lookup"><span data-stu-id="833e6-336">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-337">**角色**</span><span class="sxs-lookup"><span data-stu-id="833e6-337">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-338">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="833e6-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="833e6-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-340">字串陣列，描述系統在資訊技術環境中扮演的角色。</span><span class="sxs-lookup"><span data-stu-id="833e6-340">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="833e6-341">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="833e6-341">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="833e6-342">**狀態**</span><span class="sxs-lookup"><span data-stu-id="833e6-342">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-343">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="833e6-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-345">指定元素狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="833e6-345">A string that specifies the status of the element.</span></span> <span data-ttu-id="833e6-346">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-346">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-347">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="833e6-347">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-348">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="833e6-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="833e6-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="833e6-350">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="833e6-350">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="833e6-351">陣列，其中包含描述對應之 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="833e6-351">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="833e6-352">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="833e6-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-353">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="833e6-353">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-354">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="833e6-354">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-356">專案的已啟用狀態上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="833e6-356">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="833e6-357">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="833e6-357">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="833e6-358">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="833e6-358">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="833e6-359">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="833e6-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="833e6-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="833e6-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="833e6-361">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="833e6-361">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="833e6-362">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="833e6-362">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="833e6-363">規格需求</span><span class="sxs-lookup"><span data-stu-id="833e6-363">Requirements</span></span>



| <span data-ttu-id="833e6-364">需求</span><span class="sxs-lookup"><span data-stu-id="833e6-364">Requirement</span></span> | <span data-ttu-id="833e6-365">值</span><span class="sxs-lookup"><span data-stu-id="833e6-365">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="833e6-366">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="833e6-366">Minimum supported client</span></span><br/> | <span data-ttu-id="833e6-367">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="833e6-367">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="833e6-368">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="833e6-368">Minimum supported server</span></span><br/> | <span data-ttu-id="833e6-369">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="833e6-369">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="833e6-370">命名空間</span><span class="sxs-lookup"><span data-stu-id="833e6-370">Namespace</span></span><br/>                | <span data-ttu-id="833e6-371">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="833e6-371">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="833e6-372">MOF</span><span class="sxs-lookup"><span data-stu-id="833e6-372">MOF</span></span><br/>                      | <dl> <span data-ttu-id="833e6-373"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="833e6-373"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="833e6-374">DLL</span><span class="sxs-lookup"><span data-stu-id="833e6-374">DLL</span></span><br/>                      | <dl> <span data-ttu-id="833e6-375"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="833e6-375"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

