---
description: Epresents 隨插即用裝置的屬性。
ms.assetid: 621f4410-8d8f-4afa-b0f0-beed263f3a13
ms.tgt_platform: multiple
title: Win32_PnPEntity 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity
- Win32_PnPEntity.Reset
- Win32_PnPEntity.SetPowerState
- Win32_PnPEntity.Availability
- Win32_PnPEntity.Caption
- Win32_PnPEntity.ClassGuid
- Win32_PnPEntity.CompatibleID
- Win32_PnPEntity.ConfigManagerErrorCode
- Win32_PnPEntity.ConfigManagerUserConfig
- Win32_PnPEntity.CreationClassName
- Win32_PnPEntity.Description
- Win32_PnPEntity.DeviceID
- Win32_PnPEntity.ErrorCleared
- Win32_PnPEntity.ErrorDescription
- Win32_PnPEntity.HardwareID
- Win32_PnPEntity.InstallDate
- Win32_PnPEntity.LastErrorCode
- Win32_PnPEntity.Manufacturer
- Win32_PnPEntity.Name
- Win32_PnPEntity.PNPClass
- Win32_PnPEntity.PNPDeviceID
- Win32_PnPEntity.PowerManagementCapabilities
- Win32_PnPEntity.PowerManagementSupported
- Win32_PnPEntity.Present
- Win32_PnPEntity.Service
- Win32_PnPEntity.Status
- Win32_PnPEntity.StatusInfo
- Win32_PnPEntity.SystemCreationClassName
- Win32_PnPEntity.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62eaa59944c9b71a1b8b3520969122ab23350bba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110233"
---
# <a name="win32_pnpentity-class"></a><span data-ttu-id="e4e3b-103">Win32 \_ PnPEntity 類別</span><span class="sxs-lookup"><span data-stu-id="e4e3b-103">Win32\_PnPEntity class</span></span>

<span data-ttu-id="e4e3b-104">**Win32 \_ PnPEntity** [WMI 類別](../wmisdk/retrieving-a-class.md)代表隨插即用裝置的屬性。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-104">The **Win32\_PnPEntity** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a Plug and Play device.</span></span> <span data-ttu-id="e4e3b-105">隨插即用的實體會顯示為位於主控台中裝置管理員的專案。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-105">Plug and Play entities are shown as entries in the Device Manager located in Control Panel.</span></span>

<span data-ttu-id="e4e3b-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e4e3b-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e3b-108">語法</span><span class="sxs-lookup"><span data-stu-id="e4e3b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FE28FD98-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPEntity : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  string   ClassGuid;
  string   CompatibleID[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareID[];
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  string   PNPClass;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  Present;
  string   Service;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="e4e3b-109">成員</span><span class="sxs-lookup"><span data-stu-id="e4e3b-109">Members</span></span>

<span data-ttu-id="e4e3b-110">**Win32 \_ PnPEntity** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e4e3b-110">The **Win32\_PnPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="e4e3b-111">方法</span><span class="sxs-lookup"><span data-stu-id="e4e3b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="e4e3b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e4e3b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e4e3b-113">方法</span><span class="sxs-lookup"><span data-stu-id="e4e3b-113">Methods</span></span>

<span data-ttu-id="e4e3b-114">**Win32 \_ PnPEntity** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-114">The **Win32\_PnPEntity** class has these methods.</span></span>



| <span data-ttu-id="e4e3b-115">方法</span><span class="sxs-lookup"><span data-stu-id="e4e3b-115">Method</span></span>                                                             | <span data-ttu-id="e4e3b-116">描述</span><span class="sxs-lookup"><span data-stu-id="e4e3b-116">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4e3b-117">**停用**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-117">**Disable**</span></span>](disable-win32-pnpentity.md)                         | <span data-ttu-id="e4e3b-118">停用此隨插即用裝置。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-118">Disables this Plug and Play device.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="e4e3b-119">**啟用**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-119">**Enable**</span></span>](enable-win32-pnpentity.md)                           | <span data-ttu-id="e4e3b-120">啟用此隨插即用裝置。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-120">Enables this Plug and Play device.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="e4e3b-121">**GetDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-121">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md) | <span data-ttu-id="e4e3b-122">取得此隨插即用裝置的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-122">Gets the specified properties of this Plug and Play device.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="e4e3b-123">**重設**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-123">**Reset**</span></span>                                                          | <span data-ttu-id="e4e3b-124">未實作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-124">Not implemented.</span></span> <span data-ttu-id="e4e3b-125">若要執行此方法，請參閱 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-125">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="e4e3b-126">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-126">**SetPowerState**</span></span>                                                  | <span data-ttu-id="e4e3b-127">未實作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-127">Not implemented.</span></span> <span data-ttu-id="e4e3b-128">若要執行此方法，請參閱 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-128">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e4e3b-129">屬性</span><span class="sxs-lookup"><span data-stu-id="e4e3b-129">Properties</span></span>

