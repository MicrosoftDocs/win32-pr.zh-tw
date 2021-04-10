---
description: CIM \_ POTSModem 類別代表一種裝置，可透過連接到單純的舊電話系統 (POTS) 網路，將二進位資料轉譯成 wave modulations 進行音效型傳輸。
ms.assetid: 2740f305-769d-464c-910a-998522f5121b
ms.tgt_platform: multiple
title: CIM_POTSModem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_POTSModem
- CIM_POTSModem.AnswerMode
- CIM_POTSModem.Availability
- CIM_POTSModem.Caption
- CIM_POTSModem.CompressionInfo
- CIM_POTSModem.ConfigManagerErrorCode
- CIM_POTSModem.ConfigManagerUserConfig
- CIM_POTSModem.CountriesSupported
- CIM_POTSModem.CountrySelected
- CIM_POTSModem.CreationClassName
- CIM_POTSModem.CurrentPasswords
- CIM_POTSModem.Description
- CIM_POTSModem.DeviceID
- CIM_POTSModem.DialType
- CIM_POTSModem.ErrorCleared
- CIM_POTSModem.ErrorControlInfo
- CIM_POTSModem.ErrorDescription
- CIM_POTSModem.InactivityTimeout
- CIM_POTSModem.InstallDate
- CIM_POTSModem.LastErrorCode
- CIM_POTSModem.MaxBaudRateToPhone
- CIM_POTSModem.MaxBaudRateToSerialPort
- CIM_POTSModem.MaxNumberOfPasswords
- CIM_POTSModem.ModulationScheme
- CIM_POTSModem.Name
- CIM_POTSModem.PNPDeviceID
- CIM_POTSModem.PowerManagementCapabilities
- CIM_POTSModem.PowerManagementSupported
- CIM_POTSModem.RingsBeforeAnswer
- CIM_POTSModem.SpeakerVolumeInfo
- CIM_POTSModem.Status
- CIM_POTSModem.StatusInfo
- CIM_POTSModem.SupportsCallback
- CIM_POTSModem.SupportsSynchronousConnect
- CIM_POTSModem.SystemCreationClassName
- CIM_POTSModem.SystemName
- CIM_POTSModem.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7fbaeedd1de4006dfdccbcec313a7428d7b7f03
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936343"
---
# <a name="cim_potsmodem-class"></a><span data-ttu-id="6bb38-103">CIM \_ POTSModem 類別</span><span class="sxs-lookup"><span data-stu-id="6bb38-103">CIM\_POTSModem class</span></span>

<span data-ttu-id="6bb38-104">**CIM \_ POTSModem** 類別代表一種裝置，可透過連接到單純的舊電話系統 (POTS) 網路，將二進位資料轉譯成 wave modulations 進行音效型傳輸。</span><span class="sxs-lookup"><span data-stu-id="6bb38-104">The **CIM\_POTSModem** class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6bb38-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="6bb38-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6bb38-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6bb38-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6bb38-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6bb38-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="6bb38-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb38-109">語法</span><span class="sxs-lookup"><span data-stu-id="6bb38-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C546-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_POTSModem : CIM_LogicalDevice
{
  uint16   AnswerMode;
  uint16   Availability;
  string   Caption;
  uint16   CompressionInfo;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  string   Description;
  string   DeviceID;
  uint16   DialType;
  boolean  ErrorCleared;
  uint16   ErrorControlInfo;
  string   ErrorDescription;
  uint32   InactivityTimeout;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    RingsBeforeAnswer;
  uint16   SpeakerVolumeInfo;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="6bb38-110">成員</span><span class="sxs-lookup"><span data-stu-id="6bb38-110">Members</span></span>

<span data-ttu-id="6bb38-111">**CIM \_ POTSModem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6bb38-111">The **CIM\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="6bb38-112">方法</span><span class="sxs-lookup"><span data-stu-id="6bb38-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="6bb38-113">屬性</span><span class="sxs-lookup"><span data-stu-id="6bb38-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6bb38-114">方法</span><span class="sxs-lookup"><span data-stu-id="6bb38-114">Methods</span></span>

<span data-ttu-id="6bb38-115">**CIM \_ POTSModem** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6bb38-115">The **CIM\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="6bb38-116">方法</span><span class="sxs-lookup"><span data-stu-id="6bb38-116">Method</span></span>                                                               | <span data-ttu-id="6bb38-117">描述</span><span class="sxs-lookup"><span data-stu-id="6bb38-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bb38-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="6bb38-118">**Reset**</span></span>](reset-method-in-class-cim-potsmodem.md)                 | <span data-ttu-id="6bb38-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="6bb38-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="6bb38-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="6bb38-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="6bb38-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6bb38-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-potsmodem.md) | <span data-ttu-id="6bb38-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="6bb38-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="6bb38-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="6bb38-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6bb38-124">屬性</span><span class="sxs-lookup"><span data-stu-id="6bb38-124">Properties</span></span>

