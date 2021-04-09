---
description: 描述顯示控制器上的主要繪圖介面。
ms.assetid: 280ABAD0-D91B-4683-9F12-32563D7FE6BF
title: Msvm_VideoHead 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHead
- Msvm_VideoHead.SetPowerState
- Msvm_VideoHead.EnableDevice
- Msvm_VideoHead.OnlineDevice
- Msvm_VideoHead.QuiesceDevice
- Msvm_VideoHead.SaveProperties
- Msvm_VideoHead.RestoreProperties
- Msvm_VideoHead.InstanceID
- Msvm_VideoHead.Caption
- Msvm_VideoHead.Description
- Msvm_VideoHead.ElementName
- Msvm_VideoHead.InstallDate
- Msvm_VideoHead.Name
- Msvm_VideoHead.OperationalStatus
- Msvm_VideoHead.StatusDescriptions
- Msvm_VideoHead.Status
- Msvm_VideoHead.HealthState
- Msvm_VideoHead.CommunicationStatus
- Msvm_VideoHead.DetailedStatus
- Msvm_VideoHead.OperatingStatus
- Msvm_VideoHead.PrimaryStatus
- Msvm_VideoHead.EnabledState
- Msvm_VideoHead.OtherEnabledState
- Msvm_VideoHead.RequestedState
- Msvm_VideoHead.EnabledDefault
- Msvm_VideoHead.TimeOfLastStateChange
- Msvm_VideoHead.AvailableRequestedStates
- Msvm_VideoHead.TransitioningToState
- Msvm_VideoHead.SystemCreationClassName
- Msvm_VideoHead.SystemName
- Msvm_VideoHead.CreationClassName
- Msvm_VideoHead.DeviceID
- Msvm_VideoHead.PowerManagementSupported
- Msvm_VideoHead.PowerManagementCapabilities
- Msvm_VideoHead.Availability
- Msvm_VideoHead.StatusInfo
- Msvm_VideoHead.LastErrorCode
- Msvm_VideoHead.ErrorDescription
- Msvm_VideoHead.ErrorCleared
- Msvm_VideoHead.OtherIdentifyingInfo
- Msvm_VideoHead.PowerOnHours
- Msvm_VideoHead.TotalPowerOnHours
- Msvm_VideoHead.IdentifyingDescriptions
- Msvm_VideoHead.AdditionalAvailability
- Msvm_VideoHead.MaxQuiesceTime
- Msvm_VideoHead.CurrentBitsPerPixel
- Msvm_VideoHead.CurrentHorizontalResolution
- Msvm_VideoHead.CurrentVerticalResolution
- Msvm_VideoHead.MaxRefreshRate
- Msvm_VideoHead.MinRefreshRate
- Msvm_VideoHead.CurrentRefreshRate
- Msvm_VideoHead.CurrentScanMode
- Msvm_VideoHead.OtherCurrentScanMode
- Msvm_VideoHead.CurrentNumberOfRows
- Msvm_VideoHead.CurrentNumberOfColumns
- Msvm_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f40e0386fe42177484fc07296a2f4567f1ee47a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114204"
---
# <a name="msvm_videohead-class"></a><span data-ttu-id="84f20-103">Msvm \_ VideoHead 類別</span><span class="sxs-lookup"><span data-stu-id="84f20-103">Msvm\_VideoHead class</span></span>

<span data-ttu-id="84f20-104">描述顯示控制器上的主要繪圖介面。</span><span class="sxs-lookup"><span data-stu-id="84f20-104">Describes the primary drawing surface on a display controller.</span></span>

