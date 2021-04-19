---
description: 代表交換器埠的 VLAN 端點。
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Msvm_VLANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5606e18fd1327f17feaac07570e5bf8c0c8eb59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991988"
---
# <a name="msvm_vlanendpoint-class"></a><span data-ttu-id="05750-103">Msvm \_ VLANEndpoint 類別</span><span class="sxs-lookup"><span data-stu-id="05750-103">Msvm\_VLANEndpoint class</span></span>

<span data-ttu-id="05750-104">代表交換器埠的 VLAN 端點。</span><span class="sxs-lookup"><span data-stu-id="05750-104">Represents the VLAN endpoint of a switch port.</span></span> <span data-ttu-id="05750-105">此端點的設定將會變更交換器埠透過交換器傳送 VLAN 封包的方式。</span><span class="sxs-lookup"><span data-stu-id="05750-105">The configuration of this endpoint will change the way the switch port sends VLAN packets through the switch.</span></span>

<span data-ttu-id="05750-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="05750-107">語法</span><span class="sxs-lookup"><span data-stu-id="05750-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
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
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a><span data-ttu-id="05750-108">成員</span><span class="sxs-lookup"><span data-stu-id="05750-108">Members</span></span>

<span data-ttu-id="05750-109">**Msvm \_ VLANEndpoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="05750-109">The **Msvm\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="05750-110">方法</span><span class="sxs-lookup"><span data-stu-id="05750-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="05750-111">屬性</span><span class="sxs-lookup"><span data-stu-id="05750-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="05750-112">方法</span><span class="sxs-lookup"><span data-stu-id="05750-112">Methods</span></span>

<span data-ttu-id="05750-113">**Msvm \_ VLANEndpoint** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="05750-113">The **Msvm\_VLANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="05750-114">方法</span><span class="sxs-lookup"><span data-stu-id="05750-114">Method</span></span>                                                             | <span data-ttu-id="05750-115">描述</span><span class="sxs-lookup"><span data-stu-id="05750-115">Description</span></span>                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="05750-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="05750-116">**RequestStateChange**</span></span>](msvm-vlanendpoint-requeststatechange.md) | <span data-ttu-id="05750-117">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="05750-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="05750-118">屬性</span><span class="sxs-lookup"><span data-stu-id="05750-118">Properties</span></span>

