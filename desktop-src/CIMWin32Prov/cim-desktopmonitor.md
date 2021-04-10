---
description: CIM \_ DesktopMonitor 類別代表桌面監視器 (CRT) 邏輯裝置的功能和管理。
ms.assetid: dc65aa38-5255-4a40-8ffc-f05f9af71dc6
ms.tgt_platform: multiple
title: 'CIM_DesktopMonitor 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.Caption
- CIM_DesktopMonitor.Description
- CIM_DesktopMonitor.InstallDate
- CIM_DesktopMonitor.Name
- CIM_DesktopMonitor.Status
- CIM_DesktopMonitor.Availability
- CIM_DesktopMonitor.ConfigManagerErrorCode
- CIM_DesktopMonitor.ConfigManagerUserConfig
- CIM_DesktopMonitor.CreationClassName
- CIM_DesktopMonitor.DeviceID
- CIM_DesktopMonitor.PowerManagementCapabilities
- CIM_DesktopMonitor.ErrorCleared
- CIM_DesktopMonitor.ErrorDescription
- CIM_DesktopMonitor.LastErrorCode
- CIM_DesktopMonitor.PNPDeviceID
- CIM_DesktopMonitor.PowerManagementSupported
- CIM_DesktopMonitor.StatusInfo
- CIM_DesktopMonitor.SystemCreationClassName
- CIM_DesktopMonitor.SystemName
- CIM_DesktopMonitor.IsLocked
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b22d0b681491bbddf0ee357b394da5f1a77aa0e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187764"
---
# <a name="cim_desktopmonitor-class-cimwin32-wmi-providers"></a><span data-ttu-id="0739c-103">CIM_DesktopMonitor 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="0739c-103">CIM_DesktopMonitor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0739c-104">**CIM \_ DesktopMonitor** 類別代表桌面監視器 (CRT) 邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="0739c-104">The **CIM\_DesktopMonitor** class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0739c-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0739c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0739c-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0739c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0739c-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0739c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0739c-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="0739c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0739c-109">語法</span><span class="sxs-lookup"><span data-stu-id="0739c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE8-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_DesktopMonitor : CIM_Display
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  IsLocked;
  uint32   Bandwidth;
  uint16   DisplayType;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="0739c-110">成員</span><span class="sxs-lookup"><span data-stu-id="0739c-110">Members</span></span>

<span data-ttu-id="0739c-111">**CIM \_ DesktopMonitor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0739c-111">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="0739c-112">方法</span><span class="sxs-lookup"><span data-stu-id="0739c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0739c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0739c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0739c-114">方法</span><span class="sxs-lookup"><span data-stu-id="0739c-114">Methods</span></span>

<span data-ttu-id="0739c-115">**CIM \_ DesktopMonitor** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0739c-115">The **CIM\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="0739c-116">方法</span><span class="sxs-lookup"><span data-stu-id="0739c-116">Method</span></span>                                                                    | <span data-ttu-id="0739c-117">描述</span><span class="sxs-lookup"><span data-stu-id="0739c-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0739c-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="0739c-118">**Reset**</span></span>](reset-method-in-class-cim-desktopmonitor.md)                 | <span data-ttu-id="0739c-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="0739c-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="0739c-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="0739c-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0739c-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0739c-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-desktopmonitor.md) | <span data-ttu-id="0739c-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="0739c-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0739c-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="0739c-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0739c-124">屬性</span><span class="sxs-lookup"><span data-stu-id="0739c-124">Properties</span></span>

<span data-ttu-id="0739c-125">**CIM \_ DesktopMonitor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0739c-125">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0739c-126">**可用性**</span><span class="sxs-lookup"><span data-stu-id="0739c-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0739c-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="0739c-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-130">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="0739c-130">Availability and status of the device.</span></span>

<span data-ttu-id="0739c-131">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0739c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0739c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0739c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="0739c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0739c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="0739c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0739c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="0739c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0739c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="0739c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0739c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="0739c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0739c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="0739c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0739c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="0739c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0739c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="0739c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0739c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="0739c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0739c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="0739c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0739c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="0739c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0739c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="0739c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-145">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="0739c-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0739c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="0739c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-147">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="0739c-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0739c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="0739c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-149">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="0739c-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0739c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="0739c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0739c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="0739c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-152">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="0739c-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0739c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="0739c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-154">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="0739c-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0739c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="0739c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-156">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="0739c-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0739c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="0739c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-158">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="0739c-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0739c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="0739c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-160">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="0739c-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0739c-161">**頻寬**</span><span class="sxs-lookup"><span data-stu-id="0739c-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0739c-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-164">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "mhz" ) </span><span class="sxs-lookup"><span data-stu-id="0739c-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-165">監視器的頻寬（以 MHz 為單位）。</span><span class="sxs-lookup"><span data-stu-id="0739c-165">Monitor's bandwidth in MHz.</span></span> <span data-ttu-id="0739c-166">如果不明，請使用 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="0739c-166">If unknown, use 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-167">**標題**</span><span class="sxs-lookup"><span data-stu-id="0739c-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-170">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="0739c-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-171">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="0739c-171">A short textual description of the object.</span></span>