<span data-ttu-id="6bb38-125">**CIM \_ POTSModem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6bb38-125">The **CIM\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6bb38-126">**AnswerMode**</span><span class="sxs-lookup"><span data-stu-id="6bb38-126">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6bb38-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-129">數據機目前的自動回應或回呼設定。</span><span class="sxs-lookup"><span data-stu-id="6bb38-129">Current auto-answer or call-back setting for the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-130">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6bb38-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6bb38-131">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6bb38-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6bb38-132">**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="6bb38-132">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="6bb38-133">**手動回答** (3) </span><span class="sxs-lookup"><span data-stu-id="6bb38-133">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="6bb38-134">**自動回應** (4) </span><span class="sxs-lookup"><span data-stu-id="6bb38-134">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="6bb38-135">**使用回撥 (5) 的自動解答**</span><span class="sxs-lookup"><span data-stu-id="6bb38-135">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-136">**可用性**</span><span class="sxs-lookup"><span data-stu-id="6bb38-136">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-137">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6bb38-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="6bb38-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-140">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="6bb38-140">Availability and status of the device.</span></span>

<span data-ttu-id="6bb38-141">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-141">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6bb38-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6bb38-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="6bb38-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6bb38-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="6bb38-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6bb38-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="6bb38-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6bb38-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="6bb38-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6bb38-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="6bb38-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6bb38-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="6bb38-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6bb38-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="6bb38-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6bb38-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="6bb38-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6bb38-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="6bb38-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6bb38-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="6bb38-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6bb38-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="6bb38-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6bb38-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="6bb38-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-155">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="6bb38-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6bb38-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="6bb38-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-157">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="6bb38-157">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6bb38-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="6bb38-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-159">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="6bb38-159">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6bb38-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="6bb38-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6bb38-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="6bb38-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-162">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="6bb38-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6bb38-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="6bb38-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-164">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="6bb38-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6bb38-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="6bb38-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-166">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="6bb38-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6bb38-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="6bb38-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-168">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="6bb38-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6bb38-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="6bb38-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-170">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="6bb38-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-171">**標題**</span><span class="sxs-lookup"><span data-stu-id="6bb38-171">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-174">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-175">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="6bb38-175">Short textual description of the object.</span></span>

