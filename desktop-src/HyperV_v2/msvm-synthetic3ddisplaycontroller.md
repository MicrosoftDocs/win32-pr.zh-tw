---
description: 代表指派給虛擬機器的綜合立體顯示控制器。
ms.assetid: 5679668B-7D0B-421C-92B6-8A320090DFF7
title: Msvm_Synthetic3DDisplayController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayController
- Msvm_Synthetic3DDisplayController.RequestStateChange
- Msvm_Synthetic3DDisplayController.SetPowerState
- Msvm_Synthetic3DDisplayController.Reset
- Msvm_Synthetic3DDisplayController.EnableDevice
- Msvm_Synthetic3DDisplayController.OnlineDevice
- Msvm_Synthetic3DDisplayController.QuiesceDevice
- Msvm_Synthetic3DDisplayController.SaveProperties
- Msvm_Synthetic3DDisplayController.RestoreProperties
- Msvm_Synthetic3DDisplayController.InstanceID
- Msvm_Synthetic3DDisplayController.Caption
- Msvm_Synthetic3DDisplayController.Description
- Msvm_Synthetic3DDisplayController.ElementName
- Msvm_Synthetic3DDisplayController.InstallDate
- Msvm_Synthetic3DDisplayController.Name
- Msvm_Synthetic3DDisplayController.OperationalStatus
- Msvm_Synthetic3DDisplayController.StatusDescriptions
- Msvm_Synthetic3DDisplayController.Status
- Msvm_Synthetic3DDisplayController.HealthState
- Msvm_Synthetic3DDisplayController.CommunicationStatus
- Msvm_Synthetic3DDisplayController.DetailedStatus
- Msvm_Synthetic3DDisplayController.OperatingStatus
- Msvm_Synthetic3DDisplayController.PrimaryStatus
- Msvm_Synthetic3DDisplayController.EnabledState
- Msvm_Synthetic3DDisplayController.OtherEnabledState
- Msvm_Synthetic3DDisplayController.RequestedState
- Msvm_Synthetic3DDisplayController.EnabledDefault
- Msvm_Synthetic3DDisplayController.TimeOfLastStateChange
- Msvm_Synthetic3DDisplayController.AvailableRequestedStates
- Msvm_Synthetic3DDisplayController.TransitioningToState
- Msvm_Synthetic3DDisplayController.SystemCreationClassName
- Msvm_Synthetic3DDisplayController.SystemName
- Msvm_Synthetic3DDisplayController.CreationClassName
- Msvm_Synthetic3DDisplayController.DeviceID
- Msvm_Synthetic3DDisplayController.PowerManagementSupported
- Msvm_Synthetic3DDisplayController.PowerManagementCapabilities
- Msvm_Synthetic3DDisplayController.Availability
- Msvm_Synthetic3DDisplayController.StatusInfo
- Msvm_Synthetic3DDisplayController.LastErrorCode
- Msvm_Synthetic3DDisplayController.ErrorDescription
- Msvm_Synthetic3DDisplayController.ErrorCleared
- Msvm_Synthetic3DDisplayController.PowerOnHours
- Msvm_Synthetic3DDisplayController.TotalPowerOnHours
- Msvm_Synthetic3DDisplayController.OtherIdentifyingInfo
- Msvm_Synthetic3DDisplayController.IdentifyingDescriptions
- Msvm_Synthetic3DDisplayController.AdditionalAvailability
- Msvm_Synthetic3DDisplayController.MaxQuiesceTime
- Msvm_Synthetic3DDisplayController.TimeOfLastReset
- Msvm_Synthetic3DDisplayController.ProtocolSupported
- Msvm_Synthetic3DDisplayController.MaxNumberControlled
- Msvm_Synthetic3DDisplayController.ProtocolDescription
- Msvm_Synthetic3DDisplayController.VideoProcessor
- Msvm_Synthetic3DDisplayController.VideoMemoryType
- Msvm_Synthetic3DDisplayController.OtherVideoMemoryType
- Msvm_Synthetic3DDisplayController.NumberOfVideoPages
- Msvm_Synthetic3DDisplayController.MaxMemorySupported
- Msvm_Synthetic3DDisplayController.AcceleratorCapabilities
- Msvm_Synthetic3DDisplayController.CapabilityDescriptions
- Msvm_Synthetic3DDisplayController.OtherVideoArchitecture
- Msvm_Synthetic3DDisplayController.VideoArchitecture
- Msvm_Synthetic3DDisplayController.AllocatedGPU
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cd102fe29cf34aa0930ca264c8820868da7daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977833"
---
# <a name="msvm_synthetic3ddisplaycontroller-class"></a><span data-ttu-id="d31d3-103">Msvm \_ Synthetic3DDisplayController 類別</span><span class="sxs-lookup"><span data-stu-id="d31d3-103">Msvm\_Synthetic3DDisplayController class</span></span>

