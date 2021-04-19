---
description: 代表系結至虛擬乙太網路交換器的擴充元件實例。
ms.assetid: 5b3e26e3-4cb9-47c9-865e-2f3232bbfc8e
title: Msvm_EthernetSwitchExtension 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtension
- Msvm_EthernetSwitchExtension.InstanceID
- Msvm_EthernetSwitchExtension.Caption
- Msvm_EthernetSwitchExtension.Description
- Msvm_EthernetSwitchExtension.ElementName
- Msvm_EthernetSwitchExtension.InstallDate
- Msvm_EthernetSwitchExtension.OperationalStatus
- Msvm_EthernetSwitchExtension.StatusDescriptions
- Msvm_EthernetSwitchExtension.Status
- Msvm_EthernetSwitchExtension.HealthState
- Msvm_EthernetSwitchExtension.CommunicationStatus
- Msvm_EthernetSwitchExtension.DetailedStatus
- Msvm_EthernetSwitchExtension.OperatingStatus
- Msvm_EthernetSwitchExtension.PrimaryStatus
- Msvm_EthernetSwitchExtension.EnabledState
- Msvm_EthernetSwitchExtension.OtherEnabledState
- Msvm_EthernetSwitchExtension.RequestedState
- Msvm_EthernetSwitchExtension.EnabledDefault
- Msvm_EthernetSwitchExtension.TimeOfLastStateChange
- Msvm_EthernetSwitchExtension.AvailableRequestedStates
- Msvm_EthernetSwitchExtension.TransitioningToState
- Msvm_EthernetSwitchExtension.SystemCreationClassName
- Msvm_EthernetSwitchExtension.SystemName
- Msvm_EthernetSwitchExtension.CreationClassName
- Msvm_EthernetSwitchExtension.Name
- Msvm_EthernetSwitchExtension.ExtensionType
- Msvm_EthernetSwitchExtension.Vendor
- Msvm_EthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a6d760737ded1a12cf369ccb3a46595627d8e38e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981059"
---
# <a name="msvm_ethernetswitchextension-class"></a><span data-ttu-id="3c474-103">Msvm \_ EthernetSwitchExtension 類別</span><span class="sxs-lookup"><span data-stu-id="3c474-103">Msvm\_EthernetSwitchExtension class</span></span>

<span data-ttu-id="3c474-104">代表系結至虛擬乙太網路交換器的擴充元件實例。</span><span class="sxs-lookup"><span data-stu-id="3c474-104">Represents an instance of an extension component bound to a virtual Ethernet switch.</span></span>

<span data-ttu-id="3c474-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3c474-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c474-106">語法</span><span class="sxs-lookup"><span data-stu-id="3c474-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtension : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption = "Virtual Switch Extension";
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
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchExtension";
  string   Name;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="3c474-107">成員</span><span class="sxs-lookup"><span data-stu-id="3c474-107">Members</span></span>

<span data-ttu-id="3c474-108">**Msvm \_ EthernetSwitchExtension** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3c474-108">The **Msvm\_EthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="3c474-109">方法</span><span class="sxs-lookup"><span data-stu-id="3c474-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3c474-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3c474-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3c474-111">方法</span><span class="sxs-lookup"><span data-stu-id="3c474-111">Methods</span></span>

<span data-ttu-id="3c474-112">**Msvm \_ EthernetSwitchExtension** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3c474-112">The **Msvm\_EthernetSwitchExtension** class has these methods.</span></span>



| <span data-ttu-id="3c474-113">方法</span><span class="sxs-lookup"><span data-stu-id="3c474-113">Method</span></span>                                                                        | <span data-ttu-id="3c474-114">描述</span><span class="sxs-lookup"><span data-stu-id="3c474-114">Description</span></span>                         |
|:------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="3c474-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3c474-115">**RequestStateChange**</span></span>](msvm-ethernetswitchextension-requeststatechange.md) | <span data-ttu-id="3c474-116">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="3c474-116">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3c474-117">屬性</span><span class="sxs-lookup"><span data-stu-id="3c474-117">Properties</span></span>

<span data-ttu-id="3c474-118">**Msvm \_ EthernetSwitchExtension** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3c474-118">The **Msvm\_EthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c474-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="3c474-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-120">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3c474-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3c474-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-122">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="3c474-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="3c474-123">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="3c474-123">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="3c474-124">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="3c474-124">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="3c474-125">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="3c474-125">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="3c474-126">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3c474-126">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="3c474-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="3c474-127"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="3c474-128"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="3c474-129"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="3c474-130"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="3c474-131"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="3c474-132"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="3c474-133"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="3c474-134"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="3c474-135"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="3c474-136"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="3c474-137">)</span><span class="sxs-lookup"><span data-stu-id="3c474-137">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c474-138">**標題**</span><span class="sxs-lookup"><span data-stu-id="3c474-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-141">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3c474-141">A short description of the object.</span></span> <span data-ttu-id="3c474-142">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「虛擬交換器擴充功能」。</span><span class="sxs-lookup"><span data-stu-id="3c474-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch Extension".</span></span>