<span data-ttu-id="84f20-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="84f20-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f20-106">語法</span><span class="sxs-lookup"><span data-stu-id="84f20-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHead : CIM_VideoHead
{
  string   InstanceID;
  string   Caption = "Video Head";
  string   Description = "Microsoft Virtual Video Head";
  string   ElementName = "Video Head";
  datetime InstallDate;
  string   Name = "Video Head";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_VideoHead";
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
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint32   CurrentVerticalResolution;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  string   OtherCurrentScanMode;
  uint32   CurrentNumberOfRows;
  uint32   CurrentNumberOfColumns;
  uint64   CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="84f20-107">成員</span><span class="sxs-lookup"><span data-stu-id="84f20-107">Members</span></span>

<span data-ttu-id="84f20-108">**Msvm \_ VideoHead** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="84f20-108">The **Msvm\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="84f20-109">方法</span><span class="sxs-lookup"><span data-stu-id="84f20-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="84f20-110">屬性</span><span class="sxs-lookup"><span data-stu-id="84f20-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="84f20-111">方法</span><span class="sxs-lookup"><span data-stu-id="84f20-111">Methods</span></span>

<span data-ttu-id="84f20-112">**Msvm \_ VideoHead** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="84f20-112">The **Msvm\_VideoHead** class has these methods.</span></span>



| <span data-ttu-id="84f20-113">方法</span><span class="sxs-lookup"><span data-stu-id="84f20-113">Method</span></span>                                                          | <span data-ttu-id="84f20-114">描述</span><span class="sxs-lookup"><span data-stu-id="84f20-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="84f20-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="84f20-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="84f20-116">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="84f20-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="84f20-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="84f20-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="84f20-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="84f20-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="84f20-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="84f20-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="84f20-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="84f20-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="84f20-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="84f20-121">**RequestStateChange**</span></span>](msvm-videohead-requeststatechange.md) | <span data-ttu-id="84f20-122">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="84f20-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="84f20-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="84f20-123">**Reset**</span></span>](msvm-videohead-reset.md)                           | <span data-ttu-id="84f20-124">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="84f20-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="84f20-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="84f20-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="84f20-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="84f20-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="84f20-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="84f20-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="84f20-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="84f20-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="84f20-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="84f20-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="84f20-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="84f20-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="84f20-131">屬性</span><span class="sxs-lookup"><span data-stu-id="84f20-131">Properties</span></span>

<span data-ttu-id="84f20-132">**Msvm \_ VideoHead** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="84f20-132">The **Msvm\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84f20-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="84f20-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-134">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="84f20-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84f20-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-136">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="84f20-137">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="84f20-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-138">**可用性**</span><span class="sxs-lookup"><span data-stu-id="84f20-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-141">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-141">The primary availability and status of the device.</span></span> <span data-ttu-id="84f20-142">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="84f20-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="84f20-143">值</span><span class="sxs-lookup"><span data-stu-id="84f20-143">Value</span></span>                                                                        | <span data-ttu-id="84f20-144">意義</span><span class="sxs-lookup"><span data-stu-id="84f20-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="84f20-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="84f20-146">不適用</span><span class="sxs-lookup"><span data-stu-id="84f20-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84f20-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="84f20-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-148">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="84f20-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84f20-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-150">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="84f20-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="84f20-151">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="84f20-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-152">**標題**</span><span class="sxs-lookup"><span data-stu-id="84f20-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-155">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="84f20-155">A short description of the object.</span></span> <span data-ttu-id="84f20-156">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="84f20-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-158">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-160">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="84f20-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="84f20-161">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="84f20-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f20-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="84f20-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="84f20-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="84f20-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="84f20-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="84f20-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="84f20-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="84f20-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="84f20-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="84f20-170">)</span><span class="sxs-lookup"><span data-stu-id="84f20-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f20-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="84f20-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-172">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-174">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="84f20-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="84f20-175">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="84f20-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-176">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="84f20-176">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84f20-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f20-179">限定詞： **單位** ( "Bits" ) </span><span class="sxs-lookup"><span data-stu-id="84f20-179">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="84f20-180">用來顯示每個圖元的位數。</span><span class="sxs-lookup"><span data-stu-id="84f20-180">The number of bits used to display each pixel.</span></span> <span data-ttu-id="84f20-181">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-181">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-182">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="84f20-182">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-183">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84f20-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f20-185">限定詞： **單位** ( "圖元" ) </span><span class="sxs-lookup"><span data-stu-id="84f20-185">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="84f20-186">目前的水準圖元數目。</span><span class="sxs-lookup"><span data-stu-id="84f20-186">The current number of horizontal pixels.</span></span> <span data-ttu-id="84f20-187">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-187">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-188">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="84f20-188">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-189">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="84f20-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-191">目前解析度所支援的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="84f20-191">The number of colors supported at the current resolutions.</span></span> <span data-ttu-id="84f20-192">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-192">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-193">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="84f20-193">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-194">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84f20-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-196">如果在字元模式中，則為這個顯示控制器的資料行數目。</span><span class="sxs-lookup"><span data-stu-id="84f20-196">If in character mode, the number of columns for this display controller.</span></span> <span data-ttu-id="84f20-197">否則為 0。</span><span class="sxs-lookup"><span data-stu-id="84f20-197">Otherwise, 0.</span></span> <span data-ttu-id="84f20-198">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-198">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-199">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="84f20-199">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-200">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84f20-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-202">如果在字元模式中，則為此影片控制器的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="84f20-202">If in character mode, the number of rows for this video controller.</span></span> <span data-ttu-id="84f20-203">否則為 0。</span><span class="sxs-lookup"><span data-stu-id="84f20-203">Otherwise, 0.</span></span> <span data-ttu-id="84f20-204">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-204">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-205">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="84f20-205">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-206">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84f20-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f20-208">限定詞： **單位** ( "赫茲" ) </span><span class="sxs-lookup"><span data-stu-id="84f20-208">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="84f20-209">目前的重新整理速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="84f20-209">The current refresh rate, in hertz.</span></span> <span data-ttu-id="84f20-210">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-210">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-211">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="84f20-211">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-212">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-214">目前的掃描模式。</span><span class="sxs-lookup"><span data-stu-id="84f20-214">The current scan mode.</span></span> <span data-ttu-id="84f20-215">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-215">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="84f20-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="84f20-216"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="84f20-217"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="84f20-218"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**非交錯操作** (3) </span><span class="sxs-lookup"><span data-stu-id="84f20-219"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**交錯操作** (4) </span><span class="sxs-lookup"><span data-stu-id="84f20-220"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f20-221">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="84f20-221">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-222">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84f20-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f20-224">限定詞： **單位** ( "圖元" ) </span><span class="sxs-lookup"><span data-stu-id="84f20-224">Qualifiers: **Units** ("Pixels")</span></span>
</dt> </dl>

<span data-ttu-id="84f20-225">目前的垂直圖元數目。</span><span class="sxs-lookup"><span data-stu-id="84f20-225">The current number of vertical pixels.</span></span> <span data-ttu-id="84f20-226">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-226">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-227">**說明**</span><span class="sxs-lookup"><span data-stu-id="84f20-227">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-230">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="84f20-230">A description of the object.</span></span> <span data-ttu-id="84f20-231">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-232">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="84f20-232">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-233">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-234">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-235">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="84f20-235">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="84f20-236">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="84f20-236">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f20-237">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="84f20-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="84f20-238"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="84f20-239"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="84f20-240"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="84f20-241"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="84f20-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="84f20-243"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="84f20-244"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="84f20-245"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="84f20-246">)</span><span class="sxs-lookup"><span data-stu-id="84f20-246">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f20-247">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="84f20-247">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-248">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-250">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，且會設定為 "Microsoft：*GUID* \\ Head \\ *Index*"。</span><span class="sxs-lookup"><span data-stu-id="84f20-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\Head\\*Index*".</span></span>

