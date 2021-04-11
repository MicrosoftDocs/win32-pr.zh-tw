---
description: 代表綜合滑鼠裝置。
ms.assetid: c04b7aa1-44fe-41f5-943f-ff49ce64be96
title: Msvm_SyntheticMouse 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse
- Msvm_SyntheticMouse.SetPowerState
- Msvm_SyntheticMouse.EnableDevice
- Msvm_SyntheticMouse.OnlineDevice
- Msvm_SyntheticMouse.QuiesceDevice
- Msvm_SyntheticMouse.SaveProperties
- Msvm_SyntheticMouse.RestoreProperties
- Msvm_SyntheticMouse.InstanceID
- Msvm_SyntheticMouse.Caption
- Msvm_SyntheticMouse.Description
- Msvm_SyntheticMouse.ElementName
- Msvm_SyntheticMouse.InstallDate
- Msvm_SyntheticMouse.Name
- Msvm_SyntheticMouse.OperationalStatus
- Msvm_SyntheticMouse.StatusDescriptions
- Msvm_SyntheticMouse.Status
- Msvm_SyntheticMouse.HealthState
- Msvm_SyntheticMouse.CommunicationStatus
- Msvm_SyntheticMouse.DetailedStatus
- Msvm_SyntheticMouse.OperatingStatus
- Msvm_SyntheticMouse.PrimaryStatus
- Msvm_SyntheticMouse.EnabledState
- Msvm_SyntheticMouse.OtherEnabledState
- Msvm_SyntheticMouse.RequestedState
- Msvm_SyntheticMouse.EnabledDefault
- Msvm_SyntheticMouse.TimeOfLastStateChange
- Msvm_SyntheticMouse.AvailableRequestedStates
- Msvm_SyntheticMouse.TransitioningToState
- Msvm_SyntheticMouse.SystemCreationClassName
- Msvm_SyntheticMouse.SystemName
- Msvm_SyntheticMouse.CreationClassName
- Msvm_SyntheticMouse.DeviceID
- Msvm_SyntheticMouse.PowerManagementSupported
- Msvm_SyntheticMouse.PowerManagementCapabilities
- Msvm_SyntheticMouse.Availability
- Msvm_SyntheticMouse.StatusInfo
- Msvm_SyntheticMouse.LastErrorCode
- Msvm_SyntheticMouse.ErrorDescription
- Msvm_SyntheticMouse.ErrorCleared
- Msvm_SyntheticMouse.OtherIdentifyingInfo
- Msvm_SyntheticMouse.PowerOnHours
- Msvm_SyntheticMouse.TotalPowerOnHours
- Msvm_SyntheticMouse.IdentifyingDescriptions
- Msvm_SyntheticMouse.AdditionalAvailability
- Msvm_SyntheticMouse.MaxQuiesceTime
- Msvm_SyntheticMouse.IsLocked
- Msvm_SyntheticMouse.PointingType
- Msvm_SyntheticMouse.NumberOfButtons
- Msvm_SyntheticMouse.Handedness
- Msvm_SyntheticMouse.Resolution
- Msvm_SyntheticMouse.AbsoluteCoordinates
- Msvm_SyntheticMouse.HorizontalPosition
- Msvm_SyntheticMouse.VerticalPosition
- Msvm_SyntheticMouse.ScrollPosition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c5be44637c91ebd57867c5062eba6f9e57ee543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689775"
---
# <a name="msvm_syntheticmouse-class"></a><span data-ttu-id="18248-103">Msvm \_ SyntheticMouse 類別</span><span class="sxs-lookup"><span data-stu-id="18248-103">Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="18248-104">代表綜合滑鼠裝置。</span><span class="sxs-lookup"><span data-stu-id="18248-104">Represents a synthetic mouse device.</span></span>