</dd> <dt>

<span data-ttu-id="3c474-143">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3c474-143">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c474-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-146">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="3c474-146">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3c474-147">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3c474-147">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3c474-148">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-148">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-149">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3c474-149">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c474-152">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="3c474-152">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3c474-153">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c474-153">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="3c474-154">此屬性一律設定為 "Msvm \_ EthernetSwitchExtension"。</span><span class="sxs-lookup"><span data-stu-id="3c474-154">This property is always set to "Msvm\_EthernetSwitchExtension".</span></span>

</dd> <dt>

<span data-ttu-id="3c474-155">**說明**</span><span class="sxs-lookup"><span data-stu-id="3c474-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-158">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3c474-158">A description of the object.</span></span> <span data-ttu-id="3c474-159">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-160">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3c474-160">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-161">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c474-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-163">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3c474-163">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3c474-164">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3c474-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3c474-165">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-166">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3c474-166">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-169">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3c474-169">A display name for the object.</span></span> <span data-ttu-id="3c474-170">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-171">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="3c474-171">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-172">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c474-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-174">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="3c474-174">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="3c474-175">這個屬性會繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3c474-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3c474-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="3c474-176"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="3c474-177"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3c474-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="3c474-178"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3c474-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3c474-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-180">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c474-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-182">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="3c474-182">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3c474-183">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="3c474-183">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="3c474-184">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3c474-184">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="3c474-185">值</span><span class="sxs-lookup"><span data-stu-id="3c474-185">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="3c474-186">意義</span><span class="sxs-lookup"><span data-stu-id="3c474-186">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="3c474-187"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-187"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="3c474-188"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="3c474-189"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-189"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="3c474-190">元素是或可能正在執行命令、將會處理任何已排入佇列的命令，並將新的要求排入佇列。</span><span class="sxs-lookup"><span data-stu-id="3c474-190">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="3c474-191"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="3c474-192">元素將不會執行命令，而且會卸載任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="3c474-192">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="3c474-193">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-193"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="3c474-194">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="3c474-194">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="3c474-195"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-195"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="3c474-196">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="3c474-196">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="3c474-197"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-197"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="3c474-198">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="3c474-198">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="3c474-199"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="3c474-199"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="3c474-200">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="3c474-200">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="3c474-201"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-201"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="3c474-202">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="3c474-202">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="3c474-203"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-203"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="3c474-204">元素已啟用但處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="3c474-204">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="3c474-205">專案的行為類似于已啟用的狀態，但它只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="3c474-205">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="3c474-206">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="3c474-206">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="3c474-207"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-207"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="3c474-208">元素正在進入已啟用的狀態。</span><span class="sxs-lookup"><span data-stu-id="3c474-208">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="3c474-209">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="3c474-209">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="3c474-210"><dt>**DMTF 保留**</dt>的 <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-210"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="3c474-211">保留的。</span><span class="sxs-lookup"><span data-stu-id="3c474-211">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="3c474-212"><dt>**廠商保留**</dt>的 <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-212"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="3c474-213">保留的。</span><span class="sxs-lookup"><span data-stu-id="3c474-213">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="3c474-214">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="3c474-214">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-215">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="3c474-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-217">指出擴充元件的類型。</span><span class="sxs-lookup"><span data-stu-id="3c474-217">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3c474-218">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="3c474-218">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="3c474-219">**Capture** (1) </span><span class="sxs-lookup"><span data-stu-id="3c474-219">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="3c474-220">**篩選** (2) </span><span class="sxs-lookup"><span data-stu-id="3c474-220">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="3c474-221">**轉送** (3) </span><span class="sxs-lookup"><span data-stu-id="3c474-221">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="3c474-222">**監視** (4) </span><span class="sxs-lookup"><span data-stu-id="3c474-222">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="3c474-223">**原生** (5) </span><span class="sxs-lookup"><span data-stu-id="3c474-223">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3c474-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3c474-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-225">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c474-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-227">指定元素目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="3c474-227">Specifies the current health of the element.</span></span> <span data-ttu-id="3c474-228">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="3c474-228">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="3c474-229">發生重大錯誤時，請檢查事件記錄檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3c474-229">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="3c474-230">**EnabledState** 屬性也可以包含詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3c474-230">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="3c474-231">例如，當磁碟空間不足時， **HealthState** 會設定為25、虛擬機器暫停，而 **EnabledState** 設定為 32768 (暫停) 。</span><span class="sxs-lookup"><span data-stu-id="3c474-231">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="3c474-232">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="3c474-233">值</span><span class="sxs-lookup"><span data-stu-id="3c474-233">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="3c474-234">意義</span><span class="sxs-lookup"><span data-stu-id="3c474-234">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="3c474-235"><dt>**確定**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-235"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="3c474-236">專案完全正常運作，且在正常指令引數內運作，而且沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c474-236">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="3c474-237"><dt>**重大失敗**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-237"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="3c474-238">元素髮生重大失敗。</span><span class="sxs-lookup"><span data-stu-id="3c474-238">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="3c474-239"><dt>**重大失敗**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-239"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="3c474-240">元素沒有作用，而且可能無法復原。</span><span class="sxs-lookup"><span data-stu-id="3c474-240">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="3c474-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3c474-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-242">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3c474-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-244">虛擬機器設定為虛擬機器建立的日期和時間，或針對管理作業系統的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3c474-244">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="3c474-245">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3c474-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c474-249">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="3c474-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3c474-250">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3c474-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3c474-251">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-252">**名稱**</span><span class="sxs-lookup"><span data-stu-id="3c474-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-253">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c474-255">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="3c474-255">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3c474-256">延伸模組元件的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="3c474-256">The unique name of the extension component.</span></span>