</dd> <dt>

<span data-ttu-id="84f20-251">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="84f20-251">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-254">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="84f20-254">A display name for the object.</span></span> <span data-ttu-id="84f20-255">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-256">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="84f20-256">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-257">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-259">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-259">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="84f20-260">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="84f20-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="84f20-261">值</span><span class="sxs-lookup"><span data-stu-id="84f20-261">Value</span></span>                                                                        | <span data-ttu-id="84f20-262">意義</span><span class="sxs-lookup"><span data-stu-id="84f20-262">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="84f20-263"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-263"><dt>2</dt></span></span> </dl> | <span data-ttu-id="84f20-264">已啟用</span><span class="sxs-lookup"><span data-stu-id="84f20-264">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="84f20-265"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-265"><dt>3</dt></span></span> </dl> | <span data-ttu-id="84f20-266">Disabled</span><span class="sxs-lookup"><span data-stu-id="84f20-266">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84f20-267">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="84f20-267">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-268">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-269">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-270">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-270">The enabled and disabled states of an element.</span></span> <span data-ttu-id="84f20-271">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="84f20-271">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="84f20-272">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-272">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="84f20-273">值</span><span class="sxs-lookup"><span data-stu-id="84f20-273">Value</span></span>                                                                        | <span data-ttu-id="84f20-274">意義</span><span class="sxs-lookup"><span data-stu-id="84f20-274">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="84f20-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="84f20-276">已啟用</span><span class="sxs-lookup"><span data-stu-id="84f20-276">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="84f20-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="84f20-278">Disabled</span><span class="sxs-lookup"><span data-stu-id="84f20-278">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84f20-279">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="84f20-279">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-280">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="84f20-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-282">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="84f20-282">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="84f20-283">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="84f20-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-284">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="84f20-284">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-285">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-287">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="84f20-287">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="84f20-288">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="84f20-288">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-289">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="84f20-289">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-290">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-292">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="84f20-292">The current health of the element.</span></span> <span data-ttu-id="84f20-293">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="84f20-293">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="84f20-294">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="84f20-294">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="84f20-295">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="84f20-296">值</span><span class="sxs-lookup"><span data-stu-id="84f20-296">Value</span></span>                                                                        | <span data-ttu-id="84f20-297">意義</span><span class="sxs-lookup"><span data-stu-id="84f20-297">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="84f20-298"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-298"><dt>5</dt></span></span> </dl> | <span data-ttu-id="84f20-299">確定</span><span class="sxs-lookup"><span data-stu-id="84f20-299">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84f20-300">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="84f20-300">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-301">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="84f20-301">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84f20-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-303">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="84f20-303">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="84f20-304">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="84f20-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="84f20-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-306">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="84f20-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-308">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="84f20-308">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="84f20-309">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-310">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84f20-310">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-311">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f20-313">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="84f20-313">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="84f20-314">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="84f20-314">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="84f20-315">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-315">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-316">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="84f20-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-317">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84f20-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-319">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84f20-319">The last error code reported by the logical device.</span></span> <span data-ttu-id="84f20-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="84f20-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-321">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="84f20-321">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-322">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="84f20-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-324">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="84f20-324">This property has been deprecated.</span></span> <span data-ttu-id="84f20-325">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="84f20-325">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-326">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="84f20-326">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-327">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84f20-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f20-329">限定詞： **單位** ( "赫茲" ) </span><span class="sxs-lookup"><span data-stu-id="84f20-329">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="84f20-330">顯示控制器的最大重新整理速率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="84f20-330">The maximum refresh rate of the display controller, in hertz.</span></span> <span data-ttu-id="84f20-331">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-331">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-332">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="84f20-332">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-333">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="84f20-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84f20-335">限定詞： **單位** ( "赫茲" ) </span><span class="sxs-lookup"><span data-stu-id="84f20-335">Qualifiers: **Units** ("Hertz")</span></span>
</dt> </dl>