<span data-ttu-id="e4e3b-130">**Win32 \_ PnPEntity** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-130">The **Win32\_PnPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4e3b-131">**可用性**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-132">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-134">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="e4e3b-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-135">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-135">Availability and status of the device.</span></span>

<span data-ttu-id="e4e3b-136">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e4e3b-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e4e3b-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e4e3b-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-140">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="e4e3b-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e4e3b-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e4e3b-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e4e3b-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e4e3b-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="e4e3b-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e4e3b-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e4e3b-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e4e3b-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e4e3b-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e4e3b-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e4e3b-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-151">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e4e3b-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-153">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e4e3b-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-155">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e4e3b-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e4e3b-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-158">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e4e3b-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-160">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e4e3b-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-162">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e4e3b-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-164">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e4e3b-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-166">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e4e3b-167">**標題**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-170">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-170">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-171">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-171">Short description of the object.</span></span>

<span data-ttu-id="e4e3b-172">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-173">**ClassGuid**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-173">**ClassGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-176">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-177">此隨插即用裝置 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-177">Globally unique identifier (GUID) of this Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-178">**CompatibleID**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-178">**CompatibleID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-179">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="e4e3b-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-181">安裝程式用來將裝置與 INF 檔案比對的廠商定義識別碼串。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-181">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="e4e3b-182">裝置可以擁有與其關聯的相容識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-182">A device can have a list of compatible IDs associated with it.</span></span> <span data-ttu-id="e4e3b-183">相容的識別碼應該依照遞減的適用性順序列出。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-183">The compatible IDs should be listed in order of decreasing suitability.</span></span> <span data-ttu-id="e4e3b-184">如果安裝程式找不到符合其中一個裝置硬體識別碼的 INF 檔案，則會使用相容的識別碼來尋找 INF 檔案。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-184">If Setup cannot locate an INF file that matches one of a device's hardware IDs, it uses compatible IDs to locate an INF file.</span></span> <span data-ttu-id="e4e3b-185">相容識別碼具有與 **sensors** 相同的格式。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-185">A compatible ID has the same format as a **HardwareID**.</span></span> <span data-ttu-id="e4e3b-186">如需詳細資訊，請參閱 [Windows 驅動程式套件](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-186">For more information, see [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-187">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-188">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-190">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-190">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-191">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e4e3b-192">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e4e3b-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e4e3b-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-195">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e4e3b-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e4e3b-197">(1)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-198">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e4e3b-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e4e3b-200">(2)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e4e3b-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e4e3b-202">(3)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-203">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e4e3b-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e4e3b-205">(4)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-206">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-206">Device is not working properly.</span></span> <span data-ttu-id="e4e3b-207">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e4e3b-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e4e3b-209">(5)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-210">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e4e3b-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e4e3b-212">(6)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-213">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e4e3b-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e4e3b-215">(7)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e4e3b-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e4e3b-217">(8)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-218">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e4e3b-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e4e3b-220">(9)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-221">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-221">Device is not working properly.</span></span> <span data-ttu-id="e4e3b-222">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-222">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e4e3b-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e4e3b-224">(10)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-224">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-225">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-225">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e4e3b-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e4e3b-227">(11)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-227">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-228">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-228">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e4e3b-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e4e3b-230"> (12) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-230">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-231">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-231">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e4e3b-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e4e3b-233">(13)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-233">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-234">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-234">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e4e3b-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e4e3b-236">(14)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-236">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-237">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-237">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e4e3b-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e4e3b-239">(15)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-239">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-240">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-240">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e4e3b-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e4e3b-242">(16)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-242">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-243">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-243">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e4e3b-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e4e3b-245">(17)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-245">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-246">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-246">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e4e3b-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e4e3b-248">(18)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-248">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-249">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-249">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e4e3b-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e4e3b-251">(19)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-251">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e4e3b-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e4e3b-253">(20)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-253">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-254">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-254">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e4e3b-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e4e3b-256">(21)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-256">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-257">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-257">System failure.</span></span> <span data-ttu-id="e4e3b-258">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-258">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e4e3b-259">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-259">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e4e3b-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e4e3b-261">(22)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-261">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-262">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-262">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e4e3b-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e4e3b-264">(23)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-264">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-265">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-265">System failure.</span></span> <span data-ttu-id="e4e3b-266">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-266">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e4e3b-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e4e3b-268">(24)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-268">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-269">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-269">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e4e3b-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e4e3b-271">(25)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-271">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-272">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e4e3b-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e4e3b-274">(26)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-274">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-275">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e4e3b-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e4e3b-277">(27)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-277">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-278">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-278">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e4e3b-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e4e3b-280">(28)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-280">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-281">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-281">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e4e3b-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e4e3b-283">(29)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-283">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-284">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-284">Device is disabled.</span></span> <span data-ttu-id="e4e3b-285">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-285">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e4e3b-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e4e3b-287">(30)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-287">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-288">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-288">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e4e3b-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e4e3b-290"> (31) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-290">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-291">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-291">Device is not working properly.</span></span> <span data-ttu-id="e4e3b-292">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-292">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e4e3b-293">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-293">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-294">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-296">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-297">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-297">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e4e3b-298">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-299">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-299">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-302">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-302">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-303">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-303">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="e4e3b-304">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-304">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e4e3b-305">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-306">**說明**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-309">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-310">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-310">Description of the object.</span></span>