</dd> <dt>

<span data-ttu-id="3c474-257">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3c474-257">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-258">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c474-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-260">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3c474-260">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3c474-261">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3c474-261">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3c474-262">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-262">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-263">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3c474-263">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-264">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="3c474-264">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3c474-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-266">陣列，其中包含物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="3c474-266">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="3c474-267">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-268">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="3c474-268">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-269">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-271">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="3c474-271">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="3c474-272">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="3c474-272">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="3c474-273">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3c474-273">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3c474-274">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3c474-274">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-275">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c474-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-277">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="3c474-277">Provides high level status information.</span></span> <span data-ttu-id="3c474-278">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="3c474-278">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="3c474-279">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="3c474-279">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3c474-280">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-281">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3c474-281">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-282">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c474-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-283">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-284">傳遞給 **RequestStateChange** 方法之元素的最後要求或預期狀態，或 12 (不適用) 如果沒有狀態變更正在進行中。</span><span class="sxs-lookup"><span data-stu-id="3c474-284">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="3c474-285">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="3c474-285">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="3c474-286">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="3c474-286">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="3c474-287">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3c474-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-288">**狀態**</span><span class="sxs-lookup"><span data-stu-id="3c474-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-291">指定元素狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="3c474-291">A string that specifies the status of the element.</span></span> <span data-ttu-id="3c474-292">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-293">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3c474-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-294">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3c474-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3c474-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c474-296">限定詞： **ArrayType** ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="3c474-296">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="3c474-297">陣列，其中包含描述對應之 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="3c474-297">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="3c474-298">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="3c474-298">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-299">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3c474-299">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c474-302">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="3c474-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3c474-303">系統建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="3c474-303">The system creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="3c474-304">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3c474-304">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-305">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c474-307">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**Name**") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="3c474-307">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3c474-308">延伸模組實例所系結的虛擬交換器名稱。</span><span class="sxs-lookup"><span data-stu-id="3c474-308">The name of the virtual switch to which the extension instance is bound to.</span></span>

</dd> <dt>

<span data-ttu-id="3c474-309">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3c474-309">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-310">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3c474-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-312">專案的已啟用狀態上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3c474-312">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3c474-313">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3c474-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3c474-314">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="3c474-314">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-315">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3c474-315">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-317">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="3c474-317">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3c474-318">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="3c474-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3c474-319">**廠商**</span><span class="sxs-lookup"><span data-stu-id="3c474-319">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-322">表示提供延伸模組的廠商。</span><span class="sxs-lookup"><span data-stu-id="3c474-322">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="3c474-323">**版本**</span><span class="sxs-lookup"><span data-stu-id="3c474-323">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c474-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3c474-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c474-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3c474-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c474-326">延伸模組的版本，格式為「*主要*」。*次要*"，例如" 2.0 "。</span><span class="sxs-lookup"><span data-stu-id="3c474-326">The version of the extension in a format of "*major*.*minor*", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c474-327">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c474-327">Requirements</span></span>



| <span data-ttu-id="3c474-328">需求</span><span class="sxs-lookup"><span data-stu-id="3c474-328">Requirement</span></span> | <span data-ttu-id="3c474-329">值</span><span class="sxs-lookup"><span data-stu-id="3c474-329">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c474-330">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c474-330">Minimum supported client</span></span><br/> | <span data-ttu-id="3c474-331">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c474-331">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3c474-332">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c474-332">Minimum supported server</span></span><br/> | <span data-ttu-id="3c474-333">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c474-333">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c474-334">命名空間</span><span class="sxs-lookup"><span data-stu-id="3c474-334">Namespace</span></span><br/>                | <span data-ttu-id="3c474-335">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3c474-335">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3c474-336">MOF</span><span class="sxs-lookup"><span data-stu-id="3c474-336">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c474-337"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-337"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c474-338">DLL</span><span class="sxs-lookup"><span data-stu-id="3c474-338">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c474-339"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c474-339"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

