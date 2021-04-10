---
description: 代表虛擬機器中的軟碟控制卡。
ms.assetid: 38A19BF3-0E8F-4DCE-B2DB-B2E3F8100E00
title: Msvm_DisketteController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteController
- Msvm_DisketteController.SetPowerState
- Msvm_DisketteController.EnableDevice
- Msvm_DisketteController.OnlineDevice
- Msvm_DisketteController.QuiesceDevice
- Msvm_DisketteController.SaveProperties
- Msvm_DisketteController.RestoreProperties
- Msvm_DisketteController.InstanceID
- Msvm_DisketteController.Caption
- Msvm_DisketteController.Description
- Msvm_DisketteController.ElementName
- Msvm_DisketteController.InstallDate
- Msvm_DisketteController.Name
- Msvm_DisketteController.OperationalStatus
- Msvm_DisketteController.StatusDescriptions
- Msvm_DisketteController.Status
- Msvm_DisketteController.HealthState
- Msvm_DisketteController.CommunicationStatus
- Msvm_DisketteController.DetailedStatus
- Msvm_DisketteController.OperatingStatus
- Msvm_DisketteController.PrimaryStatus
- Msvm_DisketteController.EnabledState
- Msvm_DisketteController.OtherEnabledState
- Msvm_DisketteController.RequestedState
- Msvm_DisketteController.EnabledDefault
- Msvm_DisketteController.TimeOfLastStateChange
- Msvm_DisketteController.AvailableRequestedStates
- Msvm_DisketteController.TransitioningToState
- Msvm_DisketteController.SystemCreationClassName
- Msvm_DisketteController.SystemName
- Msvm_DisketteController.CreationClassName
- Msvm_DisketteController.DeviceID
- Msvm_DisketteController.PowerManagementSupported
- Msvm_DisketteController.PowerManagementCapabilities
- Msvm_DisketteController.Availability
- Msvm_DisketteController.StatusInfo
- Msvm_DisketteController.LastErrorCode
- Msvm_DisketteController.ErrorDescription
- Msvm_DisketteController.ErrorCleared
- Msvm_DisketteController.OtherIdentifyingInfo
- Msvm_DisketteController.PowerOnHours
- Msvm_DisketteController.TotalPowerOnHours
- Msvm_DisketteController.IdentifyingDescriptions
- Msvm_DisketteController.AdditionalAvailability
- Msvm_DisketteController.MaxQuiesceTime
- Msvm_DisketteController.TimeOfLastReset
- Msvm_DisketteController.ProtocolSupported
- Msvm_DisketteController.MaxNumberControlled
- Msvm_DisketteController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f1e4e731464e25dc8e871ebd17cdcddd4e262673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690264"
---
# <a name="msvm_diskettecontroller-class"></a><span data-ttu-id="9600e-103">Msvm \_ DisketteController 類別</span><span class="sxs-lookup"><span data-stu-id="9600e-103">Msvm\_DisketteController class</span></span>

<span data-ttu-id="9600e-104">代表虛擬機器中的軟碟控制卡。</span><span class="sxs-lookup"><span data-stu-id="9600e-104">Represents the floppy controller in the virtual machine.</span></span> <span data-ttu-id="9600e-105">磁碟控制卡已修正，因此沒有相關聯的資源集區。</span><span class="sxs-lookup"><span data-stu-id="9600e-105">The floppy controller is fixed, therefore there is no resource pool associated with it.</span></span>