<span data-ttu-id="05750-119">**Msvm \_ VLANEndpoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-119">The **Msvm\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05750-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="05750-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-121">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="05750-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="05750-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-123">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="05750-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="05750-124">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="05750-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="05750-125">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="05750-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="05750-126">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="05750-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="05750-127">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="05750-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="05750-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="05750-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="05750-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="05750-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="05750-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="05750-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="05750-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="05750-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="05750-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="05750-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="05750-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="05750-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="05750-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="05750-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="05750-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="05750-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="05750-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="05750-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="05750-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="05750-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="05750-138">)</span><span class="sxs-lookup"><span data-stu-id="05750-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05750-139">**標題**</span><span class="sxs-lookup"><span data-stu-id="05750-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-140">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="05750-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-142">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="05750-142">A short description of the object.</span></span> <span data-ttu-id="05750-143">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「VLAN 端點」。</span><span class="sxs-lookup"><span data-stu-id="05750-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="05750-144">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="05750-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-145">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-147">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="05750-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="05750-148">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="05750-149">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="05750-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="05750-150">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="05750-150">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-151">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="05750-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-153">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="05750-153">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="05750-154">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)，而且一律設定為 "Msvm \_ VLANEndpoint"。</span><span class="sxs-lookup"><span data-stu-id="05750-154">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VLANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="05750-155">**說明**</span><span class="sxs-lookup"><span data-stu-id="05750-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05750-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-158">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="05750-158">A description of the object.</span></span> <span data-ttu-id="05750-159">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「Microsoft VLAN 端點」。</span><span class="sxs-lookup"><span data-stu-id="05750-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="05750-160">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="05750-160">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-161">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-162">存取類型：僅限寫入</span><span class="sxs-lookup"><span data-stu-id="05750-162">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-163">要求使用的所需 VLAN 模式。</span><span class="sxs-lookup"><span data-stu-id="05750-163">The desired VLAN mode that is requested for use.</span></span> <span data-ttu-id="05750-164">目前的模式是由 **OperationalEndpointMode** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="05750-164">The current mode is given by the **OperationalEndpointMode** property.</span></span> <span data-ttu-id="05750-165">這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。</span><span class="sxs-lookup"><span data-stu-id="05750-165">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="05750-166">值</span><span class="sxs-lookup"><span data-stu-id="05750-166">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="05750-167">意義</span><span class="sxs-lookup"><span data-stu-id="05750-167">Meaning</span></span>                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="05750-168"><dt>**DMTF 保留**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05750-168"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="05750-169"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="05750-169"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="05750-170"><dt>**存取**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="05750-170"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="05750-171">將端點/切換埠置於永久 nontrunking 模式，並協調以將連結轉換成 nontrunk 連結。</span><span class="sxs-lookup"><span data-stu-id="05750-171">Puts the endpoint/switch port into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="05750-172">端點會變成 nontrunk 介面。</span><span class="sxs-lookup"><span data-stu-id="05750-172">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="05750-173"><dt>**動態 Auto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="05750-173"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="05750-174">讓端點能夠將連結轉換為主幹連結。</span><span class="sxs-lookup"><span data-stu-id="05750-174">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="05750-175">如果相鄰介面設定為主幹或理想模式，則端點會變成主幹介面。</span><span class="sxs-lookup"><span data-stu-id="05750-175">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="05750-176"><dt>**動態預期**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="05750-176"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="05750-177">讓端點主動嘗試將連結轉換成主幹連結。</span><span class="sxs-lookup"><span data-stu-id="05750-177">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="05750-178">如果相鄰介面設定為主幹、理想或自動模式，則端點會變成主幹介面。</span><span class="sxs-lookup"><span data-stu-id="05750-178">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="05750-179">所有乙太網路介面的預設交換器埠模式都是動態的。</span><span class="sxs-lookup"><span data-stu-id="05750-179">The default switch-port mode for all Ethernet interfaces is dynamic desirable.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="05750-180"><dt>**主幹**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="05750-180"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="05750-181">將端點置於永久的中繼模式，並協調以將連結轉換成主幹連結。</span><span class="sxs-lookup"><span data-stu-id="05750-181">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="05750-182">即使相鄰介面不是主幹介面，端點仍會變成主幹介面。</span><span class="sxs-lookup"><span data-stu-id="05750-182">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="05750-183"><dt>**Dot1Q**</dt>通道 <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="05750-183"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="05750-184">將介面設定為通道， (nontrunking) 端點/埠連接到具有 802.1 Q 主幹埠的非對稱連結。</span><span class="sxs-lookup"><span data-stu-id="05750-184">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="05750-185">802.1 q 通道是用來維護服務提供者網路間客戶的 VLAN 完整性。</span><span class="sxs-lookup"><span data-stu-id="05750-185">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="05750-186"><dt>**DMTF 保留**</dt>的 <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="05750-186"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="05750-187"><dt>**廠商保留**</dt>的 <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="05750-187"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="05750-188">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="05750-188">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-189">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-191">要求使用的 VLAN 封裝類型。</span><span class="sxs-lookup"><span data-stu-id="05750-191">The type of VLAN encapsulation that is requested for use.</span></span> <span data-ttu-id="05750-192">目前使用的封裝是由 **OperationalVLANTrunkEncapsulation** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="05750-192">The encapsulation currently in use is given by the **OperationalVLANTrunkEncapsulation** property.</span></span> <span data-ttu-id="05750-193">只有當端點以中繼模式運作時，才適用此屬性 (如需其他詳細資料) ，請參閱 **OperationalEndpointMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-193">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="05750-194">此屬性為 2 (不適用)  (也就是端點永遠不會置於中繼模式) 、特定類型 (802.1 Q 或 Cisco ISL) ，或 5 (協商) ，也就是此介面與其鄰近 (之間的協商結果。</span><span class="sxs-lookup"><span data-stu-id="05750-194">This property is either 2 (Not Applicable) (that is, the endpoint will never be placed in a trunking mode), a particular type (802.1Q or Cisco ISL), or 5 (Negotiate) (that is, the result of the negotiation between this interface and its neighbor).</span></span> <span data-ttu-id="05750-195">如果端點不支援協商，則不允許值 5 (協商) 。</span><span class="sxs-lookup"><span data-stu-id="05750-195">The value, 5 (Negotiate) is not allowed if the endpoint does not support negotiation.</span></span> <span data-ttu-id="05750-196">這項功能與硬體和廠商相依。</span><span class="sxs-lookup"><span data-stu-id="05750-196">This capability is hardware and vendor dependent.</span></span> <span data-ttu-id="05750-197">這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。</span><span class="sxs-lookup"><span data-stu-id="05750-197">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="05750-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (0) </span><span class="sxs-lookup"><span data-stu-id="05750-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (0)</span></span>
</dt> <dt>

<span data-ttu-id="05750-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="05750-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="05750-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (2) </span><span class="sxs-lookup"><span data-stu-id="05750-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="05750-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3) </span><span class="sxs-lookup"><span data-stu-id="05750-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="05750-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**CISCO ISL** (4) </span><span class="sxs-lookup"><span data-stu-id="05750-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="05750-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**協商** (5) </span><span class="sxs-lookup"><span data-stu-id="05750-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (5)</span></span>
</dt> <dt>

<span data-ttu-id="05750-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (6 32767) </span><span class="sxs-lookup"><span data-stu-id="05750-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="05750-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (32768 65535) </span><span class="sxs-lookup"><span data-stu-id="05750-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05750-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="05750-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-207">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-209">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-209">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="05750-210">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="05750-211">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="05750-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="05750-212">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="05750-212">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-213">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="05750-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-215">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="05750-215">A display name for the object.</span></span> <span data-ttu-id="05750-216">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="05750-216">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05750-217">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="05750-217">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-218">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-220">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="05750-220">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="05750-221">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="05750-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="05750-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="05750-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-223">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-225">此元素的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="05750-225">The enabled and disabled states of this element.</span></span> <span data-ttu-id="05750-226">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="05750-226">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="05750-227">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="05750-227">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-228">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-230">指出是否已在主幹端點/埠上啟用或停用 GARP VLAN 註冊通訊協定 (GVRP) 。</span><span class="sxs-lookup"><span data-stu-id="05750-230">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint/port.</span></span> <span data-ttu-id="05750-231">除非端點支援 GVRP，否則此屬性為 2 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="05750-231">This property is 2 (Not Applicable) unless GVRP is supported by the endpoint.</span></span> <span data-ttu-id="05750-232">只有當端點以中繼模式運作時，才適用此屬性 (如需其他詳細資料) ，請參閱 **OperationalEndpointMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-232">This property is applicable only when the endpoint is operating in trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="05750-233">這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。</span><span class="sxs-lookup"><span data-stu-id="05750-233">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="05750-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="05750-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="05750-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (2) </span><span class="sxs-lookup"><span data-stu-id="05750-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="05750-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="05750-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="05750-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**已停用** (4 ) </span><span class="sxs-lookup"><span data-stu-id="05750-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Disabled** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05750-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="05750-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-239">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-241">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="05750-241">The current health of the element.</span></span> <span data-ttu-id="05750-242">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="05750-242">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="05750-243">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="05750-243">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="05750-244">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="05750-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="05750-245">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="05750-245">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-246">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="05750-246">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="05750-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-248">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="05750-248">The date and time when the object was installed.</span></span> <span data-ttu-id="05750-249">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且不會使用它。</span><span class="sxs-lookup"><span data-stu-id="05750-249">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="05750-250">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="05750-250">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05750-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05750-253">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="05750-253">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="05750-254">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="05750-254">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="05750-255">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="05750-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="05750-256">**名稱**</span><span class="sxs-lookup"><span data-stu-id="05750-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05750-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-259">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="05750-259">The label by which the object is known.</span></span> <span data-ttu-id="05750-260">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="05750-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="05750-261">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="05750-261">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-262">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-262">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="05750-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-264">為確保 **Name** 屬性的值是唯一的，所選取的命名啟發式。</span><span class="sxs-lookup"><span data-stu-id="05750-264">The naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="05750-265">這個屬性是從 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) 繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="05750-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="05750-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="05750-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-267">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-269">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="05750-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="05750-270">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="05750-271">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="05750-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="05750-272">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="05750-272">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-273">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-275">VLAN 端點的設定模式。</span><span class="sxs-lookup"><span data-stu-id="05750-275">The configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="05750-276">這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。</span><span class="sxs-lookup"><span data-stu-id="05750-276">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="05750-277">值</span><span class="sxs-lookup"><span data-stu-id="05750-277">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="05750-278">意義</span><span class="sxs-lookup"><span data-stu-id="05750-278">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="05750-279"><dt>**DMTF 保留**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05750-279"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="05750-280"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="05750-280"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       | <span data-ttu-id="05750-281">端點不是 VLAN 感知。</span><span class="sxs-lookup"><span data-stu-id="05750-281">The endpoint is not VLAN aware.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="05750-282"><dt>**存取**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="05750-282"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="05750-283">將端點置於永久 nontrunking 模式，並協調以將連結轉換成 nontrunk 連結。</span><span class="sxs-lookup"><span data-stu-id="05750-283">Puts the endpoint into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="05750-284">端點會變成 nontrunk 介面。</span><span class="sxs-lookup"><span data-stu-id="05750-284">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="05750-285"><dt>**動態 Auto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="05750-285"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="05750-286">讓端點能夠將連結轉換為主幹連結。</span><span class="sxs-lookup"><span data-stu-id="05750-286">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="05750-287">如果相鄰介面設定為主幹或理想模式，則端點會變成主幹介面。</span><span class="sxs-lookup"><span data-stu-id="05750-287">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="05750-288"><dt>**動態預期**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="05750-288"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="05750-289">讓端點主動嘗試將連結轉換成主幹連結。</span><span class="sxs-lookup"><span data-stu-id="05750-289">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="05750-290">如果相鄰介面設定為主幹、理想或自動模式，則端點會變成主幹介面。</span><span class="sxs-lookup"><span data-stu-id="05750-290">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="05750-291">這是所有乙太網路介面的預設交換器埠模式。</span><span class="sxs-lookup"><span data-stu-id="05750-291">This is the default switch-port mode for all Ethernet interfaces.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="05750-292"><dt>**主幹**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="05750-292"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="05750-293">將端點置於永久的中繼模式，並協調以將連結轉換成主幹連結。</span><span class="sxs-lookup"><span data-stu-id="05750-293">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="05750-294">即使相鄰介面不是主幹介面，端點仍會變成主幹介面。</span><span class="sxs-lookup"><span data-stu-id="05750-294">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="05750-295"><dt>**Dot1Q**</dt>通道 <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="05750-295"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="05750-296">將介面設定為通道， (nontrunking) 端點/埠連接到具有 802.1 Q 主幹埠的非對稱連結。</span><span class="sxs-lookup"><span data-stu-id="05750-296">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="05750-297">802.1 q 通道是用來維護服務提供者網路間客戶的 VLAN 完整性。</span><span class="sxs-lookup"><span data-stu-id="05750-297">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="05750-298"><dt>**DMTF 保留**</dt>的 <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="05750-298"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="05750-299"><dt>**廠商保留**</dt>的 <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="05750-299"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="05750-300">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="05750-300">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-301">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="05750-301">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="05750-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-303">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="05750-303">The current statuses of the object.</span></span> <span data-ttu-id="05750-304">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="05750-304">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="05750-305">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="05750-305">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-306">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-308">在主幹端點/埠上使用的 VLAN 封裝類型。</span><span class="sxs-lookup"><span data-stu-id="05750-308">The type of VLAN encapsulation in use on a trunk endpoint/port.</span></span> <span data-ttu-id="05750-309">此屬性為 2 (不適用)  (也就是端點未在中繼模式中運作) 、特定類型 (3 802.1 Q 或 4-Cisco ISL) 、5 (協商) ，也就是端點正在協調封裝類型 (。</span><span class="sxs-lookup"><span data-stu-id="05750-309">This property is either 2 (Not Applicable) (that is, the endpoint is not operating in trunking mode), a particular type (3 - 802.1Q or 4 - Cisco ISL), 5 (Negotiate) (that is, the endpoints are negotiating the encapsulation type).</span></span> <span data-ttu-id="05750-310">只有當端點以中繼模式運作時，才適用此屬性 (如需其他詳細資料) ，請參閱 **OperationalEndpointMode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-310">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="05750-311">這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。</span><span class="sxs-lookup"><span data-stu-id="05750-311">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="05750-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="05750-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="05750-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="05750-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="05750-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (2) </span><span class="sxs-lookup"><span data-stu-id="05750-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="05750-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3) </span><span class="sxs-lookup"><span data-stu-id="05750-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="05750-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**CISCO ISL** (4) </span><span class="sxs-lookup"><span data-stu-id="05750-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="05750-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**協商** (5) </span><span class="sxs-lookup"><span data-stu-id="05750-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negotiating** (5)</span></span>
</dt> <dt>

<span data-ttu-id="05750-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** 的 (6 32767) </span><span class="sxs-lookup"><span data-stu-id="05750-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="05750-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (32768 65535) </span><span class="sxs-lookup"><span data-stu-id="05750-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="05750-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="05750-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-321">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="05750-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-323">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="05750-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="05750-324">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="05750-324">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="05750-325">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="05750-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="05750-326">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="05750-326">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-327">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05750-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-329">當 **OperationalEndpointMode** 屬性的值設定為1時，此 vlan 端點所支援的 vlan 端點模型類型 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="05750-329">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the **OperationalEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="05750-330">當 **OperationalEndpointMode** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="05750-330">This property should be set to **Null** when the **OperationalEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="05750-331">這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。</span><span class="sxs-lookup"><span data-stu-id="05750-331">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="05750-332">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="05750-332">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05750-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-335">當 **OperationalVLANTrunkEncapsulation** 屬性的值設定為 1 (其他) 時，此 vlan 端點所支援的 vlan 封裝類型。</span><span class="sxs-lookup"><span data-stu-id="05750-335">The type of VLAN encapsulation that is supported by this VLAN endpoint, when the value of the **OperationalVLANTrunkEncapsulation** property is set to 1 (Other).</span></span> <span data-ttu-id="05750-336">當所需的封裝屬性是1以外的任何值時，這個屬性應該設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="05750-336">This property should be set to **Null** when the desired encapsulation property is any value other than 1.</span></span> <span data-ttu-id="05750-337">這個屬性繼承自 [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)。</span><span class="sxs-lookup"><span data-stu-id="05750-337">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="05750-338">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="05750-338">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-339">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-339">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="05750-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-341">當這個類別的 **型** 別屬性 (或其任何子類別) 設定為 1 (其他) 時，通訊協定端點的類型。</span><span class="sxs-lookup"><span data-stu-id="05750-341">The type of protocol endpoint when the **Type** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="05750-342">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)，一律設為「虛擬乙太網路」。</span><span class="sxs-lookup"><span data-stu-id="05750-342">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="05750-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="05750-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-344">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-346">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="05750-346">Provides high level status information.</span></span> <span data-ttu-id="05750-347">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="05750-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="05750-348">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="05750-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="05750-349">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="05750-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="05750-350">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="05750-350">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-351">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-353">[IANA IFTYPE MIB](https://www.iana.org/assignments/ianaiftype-mib)。</span><span class="sxs-lookup"><span data-stu-id="05750-353">The [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="05750-354">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)，且一律設定為 1 (其他) 。</span><span class="sxs-lookup"><span data-stu-id="05750-354">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="05750-355">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="05750-355">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-356">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-358">這個屬性是從 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) 繼承而來的。</span><span class="sxs-lookup"><span data-stu-id="05750-358">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="05750-359">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="05750-359">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-360">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-362">上次要求或預期的管理服務狀態。</span><span class="sxs-lookup"><span data-stu-id="05750-362">The last requested or desired state for the management service.</span></span> <span data-ttu-id="05750-363">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="05750-363">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="05750-364">值</span><span class="sxs-lookup"><span data-stu-id="05750-364">Value</span></span>                                                                         | <span data-ttu-id="05750-365">意義</span><span class="sxs-lookup"><span data-stu-id="05750-365">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="05750-366"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="05750-366"><dt>12</dt></span></span> </dl> | <span data-ttu-id="05750-367">不適用。</span><span class="sxs-lookup"><span data-stu-id="05750-367">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="05750-368">**狀態**</span><span class="sxs-lookup"><span data-stu-id="05750-368">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-369">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05750-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-371">描述元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="05750-371">Describes the status of the element.</span></span> <span data-ttu-id="05750-372">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="05750-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="05750-373">正常</span><span class="sxs-lookup"><span data-stu-id="05750-373">"OK"</span></span>