<span data-ttu-id="e4e3b-311">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-315">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-316">隨插即用裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-316">Identifier of the Plug and Play device.</span></span>

<span data-ttu-id="e4e3b-317">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-319">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-321">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="e4e3b-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-326">**LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="e4e3b-327">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-328">**Sensors**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-328">**HardwareID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-329">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="e4e3b-329">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-331">安裝程式用來將裝置與 INF 檔案比對的廠商定義識別碼串。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-331">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="e4e3b-332">通常，裝置會有相關聯的硬體識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-332">Normally, a device has an associated list of hardware IDs.</span></span> <span data-ttu-id="e4e3b-333">例外狀況是1394匯流排驅動程式，它不會使用硬體識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-333">An exception is the 1394 bus driver, which does not use hardware IDs.</span></span> <span data-ttu-id="e4e3b-334">清單中的第一個硬體識別碼應該是裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-334">The first hardware ID in the list should be the device ID.</span></span> <span data-ttu-id="e4e3b-335">其餘的識別碼應該依照遞減的適用性順序列出。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-335">The remaining IDs should be listed in order of decreasing suitability.</span></span>

<span data-ttu-id="e4e3b-336">硬體識別碼會以下列其中一種格式出現：</span><span class="sxs-lookup"><span data-stu-id="e4e3b-336">Hardware IDs appear in one the following formats:</span></span>

-   <span data-ttu-id="e4e3b-337">列舉值 \\ 列舉值特定-裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="e4e3b-337">enumerator\\enumerator-specific-device-ID</span></span>

    <span data-ttu-id="e4e3b-338">這是個別 PnP 裝置最常用的格式。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-338">This is the most common format for individual PnP devices.</span></span> <span data-ttu-id="e4e3b-339">列舉值的範例有 BIOS 或 ISAPNP。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-339">An example of an enumerator is the BIOS or ISAPNP.</span></span>