<span data-ttu-id="6bb38-176">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-177">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="6bb38-177">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-178">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6bb38-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-180">數據機的資料壓縮特性。</span><span class="sxs-lookup"><span data-stu-id="6bb38-180">Data compression characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-181">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6bb38-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6bb38-182">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6bb38-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="6bb38-183">**無壓縮** (2) </span><span class="sxs-lookup"><span data-stu-id="6bb38-183">**No Compression** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="6bb38-184">**MNP 5** (3) </span><span class="sxs-lookup"><span data-stu-id="6bb38-184">**MNP 5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="6bb38-185">**42bis** (4) </span><span class="sxs-lookup"><span data-stu-id="6bb38-185">**V.42bis** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-186">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6bb38-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-187">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6bb38-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-188">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-189">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-190">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6bb38-190">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6bb38-191">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6bb38-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6bb38-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="6bb38-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-194">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="6bb38-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6bb38-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6bb38-196">(1)</span><span class="sxs-lookup"><span data-stu-id="6bb38-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-197">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="6bb38-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6bb38-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6bb38-199">(2)</span><span class="sxs-lookup"><span data-stu-id="6bb38-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6bb38-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6bb38-201">(3)</span><span class="sxs-lookup"><span data-stu-id="6bb38-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-202">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="6bb38-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6bb38-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6bb38-204">(4)</span><span class="sxs-lookup"><span data-stu-id="6bb38-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-205">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6bb38-205">Device is not working properly.</span></span> <span data-ttu-id="6bb38-206">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="6bb38-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6bb38-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6bb38-208">(5)</span><span class="sxs-lookup"><span data-stu-id="6bb38-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-209">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="6bb38-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6bb38-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6bb38-211">(6)</span><span class="sxs-lookup"><span data-stu-id="6bb38-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-212">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="6bb38-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6bb38-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6bb38-214">(7)</span><span class="sxs-lookup"><span data-stu-id="6bb38-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6bb38-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6bb38-216">(8)</span><span class="sxs-lookup"><span data-stu-id="6bb38-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-217">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="6bb38-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6bb38-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6bb38-219">(9)</span><span class="sxs-lookup"><span data-stu-id="6bb38-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-220">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6bb38-220">Device is not working properly.</span></span> <span data-ttu-id="6bb38-221">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="6bb38-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6bb38-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6bb38-223">(10)</span><span class="sxs-lookup"><span data-stu-id="6bb38-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-224">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="6bb38-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6bb38-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6bb38-226">(11)</span><span class="sxs-lookup"><span data-stu-id="6bb38-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-227">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="6bb38-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6bb38-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6bb38-229"> (12) </span><span class="sxs-lookup"><span data-stu-id="6bb38-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-230">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="6bb38-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6bb38-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6bb38-232">(13)</span><span class="sxs-lookup"><span data-stu-id="6bb38-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-233">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="6bb38-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6bb38-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6bb38-235">(14)</span><span class="sxs-lookup"><span data-stu-id="6bb38-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-236">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6bb38-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6bb38-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6bb38-238">(15)</span><span class="sxs-lookup"><span data-stu-id="6bb38-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-239">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6bb38-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6bb38-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6bb38-241">(16)</span><span class="sxs-lookup"><span data-stu-id="6bb38-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-242">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="6bb38-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6bb38-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6bb38-244">(17)</span><span class="sxs-lookup"><span data-stu-id="6bb38-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-245">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="6bb38-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6bb38-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6bb38-247">(18)</span><span class="sxs-lookup"><span data-stu-id="6bb38-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-248">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="6bb38-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6bb38-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6bb38-250">(19)</span><span class="sxs-lookup"><span data-stu-id="6bb38-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6bb38-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6bb38-252">(20)</span><span class="sxs-lookup"><span data-stu-id="6bb38-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-253">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="6bb38-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6bb38-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6bb38-255">(21)</span><span class="sxs-lookup"><span data-stu-id="6bb38-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-256">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="6bb38-256">System failure.</span></span> <span data-ttu-id="6bb38-257">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="6bb38-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6bb38-258">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="6bb38-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6bb38-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6bb38-260">(22)</span><span class="sxs-lookup"><span data-stu-id="6bb38-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-261">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="6bb38-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6bb38-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6bb38-263">(23)</span><span class="sxs-lookup"><span data-stu-id="6bb38-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-264">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="6bb38-264">System failure.</span></span> <span data-ttu-id="6bb38-265">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="6bb38-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6bb38-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6bb38-267">(24)</span><span class="sxs-lookup"><span data-stu-id="6bb38-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-268">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="6bb38-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6bb38-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6bb38-270">(25)</span><span class="sxs-lookup"><span data-stu-id="6bb38-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-271">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="6bb38-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6bb38-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6bb38-273">(26)</span><span class="sxs-lookup"><span data-stu-id="6bb38-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-274">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="6bb38-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6bb38-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6bb38-276">(27)</span><span class="sxs-lookup"><span data-stu-id="6bb38-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-277">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="6bb38-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6bb38-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6bb38-279">(28)</span><span class="sxs-lookup"><span data-stu-id="6bb38-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-280">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="6bb38-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6bb38-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6bb38-282">(29)</span><span class="sxs-lookup"><span data-stu-id="6bb38-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-283">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="6bb38-283">Device is disabled.</span></span> <span data-ttu-id="6bb38-284">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="6bb38-284">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6bb38-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6bb38-286">(30)</span><span class="sxs-lookup"><span data-stu-id="6bb38-286">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-287">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="6bb38-287">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6bb38-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="6bb38-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6bb38-289"> (31) </span><span class="sxs-lookup"><span data-stu-id="6bb38-289">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-290">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6bb38-290">Device is not working properly.</span></span> <span data-ttu-id="6bb38-291">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="6bb38-291">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-292">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6bb38-292">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-293">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6bb38-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-294">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-295">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-295">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-296">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="6bb38-296">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6bb38-297">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-298">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="6bb38-298">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-299">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="6bb38-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-301">數據機可以操作的國家或地區。</span><span class="sxs-lookup"><span data-stu-id="6bb38-301">Countries or regions in which the modem can operate.</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-302">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="6bb38-302">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-305">目前正在進行數據機程式設計的國家或地區。</span><span class="sxs-lookup"><span data-stu-id="6bb38-305">Country or region for which the modem is currently programmed.</span></span> <span data-ttu-id="6bb38-306">當支援多個國家或地區時，此屬性會定義目前已選取要使用哪一個。</span><span class="sxs-lookup"><span data-stu-id="6bb38-306">When multiple countries or regions are supported, this property defines which one is currently selected for use.</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6bb38-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-308">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-310">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6bb38-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-311">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bb38-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6bb38-312">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="6bb38-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6bb38-313">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-314">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="6bb38-314">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-315">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="6bb38-315">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-317">目前已定義數據機的密碼。</span><span class="sxs-lookup"><span data-stu-id="6bb38-317">Currently defined passwords for the modem.</span></span> <span data-ttu-id="6bb38-318">基於安全性考慮，此陣列可以保留空白。</span><span class="sxs-lookup"><span data-stu-id="6bb38-318">This array can be left blank for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-319">**說明**</span><span class="sxs-lookup"><span data-stu-id="6bb38-319">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-320">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-322">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-323">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="6bb38-323">Textual description of the object.</span></span>

