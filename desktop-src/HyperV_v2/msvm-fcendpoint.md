---
description: 代表光纖通道埠的邏輯連接點。
ms.assetid: 54e9cb76-04f2-417b-b250-1b3156772694
title: Msvm_FcEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcEndpoint
- Msvm_FcEndpoint.InstanceID
- Msvm_FcEndpoint.Caption
- Msvm_FcEndpoint.Description
- Msvm_FcEndpoint.ElementName
- Msvm_FcEndpoint.InstallDate
- Msvm_FcEndpoint.Name
- Msvm_FcEndpoint.OperationalStatus
- Msvm_FcEndpoint.StatusDescriptions
- Msvm_FcEndpoint.Status
- Msvm_FcEndpoint.HealthState
- Msvm_FcEndpoint.CommunicationStatus
- Msvm_FcEndpoint.DetailedStatus
- Msvm_FcEndpoint.OperatingStatus
- Msvm_FcEndpoint.PrimaryStatus
- Msvm_FcEndpoint.EnabledState
- Msvm_FcEndpoint.OtherEnabledState
- Msvm_FcEndpoint.RequestedState
- Msvm_FcEndpoint.EnabledDefault
- Msvm_FcEndpoint.TimeOfLastStateChange
- Msvm_FcEndpoint.AvailableRequestedStates
- Msvm_FcEndpoint.TransitioningToState
- Msvm_FcEndpoint.SystemCreationClassName
- Msvm_FcEndpoint.SystemName
- Msvm_FcEndpoint.CreationClassName
- Msvm_FcEndpoint.NameFormat
- Msvm_FcEndpoint.ProtocolType
- Msvm_FcEndpoint.ProtocolIFType
- Msvm_FcEndpoint.OtherTypeDescription
- Msvm_FcEndpoint.Connected
- Msvm_FcEndpoint.WWPN
- Msvm_FcEndpoint.WWNN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b28136cfc4f0afcf84b5f53ade4976760c997e36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511889"
---
# <a name="msvm_fcendpoint-class"></a><span data-ttu-id="2f412-103">Msvm \_ FcEndpoint 類別</span><span class="sxs-lookup"><span data-stu-id="2f412-103">Msvm\_FcEndpoint class</span></span>

<span data-ttu-id="2f412-104">代表光纖通道埠的邏輯連接點。</span><span class="sxs-lookup"><span data-stu-id="2f412-104">Represents the logical connection point for a Fibre Channel port.</span></span> <span data-ttu-id="2f412-105">當光纖通道端點連線到交換器埠時，連線至光纖通道端點的光纖通道埠會光纖通道連線。</span><span class="sxs-lookup"><span data-stu-id="2f412-105">When the Fibre Channel endpoint is connected to a switch port, the Fibre Channel port connected to the Fibre Channel endpoint has Fibre Channel connectivity.</span></span>

