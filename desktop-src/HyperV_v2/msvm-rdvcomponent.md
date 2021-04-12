---
description: 代表 RDV 元件的狀態，該元件負責將父系的傳輸提供給來賓以供設定之用。
ms.assetid: 240d2659-01ec-4300-a17e-0b1ec90483df
title: Msvm_RdvComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent
- Msvm_RdvComponent.RequestStateChange
- Msvm_RdvComponent.SetPowerState
- Msvm_RdvComponent.Reset
- Msvm_RdvComponent.EnableDevice
- Msvm_RdvComponent.OnlineDevice
- Msvm_RdvComponent.QuiesceDevice
- Msvm_RdvComponent.SaveProperties
- Msvm_RdvComponent.RestoreProperties
- Msvm_RdvComponent.InstanceID
- Msvm_RdvComponent.Caption
- Msvm_RdvComponent.Description
- Msvm_RdvComponent.ElementName
- Msvm_RdvComponent.InstallDate
- Msvm_RdvComponent.Name
- Msvm_RdvComponent.OperationalStatus
- Msvm_RdvComponent.StatusDescriptions
- Msvm_RdvComponent.Status
- Msvm_RdvComponent.HealthState
- Msvm_RdvComponent.CommunicationStatus
- Msvm_RdvComponent.DetailedStatus
- Msvm_RdvComponent.OperatingStatus
- Msvm_RdvComponent.PrimaryStatus
- Msvm_RdvComponent.EnabledState
- Msvm_RdvComponent.OtherEnabledState
- Msvm_RdvComponent.RequestedState
- Msvm_RdvComponent.EnabledDefault
- Msvm_RdvComponent.TimeOfLastStateChange
- Msvm_RdvComponent.AvailableRequestedStates
- Msvm_RdvComponent.TransitioningToState
- Msvm_RdvComponent.SystemCreationClassName
- Msvm_RdvComponent.SystemName
- Msvm_RdvComponent.CreationClassName
- Msvm_RdvComponent.DeviceID
- Msvm_RdvComponent.PowerManagementSupported
- Msvm_RdvComponent.PowerManagementCapabilities
- Msvm_RdvComponent.Availability
- Msvm_RdvComponent.StatusInfo
- Msvm_RdvComponent.LastErrorCode
- Msvm_RdvComponent.ErrorDescription
- Msvm_RdvComponent.ErrorCleared
- Msvm_RdvComponent.OtherIdentifyingInfo
- Msvm_RdvComponent.PowerOnHours
- Msvm_RdvComponent.TotalPowerOnHours
- Msvm_RdvComponent.IdentifyingDescriptions
- Msvm_RdvComponent.AdditionalAvailability
- Msvm_RdvComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e1dbffb7db18ef2441d4c8e06cff23af2648e5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192989"
---
# <a name="msvm_rdvcomponent-class"></a><span data-ttu-id="0def9-103">Msvm \_ RdvComponent 類別</span><span class="sxs-lookup"><span data-stu-id="0def9-103">Msvm\_RdvComponent class</span></span>

<span data-ttu-id="0def9-104">代表 RDV 元件的狀態，該元件負責將父系的傳輸提供給來賓以供設定之用。</span><span class="sxs-lookup"><span data-stu-id="0def9-104">Represents the state of the RDV component, which is responsible for providing a transport for the parent to the guest for configuration purposes.</span></span>

<span data-ttu-id="0def9-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0def9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0def9-106">語法</span><span class="sxs-lookup"><span data-stu-id="0def9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "RDV";
  string   Description = "Remote Desktop Virtualization Service";
  string   ElementName = "RDV";
  datetime InstallDate;
  string   Name = "RDV";
  uint16   OperationalStatus[] = {2};
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_RdvComponent";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="0def9-107">成員</span><span class="sxs-lookup"><span data-stu-id="0def9-107">Members</span></span>

<span data-ttu-id="0def9-108">**Msvm \_ RdvComponent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0def9-108">The **Msvm\_RdvComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="0def9-109">方法</span><span class="sxs-lookup"><span data-stu-id="0def9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0def9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0def9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0def9-111">方法</span><span class="sxs-lookup"><span data-stu-id="0def9-111">Methods</span></span>

<span data-ttu-id="0def9-112">**Msvm \_ RdvComponent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0def9-112">The **Msvm\_RdvComponent** class has these methods.</span></span>