-   <span data-ttu-id="e4e3b-340">\*列舉值特定識別碼</span><span class="sxs-lookup"><span data-stu-id="e4e3b-340">\*enumerator-specific ID</span></span>

    <span data-ttu-id="e4e3b-341">星號 (\*) 表示一個以上的列舉值使用。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-341">An asterisk (\*) indicates use by more than one enumerator.</span></span>

-   <span data-ttu-id="e4e3b-342">裝置類別特定識別碼</span><span class="sxs-lookup"><span data-stu-id="e4e3b-342">device-class-specific ID</span></span>

    <span data-ttu-id="e4e3b-343">自訂格式。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-343">A custom format.</span></span>

<span data-ttu-id="e4e3b-344">硬體識別碼的範例包括：</span><span class="sxs-lookup"><span data-stu-id="e4e3b-344">Examples of Hardware IDs are:</span></span>

<dl> <dd><span data-ttu-id="e4e3b-345">根 \\ \* PNPOF08</span><span class="sxs-lookup"><span data-stu-id="e4e3b-345">root\\\*PNPOF08</span></span></dd> <dd><span data-ttu-id="e4e3b-346">PC \\ VEN \_ 1000&DEV \_ 001&子系統 \_ 00000000&REV \_ 02</span><span class="sxs-lookup"><span data-stu-id="e4e3b-346">PC\\VEN\_1000&DEV\_001&SUBSYS\_00000000&REV\_02</span></span></dd> </dl>

