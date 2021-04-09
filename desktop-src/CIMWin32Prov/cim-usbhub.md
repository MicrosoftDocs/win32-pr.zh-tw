---
description: CIM \_ USBHub 類別代表 USB 集線器的功能和管理。
ms.assetid: 33618963-3053-4c01-992e-aa6d9774f84b
ms.tgt_platform: multiple
title: CIM_USBHub 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub
- CIM_USBHub.Availability
- CIM_USBHub.Caption
- CIM_USBHub.ClassCode
- CIM_USBHub.ConfigManagerErrorCode
- CIM_USBHub.ConfigManagerUserConfig
- CIM_USBHub.CreationClassName
- CIM_USBHub.CurrentAlternateSettings
- CIM_USBHub.CurrentConfigValue
- CIM_USBHub.Description
- CIM_USBHub.DeviceID
- CIM_USBHub.ErrorCleared
- CIM_USBHub.ErrorDescription
- CIM_USBHub.GangSwitched
- CIM_USBHub.InstallDate
- CIM_USBHub.LastErrorCode
- CIM_USBHub.Name
- CIM_USBHub.NumberOfConfigs
- CIM_USBHub.NumberOfPorts
- CIM_USBHub.PNPDeviceID
- CIM_USBHub.PowerManagementCapabilities
- CIM_USBHub.PowerManagementSupported
- CIM_USBHub.ProtocolCode
- CIM_USBHub.Status
- CIM_USBHub.StatusInfo
- CIM_USBHub.SubclassCode
- CIM_USBHub.SystemCreationClassName
- CIM_USBHub.SystemName
- CIM_USBHub.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9213b155b069b4aa19f2cbe910c0614f511ff8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936061"
---
# <a name="cim_usbhub-class"></a><span data-ttu-id="cf67c-103">CIM \_ USBHub 類別</span><span class="sxs-lookup"><span data-stu-id="cf67c-103">CIM\_USBHub class</span></span>