<span data-ttu-id="05750-374">錯誤</span><span class="sxs-lookup"><span data-stu-id="05750-374">"Error"</span></span>

<span data-ttu-id="05750-375">降級</span><span class="sxs-lookup"><span data-stu-id="05750-375">"Degraded"</span></span>

<span data-ttu-id="05750-376">不明</span><span class="sxs-lookup"><span data-stu-id="05750-376">"Unknown"</span></span>

<span data-ttu-id="05750-377">「Pred 失敗」</span><span class="sxs-lookup"><span data-stu-id="05750-377">"Pred Fail"</span></span>

<span data-ttu-id="05750-378">入門</span><span class="sxs-lookup"><span data-stu-id="05750-378">"Starting"</span></span>

<span data-ttu-id="05750-379">從而</span><span class="sxs-lookup"><span data-stu-id="05750-379">"Stopping"</span></span>

<span data-ttu-id="05750-380">維護</span><span class="sxs-lookup"><span data-stu-id="05750-380">"Service"</span></span>

<span data-ttu-id="05750-381">強調</span><span class="sxs-lookup"><span data-stu-id="05750-381">"Stressed"</span></span>

<span data-ttu-id="05750-382">"NonRecover"</span><span class="sxs-lookup"><span data-stu-id="05750-382">"NonRecover"</span></span>