<span data-ttu-id="0739c-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-173">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0739c-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-174">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0739c-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-176">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0739c-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-177">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0739c-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0739c-178">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0739c-179">**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="0739c-179">**This device is working properly.**</span></span> <span data-ttu-id="0739c-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="0739c-180">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0739c-181">**這個裝置並未正確設定。**</span><span class="sxs-lookup"><span data-stu-id="0739c-181">**This device is not configured correctly.**</span></span> <span data-ttu-id="0739c-182">(1)</span><span class="sxs-lookup"><span data-stu-id="0739c-182">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0739c-183">**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0739c-183">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0739c-184">(2)</span><span class="sxs-lookup"><span data-stu-id="0739c-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0739c-185">**這個裝置的驅動程式可能已損毀，或您系統的記憶體或其他資源可能不足。**</span><span class="sxs-lookup"><span data-stu-id="0739c-185">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0739c-186">(3)</span><span class="sxs-lookup"><span data-stu-id="0739c-186">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0739c-187">**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="0739c-187">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0739c-188">(4)</span><span class="sxs-lookup"><span data-stu-id="0739c-188">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0739c-189">**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="0739c-189">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0739c-190">(5)</span><span class="sxs-lookup"><span data-stu-id="0739c-190">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0739c-191">**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="0739c-191">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0739c-192">(6)</span><span class="sxs-lookup"><span data-stu-id="0739c-192">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0739c-193">**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="0739c-193">**Cannot filter.**</span></span> <span data-ttu-id="0739c-194">(7)</span><span class="sxs-lookup"><span data-stu-id="0739c-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0739c-195">**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="0739c-195">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0739c-196">(8)</span><span class="sxs-lookup"><span data-stu-id="0739c-196">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0739c-197">**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="0739c-197">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0739c-198">(9)</span><span class="sxs-lookup"><span data-stu-id="0739c-198">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0739c-199">**這個裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="0739c-199">**This device cannot start.**</span></span> <span data-ttu-id="0739c-200">(10)</span><span class="sxs-lookup"><span data-stu-id="0739c-200">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0739c-201">**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="0739c-201">**This device failed.**</span></span> <span data-ttu-id="0739c-202">(11)</span><span class="sxs-lookup"><span data-stu-id="0739c-202">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0739c-203">**這個裝置沒有足夠資源可供使用。**</span><span class="sxs-lookup"><span data-stu-id="0739c-203">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0739c-204"> (12) </span><span class="sxs-lookup"><span data-stu-id="0739c-204">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0739c-205">**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="0739c-205">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0739c-206">(13)</span><span class="sxs-lookup"><span data-stu-id="0739c-206">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0739c-207">**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="0739c-207">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0739c-208">(14)</span><span class="sxs-lookup"><span data-stu-id="0739c-208">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0739c-209">**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="0739c-209">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0739c-210">(15)</span><span class="sxs-lookup"><span data-stu-id="0739c-210">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0739c-211">**Windows 無法識別這個裝置所使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="0739c-211">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0739c-212">(16)</span><span class="sxs-lookup"><span data-stu-id="0739c-212">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0739c-213">**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="0739c-213">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0739c-214">(17)</span><span class="sxs-lookup"><span data-stu-id="0739c-214">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0739c-215">**重新安裝這個裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0739c-215">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0739c-216">(18)</span><span class="sxs-lookup"><span data-stu-id="0739c-216">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0739c-217">**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="0739c-217">**Failure using the VxD loader.**</span></span> <span data-ttu-id="0739c-218">(19)</span><span class="sxs-lookup"><span data-stu-id="0739c-218">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0739c-219">**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="0739c-219">**Your registry might be corrupted.**</span></span> <span data-ttu-id="0739c-220">(20)</span><span class="sxs-lookup"><span data-stu-id="0739c-220">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0739c-221">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0739c-221">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0739c-222">(21)</span><span class="sxs-lookup"><span data-stu-id="0739c-222">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0739c-223">**這個裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="0739c-223">**This device is disabled.**</span></span> <span data-ttu-id="0739c-224">(22)</span><span class="sxs-lookup"><span data-stu-id="0739c-224">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0739c-225">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="0739c-225">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0739c-226">(23)</span><span class="sxs-lookup"><span data-stu-id="0739c-226">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0739c-227">**這個裝置可能不存在、運作不正確、或並未安裝所有的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0739c-227">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0739c-228">(24)</span><span class="sxs-lookup"><span data-stu-id="0739c-228">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0739c-229">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0739c-229">**Windows is still setting up this device.**</span></span> <span data-ttu-id="0739c-230">(25)</span><span class="sxs-lookup"><span data-stu-id="0739c-230">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0739c-231">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="0739c-231">**Windows is still setting up this device.**</span></span> <span data-ttu-id="0739c-232">(26)</span><span class="sxs-lookup"><span data-stu-id="0739c-232">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0739c-233">**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="0739c-233">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0739c-234">(27)</span><span class="sxs-lookup"><span data-stu-id="0739c-234">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0739c-235">**這個裝置的驅動程式尚未安裝。**</span><span class="sxs-lookup"><span data-stu-id="0739c-235">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0739c-236">(28)</span><span class="sxs-lookup"><span data-stu-id="0739c-236">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0739c-237">**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="0739c-237">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0739c-238">(29)</span><span class="sxs-lookup"><span data-stu-id="0739c-238">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0739c-239">**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="0739c-239">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0739c-240">(30)</span><span class="sxs-lookup"><span data-stu-id="0739c-240">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0739c-241">**這個裝置並未正確執行，因為 Windows 無法載入這個裝置必需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="0739c-241">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0739c-242"> (31) </span><span class="sxs-lookup"><span data-stu-id="0739c-242">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0739c-243">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="0739c-243">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-244">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0739c-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-245">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-246">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0739c-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-247">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="0739c-247">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0739c-248">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-248">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-249">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0739c-249">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-250">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-251">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-252">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0739c-252">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0739c-253">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="0739c-253">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0739c-254">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="0739c-254">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0739c-255">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-255">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-256">**說明**</span><span class="sxs-lookup"><span data-stu-id="0739c-256">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-259">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="0739c-259">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-260">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="0739c-260">A textual description of the object.</span></span>