<span data-ttu-id="84f20-336">影片控制器的最小重新整理頻率（以赫茲為單位）。</span><span class="sxs-lookup"><span data-stu-id="84f20-336">The minimum refresh rate of the video controller, in hertz.</span></span> <span data-ttu-id="84f20-337">這個屬性繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-337">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-338">**名稱**</span><span class="sxs-lookup"><span data-stu-id="84f20-338">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-339">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-341">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="84f20-341">The label by which the object is known.</span></span> <span data-ttu-id="84f20-342">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，它與 **ElementName** 屬性相同。</span><span class="sxs-lookup"><span data-stu-id="84f20-342">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-343">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="84f20-343">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-344">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-346">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="84f20-346">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="84f20-347">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="84f20-347">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f20-348">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="84f20-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="84f20-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="84f20-350"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="84f20-351"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="84f20-352"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="84f20-353"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="84f20-354"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="84f20-355"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="84f20-356"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="84f20-357"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="84f20-358"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="84f20-359"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="84f20-360"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="84f20-361"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="84f20-362"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="84f20-363"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="84f20-364"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="84f20-365"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="84f20-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="84f20-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="84f20-368">)</span><span class="sxs-lookup"><span data-stu-id="84f20-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f20-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="84f20-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-370">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="84f20-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84f20-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-372">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-372">The current statuses of the object.</span></span> <span data-ttu-id="84f20-373">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-374">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="84f20-374">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-375">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-377">當實例的 **CurrentScanMode** 屬性為1時 (其他) 的目前掃描模式。</span><span class="sxs-lookup"><span data-stu-id="84f20-377">The current scan mode when the instance's **CurrentScanMode** property is 1 (Other).</span></span> <span data-ttu-id="84f20-378">這個屬性會繼承自 [**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85)) ，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="84f20-378">This property is inherited from [**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-379">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="84f20-379">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-380">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-382">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="84f20-382">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="84f20-383">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="84f20-383">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="84f20-384">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="84f20-384">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-385">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="84f20-385">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-386">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="84f20-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84f20-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-388">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="84f20-388">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="84f20-389">這個屬性會繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="84f20-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-390">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="84f20-390">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-391">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="84f20-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="84f20-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-393">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="84f20-393">The power management capabilities of the device.</span></span> <span data-ttu-id="84f20-394">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="84f20-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="84f20-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-396">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="84f20-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-398">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="84f20-398">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="84f20-399">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="84f20-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-400">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="84f20-400">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-401">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="84f20-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-403">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="84f20-403">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="84f20-404">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="84f20-404">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-405">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="84f20-405">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-406">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-408">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="84f20-408">Provides high level status information.</span></span> <span data-ttu-id="84f20-409">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-409">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="84f20-410">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="84f20-410">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="84f20-411">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="84f20-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="84f20-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-413"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="84f20-413"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="84f20-414"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="84f20-415"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="84f20-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f20-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="84f20-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="84f20-418">)</span><span class="sxs-lookup"><span data-stu-id="84f20-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84f20-419">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="84f20-419">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-420">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-422">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-422">The last requested or desired state for the element.</span></span> <span data-ttu-id="84f20-423">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="84f20-423">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="84f20-424">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-424">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="84f20-425">值</span><span class="sxs-lookup"><span data-stu-id="84f20-425">Value</span></span>                                                                         | <span data-ttu-id="84f20-426">意義</span><span class="sxs-lookup"><span data-stu-id="84f20-426">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="84f20-427"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-427"><dt>12</dt></span></span> </dl> | <span data-ttu-id="84f20-428">不適用</span><span class="sxs-lookup"><span data-stu-id="84f20-428">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="84f20-429">**狀態**</span><span class="sxs-lookup"><span data-stu-id="84f20-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-432">字串，指定物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-432">A string that specifies the current status of the object.</span></span> <span data-ttu-id="84f20-433">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="84f20-433">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-434">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="84f20-434">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-435">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="84f20-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="84f20-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-437">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="84f20-437">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="84f20-438">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="84f20-438">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="84f20-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-440">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-442">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-442">The current state of the logical device.</span></span> <span data-ttu-id="84f20-443">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="84f20-443">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-444">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="84f20-444">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-447">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="84f20-447">The scoping system's creation class name.</span></span> <span data-ttu-id="84f20-448">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="84f20-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="84f20-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-450">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="84f20-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-452">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="84f20-452">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="84f20-453">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="84f20-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="84f20-454">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="84f20-454">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-455">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="84f20-455">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-456">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-457">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="84f20-457">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="84f20-458">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="84f20-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-459">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="84f20-459">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-460">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="84f20-460">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-461">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-462">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="84f20-462">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="84f20-463">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="84f20-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="84f20-464">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="84f20-464">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84f20-465">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="84f20-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84f20-466">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="84f20-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84f20-467">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="84f20-467">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="84f20-468">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="84f20-468">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="84f20-469">值</span><span class="sxs-lookup"><span data-stu-id="84f20-469">Value</span></span>                                                                         | <span data-ttu-id="84f20-470">意義</span><span class="sxs-lookup"><span data-stu-id="84f20-470">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="84f20-471"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-471"><dt>12</dt></span></span> </dl> | <span data-ttu-id="84f20-472">不適用</span><span class="sxs-lookup"><span data-stu-id="84f20-472">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84f20-473">備註</span><span class="sxs-lookup"><span data-stu-id="84f20-473">Remarks</span></span>

