---
description: 硬體實體的抽象或模擬，可能或可能不是以實體硬體為基礎。
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: 'CIM_LogicalDevice 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689504"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="8a6de-103">CIM_LogicalDevice 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="8a6de-103">CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="8a6de-104">硬體實體的抽象或模擬，可能或可能不是以實體硬體為基礎。</span><span class="sxs-lookup"><span data-stu-id="8a6de-104">An abstraction or emulation of a hardware entity that may or may not be based on physical hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6de-105">語法</span><span class="sxs-lookup"><span data-stu-id="8a6de-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="8a6de-106">成員</span><span class="sxs-lookup"><span data-stu-id="8a6de-106">Members</span></span>

<span data-ttu-id="8a6de-107">**CIM \_ LogicalDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8a6de-107">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="8a6de-108">方法</span><span class="sxs-lookup"><span data-stu-id="8a6de-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="8a6de-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8a6de-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8a6de-110">方法</span><span class="sxs-lookup"><span data-stu-id="8a6de-110">Methods</span></span>

<span data-ttu-id="8a6de-111">**CIM \_ LogicalDevice** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8a6de-111">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="8a6de-112">方法</span><span class="sxs-lookup"><span data-stu-id="8a6de-112">Method</span></span>                                                           | <span data-ttu-id="8a6de-113">描述</span><span class="sxs-lookup"><span data-stu-id="8a6de-113">Description</span></span>                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a6de-114">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="8a6de-114">**EnableDevice**</span></span>](cim-logicaldevice-enabledevice.md)           | <span data-ttu-id="8a6de-115">此方法已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-115">This method is deprecated.</span></span> <span data-ttu-id="8a6de-116">請改用 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="8a6de-116">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="8a6de-117">已 **淘汰的描述：** 啟用或停用邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="8a6de-117">**Deprecated description:** Enables or disables the logical device.</span></span><br/>                                                                     |
| [<span data-ttu-id="8a6de-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="8a6de-118">**OnlineDevice**</span></span>](cim-logicaldevice-onlinedevice.md)           | <span data-ttu-id="8a6de-119">此方法已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-119">This method is deprecated.</span></span> <span data-ttu-id="8a6de-120">請改用 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="8a6de-120">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="8a6de-121">已 **淘汰的描述：** 讓邏輯裝置上線，讓它能夠接受要求或離線，使它無法再接受要求。</span><span class="sxs-lookup"><span data-stu-id="8a6de-121">**Deprecated description:** Brings the logical device online so it can accept requests, or offline so it can no longer accept requests.</span></span><br/> |
| [<span data-ttu-id="8a6de-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="8a6de-122">**QuiesceDevice**</span></span>](cim-logicaldevice-quiescedevice.md)         | <span data-ttu-id="8a6de-123">此方法已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-123">This method is deprecated.</span></span> <span data-ttu-id="8a6de-124">請改用 **RequestStateChange** 方法。</span><span class="sxs-lookup"><span data-stu-id="8a6de-124">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="8a6de-125">已 **淘汰的描述：** 暫時暫停邏輯裝置上的活動，或重新啟用活動。</span><span class="sxs-lookup"><span data-stu-id="8a6de-125">**Deprecated description:** Temporarily suspends activity on the logical device, or re-enables the activity.</span></span><br/>                            |
| [<span data-ttu-id="8a6de-126">**重設**</span><span class="sxs-lookup"><span data-stu-id="8a6de-126">**Reset**</span></span>](cim-logicaldevice-reset.md)                         | <span data-ttu-id="8a6de-127">重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="8a6de-127">Resets the logical device.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="8a6de-128">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="8a6de-128">**RestoreProperties**</span></span>](cim-logicaldevice-restoreproperties.md) | <span data-ttu-id="8a6de-129">還原先前的邏輯裝置設定和狀態。</span><span class="sxs-lookup"><span data-stu-id="8a6de-129">Restores a previous configuration and state of the logical device.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="8a6de-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="8a6de-130">**SaveProperties**</span></span>](cim-logicaldevice-saveproperties.md)       | <span data-ttu-id="8a6de-131">儲存邏輯裝置的設定和狀態。</span><span class="sxs-lookup"><span data-stu-id="8a6de-131">Saves the configuration and state of the logical device.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="8a6de-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8a6de-132">**SetPowerState**</span></span>](cim-logicaldevice-setpowerstate.md)         | <span data-ttu-id="8a6de-133">此方法已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-133">This method is deprecated.</span></span> <span data-ttu-id="8a6de-134">相反地，請使用 **CIM \_ PowerManagementService** 類別的 **SetPowerState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8a6de-134">Instead, use the **SetPowerState** property of the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="8a6de-135">已 **淘汰的描述：** 設定邏輯裝置的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="8a6de-135">**Deprecated description:** Sets the power state of the logical device.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="8a6de-136">屬性</span><span class="sxs-lookup"><span data-stu-id="8a6de-136">Properties</span></span>

<span data-ttu-id="8a6de-137">**CIM \_ LogicalDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8a6de-137">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a6de-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="8a6de-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-139">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8a6de-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-141">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ LogicalDevice**.**可用性**") </span><span class="sxs-lookup"><span data-stu-id="8a6de-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**Availability**")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-142">包含邏輯裝置之可用性資訊的陣列，以及 **可用性** 屬性的。</span><span class="sxs-lookup"><span data-stu-id="8a6de-142">An array that contains availability information about of the logical device, in addition to the that of the **Availability** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8a6de-143">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8a6de-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8a6de-144">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8a6de-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8a6de-145">執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="8a6de-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8a6de-146">**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="8a6de-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8a6de-147">**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="8a6de-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8a6de-148">**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="8a6de-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8a6de-149">**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="8a6de-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8a6de-150">**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="8a6de-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8a6de-151">**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="8a6de-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8a6de-152"> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="8a6de-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8a6de-153">**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="8a6de-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8a6de-154">**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="8a6de-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8a6de-155">省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="8a6de-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8a6de-156">省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="8a6de-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8a6de-157">省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="8a6de-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8a6de-158"> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="8a6de-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8a6de-159">省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="8a6de-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8a6de-160">已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="8a6de-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8a6de-161">**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="8a6de-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8a6de-162">**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="8a6de-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8a6de-163">**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="8a6de-163">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a6de-164">**可用性**</span><span class="sxs-lookup"><span data-stu-id="8a6de-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8a6de-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-167">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 006.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus "，" MIF。DMTF \| 主機裝置 \| 001.5 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**。**AdditionalAvailability**") </span><span class="sxs-lookup"><span data-stu-id="8a6de-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus", "MIF.DMTF\|Host Device\|001.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**AdditionalAvailability**")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-168">包含邏輯裝置的可用性。</span><span class="sxs-lookup"><span data-stu-id="8a6de-168">Contains the availability of the logical device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8a6de-169">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8a6de-169">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8a6de-170">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8a6de-170">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8a6de-171">執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="8a6de-171">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8a6de-172">**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="8a6de-172">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8a6de-173">**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="8a6de-173">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8a6de-174">**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="8a6de-174">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8a6de-175">**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="8a6de-175">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8a6de-176">**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="8a6de-176">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8a6de-177">**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="8a6de-177">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8a6de-178"> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="8a6de-178">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8a6de-179">**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="8a6de-179">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8a6de-180">**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="8a6de-180">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8a6de-181">省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="8a6de-181">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8a6de-182">省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="8a6de-182">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8a6de-183">省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="8a6de-183">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8a6de-184"> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="8a6de-184">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8a6de-185">省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="8a6de-185">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8a6de-186">已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="8a6de-186">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8a6de-187">**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="8a6de-187">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8a6de-188">**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="8a6de-188">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8a6de-189">**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="8a6de-189">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a6de-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a6de-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8a6de-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-193">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="8a6de-193">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-194">用來建立邏輯裝置實例的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="8a6de-194">The class name used to create an instance of the logical device.</span></span> <span data-ttu-id="8a6de-195">**CreationClassName** 與這個類別的其他索引鍵屬性結合，可唯一識別此類別和其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8a6de-195">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8a6de-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8a6de-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-199">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="8a6de-199">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-200">邏輯裝置的唯一識別碼，例如位址。</span><span class="sxs-lookup"><span data-stu-id="8a6de-200">A unique identifier of the logical device, such as the address.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-201">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8a6de-201">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-202">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8a6de-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-204">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。**OperationalStatus**") </span><span class="sxs-lookup"><span data-stu-id="8a6de-204">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-205">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-205">This property is deprecated.</span></span> <span data-ttu-id="8a6de-206">請改為使用 **CIM \_ ManagedSystemElement** 類別中的 **OperationalStatus** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8a6de-206">Instead, use the **OperationalStatus** property from the **CIM\_ManagedSystemElement** class.</span></span>

<span data-ttu-id="8a6de-207">已 **淘汰的描述：** 指出是否清除 **LastErrorCode** 屬性所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a6de-207">**Deprecated description:** Indicates whether an error reported by the **LastErrorCode** property is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-208">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8a6de-208">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-209">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8a6de-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-211">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ DeviceErrorData. ErrorDescription" ) </span><span class="sxs-lookup"><span data-stu-id="8a6de-211">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.ErrorDescription")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-212">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-212">This property is deprecated.</span></span> <span data-ttu-id="8a6de-213">相反地，請使用 **CIM \_ DeviceErrorData** 類別的 **ErrorDescription** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8a6de-213">Instead, use the **ErrorDescription** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="8a6de-214">已 **淘汰的描述：\*\*\*\*LastErrorCode** 屬性所報告之錯誤的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8a6de-214">**Deprecated description:** Additional information about the error reported by the **LastErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-215">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8a6de-215">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-216">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8a6de-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-217">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-218">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ LogicalDevice**。**OtherIdentifyingInfo**") </span><span class="sxs-lookup"><span data-stu-id="8a6de-218">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-219">字串陣列，描述相同索引的 **OtherIdentifyingInfo** 陣列專案。</span><span class="sxs-lookup"><span data-stu-id="8a6de-219">An array of strings that describe the **OtherIdentifyingInfo** array items of the same index.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-220">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8a6de-220">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-221">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8a6de-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-222">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-223">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ DeviceErrorData. LastErrorCode" ) </span><span class="sxs-lookup"><span data-stu-id="8a6de-223">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.LastErrorCode")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-224">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-224">This property is deprecated.</span></span> <span data-ttu-id="8a6de-225">相反地，我們會使用 **CIM \_ DeviceErrorData** 類別的 **LastErrorCode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8a6de-225">Instead, we use the **LastErrorCode** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="8a6de-226">已 **淘汰的描述：** 邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8a6de-226">**Deprecated description:** The last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-227">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="8a6de-227">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-228">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8a6de-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-230">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) </span><span class="sxs-lookup"><span data-stu-id="8a6de-230">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-231">此屬性已過時而不應使用。</span><span class="sxs-lookup"><span data-stu-id="8a6de-231">This property is deprecated and should not be used.</span></span>