<span data-ttu-id="e4e3b-347">如需詳細資訊，請參閱 [Windows 驅動程式套件](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-347">For more information, see the [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-348">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-348">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-349">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-351">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="e4e3b-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-352">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-352">Date and time the object was installed.</span></span> <span data-ttu-id="e4e3b-353">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-353">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e4e3b-354">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-354">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-355">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-355">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-356">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-358">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-358">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e4e3b-359">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-360">**製造商**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-360">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-363">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-364">隨插即用裝置的製造商名稱。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-364">Name of the manufacturer of the Plug and Play device.</span></span>

<span data-ttu-id="e4e3b-365">範例： "Acme"</span><span class="sxs-lookup"><span data-stu-id="e4e3b-365">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-366">**名稱**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-366">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-369">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-369">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-370">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-370">Label by which the object is known.</span></span> <span data-ttu-id="e4e3b-371">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-371">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="e4e3b-372">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-373">**PNPClass**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-373">**PNPClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-376">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

> [!WARNING]
> <span data-ttu-id="e4e3b-377">雖然這個屬性是列在 MOF 檔案中，但實際上並不存在於類別中。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-377">This property, despite being listed in the MOF file, does not actually exist in the class.</span></span> <span data-ttu-id="e4e3b-378">此屬性只會在此描述，以提供完整性，並清楚說明 MOF 檔案本身。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-378">The property is described here only for the sake of completeness, and to clarify the MOF file itself.</span></span>

 

<span data-ttu-id="e4e3b-379">此隨插即用裝置的型別名稱。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-379">The name of the type of this Plug and Play device.</span></span>

<span data-ttu-id="e4e3b-380">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 這個屬性不在 MOF 檔案中。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-380">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not in the MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-381">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-381">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-384">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-384">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-385">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-385">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="e4e3b-386">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e4e3b-387">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e4e3b-387">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-388">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-388">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-389">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="e4e3b-389">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-391">未實作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-391">Not implemented.</span></span>

<span data-ttu-id="e4e3b-392">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e4e3b-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-394">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-394">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e4e3b-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-396">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-396">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e4e3b-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-398">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-398">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e4e3b-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-400">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-400">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e4e3b-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-402">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-402">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e4e3b-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-404">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-404">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="e4e3b-405">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-405">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="e4e3b-406">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-406">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e4e3b-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-408">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-408">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e4e3b-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e4e3b-410">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-410">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e4e3b-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-412">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-414">未實作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-414">Not implemented.</span></span>

<span data-ttu-id="e4e3b-415">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-416">**目前**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-416">**Present**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-417">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-419">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-419">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-420">此隨插即用裝置目前是否位於系統中。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-420">Whether this Plug and Play device is currently in the system.</span></span>

<span data-ttu-id="e4e3b-421">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-421">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-422">**服務**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-422">**Service**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-423">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-425">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-426">支援此隨插即用裝置的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-426">Name of the service that supports this Plug and Play device.</span></span> <span data-ttu-id="e4e3b-427">如需詳細資訊，請參閱 [**Win32 \_ SystemDriverPnPEntity**](win32-systemdriverpnpentity.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-427">For more information, see [**Win32\_SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span></span>

<span data-ttu-id="e4e3b-428">範例： "atapi"</span><span class="sxs-lookup"><span data-stu-id="e4e3b-428">Example: "atapi"</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-429">**狀態**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-430">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-432">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-433">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-433">Current status of the object.</span></span> <span data-ttu-id="e4e3b-434">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e4e3b-435">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e4e3b-436">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e4e3b-437">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e4e3b-438">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e4e3b-439">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e4e3b-440">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="e4e3b-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e4e3b-441">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e4e3b-442">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e4e3b-443">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e4e3b-444">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e4e3b-445">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e4e3b-446">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e4e3b-447">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e4e3b-448">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e4e3b-449">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e4e3b-450">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e4e3b-451">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e4e3b-452">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e4e3b-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-454">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-456">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="e4e3b-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-457">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-457">State of the logical device.</span></span> <span data-ttu-id="e4e3b-458">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e4e3b-459">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e4e3b-460">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e4e3b-461">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e4e3b-462">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e4e3b-463">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e4e3b-464">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="e4e3b-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e4e3b-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-466">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-467">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-468">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-469">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="e4e3b-470">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4e3b-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4e3b-472">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-473">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e4e3b-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4e3b-474">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e4e3b-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e4e3b-475">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-475">Name of the scoping system.</span></span>

<span data-ttu-id="e4e3b-476">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4e3b-477">備註</span><span class="sxs-lookup"><span data-stu-id="e4e3b-477">Remarks</span></span>

<span data-ttu-id="e4e3b-478">**Win32 \_ PnPEntity** 類別衍生自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-478">The **Win32\_PnPEntity** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e4e3b-479">範例</span><span class="sxs-lookup"><span data-stu-id="e4e3b-479">Examples</span></span>

<span data-ttu-id="e4e3b-480">TechNet 資源庫上的 [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell 範例會使用 **Win32 \_ PNPENTITY** ，以使用 WMI 抓取無法運作的硬體清單。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-480">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_PnPEntity** to retrieve a list of non-working hardware using WMI.</span></span>

<span data-ttu-id="e4e3b-481">下列 VBScript 程式碼範例會藉由建立遠端電腦名稱稱陣列，然後在每部電腦上顯示隨插即用裝置（Win32 PnPEntity 的實例）的名稱，連接到同一網域中的一組遠端電腦 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e4e3b-481">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of Win32\_PnPEntity—on each computer.</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer& "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="e4e3b-482">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4e3b-482">Requirements</span></span>



| <span data-ttu-id="e4e3b-483">需求</span><span class="sxs-lookup"><span data-stu-id="e4e3b-483">Requirement</span></span> | <span data-ttu-id="e4e3b-484">值</span><span class="sxs-lookup"><span data-stu-id="e4e3b-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e3b-485">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4e3b-485">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e3b-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4e3b-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e4e3b-487">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4e3b-487">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e3b-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4e3b-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e4e3b-489">命名空間</span><span class="sxs-lookup"><span data-stu-id="e4e3b-489">Namespace</span></span><br/>                | <span data-ttu-id="e4e3b-490">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e4e3b-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e4e3b-491">MOF</span><span class="sxs-lookup"><span data-stu-id="e4e3b-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4e3b-492"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4e3b-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4e3b-493">DLL</span><span class="sxs-lookup"><span data-stu-id="e4e3b-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4e3b-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4e3b-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4e3b-495">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4e3b-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e3b-496">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="e4e3b-496">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="e4e3b-497">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="e4e3b-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e4e3b-498">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="e4e3b-498">Connecting to WMI on a Remote Computer</span></span>](../wmisdk/connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="e4e3b-499">WMI 工作：電腦硬體</span><span class="sxs-lookup"><span data-stu-id="e4e3b-499">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