<span data-ttu-id="05750-383">「無連絡人」</span><span class="sxs-lookup"><span data-stu-id="05750-383">"No Contact"</span></span>

<span data-ttu-id="05750-384">「遺失通訊」</span><span class="sxs-lookup"><span data-stu-id="05750-384">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="05750-385">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="05750-385">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-386">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="05750-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="05750-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-388">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="05750-388">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="05750-389">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="05750-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="05750-390">**SupportedEndpointModes**</span><span class="sxs-lookup"><span data-stu-id="05750-390">**SupportedEndpointModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-391">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="05750-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="05750-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="05750-393">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) </span><span class="sxs-lookup"><span data-stu-id="05750-393">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="05750-394">此埠所支援的端點模式。</span><span class="sxs-lookup"><span data-stu-id="05750-394">The endpoint modes supported by this port.</span></span>

</dd> <dt>

<span data-ttu-id="05750-395">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="05750-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-396">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05750-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-398">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="05750-398">The creation class name of the scoping system.</span></span> <span data-ttu-id="05750-399">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)，且一律設定為 "Msvm \_ VirtualSwitch"</span><span class="sxs-lookup"><span data-stu-id="05750-399">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VirtualSwitch"</span></span>

</dd> <dt>

<span data-ttu-id="05750-400">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="05750-400">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-401">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="05750-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="05750-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-403">範圍系統的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="05750-403">The system name of the scoping system.</span></span> <span data-ttu-id="05750-404">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。</span><span class="sxs-lookup"><span data-stu-id="05750-404">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="05750-405">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="05750-405">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-406">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="05750-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="05750-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-408">專案的已啟用狀態上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="05750-408">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="05750-409">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不受支援。</span><span class="sxs-lookup"><span data-stu-id="05750-409">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="05750-410">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="05750-410">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05750-411">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="05750-411">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="05750-412">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="05750-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05750-413">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="05750-413">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="05750-414">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="05750-414">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05750-415">備註</span><span class="sxs-lookup"><span data-stu-id="05750-415">Remarks</span></span>

