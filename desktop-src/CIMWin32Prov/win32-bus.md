---
description: Win32 \_ 匯流排 WMI 類別代表執行 Windows 作業系統的電腦所見到的實體匯流排。 Windows bus 的任何實例都是此類別 (或成員) 的子系。
ms.assetid: 76ba15f4-8c7b-4713-b5a2-e444fbab064a
ms.tgt_platform: multiple
title: Win32_Bus 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Bus
- Win32_Bus.Reset
- Win32_Bus.SetPowerState
- Win32_Bus.Availability
- Win32_Bus.BusNum
- Win32_Bus.BusType
- Win32_Bus.Caption
- Win32_Bus.ConfigManagerErrorCode
- Win32_Bus.ConfigManagerUserConfig
- Win32_Bus.CreationClassName
- Win32_Bus.Description
- Win32_Bus.DeviceID
- Win32_Bus.ErrorCleared
- Win32_Bus.ErrorDescription
- Win32_Bus.InstallDate
- Win32_Bus.LastErrorCode
- Win32_Bus.Name
- Win32_Bus.PNPDeviceID
- Win32_Bus.PowerManagementCapabilities
- Win32_Bus.PowerManagementSupported
- Win32_Bus.Status
- Win32_Bus.StatusInfo
- Win32_Bus.SystemCreationClassName
- Win32_Bus.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac31a2187ee7e4974e1ddedbf084efd482748753
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847146"
---
# <a name="win32_bus-class"></a><span data-ttu-id="298aa-104">Win32 \_ 匯流排類別</span><span class="sxs-lookup"><span data-stu-id="298aa-104">Win32\_Bus class</span></span>

<span data-ttu-id="298aa-105">**Win32 \_ 匯流排** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表執行 Windows 作業系統的電腦所見到的實體匯流排。</span><span class="sxs-lookup"><span data-stu-id="298aa-105">The **Win32\_Bus** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical bus as seen by a computer running a Windows operating system.</span></span> <span data-ttu-id="298aa-106">Windows bus 的任何實例都是此類別 (或成員) 的子系。</span><span class="sxs-lookup"><span data-stu-id="298aa-106">Any instance of a Windows bus is a descendant (or member) of this class.</span></span>