<span data-ttu-id="8a6de-232">已 **淘汰的描述：** 裝置可以保持暫時停用狀態的最長時間（以毫秒為單位） (**Availability** 和 **AdditionalAvailability** 屬性設定為 "21" 靜止 ) 。</span><span class="sxs-lookup"><span data-stu-id="8a6de-232">**Deprecated description:** The maximum time in milliseconds, that a device can remain in a temporarily disabled state (**Availability** and **AdditionalAvailability** properties set to "21"   quiescent ).</span></span> <span data-ttu-id="8a6de-233">值為 "0" 表示邏輯裝置可無限期保持暫時停用狀態。</span><span class="sxs-lookup"><span data-stu-id="8a6de-233">A value of "0" indicates that the logical device can remain in a temporarily disabled state indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-234">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8a6de-234">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-235">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="8a6de-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-237">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ LogicalDevice**.**IdentifyingDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="8a6de-237">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-238">識別邏輯裝置的資訊，而不是 **DeviceID**。</span><span class="sxs-lookup"><span data-stu-id="8a6de-238">Information that identifies the logical device, other than **DeviceID**.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-239">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8a6de-239">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-240">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8a6de-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-242">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ PowerManagementCapabilities. PowerCapabilities" ) </span><span class="sxs-lookup"><span data-stu-id="8a6de-242">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-243">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-243">This property is deprecated.</span></span> <span data-ttu-id="8a6de-244">相反地，請使用 **CIM \_ PowerManagementCapabilities** 類別。</span><span class="sxs-lookup"><span data-stu-id="8a6de-244">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="8a6de-245">已 **淘汰的描述：** 陣列，其中包含裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="8a6de-245">**Deprecated description:** An array that contains the power management capabilities of the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8a6de-246">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8a6de-246">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8a6de-247">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="8a6de-247">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8a6de-248">**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="8a6de-248">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8a6de-249">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="8a6de-249">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8a6de-250">**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="8a6de-250">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8a6de-251">可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="8a6de-251">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8a6de-252">支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="8a6de-252">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8a6de-253">**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="8a6de-253">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a6de-254">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8a6de-254">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-255">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8a6de-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-256">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-257">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ PowerManagementCapabilities" ) </span><span class="sxs-lookup"><span data-stu-id="8a6de-257">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-258">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-258">This property is deprecated.</span></span> <span data-ttu-id="8a6de-259">請改為使用 **PowerManagementCapabilities** 類別。</span><span class="sxs-lookup"><span data-stu-id="8a6de-259">Instead, use the **PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="8a6de-260">已 **淘汰的描述：** 如果邏輯裝置可以受到電源管理，則為 true;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="8a6de-260">**Deprecated description:  true** if the logical device can be power managed; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-261">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8a6de-261">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-262">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8a6de-262">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-264">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Hours" ) ， **Counter**</span><span class="sxs-lookup"><span data-stu-id="8a6de-264">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-265">邏輯裝置自上一次電源週期起的電源，連續時數。</span><span class="sxs-lookup"><span data-stu-id="8a6de-265">The number of consecutive hours the logical device has been powered, since its last power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-266">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8a6de-266">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-267">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8a6de-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-269">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)。**EnabledState**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 操作狀態 \| 006.4 ") </span><span class="sxs-lookup"><span data-stu-id="8a6de-269">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.4")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-270">此屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="8a6de-270">This property is deprecated.</span></span> <span data-ttu-id="8a6de-271">相反地，請使用 **CIM \_ PowerManagementCapabilities** 類別。</span><span class="sxs-lookup"><span data-stu-id="8a6de-271">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="8a6de-272">已 **淘汰的描述：** 指出邏輯裝置是否已啟用或處於相關狀態。</span><span class="sxs-lookup"><span data-stu-id="8a6de-272">**Deprecated description:** Indicates whether the logical device is enabled or in a related state.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8a6de-273">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8a6de-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8a6de-274">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8a6de-274">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8a6de-275">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="8a6de-275">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8a6de-276">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="8a6de-276">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8a6de-277">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="8a6de-277">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8a6de-278">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a6de-278">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8a6de-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-281">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**CreationClassName**") </span><span class="sxs-lookup"><span data-stu-id="8a6de-281">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-282">用來建立包含邏輯裝置之系統實例的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="8a6de-282">The class name used to create an instance of the system that contains the logical device.</span></span> <span data-ttu-id="8a6de-283">**SystemCreationClassName** 與這個類別的其他索引鍵屬性結合，可唯一識別此類別及其子類別的實例。</span><span class="sxs-lookup"><span data-stu-id="8a6de-283">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-284">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8a6de-284">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-285">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8a6de-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-287">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) ， [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ System**](cim-system.md).**名稱**") </span><span class="sxs-lookup"><span data-stu-id="8a6de-287">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-288">包含邏輯裝置的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="8a6de-288">The name of the system that contains the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="8a6de-289">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8a6de-289">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a6de-290">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8a6de-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8a6de-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a6de-292">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Hours" ) ， **Counter**</span><span class="sxs-lookup"><span data-stu-id="8a6de-292">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="8a6de-293">邏輯裝置已通電的總時數。</span><span class="sxs-lookup"><span data-stu-id="8a6de-293">The total number of hours the logical device has been powered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a6de-294">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a6de-294">Requirements</span></span>



| <span data-ttu-id="8a6de-295">需求</span><span class="sxs-lookup"><span data-stu-id="8a6de-295">Requirement</span></span> | <span data-ttu-id="8a6de-296">值</span><span class="sxs-lookup"><span data-stu-id="8a6de-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6de-297">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a6de-297">Minimum supported client</span></span><br/> | <span data-ttu-id="8a6de-298">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8a6de-298">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8a6de-299">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a6de-299">Minimum supported server</span></span><br/> | <span data-ttu-id="8a6de-300">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a6de-300">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8a6de-301">命名空間</span><span class="sxs-lookup"><span data-stu-id="8a6de-301">Namespace</span></span><br/>                | <span data-ttu-id="8a6de-302">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="8a6de-302">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8a6de-303">MOF</span><span class="sxs-lookup"><span data-stu-id="8a6de-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a6de-304"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8a6de-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a6de-305">DLL</span><span class="sxs-lookup"><span data-stu-id="8a6de-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a6de-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a6de-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a6de-307">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a6de-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a6de-308">**CIM \_ EnabledLogicalElement**</span><span class="sxs-lookup"><span data-stu-id="8a6de-308">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