<span data-ttu-id="05750-416">存取 **Msvm \_ VLANEndpoint** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="05750-416">Access to the **Msvm\_VLANEndpoint** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="05750-417">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="05750-417">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="05750-418">範例</span><span class="sxs-lookup"><span data-stu-id="05750-418">Examples</span></span>

<span data-ttu-id="05750-419">請參閱 [查詢網路物件](querying-networking-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="05750-419">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05750-420">規格需求</span><span class="sxs-lookup"><span data-stu-id="05750-420">Requirements</span></span>



| <span data-ttu-id="05750-421">需求</span><span class="sxs-lookup"><span data-stu-id="05750-421">Requirement</span></span> | <span data-ttu-id="05750-422">值</span><span class="sxs-lookup"><span data-stu-id="05750-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05750-423">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="05750-423">Minimum supported client</span></span><br/> | <span data-ttu-id="05750-424">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05750-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="05750-425">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="05750-425">Minimum supported server</span></span><br/> | <span data-ttu-id="05750-426">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="05750-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05750-427">命名空間</span><span class="sxs-lookup"><span data-stu-id="05750-427">Namespace</span></span><br/>                | <span data-ttu-id="05750-428">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="05750-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="05750-429">MOF</span><span class="sxs-lookup"><span data-stu-id="05750-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05750-430"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="05750-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05750-431">DLL</span><span class="sxs-lookup"><span data-stu-id="05750-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05750-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05750-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05750-433">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05750-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05750-434">**CIM \_ VLANEndpoint**</span><span class="sxs-lookup"><span data-stu-id="05750-434">**CIM\_VLANEndpoint**</span></span>](cim-vlanendpoint.md)
</dt> <dt>

[<span data-ttu-id="05750-435">**CIM \_ VLANEndpoint**</span><span class="sxs-lookup"><span data-stu-id="05750-435">**CIM\_VLANEndpoint**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