<span data-ttu-id="18248-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="18248-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18248-106">語法</span><span class="sxs-lookup"><span data-stu-id="18248-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticMouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Synthetic Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {
                "OK"
              };
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
  string   CreationClassName = "Msvm_SyntheticMouse";
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
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = True;
  sint32   HorizontalPosition;
  sint32   VerticalPosition;
  sint32   ScrollPosition;
};
```

## <a name="members"></a><span data-ttu-id="18248-107">成員</span><span class="sxs-lookup"><span data-stu-id="18248-107">Members</span></span>

<span data-ttu-id="18248-108">**Msvm \_ SyntheticMouse** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="18248-108">The **Msvm\_SyntheticMouse** class has these types of members:</span></span>

-   [<span data-ttu-id="18248-109">方法</span><span class="sxs-lookup"><span data-stu-id="18248-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="18248-110">屬性</span><span class="sxs-lookup"><span data-stu-id="18248-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18248-111">方法</span><span class="sxs-lookup"><span data-stu-id="18248-111">Methods</span></span>

<span data-ttu-id="18248-112">**Msvm \_ SyntheticMouse** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="18248-112">The **Msvm\_SyntheticMouse** class has these methods.</span></span>



| <span data-ttu-id="18248-113">方法</span><span class="sxs-lookup"><span data-stu-id="18248-113">Method</span></span>                                                                 | <span data-ttu-id="18248-114">描述</span><span class="sxs-lookup"><span data-stu-id="18248-114">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="18248-115">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="18248-115">**ClickButton**</span></span>](clickbutton-msvm-syntheticmouse.md)                 | <span data-ttu-id="18248-116">模擬指定裝置按鈕的按鈕點擊。</span><span class="sxs-lookup"><span data-stu-id="18248-116">Simulates a button click of the specified device button.</span></span><br/>           |
| <span data-ttu-id="18248-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="18248-117">**EnableDevice**</span></span>                                                       | <span data-ttu-id="18248-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="18248-118">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="18248-119">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="18248-119">**GetButtonState**</span></span>](getbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="18248-120">抓取指定裝置按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-120">Retrieves the current state of the specified device button.</span></span><br/>        |
| <span data-ttu-id="18248-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="18248-121">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="18248-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="18248-122">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="18248-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="18248-123">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="18248-124">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="18248-124">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="18248-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="18248-125">**RequestStateChange**</span></span>](msvm-syntheticmouse-requeststatechange.md)   | <span data-ttu-id="18248-126">要求狀態變更</span><span class="sxs-lookup"><span data-stu-id="18248-126">Requests a state change</span></span><br/>                                            |
| [<span data-ttu-id="18248-127">**重設**</span><span class="sxs-lookup"><span data-stu-id="18248-127">**Reset**</span></span>](msvm-syntheticmouse-reset.md)                             | <span data-ttu-id="18248-128">重設裝置。</span><span class="sxs-lookup"><span data-stu-id="18248-128">Resets the device.</span></span><br/>                                                 |
| <span data-ttu-id="18248-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="18248-129">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="18248-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="18248-130">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="18248-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="18248-131">**SaveProperties**</span></span>                                                     | <span data-ttu-id="18248-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="18248-132">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="18248-133">**SetAbsolutePosition**</span><span class="sxs-lookup"><span data-stu-id="18248-133">**SetAbsolutePosition**</span></span>](setabsoluteposition-msvm-syntheticmouse.md) | <span data-ttu-id="18248-134">設定滑鼠游標的水準和垂直位置。</span><span class="sxs-lookup"><span data-stu-id="18248-134">Sets the horizontal and vertical position of the mouse cursor.</span></span><br/>     |
| [<span data-ttu-id="18248-135">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="18248-135">**SetButtonState**</span></span>](setbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="18248-136">設定指定裝置按鈕的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-136">Sets the current state of the specified device button.</span></span><br/>             |
| <span data-ttu-id="18248-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="18248-137">**SetPowerState**</span></span>                                                      | <span data-ttu-id="18248-138">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="18248-138">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="18248-139">**SetScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="18248-139">**SetScrollPosition**</span></span>](setscrollposition-msvm-syntheticmouse.md)     | <span data-ttu-id="18248-140">設定指向指標裝置之滾輪控制項的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="18248-140">Sets the z-coordinate of the wheel control of the pointing device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="18248-141">屬性</span><span class="sxs-lookup"><span data-stu-id="18248-141">Properties</span></span>

<span data-ttu-id="18248-142">**Msvm \_ SyntheticMouse** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="18248-142">The **Msvm\_SyntheticMouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18248-143">**AbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="18248-143">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-144">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="18248-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18248-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-146">指出裝置是否在絕對或相對座標上運作。</span><span class="sxs-lookup"><span data-stu-id="18248-146">Indicates whether the device operates on absolute or relative coordinates.</span></span>



| <span data-ttu-id="18248-147">值</span><span class="sxs-lookup"><span data-stu-id="18248-147">Value</span></span>                                                                                | <span data-ttu-id="18248-148">意義</span><span class="sxs-lookup"><span data-stu-id="18248-148">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="18248-149"><dt>**對**</dt></span><span class="sxs-lookup"><span data-stu-id="18248-149"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="18248-150">裝置的座標是絕對的。</span><span class="sxs-lookup"><span data-stu-id="18248-150">The device's coordinates are absolute.</span></span><br/> |
| <dl> <span data-ttu-id="18248-151"><dt>**否**</dt></span><span class="sxs-lookup"><span data-stu-id="18248-151"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="18248-152">裝置的座標是相對的。</span><span class="sxs-lookup"><span data-stu-id="18248-152">The device's coordinates are relative.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18248-153">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="18248-153">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-154">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="18248-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18248-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-156">裝置的任何額外可用性和狀態，超出 **可用性** 屬性中指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="18248-156">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="18248-157">**Availability** 屬性代表裝置的主要狀態和可用性。</span><span class="sxs-lookup"><span data-stu-id="18248-157">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="18248-158">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-158">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="18248-159">值</span><span class="sxs-lookup"><span data-stu-id="18248-159">Value</span></span>                                                                          | <span data-ttu-id="18248-160">意義</span><span class="sxs-lookup"><span data-stu-id="18248-160">Meaning</span></span>                   |
|--------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{6}</dt> </dl> | <span data-ttu-id="18248-161">不適用</span><span class="sxs-lookup"><span data-stu-id="18248-161">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18248-162">**可用性**</span><span class="sxs-lookup"><span data-stu-id="18248-162">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-165">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-165">The primary availability and status of the device.</span></span> <span data-ttu-id="18248-166">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-166">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="18248-167">值</span><span class="sxs-lookup"><span data-stu-id="18248-167">Value</span></span>                                                                        | <span data-ttu-id="18248-168">意義</span><span class="sxs-lookup"><span data-stu-id="18248-168">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="18248-169"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="18248-169"><dt>6</dt></span></span> </dl> | <span data-ttu-id="18248-170">不適用</span><span class="sxs-lookup"><span data-stu-id="18248-170">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18248-171">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="18248-171">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-172">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="18248-172">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18248-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-174">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="18248-174">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="18248-175">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18248-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18248-176">**標題**</span><span class="sxs-lookup"><span data-stu-id="18248-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-179">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="18248-179">A short description of the object.</span></span> <span data-ttu-id="18248-180">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18248-181">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="18248-181">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-182">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-184">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="18248-184">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="18248-185">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="18248-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18248-186">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18248-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="18248-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18248-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="18248-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18248-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="18248-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18248-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="18248-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18248-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="18248-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18248-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="18248-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18248-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="18248-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18248-194">)</span><span class="sxs-lookup"><span data-stu-id="18248-194">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18248-195">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18248-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18248-198">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="18248-198">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="18248-199">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="18248-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="18248-200">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="18248-200">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="18248-201">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18248-202">**說明**</span><span class="sxs-lookup"><span data-stu-id="18248-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-205">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="18248-205">A description of the object.</span></span> <span data-ttu-id="18248-206">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18248-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="18248-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-210">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="18248-210">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="18248-211">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="18248-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18248-212">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18248-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="18248-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18248-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="18248-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18248-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="18248-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18248-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="18248-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18248-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="18248-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18248-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="18248-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="18248-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="18248-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18248-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="18248-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18248-221">)</span><span class="sxs-lookup"><span data-stu-id="18248-221">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18248-222">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="18248-222">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18248-225">限定詞： **MaxLen** (64) </span><span class="sxs-lookup"><span data-stu-id="18248-225">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="18248-226">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="18248-226">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="18248-227">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="18248-227">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="18248-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="18248-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-231">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="18248-231">A display name for the object.</span></span> <span data-ttu-id="18248-232">除了索引鍵屬性、身分識別資料和描述資訊之外，此屬性還可讓每個實例定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="18248-232">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="18248-233">**CIM \_ ManagedSystemElement** 類別的 [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)屬性也會定義為顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="18248-233">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="18248-234">但是，它通常是一個重要的子類別。</span><span class="sxs-lookup"><span data-stu-id="18248-234">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="18248-235">相同的屬性可以同時傳達身分識別和顯示名稱，而不會有不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="18248-235">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="18248-236">如果 [**名稱**](msvm-keyboard.md) 存在，而且不是索引鍵 (例如針對 LogicalDevice) 的實例，則 **名稱** 和 **ElementName** 屬性都可以同時存在相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="18248-236">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="18248-237">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18248-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="18248-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-239">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-241">系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 。</span><span class="sxs-lookup"><span data-stu-id="18248-241">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="18248-242">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="18248-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="18248-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="18248-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-244">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-246">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="18248-247">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="18248-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="18248-248">值</span><span class="sxs-lookup"><span data-stu-id="18248-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="18248-249">意義</span><span class="sxs-lookup"><span data-stu-id="18248-249">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="18248-250"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="18248-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="18248-251">來賓虛擬機器支援綜合滑鼠。</span><span class="sxs-lookup"><span data-stu-id="18248-251">The guest virtual machine supports a synthetic mouse.</span></span><br/>         |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="18248-252"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="18248-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="18248-253">來賓虛擬機器不支援綜合滑鼠。</span><span class="sxs-lookup"><span data-stu-id="18248-253">The guest virtual machine does not support a synthetic mouse.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18248-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="18248-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-255">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="18248-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18248-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-257">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="18248-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="18248-258">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="18248-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18248-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="18248-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-262">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="18248-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="18248-263">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="18248-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18248-264">**Handedness**</span><span class="sxs-lookup"><span data-stu-id="18248-264">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-265">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-265">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-267">適用于右手邊或左邊作業的指標裝置設定。</span><span class="sxs-lookup"><span data-stu-id="18248-267">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="18248-268">這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-268">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="18248-269">值</span><span class="sxs-lookup"><span data-stu-id="18248-269">Value</span></span>                                                                        | <span data-ttu-id="18248-270">意義</span><span class="sxs-lookup"><span data-stu-id="18248-270">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="18248-271"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="18248-271"><dt>0</dt></span></span> </dl> | <span data-ttu-id="18248-272">Unknown</span><span class="sxs-lookup"><span data-stu-id="18248-272">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="18248-273"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="18248-273"><dt>1</dt></span></span> </dl> | <span data-ttu-id="18248-274">不適用。</span><span class="sxs-lookup"><span data-stu-id="18248-274">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="18248-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="18248-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="18248-276">右手操作。</span><span class="sxs-lookup"><span data-stu-id="18248-276">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="18248-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="18248-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="18248-278">左手操作。</span><span class="sxs-lookup"><span data-stu-id="18248-278">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="18248-279">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="18248-279">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-280">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-282">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="18248-282">The current health of the element.</span></span> <span data-ttu-id="18248-283">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-283">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18248-284">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="18248-284">**HorizontalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-285">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="18248-285">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18248-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-287">指標裝置的絕對 x 座標。</span><span class="sxs-lookup"><span data-stu-id="18248-287">The absolute x-coordinate of the pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="18248-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="18248-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-289">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="18248-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18248-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-291">自由格式字串的陣列，提供 [**OtherIdentifyingInfo**](msvm-keyboard.md) 陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="18248-291">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="18248-292">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18248-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18248-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-294">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="18248-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18248-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-296">建立虛擬機器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="18248-296">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="18248-297">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18248-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18248-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-299">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18248-301">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="18248-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="18248-302">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="18248-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="18248-303">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18248-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="18248-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-305">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="18248-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18248-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-307">指出裝置是否已鎖定，防止使用者輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="18248-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="18248-308">這個屬性繼承自 [**CIM \_ UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="18248-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18248-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-310">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="18248-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18248-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-312">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="18248-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="18248-313">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="18248-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18248-314">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="18248-314">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-315">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="18248-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18248-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-317">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="18248-317">This property has been deprecated.</span></span> <span data-ttu-id="18248-318">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18248-319">**名稱**</span><span class="sxs-lookup"><span data-stu-id="18248-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18248-322">限定詞： **MaxLen** (1024) </span><span class="sxs-lookup"><span data-stu-id="18248-322">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="18248-323">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="18248-323">The label by which the object is known.</span></span> <span data-ttu-id="18248-324">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="18248-324">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="18248-325">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18248-326">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="18248-326">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-327">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="18248-327">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="18248-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-329">指標裝置上的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="18248-329">The number of buttons on the pointing device.</span></span> <span data-ttu-id="18248-330">這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-330">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="18248-331">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="18248-331">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-332">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-334">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="18248-334">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="18248-335">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="18248-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18248-336">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18248-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="18248-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18248-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="18248-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18248-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="18248-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18248-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="18248-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18248-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="18248-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18248-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="18248-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="18248-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="18248-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="18248-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="18248-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="18248-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="18248-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="18248-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="18248-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="18248-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="18248-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="18248-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="18248-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="18248-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="18248-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="18248-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="18248-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="18248-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="18248-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="18248-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="18248-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="18248-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="18248-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="18248-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="18248-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18248-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="18248-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18248-356">)</span><span class="sxs-lookup"><span data-stu-id="18248-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18248-357">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="18248-357">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-358">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="18248-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18248-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-360">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-360">The current status of the element.</span></span> <span data-ttu-id="18248-361">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18248-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="18248-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-363">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-365">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-365">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="18248-366">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="18248-366">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="18248-367">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="18248-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="18248-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="18248-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-369">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="18248-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18248-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-371">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="18248-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="18248-372">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18248-373">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="18248-373">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-374">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-376">指標裝置的類型。</span><span class="sxs-lookup"><span data-stu-id="18248-376">The type of pointing device.</span></span> <span data-ttu-id="18248-377">這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-377">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="18248-378">值</span><span class="sxs-lookup"><span data-stu-id="18248-378">Value</span></span>                                                                        | <span data-ttu-id="18248-379">意義</span><span class="sxs-lookup"><span data-stu-id="18248-379">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="18248-380"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="18248-380"><dt>3</dt></span></span> </dl> | <span data-ttu-id="18248-381">滑鼠</span><span class="sxs-lookup"><span data-stu-id="18248-381">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18248-382">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="18248-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-383">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="18248-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18248-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-385">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="18248-385">The power management capabilities of the device.</span></span> <span data-ttu-id="18248-386">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="18248-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18248-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="18248-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-388">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="18248-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18248-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-390">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="18248-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="18248-391">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="18248-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18248-392">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="18248-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-393">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="18248-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18248-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-395">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="18248-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="18248-396">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="18248-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18248-397">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="18248-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-398">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-400">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="18248-400">Provides high level status information.</span></span> <span data-ttu-id="18248-401">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="18248-402">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="18248-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18248-403">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18248-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="18248-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18248-405"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="18248-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18248-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="18248-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18248-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="18248-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18248-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="18248-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18248-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="18248-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18248-410">)</span><span class="sxs-lookup"><span data-stu-id="18248-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18248-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="18248-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-412">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-414">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-414">The last requested or desired state for the element.</span></span> <span data-ttu-id="18248-415">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="18248-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="18248-416">值</span><span class="sxs-lookup"><span data-stu-id="18248-416">Value</span></span>                                                                         | <span data-ttu-id="18248-417">意義</span><span class="sxs-lookup"><span data-stu-id="18248-417">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="18248-418"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="18248-418"><dt>12</dt></span></span> </dl> | <span data-ttu-id="18248-419">不適用</span><span class="sxs-lookup"><span data-stu-id="18248-419">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18248-420">**解決方法**</span><span class="sxs-lookup"><span data-stu-id="18248-420">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-421">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="18248-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18248-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-423">指標裝置的追蹤解析度（以每英寸計數計算）。</span><span class="sxs-lookup"><span data-stu-id="18248-423">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="18248-424">這個屬性繼承自 [**CIM \_ PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-424">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="18248-425">**ScrollPosition**</span><span class="sxs-lookup"><span data-stu-id="18248-425">**ScrollPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-426">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="18248-426">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18248-427">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18248-428">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Mickeys" ) </span><span class="sxs-lookup"><span data-stu-id="18248-428">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="18248-429">滑鼠裝置的 z 座標位置。</span><span class="sxs-lookup"><span data-stu-id="18248-429">The z-coordinate position of the mouse device.</span></span>

</dd> <dt>

<span data-ttu-id="18248-430">**狀態**</span><span class="sxs-lookup"><span data-stu-id="18248-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-431">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-432">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-433">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-433">The current status of the object.</span></span> <span data-ttu-id="18248-434">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="18248-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18248-435">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="18248-435">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-436">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="18248-436">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18248-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-438">描述各種 [**OperationalStatus**](msvm-bioselement.md) 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="18248-438">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="18248-439">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="18248-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18248-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="18248-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-441">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-443">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-443">The current state of the logical device.</span></span> <span data-ttu-id="18248-444">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="18248-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18248-445">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18248-445">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-446">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18248-448">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="18248-448">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="18248-449">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="18248-449">The creation class name of the scoping system.</span></span> <span data-ttu-id="18248-450">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18248-451">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="18248-451">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-452">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="18248-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18248-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18248-454">限定詞： **MaxLen** (256) </span><span class="sxs-lookup"><span data-stu-id="18248-454">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="18248-455">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="18248-455">The name of the scoping system.</span></span> <span data-ttu-id="18248-456">此值會對應至範圍虛擬機器之 Msvm 的非程式類型類別的 [**名稱**](msvm-computersystem.md)屬性值。 **\_**</span><span class="sxs-lookup"><span data-stu-id="18248-456">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="18248-457">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="18248-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18248-458">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="18248-458">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-459">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="18248-459">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18248-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-461">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="18248-461">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="18248-462">如果未變更元素的狀態，且已填入此屬性，則必須將它設定為0間隔值。</span><span class="sxs-lookup"><span data-stu-id="18248-462">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="18248-463">如果已要求狀態變更，但遭到拒絕或尚未處理，則必須更新屬性。</span><span class="sxs-lookup"><span data-stu-id="18248-463">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="18248-464">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18248-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18248-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="18248-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-466">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="18248-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18248-467">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-468">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="18248-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="18248-469">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="18248-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18248-470">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="18248-470">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-471">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="18248-471">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18248-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-473">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="18248-473">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="18248-474">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18248-474">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18248-475">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="18248-475">**VerticalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18248-476">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="18248-476">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18248-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="18248-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18248-478">指標裝置的絕對 y 座標。</span><span class="sxs-lookup"><span data-stu-id="18248-478">The absolute y-coordinate of the pointing device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18248-479">備註</span><span class="sxs-lookup"><span data-stu-id="18248-479">Remarks</span></span>

<span data-ttu-id="18248-480">存取 **Msvm \_ SyntheticMouse** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="18248-480">Access to the **Msvm\_SyntheticMouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="18248-481">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="18248-481">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="18248-482">規格需求</span><span class="sxs-lookup"><span data-stu-id="18248-482">Requirements</span></span>



| <span data-ttu-id="18248-483">需求</span><span class="sxs-lookup"><span data-stu-id="18248-483">Requirement</span></span> | <span data-ttu-id="18248-484">值</span><span class="sxs-lookup"><span data-stu-id="18248-484">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18248-485">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18248-485">Minimum supported client</span></span><br/> | <span data-ttu-id="18248-486">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18248-486">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="18248-487">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18248-487">Minimum supported server</span></span><br/> | <span data-ttu-id="18248-488">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18248-488">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18248-489">命名空間</span><span class="sxs-lookup"><span data-stu-id="18248-489">Namespace</span></span><br/>                | <span data-ttu-id="18248-490">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="18248-490">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="18248-491">MOF</span><span class="sxs-lookup"><span data-stu-id="18248-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18248-492"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="18248-492"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18248-493">DLL</span><span class="sxs-lookup"><span data-stu-id="18248-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18248-494"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18248-494"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18248-495">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18248-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18248-496">**CIM \_ PointingDevice**</span><span class="sxs-lookup"><span data-stu-id="18248-496">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="18248-497">**CIM \_ PointingDevice**</span><span class="sxs-lookup"><span data-stu-id="18248-497">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="18248-498">輸入類別</span><span class="sxs-lookup"><span data-stu-id="18248-498">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