<span data-ttu-id="0739c-261">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-261">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-262">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0739c-262">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-263">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-264">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-265">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0739c-265">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0739c-266">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="0739c-266">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0739c-267">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-267">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-268">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="0739c-268">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-269">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0739c-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0739c-271">桌面監視器或 CRT 的類型。</span><span class="sxs-lookup"><span data-stu-id="0739c-271">Type of desktop monitor or CRT.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0739c-272">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0739c-272">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0739c-273">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0739c-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="0739c-274">**Multiscan 色彩** (2) </span><span class="sxs-lookup"><span data-stu-id="0739c-274">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="0739c-275">**Multiscan 單色** (3) </span><span class="sxs-lookup"><span data-stu-id="0739c-275">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="0739c-276">**固定頻率色彩** (4) </span><span class="sxs-lookup"><span data-stu-id="0739c-276">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="0739c-277">**固定頻率單色** (5) </span><span class="sxs-lookup"><span data-stu-id="0739c-277">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0739c-278">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0739c-278">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-279">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0739c-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0739c-281">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="0739c-281">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0739c-282">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-283">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0739c-283">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-284">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0739c-286">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="0739c-286">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0739c-287">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-288">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0739c-288">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-289">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0739c-289">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-291">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="0739c-291">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-292">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="0739c-292">Indicates when the object was installed.</span></span> <span data-ttu-id="0739c-293">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="0739c-293">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0739c-294">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-295">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="0739c-295">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-296">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0739c-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0739c-298">若 **為 TRUE**，則會鎖定裝置，防止使用者輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="0739c-298">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="0739c-299">這個屬性繼承自 [**CIM \_ UserDevice**](cim-userdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-299">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-300">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0739c-300">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-301">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0739c-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0739c-303">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0739c-303">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0739c-304">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-305">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0739c-305">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-306">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-308">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="0739c-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-309">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="0739c-309">Label by which the object is known.</span></span> <span data-ttu-id="0739c-310">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="0739c-310">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0739c-311">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-312">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0739c-312">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-315">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="0739c-315">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-316">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="0739c-316">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0739c-317">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0739c-317">Example: "\*PNP030b"</span></span>

<span data-ttu-id="0739c-318">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-319">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0739c-319">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-320">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0739c-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0739c-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0739c-322">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="0739c-322">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="0739c-323">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0739c-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="0739c-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-325">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="0739c-325">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0739c-326"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="0739c-326"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-327">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="0739c-327">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0739c-328"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="0739c-328"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-329">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="0739c-329">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0739c-330"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="0739c-330"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-331">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="0739c-331">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0739c-332"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="0739c-332"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-333">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="0739c-333">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0739c-334"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="0739c-334"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-335">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="0739c-335">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="0739c-336">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="0739c-336">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="0739c-337">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="0739c-337">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0739c-338"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="0739c-338"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-339">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="0739c-339">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0739c-340"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="0739c-340"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0739c-341">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="0739c-341">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0739c-342">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0739c-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-343">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="0739c-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0739c-345">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="0739c-345">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0739c-346">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="0739c-346">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0739c-347">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="0739c-347">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0739c-348">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="0739c-348">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0739c-349">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-350">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="0739c-350">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-351">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0739c-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0739c-353">顯示器的邏輯高度，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="0739c-353">Logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="0739c-354">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="0739c-354">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-355">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0739c-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0739c-357">顯示器的邏輯寬度，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="0739c-357">Logical width of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="0739c-358">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0739c-358">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-359">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-361">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="0739c-361">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-362">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="0739c-362">String that indicates the current status of the object.</span></span> <span data-ttu-id="0739c-363">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="0739c-363">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0739c-364">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="0739c-364">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0739c-365">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="0739c-365">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0739c-366">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0739c-366">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0739c-367">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="0739c-367">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0739c-368">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0739c-368">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0739c-369">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0739c-370">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="0739c-370">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0739c-371">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0739c-371">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0739c-372">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-372">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0739c-373">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-373">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0739c-374">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-374">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0739c-375">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-375">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0739c-376">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-376">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0739c-377">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-377">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0739c-378">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-378">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0739c-379">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-379">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0739c-380">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="0739c-380">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0739c-381">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-381">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0739c-382">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="0739c-382">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0739c-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0739c-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-384">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0739c-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-386">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="0739c-386">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0739c-387">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="0739c-387">State of the logical device.</span></span> <span data-ttu-id="0739c-388">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="0739c-388">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="0739c-389">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0739c-390">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0739c-390">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0739c-391">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="0739c-391">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0739c-392">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="0739c-392">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0739c-393">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="0739c-393">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0739c-394">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="0739c-394">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0739c-395">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0739c-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-396">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-398">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0739c-398">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0739c-399">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="0739c-399">The scoping system's creation class name.</span></span>

<span data-ttu-id="0739c-400">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0739c-401">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0739c-401">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0739c-402">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0739c-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0739c-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0739c-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0739c-404">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0739c-404">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0739c-405">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="0739c-405">The scoping system's name.</span></span>

<span data-ttu-id="0739c-406">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0739c-407">備註</span><span class="sxs-lookup"><span data-stu-id="0739c-407">Remarks</span></span>

<span data-ttu-id="0739c-408">**Cim \_ DesktopMonitor** 類別衍生自 [**cim \_ 顯示**](cim-display.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-408">The **CIM\_DesktopMonitor** class is derived from [**CIM\_Display**](cim-display.md).</span></span>

<span data-ttu-id="0739c-409">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="0739c-409">WMI does not implement this class.</span></span> <span data-ttu-id="0739c-410">如需衍生自 **CIM \_ DesktopMonitor** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="0739c-410">For more information about classes derived from **CIM\_DesktopMonitor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0739c-411">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0739c-411">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0739c-412">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0739c-412">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0739c-413">規格需求</span><span class="sxs-lookup"><span data-stu-id="0739c-413">Requirements</span></span>



| <span data-ttu-id="0739c-414">需求</span><span class="sxs-lookup"><span data-stu-id="0739c-414">Requirement</span></span> | <span data-ttu-id="0739c-415">值</span><span class="sxs-lookup"><span data-stu-id="0739c-415">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0739c-416">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0739c-416">Minimum supported client</span></span><br/> | <span data-ttu-id="0739c-417">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0739c-417">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0739c-418">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0739c-418">Minimum supported server</span></span><br/> | <span data-ttu-id="0739c-419">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0739c-419">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0739c-420">命名空間</span><span class="sxs-lookup"><span data-stu-id="0739c-420">Namespace</span></span><br/>                | <span data-ttu-id="0739c-421">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0739c-421">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0739c-422">MOF</span><span class="sxs-lookup"><span data-stu-id="0739c-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0739c-423"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0739c-423"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0739c-424">DLL</span><span class="sxs-lookup"><span data-stu-id="0739c-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0739c-425"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0739c-425"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0739c-426">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0739c-426">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0739c-427">**CIM \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="0739c-427">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

