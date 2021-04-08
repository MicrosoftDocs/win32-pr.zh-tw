---
description: 代表虛擬乙太網路交換器。 每個交換器都有許多不同的埠可連接網路介面卡。 參數本身並非高度可設定的，而且主要做為預留位置。
ms.assetid: 9415477a-9423-40fa-a887-3a93da1374af
title: Msvm_VirtualEthernetSwitch 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitch
- Msvm_VirtualEthernetSwitch.SetPowerState
- Msvm_VirtualEthernetSwitch.InstanceID
- Msvm_VirtualEthernetSwitch.Caption
- Msvm_VirtualEthernetSwitch.Description
- Msvm_VirtualEthernetSwitch.ElementName
- Msvm_VirtualEthernetSwitch.InstallDate
- Msvm_VirtualEthernetSwitch.OperationalStatus
- Msvm_VirtualEthernetSwitch.StatusDescriptions
- Msvm_VirtualEthernetSwitch.Status
- Msvm_VirtualEthernetSwitch.HealthState
- Msvm_VirtualEthernetSwitch.CommunicationStatus
- Msvm_VirtualEthernetSwitch.DetailedStatus
- Msvm_VirtualEthernetSwitch.OperatingStatus
- Msvm_VirtualEthernetSwitch.PrimaryStatus
- Msvm_VirtualEthernetSwitch.EnabledState
- Msvm_VirtualEthernetSwitch.OtherEnabledState
- Msvm_VirtualEthernetSwitch.RequestedState
- Msvm_VirtualEthernetSwitch.EnabledDefault
- Msvm_VirtualEthernetSwitch.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitch.AvailableRequestedStates
- Msvm_VirtualEthernetSwitch.TransitioningToState
- Msvm_VirtualEthernetSwitch.CreationClassName
- Msvm_VirtualEthernetSwitch.Name
- Msvm_VirtualEthernetSwitch.PrimaryOwnerName
- Msvm_VirtualEthernetSwitch.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitch.Roles
- Msvm_VirtualEthernetSwitch.NameFormat
- Msvm_VirtualEthernetSwitch.OtherIdentifyingInfo
- Msvm_VirtualEthernetSwitch.IdentifyingDescriptions
- Msvm_VirtualEthernetSwitch.Dedicated
- Msvm_VirtualEthernetSwitch.OtherDedicatedDescriptions
- Msvm_VirtualEthernetSwitch.ResetCapability
- Msvm_VirtualEthernetSwitch.PowerManagementCapabilities
- Msvm_VirtualEthernetSwitch.MaxVMQOffloads
- Msvm_VirtualEthernetSwitch.MaxIOVOffloads
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1cd916e24a6e34ed6a70002c4988f55810050c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850276"
---
# <a name="msvm_virtualethernetswitch-class"></a><span data-ttu-id="89c4e-105">Msvm \_ VirtualEthernetSwitch 類別</span><span class="sxs-lookup"><span data-stu-id="89c4e-105">Msvm\_VirtualEthernetSwitch class</span></span>