| <span data-ttu-id="0def9-113">方法</span><span class="sxs-lookup"><span data-stu-id="0def9-113">Method</span></span>                                                       | <span data-ttu-id="0def9-114">描述</span><span class="sxs-lookup"><span data-stu-id="0def9-114">Description</span></span>                                                                                                                                                                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0def9-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="0def9-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="0def9-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0def9-116">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="0def9-117">**EnableEndPoints**</span><span class="sxs-lookup"><span data-stu-id="0def9-117">**EnableEndPoints**</span></span>](enableendpoints-msvm-rdvcomponent.md) | <span data-ttu-id="0def9-118">要求遠端桌面服務的虛擬裝置啟動與虛擬機器的管道連接。</span><span class="sxs-lookup"><span data-stu-id="0def9-118">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span> <span data-ttu-id="0def9-119">如果傳回零 (0) ，表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0def9-119">If zero (0) is returned, then the operation was successful.</span></span> <span data-ttu-id="0def9-120">任何其他傳回碼表示錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="0def9-120">Any other return code indicates an error condition.</span></span><br/> |
| <span data-ttu-id="0def9-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="0def9-121">**OnlineDevice**</span></span>                                             | <span data-ttu-id="0def9-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0def9-122">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="0def9-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="0def9-123">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="0def9-124">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0def9-124">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="0def9-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0def9-125">**RequestStateChange**</span></span>                                       | <span data-ttu-id="0def9-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0def9-126">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="0def9-127">**重設**</span><span class="sxs-lookup"><span data-stu-id="0def9-127">**Reset**</span></span>                                                    | <span data-ttu-id="0def9-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0def9-128">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="0def9-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="0def9-129">**RestoreProperties**</span></span>                                        | <span data-ttu-id="0def9-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0def9-130">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="0def9-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="0def9-131">**SaveProperties**</span></span>                                           | <span data-ttu-id="0def9-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0def9-132">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="0def9-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0def9-133">**SetPowerState**</span></span>                                            | <span data-ttu-id="0def9-134">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0def9-134">This method is not supported.</span></span><br/>                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="0def9-135">屬性</span><span class="sxs-lookup"><span data-stu-id="0def9-135">Properties</span></span>

