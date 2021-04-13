---
description: 代表連接到電腦系統的監視或顯示裝置類型。
ms.assetid: 922be3c1-3c7b-4418-a72f-ab5ada91a7a4
ms.tgt_platform: multiple
title: Win32_DesktopMonitor 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DesktopMonitor
- Win32_DesktopMonitor.Reset
- Win32_DesktopMonitor.SetPowerState
- Win32_DesktopMonitor.Availability
- Win32_DesktopMonitor.Bandwidth
- Win32_DesktopMonitor.Caption
- Win32_DesktopMonitor.ConfigManagerErrorCode
- Win32_DesktopMonitor.ConfigManagerUserConfig
- Win32_DesktopMonitor.CreationClassName
- Win32_DesktopMonitor.Description
- Win32_DesktopMonitor.DeviceID
- Win32_DesktopMonitor.DisplayType
- Win32_DesktopMonitor.ErrorCleared
- Win32_DesktopMonitor.ErrorDescription
- Win32_DesktopMonitor.InstallDate
- Win32_DesktopMonitor.IsLocked
- Win32_DesktopMonitor.LastErrorCode
- Win32_DesktopMonitor.MonitorManufacturer
- Win32_DesktopMonitor.MonitorType
- Win32_DesktopMonitor.Name
- Win32_DesktopMonitor.PixelsPerXLogicalInch
- Win32_DesktopMonitor.PixelsPerYLogicalInch
- Win32_DesktopMonitor.PNPDeviceID
- Win32_DesktopMonitor.PowerManagementCapabilities
- Win32_DesktopMonitor.PowerManagementSupported
- Win32_DesktopMonitor.ScreenHeight
- Win32_DesktopMonitor.ScreenWidth
- Win32_DesktopMonitor.Status
- Win32_DesktopMonitor.StatusInfo
- Win32_DesktopMonitor.SystemCreationClassName
- Win32_DesktopMonitor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccf986957d73dd93837b0ab7a1e10b50aec5e8f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510734"
---
# <a name="win32_desktopmonitor-class"></a><span data-ttu-id="d42eb-103">Win32 \_ DesktopMonitor 類別</span><span class="sxs-lookup"><span data-stu-id="d42eb-103">Win32\_DesktopMonitor class</span></span>

<span data-ttu-id="d42eb-104">**Win32 \_ DesktopMonitor** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表連接到電腦系統的監視或顯示裝置類型。</span><span class="sxs-lookup"><span data-stu-id="d42eb-104">The **Win32\_DesktopMonitor** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the type of monitor or display device attached to the computer system.</span></span>