<span data-ttu-id="6bb38-324">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-324">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-325">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6bb38-325">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-326">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-328">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6bb38-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-329">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="6bb38-329">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6bb38-330">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-331">**DialType**</span><span class="sxs-lookup"><span data-stu-id="6bb38-331">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-332">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6bb38-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-334">使用的撥號類型。</span><span class="sxs-lookup"><span data-stu-id="6bb38-334">Type of dialing that is used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-335">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6bb38-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="6bb38-336">**語氣** (1) </span><span class="sxs-lookup"><span data-stu-id="6bb38-336">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="6bb38-337">**脈衝** (2) </span><span class="sxs-lookup"><span data-stu-id="6bb38-337">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-338">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6bb38-338">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-339">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6bb38-339">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-341">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="6bb38-341">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6bb38-342">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-343">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="6bb38-343">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-344">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6bb38-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-346">數據機的錯誤修正特性。</span><span class="sxs-lookup"><span data-stu-id="6bb38-346">Error correction characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-347">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6bb38-347">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6bb38-348">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6bb38-348">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="6bb38-349">**沒有錯誤更正** (2) </span><span class="sxs-lookup"><span data-stu-id="6bb38-349">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="6bb38-350">**MNP 4** (3) </span><span class="sxs-lookup"><span data-stu-id="6bb38-350">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="6bb38-351">**LAPM** (4) </span><span class="sxs-lookup"><span data-stu-id="6bb38-351">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-352">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6bb38-352">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-353">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-355">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="6bb38-355">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6bb38-356">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-357">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="6bb38-357">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-358">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6bb38-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-360">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「秒」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-361">如果未交換任何資料，則為電話線路自動中斷連線的時間限制 (秒) 。</span><span class="sxs-lookup"><span data-stu-id="6bb38-361">Time limit (in seconds) for automatic disconnection of the phone line if no data is exchanged.</span></span> <span data-ttu-id="6bb38-362">值為 0 (零) 表示此功能存在但未啟用。</span><span class="sxs-lookup"><span data-stu-id="6bb38-362">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-363">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6bb38-363">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-364">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="6bb38-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-366">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="6bb38-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-367">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6bb38-367">Date and time the object was installed.</span></span> <span data-ttu-id="6bb38-368">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="6bb38-368">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6bb38-369">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6bb38-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-371">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6bb38-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-373">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6bb38-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6bb38-374">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-375">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="6bb38-375">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-376">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6bb38-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-378">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-378">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-379">用來存取電話系統的最大可設定通訊速度。</span><span class="sxs-lookup"><span data-stu-id="6bb38-379">Maximum settable communication speed for accessing the phone system.</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-380">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="6bb38-380">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-381">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6bb38-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-383">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-383">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-384">外部數據機的 COM 埠可設定的最大通訊速度。</span><span class="sxs-lookup"><span data-stu-id="6bb38-384">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="6bb38-385">如果不適用，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="6bb38-385">Enter 0 (zero) if not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-386">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="6bb38-386">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-387">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6bb38-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-389">數據機本身中可定義的最大密碼數目。</span><span class="sxs-lookup"><span data-stu-id="6bb38-389">Maximum number of passwords definable in the modem itself.</span></span> <span data-ttu-id="6bb38-390">如果不支援這項功能，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="6bb38-390">If this feature is not supported, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-391">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="6bb38-391">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-392">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6bb38-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-394">數據機的配置。</span><span class="sxs-lookup"><span data-stu-id="6bb38-394">Modulation scheme of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-395">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6bb38-395">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6bb38-396">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6bb38-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6bb38-397">**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="6bb38-397">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="6bb38-398">**鐘 103** (3) </span><span class="sxs-lookup"><span data-stu-id="6bb38-398">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="6bb38-399">**鐘 212A** (4) </span><span class="sxs-lookup"><span data-stu-id="6bb38-399">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="6bb38-400">**V. 22bis** (5) </span><span class="sxs-lookup"><span data-stu-id="6bb38-400">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="6bb38-401">**V. 32** (6) </span><span class="sxs-lookup"><span data-stu-id="6bb38-401">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="6bb38-402">**32bis** (7) </span><span class="sxs-lookup"><span data-stu-id="6bb38-402">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="6bb38-403">**V.** (8) </span><span class="sxs-lookup"><span data-stu-id="6bb38-403">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="6bb38-404">**V. FC** (9) </span><span class="sxs-lookup"><span data-stu-id="6bb38-404">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="6bb38-405">**864** (10) </span><span class="sxs-lookup"><span data-stu-id="6bb38-405">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="6bb38-406">**34bis** (11) </span><span class="sxs-lookup"><span data-stu-id="6bb38-406">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-407">**名稱**</span><span class="sxs-lookup"><span data-stu-id="6bb38-407">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-408">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-410">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-410">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-411">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="6bb38-411">Label by which the object is known.</span></span> <span data-ttu-id="6bb38-412">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="6bb38-412">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6bb38-413">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-414">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6bb38-414">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-417">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-417">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-418">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bb38-418">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="6bb38-419">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6bb38-420">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6bb38-420">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-421">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6bb38-421">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-422">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6bb38-422">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-423">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-424">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="6bb38-424">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6bb38-425">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="6bb38-425">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6bb38-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6bb38-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="6bb38-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6bb38-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="6bb38-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6bb38-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="6bb38-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-430">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="6bb38-430">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6bb38-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="6bb38-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-432">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="6bb38-432">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6bb38-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="6bb38-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-434">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6bb38-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6bb38-435">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="6bb38-435">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="6bb38-436">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-436">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6bb38-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="6bb38-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-438">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="6bb38-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6bb38-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="6bb38-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6bb38-440">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="6bb38-440">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-441">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6bb38-441">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-442">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6bb38-442">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-444">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="6bb38-444">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6bb38-445">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="6bb38-445">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6bb38-446">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="6bb38-446">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6bb38-447">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="6bb38-447">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="6bb38-448">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-449">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="6bb38-449">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-450">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="6bb38-450">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-452">數據機接聽撥入電話之前的響鈴次數。</span><span class="sxs-lookup"><span data-stu-id="6bb38-452">Number of rings before the modem answers an incoming call.</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-453">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="6bb38-453">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-454">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6bb38-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-456">數據機聲音的音量層級。</span><span class="sxs-lookup"><span data-stu-id="6bb38-456">Volume level of the audible tones from the modem.</span></span> <span data-ttu-id="6bb38-457">例如，可以報告 [高]、[中] 或 [低] 卷。</span><span class="sxs-lookup"><span data-stu-id="6bb38-457">For example, high, medium, or low volume can be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-458">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6bb38-458">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6bb38-459">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6bb38-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6bb38-460">**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="6bb38-460">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="6bb38-461">**高** (3) </span><span class="sxs-lookup"><span data-stu-id="6bb38-461">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="6bb38-462">**中型** (4) </span><span class="sxs-lookup"><span data-stu-id="6bb38-462">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="6bb38-463">**低** (5) </span><span class="sxs-lookup"><span data-stu-id="6bb38-463">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="6bb38-464">**Off** (6) </span><span class="sxs-lookup"><span data-stu-id="6bb38-464">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="6bb38-465">**自動** (7) </span><span class="sxs-lookup"><span data-stu-id="6bb38-465">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-466">**狀態**</span><span class="sxs-lookup"><span data-stu-id="6bb38-466">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-467">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-468">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-469">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-469">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-470">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6bb38-470">Current status of the object.</span></span> <span data-ttu-id="6bb38-471">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6bb38-472">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="6bb38-472">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6bb38-473">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6bb38-474">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6bb38-475">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-476">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6bb38-477">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6bb38-478">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6bb38-479">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6bb38-480">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6bb38-481">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6bb38-482">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6bb38-483">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6bb38-484">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="6bb38-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6bb38-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-486">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6bb38-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-488">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="6bb38-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-489">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="6bb38-489">State of the logical device.</span></span> <span data-ttu-id="6bb38-490">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="6bb38-490">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6bb38-491">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6bb38-492">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="6bb38-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6bb38-493">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="6bb38-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6bb38-494">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="6bb38-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6bb38-495">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="6bb38-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6bb38-496">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="6bb38-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6bb38-497">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="6bb38-497">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-498">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6bb38-498">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-499">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-500">若 **為 TRUE**，則表示數據機支援回撥。</span><span class="sxs-lookup"><span data-stu-id="6bb38-500">If **TRUE**, the modem supports call-back.</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-501">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="6bb38-501">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-502">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6bb38-502">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-503">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-504">若為 **TRUE**，則支援同步，以及非同步通訊。</span><span class="sxs-lookup"><span data-stu-id="6bb38-504">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6bb38-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-506">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-508">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6bb38-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-509">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="6bb38-509">Scoping system's creation class name.</span></span>