<span data-ttu-id="2f412-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f412-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f412-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f412-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcEndpoint : CIM_ProtocolEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  boolean  Connected;
  string   WWPN;
  string   WWNN;
};
```

## <a name="members"></a><span data-ttu-id="2f412-108">成員</span><span class="sxs-lookup"><span data-stu-id="2f412-108">Members</span></span>

<span data-ttu-id="2f412-109">**Msvm \_ FcEndpoint** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2f412-109">The **Msvm\_FcEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="2f412-110">方法</span><span class="sxs-lookup"><span data-stu-id="2f412-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2f412-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2f412-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2f412-112">方法</span><span class="sxs-lookup"><span data-stu-id="2f412-112">Methods</span></span>

<span data-ttu-id="2f412-113">**Msvm \_ FcEndpoint** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2f412-113">The **Msvm\_FcEndpoint** class has these methods.</span></span>



| <span data-ttu-id="2f412-114">方法</span><span class="sxs-lookup"><span data-stu-id="2f412-114">Method</span></span>                                                           | <span data-ttu-id="2f412-115">描述</span><span class="sxs-lookup"><span data-stu-id="2f412-115">Description</span></span>                         |
|:-----------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="2f412-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2f412-116">**RequestStateChange**</span></span>](msvm-fcendpoint-requeststatechange.md) | <span data-ttu-id="2f412-117">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="2f412-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2f412-118">屬性</span><span class="sxs-lookup"><span data-stu-id="2f412-118">Properties</span></span>

<span data-ttu-id="2f412-119">**Msvm \_ FcEndpoint** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2f412-119">The **Msvm\_FcEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f412-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2f412-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-121">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2f412-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f412-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-123">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="2f412-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="2f412-124">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))類別之目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="2f412-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class.</span></span> <span data-ttu-id="2f412-125">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="2f412-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="2f412-126">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2f412-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="2f412-127">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="2f412-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2f412-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="2f412-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="2f412-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="2f412-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="2f412-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="2f412-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="2f412-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="2f412-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="2f412-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="2f412-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="2f412-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="2f412-138">)</span><span class="sxs-lookup"><span data-stu-id="2f412-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2f412-139">**標題**</span><span class="sxs-lookup"><span data-stu-id="2f412-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-142">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="2f412-142">A short description of the object.</span></span> <span data-ttu-id="2f412-143">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-144">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2f412-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-145">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-147">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="2f412-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2f412-148">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="2f412-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2f412-149">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-150">**已連接**</span><span class="sxs-lookup"><span data-stu-id="2f412-150">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-151">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f412-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-153">如果這個光纖通道端點主動連線到另一個光纖通道端點，這個屬性會設定為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="2f412-153">This property is set to **True** if this Fibre Channel endpoint is actively connected to another Fibre Channel endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="2f412-154">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2f412-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f412-157">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="2f412-157">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2f412-158">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f412-158">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2f412-159">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。</span><span class="sxs-lookup"><span data-stu-id="2f412-159">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-160">**說明**</span><span class="sxs-lookup"><span data-stu-id="2f412-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-163">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="2f412-163">A description of the object.</span></span> <span data-ttu-id="2f412-164">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-165">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2f412-165">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-166">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-168">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2f412-168">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2f412-169">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="2f412-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2f412-170">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2f412-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-174">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="2f412-174">A display name for the object.</span></span> <span data-ttu-id="2f412-175">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-176">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2f412-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-177">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-179">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="2f412-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="2f412-180">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2f412-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2f412-181"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="2f412-181"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-182"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="2f412-182"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-183"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**已啟用但離線** (6) </span><span class="sxs-lookup"><span data-stu-id="2f412-183"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2f412-184">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2f412-184">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-185">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-187">指定已規劃系統的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="2f412-187">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="2f412-188">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="2f412-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="2f412-189">值</span><span class="sxs-lookup"><span data-stu-id="2f412-189">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="2f412-190">意義</span><span class="sxs-lookup"><span data-stu-id="2f412-190">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2f412-191"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2f412-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="2f412-192">系統已關閉。</span><span class="sxs-lookup"><span data-stu-id="2f412-192">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="2f412-193"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2f412-193"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="2f412-194">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="2f412-194">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="2f412-195"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2f412-195"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="2f412-196">系統已啟用但離線。</span><span class="sxs-lookup"><span data-stu-id="2f412-196">The system is enabled, but offline.</span></span> <span data-ttu-id="2f412-197">將會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="2f412-197">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2f412-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2f412-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-199">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-201">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="2f412-201">The current health of the element.</span></span> <span data-ttu-id="2f412-202">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="2f412-202">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="2f412-203">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2f412-203">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="2f412-204">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-205">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2f412-205">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-206">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2f412-206">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-208">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="2f412-208">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="2f412-209">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2f412-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f412-213">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="2f412-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2f412-214">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2f412-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2f412-215">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-216">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2f412-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-219">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="2f412-219">The label by which the object is known.</span></span> <span data-ttu-id="2f412-220">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-221">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="2f412-221">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f412-224">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="2f412-224">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2f412-225">包含已選取的命名啟發式，以確保 **Name** 屬性的值是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2f412-225">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="2f412-226">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。</span><span class="sxs-lookup"><span data-stu-id="2f412-226">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-227">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2f412-227">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-228">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-230">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2f412-230">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2f412-231">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="2f412-231">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2f412-232">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-233">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2f412-233">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-234">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2f412-234">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f412-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-236">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="2f412-236">The current statuses of the object.</span></span> <span data-ttu-id="2f412-237">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-238">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2f412-238">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-239">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-241">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="2f412-241">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="2f412-242">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2f412-242">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="2f412-243">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f412-243">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2f412-244">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="2f412-244">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-245">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f412-247">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="2f412-247">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2f412-248">描述當這個類別的 **ProtocolIFType** 屬性 (或其任何子類別) 設定為 1 (其他) 時，通訊協定端點型別的字串。</span><span class="sxs-lookup"><span data-stu-id="2f412-248">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="2f412-249">當 **ProtocolIFType** 屬性是1以外的任何值時，這個屬性應該設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2f412-249">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="2f412-250">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。</span><span class="sxs-lookup"><span data-stu-id="2f412-250">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-251">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2f412-251">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-252">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-254">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="2f412-254">Provides high level status information.</span></span> <span data-ttu-id="2f412-255">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="2f412-255">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="2f412-256">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="2f412-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2f412-257">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-258">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="2f412-258">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-259">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-261">屬性是用來分類和分類這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="2f412-261">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="2f412-262">如果 **ProtocolIFType** 設定為 1 (其他) ，則應該在 **OtherTypeDescription** 屬性中提供類型資訊。</span><span class="sxs-lookup"><span data-stu-id="2f412-262">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="2f412-263">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。</span><span class="sxs-lookup"><span data-stu-id="2f412-263">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="2f412-264">**ProtocolIFType** 是與 [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib)同步的列舉。</span><span class="sxs-lookup"><span data-stu-id="2f412-264">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="2f412-265">也會包含其他以 DMTF 定義的值。</span><span class="sxs-lookup"><span data-stu-id="2f412-265">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="2f412-266"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2f412-266"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2f412-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-268"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**一般 1822** (2) </span><span class="sxs-lookup"><span data-stu-id="2f412-268"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-269"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3) </span><span class="sxs-lookup"><span data-stu-id="2f412-269"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-270"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN** (4) </span><span class="sxs-lookup"><span data-stu-id="2f412-270"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X.25** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-271"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5) </span><span class="sxs-lookup"><span data-stu-id="2f412-271"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X.25** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-272"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**ETHERNET CSMA/CD** (6) </span><span class="sxs-lookup"><span data-stu-id="2f412-272"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-273"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7) </span><span class="sxs-lookup"><span data-stu-id="2f412-273"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-274"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 權杖匯流排** (8) </span><span class="sxs-lookup"><span data-stu-id="2f412-274"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 Token Bus** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-275"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 權杖環** (9) </span><span class="sxs-lookup"><span data-stu-id="2f412-275"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 Token Ring** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-276"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10) </span><span class="sxs-lookup"><span data-stu-id="2f412-276"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-277"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11) </span><span class="sxs-lookup"><span data-stu-id="2f412-277"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-278"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12) </span><span class="sxs-lookup"><span data-stu-id="2f412-278"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-279"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13) </span><span class="sxs-lookup"><span data-stu-id="2f412-279"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-280"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14) </span><span class="sxs-lookup"><span data-stu-id="2f412-280"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-281"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15) </span><span class="sxs-lookup"><span data-stu-id="2f412-281"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-282"><span id="LAP-B"></span><span id="lap-b"></span>**膝上-B** (16) </span><span class="sxs-lookup"><span data-stu-id="2f412-282"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-283"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17) </span><span class="sxs-lookup"><span data-stu-id="2f412-283"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-284"><span id="DS1"></span><span id="ds1"></span>**DS1** (18) </span><span class="sxs-lookup"><span data-stu-id="2f412-284"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-285"><span id="E1"></span><span id="e1"></span>**E1** (19) </span><span class="sxs-lookup"><span data-stu-id="2f412-285"><span id="E1"></span><span id="e1"></span>**E1** (19)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-286"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**基本 ISDN** (20) </span><span class="sxs-lookup"><span data-stu-id="2f412-286"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Basic ISDN** (20)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-287"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**主要 ISDN** (21) </span><span class="sxs-lookup"><span data-stu-id="2f412-287"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primary ISDN** (21)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-288"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**專屬點對點序列** (22) </span><span class="sxs-lookup"><span data-stu-id="2f412-288"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietary Point-to-Point Serial** (22)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-289"><span id="PPP"></span><span id="ppp"></span>**PPP** (23) </span><span class="sxs-lookup"><span data-stu-id="2f412-289"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-290"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**軟體回送** (24) </span><span class="sxs-lookup"><span data-stu-id="2f412-290"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software Loopback** (24)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-291"><span id="EON"></span><span id="eon"></span>**EON** (25) </span><span class="sxs-lookup"><span data-stu-id="2f412-291"><span id="EON"></span><span id="eon"></span>**EON** (25)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-292"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26) </span><span class="sxs-lookup"><span data-stu-id="2f412-292"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-293"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27) </span><span class="sxs-lookup"><span data-stu-id="2f412-293"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-294"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28) </span><span class="sxs-lookup"><span data-stu-id="2f412-294"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-295"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29) </span><span class="sxs-lookup"><span data-stu-id="2f412-295"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-296"><span id="DS3"></span><span id="ds3"></span>**DS3** (30) </span><span class="sxs-lookup"><span data-stu-id="2f412-296"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-297"><span id="SIP"></span><span id="sip"></span>**SIP** (31) </span><span class="sxs-lookup"><span data-stu-id="2f412-297"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-298"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**框架轉送** (32) </span><span class="sxs-lookup"><span data-stu-id="2f412-298"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-299"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33) </span><span class="sxs-lookup"><span data-stu-id="2f412-299"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-300"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**平行** (34) </span><span class="sxs-lookup"><span data-stu-id="2f412-300"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-301"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35) </span><span class="sxs-lookup"><span data-stu-id="2f412-301"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-302"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36) </span><span class="sxs-lookup"><span data-stu-id="2f412-302"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-303"><span id="ATM"></span><span id="atm"></span>**ATM** (37) </span><span class="sxs-lookup"><span data-stu-id="2f412-303"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-304"><span id="MIO_X.25"></span><span id="mio_x.25"></span>MIO (38) **的**</span><span class="sxs-lookup"><span data-stu-id="2f412-304"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**MIO X.25** (38)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-305"><span id="SONET"></span><span id="sonet"></span>**SONET** (39) </span><span class="sxs-lookup"><span data-stu-id="2f412-305"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-306"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**PLE** (40) </span><span class="sxs-lookup"><span data-stu-id="2f412-306"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X.25 PLE** (40)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-307"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211 c** (41) </span><span class="sxs-lookup"><span data-stu-id="2f412-307"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211c** (41)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-308"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42) </span><span class="sxs-lookup"><span data-stu-id="2f412-308"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-309"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43) </span><span class="sxs-lookup"><span data-stu-id="2f412-309"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-310"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**框架轉送服務** (44) </span><span class="sxs-lookup"><span data-stu-id="2f412-310"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay Service** (44)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-311"><span id="V.35"></span><span id="v.35"></span>**V. 35** (45) </span><span class="sxs-lookup"><span data-stu-id="2f412-311"><span id="V.35"></span><span id="v.35"></span>**V.35** (45)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-312"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46) </span><span class="sxs-lookup"><span data-stu-id="2f412-312"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-313"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47) </span><span class="sxs-lookup"><span data-stu-id="2f412-313"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-314"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**數據機** (48) </span><span class="sxs-lookup"><span data-stu-id="2f412-314"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-315"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49) </span><span class="sxs-lookup"><span data-stu-id="2f412-315"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-316"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET 路徑** (50) </span><span class="sxs-lookup"><span data-stu-id="2f412-316"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET Path** (50)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-317"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51) </span><span class="sxs-lookup"><span data-stu-id="2f412-317"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-318"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52) </span><span class="sxs-lookup"><span data-stu-id="2f412-318"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-319"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**專屬的 Virtual/Internal** (53) </span><span class="sxs-lookup"><span data-stu-id="2f412-319"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietary Virtual/Internal** (53)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-320"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**專屬多重通道** (54) </span><span class="sxs-lookup"><span data-stu-id="2f412-320"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietary Multiplexor** (54)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-321"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55) </span><span class="sxs-lookup"><span data-stu-id="2f412-321"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-322"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**光纖通道** (56) </span><span class="sxs-lookup"><span data-stu-id="2f412-322"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-323"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI 介面** (57) </span><span class="sxs-lookup"><span data-stu-id="2f412-323"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI Interface** (57)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-324"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**框架轉送互連** (58) </span><span class="sxs-lookup"><span data-stu-id="2f412-324"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay Interconnect** (58)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-325"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**適用于 802.3 (59) 的 ATM 模擬 LAN**</span><span class="sxs-lookup"><span data-stu-id="2f412-325"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM Emulated LAN for 802.3** (59)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-326"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**適用于 802.5 (60) 的 ATM 模擬 LAN**</span><span class="sxs-lookup"><span data-stu-id="2f412-326"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM Emulated LAN for 802.5** (60)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-327"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM 模擬線路** (61) </span><span class="sxs-lookup"><span data-stu-id="2f412-327"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM Emulated Circuit** (61)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-328"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**快速乙太網路 (100BaseT)** (62) </span><span class="sxs-lookup"><span data-stu-id="2f412-328"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-329"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63) </span><span class="sxs-lookup"><span data-stu-id="2f412-329"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-330"><span id="V.11"></span><span id="v.11"></span>**11** (64) </span><span class="sxs-lookup"><span data-stu-id="2f412-330"><span id="V.11"></span><span id="v.11"></span>**V.11** (64)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-331"><span id="V.36"></span><span id="v.36"></span>**5v** (65) </span><span class="sxs-lookup"><span data-stu-id="2f412-331"><span id="V.36"></span><span id="v.36"></span>**V.36** (65)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-332"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 在 64k** (66) </span><span class="sxs-lookup"><span data-stu-id="2f412-332"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 at 64K** (66)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-333"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703，以 2mb** (67) </span><span class="sxs-lookup"><span data-stu-id="2f412-333"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 at 2Mb** (67)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-334"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68) </span><span class="sxs-lookup"><span data-stu-id="2f412-334"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-335"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**快速 Ethernet 100BaseFX** (69) </span><span class="sxs-lookup"><span data-stu-id="2f412-335"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-336"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70) </span><span class="sxs-lookup"><span data-stu-id="2f412-336"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-337"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71) </span><span class="sxs-lookup"><span data-stu-id="2f412-337"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-338"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72) </span><span class="sxs-lookup"><span data-stu-id="2f412-338"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-339"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73) </span><span class="sxs-lookup"><span data-stu-id="2f412-339"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-340"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span> (74) 的 **資料連結切換**</span><span class="sxs-lookup"><span data-stu-id="2f412-340"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Data Link Switching** (74)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-341"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T 介面** (75) </span><span class="sxs-lookup"><span data-stu-id="2f412-341"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T Interface** (75)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-342"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U 介面** (76) </span><span class="sxs-lookup"><span data-stu-id="2f412-342"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U Interface** (76)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-343"><span id="LAP-D"></span><span id="lap-d"></span>**膝上-D** (77) </span><span class="sxs-lookup"><span data-stu-id="2f412-343"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-344"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP 交換器** (78) </span><span class="sxs-lookup"><span data-stu-id="2f412-344"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP Switch** (78)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-345"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**遠端來源路由橋接** (79) </span><span class="sxs-lookup"><span data-stu-id="2f412-345"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote Source Route Bridging** (79)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-346"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80) </span><span class="sxs-lookup"><span data-stu-id="2f412-346"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-347"><span id="DS0"></span><span id="ds0"></span>**DS0** (81) </span><span class="sxs-lookup"><span data-stu-id="2f412-347"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-348"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0** 組合 (82) </span><span class="sxs-lookup"><span data-stu-id="2f412-348"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-349"><span id="BSC"></span><span id="bsc"></span>**.Bsc** (83) </span><span class="sxs-lookup"><span data-stu-id="2f412-349"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-350"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**非同步** (84) </span><span class="sxs-lookup"><span data-stu-id="2f412-350"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-351"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**對抗網路廣播** (85) </span><span class="sxs-lookup"><span data-stu-id="2f412-351"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat Net Radio** (85)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-352"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5 r DTR** (86) </span><span class="sxs-lookup"><span data-stu-id="2f412-352"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5r DTR** (86)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-353"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc 報表系統** (87) </span><span class="sxs-lookup"><span data-stu-id="2f412-353"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc Report System** (87)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-354"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk 遠端存取通訊協定** (88) </span><span class="sxs-lookup"><span data-stu-id="2f412-354"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk Remote Access Protocol** (88)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-355"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**專屬的無連接** (89) </span><span class="sxs-lookup"><span data-stu-id="2f412-355"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietary Connectionless** (89)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-356"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X. 29 主機板** (90) </span><span class="sxs-lookup"><span data-stu-id="2f412-356"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X.29 Host PAD** (90)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-357"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X. 3 終端機板** (91) </span><span class="sxs-lookup"><span data-stu-id="2f412-357"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X.3 Terminal PAD** (91)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-358"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**框架轉送 MPI** (92) </span><span class="sxs-lookup"><span data-stu-id="2f412-358"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-359"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X 213** (93) </span><span class="sxs-lookup"><span data-stu-id="2f412-359"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X.213** (93)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-360"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94) </span><span class="sxs-lookup"><span data-stu-id="2f412-360"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-361"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95) </span><span class="sxs-lookup"><span data-stu-id="2f412-361"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-362"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96) </span><span class="sxs-lookup"><span data-stu-id="2f412-362"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-363"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97) </span><span class="sxs-lookup"><span data-stu-id="2f412-363"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-364"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98) </span><span class="sxs-lookup"><span data-stu-id="2f412-364"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-365"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99) </span><span class="sxs-lookup"><span data-stu-id="2f412-365"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-366"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**語音接收和傳輸** (100) </span><span class="sxs-lookup"><span data-stu-id="2f412-366"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Voice Receive and Transmit** (100)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-367"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**語音外部 Exchange 辦公室** (101) </span><span class="sxs-lookup"><span data-stu-id="2f412-367"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Voice Foreign Exchange Office** (101)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-368"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**語音外部交換服務** (102) </span><span class="sxs-lookup"><span data-stu-id="2f412-368"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Voice Foreign Exchange Service** (102)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-369"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**語音封裝** (103) </span><span class="sxs-lookup"><span data-stu-id="2f412-369"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Voice Encapsulation** (103)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-370"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**語音 OVER IP** (104) </span><span class="sxs-lookup"><span data-stu-id="2f412-370"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-371"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105) </span><span class="sxs-lookup"><span data-stu-id="2f412-371"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-372"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106) </span><span class="sxs-lookup"><span data-stu-id="2f412-372"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-373"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107) </span><span class="sxs-lookup"><span data-stu-id="2f412-373"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-374"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP 多重連結** 組合 (108) </span><span class="sxs-lookup"><span data-stu-id="2f412-374"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP Multilink Bundle** (108)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-375"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP OVER CDLC** (109) </span><span class="sxs-lookup"><span data-stu-id="2f412-375"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP over CDLC** (109)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-376"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP OVER 進儉樸爬** (110) </span><span class="sxs-lookup"><span data-stu-id="2f412-376"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over CLAW** (110)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-377"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**堆疊至堆疊** (111) </span><span class="sxs-lookup"><span data-stu-id="2f412-377"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack to Stack** (111)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-378"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**虛擬 IP 位址** (112) </span><span class="sxs-lookup"><span data-stu-id="2f412-378"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtual IP Address** (112)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-379"><span id="MPC"></span><span id="mpc"></span>**MPC** (113) </span><span class="sxs-lookup"><span data-stu-id="2f412-379"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-380"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>透過 **ATM 的 IP** (114) </span><span class="sxs-lookup"><span data-stu-id="2f412-380"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP over ATM** (114)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-381"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5 j 光纖權杖環** (115) </span><span class="sxs-lookup"><span data-stu-id="2f412-381"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5j Fibre Token Ring** (115)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-382"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116) </span><span class="sxs-lookup"><span data-stu-id="2f412-382"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-383"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117) </span><span class="sxs-lookup"><span data-stu-id="2f412-383"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-384"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118) </span><span class="sxs-lookup"><span data-stu-id="2f412-384"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-385"><span id="LAP-F"></span><span id="lap-f"></span>**膝上-F** (119) </span><span class="sxs-lookup"><span data-stu-id="2f412-385"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-386"><span id="V.37"></span><span id="v.37"></span>**37** (120) </span><span class="sxs-lookup"><span data-stu-id="2f412-386"><span id="V.37"></span><span id="v.37"></span>**V.37** (120)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-387"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**MLP** (121) </span><span class="sxs-lookup"><span data-stu-id="2f412-387"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X.25 MLP** (121)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-388"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span> (122) **的25個搜尋群組**</span><span class="sxs-lookup"><span data-stu-id="2f412-388"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X.25 Hunt Group** (122)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-389"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**TRANSP HDLC** (123) </span><span class="sxs-lookup"><span data-stu-id="2f412-389"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-390"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**交錯通道** (124) </span><span class="sxs-lookup"><span data-stu-id="2f412-390"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave Channel** (124)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-391"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125) </span><span class="sxs-lookup"><span data-stu-id="2f412-391"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-392"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**Ip 網路中 APPN HPR 的 ip ()** (126) </span><span class="sxs-lookup"><span data-stu-id="2f412-392"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (for APPN HPR in IP Networks)** (126)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-393"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC 層** (127) </span><span class="sxs-lookup"><span data-stu-id="2f412-393"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC Layer** (127)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-394"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV 下游** (128) </span><span class="sxs-lookup"><span data-stu-id="2f412-394"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV Downstream** (128)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-395"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV 上游** (129) </span><span class="sxs-lookup"><span data-stu-id="2f412-395"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV Upstream** (129)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-396"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**AVALON 12MPP 交換器** (130) </span><span class="sxs-lookup"><span data-stu-id="2f412-396"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Avalon 12MPP Switch** (130)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-397"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>通道 **(131**) </span><span class="sxs-lookup"><span data-stu-id="2f412-397"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-398"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**咖啡** (132) </span><span class="sxs-lookup"><span data-stu-id="2f412-398"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Coffee** (132)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-399"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**線路模擬服務** (133) </span><span class="sxs-lookup"><span data-stu-id="2f412-399"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation Service** (133)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-400"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM 子介面** (134) </span><span class="sxs-lookup"><span data-stu-id="2f412-400"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM SubInterface** (134)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-401"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**使用 802.1 q (135 的第2層 VLAN**) </span><span class="sxs-lookup"><span data-stu-id="2f412-401"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2 VLAN using 802.1Q** (135)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-402"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**使用 IP (136 的第3層 VLAN**) </span><span class="sxs-lookup"><span data-stu-id="2f412-402"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3 VLAN using IP** (136)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-403"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**使用 IPX 的第3層 VLAN** (137) </span><span class="sxs-lookup"><span data-stu-id="2f412-403"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3 VLAN using IPX** (137)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-404"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**數位電源線** (138) </span><span class="sxs-lookup"><span data-stu-id="2f412-404"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digital Power Line** (138)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-405"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>IP (139) 的 **多媒體郵件**</span><span class="sxs-lookup"><span data-stu-id="2f412-405"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia Mail over IP** (139)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-406"><span id="DTM"></span><span id="dtm"></span>**DTM** (140) </span><span class="sxs-lookup"><span data-stu-id="2f412-406"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-407"><span id="DCN"></span><span id="dcn"></span>**DCN** (141) </span><span class="sxs-lookup"><span data-stu-id="2f412-407"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-408"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP 轉送** (142) </span><span class="sxs-lookup"><span data-stu-id="2f412-408"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP Forwarding** (142)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-409"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143) </span><span class="sxs-lookup"><span data-stu-id="2f412-409"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-410"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144) </span><span class="sxs-lookup"><span data-stu-id="2f412-410"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-411"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145) </span><span class="sxs-lookup"><span data-stu-id="2f412-411"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-412"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**RCC MAC 層** (146) </span><span class="sxs-lookup"><span data-stu-id="2f412-412"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**DVB-RCC MAC Layer** (146)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-413"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-T RCC 下游** (147) </span><span class="sxs-lookup"><span data-stu-id="2f412-413"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC Downstream** (147)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-414"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-T RCC 上游** (148) </span><span class="sxs-lookup"><span data-stu-id="2f412-414"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC Upstream** (148)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-415"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM 虛擬** (149) </span><span class="sxs-lookup"><span data-stu-id="2f412-415"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM Virtual** (149)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-416"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS** 通道 (150) </span><span class="sxs-lookup"><span data-stu-id="2f412-416"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS Tunnel** (150)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-417"><span id="SRP"></span><span id="srp"></span>**SRP** (151) </span><span class="sxs-lookup"><span data-stu-id="2f412-417"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-418"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>透過 **ATM 的語音** (152) </span><span class="sxs-lookup"><span data-stu-id="2f412-418"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-419"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**語音 Over 框架轉送** (153) </span><span class="sxs-lookup"><span data-stu-id="2f412-419"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-420"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154) </span><span class="sxs-lookup"><span data-stu-id="2f412-420"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-421"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**複合連結** (155) </span><span class="sxs-lookup"><span data-stu-id="2f412-421"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Composite Link** (155)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-422"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 信號連結** (156) </span><span class="sxs-lookup"><span data-stu-id="2f412-422"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signaling Link** (156)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-423"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**專屬 P2P 無線** (157) </span><span class="sxs-lookup"><span data-stu-id="2f412-423"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietary P2P Wireless** (157)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-424"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**向前框架** (158) </span><span class="sxs-lookup"><span data-stu-id="2f412-424"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame Forward** (158)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-425"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>透過 ATM (159) **RFC1483 多重通訊協定**</span><span class="sxs-lookup"><span data-stu-id="2f412-425"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol over ATM** (159)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-426"><span id="USB"></span><span id="usb"></span>**USB** (160) </span><span class="sxs-lookup"><span data-stu-id="2f412-426"><span id="USB"></span><span id="usb"></span>**USB** (160)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-427"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3 Ad 連結匯總** (161) </span><span class="sxs-lookup"><span data-stu-id="2f412-427"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3ad Link Aggregate** (161)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-428"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP 原則帳戶** 處理 (162) </span><span class="sxs-lookup"><span data-stu-id="2f412-428"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP Policy Accounting** (162)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-429"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 多重連結 FR** (163) </span><span class="sxs-lookup"><span data-stu-id="2f412-429"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink FR** (163)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-430"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H. 323 閘道管理員** (164) </span><span class="sxs-lookup"><span data-stu-id="2f412-430"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H.323 Gatekeeper** (164)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-431"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H. 323 Proxy** (165) </span><span class="sxs-lookup"><span data-stu-id="2f412-431"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H.323 Proxy** (165)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-432"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166) </span><span class="sxs-lookup"><span data-stu-id="2f412-432"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-433"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**多重頻率的信號連結** (167) </span><span class="sxs-lookup"><span data-stu-id="2f412-433"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Multi-Frequency Signaling Link** (167)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-434"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168) </span><span class="sxs-lookup"><span data-stu-id="2f412-434"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-435"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169) </span><span class="sxs-lookup"><span data-stu-id="2f412-435"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-436"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 設備資料連結** (170) </span><span class="sxs-lookup"><span data-stu-id="2f412-436"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 Facility Data Link** (170)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-437"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>透過 **SONET/SDH** (171) 的封包</span><span class="sxs-lookup"><span data-stu-id="2f412-437"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-438"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**ASI 輸入** (172) </span><span class="sxs-lookup"><span data-stu-id="2f412-438"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**DVB-ASI Input** (172)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-439"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**ASI 輸出** (173) </span><span class="sxs-lookup"><span data-stu-id="2f412-439"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**DVB-ASI Output** (173)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-440"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**電源線** (174) </span><span class="sxs-lookup"><span data-stu-id="2f412-440"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Power Line** (174)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-441"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**非設備相關信號** (175) </span><span class="sxs-lookup"><span data-stu-id="2f412-441"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Non Facility Associated Signaling** (175)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-442"><span id="TR008"></span><span id="tr008"></span>**TR008** (176) </span><span class="sxs-lookup"><span data-stu-id="2f412-442"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-443"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177) </span><span class="sxs-lookup"><span data-stu-id="2f412-443"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-444"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178) </span><span class="sxs-lookup"><span data-stu-id="2f412-444"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-445"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179) </span><span class="sxs-lookup"><span data-stu-id="2f412-445"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-446"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**專屬的無線 MAC 層** (180) </span><span class="sxs-lookup"><span data-stu-id="2f412-446"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietary Wireless MAC Layer** (180)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-447"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**專屬無線下游** (181) </span><span class="sxs-lookup"><span data-stu-id="2f412-447"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietary Wireless Downstream** (181)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-448"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**專屬無線上游** (182) </span><span class="sxs-lookup"><span data-stu-id="2f412-448"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietary Wireless Upstream** (182)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-449"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN 類型 2** (183) </span><span class="sxs-lookup"><span data-stu-id="2f412-449"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN Type 2** (183)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-450"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Multipoint 的專用寬頻無線存取點** (184) </span><span class="sxs-lookup"><span data-stu-id="2f412-450"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Proprietary Broadband Wireless Access Point to Multipoint** (184)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-451"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET 額外負荷通道** (185) </span><span class="sxs-lookup"><span data-stu-id="2f412-451"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET Overhead Channel** (185)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-452"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**數位包裝程式額外負荷通道** (186) </span><span class="sxs-lookup"><span data-stu-id="2f412-452"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Digital Wrapper Overhead Channel** (186)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-453"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM 調適層 2** (187) </span><span class="sxs-lookup"><span data-stu-id="2f412-453"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM Adaptation Layer 2** (187)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-454"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**無線電 MAC** (188) </span><span class="sxs-lookup"><span data-stu-id="2f412-454"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio MAC** (188)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-455"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM 無線電** (189) </span><span class="sxs-lookup"><span data-stu-id="2f412-455"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-456"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**電腦間主幹** (190) </span><span class="sxs-lookup"><span data-stu-id="2f412-456"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Inter Machine Trunk** (190)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-457"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191) </span><span class="sxs-lookup"><span data-stu-id="2f412-457"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-458"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long READ DSL** (192) </span><span class="sxs-lookup"><span data-stu-id="2f412-458"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long Read DSL** (192)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-459"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**框架轉送 DLCI 端點** (193) </span><span class="sxs-lookup"><span data-stu-id="2f412-459"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Frame Relay DLCI Endpoint** (193)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-460"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI 端點** (194) </span><span class="sxs-lookup"><span data-stu-id="2f412-460"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI Endpoint** (194)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-461"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**光學通道** (195) </span><span class="sxs-lookup"><span data-stu-id="2f412-461"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optical Channel** (195)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-462"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**光學傳輸** (196) </span><span class="sxs-lookup"><span data-stu-id="2f412-462"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optical Transport** (196)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-463"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**專屬的 ATM** (197) </span><span class="sxs-lookup"><span data-stu-id="2f412-463"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietary ATM** (197)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-464"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**語音 Over 纜線** (198) </span><span class="sxs-lookup"><span data-stu-id="2f412-464"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice over Cable** (198)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-465"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**(199**) 的不限</span><span class="sxs-lookup"><span data-stu-id="2f412-465"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**Infiniband** (199)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-466"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**連結** (200) </span><span class="sxs-lookup"><span data-stu-id="2f412-466"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**TE Link** (200)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-467"><span id="Q.2931"></span><span id="q.2931"></span>**2931** (201) </span><span class="sxs-lookup"><span data-stu-id="2f412-467"><span id="Q.2931"></span><span id="q.2931"></span>**Q.2931** (201)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-468"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**虛擬主幹群組** (202) </span><span class="sxs-lookup"><span data-stu-id="2f412-468"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtual Trunk Group** (202)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-469"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP 主幹群組** (203) </span><span class="sxs-lookup"><span data-stu-id="2f412-469"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP Trunk Group** (203)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-470"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP 信號** (204) </span><span class="sxs-lookup"><span data-stu-id="2f412-470"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP Signaling** (204)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-471"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV 上游通道** (205) </span><span class="sxs-lookup"><span data-stu-id="2f412-471"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV Upstream Channel** (205)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-472"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206) </span><span class="sxs-lookup"><span data-stu-id="2f412-472"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-473"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155MB PON** (207) </span><span class="sxs-lookup"><span data-stu-id="2f412-473"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155Mb PON** (207)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-474"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622MB PON** (208) </span><span class="sxs-lookup"><span data-stu-id="2f412-474"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622Mb PON** (208)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-475"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**透明橋接器** (209) </span><span class="sxs-lookup"><span data-stu-id="2f412-475"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparent Bridge** (209)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-476"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**行群組** (210) </span><span class="sxs-lookup"><span data-stu-id="2f412-476"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Line Group** (210)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-477"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**語音 & 功能群組** (211) </span><span class="sxs-lookup"><span data-stu-id="2f412-477"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Voice & Feature Group** (211)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-478"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**VOICE FGD EANA** (212) </span><span class="sxs-lookup"><span data-stu-id="2f412-478"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-479"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**語音** (213) </span><span class="sxs-lookup"><span data-stu-id="2f412-479"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice DID** (213)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-480"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG 傳輸** (214) </span><span class="sxs-lookup"><span data-stu-id="2f412-480"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG Transport** (214)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-481"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215) </span><span class="sxs-lookup"><span data-stu-id="2f412-481"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6To4** (215)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-482"><span id="GTP"></span><span id="gtp"></span>**GTP** (216) </span><span class="sxs-lookup"><span data-stu-id="2f412-482"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-483"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217) </span><span class="sxs-lookup"><span data-stu-id="2f412-483"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-484"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218) </span><span class="sxs-lookup"><span data-stu-id="2f412-484"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-485"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**光學通道群組** (219) </span><span class="sxs-lookup"><span data-stu-id="2f412-485"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optical Channel Group** (219)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-486"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220) </span><span class="sxs-lookup"><span data-stu-id="2f412-486"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-487"><span id="GFP"></span><span id="gfp"></span>**GFP** (221) </span><span class="sxs-lookup"><span data-stu-id="2f412-487"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-488"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222) </span><span class="sxs-lookup"><span data-stu-id="2f412-488"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-489"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223) </span><span class="sxs-lookup"><span data-stu-id="2f412-489"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-490"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224) </span><span class="sxs-lookup"><span data-stu-id="2f412-490"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-491"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA 保留** (225. 4095) </span><span class="sxs-lookup"><span data-stu-id="2f412-491"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-492"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096) </span><span class="sxs-lookup"><span data-stu-id="2f412-492"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-493"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097) </span><span class="sxs-lookup"><span data-stu-id="2f412-493"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-494"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098) </span><span class="sxs-lookup"><span data-stu-id="2f412-494"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-495"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099) </span><span class="sxs-lookup"><span data-stu-id="2f412-495"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-496"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100) </span><span class="sxs-lookup"><span data-stu-id="2f412-496"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-497"><span id="SNA"></span><span id="sna"></span>**SNA** (4101) </span><span class="sxs-lookup"><span data-stu-id="2f412-497"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-498"><span id="CONP"></span><span id="conp"></span>**CONP** (4102) </span><span class="sxs-lookup"><span data-stu-id="2f412-498"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-499"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103) </span><span class="sxs-lookup"><span data-stu-id="2f412-499"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-500"><span id="VINES"></span><span id="vines"></span>**VINES** (4104) </span><span class="sxs-lookup"><span data-stu-id="2f412-500"><span id="VINES"></span><span id="vines"></span>**VINES** (4104)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-501"><span id="XNS"></span><span id="xns"></span>**XNS** (4105) </span><span class="sxs-lookup"><span data-stu-id="2f412-501"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-502"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B 通道端點** (4106) </span><span class="sxs-lookup"><span data-stu-id="2f412-502"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B Channel Endpoint** (4106)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-503"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN 資料通道端點** (4107) </span><span class="sxs-lookup"><span data-stu-id="2f412-503"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN D Channel Endpoint** (4107)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-504"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108) </span><span class="sxs-lookup"><span data-stu-id="2f412-504"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-505"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109) </span><span class="sxs-lookup"><span data-stu-id="2f412-505"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-506"><span id="UDP"></span><span id="udp"></span>**UDP** (4110) </span><span class="sxs-lookup"><span data-stu-id="2f412-506"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-507"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111) </span><span class="sxs-lookup"><span data-stu-id="2f412-507"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-508"><span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112) </span><span class="sxs-lookup"><span data-stu-id="2f412-508"><span id="802.11a"></span><span id="802.11A"></span>**802.11a** (4112)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-509"><span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113) </span><span class="sxs-lookup"><span data-stu-id="2f412-509"><span id="802.11b"></span><span id="802.11B"></span>**802.11b** (4113)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-510"><span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114) </span><span class="sxs-lookup"><span data-stu-id="2f412-510"><span id="802.11g"></span><span id="802.11G"></span>**802.11g** (4114)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-511"><span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115) </span><span class="sxs-lookup"><span data-stu-id="2f412-511"><span id="802.11h"></span><span id="802.11H"></span>**802.11h** (4115)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-512"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200) </span><span class="sxs-lookup"><span data-stu-id="2f412-512"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-513"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201) </span><span class="sxs-lookup"><span data-stu-id="2f412-513"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-514"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202) </span><span class="sxs-lookup"><span data-stu-id="2f412-514"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-515"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203) </span><span class="sxs-lookup"><span data-stu-id="2f412-515"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-516"><span id="HTTP"></span><span id="http"></span>**HTTP** (4204) </span><span class="sxs-lookup"><span data-stu-id="2f412-516"><span id="HTTP"></span><span id="http"></span>**HTTP** (4204)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-517"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205) </span><span class="sxs-lookup"><span data-stu-id="2f412-517"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-518"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300) </span><span class="sxs-lookup"><span data-stu-id="2f412-518"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-519"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400) </span><span class="sxs-lookup"><span data-stu-id="2f412-519"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-520"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401) </span><span class="sxs-lookup"><span data-stu-id="2f412-520"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-521"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402) </span><span class="sxs-lookup"><span data-stu-id="2f412-521"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-522"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403) </span><span class="sxs-lookup"><span data-stu-id="2f412-522"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-523"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404) </span><span class="sxs-lookup"><span data-stu-id="2f412-523"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-524"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405) </span><span class="sxs-lookup"><span data-stu-id="2f412-524"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-525"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406) </span><span class="sxs-lookup"><span data-stu-id="2f412-525"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-526"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2f412-526"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2f412-527"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (32768。</span><span class="sxs-lookup"><span data-stu-id="2f412-527"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="2f412-528">)</span><span class="sxs-lookup"><span data-stu-id="2f412-528">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2f412-529">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="2f412-529">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-530">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-531">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-532">這個屬性已被取代，代替 **ProtocolIFType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2f412-532">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="2f412-533">這個屬性繼承自 [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)。</span><span class="sxs-lookup"><span data-stu-id="2f412-533">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-534">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2f412-534">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-535">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-535">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-536">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-537">上次要求或預期的管理服務狀態。</span><span class="sxs-lookup"><span data-stu-id="2f412-537">The last requested or desired state for the management service.</span></span> <span data-ttu-id="2f412-538">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="2f412-538">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="2f412-539">值</span><span class="sxs-lookup"><span data-stu-id="2f412-539">Value</span></span>                                                                         | <span data-ttu-id="2f412-540">意義</span><span class="sxs-lookup"><span data-stu-id="2f412-540">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="2f412-541"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="2f412-541"><dt>12</dt></span></span> </dl> | <span data-ttu-id="2f412-542">不適用。</span><span class="sxs-lookup"><span data-stu-id="2f412-542">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2f412-543">**狀態**</span><span class="sxs-lookup"><span data-stu-id="2f412-543">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-544">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-545">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-545">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-546">描述元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="2f412-546">Describes the status of the element.</span></span> <span data-ttu-id="2f412-547">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-547">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="2f412-548">正常</span><span class="sxs-lookup"><span data-stu-id="2f412-548">"OK"</span></span>

<span data-ttu-id="2f412-549">錯誤</span><span class="sxs-lookup"><span data-stu-id="2f412-549">"Error"</span></span>

<span data-ttu-id="2f412-550">降級</span><span class="sxs-lookup"><span data-stu-id="2f412-550">"Degraded"</span></span>

<span data-ttu-id="2f412-551">不明</span><span class="sxs-lookup"><span data-stu-id="2f412-551">"Unknown"</span></span>

<span data-ttu-id="2f412-552">「Pred 失敗」</span><span class="sxs-lookup"><span data-stu-id="2f412-552">"Pred Fail"</span></span>

<span data-ttu-id="2f412-553">入門</span><span class="sxs-lookup"><span data-stu-id="2f412-553">"Starting"</span></span>

<span data-ttu-id="2f412-554">從而</span><span class="sxs-lookup"><span data-stu-id="2f412-554">"Stopping"</span></span>

<span data-ttu-id="2f412-555">維護</span><span class="sxs-lookup"><span data-stu-id="2f412-555">"Service"</span></span>

<span data-ttu-id="2f412-556">強調</span><span class="sxs-lookup"><span data-stu-id="2f412-556">"Stressed"</span></span>

<span data-ttu-id="2f412-557">"NonRecover"</span><span class="sxs-lookup"><span data-stu-id="2f412-557">"NonRecover"</span></span>

<span data-ttu-id="2f412-558">「無連絡人」</span><span class="sxs-lookup"><span data-stu-id="2f412-558">"No Contact"</span></span>

<span data-ttu-id="2f412-559">「遺失通訊」</span><span class="sxs-lookup"><span data-stu-id="2f412-559">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="2f412-560">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2f412-560">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-561">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2f412-561">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2f412-562">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-562">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-563">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="2f412-563">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2f412-564">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="2f412-564">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-565">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2f412-565">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-566">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-567">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-568">裝載系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="2f412-568">The hosting system's creation class name.</span></span> <span data-ttu-id="2f412-569">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。</span><span class="sxs-lookup"><span data-stu-id="2f412-569">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-570">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2f412-570">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-571">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-572">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f412-573">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="2f412-573">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="2f412-574">主控系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f412-574">The name of the hosting system.</span></span> <span data-ttu-id="2f412-575">這個屬性繼承自 [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)。</span><span class="sxs-lookup"><span data-stu-id="2f412-575">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="2f412-576">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2f412-576">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-577">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2f412-577">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-578">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-578">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-579">專案的已啟用狀態上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="2f412-579">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2f412-580">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不受支援。</span><span class="sxs-lookup"><span data-stu-id="2f412-580">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2f412-581">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2f412-581">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-582">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f412-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-583">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-583">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-584">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="2f412-584">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2f412-585">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="2f412-585">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f412-586">**WWNN**</span><span class="sxs-lookup"><span data-stu-id="2f412-586">**WWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-587">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-588">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-588">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-589">此端點所連接之光纖通道埠的全球節點名稱。</span><span class="sxs-lookup"><span data-stu-id="2f412-589">The world wide node name of the Fibre Channel port this endpoint is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="2f412-590">**WWPN**</span><span class="sxs-lookup"><span data-stu-id="2f412-590">**WWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f412-591">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f412-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f412-592">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f412-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f412-593">此端點所連接之光纖通道埠的全球埠名稱。</span><span class="sxs-lookup"><span data-stu-id="2f412-593">The world wide port name of the Fibre Channel port this endpoint is connected to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f412-594">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f412-594">Requirements</span></span>



| <span data-ttu-id="2f412-595">需求</span><span class="sxs-lookup"><span data-stu-id="2f412-595">Requirement</span></span> | <span data-ttu-id="2f412-596">值</span><span class="sxs-lookup"><span data-stu-id="2f412-596">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f412-597">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f412-597">Minimum supported client</span></span><br/> | <span data-ttu-id="2f412-598">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f412-598">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f412-599">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f412-599">Minimum supported server</span></span><br/> | <span data-ttu-id="2f412-600">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f412-600">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f412-601">命名空間</span><span class="sxs-lookup"><span data-stu-id="2f412-601">Namespace</span></span><br/>                | <span data-ttu-id="2f412-602">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="2f412-602">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f412-603">MOF</span><span class="sxs-lookup"><span data-stu-id="2f412-603">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f412-604"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2f412-604"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f412-605">DLL</span><span class="sxs-lookup"><span data-stu-id="2f412-605">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f412-606"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f412-606"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

