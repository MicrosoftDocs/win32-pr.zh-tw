---
description: 代表鍵盤裝置。
ms.assetid: 2a59fe90-12e2-471c-b49e-dfb4f4a31e0c
title: Msvm_Keyboard 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard
- Msvm_Keyboard.SetPowerState
- Msvm_Keyboard.EnableDevice
- Msvm_Keyboard.OnlineDevice
- Msvm_Keyboard.QuiesceDevice
- Msvm_Keyboard.SaveProperties
- Msvm_Keyboard.RestoreProperties
- Msvm_Keyboard.InstanceID
- Msvm_Keyboard.Caption
- Msvm_Keyboard.Description
- Msvm_Keyboard.ElementName
- Msvm_Keyboard.InstallDate
- Msvm_Keyboard.Name
- Msvm_Keyboard.OperationalStatus
- Msvm_Keyboard.StatusDescriptions
- Msvm_Keyboard.Status
- Msvm_Keyboard.HealthState
- Msvm_Keyboard.CommunicationStatus
- Msvm_Keyboard.DetailedStatus
- Msvm_Keyboard.OperatingStatus
- Msvm_Keyboard.PrimaryStatus
- Msvm_Keyboard.EnabledState
- Msvm_Keyboard.OtherEnabledState
- Msvm_Keyboard.RequestedState
- Msvm_Keyboard.EnabledDefault
- Msvm_Keyboard.TimeOfLastStateChange
- Msvm_Keyboard.AvailableRequestedStates
- Msvm_Keyboard.TransitioningToState
- Msvm_Keyboard.SystemCreationClassName
- Msvm_Keyboard.SystemName
- Msvm_Keyboard.CreationClassName
- Msvm_Keyboard.DeviceID
- Msvm_Keyboard.PowerManagementSupported
- Msvm_Keyboard.PowerManagementCapabilities
- Msvm_Keyboard.Availability
- Msvm_Keyboard.StatusInfo
- Msvm_Keyboard.LastErrorCode
- Msvm_Keyboard.ErrorDescription
- Msvm_Keyboard.ErrorCleared
- Msvm_Keyboard.OtherIdentifyingInfo
- Msvm_Keyboard.PowerOnHours
- Msvm_Keyboard.TotalPowerOnHours
- Msvm_Keyboard.IdentifyingDescriptions
- Msvm_Keyboard.AdditionalAvailability
- Msvm_Keyboard.MaxQuiesceTime
- Msvm_Keyboard.IsLocked
- Msvm_Keyboard.Layout
- Msvm_Keyboard.NumberOfFunctionKeys
- Msvm_Keyboard.Password
- Msvm_Keyboard.UnicodeSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37c4faceb9072c1851868eb23c031e715cb6e1c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026728"
---
# <a name="msvm_keyboard-class"></a><span data-ttu-id="ec889-103">Msvm \_ 鍵盤類別</span><span class="sxs-lookup"><span data-stu-id="ec889-103">Msvm\_Keyboard class</span></span>

<span data-ttu-id="ec889-104">代表鍵盤裝置。</span><span class="sxs-lookup"><span data-stu-id="ec889-104">Represents a keyboard device.</span></span> <span data-ttu-id="ec889-105">鍵盤是一律存在於虛擬機器中的邏輯裝置，因此不會透過資源集區配置。</span><span class="sxs-lookup"><span data-stu-id="ec889-105">Keyboards are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="ec889-106">一個實例一律存在於虛擬電腦系統中。</span><span class="sxs-lookup"><span data-stu-id="ec889-106">One instance is always present in a virtual computer system.</span></span>