<span data-ttu-id="cf67c-104">**CIM \_ USBHub** 類別代表 USB 集線器的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="cf67c-104">The **CIM\_USBHub** class represents the capabilities and management of a USB hub.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf67c-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="cf67c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cf67c-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cf67c-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf67c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cf67c-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="cf67c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf67c-109">語法</span><span class="sxs-lookup"><span data-stu-id="cf67c-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBHub : CIM_USBDevice
{
  uint16   Availability;
  string   Caption;
  uint8    ClassCode;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint8    CurrentAlternateSettings[];
  uint8    CurrentConfigValue;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  boolean  GangSwitched;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
  uint8    NumberOfPorts;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    ProtocolCode;
  string   Status;
  uint16   StatusInfo;
  uint8    SubclassCode;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   USBVersion;
};
```

## <a name="members"></a><span data-ttu-id="cf67c-110">成員</span><span class="sxs-lookup"><span data-stu-id="cf67c-110">Members</span></span>

<span data-ttu-id="cf67c-111">**CIM \_ USBHub** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cf67c-111">The **CIM\_USBHub** class has these types of members:</span></span>

-   [<span data-ttu-id="cf67c-112">方法</span><span class="sxs-lookup"><span data-stu-id="cf67c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="cf67c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="cf67c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cf67c-114">方法</span><span class="sxs-lookup"><span data-stu-id="cf67c-114">Methods</span></span>

<span data-ttu-id="cf67c-115">**CIM \_ USBHub** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="cf67c-115">The **CIM\_USBHub** class has these methods.</span></span>



| <span data-ttu-id="cf67c-116">方法</span><span class="sxs-lookup"><span data-stu-id="cf67c-116">Method</span></span>                                                            | <span data-ttu-id="cf67c-117">描述</span><span class="sxs-lookup"><span data-stu-id="cf67c-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf67c-118">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="cf67c-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbhub.md) | <span data-ttu-id="cf67c-119">傳回 USB 裝置描述項。</span><span class="sxs-lookup"><span data-stu-id="cf67c-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="cf67c-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="cf67c-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="cf67c-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="cf67c-121">**Reset**</span></span>](reset-method-in-class-cim-usbhub.md)                 | <span data-ttu-id="cf67c-122">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="cf67c-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="cf67c-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="cf67c-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="cf67c-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cf67c-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbhub.md) | <span data-ttu-id="cf67c-125">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="cf67c-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="cf67c-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="cf67c-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cf67c-127">屬性</span><span class="sxs-lookup"><span data-stu-id="cf67c-127">Properties</span></span>

<span data-ttu-id="cf67c-128">**CIM \_ USBHub** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cf67c-128">The **CIM\_USBHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf67c-129">**可用性**</span><span class="sxs-lookup"><span data-stu-id="cf67c-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf67c-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-132">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="cf67c-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-133">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="cf67c-133">Availability and status of the device.</span></span>

<span data-ttu-id="cf67c-134">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cf67c-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="cf67c-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cf67c-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="cf67c-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="cf67c-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="cf67c-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-138">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="cf67c-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="cf67c-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="cf67c-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="cf67c-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="cf67c-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cf67c-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="cf67c-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="cf67c-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="cf67c-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="cf67c-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="cf67c-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="cf67c-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="cf67c-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cf67c-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="cf67c-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="cf67c-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="cf67c-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="cf67c-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="cf67c-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="cf67c-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="cf67c-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-149">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="cf67c-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="cf67c-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="cf67c-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-151">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="cf67c-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="cf67c-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="cf67c-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-153">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="cf67c-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="cf67c-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="cf67c-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="cf67c-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="cf67c-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-156">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="cf67c-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="cf67c-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="cf67c-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-158">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="cf67c-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="cf67c-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="cf67c-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-160">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="cf67c-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="cf67c-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="cf67c-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-162">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="cf67c-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="cf67c-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="cf67c-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-164">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="cf67c-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cf67c-165">**標題**</span><span class="sxs-lookup"><span data-stu-id="cf67c-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-168">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-169">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="cf67c-169">Short textual description of the object.</span></span>

<span data-ttu-id="cf67c-170">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-171">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="cf67c-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-172">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="cf67c-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-174">USB 類別代碼。</span><span class="sxs-lookup"><span data-stu-id="cf67c-174">USB class code.</span></span>

<span data-ttu-id="cf67c-175">這個屬性繼承自 [**CIM \_ USBDevice**](cim-usbdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-175">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-176">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cf67c-176">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-177">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cf67c-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-178">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-179">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-179">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-180">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cf67c-180">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="cf67c-181">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-181">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="cf67c-182"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-182"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="cf67c-183"> (0)</span><span class="sxs-lookup"><span data-stu-id="cf67c-183">(0)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-184">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="cf67c-184">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="cf67c-185"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-185"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="cf67c-186">(1)</span><span class="sxs-lookup"><span data-stu-id="cf67c-186">(1)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-187">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="cf67c-187">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cf67c-188"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-188"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="cf67c-189">(2)</span><span class="sxs-lookup"><span data-stu-id="cf67c-189">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="cf67c-190"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-190"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="cf67c-191">(3)</span><span class="sxs-lookup"><span data-stu-id="cf67c-191">(3)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-192">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="cf67c-192">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cf67c-193"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-193"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="cf67c-194">(4)</span><span class="sxs-lookup"><span data-stu-id="cf67c-194">(4)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-195">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="cf67c-195">Device is not working properly.</span></span> <span data-ttu-id="cf67c-196">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="cf67c-196">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="cf67c-197"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-197"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="cf67c-198">(5)</span><span class="sxs-lookup"><span data-stu-id="cf67c-198">(5)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-199">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="cf67c-199">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="cf67c-200"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-200"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="cf67c-201">(6)</span><span class="sxs-lookup"><span data-stu-id="cf67c-201">(6)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-202">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="cf67c-202">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="cf67c-203"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-203"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="cf67c-204">(7)</span><span class="sxs-lookup"><span data-stu-id="cf67c-204">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="cf67c-205"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-205"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="cf67c-206">(8)</span><span class="sxs-lookup"><span data-stu-id="cf67c-206">(8)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-207">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="cf67c-207">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="cf67c-208"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-208"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="cf67c-209">(9)</span><span class="sxs-lookup"><span data-stu-id="cf67c-209">(9)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-210">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="cf67c-210">Device is not working properly.</span></span> <span data-ttu-id="cf67c-211">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="cf67c-211">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="cf67c-212"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-212"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="cf67c-213">(10)</span><span class="sxs-lookup"><span data-stu-id="cf67c-213">(10)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-214">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="cf67c-214">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="cf67c-215"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-215"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="cf67c-216">(11)</span><span class="sxs-lookup"><span data-stu-id="cf67c-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-217">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="cf67c-217">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="cf67c-218"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-218"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="cf67c-219"> (12) </span><span class="sxs-lookup"><span data-stu-id="cf67c-219">(12)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-220">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="cf67c-220">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="cf67c-221"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-221"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="cf67c-222">(13)</span><span class="sxs-lookup"><span data-stu-id="cf67c-222">(13)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-223">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="cf67c-223">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="cf67c-224"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-224"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="cf67c-225">(14)</span><span class="sxs-lookup"><span data-stu-id="cf67c-225">(14)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-226">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="cf67c-226">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="cf67c-227"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-227"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="cf67c-228">(15)</span><span class="sxs-lookup"><span data-stu-id="cf67c-228">(15)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-229">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="cf67c-229">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="cf67c-230"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-230"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="cf67c-231">(16)</span><span class="sxs-lookup"><span data-stu-id="cf67c-231">(16)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-232">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="cf67c-232">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="cf67c-233"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-233"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="cf67c-234">(17)</span><span class="sxs-lookup"><span data-stu-id="cf67c-234">(17)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-235">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="cf67c-235">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cf67c-236"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-236"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="cf67c-237">(18)</span><span class="sxs-lookup"><span data-stu-id="cf67c-237">(18)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-238">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="cf67c-238">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="cf67c-239"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-239"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="cf67c-240">(19)</span><span class="sxs-lookup"><span data-stu-id="cf67c-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cf67c-241"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-241"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="cf67c-242">(20)</span><span class="sxs-lookup"><span data-stu-id="cf67c-242">(20)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-243">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="cf67c-243">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="cf67c-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="cf67c-245">(21)</span><span class="sxs-lookup"><span data-stu-id="cf67c-245">(21)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-246">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="cf67c-246">System failure.</span></span> <span data-ttu-id="cf67c-247">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="cf67c-247">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="cf67c-248">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="cf67c-248">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="cf67c-249"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-249"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="cf67c-250">(22)</span><span class="sxs-lookup"><span data-stu-id="cf67c-250">(22)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-251">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="cf67c-251">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="cf67c-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="cf67c-253">(23)</span><span class="sxs-lookup"><span data-stu-id="cf67c-253">(23)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-254">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="cf67c-254">System failure.</span></span> <span data-ttu-id="cf67c-255">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="cf67c-255">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="cf67c-256"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-256"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="cf67c-257">(24)</span><span class="sxs-lookup"><span data-stu-id="cf67c-257">(24)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-258">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="cf67c-258">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cf67c-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cf67c-260">(25)</span><span class="sxs-lookup"><span data-stu-id="cf67c-260">(25)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-261">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="cf67c-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cf67c-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cf67c-263">(26)</span><span class="sxs-lookup"><span data-stu-id="cf67c-263">(26)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-264">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="cf67c-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="cf67c-265"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-265"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="cf67c-266">(27)</span><span class="sxs-lookup"><span data-stu-id="cf67c-266">(27)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-267">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="cf67c-267">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="cf67c-268"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-268"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="cf67c-269">(28)</span><span class="sxs-lookup"><span data-stu-id="cf67c-269">(28)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-270">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="cf67c-270">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="cf67c-271"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-271"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="cf67c-272">(29)</span><span class="sxs-lookup"><span data-stu-id="cf67c-272">(29)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-273">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="cf67c-273">Device is disabled.</span></span> <span data-ttu-id="cf67c-274">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="cf67c-274">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="cf67c-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="cf67c-276">(30)</span><span class="sxs-lookup"><span data-stu-id="cf67c-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-277">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="cf67c-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cf67c-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="cf67c-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="cf67c-279"> (31) </span><span class="sxs-lookup"><span data-stu-id="cf67c-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-280">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="cf67c-280">Device is not working properly.</span></span> <span data-ttu-id="cf67c-281">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="cf67c-281">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cf67c-282">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="cf67c-282">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-283">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cf67c-283">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-285">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-285">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-286">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="cf67c-286">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="cf67c-287">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cf67c-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-289">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-290">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-291">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cf67c-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-292">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf67c-292">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cf67c-293">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="cf67c-293">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cf67c-294">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-295">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="cf67c-295">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-296">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="cf67c-296">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-298">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ USBDevice**](cim-usbdevice.md).**CurrentConfigValue**") </span><span class="sxs-lookup"><span data-stu-id="cf67c-298">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_USBDevice**](cim-usbdevice.md).**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-299">在目前選取的設定中，每個介面的 USB 替代設定 (由 **CurrentConfigValue** 屬性) 指出。</span><span class="sxs-lookup"><span data-stu-id="cf67c-299">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="cf67c-300">此陣列針對設定中的每個介面都有一個專案。</span><span class="sxs-lookup"><span data-stu-id="cf67c-300">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="cf67c-301">如果 **CurrentConfigValue** 屬性的值為 0 (零) ，表示未設定裝置，則表示未定義該陣列。</span><span class="sxs-lookup"><span data-stu-id="cf67c-301">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="cf67c-302">如需有關剖析這個八位字串的詳細資訊，請參閱 USB 規格。</span><span class="sxs-lookup"><span data-stu-id="cf67c-302">For more information about parsing this octet string, see the USB specification.</span></span>

<span data-ttu-id="cf67c-303">這個屬性繼承自 [**CIM \_ USBDevice**](cim-usbdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-303">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-304">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="cf67c-304">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-305">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="cf67c-305">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-307">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ USBDevice**](cim-usbdevice.md).**CurrentAlternateSettings**") </span><span class="sxs-lookup"><span data-stu-id="cf67c-307">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_USBDevice**](cim-usbdevice.md).**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-308">目前為裝置選取的設定。</span><span class="sxs-lookup"><span data-stu-id="cf67c-308">Configuration currently selected for the device.</span></span> <span data-ttu-id="cf67c-309">如果此值為 0 (零) ，則不會設定裝置。</span><span class="sxs-lookup"><span data-stu-id="cf67c-309">If this value is 0 (zero), the device is unconfigured.</span></span>

<span data-ttu-id="cf67c-310">這個屬性繼承自 [**CIM \_ USBDevice**](cim-usbdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-310">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-311">**說明**</span><span class="sxs-lookup"><span data-stu-id="cf67c-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-312">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-314">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-315">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="cf67c-315">Textual description of the object.</span></span>

<span data-ttu-id="cf67c-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-317">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cf67c-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-318">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-320">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cf67c-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-321">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="cf67c-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="cf67c-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="cf67c-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-324">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cf67c-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-326">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="cf67c-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="cf67c-327">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cf67c-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-331">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="cf67c-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="cf67c-332">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-333">**GangSwitched**</span><span class="sxs-lookup"><span data-stu-id="cf67c-333">**GangSwitched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-334">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cf67c-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-336">若 **為 TRUE**，則電源會同時切換至中樞上的所有埠。</span><span class="sxs-lookup"><span data-stu-id="cf67c-336">If **TRUE**, power is switched to all ports on the hub simultaneously.</span></span> <span data-ttu-id="cf67c-337">若為 **FALSE**，則會針對每個埠個別切換電源。</span><span class="sxs-lookup"><span data-stu-id="cf67c-337">If **FALSE**, power is switched individually for each port.</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cf67c-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-339">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="cf67c-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-341">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="cf67c-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-342">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="cf67c-342">Date and time the object was installed.</span></span> <span data-ttu-id="cf67c-343">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="cf67c-343">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cf67c-344">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cf67c-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-346">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cf67c-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-348">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cf67c-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="cf67c-349">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-350">**名稱**</span><span class="sxs-lookup"><span data-stu-id="cf67c-350">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-351">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-353">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-353">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-354">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="cf67c-354">Label by which the object is known.</span></span> <span data-ttu-id="cf67c-355">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="cf67c-355">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cf67c-356">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-357">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="cf67c-357">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-358">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="cf67c-358">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-360">為裝置定義的裝置設定數目。</span><span class="sxs-lookup"><span data-stu-id="cf67c-360">Number of device configurations that are defined for the device.</span></span>

<span data-ttu-id="cf67c-361">這個屬性繼承自 [**CIM \_ USBDevice**](cim-usbdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-361">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-362">**NumberOfPorts**</span><span class="sxs-lookup"><span data-stu-id="cf67c-362">**NumberOfPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-363">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="cf67c-363">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-365">中樞上下游埠的數目，包括內嵌于中樞晶片中的埠。</span><span class="sxs-lookup"><span data-stu-id="cf67c-365">Number of downstream ports on the hub, including those embedded in the hub's silicon.</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-366">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="cf67c-366">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-369">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-369">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-370">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf67c-370">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="cf67c-371">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="cf67c-371">Example: "\*PNP030b"</span></span>

<span data-ttu-id="cf67c-372">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-373">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="cf67c-373">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-374">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="cf67c-374">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-376">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="cf67c-376">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="cf67c-377">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cf67c-378"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="cf67c-378"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="cf67c-379"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="cf67c-379"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cf67c-380"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="cf67c-380"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cf67c-381"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="cf67c-381"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-382">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="cf67c-382">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="cf67c-383"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="cf67c-383"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-384">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="cf67c-384">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="cf67c-385"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="cf67c-385"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-386">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="cf67c-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="cf67c-387">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="cf67c-387">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="cf67c-388">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-388">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="cf67c-389"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="cf67c-389"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-390">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="cf67c-390">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="cf67c-391"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="cf67c-391"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cf67c-392">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="cf67c-392">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cf67c-393">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="cf67c-393">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-394">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cf67c-394">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-396">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="cf67c-396">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="cf67c-397">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="cf67c-397">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="cf67c-398">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="cf67c-398">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="cf67c-399">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="cf67c-399">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="cf67c-400">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-401">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="cf67c-401">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-402">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="cf67c-402">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-404">USB 通訊協定代碼。</span><span class="sxs-lookup"><span data-stu-id="cf67c-404">USB protocol code.</span></span>

<span data-ttu-id="cf67c-405">這個屬性繼承自 [**CIM \_ USBDevice**](cim-usbdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-405">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-406">**狀態**</span><span class="sxs-lookup"><span data-stu-id="cf67c-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-407">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-409">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-409">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-410">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="cf67c-410">Current status of the object.</span></span>

<span data-ttu-id="cf67c-411">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cf67c-412">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="cf67c-412">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cf67c-413">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-413">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cf67c-414">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-414">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cf67c-415">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-415">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cf67c-416">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-416">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cf67c-417">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-417">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cf67c-418">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-418">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cf67c-419">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-419">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cf67c-420">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-420">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cf67c-421">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-421">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cf67c-422">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-422">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cf67c-423">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-423">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cf67c-424">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="cf67c-424">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cf67c-425">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cf67c-425">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-426">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf67c-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-427">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-428">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="cf67c-428">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-429">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="cf67c-429">State of the logical device.</span></span> <span data-ttu-id="cf67c-430">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="cf67c-430">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="cf67c-431">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cf67c-432">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="cf67c-432">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cf67c-433">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="cf67c-433">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cf67c-434">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="cf67c-434">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cf67c-435">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="cf67c-435">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cf67c-436">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="cf67c-436">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cf67c-437">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="cf67c-437">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-438">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="cf67c-438">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-439">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-440">USB 子類別程式碼。</span><span class="sxs-lookup"><span data-stu-id="cf67c-440">USB subclass code.</span></span>

<span data-ttu-id="cf67c-441">這個屬性繼承自 [**CIM \_ USBDevice**](cim-usbdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-441">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-442">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cf67c-442">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-443">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-445">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cf67c-445">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-446">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="cf67c-446">Scoping system's creation class name.</span></span>

<span data-ttu-id="cf67c-447">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-448">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cf67c-448">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-449">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cf67c-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-451">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cf67c-451">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-452">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="cf67c-452">Scoping system's name.</span></span>

<span data-ttu-id="cf67c-453">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf67c-454">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="cf67c-454">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf67c-455">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="cf67c-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf67c-456">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cf67c-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf67c-457">USB 裝置支援的最新 USB 版本。</span><span class="sxs-lookup"><span data-stu-id="cf67c-457">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="cf67c-458">這個屬性會以二進位編碼的十進位 (BCD) ，其中小數點是在第二個和第三位數之間隱含的。</span><span class="sxs-lookup"><span data-stu-id="cf67c-458">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="cf67c-459">例如，0x201 的值表示支援2.01 版。</span><span class="sxs-lookup"><span data-stu-id="cf67c-459">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

<span data-ttu-id="cf67c-460">這個屬性繼承自 [**CIM \_ USBDevice**](cim-usbdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-460">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf67c-461">備註</span><span class="sxs-lookup"><span data-stu-id="cf67c-461">Remarks</span></span>

<span data-ttu-id="cf67c-462">**Cim \_ USBHub** 類別衍生自 [**cim \_ USBDevice**](cim-usbdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-462">The **CIM\_USBHub** class is derived from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

<span data-ttu-id="cf67c-463">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="cf67c-463">WMI does not implement this class.</span></span> <span data-ttu-id="cf67c-464">針對衍生自 **CIM \_ USBHUB** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cf67c-464">For WMI classes derived from **CIM\_USBHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cf67c-465">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="cf67c-465">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cf67c-466">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="cf67c-466">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf67c-467">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf67c-467">Requirements</span></span>



| <span data-ttu-id="cf67c-468">需求</span><span class="sxs-lookup"><span data-stu-id="cf67c-468">Requirement</span></span> | <span data-ttu-id="cf67c-469">值</span><span class="sxs-lookup"><span data-stu-id="cf67c-469">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf67c-470">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf67c-470">Minimum supported client</span></span><br/> | <span data-ttu-id="cf67c-471">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf67c-471">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf67c-472">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf67c-472">Minimum supported server</span></span><br/> | <span data-ttu-id="cf67c-473">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf67c-473">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf67c-474">命名空間</span><span class="sxs-lookup"><span data-stu-id="cf67c-474">Namespace</span></span><br/>                | <span data-ttu-id="cf67c-475">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cf67c-475">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf67c-476">MOF</span><span class="sxs-lookup"><span data-stu-id="cf67c-476">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf67c-477"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf67c-477"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf67c-478">DLL</span><span class="sxs-lookup"><span data-stu-id="cf67c-478">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf67c-479"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf67c-479"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf67c-480">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf67c-480">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf67c-481">**CIM \_ USBDevice**</span><span class="sxs-lookup"><span data-stu-id="cf67c-481">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