<span data-ttu-id="0def9-136">**Msvm \_ RdvComponent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0def9-136">The **Msvm\_RdvComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0def9-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="0def9-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-138">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0def9-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0def9-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-140">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="0def9-141">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-142">**可用性**</span><span class="sxs-lookup"><span data-stu-id="0def9-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-143">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-145">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-145">The primary availability and status of the device.</span></span> <span data-ttu-id="0def9-146">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0def9-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-148">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0def9-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0def9-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-150">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="0def9-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="0def9-151">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0def9-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-152">**標題**</span><span class="sxs-lookup"><span data-stu-id="0def9-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-155">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="0def9-155">A short description of the object.</span></span> <span data-ttu-id="0def9-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0def9-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-158">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-160">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="0def9-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0def9-161">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0def9-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0def9-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0def9-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0def9-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="0def9-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="0def9-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="0def9-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="0def9-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0def9-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0def9-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0def9-170">)</span><span class="sxs-lookup"><span data-stu-id="0def9-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0def9-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0def9-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-174">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="0def9-174">The scoping system's creation class name.</span></span> <span data-ttu-id="0def9-175">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0def9-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-176">**說明**</span><span class="sxs-lookup"><span data-stu-id="0def9-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-179">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="0def9-179">A description of the object.</span></span> <span data-ttu-id="0def9-180">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0def9-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-182">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-184">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0def9-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0def9-185">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0def9-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0def9-186">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0def9-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="0def9-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="0def9-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="0def9-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="0def9-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="0def9-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="0def9-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0def9-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0def9-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0def9-195">)</span><span class="sxs-lookup"><span data-stu-id="0def9-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0def9-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0def9-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-199">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="0def9-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="0def9-200">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0def9-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0def9-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-204">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0def9-204">A display name for the object.</span></span> <span data-ttu-id="0def9-205">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0def9-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-207">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-209">系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0def9-209">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="0def9-210">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0def9-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-211">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0def9-211">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-212">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-214">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-214">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0def9-215">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0def9-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="0def9-216">值</span><span class="sxs-lookup"><span data-stu-id="0def9-216">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="0def9-217">意義</span><span class="sxs-lookup"><span data-stu-id="0def9-217">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="0def9-218"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-218"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="0def9-219">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-219">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="0def9-220"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-220"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="0def9-221"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-221"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="0def9-222">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="0def9-222">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="0def9-223"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-223"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="0def9-224">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="0def9-224">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="0def9-225">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-225"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="0def9-226">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="0def9-226">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="0def9-227"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-227"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="0def9-228">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="0def9-228">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="0def9-229"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-229"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="0def9-230">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="0def9-230">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="0def9-231"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="0def9-231"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="0def9-232">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-232">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="0def9-233"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-233"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="0def9-234">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="0def9-234">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="0def9-235"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-235"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="0def9-236">元素已啟用但處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="0def9-236">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="0def9-237">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="0def9-237">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="0def9-238">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="0def9-238">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="0def9-239"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-239"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="0def9-240">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="0def9-240">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="0def9-241">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="0def9-241">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="0def9-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0def9-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-243">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0def9-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-245">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0def9-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="0def9-246">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0def9-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-250">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0def9-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="0def9-251">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0def9-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-253">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-255">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="0def9-255">The current health of the element.</span></span> <span data-ttu-id="0def9-256">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0def9-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-258">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0def9-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0def9-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-260">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0def9-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="0def9-261">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0def9-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-263">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0def9-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-265">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0def9-265">The date and time when the object was installed.</span></span> <span data-ttu-id="0def9-266">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="0def9-266">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="0def9-267">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-268">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0def9-268">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-269">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0def9-271">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="0def9-271">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0def9-272">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="0def9-272">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0def9-273">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-273">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0def9-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-275">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0def9-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-277">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0def9-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="0def9-278">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="0def9-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-280">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0def9-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-282">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="0def9-282">This property has been deprecated.</span></span> <span data-ttu-id="0def9-283">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-284">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0def9-284">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-285">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-287">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0def9-287">The label by which the object is known.</span></span> <span data-ttu-id="0def9-288">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-289">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0def9-289">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-290">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-292">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0def9-292">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0def9-293">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0def9-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0def9-294">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0def9-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0def9-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="0def9-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="0def9-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="0def9-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="0def9-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="0def9-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="0def9-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="0def9-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="0def9-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="0def9-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="0def9-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="0def9-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="0def9-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="0def9-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="0def9-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="0def9-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="0def9-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0def9-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0def9-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0def9-314">)</span><span class="sxs-lookup"><span data-stu-id="0def9-314">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0def9-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0def9-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-316">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0def9-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0def9-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-318">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-318">The current statuses of the object.</span></span> <span data-ttu-id="0def9-319">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0def9-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-323">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="0def9-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0def9-324">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0def9-324">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="0def9-325">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0def9-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-326">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0def9-326">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-327">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0def9-327">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0def9-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-329">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="0def9-329">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="0def9-330">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-331">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0def9-331">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-332">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0def9-332">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0def9-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-334">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="0def9-334">The power management capabilities of the device.</span></span> <span data-ttu-id="0def9-335">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-335">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-336">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0def9-336">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-337">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0def9-337">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-339">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="0def9-339">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="0def9-340">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0def9-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-342">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0def9-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-344">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="0def9-344">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="0def9-345">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-346">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0def9-346">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-347">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-349">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0def9-349">Provides high level status information.</span></span> <span data-ttu-id="0def9-350">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-350">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0def9-351">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0def9-351">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0def9-352">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0def9-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0def9-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-354"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="0def9-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="0def9-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="0def9-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0def9-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0def9-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="0def9-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0def9-359">)</span><span class="sxs-lookup"><span data-stu-id="0def9-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0def9-360">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0def9-360">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-361">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-363">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-363">The last requested or desired state for the element.</span></span> <span data-ttu-id="0def9-364">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="0def9-364">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-365">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0def9-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-366">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-368">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-368">The current status of the object.</span></span> <span data-ttu-id="0def9-369">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-369">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-370">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0def9-370">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-371">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0def9-371">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0def9-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-373">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="0def9-373">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0def9-374">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0def9-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-375">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0def9-375">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-376">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-378">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-378">The current state of the logical device.</span></span> <span data-ttu-id="0def9-379">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-379">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-380">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0def9-380">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-383">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="0def9-383">The scoping system's creation class name.</span></span> <span data-ttu-id="0def9-384">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0def9-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-385">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0def9-385">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-386">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0def9-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-388">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="0def9-388">The scoping system's name.</span></span> <span data-ttu-id="0def9-389">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0def9-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0def9-390">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0def9-390">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-391">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0def9-391">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-393">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="0def9-393">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0def9-394">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0def9-394">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-395">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0def9-395">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-396">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0def9-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-398">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="0def9-398">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="0def9-399">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0def9-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0def9-400">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0def9-400">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0def9-401">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0def9-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0def9-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0def9-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0def9-403">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="0def9-403">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0def9-404">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0def9-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0def9-405">規格需求</span><span class="sxs-lookup"><span data-stu-id="0def9-405">Requirements</span></span>



| <span data-ttu-id="0def9-406">需求</span><span class="sxs-lookup"><span data-stu-id="0def9-406">Requirement</span></span> | <span data-ttu-id="0def9-407">值</span><span class="sxs-lookup"><span data-stu-id="0def9-407">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0def9-408">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0def9-408">Minimum supported client</span></span><br/> | <span data-ttu-id="0def9-409">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0def9-409">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0def9-410">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0def9-410">Minimum supported server</span></span><br/> | <span data-ttu-id="0def9-411">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0def9-411">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0def9-412">命名空間</span><span class="sxs-lookup"><span data-stu-id="0def9-412">Namespace</span></span><br/>                | <span data-ttu-id="0def9-413">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0def9-413">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0def9-414">MOF</span><span class="sxs-lookup"><span data-stu-id="0def9-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0def9-415"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-415"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0def9-416">DLL</span><span class="sxs-lookup"><span data-stu-id="0def9-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0def9-417"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0def9-417"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

