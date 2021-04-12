---
description: 表示 PS2 滑鼠裝置。
ms.assetid: 5e02ec15-95e6-4d82-833e-a48ca117a890
title: Msvm_Ps2Mouse 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse
- Msvm_Ps2Mouse.SetPowerState
- Msvm_Ps2Mouse.EnableDevice
- Msvm_Ps2Mouse.OnlineDevice
- Msvm_Ps2Mouse.QuiesceDevice
- Msvm_Ps2Mouse.SaveProperties
- Msvm_Ps2Mouse.RestoreProperties
- Msvm_Ps2Mouse.InstanceID
- Msvm_Ps2Mouse.Caption
- Msvm_Ps2Mouse.Description
- Msvm_Ps2Mouse.ElementName
- Msvm_Ps2Mouse.InstallDate
- Msvm_Ps2Mouse.Name
- Msvm_Ps2Mouse.OperationalStatus
- Msvm_Ps2Mouse.StatusDescriptions
- Msvm_Ps2Mouse.Status
- Msvm_Ps2Mouse.HealthState
- Msvm_Ps2Mouse.CommunicationStatus
- Msvm_Ps2Mouse.DetailedStatus
- Msvm_Ps2Mouse.OperatingStatus
- Msvm_Ps2Mouse.PrimaryStatus
- Msvm_Ps2Mouse.EnabledState
- Msvm_Ps2Mouse.OtherEnabledState
- Msvm_Ps2Mouse.RequestedState
- Msvm_Ps2Mouse.EnabledDefault
- Msvm_Ps2Mouse.TimeOfLastStateChange
- Msvm_Ps2Mouse.AvailableRequestedStates
- Msvm_Ps2Mouse.TransitioningToState
- Msvm_Ps2Mouse.SystemCreationClassName
- Msvm_Ps2Mouse.SystemName
- Msvm_Ps2Mouse.CreationClassName
- Msvm_Ps2Mouse.DeviceID
- Msvm_Ps2Mouse.PowerManagementSupported
- Msvm_Ps2Mouse.PowerManagementCapabilities
- Msvm_Ps2Mouse.Availability
- Msvm_Ps2Mouse.StatusInfo
- Msvm_Ps2Mouse.LastErrorCode
- Msvm_Ps2Mouse.ErrorDescription
- Msvm_Ps2Mouse.ErrorCleared
- Msvm_Ps2Mouse.OtherIdentifyingInfo
- Msvm_Ps2Mouse.PowerOnHours
- Msvm_Ps2Mouse.TotalPowerOnHours
- Msvm_Ps2Mouse.IdentifyingDescriptions
- Msvm_Ps2Mouse.AdditionalAvailability
- Msvm_Ps2Mouse.MaxQuiesceTime
- Msvm_Ps2Mouse.IsLocked
- Msvm_Ps2Mouse.PointingType
- Msvm_Ps2Mouse.NumberOfButtons
- Msvm_Ps2Mouse.Handedness
- Msvm_Ps2Mouse.Resolution
- Msvm_Ps2Mouse.AbsoluteCoordinates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d25d168b85a79c5212afc719ce6ec83ca9780395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319287"
---
# <a name="msvm_ps2mouse-class"></a><span data-ttu-id="c790a-103">Msvm \_ Ps2Mouse 類別</span><span class="sxs-lookup"><span data-stu-id="c790a-103">Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="c790a-104">表示 PS2 滑鼠裝置。</span><span class="sxs-lookup"><span data-stu-id="c790a-104">Represents a PS2 mouse device.</span></span> <span data-ttu-id="c790a-105">此類別的實例是一律存在於虛擬機器中的邏輯裝置，因此不會透過資源集區配置。</span><span class="sxs-lookup"><span data-stu-id="c790a-105">Instances of this class are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="c790a-106">一個實例一律存在於虛擬機器中。</span><span class="sxs-lookup"><span data-stu-id="c790a-106">One instance is always present in a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="c790a-107">第2代虛擬機器無法使用此類別。</span><span class="sxs-lookup"><span data-stu-id="c790a-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="c790a-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c790a-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c790a-109">語法</span><span class="sxs-lookup"><span data-stu-id="c790a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Ps2Mouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Emulated Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_PS2Mouse";
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
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = False;
};
```

## <a name="members"></a><span data-ttu-id="c790a-110">成員</span><span class="sxs-lookup"><span data-stu-id="c790a-110">Members</span></span>

<span data-ttu-id="c790a-111">**Msvm \_ Ps2Mouse** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c790a-111">The **Msvm\_Ps2Mouse** class has these types of members:</span></span>

-   [<span data-ttu-id="c790a-112">方法</span><span class="sxs-lookup"><span data-stu-id="c790a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c790a-113">屬性</span><span class="sxs-lookup"><span data-stu-id="c790a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c790a-114">方法</span><span class="sxs-lookup"><span data-stu-id="c790a-114">Methods</span></span>

<span data-ttu-id="c790a-115">**Msvm \_ Ps2Mouse** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c790a-115">The **Msvm\_Ps2Mouse** class has these methods.</span></span>



| <span data-ttu-id="c790a-116">方法</span><span class="sxs-lookup"><span data-stu-id="c790a-116">Method</span></span>                                                           | <span data-ttu-id="c790a-117">描述</span><span class="sxs-lookup"><span data-stu-id="c790a-117">Description</span></span>                                                                                           |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c790a-118">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="c790a-118">**ClickButton**</span></span>](clickbutton-msvm-ps2mouse.md)                 | <span data-ttu-id="c790a-119">在指定的裝置按鈕上，模擬按鈕點擊、向下序列。</span><span class="sxs-lookup"><span data-stu-id="c790a-119">Simulates a button click, a down-up sequence, on the specified device button.</span></span><br/>              |
| <span data-ttu-id="c790a-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="c790a-120">**EnableDevice**</span></span>                                                 | <span data-ttu-id="c790a-121">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c790a-121">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="c790a-122">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="c790a-122">**GetButtonState**</span></span>](getbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="c790a-123">抓取指定裝置按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-123">Retrieves the current state of the specified device button.</span></span><br/>                                |
| <span data-ttu-id="c790a-124">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="c790a-124">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="c790a-125">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c790a-125">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="c790a-126">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="c790a-126">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="c790a-127">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c790a-127">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="c790a-128">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c790a-128">**RequestStateChange**</span></span>](msvm-ps2mouse-requeststatechange.md)   | <span data-ttu-id="c790a-129">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="c790a-129">Requests a state change.</span></span><br/>                                                                   |
| [<span data-ttu-id="c790a-130">**重設**</span><span class="sxs-lookup"><span data-stu-id="c790a-130">**Reset**</span></span>](msvm-ps2mouse-reset.md)                             | <span data-ttu-id="c790a-131">重設裝置。</span><span class="sxs-lookup"><span data-stu-id="c790a-131">Resets the device.</span></span><br/>                                                                         |
| <span data-ttu-id="c790a-132">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="c790a-132">**RestoreProperties**</span></span>                                            | <span data-ttu-id="c790a-133">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c790a-133">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="c790a-134">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="c790a-134">**SaveProperties**</span></span>                                               | <span data-ttu-id="c790a-135">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c790a-135">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="c790a-136">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="c790a-136">**SetButtonState**</span></span>](setbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="c790a-137">設定指定裝置按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-137">Sets the current state of the specified device button.</span></span><br/>                                     |
| <span data-ttu-id="c790a-138">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c790a-138">**SetPowerState**</span></span>                                                | <span data-ttu-id="c790a-139">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c790a-139">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="c790a-140">**SetRelativePosition**</span><span class="sxs-lookup"><span data-stu-id="c790a-140">**SetRelativePosition**</span></span>](setrelativeposition-msvm-ps2mouse.md) | <span data-ttu-id="c790a-141">以指定的水準和垂直差異來位移滑鼠指標的位置。</span><span class="sxs-lookup"><span data-stu-id="c790a-141">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span><br/> |
| [<span data-ttu-id="c790a-142">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="c790a-142">**SetScrollPosition**</span></span>](setscrollposition-msvm-ps2mouse.md)     | <span data-ttu-id="c790a-143">調整指標裝置之滾輪控制項的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="c790a-143">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="c790a-144">屬性</span><span class="sxs-lookup"><span data-stu-id="c790a-144">Properties</span></span>

<span data-ttu-id="c790a-145">**Msvm \_ Ps2Mouse** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c790a-145">The **Msvm\_Ps2Mouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c790a-146">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="c790a-146">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-147">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c790a-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-149">指出裝置是否在絕對座標上運作。</span><span class="sxs-lookup"><span data-stu-id="c790a-149">Indicates whether the device operates on absolute coordinates.</span></span> <span data-ttu-id="c790a-150">如果未設定，則裝置的座標是相對的。</span><span class="sxs-lookup"><span data-stu-id="c790a-150">If not set, the device's coordinates are relative.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="c790a-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-152">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c790a-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c790a-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-154">裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="c790a-154">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="c790a-155">**Availability** 屬性代表裝置的主要狀態和可用性。</span><span class="sxs-lookup"><span data-stu-id="c790a-155">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="c790a-156">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-156">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="c790a-157">值</span><span class="sxs-lookup"><span data-stu-id="c790a-157">Value</span></span>                                                                        | <span data-ttu-id="c790a-158">意義</span><span class="sxs-lookup"><span data-stu-id="c790a-158">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c790a-159"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-159"><dt>6</dt></span></span> </dl> | <span data-ttu-id="c790a-160">不適用</span><span class="sxs-lookup"><span data-stu-id="c790a-160">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c790a-161">**可用性**</span><span class="sxs-lookup"><span data-stu-id="c790a-161">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-162">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-164">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-164">The primary availability and status of the device.</span></span> <span data-ttu-id="c790a-165">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-165">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="c790a-166">值</span><span class="sxs-lookup"><span data-stu-id="c790a-166">Value</span></span>                                                                        | <span data-ttu-id="c790a-167">意義</span><span class="sxs-lookup"><span data-stu-id="c790a-167">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c790a-168"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-168"><dt>6</dt></span></span> </dl> | <span data-ttu-id="c790a-169">不適用</span><span class="sxs-lookup"><span data-stu-id="c790a-169">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c790a-170">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c790a-170">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-171">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c790a-171">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c790a-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-173">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="c790a-173">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="c790a-174">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c790a-174">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-175">**標題**</span><span class="sxs-lookup"><span data-stu-id="c790a-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-178">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="c790a-178">A short description of the object.</span></span> <span data-ttu-id="c790a-179">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c790a-179">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-180">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c790a-180">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-181">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-183">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="c790a-183">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c790a-184">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c790a-184">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c790a-185">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c790a-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c790a-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c790a-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="c790a-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="c790a-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="c790a-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="c790a-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c790a-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c790a-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c790a-193">)</span><span class="sxs-lookup"><span data-stu-id="c790a-193">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c790a-194">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c790a-194">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c790a-197">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="c790a-197">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c790a-198">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="c790a-198">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c790a-199">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="c790a-199">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="c790a-200">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-201">**說明**</span><span class="sxs-lookup"><span data-stu-id="c790a-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-204">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c790a-204">A description of the object.</span></span> <span data-ttu-id="c790a-205">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c790a-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c790a-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-207">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-209">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c790a-209">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c790a-210">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c790a-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c790a-211">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c790a-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c790a-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="c790a-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="c790a-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="c790a-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="c790a-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="c790a-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="c790a-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c790a-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c790a-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c790a-220">)</span><span class="sxs-lookup"><span data-stu-id="c790a-220">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c790a-221">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c790a-221">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c790a-224">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="c790a-224">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="c790a-225">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="c790a-225">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="c790a-226">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="c790a-226">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="c790a-227">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c790a-227">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-230">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c790a-230">A display name for the object.</span></span> <span data-ttu-id="c790a-231">除了索引鍵屬性、身分識別資料和描述資訊之外，此屬性還可讓每個實例定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c790a-231">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="c790a-232">**CIM \_ ManagedSystemElement** 類別的 [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)屬性也會定義為顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c790a-232">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="c790a-233">但是，它通常是一個重要的子類別。</span><span class="sxs-lookup"><span data-stu-id="c790a-233">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="c790a-234">相同的屬性可以同時傳達身分識別和顯示名稱，而不會有不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="c790a-234">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="c790a-235">如果 [**名稱**](msvm-keyboard.md) 存在，而且不是 (的索引鍵（例如針對 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)) 的實例），則 **名稱** 和 **ElementName** 屬性中都可以同時存在相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="c790a-235">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="c790a-236">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「滑鼠」。</span><span class="sxs-lookup"><span data-stu-id="c790a-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Mouse".</span></span>

</dd> <dt>

<span data-ttu-id="c790a-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c790a-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-238">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-239">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-240">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-240">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="c790a-241">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c790a-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c790a-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-243">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-244">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-245">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c790a-246">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c790a-246">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-247">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c790a-247">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-248">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c790a-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-250">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c790a-250">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="c790a-251">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c790a-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-252">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c790a-252">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-253">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-254">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-255">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c790a-255">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="c790a-256">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c790a-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-257">**Handedness**</span><span class="sxs-lookup"><span data-stu-id="c790a-257">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-258">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-260">適用于右手邊或左邊作業的指標裝置設定。</span><span class="sxs-lookup"><span data-stu-id="c790a-260">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="c790a-261">這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-261">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="c790a-262">值</span><span class="sxs-lookup"><span data-stu-id="c790a-262">Value</span></span>                                                                        | <span data-ttu-id="c790a-263">意義</span><span class="sxs-lookup"><span data-stu-id="c790a-263">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="c790a-264"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-264"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c790a-265">Unknown</span><span class="sxs-lookup"><span data-stu-id="c790a-265">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="c790a-266"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-266"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c790a-267">不適用。</span><span class="sxs-lookup"><span data-stu-id="c790a-267">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="c790a-268"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-268"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c790a-269">右手操作。</span><span class="sxs-lookup"><span data-stu-id="c790a-269">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="c790a-270"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-270"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c790a-271">左手操作。</span><span class="sxs-lookup"><span data-stu-id="c790a-271">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="c790a-272">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c790a-272">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-273">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-275">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="c790a-275">The current health of the element.</span></span> <span data-ttu-id="c790a-276">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) </span><span class="sxs-lookup"><span data-stu-id="c790a-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK)</span></span>

</dd> <dt>

<span data-ttu-id="c790a-277">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c790a-277">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-278">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c790a-278">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c790a-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-280">自由格式字串的陣列，提供 [**OtherIdentifyingInfo**](msvm-keyboard.md) 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c790a-280">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="c790a-281">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c790a-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-283">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c790a-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-285">建立虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c790a-285">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="c790a-286">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c790a-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-287">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c790a-287">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c790a-290">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="c790a-290">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c790a-291">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c790a-291">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c790a-292">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c790a-292">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-293">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="c790a-293">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-294">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c790a-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-296">指出裝置是否已鎖定，防止使用者輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="c790a-296">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="c790a-297">這個屬性繼承自 [**CIM \_ UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-297">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-298">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c790a-298">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-299">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c790a-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-301">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c790a-301">The last error code reported by the logical device.</span></span> <span data-ttu-id="c790a-302">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c790a-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-303">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="c790a-303">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-304">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c790a-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-306">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="c790a-306">This property has been deprecated.</span></span> <span data-ttu-id="c790a-307">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-308">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c790a-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c790a-311">限定詞： **MaxLen** (1024) </span><span class="sxs-lookup"><span data-stu-id="c790a-311">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="c790a-312">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="c790a-312">The label by which the object is known.</span></span> <span data-ttu-id="c790a-313">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="c790a-313">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="c790a-314">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c790a-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-315">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="c790a-315">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-316">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="c790a-316">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-318">指標裝置上的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="c790a-318">The number of buttons on the pointing device.</span></span> <span data-ttu-id="c790a-319">這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-319">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c790a-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-321">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-323">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c790a-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c790a-324">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c790a-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c790a-325">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c790a-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c790a-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c790a-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="c790a-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="c790a-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="c790a-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="c790a-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="c790a-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="c790a-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="c790a-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="c790a-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="c790a-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="c790a-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="c790a-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="c790a-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="c790a-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="c790a-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="c790a-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="c790a-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c790a-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c790a-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c790a-345">)</span><span class="sxs-lookup"><span data-stu-id="c790a-345">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c790a-346">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c790a-346">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-347">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c790a-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c790a-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-349">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-349">The current status of the element.</span></span> <span data-ttu-id="c790a-350">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="c790a-350">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-351">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c790a-351">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-354">當 [**EnabledState**](msvm-keyboard.md) 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-354">The enabled or disabled state of the element when the [**EnabledState**](msvm-keyboard.md) property is set to 1 (Other).</span></span> <span data-ttu-id="c790a-355">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c790a-355">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c790a-356">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c790a-356">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-357">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c790a-357">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-358">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c790a-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c790a-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-360">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="c790a-360">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c790a-361">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-362">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="c790a-362">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-363">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-363">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-365">指標裝置的型別。</span><span class="sxs-lookup"><span data-stu-id="c790a-365">The type of the pointing device.</span></span> <span data-ttu-id="c790a-366">這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-366">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="c790a-367">值</span><span class="sxs-lookup"><span data-stu-id="c790a-367">Value</span></span>                                                                        | <span data-ttu-id="c790a-368">意義</span><span class="sxs-lookup"><span data-stu-id="c790a-368">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="c790a-369"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-369"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c790a-370">滑鼠</span><span class="sxs-lookup"><span data-stu-id="c790a-370">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c790a-371">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c790a-371">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-372">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c790a-372">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c790a-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-374">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="c790a-374">The power management capabilities of the device.</span></span> <span data-ttu-id="c790a-375">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c790a-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-376">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c790a-376">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-377">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c790a-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-379">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="c790a-379">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="c790a-380">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c790a-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-381">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c790a-381">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-382">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c790a-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-384">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="c790a-384">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="c790a-385">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c790a-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-386">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c790a-386">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-387">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-389">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="c790a-389">Provides high level status information.</span></span> <span data-ttu-id="c790a-390">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-390">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c790a-391">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c790a-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c790a-392">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c790a-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c790a-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c790a-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-394"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="c790a-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="c790a-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="c790a-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c790a-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c790a-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c790a-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c790a-399">)</span><span class="sxs-lookup"><span data-stu-id="c790a-399">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c790a-400">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c790a-400">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-401">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-403">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-403">The last requested or desired state for the element.</span></span> <span data-ttu-id="c790a-404">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c790a-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c790a-405">值</span><span class="sxs-lookup"><span data-stu-id="c790a-405">Value</span></span>                                                                         | <span data-ttu-id="c790a-406">意義</span><span class="sxs-lookup"><span data-stu-id="c790a-406">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="c790a-407"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-407"><dt>12</dt></span></span> </dl> | <span data-ttu-id="c790a-408">不適用。</span><span class="sxs-lookup"><span data-stu-id="c790a-408">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c790a-409">**解決方法**</span><span class="sxs-lookup"><span data-stu-id="c790a-409">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-410">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c790a-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-412">指標裝置的追蹤解析度（以每英寸計數計算）。</span><span class="sxs-lookup"><span data-stu-id="c790a-412">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="c790a-413">這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-413">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-414">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c790a-414">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-417">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-417">The current status of the object.</span></span> <span data-ttu-id="c790a-418">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c790a-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c790a-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-420">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c790a-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c790a-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-422">描述各種 [**OperationalStatus**](msvm-bioselement.md) 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="c790a-422">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="c790a-423">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ，且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="c790a-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c790a-424">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c790a-424">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-425">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-425">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-426">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-427">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-427">The current state of the logical device.</span></span> <span data-ttu-id="c790a-428">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c790a-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-429">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c790a-429">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c790a-432">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="c790a-432">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c790a-433">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c790a-433">The scoping system's creation class name.</span></span> <span data-ttu-id="c790a-434">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-435">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c790a-435">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-436">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c790a-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c790a-438">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="c790a-438">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c790a-439">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="c790a-439">The scoping system's name.</span></span> <span data-ttu-id="c790a-440">此值會對應至範圍虛擬機器之 Msvm 的非程式類型類別的 [**名稱**](msvm-computersystem.md)屬性值。 **\_**</span><span class="sxs-lookup"><span data-stu-id="c790a-440">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="c790a-441">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="c790a-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-442">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c790a-442">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-443">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c790a-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-445">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="c790a-445">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c790a-446">如果未變更元素的狀態，且已填入此屬性，則必須將它設定為0間隔值。</span><span class="sxs-lookup"><span data-stu-id="c790a-446">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="c790a-447">如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。</span><span class="sxs-lookup"><span data-stu-id="c790a-447">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="c790a-448">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c790a-448">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c790a-449">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c790a-449">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-450">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c790a-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-452">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="c790a-452">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="c790a-453">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="c790a-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c790a-454">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c790a-454">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c790a-455">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c790a-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c790a-456">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c790a-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c790a-457">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="c790a-457">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c790a-458">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c790a-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c790a-459">備註</span><span class="sxs-lookup"><span data-stu-id="c790a-459">Remarks</span></span>

<span data-ttu-id="c790a-460">存取 **Msvm \_ Ps2Mouse** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="c790a-460">Access to the **Msvm\_Ps2Mouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c790a-461">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="c790a-461">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c790a-462">規格需求</span><span class="sxs-lookup"><span data-stu-id="c790a-462">Requirements</span></span>



| <span data-ttu-id="c790a-463">需求</span><span class="sxs-lookup"><span data-stu-id="c790a-463">Requirement</span></span> | <span data-ttu-id="c790a-464">值</span><span class="sxs-lookup"><span data-stu-id="c790a-464">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c790a-465">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c790a-465">Minimum supported client</span></span><br/> | <span data-ttu-id="c790a-466">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c790a-466">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c790a-467">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c790a-467">Minimum supported server</span></span><br/> | <span data-ttu-id="c790a-468">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c790a-468">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c790a-469">命名空間</span><span class="sxs-lookup"><span data-stu-id="c790a-469">Namespace</span></span><br/>                | <span data-ttu-id="c790a-470">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c790a-470">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c790a-471">MOF</span><span class="sxs-lookup"><span data-stu-id="c790a-471">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c790a-472"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-472"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c790a-473">DLL</span><span class="sxs-lookup"><span data-stu-id="c790a-473">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c790a-474"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c790a-474"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c790a-475">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c790a-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c790a-476">**CIM \_ PointingDevice**</span><span class="sxs-lookup"><span data-stu-id="c790a-476">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="c790a-477">**CIM \_ PointingDevice**</span><span class="sxs-lookup"><span data-stu-id="c790a-477">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="c790a-478">輸入類別</span><span class="sxs-lookup"><span data-stu-id="c790a-478">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