<span data-ttu-id="89c4e-106">代表虛擬乙太網路交換器。</span><span class="sxs-lookup"><span data-stu-id="89c4e-106">Represents a virtual Ethernet switch.</span></span> <span data-ttu-id="89c4e-107">每個交換器都有許多不同的埠可連接網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="89c4e-107">Each switch has many different ports to which network adapters can be attached.</span></span> <span data-ttu-id="89c4e-108">參數本身並非高度可設定的，而且主要做為預留位置。</span><span class="sxs-lookup"><span data-stu-id="89c4e-108">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="89c4e-109">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="89c4e-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c4e-110">語法</span><span class="sxs-lookup"><span data-stu-id="89c4e-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Virtual Switch";
  string   Description = "Microsoft Virtual Switch";
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
  string   CreationClassName = "Msvm_VirtualEthernetSwitch";
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 5;
  uint16   PowerManagementCapabilities[];
  uint32   MaxVMQOffloads;
  uint32   MaxIOVOffloads;
};
```

## <a name="members"></a><span data-ttu-id="89c4e-111">成員</span><span class="sxs-lookup"><span data-stu-id="89c4e-111">Members</span></span>

<span data-ttu-id="89c4e-112">**Msvm \_ VirtualEthernetSwitch** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="89c4e-112">The **Msvm\_VirtualEthernetSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="89c4e-113">方法</span><span class="sxs-lookup"><span data-stu-id="89c4e-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="89c4e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="89c4e-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="89c4e-115">方法</span><span class="sxs-lookup"><span data-stu-id="89c4e-115">Methods</span></span>

<span data-ttu-id="89c4e-116">**Msvm \_ VirtualEthernetSwitch** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="89c4e-116">The **Msvm\_VirtualEthernetSwitch** class has these methods.</span></span>



| <span data-ttu-id="89c4e-117">方法</span><span class="sxs-lookup"><span data-stu-id="89c4e-117">Method</span></span>                                                                      | <span data-ttu-id="89c4e-118">描述</span><span class="sxs-lookup"><span data-stu-id="89c4e-118">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="89c4e-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="89c4e-119">**RequestStateChange**</span></span>](msvm-virtualethernetswitch-requeststatechange.md) | <span data-ttu-id="89c4e-120">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="89c4e-120">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="89c4e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="89c4e-121">**SetPowerState**</span></span>                                                           | <span data-ttu-id="89c4e-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="89c4e-122">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="89c4e-123">屬性</span><span class="sxs-lookup"><span data-stu-id="89c4e-123">Properties</span></span>

<span data-ttu-id="89c4e-124">**Msvm \_ VirtualEthernetSwitch** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="89c4e-124">The **Msvm\_VirtualEthernetSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89c4e-125">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="89c4e-125">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-126">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="89c4e-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-128">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="89c4e-128">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="89c4e-129">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="89c4e-129">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="89c4e-130">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="89c4e-130">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="89c4e-131">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="89c4e-131">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="89c4e-132">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="89c4e-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="89c4e-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="89c4e-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="89c4e-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="89c4e-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="89c4e-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="89c4e-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="89c4e-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="89c4e-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="89c4e-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="89c4e-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="89c4e-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="89c4e-143">)</span><span class="sxs-lookup"><span data-stu-id="89c4e-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89c4e-144">**標題**</span><span class="sxs-lookup"><span data-stu-id="89c4e-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-147">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="89c4e-147">A short description of the object.</span></span> <span data-ttu-id="89c4e-148">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「虛擬交換器」。</span><span class="sxs-lookup"><span data-stu-id="89c4e-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-149">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="89c4e-149">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-150">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-152">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="89c4e-152">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="89c4e-153">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="89c4e-153">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="89c4e-154">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="89c4e-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="89c4e-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="89c4e-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="89c4e-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="89c4e-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="89c4e-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="89c4e-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="89c4e-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="89c4e-162">)</span><span class="sxs-lookup"><span data-stu-id="89c4e-162">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89c4e-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="89c4e-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-166">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="89c4e-166">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="89c4e-167">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 "Msvm \_ VirtualEthernetSwitch"。</span><span class="sxs-lookup"><span data-stu-id="89c4e-167">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-168">**專用**</span><span class="sxs-lookup"><span data-stu-id="89c4e-168">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-169">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="89c4e-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-171">指出電腦系統是否為特殊用途的系統 (專用於特定用途) ，而不是一般用途的系統。</span><span class="sxs-lookup"><span data-stu-id="89c4e-171">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="89c4e-172">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 0 (並非專用) 。</span><span class="sxs-lookup"><span data-stu-id="89c4e-172">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-173">**說明**</span><span class="sxs-lookup"><span data-stu-id="89c4e-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-176">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="89c4e-176">A description of the object.</span></span> <span data-ttu-id="89c4e-177">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft 虛擬交換器」。</span><span class="sxs-lookup"><span data-stu-id="89c4e-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="89c4e-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-179">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-181">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="89c4e-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="89c4e-182">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="89c4e-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="89c4e-183">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="89c4e-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="89c4e-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="89c4e-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="89c4e-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="89c4e-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="89c4e-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="89c4e-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="89c4e-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="89c4e-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="89c4e-192">)</span><span class="sxs-lookup"><span data-stu-id="89c4e-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89c4e-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="89c4e-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-196">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="89c4e-196">A display name for the object.</span></span> <span data-ttu-id="89c4e-197">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="89c4e-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-199">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-201">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="89c4e-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="89c4e-202">這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="89c4e-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="89c4e-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="89c4e-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="89c4e-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="89c4e-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89c4e-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="89c4e-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-207">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-209">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="89c4e-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="89c4e-210">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="89c4e-210">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="89c4e-211">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="89c4e-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-212">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="89c4e-212">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-213">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-215">指定元素目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="89c4e-215">Specifies the current health of the element.</span></span> <span data-ttu-id="89c4e-216">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="89c4e-216">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="89c4e-217">發生重大錯誤時，請檢查事件記錄檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="89c4e-217">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="89c4e-218">**EnabledState** 屬性也可以包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="89c4e-218">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="89c4e-219">例如，當磁碟空間不足時， **HealthState** 會設定為25、虛擬機器暫停，而 **EnabledState** 設定為 32768 (暫停) 。</span><span class="sxs-lookup"><span data-stu-id="89c4e-219">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="89c4e-220">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="89c4e-221">值</span><span class="sxs-lookup"><span data-stu-id="89c4e-221">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="89c4e-222">意義</span><span class="sxs-lookup"><span data-stu-id="89c4e-222">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="89c4e-223"><dt>**確定**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="89c4e-223"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="89c4e-224">專案完全正常運作，且在正常指令引數內運作，而且沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="89c4e-224">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="89c4e-225"><dt>**重大失敗**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="89c4e-225"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="89c4e-226">元素髮生重大失敗。</span><span class="sxs-lookup"><span data-stu-id="89c4e-226">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="89c4e-227"><dt>**重大失敗**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="89c4e-227"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="89c4e-228">元素沒有作用，而且可能無法復原。</span><span class="sxs-lookup"><span data-stu-id="89c4e-228">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="89c4e-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="89c4e-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-230">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89c4e-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-232">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89c4e-232">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-233">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="89c4e-233">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-234">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="89c4e-234">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-236">虛擬機器設定為虛擬機器建立的日期和時間，或針對管理作業系統的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89c4e-236">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="89c4e-237">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-238">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="89c4e-238">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-239">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-241">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="89c4e-241">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-242">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="89c4e-242">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="89c4e-243">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-243">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-244">**MaxIOVOffloads**</span><span class="sxs-lookup"><span data-stu-id="89c4e-244">**MaxIOVOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-245">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="89c4e-245">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-247">此參數上可用的單一根 IO 虛擬化 (SR-IOV) 虛擬函式卸載的最大數目。</span><span class="sxs-lookup"><span data-stu-id="89c4e-247">The maximum number of single root IO virtualization (SR-IOV) virtual function offloads available on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-248">**MaxVMQOffloads**</span><span class="sxs-lookup"><span data-stu-id="89c4e-248">**MaxVMQOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-249">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="89c4e-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-250">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="89c4e-250">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-251"> (VMQ 的虛擬機器佇列數目上限) 卸載此交換器上的埠允許。</span><span class="sxs-lookup"><span data-stu-id="89c4e-251">The maximum number of virtual machine queue (VMQ) offloads allowed for a port on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-252">**名稱**</span><span class="sxs-lookup"><span data-stu-id="89c4e-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-253">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-255">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="89c4e-255">The label by which the object is known.</span></span> <span data-ttu-id="89c4e-256">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 "*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="89c4e-256">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-257">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="89c4e-257">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-260">識別如何產生系統名稱的字串，使用子類別的啟發式法。</span><span class="sxs-lookup"><span data-stu-id="89c4e-260">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="89c4e-261">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89c4e-261">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-262">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="89c4e-262">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-263">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-265">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="89c4e-265">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="89c4e-266">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="89c4e-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="89c4e-267">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="89c4e-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="89c4e-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="89c4e-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="89c4e-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="89c4e-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="89c4e-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="89c4e-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="89c4e-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="89c4e-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="89c4e-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="89c4e-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="89c4e-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="89c4e-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="89c4e-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="89c4e-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="89c4e-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="89c4e-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="89c4e-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="89c4e-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="89c4e-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="89c4e-287">)</span><span class="sxs-lookup"><span data-stu-id="89c4e-287">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89c4e-288">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="89c4e-288">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-289">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="89c4e-289">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-291">陣列，其中包含物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="89c4e-291">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="89c4e-292">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-293">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="89c4e-293">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-294">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89c4e-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-296">描述當 **專用** 陣列包含值 2 (其他) 時，如何或為何專用系統的字串。</span><span class="sxs-lookup"><span data-stu-id="89c4e-296">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="89c4e-297">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89c4e-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-298">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="89c4e-298">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-299">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-301">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="89c4e-301">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="89c4e-302">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="89c4e-302">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="89c4e-303">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89c4e-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-304">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="89c4e-304">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-305">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89c4e-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-307">這個屬性繼承自 [**CIM 的 \_ 程式集**](/windows/desktop/CIMWin32Prov/cim-computersystem)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89c4e-307">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-308">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="89c4e-308">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-309">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="89c4e-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-311">這個屬性繼承自 [**CIM 的 \_ 程式**](/windows/desktop/CIMWin32Prov/cim-computersystem)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="89c4e-311">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-312">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="89c4e-312">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-315">指出如何達到主要系統擁有者 (的字串，例如電話號碼或電子郵件地址) 。</span><span class="sxs-lookup"><span data-stu-id="89c4e-315">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="89c4e-316">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89c4e-316">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-317">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="89c4e-317">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-318">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-320">主要系統擁有者的名稱。</span><span class="sxs-lookup"><span data-stu-id="89c4e-320">The name of the primary system owner.</span></span> <span data-ttu-id="89c4e-321">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89c4e-321">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-322">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="89c4e-322">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-323">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-325">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="89c4e-325">Provides high level status information.</span></span> <span data-ttu-id="89c4e-326">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="89c4e-326">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="89c4e-327">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="89c4e-327">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="89c4e-328">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="89c4e-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="89c4e-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-330"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="89c4e-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="89c4e-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="89c4e-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="89c4e-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="89c4e-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="89c4e-335">)</span><span class="sxs-lookup"><span data-stu-id="89c4e-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89c4e-336">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="89c4e-336">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-337">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-339">傳遞給 **RequestStateChange** 方法之元素的最後要求或預期狀態，或 12 (不適用) 如果沒有狀態變更正在進行中。</span><span class="sxs-lookup"><span data-stu-id="89c4e-339">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="89c4e-340">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="89c4e-340">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="89c4e-341">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="89c4e-341">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="89c4e-342">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="89c4e-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-343">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="89c4e-343">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-344">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-346">這個屬性繼承自 [**CIM 的 \_ 執行程式**](/windows/desktop/CIMWin32Prov/cim-computersystem)，而且一律設定為 5 (不會) 。</span><span class="sxs-lookup"><span data-stu-id="89c4e-346">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 5 (Not implemented).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-347">**角色**</span><span class="sxs-lookup"><span data-stu-id="89c4e-347">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-348">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89c4e-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-350">字串陣列，描述系統在資訊技術環境中扮演的角色。</span><span class="sxs-lookup"><span data-stu-id="89c4e-350">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="89c4e-351">這個屬性繼承自 [**CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)，且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="89c4e-351">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-352">**狀態**</span><span class="sxs-lookup"><span data-stu-id="89c4e-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="89c4e-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-355">指定元素狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="89c4e-355">A string that specifies the status of the element.</span></span> <span data-ttu-id="89c4e-356">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-357">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="89c4e-357">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-358">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="89c4e-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-360">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="89c4e-360">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-361">陣列，其中包含描述對應之 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="89c4e-361">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="89c4e-362">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="89c4e-362">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-363">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="89c4e-363">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-364">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="89c4e-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-366">專案的已啟用狀態上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="89c4e-366">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="89c4e-367">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="89c4e-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="89c4e-368">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="89c4e-368">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c4e-369">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="89c4e-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="89c4e-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="89c4e-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89c4e-371">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="89c4e-371">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="89c4e-372">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="89c4e-372">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89c4e-373">規格需求</span><span class="sxs-lookup"><span data-stu-id="89c4e-373">Requirements</span></span>



| <span data-ttu-id="89c4e-374">需求</span><span class="sxs-lookup"><span data-stu-id="89c4e-374">Requirement</span></span> | <span data-ttu-id="89c4e-375">值</span><span class="sxs-lookup"><span data-stu-id="89c4e-375">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c4e-376">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89c4e-376">Minimum supported client</span></span><br/> | <span data-ttu-id="89c4e-377">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89c4e-377">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="89c4e-378">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89c4e-378">Minimum supported server</span></span><br/> | <span data-ttu-id="89c4e-379">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89c4e-379">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89c4e-380">命名空間</span><span class="sxs-lookup"><span data-stu-id="89c4e-380">Namespace</span></span><br/>                | <span data-ttu-id="89c4e-381">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="89c4e-381">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="89c4e-382">MOF</span><span class="sxs-lookup"><span data-stu-id="89c4e-382">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89c4e-383"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="89c4e-383"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89c4e-384">DLL</span><span class="sxs-lookup"><span data-stu-id="89c4e-384">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89c4e-385"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89c4e-385"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