<span data-ttu-id="84f20-474">存取 **Msvm \_ VideoHead** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="84f20-474">Access to the **Msvm\_VideoHead** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="84f20-475">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="84f20-475">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="84f20-476">規格需求</span><span class="sxs-lookup"><span data-stu-id="84f20-476">Requirements</span></span>



| <span data-ttu-id="84f20-477">需求</span><span class="sxs-lookup"><span data-stu-id="84f20-477">Requirement</span></span> | <span data-ttu-id="84f20-478">值</span><span class="sxs-lookup"><span data-stu-id="84f20-478">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f20-479">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84f20-479">Minimum supported client</span></span><br/> | <span data-ttu-id="84f20-480">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84f20-480">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="84f20-481">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84f20-481">Minimum supported server</span></span><br/> | <span data-ttu-id="84f20-482">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84f20-482">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84f20-483">命名空間</span><span class="sxs-lookup"><span data-stu-id="84f20-483">Namespace</span></span><br/>                | <span data-ttu-id="84f20-484">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="84f20-484">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84f20-485">MOF</span><span class="sxs-lookup"><span data-stu-id="84f20-485">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84f20-486"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-486"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84f20-487">DLL</span><span class="sxs-lookup"><span data-stu-id="84f20-487">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f20-488"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84f20-488"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84f20-489">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84f20-489">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f20-490">**CIM \_ VideoHead**</span><span class="sxs-lookup"><span data-stu-id="84f20-490">**CIM\_VideoHead**</span></span>](cim-videohead.md)
</dt> <dt>

<span data-ttu-id="84f20-491">[**CIM \_ VideoHead**](/previous-versions//cc136948(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84f20-491">[**CIM\_VideoHead**](/previous-versions//cc136948(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="84f20-492">影片類別</span><span class="sxs-lookup"><span data-stu-id="84f20-492">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