<span data-ttu-id="d31d3-104">代表指派給虛擬機器的綜合立體顯示控制器。</span><span class="sxs-lookup"><span data-stu-id="d31d3-104">Represents the synthetic 3-D display controller that is assigned to a virtual machine.</span></span> <span data-ttu-id="d31d3-105">此類別只會與使用 RemoteFX 的虛擬機器搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d31d3-105">This class is only used with virtual machines that use RemoteFX.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d31d3-106">當您將綜合3d 顯示控制器新增至虛擬機器時，您必須停用任何附加至該虛擬機器的綜合顯示控制器 ([**Msvm \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d31d3-106">When you add a synthetic 3-D display controller to a virtual machine, you must disable any synthetic display controller ([**Msvm\_SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) that is attached to that virtual machine.</span></span>

 

<span data-ttu-id="d31d3-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d31d3-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d31d3-108">語法</span><span class="sxs-lookup"><span data-stu-id="d31d3-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Synthetic3DDisplayController : CIM_DisplayController
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
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 2048;
  uint32   MaxMemorySupported = 8388608;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
  string   AllocatedGPU;
};
```

## <a name="members"></a><span data-ttu-id="d31d3-109">成員</span><span class="sxs-lookup"><span data-stu-id="d31d3-109">Members</span></span>

<span data-ttu-id="d31d3-110">**Msvm \_ Synthetic3DDisplayController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d31d3-110">The **Msvm\_Synthetic3DDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="d31d3-111">方法</span><span class="sxs-lookup"><span data-stu-id="d31d3-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d31d3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d31d3-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d31d3-113">方法</span><span class="sxs-lookup"><span data-stu-id="d31d3-113">Methods</span></span>

<span data-ttu-id="d31d3-114">**Msvm \_ Synthetic3DDisplayController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d31d3-114">The **Msvm\_Synthetic3DDisplayController** class has these methods.</span></span>



| <span data-ttu-id="d31d3-115">方法</span><span class="sxs-lookup"><span data-stu-id="d31d3-115">Method</span></span>                 | <span data-ttu-id="d31d3-116">描述</span><span class="sxs-lookup"><span data-stu-id="d31d3-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="d31d3-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d31d3-117">**EnableDevice**</span></span>       | <span data-ttu-id="d31d3-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d31d3-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d31d3-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d31d3-119">**OnlineDevice**</span></span>       | <span data-ttu-id="d31d3-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d31d3-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d31d3-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d31d3-121">**QuiesceDevice**</span></span>      | <span data-ttu-id="d31d3-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d31d3-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d31d3-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d31d3-123">**RequestStateChange**</span></span> | <span data-ttu-id="d31d3-124">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d31d3-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d31d3-125">**重設**</span><span class="sxs-lookup"><span data-stu-id="d31d3-125">**Reset**</span></span>              | <span data-ttu-id="d31d3-126">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d31d3-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d31d3-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="d31d3-127">**RestoreProperties**</span></span>  | <span data-ttu-id="d31d3-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d31d3-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d31d3-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="d31d3-129">**SaveProperties**</span></span>     | <span data-ttu-id="d31d3-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d31d3-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d31d3-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d31d3-131">**SetPowerState**</span></span>      | <span data-ttu-id="d31d3-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="d31d3-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d31d3-133">屬性</span><span class="sxs-lookup"><span data-stu-id="d31d3-133">Properties</span></span>

<span data-ttu-id="d31d3-134">**Msvm \_ Synthetic3DDisplayController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d31d3-134">The **Msvm\_Synthetic3DDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d31d3-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d31d3-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-136">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d31d3-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-138">顯示控制器的圖形和3D 功能。</span><span class="sxs-lookup"><span data-stu-id="d31d3-138">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="d31d3-139">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d31d3-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-141">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d31d3-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-143">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="d31d3-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-144">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="d31d3-144">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-147">限定詞： [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="d31d3-147">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-148">實體圖形處理單元的識別碼 (GPU) 配置給此虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d31d3-148">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="d31d3-149">這個屬性只適用于使用 RemoteFX 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d31d3-149">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-150">**可用性**</span><span class="sxs-lookup"><span data-stu-id="d31d3-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-153">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 6 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="d31d3-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d31d3-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-155">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d31d3-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-157">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="d31d3-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d31d3-158">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d31d3-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d31d3-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-160">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d31d3-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-162">自由格式字串的陣列，可針對 **AcceleratorCapabilities** 屬性陣列中所指定的任何影片加速器功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="d31d3-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="d31d3-163">這個陣列的每個專案都與位於相同索引的 **AcceleratorCapabilities** 屬性陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="d31d3-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="d31d3-164">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-165">**標題**</span><span class="sxs-lookup"><span data-stu-id="d31d3-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-168">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d31d3-168">A short description of the object.</span></span> <span data-ttu-id="d31d3-169">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d31d3-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-171">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-173">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="d31d3-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d31d3-174">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="d31d3-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d31d3-175">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d31d3-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d31d3-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="d31d3-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="d31d3-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="d31d3-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="d31d3-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d31d3-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="d31d3-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d31d3-183">)</span><span class="sxs-lookup"><span data-stu-id="d31d3-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d31d3-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d31d3-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-185">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-187">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="d31d3-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d31d3-188">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-189">**說明**</span><span class="sxs-lookup"><span data-stu-id="d31d3-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-192">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d31d3-192">A description of the object.</span></span> <span data-ttu-id="d31d3-193">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d31d3-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-195">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-197">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d31d3-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d31d3-198">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="d31d3-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d31d3-199">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d31d3-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="d31d3-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="d31d3-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="d31d3-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="d31d3-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="d31d3-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="d31d3-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d31d3-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="d31d3-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d31d3-208">)</span><span class="sxs-lookup"><span data-stu-id="d31d3-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d31d3-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d31d3-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-212">裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d31d3-212">The device identifier.</span></span> <span data-ttu-id="d31d3-213">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 "Microsoft：*GUID*"。</span><span class="sxs-lookup"><span data-stu-id="d31d3-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d31d3-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-215">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-217">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d31d3-217">A display name for the object.</span></span> <span data-ttu-id="d31d3-218">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d31d3-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-220">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-221">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-222">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="d31d3-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d31d3-223">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="d31d3-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-224">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d31d3-224">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-227">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="d31d3-227">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d31d3-228">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="d31d3-228">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d31d3-229">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 或 3 (停用) 。</span><span class="sxs-lookup"><span data-stu-id="d31d3-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to either 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d31d3-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-231">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d31d3-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-232">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-233">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d31d3-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-237">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d31d3-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-239">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-241">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="d31d3-241">The current health of the element.</span></span> <span data-ttu-id="d31d3-242">這個屬性工作表示這個專案的健康情況，但不一定是它的子項目。</span><span class="sxs-lookup"><span data-stu-id="d31d3-242">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="d31d3-243">可能的值是從0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d31d3-243">The possible values are from 0 through 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d31d3-244">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d31d3-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-246">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d31d3-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-247">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-248">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d31d3-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d31d3-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-250">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d31d3-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-252">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d31d3-252">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d31d3-253">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-253">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-254">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d31d3-254">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-255">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-257">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="d31d3-257">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-258">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d31d3-258">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d31d3-259">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-259">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-260">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d31d3-260">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-261">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d31d3-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-263">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-264">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="d31d3-264">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-265">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d31d3-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-266">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-267">支援的最大記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d31d3-267">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="d31d3-268">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-268">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-269">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="d31d3-269">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-270">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d31d3-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-272">此控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="d31d3-272">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="d31d3-273">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="d31d3-273">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="d31d3-274">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d31d3-274">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="d31d3-275">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-275">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d31d3-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-277">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d31d3-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-279">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-279">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-280">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d31d3-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-281">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-283">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="d31d3-283">The label by which the object is known.</span></span> <span data-ttu-id="d31d3-284">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-285">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="d31d3-285">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-286">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d31d3-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-288">提供目前的解析度和可用記憶體所支援的影片頁面數目。</span><span class="sxs-lookup"><span data-stu-id="d31d3-288">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="d31d3-289">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-289">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-290">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d31d3-290">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-291">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-293">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d31d3-293">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d31d3-294">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="d31d3-294">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d31d3-295">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d31d3-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d31d3-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="d31d3-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="d31d3-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="d31d3-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="d31d3-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="d31d3-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="d31d3-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="d31d3-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="d31d3-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="d31d3-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="d31d3-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="d31d3-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="d31d3-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="d31d3-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="d31d3-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="d31d3-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="d31d3-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d31d3-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="d31d3-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d31d3-315">)</span><span class="sxs-lookup"><span data-stu-id="d31d3-315">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d31d3-316">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d31d3-316">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-317">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d31d3-317">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-319">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d31d3-319">The current statuses of the object.</span></span> <span data-ttu-id="d31d3-320">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-321">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d31d3-321">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-324">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="d31d3-324">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d31d3-325">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d31d3-325">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d31d3-326">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d31d3-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-327">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d31d3-327">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-328">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d31d3-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-330">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d31d3-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-331">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="d31d3-331">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-332">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-334">描述影片架構類型的字串，當 **VideoArchitecture** 屬性是 1 ( "Other" ) 時。</span><span class="sxs-lookup"><span data-stu-id="d31d3-334">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="d31d3-335">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-335">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-336">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="d31d3-336">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-339">當實例的 **VideoMemoryType** 屬性為1時 (其他) 的視訊記憶體類型。</span><span class="sxs-lookup"><span data-stu-id="d31d3-339">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="d31d3-340">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-340">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-341">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d31d3-341">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-342">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d31d3-342">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-344">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d31d3-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-346">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d31d3-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-348">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-349">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d31d3-349">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-350">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d31d3-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-352">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d31d3-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-354">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-356">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d31d3-356">Provides high level status information.</span></span> <span data-ttu-id="d31d3-357">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="d31d3-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d31d3-358">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="d31d3-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d31d3-359">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d31d3-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d31d3-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-361"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="d31d3-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="d31d3-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="d31d3-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d31d3-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="d31d3-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d31d3-366">)</span><span class="sxs-lookup"><span data-stu-id="d31d3-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d31d3-367">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="d31d3-367">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-368">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-370">提供與控制器所支援的通訊協定相關之詳細資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="d31d3-370">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="d31d3-371">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-371">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-372">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="d31d3-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-373">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-375">控制器用來存取受控制裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d31d3-375">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="d31d3-376">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-376">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-377">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d31d3-377">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-378">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-379">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-380">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="d31d3-380">The last requested or desired state for the element.</span></span> <span data-ttu-id="d31d3-381">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="d31d3-381">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d31d3-382">這個屬性是用來比較最後一個要求和目前啟用或停用的狀態。</span><span class="sxs-lookup"><span data-stu-id="d31d3-382">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="d31d3-383">特定的 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) 實例可能不支援 **RequestStateChange**。</span><span class="sxs-lookup"><span data-stu-id="d31d3-383">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="d31d3-384">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="d31d3-384">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="d31d3-385">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 2 (啟用) 、3 (停用) 或 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="d31d3-385">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-386">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d31d3-386">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-387">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-389">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-390">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d31d3-390">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-391">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="d31d3-391">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-393">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="d31d3-393">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d31d3-394">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-394">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-395">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d31d3-395">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-396">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-398">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d31d3-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-400">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-401">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-402">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="d31d3-402">The scoping system's creation class name.</span></span> <span data-ttu-id="d31d3-403">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d31d3-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-405">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-406">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-407">範圍虛擬機器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d31d3-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="d31d3-408">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-409">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="d31d3-409">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-410">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d31d3-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-411">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-412">虛擬機器的上次開機時間。</span><span class="sxs-lookup"><span data-stu-id="d31d3-412">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="d31d3-413">這個屬性繼承自 [**CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)。</span><span class="sxs-lookup"><span data-stu-id="d31d3-413">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-414">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d31d3-414">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-415">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d31d3-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-417">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="d31d3-417">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d31d3-418">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-418">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-419">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d31d3-419">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-420">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="d31d3-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-421">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-422">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="d31d3-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-423">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d31d3-423">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-424">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-426">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="d31d3-426">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d31d3-427">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d31d3-427">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-428">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="d31d3-428">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-429">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-431">指定用來產生視訊訊號的顯示器控制器影片架構。</span><span class="sxs-lookup"><span data-stu-id="d31d3-431">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="d31d3-432">通常，專用的視頻處理器會根據指定的架構產生影片信號。</span><span class="sxs-lookup"><span data-stu-id="d31d3-432">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="d31d3-433">它是顯示控制器最大解析度功能的指標。</span><span class="sxs-lookup"><span data-stu-id="d31d3-433">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="d31d3-434">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-434">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="d31d3-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d31d3-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d31d3-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2) </span><span class="sxs-lookup"><span data-stu-id="d31d3-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3) </span><span class="sxs-lookup"><span data-stu-id="d31d3-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4) </span><span class="sxs-lookup"><span data-stu-id="d31d3-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5) </span><span class="sxs-lookup"><span data-stu-id="d31d3-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6) </span><span class="sxs-lookup"><span data-stu-id="d31d3-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7) </span><span class="sxs-lookup"><span data-stu-id="d31d3-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8) </span><span class="sxs-lookup"><span data-stu-id="d31d3-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9) </span><span class="sxs-lookup"><span data-stu-id="d31d3-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10) </span><span class="sxs-lookup"><span data-stu-id="d31d3-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**線性框架緩衝區** (11) </span><span class="sxs-lookup"><span data-stu-id="d31d3-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160) </span><span class="sxs-lookup"><span data-stu-id="d31d3-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d31d3-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="d31d3-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d31d3-450">)</span><span class="sxs-lookup"><span data-stu-id="d31d3-450">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d31d3-451">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="d31d3-451">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-452">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d31d3-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-454">視訊記憶體的類型。</span><span class="sxs-lookup"><span data-stu-id="d31d3-454">The type of video memory.</span></span> <span data-ttu-id="d31d3-455">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-455">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d31d3-456">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="d31d3-456">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31d3-457">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d31d3-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31d3-458">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d31d3-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d31d3-459">描述視頻處理器/控制器的字串。</span><span class="sxs-lookup"><span data-stu-id="d31d3-459">A string that describes the video processor/controller.</span></span> <span data-ttu-id="d31d3-460">這個屬性繼承自 [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d31d3-460">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d31d3-461">規格需求</span><span class="sxs-lookup"><span data-stu-id="d31d3-461">Requirements</span></span>



| <span data-ttu-id="d31d3-462">需求</span><span class="sxs-lookup"><span data-stu-id="d31d3-462">Requirement</span></span> | <span data-ttu-id="d31d3-463">值</span><span class="sxs-lookup"><span data-stu-id="d31d3-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d31d3-464">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d31d3-464">Minimum supported client</span></span><br/> | <span data-ttu-id="d31d3-465">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d31d3-465">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d31d3-466">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d31d3-466">Minimum supported server</span></span><br/> | <span data-ttu-id="d31d3-467">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d31d3-467">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d31d3-468">命名空間</span><span class="sxs-lookup"><span data-stu-id="d31d3-468">Namespace</span></span><br/>                | <span data-ttu-id="d31d3-469">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d31d3-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d31d3-470">MOF</span><span class="sxs-lookup"><span data-stu-id="d31d3-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d31d3-471"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d31d3-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d31d3-472">DLL</span><span class="sxs-lookup"><span data-stu-id="d31d3-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d31d3-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d31d3-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d31d3-474">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d31d3-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d31d3-475">**CIM \_ DisplayController**</span><span class="sxs-lookup"><span data-stu-id="d31d3-475">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> </dl>

 