<span data-ttu-id="9600e-106">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="9600e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9600e-107">語法</span><span class="sxs-lookup"><span data-stu-id="9600e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteController : CIM_Controller
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName = "Msvm_DisketteController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 7;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Diskette Protocol";
};
```

## <a name="members"></a><span data-ttu-id="9600e-108">成員</span><span class="sxs-lookup"><span data-stu-id="9600e-108">Members</span></span>

<span data-ttu-id="9600e-109">**Msvm \_ DisketteController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9600e-109">The **Msvm\_DisketteController** class has these types of members:</span></span>

-   [<span data-ttu-id="9600e-110">方法</span><span class="sxs-lookup"><span data-stu-id="9600e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9600e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9600e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9600e-112">方法</span><span class="sxs-lookup"><span data-stu-id="9600e-112">Methods</span></span>

<span data-ttu-id="9600e-113">**Msvm \_ DisketteController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9600e-113">The **Msvm\_DisketteController** class has these methods.</span></span>



| <span data-ttu-id="9600e-114">方法</span><span class="sxs-lookup"><span data-stu-id="9600e-114">Method</span></span>                                                                   | <span data-ttu-id="9600e-115">描述</span><span class="sxs-lookup"><span data-stu-id="9600e-115">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="9600e-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="9600e-116">**EnableDevice**</span></span>                                                         | <span data-ttu-id="9600e-117">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9600e-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9600e-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="9600e-118">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="9600e-119">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9600e-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9600e-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="9600e-120">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="9600e-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9600e-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="9600e-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9600e-122">**RequestStateChange**</span></span>](msvm-diskettecontroller-requeststatechange.md) | <span data-ttu-id="9600e-123">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9600e-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="9600e-124">**重設**</span><span class="sxs-lookup"><span data-stu-id="9600e-124">**Reset**</span></span>](msvm-diskettecontroller-reset.md)                           | <span data-ttu-id="9600e-125">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="9600e-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="9600e-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="9600e-126">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="9600e-127">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9600e-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9600e-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="9600e-128">**SaveProperties**</span></span>                                                       | <span data-ttu-id="9600e-129">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9600e-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="9600e-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9600e-130">**SetPowerState**</span></span>                                                        | <span data-ttu-id="9600e-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="9600e-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9600e-132">屬性</span><span class="sxs-lookup"><span data-stu-id="9600e-132">Properties</span></span>

<span data-ttu-id="9600e-133">**Msvm \_ DisketteController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9600e-133">The **Msvm\_DisketteController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9600e-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="9600e-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-135">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9600e-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9600e-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-137">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="9600e-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-138">**可用性**</span><span class="sxs-lookup"><span data-stu-id="9600e-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-141">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="9600e-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-142">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9600e-142">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-143">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9600e-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9600e-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-145">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="9600e-145">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9600e-146">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9600e-146">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-147">**標題**</span><span class="sxs-lookup"><span data-stu-id="9600e-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-150">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="9600e-150">A short description of the object.</span></span> <span data-ttu-id="9600e-151">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-152">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9600e-152">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-153">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-155">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="9600e-155">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9600e-156">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9600e-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9600e-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9600e-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9600e-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="9600e-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="9600e-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="9600e-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="9600e-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="9600e-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="9600e-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9600e-165">)</span><span class="sxs-lookup"><span data-stu-id="9600e-165">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9600e-166">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9600e-166">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-169">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="9600e-169">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9600e-170">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且會設定為 "Msvm \_ DisketteController"。</span><span class="sxs-lookup"><span data-stu-id="9600e-170">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_DisketteController".</span></span>

</dd> <dt>

<span data-ttu-id="9600e-171">**說明**</span><span class="sxs-lookup"><span data-stu-id="9600e-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-174">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="9600e-174">A description of the object.</span></span> <span data-ttu-id="9600e-175">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9600e-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-177">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-179">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9600e-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9600e-180">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9600e-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9600e-181">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9600e-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="9600e-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="9600e-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="9600e-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="9600e-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="9600e-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="9600e-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="9600e-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="9600e-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9600e-190">)</span><span class="sxs-lookup"><span data-stu-id="9600e-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9600e-191">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9600e-191">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-194">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="9600e-194">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="9600e-195">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="9600e-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-196">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9600e-196">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-199">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9600e-199">A display name for the object.</span></span> <span data-ttu-id="9600e-200">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-201">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9600e-201">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-202">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-204">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-204">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9600e-205">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9600e-205">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9600e-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-207">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-209">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9600e-210">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="9600e-210">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="9600e-211">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9600e-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9600e-212">值</span><span class="sxs-lookup"><span data-stu-id="9600e-212">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9600e-213">意義</span><span class="sxs-lookup"><span data-stu-id="9600e-213">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9600e-214"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9600e-215">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-215">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9600e-216"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-216"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="9600e-217"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-217"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="9600e-218">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="9600e-218">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="9600e-219"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-219"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9600e-220">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="9600e-220">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="9600e-221">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-221"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="9600e-222">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="9600e-222">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="9600e-223"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-223"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="9600e-224">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="9600e-224">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="9600e-225"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-225"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="9600e-226">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="9600e-226">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="9600e-227"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="9600e-227"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="9600e-228">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-228">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="9600e-229"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-229"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="9600e-230">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="9600e-230">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="9600e-231"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-231"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="9600e-232">已啟用元素，但它處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="9600e-232">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="9600e-233">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="9600e-233">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="9600e-234">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="9600e-234">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="9600e-235"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-235"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="9600e-236">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="9600e-236">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="9600e-237">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="9600e-237">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="9600e-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9600e-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-239">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9600e-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-241">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-241">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-242">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9600e-242">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-245">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-246">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9600e-246">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-247">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-249">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="9600e-249">The current health of the element.</span></span> <span data-ttu-id="9600e-250">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="9600e-250">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9600e-251">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="9600e-251">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9600e-252">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-253">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9600e-253">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-254">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9600e-254">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9600e-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-256">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9600e-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-257">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9600e-257">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-258">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9600e-258">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-260">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="9600e-260">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="9600e-261">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-262">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9600e-262">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-263">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9600e-265">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="9600e-265">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9600e-266">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="9600e-266">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9600e-267">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-267">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-268">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9600e-268">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-269">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9600e-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-271">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-272">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="9600e-272">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-273">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9600e-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-275">此控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="9600e-275">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="9600e-276">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="9600e-276">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="9600e-277">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9600e-277">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="9600e-278">這個屬性會繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)，而且會設定為1。</span><span class="sxs-lookup"><span data-stu-id="9600e-278">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="9600e-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-280">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9600e-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-282">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-283">**名稱**</span><span class="sxs-lookup"><span data-stu-id="9600e-283">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-284">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-286">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="9600e-286">The label by which the object is known.</span></span> <span data-ttu-id="9600e-287">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-288">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9600e-288">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-289">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-291">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9600e-291">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9600e-292">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9600e-292">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9600e-293">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9600e-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9600e-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="9600e-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="9600e-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="9600e-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="9600e-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="9600e-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="9600e-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="9600e-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="9600e-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="9600e-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="9600e-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="9600e-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="9600e-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="9600e-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="9600e-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="9600e-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="9600e-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="9600e-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="9600e-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9600e-313">)</span><span class="sxs-lookup"><span data-stu-id="9600e-313">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9600e-314">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9600e-314">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-315">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9600e-315">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9600e-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-317">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-317">The current statuses of the object.</span></span> <span data-ttu-id="9600e-318">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-319">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9600e-319">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-322">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-322">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9600e-323">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="9600e-323">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9600e-324">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9600e-324">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-325">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="9600e-325">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-326">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9600e-326">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9600e-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-328">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9600e-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-329">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9600e-329">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-330">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="9600e-330">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9600e-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-332">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-332">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-333">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9600e-333">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-334">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9600e-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-336">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-337">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9600e-337">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-338">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9600e-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-340">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-341">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9600e-341">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-342">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-342">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-344">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9600e-344">Provides high level status information.</span></span> <span data-ttu-id="9600e-345">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-345">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9600e-346">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="9600e-346">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9600e-347">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9600e-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="9600e-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-349"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="9600e-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="9600e-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="9600e-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="9600e-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9600e-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="9600e-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9600e-354">)</span><span class="sxs-lookup"><span data-stu-id="9600e-354">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9600e-355">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="9600e-355">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-356">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-358">提供與控制器所支援的通訊協定相關之詳細資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="9600e-358">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="9600e-359">這個屬性會繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)，且會設定為「磁片協定」。</span><span class="sxs-lookup"><span data-stu-id="9600e-359">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to "Diskette Protocol".</span></span>

</dd> <dt>

<span data-ttu-id="9600e-360">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="9600e-360">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-361">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-363">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9600e-363">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="9600e-364">這個屬性會繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)，而且會設定為 7 (彈性的磁片) 。</span><span class="sxs-lookup"><span data-stu-id="9600e-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 7 (Flexible Diskette).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-365">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9600e-365">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-366">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-368">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-368">The last requested or desired state for the element.</span></span> <span data-ttu-id="9600e-369">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="9600e-369">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9600e-370">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-370">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="9600e-371">啟用的邏輯元素的特定實例可能不支援 **RequestedStateChange**。</span><span class="sxs-lookup"><span data-stu-id="9600e-371">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="9600e-372">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="9600e-372">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="9600e-373">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9600e-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-374">**狀態**</span><span class="sxs-lookup"><span data-stu-id="9600e-374">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-375">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-377">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9600e-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-379">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="9600e-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9600e-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-381">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="9600e-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9600e-382">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="9600e-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9600e-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-384">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-386">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-387">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9600e-387">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-388">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-390">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="9600e-390">The scoping system's creation class name.</span></span> <span data-ttu-id="9600e-391">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="9600e-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-392">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9600e-392">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-393">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9600e-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-395">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9600e-395">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="9600e-396">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="9600e-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-397">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="9600e-397">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-398">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9600e-398">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-400">虛擬機器的上次開機時間。</span><span class="sxs-lookup"><span data-stu-id="9600e-400">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="9600e-401">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="9600e-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="9600e-402">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9600e-402">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-403">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="9600e-403">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-405">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="9600e-405">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9600e-406">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9600e-406">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-407">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="9600e-407">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-408">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="9600e-408">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-410">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="9600e-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9600e-411">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9600e-411">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9600e-412">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="9600e-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9600e-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="9600e-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9600e-414">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="9600e-414">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9600e-415">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="9600e-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9600e-416">備註</span><span class="sxs-lookup"><span data-stu-id="9600e-416">Remarks</span></span>

<span data-ttu-id="9600e-417">存取 **Msvm \_ DisketteController** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="9600e-417">Access to the **Msvm\_DisketteController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9600e-418">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="9600e-418">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9600e-419">規格需求</span><span class="sxs-lookup"><span data-stu-id="9600e-419">Requirements</span></span>



| <span data-ttu-id="9600e-420">需求</span><span class="sxs-lookup"><span data-stu-id="9600e-420">Requirement</span></span> | <span data-ttu-id="9600e-421">值</span><span class="sxs-lookup"><span data-stu-id="9600e-421">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9600e-422">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9600e-422">Minimum supported client</span></span><br/> | <span data-ttu-id="9600e-423">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9600e-423">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9600e-424">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9600e-424">Minimum supported server</span></span><br/> | <span data-ttu-id="9600e-425">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9600e-425">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9600e-426">命名空間</span><span class="sxs-lookup"><span data-stu-id="9600e-426">Namespace</span></span><br/>                | <span data-ttu-id="9600e-427">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="9600e-427">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9600e-428">MOF</span><span class="sxs-lookup"><span data-stu-id="9600e-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9600e-429"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-429"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9600e-430">DLL</span><span class="sxs-lookup"><span data-stu-id="9600e-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9600e-431"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9600e-431"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9600e-432">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9600e-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9600e-433">**CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="9600e-433">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="9600e-434">**CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="9600e-434">**CIM\_Controller**</span></span>](/windows/desktop/CIMWin32Prov/cim-controller)
</dt> <dt>

[<span data-ttu-id="9600e-435">儲存類別</span><span class="sxs-lookup"><span data-stu-id="9600e-435">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