<span data-ttu-id="6bb38-510">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6bb38-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-512">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6bb38-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-513">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-514">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6bb38-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-515">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="6bb38-515">Scoping system's name.</span></span>

<span data-ttu-id="6bb38-516">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bb38-517">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="6bb38-517">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bb38-518">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="6bb38-518">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6bb38-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6bb38-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6bb38-520">上次重設此控制器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6bb38-520">Date and time this controller was last reset.</span></span> <span data-ttu-id="6bb38-521">這可能表示控制器關閉或重新初始化。</span><span class="sxs-lookup"><span data-stu-id="6bb38-521">This could mean the controller was powered down, or reinitialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bb38-522">備註</span><span class="sxs-lookup"><span data-stu-id="6bb38-522">Remarks</span></span>

<span data-ttu-id="6bb38-523">**Cim \_ POTSModem** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-523">The **CIM\_POTSModem** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6bb38-524">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="6bb38-524">WMI does not implement this class.</span></span> <span data-ttu-id="6bb38-525">針對衍生自 **CIM \_ POTSMODEM** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb38-525">For WMI classes derived from **CIM\_POTSModem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6bb38-526">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="6bb38-526">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6bb38-527">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6bb38-527">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb38-528">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bb38-528">Requirements</span></span>



| <span data-ttu-id="6bb38-529">需求</span><span class="sxs-lookup"><span data-stu-id="6bb38-529">Requirement</span></span> | <span data-ttu-id="6bb38-530">值</span><span class="sxs-lookup"><span data-stu-id="6bb38-530">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb38-531">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb38-531">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb38-532">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6bb38-532">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6bb38-533">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bb38-533">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb38-534">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6bb38-534">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6bb38-535">命名空間</span><span class="sxs-lookup"><span data-stu-id="6bb38-535">Namespace</span></span><br/>                | <span data-ttu-id="6bb38-536">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6bb38-536">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6bb38-537">MOF</span><span class="sxs-lookup"><span data-stu-id="6bb38-537">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bb38-538"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bb38-538"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bb38-539">DLL</span><span class="sxs-lookup"><span data-stu-id="6bb38-539">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bb38-540"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb38-540"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb38-541">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bb38-541">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb38-542">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="6bb38-542">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

