---
description: 代表 IDE 控制器。
ms.assetid: DFD4D90E-CA91-42B3-AC88-9E9D26089C36
title: Msvm_IDEController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_IDEController
- Msvm_IDEController.SetPowerState
- Msvm_IDEController.EnableDevice
- Msvm_IDEController.OnlineDevice
- Msvm_IDEController.QuiesceDevice
- Msvm_IDEController.SaveProperties
- Msvm_IDEController.RestoreProperties
- Msvm_IDEController.InstanceID
- Msvm_IDEController.Caption
- Msvm_IDEController.Description
- Msvm_IDEController.ElementName
- Msvm_IDEController.InstallDate
- Msvm_IDEController.Name
- Msvm_IDEController.OperationalStatus
- Msvm_IDEController.StatusDescriptions
- Msvm_IDEController.Status
- Msvm_IDEController.HealthState
- Msvm_IDEController.CommunicationStatus
- Msvm_IDEController.DetailedStatus
- Msvm_IDEController.OperatingStatus
- Msvm_IDEController.PrimaryStatus
- Msvm_IDEController.EnabledState
- Msvm_IDEController.OtherEnabledState
- Msvm_IDEController.RequestedState
- Msvm_IDEController.EnabledDefault
- Msvm_IDEController.TimeOfLastStateChange
- Msvm_IDEController.AvailableRequestedStates
- Msvm_IDEController.TransitioningToState
- Msvm_IDEController.SystemCreationClassName
- Msvm_IDEController.SystemName
- Msvm_IDEController.CreationClassName
- Msvm_IDEController.DeviceID
- Msvm_IDEController.PowerManagementSupported
- Msvm_IDEController.PowerManagementCapabilities
- Msvm_IDEController.Availability
- Msvm_IDEController.StatusInfo
- Msvm_IDEController.LastErrorCode
- Msvm_IDEController.ErrorDescription
- Msvm_IDEController.ErrorCleared
- Msvm_IDEController.OtherIdentifyingInfo
- Msvm_IDEController.PowerOnHours
- Msvm_IDEController.TotalPowerOnHours
- Msvm_IDEController.IdentifyingDescriptions
- Msvm_IDEController.AdditionalAvailability
- Msvm_IDEController.MaxQuiesceTime
- Msvm_IDEController.TimeOfLastReset
- Msvm_IDEController.ProtocolSupported
- Msvm_IDEController.MaxNumberControlled
- Msvm_IDEController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25da1bddfa029ca5a6892006283e322d91a328a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971437"
---
# <a name="msvm_idecontroller-class"></a><span data-ttu-id="0ed09-103">Msvm \_ IDEController 類別</span><span class="sxs-lookup"><span data-stu-id="0ed09-103">Msvm\_IDEController class</span></span>

<span data-ttu-id="0ed09-104">代表 IDE 控制器。</span><span class="sxs-lookup"><span data-stu-id="0ed09-104">Represents an IDE controller.</span></span> <span data-ttu-id="0ed09-105">此類別最多可支援四個連接到控制器的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="0ed09-105">This class can support up to four drives attached to the controller.</span></span> <span data-ttu-id="0ed09-106">IDE 控制器已在虛擬機器中修正，因此沒有相關聯的資源集區。</span><span class="sxs-lookup"><span data-stu-id="0ed09-106">The IDE controller is fixed in the virtual machine and therefore does not have a resource pool associated with it.</span></span>