<span data-ttu-id="298aa-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="298aa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="298aa-108">語法</span><span class="sxs-lookup"><span data-stu-id="298aa-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Bus : CIM_LogicalDevice
{
  uint16   Availability;
  uint32   BusNum;
  uint32   BusType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="298aa-109">成員</span><span class="sxs-lookup"><span data-stu-id="298aa-109">Members</span></span>

<span data-ttu-id="298aa-110">**Win32 \_ 匯流排** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="298aa-110">The **Win32\_Bus** class has these types of members:</span></span>

-   [<span data-ttu-id="298aa-111">方法</span><span class="sxs-lookup"><span data-stu-id="298aa-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="298aa-112">屬性</span><span class="sxs-lookup"><span data-stu-id="298aa-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="298aa-113">方法</span><span class="sxs-lookup"><span data-stu-id="298aa-113">Methods</span></span>

<span data-ttu-id="298aa-114">**Win32 \_ 匯流排** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="298aa-114">The **Win32\_Bus** class has these methods.</span></span>



| <span data-ttu-id="298aa-115">方法</span><span class="sxs-lookup"><span data-stu-id="298aa-115">Method</span></span>            | <span data-ttu-id="298aa-116">描述</span><span class="sxs-lookup"><span data-stu-id="298aa-116">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="298aa-117">**重設**</span><span class="sxs-lookup"><span data-stu-id="298aa-117">**Reset**</span></span>         | <span data-ttu-id="298aa-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="298aa-118">Not implemented.</span></span> <span data-ttu-id="298aa-119">若要執行此方法，請參閱 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="298aa-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="298aa-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="298aa-120">**SetPowerState**</span></span> | <span data-ttu-id="298aa-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="298aa-121">Not implemented.</span></span> <span data-ttu-id="298aa-122">若要執行此方法，請參閱 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法，以取得檔。</span><span class="sxs-lookup"><span data-stu-id="298aa-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="298aa-123">屬性</span><span class="sxs-lookup"><span data-stu-id="298aa-123">Properties</span></span>

<span data-ttu-id="298aa-124">**Win32 \_ 匯流排** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="298aa-124">The **Win32\_Bus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="298aa-125">**可用性**</span><span class="sxs-lookup"><span data-stu-id="298aa-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="298aa-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="298aa-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-129">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="298aa-129">Availability and status of the device.</span></span>

<span data-ttu-id="298aa-130">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="298aa-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="298aa-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="298aa-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="298aa-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="298aa-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="298aa-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-134">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="298aa-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="298aa-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="298aa-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="298aa-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="298aa-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="298aa-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="298aa-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="298aa-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="298aa-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="298aa-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="298aa-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="298aa-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="298aa-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="298aa-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="298aa-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="298aa-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="298aa-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="298aa-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="298aa-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="298aa-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="298aa-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-145">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="298aa-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="298aa-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="298aa-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-147">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="298aa-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="298aa-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="298aa-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-149">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="298aa-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="298aa-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="298aa-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="298aa-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="298aa-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-152">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="298aa-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="298aa-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="298aa-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-154">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="298aa-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="298aa-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="298aa-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-156">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="298aa-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="298aa-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="298aa-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-158">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="298aa-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="298aa-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="298aa-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-160">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="298aa-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="298aa-161">**BusNum**</span><span class="sxs-lookup"><span data-stu-id="298aa-161">**BusNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="298aa-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-164">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-165">指派給實體匯流排的邏輯編號。</span><span class="sxs-lookup"><span data-stu-id="298aa-165">Logical number assigned to the physical bus.</span></span>

<span data-ttu-id="298aa-166">範例：1</span><span class="sxs-lookup"><span data-stu-id="298aa-166">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="298aa-167">**BusType**</span><span class="sxs-lookup"><span data-stu-id="298aa-167">**BusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-168">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="298aa-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-170">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| cHwRes \| INTERFACE \_ TYPE" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|cHwRes\|INTERFACE\_TYPE")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-171">實體匯流排的型別。</span><span class="sxs-lookup"><span data-stu-id="298aa-171">Type of the physical bus.</span></span> <span data-ttu-id="298aa-172">此值將是在 Bus 中定義之 **介面 \_ 型** 別列舉的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="298aa-172">This value will be one of the values in the **INTERFACE\_TYPE** enumeration defined in Bus.h.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="298aa-173">**未定義** 的 (-1) </span><span class="sxs-lookup"><span data-stu-id="298aa-173">**Undefined** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="298aa-174">**內部** (0) </span><span class="sxs-lookup"><span data-stu-id="298aa-174">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="298aa-175">**ISA** (1) </span><span class="sxs-lookup"><span data-stu-id="298aa-175">**ISA** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="298aa-176">**EISA** (2) </span><span class="sxs-lookup"><span data-stu-id="298aa-176">**EISA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MicroChannel"></span><span id="microchannel"></span><span id="MICROCHANNEL"></span>

<span data-ttu-id="298aa-177">**MicroChannel** (3) </span><span class="sxs-lookup"><span data-stu-id="298aa-177">**MicroChannel** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboChannel"></span><span id="turbochannel"></span><span id="TURBOCHANNEL"></span>

<span data-ttu-id="298aa-178">**TurboChannel** (4) </span><span class="sxs-lookup"><span data-stu-id="298aa-178">**TurboChannel** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Bus"></span><span id="pci_bus"></span><span id="PCI_BUS"></span>

<span data-ttu-id="298aa-179">**PCI 匯流排** (5) </span><span class="sxs-lookup"><span data-stu-id="298aa-179">**PCI Bus** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="298aa-180">**Vm 匯流排** (6) </span><span class="sxs-lookup"><span data-stu-id="298aa-180">**VME Bus** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="298aa-181">**NuBus** (7) </span><span class="sxs-lookup"><span data-stu-id="298aa-181">**NuBus** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Bus"></span><span id="pcmcia_bus"></span><span id="PCMCIA_BUS"></span>

<span data-ttu-id="298aa-182">**PCMCIA 匯流排** (8) </span><span class="sxs-lookup"><span data-stu-id="298aa-182">**PCMCIA Bus** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="C_Bus"></span><span id="c_bus"></span><span id="C_BUS"></span>

<span data-ttu-id="298aa-183">**C 匯流排** (9) </span><span class="sxs-lookup"><span data-stu-id="298aa-183">**C Bus** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MPI_Bus"></span><span id="mpi_bus"></span><span id="MPI_BUS"></span>

<span data-ttu-id="298aa-184">**MPI 匯流排** (10) </span><span class="sxs-lookup"><span data-stu-id="298aa-184">**MPI Bus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MPSA_Bus"></span><span id="mpsa_bus"></span><span id="MPSA_BUS"></span>

<span data-ttu-id="298aa-185">**MPSA Bus** (11) </span><span class="sxs-lookup"><span data-stu-id="298aa-185">**MPSA Bus** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Processor"></span><span id="internal_processor"></span><span id="INTERNAL_PROCESSOR"></span>

<span data-ttu-id="298aa-186">**內部處理器** (12) </span><span class="sxs-lookup"><span data-stu-id="298aa-186">**Internal Processor** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Power_Bus"></span><span id="internal_power_bus"></span><span id="INTERNAL_POWER_BUS"></span>

<span data-ttu-id="298aa-187">**內部電源匯流排** (13) </span><span class="sxs-lookup"><span data-stu-id="298aa-187">**Internal Power Bus** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_ISA_Bus"></span><span id="pnp_isa_bus"></span><span id="PNP_ISA_BUS"></span>

<span data-ttu-id="298aa-188">**PNP ISA Bus** (14) </span><span class="sxs-lookup"><span data-stu-id="298aa-188">**PNP ISA Bus** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_Bus"></span><span id="pnp_bus"></span><span id="PNP_BUS"></span>

<span data-ttu-id="298aa-189">**PNP 匯流排** (15) </span><span class="sxs-lookup"><span data-stu-id="298aa-189">**PNP Bus** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum_Interface_Type"></span><span id="maximum_interface_type"></span><span id="MAXIMUM_INTERFACE_TYPE"></span>

<span data-ttu-id="298aa-190">**最大介面類別型** (16) </span><span class="sxs-lookup"><span data-stu-id="298aa-190">**Maximum Interface Type** (16)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="298aa-191">**標題**</span><span class="sxs-lookup"><span data-stu-id="298aa-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-194">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-195">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="298aa-195">Short description of the object a one-line string.</span></span>

<span data-ttu-id="298aa-196">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-197">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="298aa-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-198">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="298aa-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-200">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-201">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="298aa-201">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="298aa-202">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="298aa-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="298aa-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="298aa-204"> (0)</span><span class="sxs-lookup"><span data-stu-id="298aa-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-205">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="298aa-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="298aa-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="298aa-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="298aa-207">(1)</span><span class="sxs-lookup"><span data-stu-id="298aa-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-208">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="298aa-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="298aa-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="298aa-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="298aa-210">(2)</span><span class="sxs-lookup"><span data-stu-id="298aa-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="298aa-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="298aa-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="298aa-212">(3)</span><span class="sxs-lookup"><span data-stu-id="298aa-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-213">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="298aa-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="298aa-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="298aa-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="298aa-215">(4)</span><span class="sxs-lookup"><span data-stu-id="298aa-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-216">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="298aa-216">Device is not working properly.</span></span> <span data-ttu-id="298aa-217">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="298aa-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="298aa-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="298aa-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="298aa-219">(5)</span><span class="sxs-lookup"><span data-stu-id="298aa-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-220">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="298aa-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="298aa-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="298aa-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="298aa-222">(6)</span><span class="sxs-lookup"><span data-stu-id="298aa-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-223">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="298aa-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="298aa-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="298aa-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="298aa-225">(7)</span><span class="sxs-lookup"><span data-stu-id="298aa-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="298aa-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="298aa-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="298aa-227">(8)</span><span class="sxs-lookup"><span data-stu-id="298aa-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-228">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="298aa-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="298aa-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="298aa-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="298aa-230">(9)</span><span class="sxs-lookup"><span data-stu-id="298aa-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-231">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="298aa-231">Device is not working properly.</span></span> <span data-ttu-id="298aa-232">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="298aa-232">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="298aa-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="298aa-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="298aa-234">(10)</span><span class="sxs-lookup"><span data-stu-id="298aa-234">(10)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-235">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="298aa-235">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="298aa-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="298aa-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="298aa-237">(11)</span><span class="sxs-lookup"><span data-stu-id="298aa-237">(11)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-238">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="298aa-238">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="298aa-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="298aa-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="298aa-240"> (12) </span><span class="sxs-lookup"><span data-stu-id="298aa-240">(12)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-241">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="298aa-241">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="298aa-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="298aa-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="298aa-243">(13)</span><span class="sxs-lookup"><span data-stu-id="298aa-243">(13)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-244">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="298aa-244">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="298aa-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="298aa-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="298aa-246">(14)</span><span class="sxs-lookup"><span data-stu-id="298aa-246">(14)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-247">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="298aa-247">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="298aa-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="298aa-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="298aa-249">(15)</span><span class="sxs-lookup"><span data-stu-id="298aa-249">(15)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-250">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="298aa-250">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="298aa-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="298aa-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="298aa-252">(16)</span><span class="sxs-lookup"><span data-stu-id="298aa-252">(16)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-253">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="298aa-253">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="298aa-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="298aa-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="298aa-255">(17)</span><span class="sxs-lookup"><span data-stu-id="298aa-255">(17)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-256">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="298aa-256">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="298aa-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="298aa-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="298aa-258">(18)</span><span class="sxs-lookup"><span data-stu-id="298aa-258">(18)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-259">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="298aa-259">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="298aa-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="298aa-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="298aa-261">(19)</span><span class="sxs-lookup"><span data-stu-id="298aa-261">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="298aa-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="298aa-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="298aa-263">(20)</span><span class="sxs-lookup"><span data-stu-id="298aa-263">(20)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-264">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="298aa-264">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="298aa-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="298aa-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="298aa-266">(21)</span><span class="sxs-lookup"><span data-stu-id="298aa-266">(21)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-267">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="298aa-267">System failure.</span></span> <span data-ttu-id="298aa-268">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="298aa-268">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="298aa-269">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="298aa-269">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="298aa-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="298aa-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="298aa-271">(22)</span><span class="sxs-lookup"><span data-stu-id="298aa-271">(22)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-272">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="298aa-272">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="298aa-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="298aa-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="298aa-274">(23)</span><span class="sxs-lookup"><span data-stu-id="298aa-274">(23)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-275">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="298aa-275">System failure.</span></span> <span data-ttu-id="298aa-276">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="298aa-276">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="298aa-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="298aa-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="298aa-278">(24)</span><span class="sxs-lookup"><span data-stu-id="298aa-278">(24)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-279">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="298aa-279">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="298aa-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="298aa-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="298aa-281">(25)</span><span class="sxs-lookup"><span data-stu-id="298aa-281">(25)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-282">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="298aa-282">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="298aa-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="298aa-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="298aa-284">(26)</span><span class="sxs-lookup"><span data-stu-id="298aa-284">(26)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-285">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="298aa-285">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="298aa-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="298aa-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="298aa-287">(27)</span><span class="sxs-lookup"><span data-stu-id="298aa-287">(27)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-288">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="298aa-288">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="298aa-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="298aa-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="298aa-290">(28)</span><span class="sxs-lookup"><span data-stu-id="298aa-290">(28)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-291">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="298aa-291">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="298aa-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="298aa-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="298aa-293">(29)</span><span class="sxs-lookup"><span data-stu-id="298aa-293">(29)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-294">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="298aa-294">Device is disabled.</span></span> <span data-ttu-id="298aa-295">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="298aa-295">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="298aa-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="298aa-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="298aa-297">(30)</span><span class="sxs-lookup"><span data-stu-id="298aa-297">(30)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-298">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="298aa-298">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="298aa-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="298aa-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="298aa-300"> (31) </span><span class="sxs-lookup"><span data-stu-id="298aa-300">(31)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-301">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="298aa-301">Device is not working properly.</span></span> <span data-ttu-id="298aa-302">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="298aa-302">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="298aa-303">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="298aa-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-304">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="298aa-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-306">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-307">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="298aa-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="298aa-308">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-309">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="298aa-309">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-310">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-311">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-312">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="298aa-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="298aa-313">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="298aa-313">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="298aa-314">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="298aa-314">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="298aa-315">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-316">**說明**</span><span class="sxs-lookup"><span data-stu-id="298aa-316">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-319">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-319">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-320">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="298aa-320">Description of the object.</span></span>

<span data-ttu-id="298aa-321">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-322">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="298aa-322">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-323">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-325">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-325">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-326">識別匯流排的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="298aa-326">Unique name that identifies the bus.</span></span>

<span data-ttu-id="298aa-327">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-328">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="298aa-328">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-329">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="298aa-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="298aa-331">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="298aa-331">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="298aa-332">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-333">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="298aa-333">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="298aa-336">有關 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="298aa-336">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="298aa-337">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="298aa-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-339">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="298aa-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-341">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="298aa-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-342">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="298aa-342">Date and time the object was installed.</span></span> <span data-ttu-id="298aa-343">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="298aa-343">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="298aa-344">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="298aa-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-346">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="298aa-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="298aa-348">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="298aa-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="298aa-349">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-350">**名稱**</span><span class="sxs-lookup"><span data-stu-id="298aa-350">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-351">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-353">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-353">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-354">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="298aa-354">Label by which the object is known.</span></span> <span data-ttu-id="298aa-355">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="298aa-355">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="298aa-356">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-357">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="298aa-357">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-360">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-360">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-361">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="298aa-361">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="298aa-362">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="298aa-363">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="298aa-363">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="298aa-364">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="298aa-364">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-365">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="298aa-365">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="298aa-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="298aa-367">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="298aa-367">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="298aa-368">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="298aa-368">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="298aa-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="298aa-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="298aa-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="298aa-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="298aa-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="298aa-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="298aa-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="298aa-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-373">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="298aa-373">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="298aa-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="298aa-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-375">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="298aa-375">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="298aa-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="298aa-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-377">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="298aa-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="298aa-378">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="298aa-378">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="298aa-379">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="298aa-379">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="298aa-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="298aa-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-381">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="298aa-381">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="298aa-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="298aa-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="298aa-383">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="298aa-383">Timed Power-On Supported</span></span>

<span data-ttu-id="298aa-384">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="298aa-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="298aa-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="298aa-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-386">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="298aa-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="298aa-388">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="298aa-388">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="298aa-389">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="298aa-389">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="298aa-390">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-391">**狀態**</span><span class="sxs-lookup"><span data-stu-id="298aa-391">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-392">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-394">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-394">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-395">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="298aa-395">Current status of the object.</span></span> <span data-ttu-id="298aa-396">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="298aa-396">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="298aa-397">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="298aa-397">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="298aa-398">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="298aa-398">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="298aa-399">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="298aa-399">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="298aa-400">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="298aa-400">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="298aa-401">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="298aa-402">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="298aa-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="298aa-403">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="298aa-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="298aa-404">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="298aa-405">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="298aa-406">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="298aa-407">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="298aa-408">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="298aa-409">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="298aa-410">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="298aa-411">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="298aa-412">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="298aa-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="298aa-413">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="298aa-414">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="298aa-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="298aa-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="298aa-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-416">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="298aa-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-418">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="298aa-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="298aa-419">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="298aa-419">State of the logical device.</span></span> <span data-ttu-id="298aa-420">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="298aa-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="298aa-421">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="298aa-422">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="298aa-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="298aa-423">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="298aa-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="298aa-424">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="298aa-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="298aa-425">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="298aa-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="298aa-426">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="298aa-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="298aa-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="298aa-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-428">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-430">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="298aa-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="298aa-431">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="298aa-431">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="298aa-432">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="298aa-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="298aa-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298aa-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="298aa-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="298aa-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="298aa-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298aa-436">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="298aa-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="298aa-437">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="298aa-437">Name of the scoping system.</span></span>

<span data-ttu-id="298aa-438">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="298aa-439">備註</span><span class="sxs-lookup"><span data-stu-id="298aa-439">Remarks</span></span>

<span data-ttu-id="298aa-440">**Win32 \_ 匯流排** 類別衍生自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="298aa-440">The **Win32\_Bus** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="298aa-441">規格需求</span><span class="sxs-lookup"><span data-stu-id="298aa-441">Requirements</span></span>



| <span data-ttu-id="298aa-442">需求</span><span class="sxs-lookup"><span data-stu-id="298aa-442">Requirement</span></span> | <span data-ttu-id="298aa-443">值</span><span class="sxs-lookup"><span data-stu-id="298aa-443">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="298aa-444">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="298aa-444">Minimum supported client</span></span><br/> | <span data-ttu-id="298aa-445">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="298aa-445">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="298aa-446">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="298aa-446">Minimum supported server</span></span><br/> | <span data-ttu-id="298aa-447">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="298aa-447">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="298aa-448">命名空間</span><span class="sxs-lookup"><span data-stu-id="298aa-448">Namespace</span></span><br/>                | <span data-ttu-id="298aa-449">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="298aa-449">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="298aa-450">MOF</span><span class="sxs-lookup"><span data-stu-id="298aa-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="298aa-451"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="298aa-451"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="298aa-452">DLL</span><span class="sxs-lookup"><span data-stu-id="298aa-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="298aa-453"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="298aa-453"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="298aa-454">另請參閱</span><span class="sxs-lookup"><span data-stu-id="298aa-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="298aa-455">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="298aa-455">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="298aa-456">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="298aa-456">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