<span data-ttu-id="d42eb-105">與 Windows 顯示驅動程式模型不相容的硬體 (WDDM) 會傳回這個類別之實例的不正確屬性值。</span><span class="sxs-lookup"><span data-stu-id="d42eb-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="d42eb-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d42eb-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d42eb-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="d42eb-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d42eb-108">語法</span><span class="sxs-lookup"><span data-stu-id="d42eb-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF0-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_DesktopMonitor : CIM_DesktopMonitor
{
  uint16   Availability;
  uint32   Bandwidth;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="d42eb-109">成員</span><span class="sxs-lookup"><span data-stu-id="d42eb-109">Members</span></span>

<span data-ttu-id="d42eb-110">**Win32 \_ DesktopMonitor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d42eb-110">The **Win32\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="d42eb-111">方法</span><span class="sxs-lookup"><span data-stu-id="d42eb-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d42eb-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d42eb-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d42eb-113">方法</span><span class="sxs-lookup"><span data-stu-id="d42eb-113">Methods</span></span>

<span data-ttu-id="d42eb-114">**Win32 \_ DesktopMonitor** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d42eb-114">The **Win32\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="d42eb-115">方法</span><span class="sxs-lookup"><span data-stu-id="d42eb-115">Method</span></span>            | <span data-ttu-id="d42eb-116">描述</span><span class="sxs-lookup"><span data-stu-id="d42eb-116">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d42eb-117">**重設**</span><span class="sxs-lookup"><span data-stu-id="d42eb-117">**Reset**</span></span>         | <span data-ttu-id="d42eb-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="d42eb-118">Not implemented.</span></span> <span data-ttu-id="d42eb-119">若要執行此方法，請參閱 [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="d42eb-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="d42eb-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d42eb-120">**SetPowerState**</span></span> | <span data-ttu-id="d42eb-121">未實作。</span><span class="sxs-lookup"><span data-stu-id="d42eb-121">Not implemented.</span></span> <span data-ttu-id="d42eb-122">若要執行此方法，請參閱 [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法，以取得檔。</span><span class="sxs-lookup"><span data-stu-id="d42eb-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d42eb-123">屬性</span><span class="sxs-lookup"><span data-stu-id="d42eb-123">Properties</span></span>

<span data-ttu-id="d42eb-124">**Win32 \_ DesktopMonitor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d42eb-124">The **Win32\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d42eb-125">**可用性**</span><span class="sxs-lookup"><span data-stu-id="d42eb-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d42eb-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-128">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="d42eb-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-129">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="d42eb-129">Availability and status of the device.</span></span>

<span data-ttu-id="d42eb-130">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d42eb-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d42eb-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d42eb-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="d42eb-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d42eb-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="d42eb-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-134">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="d42eb-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d42eb-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="d42eb-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d42eb-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="d42eb-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d42eb-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="d42eb-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d42eb-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="d42eb-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d42eb-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="d42eb-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d42eb-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="d42eb-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d42eb-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="d42eb-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d42eb-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="d42eb-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d42eb-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="d42eb-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d42eb-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="d42eb-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-145">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="d42eb-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d42eb-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="d42eb-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-147">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="d42eb-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d42eb-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="d42eb-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-149">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="d42eb-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d42eb-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="d42eb-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d42eb-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="d42eb-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-152">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="d42eb-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d42eb-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="d42eb-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-154">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="d42eb-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d42eb-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="d42eb-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-156">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="d42eb-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d42eb-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="d42eb-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-158">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="d42eb-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d42eb-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="d42eb-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-160">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="d42eb-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d42eb-161">**頻寬**</span><span class="sxs-lookup"><span data-stu-id="d42eb-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d42eb-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-164">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "mhz" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-165">監視器的頻寬（以 mhz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="d42eb-165">Monitor's bandwidth in megahertz.</span></span> <span data-ttu-id="d42eb-166">如果不明，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="d42eb-166">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="d42eb-167">這個屬性繼承自 [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-167">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-168">**標題**</span><span class="sxs-lookup"><span data-stu-id="d42eb-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-171">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-172">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="d42eb-172">Short description of the object.</span></span>

<span data-ttu-id="d42eb-173">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d42eb-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-175">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d42eb-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-177">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-178">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d42eb-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d42eb-179">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d42eb-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d42eb-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="d42eb-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-182">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="d42eb-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d42eb-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d42eb-184">(1)</span><span class="sxs-lookup"><span data-stu-id="d42eb-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-185">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="d42eb-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d42eb-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d42eb-187">(2)</span><span class="sxs-lookup"><span data-stu-id="d42eb-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d42eb-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d42eb-189">(3)</span><span class="sxs-lookup"><span data-stu-id="d42eb-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-190">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="d42eb-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d42eb-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d42eb-192">(4)</span><span class="sxs-lookup"><span data-stu-id="d42eb-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-193">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d42eb-193">Device is not working properly.</span></span> <span data-ttu-id="d42eb-194">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="d42eb-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d42eb-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d42eb-196">(5)</span><span class="sxs-lookup"><span data-stu-id="d42eb-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-197">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="d42eb-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d42eb-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d42eb-199">(6)</span><span class="sxs-lookup"><span data-stu-id="d42eb-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-200">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="d42eb-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d42eb-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d42eb-202">(7)</span><span class="sxs-lookup"><span data-stu-id="d42eb-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d42eb-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d42eb-204">(8)</span><span class="sxs-lookup"><span data-stu-id="d42eb-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-205">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="d42eb-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d42eb-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d42eb-207">(9)</span><span class="sxs-lookup"><span data-stu-id="d42eb-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-208">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d42eb-208">Device is not working properly.</span></span> <span data-ttu-id="d42eb-209">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="d42eb-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d42eb-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d42eb-211">(10)</span><span class="sxs-lookup"><span data-stu-id="d42eb-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-212">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="d42eb-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d42eb-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d42eb-214">(11)</span><span class="sxs-lookup"><span data-stu-id="d42eb-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-215">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="d42eb-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d42eb-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d42eb-217"> (12) </span><span class="sxs-lookup"><span data-stu-id="d42eb-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-218">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="d42eb-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d42eb-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d42eb-220">(13)</span><span class="sxs-lookup"><span data-stu-id="d42eb-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-221">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="d42eb-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d42eb-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d42eb-223">(14)</span><span class="sxs-lookup"><span data-stu-id="d42eb-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-224">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d42eb-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d42eb-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d42eb-226">(15)</span><span class="sxs-lookup"><span data-stu-id="d42eb-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-227">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d42eb-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d42eb-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d42eb-229">(16)</span><span class="sxs-lookup"><span data-stu-id="d42eb-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-230">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="d42eb-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d42eb-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d42eb-232">(17)</span><span class="sxs-lookup"><span data-stu-id="d42eb-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-233">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="d42eb-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d42eb-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d42eb-235">(18)</span><span class="sxs-lookup"><span data-stu-id="d42eb-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-236">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d42eb-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d42eb-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d42eb-238">(19)</span><span class="sxs-lookup"><span data-stu-id="d42eb-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d42eb-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d42eb-240">(20)</span><span class="sxs-lookup"><span data-stu-id="d42eb-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-241">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="d42eb-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d42eb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d42eb-243">(21)</span><span class="sxs-lookup"><span data-stu-id="d42eb-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-244">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="d42eb-244">System failure.</span></span> <span data-ttu-id="d42eb-245">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="d42eb-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d42eb-246">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="d42eb-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d42eb-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d42eb-248">(22)</span><span class="sxs-lookup"><span data-stu-id="d42eb-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-249">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="d42eb-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d42eb-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d42eb-251">(23)</span><span class="sxs-lookup"><span data-stu-id="d42eb-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-252">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="d42eb-252">System failure.</span></span> <span data-ttu-id="d42eb-253">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="d42eb-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d42eb-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d42eb-255">(24)</span><span class="sxs-lookup"><span data-stu-id="d42eb-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-256">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="d42eb-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d42eb-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d42eb-258">(25)</span><span class="sxs-lookup"><span data-stu-id="d42eb-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-259">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="d42eb-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d42eb-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d42eb-261">(26)</span><span class="sxs-lookup"><span data-stu-id="d42eb-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-262">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="d42eb-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d42eb-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d42eb-264">(27)</span><span class="sxs-lookup"><span data-stu-id="d42eb-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-265">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="d42eb-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d42eb-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d42eb-267">(28)</span><span class="sxs-lookup"><span data-stu-id="d42eb-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-268">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d42eb-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d42eb-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d42eb-270">(29)</span><span class="sxs-lookup"><span data-stu-id="d42eb-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-271">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="d42eb-271">Device is disabled.</span></span> <span data-ttu-id="d42eb-272">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="d42eb-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d42eb-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d42eb-274">(30)</span><span class="sxs-lookup"><span data-stu-id="d42eb-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-275">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="d42eb-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d42eb-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="d42eb-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d42eb-277"> (31) </span><span class="sxs-lookup"><span data-stu-id="d42eb-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-278">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="d42eb-278">Device is not working properly.</span></span> <span data-ttu-id="d42eb-279">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="d42eb-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d42eb-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d42eb-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-281">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d42eb-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-283">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-283">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-284">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="d42eb-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d42eb-285">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d42eb-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-287">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-289">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d42eb-289">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-290">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="d42eb-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d42eb-291">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="d42eb-291">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d42eb-292">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-293">**說明**</span><span class="sxs-lookup"><span data-stu-id="d42eb-293">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-294">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-296">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-297">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d42eb-297">Description of the object.</span></span>

<span data-ttu-id="d42eb-298">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-298">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-299">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d42eb-299">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-302">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32API \| Windows GDI \| HMONITOR" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows GDI\|HMONITOR")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-303">桌面監視器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d42eb-303">Unique identifier of a desktop monitor.</span></span>

<span data-ttu-id="d42eb-304">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-305">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="d42eb-305">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-306">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d42eb-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-308">桌面監視器或 CRT 的類型。</span><span class="sxs-lookup"><span data-stu-id="d42eb-308">Type of desktop monitor or CRT.</span></span>

<span data-ttu-id="d42eb-309">這個屬性繼承自 [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-309">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d42eb-310">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d42eb-310">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d42eb-311">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d42eb-311">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="d42eb-312">**Multiscan 色彩** (2) </span><span class="sxs-lookup"><span data-stu-id="d42eb-312">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="d42eb-313">**Multiscan 單色** (3) </span><span class="sxs-lookup"><span data-stu-id="d42eb-313">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="d42eb-314">**固定頻率色彩** (4) </span><span class="sxs-lookup"><span data-stu-id="d42eb-314">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="d42eb-315">**固定頻率單色** (5) </span><span class="sxs-lookup"><span data-stu-id="d42eb-315">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d42eb-316">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d42eb-316">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-317">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d42eb-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-319">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="d42eb-319">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d42eb-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-321">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d42eb-321">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-324">自由格式的字串提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d42eb-324">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="d42eb-325">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-326">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d42eb-326">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-327">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d42eb-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-329">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="d42eb-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-330">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="d42eb-330">Date and time the object was installed.</span></span> <span data-ttu-id="d42eb-331">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="d42eb-331">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d42eb-332">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-333">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="d42eb-333">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-334">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d42eb-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-336">若 **為 TRUE**，則會鎖定裝置，防止使用者輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="d42eb-336">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="d42eb-337">這個屬性繼承自 [**CIM \_ UserDevice**](cim-userdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-337">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-338">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d42eb-338">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-339">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d42eb-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-341">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d42eb-341">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d42eb-342">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-343">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="d42eb-343">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-344">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-346">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-347">監視器製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="d42eb-347">Name of the monitor manufacturer.</span></span>

<span data-ttu-id="d42eb-348">範例： "NEC"</span><span class="sxs-lookup"><span data-stu-id="d42eb-348">Example: "NEC"</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-349">**監視類型**</span><span class="sxs-lookup"><span data-stu-id="d42eb-349">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-350">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-352">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-352">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-353">監視器的類型。</span><span class="sxs-lookup"><span data-stu-id="d42eb-353">Type of monitor.</span></span>

<span data-ttu-id="d42eb-354">範例： "NEC 5FGp"</span><span class="sxs-lookup"><span data-stu-id="d42eb-354">Example: "NEC 5FGp"</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-355">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d42eb-355">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-356">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-358">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-359">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="d42eb-359">Label by which the object is known.</span></span> <span data-ttu-id="d42eb-360">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="d42eb-360">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d42eb-361">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-361">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-362">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="d42eb-362">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-363">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d42eb-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-365">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置內容函式 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)」 ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每個邏輯英寸的圖元數」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-365">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-366">沿著 X 軸的解析度 (水準方向) 監視器。</span><span class="sxs-lookup"><span data-stu-id="d42eb-366">Resolution along the x-axis (horizontal direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-367">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="d42eb-367">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-368">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d42eb-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-370">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「Win32API \| 裝置內容函式 \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)」 ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每個邏輯英寸的圖元數」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-371">沿著 y 軸的解析度 (垂直方向) 監視器。</span><span class="sxs-lookup"><span data-stu-id="d42eb-371">Resolution along the y-axis (vertical direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-372">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d42eb-372">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-373">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-375">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-375">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-376">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="d42eb-376">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d42eb-377">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d42eb-378">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d42eb-378">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-379">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d42eb-379">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-380">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="d42eb-380">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-382">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="d42eb-382">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d42eb-383">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-383">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d42eb-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="d42eb-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d42eb-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="d42eb-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-386">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="d42eb-386">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d42eb-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="d42eb-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d42eb-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="d42eb-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-389">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="d42eb-389">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d42eb-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="d42eb-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-391">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="d42eb-391">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d42eb-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="d42eb-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-393">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d42eb-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d42eb-394">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="d42eb-394">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d42eb-395">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-395">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d42eb-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="d42eb-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-397">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="d42eb-397">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d42eb-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="d42eb-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d42eb-399">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="d42eb-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d42eb-400">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d42eb-400">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-401">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="d42eb-401">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-403">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="d42eb-403">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="d42eb-404">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="d42eb-404">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d42eb-405">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-406">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="d42eb-406">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-407">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d42eb-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-409">螢幕座標中顯示的邏輯高度。</span><span class="sxs-lookup"><span data-stu-id="d42eb-409">Logical height of the display in screen coordinates.</span></span>

<span data-ttu-id="d42eb-410">這個屬性繼承自 [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-410">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-411">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="d42eb-411">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-412">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d42eb-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-414">螢幕座標中顯示的邏輯寬度。</span><span class="sxs-lookup"><span data-stu-id="d42eb-414">Logical width of the display in screen coordinates.</span></span>

<span data-ttu-id="d42eb-415">這個屬性繼承自 [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-415">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-416">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d42eb-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-417">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-419">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-420">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d42eb-420">Current status of the object.</span></span> <span data-ttu-id="d42eb-421">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="d42eb-421">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d42eb-422">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="d42eb-422">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d42eb-423">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="d42eb-423">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d42eb-424">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="d42eb-424">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d42eb-425">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="d42eb-425">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d42eb-426">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d42eb-427">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="d42eb-427">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d42eb-428">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-428">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d42eb-429">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-429">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d42eb-430">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-430">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d42eb-431">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-431">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d42eb-432">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-432">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d42eb-433">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-433">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d42eb-434">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-434">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d42eb-435">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-435">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d42eb-436">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-436">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d42eb-437">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-437">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d42eb-438">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-438">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d42eb-439">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="d42eb-439">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d42eb-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d42eb-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-441">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="d42eb-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-442">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-443">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="d42eb-443">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-444">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="d42eb-444">State of the logical device.</span></span> <span data-ttu-id="d42eb-445">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="d42eb-445">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d42eb-446">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d42eb-447">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="d42eb-447">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d42eb-448">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="d42eb-448">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d42eb-449">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="d42eb-449">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d42eb-450">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="d42eb-450">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d42eb-451">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="d42eb-451">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d42eb-452">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d42eb-452">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-453">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-454">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-455">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d42eb-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-456">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d42eb-456">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d42eb-457">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d42eb-458">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d42eb-458">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d42eb-459">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d42eb-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-460">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d42eb-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d42eb-461">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d42eb-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d42eb-462">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="d42eb-462">Name of the scoping system.</span></span>

<span data-ttu-id="d42eb-463">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d42eb-464">備註</span><span class="sxs-lookup"><span data-stu-id="d42eb-464">Remarks</span></span>

<span data-ttu-id="d42eb-465">**Win32 \_ DesktopMonitor** 類別衍生自 [**cim \_ DesktopMonitor**](cim-desktopmonitor.md)，它衍生自 [**cim \_ 顯示**](cim-display.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-465">The **Win32\_DesktopMonitor** class is derived from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), which derives from [**CIM\_Display**](cim-display.md).</span></span> <span data-ttu-id="d42eb-466">**CIM \_顯示** 衍生自 cim [**\_ UserDevice**](cim-userdevice.md)，它衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d42eb-466">**CIM\_Display** is derived from [**CIM\_UserDevice**](cim-userdevice.md), which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d42eb-467">範例</span><span class="sxs-lookup"><span data-stu-id="d42eb-467">Examples</span></span>

<span data-ttu-id="d42eb-468">PS 在 TechNet 資源庫上 [使用 visio PowerShell 範例建立電腦設定繪圖](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) 使用 **Win32 \_ DesktopMonitor** 與 visio automation 模型互動，以建立 visio 繪圖。</span><span class="sxs-lookup"><span data-stu-id="d42eb-468">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_DesktopMonitor** to interact with the Visio automation model to create a Visio drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d42eb-469">規格需求</span><span class="sxs-lookup"><span data-stu-id="d42eb-469">Requirements</span></span>



| <span data-ttu-id="d42eb-470">需求</span><span class="sxs-lookup"><span data-stu-id="d42eb-470">Requirement</span></span> | <span data-ttu-id="d42eb-471">值</span><span class="sxs-lookup"><span data-stu-id="d42eb-471">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d42eb-472">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d42eb-472">Minimum supported client</span></span><br/> | <span data-ttu-id="d42eb-473">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d42eb-473">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d42eb-474">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d42eb-474">Minimum supported server</span></span><br/> | <span data-ttu-id="d42eb-475">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d42eb-475">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d42eb-476">命名空間</span><span class="sxs-lookup"><span data-stu-id="d42eb-476">Namespace</span></span><br/>                | <span data-ttu-id="d42eb-477">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d42eb-477">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d42eb-478">MOF</span><span class="sxs-lookup"><span data-stu-id="d42eb-478">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d42eb-479"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d42eb-479"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d42eb-480">DLL</span><span class="sxs-lookup"><span data-stu-id="d42eb-480">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d42eb-481"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d42eb-481"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d42eb-482">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d42eb-482">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d42eb-483">**CIM \_ DesktopMonitor**</span><span class="sxs-lookup"><span data-stu-id="d42eb-483">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dt>

[<span data-ttu-id="d42eb-484">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="d42eb-484">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d42eb-485">WMI 工作：桌面管理</span><span class="sxs-lookup"><span data-stu-id="d42eb-485">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