<span data-ttu-id="ec889-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec889-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec889-108">語法</span><span class="sxs-lookup"><span data-stu-id="ec889-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Keyboard : CIM_UserDevice
{
  string   InstanceID;
  string   Caption = "Keyboard";
  string   Description = "Microsoft Virtual Keyboard";
  string   ElementName = "Keyboard";
  datetime InstallDate;
  string   Name = "Keyboard";
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
  string   CreationClassName = "Msvm_Keyboard";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  boolean  IsLocked = False;
  string   Layout = "00000409";
  uint16   NumberOfFunctionKeys = 12;
  uint16   Password = 5;
  boolean  UnicodeSupported;
};
```

## <a name="members"></a><span data-ttu-id="ec889-109">成員</span><span class="sxs-lookup"><span data-stu-id="ec889-109">Members</span></span>

<span data-ttu-id="ec889-110">**Msvm \_ 鍵盤** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ec889-110">The **Msvm\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="ec889-111">方法</span><span class="sxs-lookup"><span data-stu-id="ec889-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ec889-112">屬性</span><span class="sxs-lookup"><span data-stu-id="ec889-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ec889-113">方法</span><span class="sxs-lookup"><span data-stu-id="ec889-113">Methods</span></span>

<span data-ttu-id="ec889-114">**Msvm \_ 鍵盤** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ec889-114">The **Msvm\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="ec889-115">方法</span><span class="sxs-lookup"><span data-stu-id="ec889-115">Method</span></span>                                                         | <span data-ttu-id="ec889-116">描述</span><span class="sxs-lookup"><span data-stu-id="ec889-116">Description</span></span>                                                   |
|:---------------------------------------------------------------|:--------------------------------------------------------------|
| <span data-ttu-id="ec889-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="ec889-117">**EnableDevice**</span></span>                                               | <span data-ttu-id="ec889-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="ec889-118">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="ec889-119">**IsKeyPressed**</span><span class="sxs-lookup"><span data-stu-id="ec889-119">**IsKeyPressed**</span></span>](iskeypressed-msvm-keyboard.md)             | <span data-ttu-id="ec889-120">捕獲索引鍵的索引鍵狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-120">Retrieves the key state of a key.</span></span><br/>                  |
| <span data-ttu-id="ec889-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="ec889-121">**OnlineDevice**</span></span>                                               | <span data-ttu-id="ec889-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="ec889-122">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="ec889-123">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="ec889-123">**PressKey**</span></span>](presskey-msvm-keyboard.md)                     | <span data-ttu-id="ec889-124">模擬按鍵的按鍵。</span><span class="sxs-lookup"><span data-stu-id="ec889-124">Simulates a key press.</span></span><br/>                             |
| <span data-ttu-id="ec889-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="ec889-125">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="ec889-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="ec889-126">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="ec889-127">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="ec889-127">**ReleaseKey**</span></span>](releasekey-msvm-keyboard.md)                 | <span data-ttu-id="ec889-128">模擬金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="ec889-128">Simulates a key release.</span></span><br/>                           |
| [<span data-ttu-id="ec889-129">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ec889-129">**RequestStateChange**</span></span>](msvm-keyboard-requeststatechange.md) | <span data-ttu-id="ec889-130">要求變更元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-130">Requests that the state of the element be changed.</span></span><br/> |
| [<span data-ttu-id="ec889-131">**重設**</span><span class="sxs-lookup"><span data-stu-id="ec889-131">**Reset**</span></span>](msvm-keyboard-reset.md)                           | <span data-ttu-id="ec889-132">重設虛擬鍵盤。</span><span class="sxs-lookup"><span data-stu-id="ec889-132">Resets the virtual keyboard.</span></span><br/>                       |
| <span data-ttu-id="ec889-133">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="ec889-133">**RestoreProperties**</span></span>                                          | <span data-ttu-id="ec889-134">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="ec889-134">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="ec889-135">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="ec889-135">**SaveProperties**</span></span>                                             | <span data-ttu-id="ec889-136">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="ec889-136">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="ec889-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ec889-137">**SetPowerState**</span></span>                                              | <span data-ttu-id="ec889-138">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="ec889-138">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="ec889-139">**TypeCtrlAltDel**</span><span class="sxs-lookup"><span data-stu-id="ec889-139">**TypeCtrlAltDel**</span></span>](typectrlaltdel-msvm-keyboard.md)         | <span data-ttu-id="ec889-140">模擬 Ctrl + Alt + Del 鍵序列。</span><span class="sxs-lookup"><span data-stu-id="ec889-140">Simulates a Ctrl+Alt+Del key sequence.</span></span><br/>             |
| [<span data-ttu-id="ec889-141">**TypeKey**</span><span class="sxs-lookup"><span data-stu-id="ec889-141">**TypeKey**</span></span>](typekey-msvm-keyboard.md)                       | <span data-ttu-id="ec889-142">模擬電子報按鍵序列。</span><span class="sxs-lookup"><span data-stu-id="ec889-142">Simulates a press-release key sequence.</span></span><br/>            |
| [<span data-ttu-id="ec889-143">**TypeScancodes**</span><span class="sxs-lookup"><span data-stu-id="ec889-143">**TypeScancodes**</span></span>](msvm-keyboard-typescancodes.md)           | <span data-ttu-id="ec889-144">使用掃描碼來模擬按鍵序列。</span><span class="sxs-lookup"><span data-stu-id="ec889-144">Simulates a key sequence using scan codes.</span></span><br/>         |
| [<span data-ttu-id="ec889-145">**TypeText**</span><span class="sxs-lookup"><span data-stu-id="ec889-145">**TypeText**</span></span>](typetext-msvm-keyboard.md)                     | <span data-ttu-id="ec889-146">模擬一連串的類型字元。</span><span class="sxs-lookup"><span data-stu-id="ec889-146">Simulates a series of typed characters.</span></span><br/>            |



 

### <a name="properties"></a><span data-ttu-id="ec889-147">屬性</span><span class="sxs-lookup"><span data-stu-id="ec889-147">Properties</span></span>

<span data-ttu-id="ec889-148">**Msvm \_ 鍵盤** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ec889-148">The **Msvm\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec889-149">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="ec889-149">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-150">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ec889-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ec889-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-152">裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="ec889-152">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="ec889-153">**Availability** 屬性代表裝置的主要狀態和可用性。</span><span class="sxs-lookup"><span data-stu-id="ec889-153">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="ec889-154">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="ec889-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-155">**可用性**</span><span class="sxs-lookup"><span data-stu-id="ec889-155">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-156">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-158">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-158">The primary availability and status of the device.</span></span> <span data-ttu-id="ec889-159">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="ec889-159">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-160">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="ec889-160">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-161">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ec889-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ec889-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-163">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="ec889-163">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="ec889-164">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ec889-164">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-165">**標題**</span><span class="sxs-lookup"><span data-stu-id="ec889-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec889-168">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="ec889-168">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ec889-169">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="ec889-169">A short description of the object.</span></span> <span data-ttu-id="ec889-170">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-171">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ec889-171">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-172">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-174">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="ec889-174">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ec889-175">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec889-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ec889-176">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ec889-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ec889-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="ec889-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="ec889-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="ec889-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="ec889-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="ec889-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="ec889-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ec889-184">)</span><span class="sxs-lookup"><span data-stu-id="ec889-184">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ec889-185">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ec889-185">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec889-188">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="ec889-188">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ec889-189">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec889-189">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ec889-190">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="ec889-190">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="ec889-191">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="ec889-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-192">**說明**</span><span class="sxs-lookup"><span data-stu-id="ec889-192">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-195">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="ec889-195">A description of the object.</span></span> <span data-ttu-id="ec889-196">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-197">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ec889-197">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-198">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-200">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ec889-200">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ec889-201">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec889-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ec889-202">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ec889-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="ec889-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="ec889-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="ec889-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="ec889-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="ec889-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="ec889-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="ec889-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="ec889-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ec889-211">)</span><span class="sxs-lookup"><span data-stu-id="ec889-211">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ec889-212">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ec889-212">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-215">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="ec889-215">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="ec889-216">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="ec889-216">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="ec889-217">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ec889-217">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-218">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-220">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ec889-220">A display name for the object.</span></span> <span data-ttu-id="ec889-221">除了索引鍵屬性、身分識別資料和描述資訊之外，此屬性還可讓每個實例定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ec889-221">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="ec889-222">**CIM \_ ManagedSystemElement** 類別的 [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)屬性也會定義為顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ec889-222">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="ec889-223">但是，它通常是一個重要的子類別。</span><span class="sxs-lookup"><span data-stu-id="ec889-223">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="ec889-224">相同的屬性可以同時傳達身分識別和顯示名稱，而不會有不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="ec889-224">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="ec889-225">如果 **名稱** 存在，而且不是 (的索引鍵（例如針對 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)) 的實例），則 **名稱** 和 **ElementName** 屬性中都可以同時存在相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="ec889-225">Where **Name** exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="ec889-226">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="ec889-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-228">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-230">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ec889-231">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ec889-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ec889-232">值</span><span class="sxs-lookup"><span data-stu-id="ec889-232">Value</span></span>                                                                        | <span data-ttu-id="ec889-233">意義</span><span class="sxs-lookup"><span data-stu-id="ec889-233">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="ec889-234"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-234"><dt>2</dt></span></span> </dl> | <span data-ttu-id="ec889-235">已啟用</span><span class="sxs-lookup"><span data-stu-id="ec889-235">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ec889-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ec889-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-237">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-239">指出專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-239">Indicates the enabled and disabled states of an element.</span></span> <span data-ttu-id="ec889-240">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="ec889-240">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="ec889-241">例如，關閉 (值 = 4) 和啟動 (值 = 10) 是啟用和停用之間的暫時性狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-241">For example, shutting down (value=4) and starting (value=10) are transient states between enabled and disabled.</span></span>



| <span data-ttu-id="ec889-242">值</span><span class="sxs-lookup"><span data-stu-id="ec889-242">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="ec889-243">意義</span><span class="sxs-lookup"><span data-stu-id="ec889-243">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="ec889-244"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-244"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="ec889-245">Unknown</span><span class="sxs-lookup"><span data-stu-id="ec889-245">Unknown</span></span><br/>                                                                                                                                                                                              |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="ec889-246"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-246"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="ec889-247">其他</span><span class="sxs-lookup"><span data-stu-id="ec889-247">Other</span></span><br/>                                                                                                                                                                                                |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="ec889-248"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-248"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="ec889-249">元素是或可能正在執行命令、將會處理任何已排入佇列的命令，並將新的要求排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ec889-249">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="ec889-250"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-250"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="ec889-251">元素將不會執行命令，而且會卸載任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="ec889-251">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="ec889-252">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-252"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="ec889-253">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="ec889-253">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="ec889-254"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-254"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="ec889-255">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="ec889-255">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="ec889-256"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-256"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="ec889-257">元素可能正在完成命令，並會卸載任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="ec889-257">The element might be completing commands and will drop any new requests.</span></span><br/>                                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="ec889-258"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="ec889-258"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="ec889-259">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-259">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="ec889-260"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-260"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="ec889-261">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="ec889-261">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="ec889-262"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-262"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="ec889-263">元素已啟用但處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="ec889-263">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="ec889-264">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="ec889-264">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="ec889-265">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ec889-265">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="ec889-266"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-266"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="ec889-267">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="ec889-267">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="ec889-268">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ec889-268">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="ec889-269"><dt>**DMTF 保留**</dt>的 <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-269"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="ec889-270">此值為 reserved。</span><span class="sxs-lookup"><span data-stu-id="ec889-270">This value is reserved.</span></span><br/>                                                                                                                                                                              |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="ec889-271"><dt>**廠商保留**</dt>的 <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-271"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="ec889-272">此值為 reserved。</span><span class="sxs-lookup"><span data-stu-id="ec889-272">This value is reserved.</span></span><br/>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="ec889-273">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ec889-273">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-274">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ec889-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-276">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec889-276">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="ec889-277">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-277">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-278">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ec889-278">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-281">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ec889-281">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="ec889-282">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-283">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ec889-283">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-284">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-286">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="ec889-286">The current health of the element.</span></span> <span data-ttu-id="ec889-287">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="ec889-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ec889-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-289">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ec889-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ec889-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-291">自由格式字串的陣列，提供 **OtherIdentifyingInfo** 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ec889-291">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="ec889-292">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="ec889-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ec889-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-294">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ec889-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-296">建立虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ec889-296">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="ec889-297">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ec889-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-299">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec889-301">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="ec889-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ec889-302">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="ec889-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ec889-303">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="ec889-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-305">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ec889-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-307">指出裝置是否已鎖定，防止使用者輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="ec889-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="ec889-308">這個屬性繼承自 [**CIM \_ UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice)。</span><span class="sxs-lookup"><span data-stu-id="ec889-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ec889-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-310">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ec889-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-312">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ec889-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="ec889-313">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-314">**版面配置**</span><span class="sxs-lookup"><span data-stu-id="ec889-314">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-315">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-317">字串，表示鍵盤的格式和配置。</span><span class="sxs-lookup"><span data-stu-id="ec889-317">A string indicating the format and layout of the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-318">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="ec889-318">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-319">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ec889-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-321">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="ec889-321">This property has been deprecated.</span></span> <span data-ttu-id="ec889-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-323">**名稱**</span><span class="sxs-lookup"><span data-stu-id="ec889-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec889-326">限定詞： **MaxLen** (1024) </span><span class="sxs-lookup"><span data-stu-id="ec889-326">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="ec889-327">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="ec889-327">The label by which the object is known.</span></span> <span data-ttu-id="ec889-328">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="ec889-328">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="ec889-329">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-330">**NumberOfFunctionKeys**</span><span class="sxs-lookup"><span data-stu-id="ec889-330">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-331">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-333">鍵盤上的功能鍵數目。</span><span class="sxs-lookup"><span data-stu-id="ec889-333">The number of function keys on the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-334">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ec889-334">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-335">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-337">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ec889-337">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ec889-338">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec889-338">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ec889-339">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ec889-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ec889-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="ec889-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="ec889-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="ec889-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="ec889-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="ec889-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="ec889-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="ec889-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="ec889-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="ec889-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="ec889-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="ec889-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="ec889-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="ec889-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="ec889-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="ec889-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="ec889-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="ec889-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="ec889-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ec889-359">)</span><span class="sxs-lookup"><span data-stu-id="ec889-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ec889-360">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ec889-360">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-361">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ec889-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ec889-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-363">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-363">The current status of the element.</span></span> <span data-ttu-id="ec889-364">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="ec889-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-365">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="ec889-365">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-366">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-368">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="ec889-368">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ec889-369">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ec889-369">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="ec889-370">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="ec889-370">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-371">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ec889-371">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-372">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ec889-372">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ec889-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-374">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="ec889-374">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="ec889-375">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ec889-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-376">**密碼**</span><span class="sxs-lookup"><span data-stu-id="ec889-376">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-377">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-379">指出是否已在鍵盤上啟用硬體層級密碼，以防止本機輸入。</span><span class="sxs-lookup"><span data-stu-id="ec889-379">Indicates whether a hardware-level password is enabled at the keyboard, preventing local input.</span></span>

<dt>

<span data-ttu-id="ec889-380">5</span><span class="sxs-lookup"><span data-stu-id="ec889-380">5</span></span>
</dt> <dd>

<span data-ttu-id="ec889-381">未實作。</span><span class="sxs-lookup"><span data-stu-id="ec889-381">Not implemented.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec889-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ec889-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-383">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="ec889-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ec889-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-385">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="ec889-385">The power management capabilities of the device.</span></span> <span data-ttu-id="ec889-386">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ec889-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-388">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ec889-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-390">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="ec889-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="ec889-391">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ec889-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-393">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ec889-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-395">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="ec889-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="ec889-396">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ec889-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-398">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-400">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="ec889-400">Provides high level status information.</span></span> <span data-ttu-id="ec889-401">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="ec889-402">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="ec889-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ec889-403">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="ec889-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ec889-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ec889-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-405"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="ec889-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="ec889-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="ec889-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="ec889-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ec889-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="ec889-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ec889-410">)</span><span class="sxs-lookup"><span data-stu-id="ec889-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ec889-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ec889-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-412">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-414">最後要求的元素狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-414">The last requested state for the element.</span></span>



| <span data-ttu-id="ec889-415">值</span><span class="sxs-lookup"><span data-stu-id="ec889-415">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="ec889-416">意義</span><span class="sxs-lookup"><span data-stu-id="ec889-416">Meaning</span></span>                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="ec889-417"><dt>**不適用**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-417"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="ec889-418">不適用。</span><span class="sxs-lookup"><span data-stu-id="ec889-418">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ec889-419">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ec889-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-420">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-422">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ec889-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-424">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ec889-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ec889-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-426">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="ec889-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ec889-427">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="ec889-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="ec889-428">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ec889-428">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-429">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-431">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-431">The current state of the logical device.</span></span> <span data-ttu-id="ec889-432">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ec889-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec889-436">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="ec889-436">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ec889-437">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="ec889-437">The scoping system's creation class name.</span></span> <span data-ttu-id="ec889-438">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 "Msvm \_ "。</span><span class="sxs-lookup"><span data-stu-id="ec889-438">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="ec889-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ec889-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-440">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ec889-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec889-442">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="ec889-442">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ec889-443">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec889-443">The scoping system's name.</span></span> <span data-ttu-id="ec889-444">此值會對應至範圍虛擬機器之 Msvm 的非程式類型類別的 **名稱** 屬性值。 [**\_**](msvm-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="ec889-444">This value corresponds to the value of the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for the scoping virtual machine.</span></span> <span data-ttu-id="ec889-445">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="ec889-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ec889-446">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="ec889-446">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-447">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ec889-447">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-448">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-449">專案的已啟用狀態上次變更的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="ec889-449">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ec889-450">如果未變更元素的狀態，且已填入此屬性，則必須將它設定為0間隔值。</span><span class="sxs-lookup"><span data-stu-id="ec889-450">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="ec889-451">如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。</span><span class="sxs-lookup"><span data-stu-id="ec889-451">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="ec889-452">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ec889-452">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-453">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ec889-453">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-454">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ec889-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-456">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="ec889-456">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="ec889-457">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="ec889-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-458">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="ec889-458">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-459">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ec889-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-461">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="ec889-461">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ec889-462">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ec889-462">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ec889-463">**UnicodeSupported**</span><span class="sxs-lookup"><span data-stu-id="ec889-463">**UnicodeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec889-464">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ec889-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec889-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ec889-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec889-466">指出虛擬鍵盤是否支援 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="ec889-466">Indicates if the virtual keyboard supports Unicode characters.</span></span> <span data-ttu-id="ec889-467">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ec889-467">This can be one of the following values.</span></span>



| <span data-ttu-id="ec889-468">值</span><span class="sxs-lookup"><span data-stu-id="ec889-468">Value</span></span>                                                                            | <span data-ttu-id="ec889-469">意義</span><span class="sxs-lookup"><span data-stu-id="ec889-469">Meaning</span></span>                                                              |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec889-470"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-470"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="ec889-471">虛擬鍵盤支援 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="ec889-471">The virtual keyboard supports Unicode characters.</span></span><br/>         |
| <dl> <span data-ttu-id="ec889-472"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-472"><dt>False</dt></span></span> </dl> | <span data-ttu-id="ec889-473">虛擬鍵盤不支援 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="ec889-473">The virtual keyboard does not support Unicode characters.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec889-474">備註</span><span class="sxs-lookup"><span data-stu-id="ec889-474">Remarks</span></span>

<span data-ttu-id="ec889-475">**Msvm \_ 鍵盤** 類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="ec889-475">Access to the **Msvm\_Keyboard** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ec889-476">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="ec889-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec889-477">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec889-477">Requirements</span></span>



| <span data-ttu-id="ec889-478">需求</span><span class="sxs-lookup"><span data-stu-id="ec889-478">Requirement</span></span> | <span data-ttu-id="ec889-479">值</span><span class="sxs-lookup"><span data-stu-id="ec889-479">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec889-480">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec889-480">Minimum supported client</span></span><br/> | <span data-ttu-id="ec889-481">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec889-481">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ec889-482">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec889-482">Minimum supported server</span></span><br/> | <span data-ttu-id="ec889-483">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec889-483">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec889-484">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec889-484">Namespace</span></span><br/>                | <span data-ttu-id="ec889-485">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="ec889-485">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ec889-486">MOF</span><span class="sxs-lookup"><span data-stu-id="ec889-486">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec889-487"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-487"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec889-488">DLL</span><span class="sxs-lookup"><span data-stu-id="ec889-488">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec889-489"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec889-489"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec889-490">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec889-490">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec889-491">**CIM \_ UserDevice**</span><span class="sxs-lookup"><span data-stu-id="ec889-491">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dt>

[<span data-ttu-id="ec889-492">**CIM \_ UserDevice**</span><span class="sxs-lookup"><span data-stu-id="ec889-492">**CIM\_UserDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-userdevice)
</dt> <dt>

[<span data-ttu-id="ec889-493">輸入類別</span><span class="sxs-lookup"><span data-stu-id="ec889-493">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