> [!Note]  
> <span data-ttu-id="0ed09-107">第2代虛擬機器無法使用此類別。</span><span class="sxs-lookup"><span data-stu-id="0ed09-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="0ed09-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ed09-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed09-109">語法</span><span class="sxs-lookup"><span data-stu-id="0ed09-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_IDEController : CIM_IDEController
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual IDE Controller";
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
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_IDEController";
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
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 37;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription = "IDE";
};
```

## <a name="members"></a><span data-ttu-id="0ed09-110">成員</span><span class="sxs-lookup"><span data-stu-id="0ed09-110">Members</span></span>

<span data-ttu-id="0ed09-111">**Msvm \_ IDEController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0ed09-111">The **Msvm\_IDEController** class has these types of members:</span></span>

-   [<span data-ttu-id="0ed09-112">方法</span><span class="sxs-lookup"><span data-stu-id="0ed09-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0ed09-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0ed09-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0ed09-114">方法</span><span class="sxs-lookup"><span data-stu-id="0ed09-114">Methods</span></span>

<span data-ttu-id="0ed09-115">**Msvm \_ IDEController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0ed09-115">The **Msvm\_IDEController** class has these methods.</span></span>



| <span data-ttu-id="0ed09-116">方法</span><span class="sxs-lookup"><span data-stu-id="0ed09-116">Method</span></span>                                                              | <span data-ttu-id="0ed09-117">描述</span><span class="sxs-lookup"><span data-stu-id="0ed09-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="0ed09-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="0ed09-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="0ed09-119">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ed09-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0ed09-120">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="0ed09-120">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="0ed09-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ed09-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0ed09-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="0ed09-122">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="0ed09-123">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ed09-123">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="0ed09-124">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0ed09-124">**RequestStateChange**</span></span>](msvm-idecontroller-requeststatechange.md) | <span data-ttu-id="0ed09-125">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0ed09-125">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="0ed09-126">**重設**</span><span class="sxs-lookup"><span data-stu-id="0ed09-126">**Reset**</span></span>](msvm-idecontroller-reset.md)                           | <span data-ttu-id="0ed09-127">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="0ed09-127">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="0ed09-128">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="0ed09-128">**RestoreProperties**</span></span>                                               | <span data-ttu-id="0ed09-129">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ed09-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0ed09-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="0ed09-130">**SaveProperties**</span></span>                                                  | <span data-ttu-id="0ed09-131">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ed09-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0ed09-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0ed09-132">**SetPowerState**</span></span>                                                   | <span data-ttu-id="0ed09-133">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="0ed09-133">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0ed09-134">屬性</span><span class="sxs-lookup"><span data-stu-id="0ed09-134">Properties</span></span>

<span data-ttu-id="0ed09-135">**Msvm \_ IDEController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0ed09-135">The **Msvm\_IDEController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ed09-136">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="0ed09-136">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-137">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ed09-137">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-139">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-139">Any additional availability and status of the device.</span></span> <span data-ttu-id="0ed09-140">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-140">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-141">**可用性**</span><span class="sxs-lookup"><span data-stu-id="0ed09-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-142">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-144">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-144">The primary availability and status of the device.</span></span> <span data-ttu-id="0ed09-145">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-145">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-146">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0ed09-146">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-147">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ed09-147">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-149">指出用於起始狀態變更之 [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement)方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="0ed09-149">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="0ed09-150">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="0ed09-150">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="0ed09-151">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="0ed09-151">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="0ed09-152">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0ed09-152">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="0ed09-153">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ed09-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-154">**標題**</span><span class="sxs-lookup"><span data-stu-id="0ed09-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-157">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="0ed09-157">A short description of the object.</span></span> <span data-ttu-id="0ed09-158">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="0ed09-159">值</span><span class="sxs-lookup"><span data-stu-id="0ed09-159">Value</span></span>                                                                                         | <span data-ttu-id="0ed09-160">意義</span><span class="sxs-lookup"><span data-stu-id="0ed09-160">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="0ed09-161"><dt>"IDE 控制器 0"</dt></span><span class="sxs-lookup"><span data-stu-id="0ed09-161"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="0ed09-162">實例代表主要控制器。</span><span class="sxs-lookup"><span data-stu-id="0ed09-162">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="0ed09-163"><dt>"IDE 控制器 1"</dt></span><span class="sxs-lookup"><span data-stu-id="0ed09-163"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="0ed09-164">實例代表次要控制器。</span><span class="sxs-lookup"><span data-stu-id="0ed09-164">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0ed09-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0ed09-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-166">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-168">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="0ed09-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0ed09-169">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0ed09-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0ed09-170">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0ed09-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-174">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ed09-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0ed09-175">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-176">**說明**</span><span class="sxs-lookup"><span data-stu-id="0ed09-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-179">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="0ed09-179">A description of the object.</span></span> <span data-ttu-id="0ed09-180">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0ed09-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-182">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-184">補充具有其他狀態詳細資料的 **PrimaryStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ed09-184">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0ed09-185">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0ed09-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0ed09-186">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-187">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0ed09-187">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-190">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且會設定為 "Microsoft：*GUID* \\ *裝置特定資料*"。</span><span class="sxs-lookup"><span data-stu-id="0ed09-190">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0ed09-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-194">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0ed09-194">A display name for the object.</span></span> <span data-ttu-id="0ed09-195">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="0ed09-196">值</span><span class="sxs-lookup"><span data-stu-id="0ed09-196">Value</span></span>                                                                                         | <span data-ttu-id="0ed09-197">意義</span><span class="sxs-lookup"><span data-stu-id="0ed09-197">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="0ed09-198"><dt>"IDE 控制器 0"</dt></span><span class="sxs-lookup"><span data-stu-id="0ed09-198"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="0ed09-199">實例代表主要控制器。</span><span class="sxs-lookup"><span data-stu-id="0ed09-199">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="0ed09-200"><dt>"IDE 控制器 1"</dt></span><span class="sxs-lookup"><span data-stu-id="0ed09-200"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="0ed09-201">實例代表次要控制器。</span><span class="sxs-lookup"><span data-stu-id="0ed09-201">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0ed09-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0ed09-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-203">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-205">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0ed09-206">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ed09-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0ed09-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-210">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0ed09-211">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="0ed09-211">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0ed09-212">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ed09-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-213">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0ed09-213">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-214">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0ed09-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-216">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0ed09-216">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="0ed09-217">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-218">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0ed09-218">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-221">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ed09-221">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="0ed09-222">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-222">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-223">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0ed09-223">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-224">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-226">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="0ed09-226">The current health of the element.</span></span> <span data-ttu-id="0ed09-227">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="0ed09-227">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="0ed09-228">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="0ed09-228">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0ed09-229">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-230">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0ed09-230">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-231">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ed09-231">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-233">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0ed09-233">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="0ed09-234">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-235">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0ed09-235">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-236">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0ed09-236">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-237">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-238">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="0ed09-238">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0ed09-239">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-240">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0ed09-240">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-243">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="0ed09-243">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-244">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="0ed09-244">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0ed09-245">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-246">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0ed09-246">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-247">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0ed09-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-249">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0ed09-249">The last error code reported by the logical device.</span></span> <span data-ttu-id="0ed09-250">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-251">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="0ed09-251">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-252">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0ed09-252">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-254">此控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="0ed09-254">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="0ed09-255">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="0ed09-255">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="0ed09-256">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0ed09-256">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="0ed09-257">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-257">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-258">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="0ed09-258">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-259">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0ed09-259">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-260">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-261">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="0ed09-261">This property has been deprecated.</span></span> <span data-ttu-id="0ed09-262">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-262">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-263">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0ed09-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-266">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0ed09-266">The label by which the object is known.</span></span> <span data-ttu-id="0ed09-267">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="0ed09-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-268">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0ed09-268">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-269">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-271">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0ed09-271">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0ed09-272">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0ed09-272">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0ed09-273">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-274">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0ed09-274">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-275">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ed09-275">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-277">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-277">The current statuses of the object.</span></span> <span data-ttu-id="0ed09-278">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-278">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-279">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0ed09-279">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-280">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-282">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-282">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0ed09-283">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0ed09-283">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0ed09-284">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ed09-284">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-285">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0ed09-285">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-286">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ed09-286">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-288">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="0ed09-288">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="0ed09-289">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0ed09-289">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-290">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0ed09-290">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-291">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ed09-291">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-293">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="0ed09-293">The power management capabilities of the device.</span></span> <span data-ttu-id="0ed09-294">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-294">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-295">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0ed09-295">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-296">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0ed09-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-298">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="0ed09-298">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="0ed09-299">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-299">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-300">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0ed09-300">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-301">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0ed09-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-303">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="0ed09-303">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="0ed09-304">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-305">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0ed09-305">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-306">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-308">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0ed09-308">Provides high level status information.</span></span> <span data-ttu-id="0ed09-309">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="0ed09-309">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="0ed09-310">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="0ed09-310">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0ed09-311">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-312">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="0ed09-312">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-315">提供與控制器所支援的通訊協定相關之詳細資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="0ed09-315">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="0ed09-316">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-316">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-317">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="0ed09-317">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-318">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-318">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-320">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0ed09-320">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="0ed09-321">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-321">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="0ed09-322">值</span><span class="sxs-lookup"><span data-stu-id="0ed09-322">Value</span></span>                                                                         | <span data-ttu-id="0ed09-323">意義</span><span class="sxs-lookup"><span data-stu-id="0ed09-323">Meaning</span></span>        |
|-------------------------------------------------------------------------------|----------------|
| <dl> <span data-ttu-id="0ed09-324"><dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="0ed09-324"><dt>37</dt></span></span> </dl> | <span data-ttu-id="0ed09-325">IDE</span><span class="sxs-lookup"><span data-stu-id="0ed09-325">IDE</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0ed09-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0ed09-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-327">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-329">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-329">The last requested or desired state for the element.</span></span> <span data-ttu-id="0ed09-330">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="0ed09-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0ed09-331">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0ed09-332">啟用的邏輯元素的特定實例可能不支援 **RequestedStateChange**。</span><span class="sxs-lookup"><span data-stu-id="0ed09-332">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="0ed09-333">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="0ed09-333">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="0ed09-334">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ed09-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-335">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0ed09-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-338">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-338">The current status of the object.</span></span> <span data-ttu-id="0ed09-339">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-340">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0ed09-340">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-341">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0ed09-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-343">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="0ed09-343">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0ed09-344">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-344">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-345">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0ed09-345">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-346">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-348">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-348">The current state of the logical device.</span></span> <span data-ttu-id="0ed09-349">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-350">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0ed09-350">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-351">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-353">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="0ed09-353">The scoping system's creation class name.</span></span> <span data-ttu-id="0ed09-354">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-355">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0ed09-355">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-356">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0ed09-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-358">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="0ed09-358">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="0ed09-359">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-359">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-360">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="0ed09-360">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-361">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0ed09-361">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-363">虛擬機器的上次開機時間。</span><span class="sxs-lookup"><span data-stu-id="0ed09-363">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="0ed09-364">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0ed09-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-366">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0ed09-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-368">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="0ed09-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0ed09-369">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0ed09-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-370">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0ed09-370">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-371">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="0ed09-371">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-373">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="0ed09-373">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="0ed09-374">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-374">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0ed09-375">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0ed09-375">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ed09-376">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0ed09-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0ed09-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0ed09-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ed09-378">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="0ed09-378">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0ed09-379">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="0ed09-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ed09-380">備註</span><span class="sxs-lookup"><span data-stu-id="0ed09-380">Remarks</span></span>

<span data-ttu-id="0ed09-381">存取 **Msvm \_ IDEController** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="0ed09-381">Access to the **Msvm\_IDEController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0ed09-382">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="0ed09-382">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed09-383">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ed09-383">Requirements</span></span>



| <span data-ttu-id="0ed09-384">需求</span><span class="sxs-lookup"><span data-stu-id="0ed09-384">Requirement</span></span> | <span data-ttu-id="0ed09-385">值</span><span class="sxs-lookup"><span data-stu-id="0ed09-385">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed09-386">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ed09-386">Minimum supported client</span></span><br/> | <span data-ttu-id="0ed09-387">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ed09-387">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0ed09-388">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ed09-388">Minimum supported server</span></span><br/> | <span data-ttu-id="0ed09-389">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ed09-389">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ed09-390">命名空間</span><span class="sxs-lookup"><span data-stu-id="0ed09-390">Namespace</span></span><br/>                | <span data-ttu-id="0ed09-391">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0ed09-391">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0ed09-392">MOF</span><span class="sxs-lookup"><span data-stu-id="0ed09-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ed09-393"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0ed09-393"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ed09-394">DLL</span><span class="sxs-lookup"><span data-stu-id="0ed09-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ed09-395"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0ed09-395"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0ed09-396">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ed09-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed09-397">**CIM \_ IDEController**</span><span class="sxs-lookup"><span data-stu-id="0ed09-397">**CIM\_IDEController**</span></span>](cim-idecontroller.md)
</dt> <dt>

<span data-ttu-id="0ed09-398">[**CIM \_ IDEController**](/previous-versions//cc136863(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0ed09-398">[**CIM\_IDEController**](/previous-versions//cc136863(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0ed09-399">儲存類別</span><span class="sxs-lookup"><span data-stu-id="0ed09-399">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

