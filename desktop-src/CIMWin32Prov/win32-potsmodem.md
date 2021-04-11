---
description: Win32 \_ POTSMODEM WMI 類別代表在執行 Windows 的電腦系統上， (POTS) 數據機的一般舊電話語音的服務和特性。
ms.assetid: 24589942-e2c3-477e-8179-59ae4a4aa85a
ms.tgt_platform: multiple
title: Win32_POTSModem 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModem
- Win32_POTSModem.Reset
- Win32_POTSModem.SetPowerState
- Win32_POTSModem.AnswerMode
- Win32_POTSModem.AttachedTo
- Win32_POTSModem.Availability
- Win32_POTSModem.BlindOff
- Win32_POTSModem.BlindOn
- Win32_POTSModem.Caption
- Win32_POTSModem.CompatibilityFlags
- Win32_POTSModem.CompressionInfo
- Win32_POTSModem.CompressionOff
- Win32_POTSModem.CompressionOn
- Win32_POTSModem.ConfigManagerErrorCode
- Win32_POTSModem.ConfigManagerUserConfig
- Win32_POTSModem.ConfigurationDialog
- Win32_POTSModem.CountriesSupported
- Win32_POTSModem.CountrySelected
- Win32_POTSModem.CreationClassName
- Win32_POTSModem.CurrentPasswords
- Win32_POTSModem.DCB
- Win32_POTSModem.Default
- Win32_POTSModem.Description
- Win32_POTSModem.DeviceID
- Win32_POTSModem.DeviceLoader
- Win32_POTSModem.DeviceType
- Win32_POTSModem.DialType
- Win32_POTSModem.DriverDate
- Win32_POTSModem.ErrorCleared
- Win32_POTSModem.ErrorControlForced
- Win32_POTSModem.ErrorControlInfo
- Win32_POTSModem.ErrorControlOff
- Win32_POTSModem.ErrorControlOn
- Win32_POTSModem.ErrorDescription
- Win32_POTSModem.FlowControlHard
- Win32_POTSModem.FlowControlOff
- Win32_POTSModem.FlowControlSoft
- Win32_POTSModem.InactivityScale
- Win32_POTSModem.InactivityTimeout
- Win32_POTSModem.Index
- Win32_POTSModem.IndexEx
- Win32_POTSModem.InstallDate
- Win32_POTSModem.LastErrorCode
- Win32_POTSModem.MaxBaudRateToPhone
- Win32_POTSModem.MaxBaudRateToSerialPort
- Win32_POTSModem.MaxNumberOfPasswords
- Win32_POTSModem.Model
- Win32_POTSModem.ModemInfPath
- Win32_POTSModem.ModemInfSection
- Win32_POTSModem.ModulationBell
- Win32_POTSModem.ModulationCCITT
- Win32_POTSModem.ModulationScheme
- Win32_POTSModem.Name
- Win32_POTSModem.PNPDeviceID
- Win32_POTSModem.PortSubClass
- Win32_POTSModem.PowerManagementCapabilities
- Win32_POTSModem.PowerManagementSupported
- Win32_POTSModem.Prefix
- Win32_POTSModem.Properties
- Win32_POTSModem.ProviderName
- Win32_POTSModem.Pulse
- Win32_POTSModem.Reset
- Win32_POTSModem.ResponsesKeyName
- Win32_POTSModem.RingsBeforeAnswer
- Win32_POTSModem.SpeakerModeDial
- Win32_POTSModem.SpeakerModeOff
- Win32_POTSModem.SpeakerModeOn
- Win32_POTSModem.SpeakerModeSetup
- Win32_POTSModem.SpeakerVolumeHigh
- Win32_POTSModem.SpeakerVolumeInfo
- Win32_POTSModem.SpeakerVolumeLow
- Win32_POTSModem.SpeakerVolumeMed
- Win32_POTSModem.Status
- Win32_POTSModem.StatusInfo
- Win32_POTSModem.StringFormat
- Win32_POTSModem.SupportsCallback
- Win32_POTSModem.SupportsSynchronousConnect
- Win32_POTSModem.SystemCreationClassName
- Win32_POTSModem.SystemName
- Win32_POTSModem.Terminator
- Win32_POTSModem.TimeOfLastReset
- Win32_POTSModem.Tone
- Win32_POTSModem.VoiceSwitchFeature
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6ec9634c5ee86d6819bf8f7a45dd521276565903
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847323"
---
# <a name="win32_potsmodem-class"></a><span data-ttu-id="f22cd-103">Win32 \_ POTSModem 類別</span><span class="sxs-lookup"><span data-stu-id="f22cd-103">Win32\_POTSModem class</span></span>

<span data-ttu-id="f22cd-104">**Win32 \_ POTSModem** [WMI 類別](../wmisdk/retrieving-a-class.md)代表在執行 Windows 的電腦系統上， (POTS) 數據機的一般舊電話語音的服務和特性。</span><span class="sxs-lookup"><span data-stu-id="f22cd-104">The **Win32\_POTSModem** [WMI class](../wmisdk/retrieving-a-class.md) represents the services and characteristics of a Plain Old Telephone Service (POTS) modem on a computer system running Windows.</span></span>

<span data-ttu-id="f22cd-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f22cd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f22cd-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="f22cd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f22cd-107">語法</span><span class="sxs-lookup"><span data-stu-id="f22cd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModem : CIM_PotsModem
{
  uint16   AnswerMode;
  string   AttachedTo;
  uint16   Availability;
  string   BlindOff;
  string   BlindOn;
  string   Caption;
  string   CompatibilityFlags;
  uint16   CompressionInfo;
  string   CompressionOff;
  string   CompressionOn;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   ConfigurationDialog;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  uint8    DCB[];
  uint8    Default[];
  string   Description;
  string   DeviceID;
  string   DeviceLoader;
  string   DeviceType;
  uint16   DialType;
  datetime DriverDate;
  boolean  ErrorCleared;
  string   ErrorControlForced;
  uint16   ErrorControlInfo;
  string   ErrorControlOff;
  string   ErrorControlOn;
  string   ErrorDescription;
  string   FlowControlHard;
  string   FlowControlOff;
  string   FlowControlSoft;
  string   InactivityScale;
  uint32   InactivityTimeout;
  uint32   Index;
  string   IndexEx;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  string   Model;
  string   ModemInfPath;
  string   ModemInfSection;
  string   ModulationBell;
  string   ModulationCCITT;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  string   PortSubClass;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Prefix;
  uint8    Properties[];
  string   ProviderName;
  string   Pulse;
  string   Reset;
  string   ResponsesKeyName;
  uint8    RingsBeforeAnswer;
  string   SpeakerModeDial;
  string   SpeakerModeOff;
  string   SpeakerModeOn;
  string   SpeakerModeSetup;
  string   SpeakerVolumeHigh;
  uint16   SpeakerVolumeInfo;
  string   SpeakerVolumeLow;
  string   SpeakerVolumeMed;
  string   Status;
  uint16   StatusInfo;
  string   StringFormat;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  string   Terminator;
  datetime TimeOfLastReset;
  string   Tone;
  string   VoiceSwitchFeature;
};
```

## <a name="members"></a><span data-ttu-id="f22cd-108">成員</span><span class="sxs-lookup"><span data-stu-id="f22cd-108">Members</span></span>

<span data-ttu-id="f22cd-109">**Win32 \_ POTSModem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f22cd-109">The **Win32\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="f22cd-110">方法</span><span class="sxs-lookup"><span data-stu-id="f22cd-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f22cd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f22cd-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f22cd-112">方法</span><span class="sxs-lookup"><span data-stu-id="f22cd-112">Methods</span></span>

<span data-ttu-id="f22cd-113">**Win32 \_ POTSModem** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f22cd-113">The **Win32\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="f22cd-114">方法</span><span class="sxs-lookup"><span data-stu-id="f22cd-114">Method</span></span>            | <span data-ttu-id="f22cd-115">描述</span><span class="sxs-lookup"><span data-stu-id="f22cd-115">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f22cd-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="f22cd-116">**Reset**</span></span>         | <span data-ttu-id="f22cd-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="f22cd-117">Not implemented.</span></span> <span data-ttu-id="f22cd-118">若要執行此方法，請參閱 [**CIM \_ PotsModem**](cim-potsmodem.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="f22cd-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/>                 |
| <span data-ttu-id="f22cd-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f22cd-119">**SetPowerState**</span></span> | <span data-ttu-id="f22cd-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="f22cd-120">Not implemented.</span></span> <span data-ttu-id="f22cd-121">若要執行此方法，請參閱 [**CIM \_ PotsModem**](cim-potsmodem.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="f22cd-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f22cd-122">屬性</span><span class="sxs-lookup"><span data-stu-id="f22cd-122">Properties</span></span>

<span data-ttu-id="f22cd-123">**Win32 \_ POTSModem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f22cd-123">The **Win32\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f22cd-124">**AnswerMode**</span><span class="sxs-lookup"><span data-stu-id="f22cd-124">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f22cd-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-127">數據機目前的自動回應或回呼設定。</span><span class="sxs-lookup"><span data-stu-id="f22cd-127">Current auto-answer or callback setting for the modem.</span></span>

<span data-ttu-id="f22cd-128">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-128">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-129">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f22cd-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f22cd-130">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f22cd-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f22cd-131">**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="f22cd-131">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="f22cd-132">**手動回答** (3) </span><span class="sxs-lookup"><span data-stu-id="f22cd-132">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="f22cd-133">**自動回應** (4) </span><span class="sxs-lookup"><span data-stu-id="f22cd-133">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="f22cd-134">**使用回撥 (5) 的自動解答**</span><span class="sxs-lookup"><span data-stu-id="f22cd-134">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-135">**AttachedTo**</span><span class="sxs-lookup"><span data-stu-id="f22cd-135">**AttachedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-138">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| AttachedTo" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|AttachedTo")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-139">連接至 POTS 數據機的埠。</span><span class="sxs-lookup"><span data-stu-id="f22cd-139">Port to which the POTS modem is attached.</span></span>

<span data-ttu-id="f22cd-140">範例： "COM1"</span><span class="sxs-lookup"><span data-stu-id="f22cd-140">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-141">**可用性**</span><span class="sxs-lookup"><span data-stu-id="f22cd-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-142">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f22cd-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-144">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="f22cd-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-145">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="f22cd-145">Availability and status of the device.</span></span>

<span data-ttu-id="f22cd-146">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f22cd-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f22cd-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="f22cd-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f22cd-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="f22cd-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-150">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="f22cd-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f22cd-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="f22cd-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f22cd-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="f22cd-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f22cd-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="f22cd-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f22cd-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="f22cd-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f22cd-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="f22cd-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f22cd-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="f22cd-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f22cd-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="f22cd-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f22cd-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="f22cd-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f22cd-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="f22cd-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f22cd-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="f22cd-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-161">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="f22cd-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f22cd-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="f22cd-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-163">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="f22cd-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f22cd-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="f22cd-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-165">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="f22cd-165">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f22cd-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="f22cd-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f22cd-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="f22cd-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-168">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="f22cd-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f22cd-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="f22cd-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-170">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="f22cd-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f22cd-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="f22cd-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-172">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="f22cd-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f22cd-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="f22cd-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-174">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="f22cd-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f22cd-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="f22cd-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-176">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="f22cd-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-177">**BlindOff**</span><span class="sxs-lookup"><span data-stu-id="f22cd-177">**BlindOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-180">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| BlindOff" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOff")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-181">用來在撥號之前偵測撥號音的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-181">Command string used to detect a dial tone before dialing.</span></span>

<span data-ttu-id="f22cd-182">範例： "X4"</span><span class="sxs-lookup"><span data-stu-id="f22cd-182">Example: "X4"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-183">**BlindOn**</span><span class="sxs-lookup"><span data-stu-id="f22cd-183">**BlindOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-184">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-186">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| BlindOn" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOn")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-187">用來撥打是否有撥號音的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-187">Command string used to dial whether or not there is a dial tone.</span></span>

<span data-ttu-id="f22cd-188">範例： "X3"</span><span class="sxs-lookup"><span data-stu-id="f22cd-188">Example: "X3"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-189">**標題**</span><span class="sxs-lookup"><span data-stu-id="f22cd-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-192">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-193">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="f22cd-193">Short description of the object.</span></span>

<span data-ttu-id="f22cd-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-195">**CompatibilityFlags**</span><span class="sxs-lookup"><span data-stu-id="f22cd-195">**CompatibilityFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-196">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-198">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| CompatibilityFlags" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|CompatibilityFlags")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-199">與此數據機裝置相容的所有數據機連接通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f22cd-199">All modem connection protocols with which this modem device is compatible.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-200">**CompressionInfo**</span><span class="sxs-lookup"><span data-stu-id="f22cd-200">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-201">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f22cd-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-203">數據機的資料壓縮特性。</span><span class="sxs-lookup"><span data-stu-id="f22cd-203">Data compression characteristics of the modem.</span></span>

<span data-ttu-id="f22cd-204">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-204">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f22cd-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f22cd-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f22cd-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-207">Unknown</span><span class="sxs-lookup"><span data-stu-id="f22cd-207">Unknown</span></span>

</dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="f22cd-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**無壓縮** (2) </span><span class="sxs-lookup"><span data-stu-id="f22cd-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**No Compression** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-209">其他</span><span class="sxs-lookup"><span data-stu-id="f22cd-209">Other</span></span>

</dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="f22cd-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3) </span><span class="sxs-lookup"><span data-stu-id="f22cd-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-211">不壓縮</span><span class="sxs-lookup"><span data-stu-id="f22cd-211">No Compression</span></span>

</dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="f22cd-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**42bis** (4) </span><span class="sxs-lookup"><span data-stu-id="f22cd-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V.42bis** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-213">MNP 5</span><span class="sxs-lookup"><span data-stu-id="f22cd-213">MNP 5</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="f22cd-214"><span id="5"></span>**.5**</span><span class="sxs-lookup"><span data-stu-id="f22cd-214"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-215">V. 42bis</span><span class="sxs-lookup"><span data-stu-id="f22cd-215">V.42bis</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-216">**CompressionOff**</span><span class="sxs-lookup"><span data-stu-id="f22cd-216">**CompressionOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-219">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Compression \_ Off" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-220">用來停用硬體資料壓縮的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-220">Command string used to disable hardware data compression.</span></span>

<span data-ttu-id="f22cd-221">範例： "S46 = 136"</span><span class="sxs-lookup"><span data-stu-id="f22cd-221">Example: "S46=136"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-222">**CompressionOn**</span><span class="sxs-lookup"><span data-stu-id="f22cd-222">**CompressionOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-225">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Compression \_ On" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_On")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-226">用來啟用硬體資料壓縮的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-226">Command string used to enable hardware data compression.</span></span>

<span data-ttu-id="f22cd-227">範例： "S46 = 138"</span><span class="sxs-lookup"><span data-stu-id="f22cd-227">Example: "S46=138"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-228">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f22cd-228">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-229">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22cd-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-231">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-231">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-232">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f22cd-232">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f22cd-233">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-233">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f22cd-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f22cd-235"> (0)</span><span class="sxs-lookup"><span data-stu-id="f22cd-235">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-236">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="f22cd-236">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f22cd-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f22cd-238">(1)</span><span class="sxs-lookup"><span data-stu-id="f22cd-238">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-239">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="f22cd-239">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f22cd-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f22cd-241">(2)</span><span class="sxs-lookup"><span data-stu-id="f22cd-241">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f22cd-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f22cd-243">(3)</span><span class="sxs-lookup"><span data-stu-id="f22cd-243">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-244">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="f22cd-244">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f22cd-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f22cd-246">(4)</span><span class="sxs-lookup"><span data-stu-id="f22cd-246">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-247">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f22cd-247">Device is not working properly.</span></span> <span data-ttu-id="f22cd-248">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="f22cd-248">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f22cd-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f22cd-250">(5)</span><span class="sxs-lookup"><span data-stu-id="f22cd-250">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-251">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="f22cd-251">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f22cd-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f22cd-253">(6)</span><span class="sxs-lookup"><span data-stu-id="f22cd-253">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-254">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="f22cd-254">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f22cd-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f22cd-256">(7)</span><span class="sxs-lookup"><span data-stu-id="f22cd-256">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f22cd-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f22cd-258">(8)</span><span class="sxs-lookup"><span data-stu-id="f22cd-258">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-259">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="f22cd-259">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f22cd-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f22cd-261">(9)</span><span class="sxs-lookup"><span data-stu-id="f22cd-261">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-262">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f22cd-262">Device is not working properly.</span></span> <span data-ttu-id="f22cd-263">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="f22cd-263">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f22cd-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f22cd-265">(10)</span><span class="sxs-lookup"><span data-stu-id="f22cd-265">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-266">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="f22cd-266">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f22cd-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f22cd-268">(11)</span><span class="sxs-lookup"><span data-stu-id="f22cd-268">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-269">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="f22cd-269">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f22cd-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f22cd-271"> (12) </span><span class="sxs-lookup"><span data-stu-id="f22cd-271">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-272">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="f22cd-272">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f22cd-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f22cd-274">(13)</span><span class="sxs-lookup"><span data-stu-id="f22cd-274">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-275">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="f22cd-275">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f22cd-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f22cd-277">(14)</span><span class="sxs-lookup"><span data-stu-id="f22cd-277">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-278">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f22cd-278">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f22cd-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f22cd-280">(15)</span><span class="sxs-lookup"><span data-stu-id="f22cd-280">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-281">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f22cd-281">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f22cd-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f22cd-283">(16)</span><span class="sxs-lookup"><span data-stu-id="f22cd-283">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-284">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="f22cd-284">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f22cd-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f22cd-286">(17)</span><span class="sxs-lookup"><span data-stu-id="f22cd-286">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-287">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f22cd-287">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f22cd-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f22cd-289">(18)</span><span class="sxs-lookup"><span data-stu-id="f22cd-289">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-290">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f22cd-290">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f22cd-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f22cd-292">(19)</span><span class="sxs-lookup"><span data-stu-id="f22cd-292">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f22cd-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f22cd-294">(20)</span><span class="sxs-lookup"><span data-stu-id="f22cd-294">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-295">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="f22cd-295">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f22cd-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f22cd-297">(21)</span><span class="sxs-lookup"><span data-stu-id="f22cd-297">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-298">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="f22cd-298">System failure.</span></span> <span data-ttu-id="f22cd-299">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="f22cd-299">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f22cd-300">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="f22cd-300">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f22cd-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f22cd-302">(22)</span><span class="sxs-lookup"><span data-stu-id="f22cd-302">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-303">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="f22cd-303">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f22cd-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f22cd-305">(23)</span><span class="sxs-lookup"><span data-stu-id="f22cd-305">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-306">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="f22cd-306">System failure.</span></span> <span data-ttu-id="f22cd-307">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="f22cd-307">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f22cd-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f22cd-309">(24)</span><span class="sxs-lookup"><span data-stu-id="f22cd-309">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-310">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f22cd-310">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f22cd-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f22cd-312">(25)</span><span class="sxs-lookup"><span data-stu-id="f22cd-312">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-313">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="f22cd-313">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f22cd-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f22cd-315">(26)</span><span class="sxs-lookup"><span data-stu-id="f22cd-315">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-316">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="f22cd-316">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f22cd-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f22cd-318">(27)</span><span class="sxs-lookup"><span data-stu-id="f22cd-318">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-319">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="f22cd-319">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f22cd-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f22cd-321">(28)</span><span class="sxs-lookup"><span data-stu-id="f22cd-321">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-322">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f22cd-322">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f22cd-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f22cd-324">(29)</span><span class="sxs-lookup"><span data-stu-id="f22cd-324">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-325">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="f22cd-325">Device is disabled.</span></span> <span data-ttu-id="f22cd-326">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="f22cd-326">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f22cd-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f22cd-328">(30)</span><span class="sxs-lookup"><span data-stu-id="f22cd-328">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-329">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="f22cd-329">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f22cd-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="f22cd-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f22cd-331"> (31) </span><span class="sxs-lookup"><span data-stu-id="f22cd-331">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-332">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="f22cd-332">Device is not working properly.</span></span> <span data-ttu-id="f22cd-333">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="f22cd-333">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-334">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f22cd-334">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-335">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f22cd-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-337">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-337">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-338">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="f22cd-338">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f22cd-339">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-340">**組態] 對話方塊**</span><span class="sxs-lookup"><span data-stu-id="f22cd-340">**ConfigurationDialog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-341">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-343">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ConfigDialog" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ConfigDialog")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-344">數據機初始化字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-344">Modem initialization string.</span></span> <span data-ttu-id="f22cd-345">這個屬性是由這個類別之其他屬性的命令字串所組成。</span><span class="sxs-lookup"><span data-stu-id="f22cd-345">This property is made up of command strings from other properties of this class.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-346">**CountriesSupported**</span><span class="sxs-lookup"><span data-stu-id="f22cd-346">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-347">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f22cd-347">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-349">數據機可以操作的國家/地區的陣列。</span><span class="sxs-lookup"><span data-stu-id="f22cd-349">Array of countries/regions in which the modem can operate.</span></span>

<span data-ttu-id="f22cd-350">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-350">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-351">**CountrySelected**</span><span class="sxs-lookup"><span data-stu-id="f22cd-351">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-354">數據機目前進行程式設計的國家/地區。</span><span class="sxs-lookup"><span data-stu-id="f22cd-354">Country/region for which the modem is currently programmed.</span></span> <span data-ttu-id="f22cd-355">當支援多個國家/地區時，此屬性會定義目前已選取要使用哪一個。</span><span class="sxs-lookup"><span data-stu-id="f22cd-355">When multiple countries/regions are supported, this property defines which one is currently selected for use.</span></span>

<span data-ttu-id="f22cd-356">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-356">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-357">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f22cd-357">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-358">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-360">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f22cd-360">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-361">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="f22cd-361">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="f22cd-362">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="f22cd-362">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f22cd-363">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-364">**CurrentPasswords**</span><span class="sxs-lookup"><span data-stu-id="f22cd-364">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-365">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="f22cd-365">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-366">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-367">目前定義的數據機密碼清單。</span><span class="sxs-lookup"><span data-stu-id="f22cd-367">List of currently defined passwords for the modem.</span></span> <span data-ttu-id="f22cd-368">基於安全性考慮，此陣列可能會保留空白。</span><span class="sxs-lookup"><span data-stu-id="f22cd-368">This array may be left blank for security reasons.</span></span>

<span data-ttu-id="f22cd-369">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-369">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-370">**DCB**</span><span class="sxs-lookup"><span data-stu-id="f22cd-370">**DCB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-371">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="f22cd-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-373">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-373">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-374">串列通訊裝置的控制設定，在此案例中為數據機裝置。</span><span class="sxs-lookup"><span data-stu-id="f22cd-374">Control settings for a serial communications device, in this case, the modem device.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-375">**預設值**</span><span class="sxs-lookup"><span data-stu-id="f22cd-375">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-376">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="f22cd-376">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-378">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Default" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Default")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-379">若 **為 TRUE**，則在執行 Windows 的電腦系統上，此 POTS 數據機是預設的數據機。</span><span class="sxs-lookup"><span data-stu-id="f22cd-379">If **TRUE**, this POTS modem is the default modem on the computer system running Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-380">**說明**</span><span class="sxs-lookup"><span data-stu-id="f22cd-380">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-383">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-383">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-384">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f22cd-384">Description of the object.</span></span>

<span data-ttu-id="f22cd-385">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-386">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f22cd-386">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-387">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-389">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-389">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-390">此 POTS 數據機與系統上其他裝置的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="f22cd-390">Unique identifier of this POTS modem from other devices on the system.</span></span>

<span data-ttu-id="f22cd-391">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-392">**DeviceLoader**</span><span class="sxs-lookup"><span data-stu-id="f22cd-392">**DeviceLoader**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-393">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-395">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DevLoader" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DevLoader")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-396">數據機的裝置載入器名稱。</span><span class="sxs-lookup"><span data-stu-id="f22cd-396">Name of the device loader for the modem.</span></span> <span data-ttu-id="f22cd-397">裝置載入器會載入並管理指定裝置的設備磁碟機和枚舉器。</span><span class="sxs-lookup"><span data-stu-id="f22cd-397">A device loader loads and manages device drivers and enumerators for a given device.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-398">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="f22cd-398">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-399">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-401">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DeviceType" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DeviceType")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-402">數據機的實體類型。</span><span class="sxs-lookup"><span data-stu-id="f22cd-402">Physical type of the modem.</span></span>

<span data-ttu-id="f22cd-403">值如下：</span><span class="sxs-lookup"><span data-stu-id="f22cd-403">The values are:</span></span>

<dl> <dd><span data-ttu-id="f22cd-404">「Null 數據機」</span><span class="sxs-lookup"><span data-stu-id="f22cd-404">"Null Modem"</span></span></dd> <dd><span data-ttu-id="f22cd-405">「內接式數據機」</span><span class="sxs-lookup"><span data-stu-id="f22cd-405">"Internal Modem"</span></span></dd> <dd><span data-ttu-id="f22cd-406">「外部數據機」</span><span class="sxs-lookup"><span data-stu-id="f22cd-406">"External Modem"</span></span></dd> <dd><span data-ttu-id="f22cd-407">「PCMCIA 數據機」</span><span class="sxs-lookup"><span data-stu-id="f22cd-407">"PCMCIA Modem"</span></span></dd> <dd><span data-ttu-id="f22cd-408">不明</span><span class="sxs-lookup"><span data-stu-id="f22cd-408">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Null_Modem"></span><span id="null_modem"></span><span id="NULL_MODEM"></span>

<span data-ttu-id="f22cd-409">**Null 數據機** ( 「Null 數據機」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-409">**Null Modem** ("Null Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Modem"></span><span id="internal_modem"></span><span id="INTERNAL_MODEM"></span>

<span data-ttu-id="f22cd-410">**內接式數據機** ( 「內接式數據機」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-410">**Internal Modem** ("Internal Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="External_Modem"></span><span id="external_modem"></span><span id="EXTERNAL_MODEM"></span>

<span data-ttu-id="f22cd-411">**外部數據機** ( 「外部數據機」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-411">**External Modem** ("External Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Modem"></span><span id="pcmcia_modem"></span><span id="PCMCIA_MODEM"></span>

<span data-ttu-id="f22cd-412"> ( 「PCMCIA 數據機」的 **Pcmcia 數據機**) </span><span class="sxs-lookup"><span data-stu-id="f22cd-412">**PCMCIA Modem** ("PCMCIA Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-413">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-413">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-414">**DialType**</span><span class="sxs-lookup"><span data-stu-id="f22cd-414">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-415">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f22cd-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-417">使用的撥號方法類型。</span><span class="sxs-lookup"><span data-stu-id="f22cd-417">Type of dialing method used.</span></span>

<span data-ttu-id="f22cd-418">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-418">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-419">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f22cd-419">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="f22cd-420">**語氣** (1) </span><span class="sxs-lookup"><span data-stu-id="f22cd-420">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="f22cd-421">**脈衝** (2) </span><span class="sxs-lookup"><span data-stu-id="f22cd-421">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-422">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="f22cd-422">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-423">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f22cd-423">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-425">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| DriverDate" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-426">數據機驅動程式的日期。</span><span class="sxs-lookup"><span data-stu-id="f22cd-426">Date of the modem driver.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-427">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f22cd-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-428">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f22cd-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-430">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="f22cd-430">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="f22cd-431">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-432">**ErrorControlForced**</span><span class="sxs-lookup"><span data-stu-id="f22cd-432">**ErrorControlForced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-433">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-435">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ 強制" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Forced")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-436">在建立連接時，用來啟用錯誤修正控制項的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-436">Command string used to enable error correction control when establishing a connection.</span></span> <span data-ttu-id="f22cd-437">這會增加連接的可靠性。</span><span class="sxs-lookup"><span data-stu-id="f22cd-437">This increases the reliability of the connection.</span></span>

<span data-ttu-id="f22cd-438">範例： "+ Q5S36 = 4S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="f22cd-438">Example: "+Q5S36=4S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-439">**ErrorControlInfo**</span><span class="sxs-lookup"><span data-stu-id="f22cd-439">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-440">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f22cd-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-442">數據機的錯誤修正特性。</span><span class="sxs-lookup"><span data-stu-id="f22cd-442">Error correction characteristics of the modem.</span></span>

<span data-ttu-id="f22cd-443">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-443">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-444">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f22cd-444">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f22cd-445">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f22cd-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="f22cd-446">**沒有錯誤更正** (2) </span><span class="sxs-lookup"><span data-stu-id="f22cd-446">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="f22cd-447">**MNP 4** (3) </span><span class="sxs-lookup"><span data-stu-id="f22cd-447">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="f22cd-448">**LAPM** (4) </span><span class="sxs-lookup"><span data-stu-id="f22cd-448">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-449">**ErrorControlOff**</span><span class="sxs-lookup"><span data-stu-id="f22cd-449">**ErrorControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-450">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-452">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ Off" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-453">用來停用錯誤控制的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-453">Command string used to disable error control.</span></span>

<span data-ttu-id="f22cd-454">範例： "+ Q6S36 = 3S48 = 128"</span><span class="sxs-lookup"><span data-stu-id="f22cd-454">Example: "+Q6S36=3S48=128"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-455">**ErrorControlOn**</span><span class="sxs-lookup"><span data-stu-id="f22cd-455">**ErrorControlOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-456">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-457">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-458">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ On" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_On")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-459">用來啟用錯誤控制的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-459">Command string used to enable error control.</span></span>

<span data-ttu-id="f22cd-460">範例： "+ Q5S36 = 7S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="f22cd-460">Example: "+Q5S36=7S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-461">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f22cd-461">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-462">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-463">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-464">有關 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f22cd-464">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="f22cd-465">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-466">**FlowControlHard**</span><span class="sxs-lookup"><span data-stu-id="f22cd-466">**FlowControlHard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-467">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-468">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-469">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ Hard" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-469">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Hard")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-470">用來啟用硬體流量控制的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-470">Command string used to enable hardware flow control.</span></span> <span data-ttu-id="f22cd-471">流量控制是由電腦之間傳送的信號所組成，確認兩部電腦都已準備好傳輸或接收資料。</span><span class="sxs-lookup"><span data-stu-id="f22cd-471">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="f22cd-472">範例： "&版 k1"</span><span class="sxs-lookup"><span data-stu-id="f22cd-472">Example: "&K1"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-473">**FlowControlOff**</span><span class="sxs-lookup"><span data-stu-id="f22cd-473">**FlowControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-474">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-476">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ Off" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-477">用來停用流程式控制制的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-477">Command string used to disable flow control.</span></span> <span data-ttu-id="f22cd-478">流量控制是由電腦之間傳送的信號所組成，確認兩部電腦都已準備好傳輸或接收資料。</span><span class="sxs-lookup"><span data-stu-id="f22cd-478">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="f22cd-479">範例： "&K0"</span><span class="sxs-lookup"><span data-stu-id="f22cd-479">Example: "&K0"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-480">**FlowControlSoft**</span><span class="sxs-lookup"><span data-stu-id="f22cd-480">**FlowControlSoft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-483">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| FlowControl \_ Soft" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-483">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Soft")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-484">用來啟用軟體流程式控制制的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-484">Command string used to enable software flow control.</span></span> <span data-ttu-id="f22cd-485">流量控制是由電腦之間傳送的信號所組成，確認兩部電腦都已準備好傳輸或接收資料。</span><span class="sxs-lookup"><span data-stu-id="f22cd-485">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="f22cd-486">範例：「&的 K2」</span><span class="sxs-lookup"><span data-stu-id="f22cd-486">Example: "&K2"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-487">**InactivityScale**</span><span class="sxs-lookup"><span data-stu-id="f22cd-487">**InactivityScale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-488">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-488">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-489">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-490">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InactivityScale" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InactivityScale")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-491">與 **InactivityTimeout** 屬性搭配使用的乘數，用來計算連接的超時時間。</span><span class="sxs-lookup"><span data-stu-id="f22cd-491">Multiplier used with the **InactivityTimeout** property to calculate the timeout period of a connection.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-492">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="f22cd-492">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-493">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22cd-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-494">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-495">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「秒」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-496">如果未交換任何資料，則為電話線路自動中斷連接的時間限制 (秒) 。</span><span class="sxs-lookup"><span data-stu-id="f22cd-496">Time limit (in seconds) for automatic disconnection of the phone line, if no data is exchanged.</span></span> <span data-ttu-id="f22cd-497">值為 0 (零) 表示此功能存在但未啟用。</span><span class="sxs-lookup"><span data-stu-id="f22cd-497">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

<span data-ttu-id="f22cd-498">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-498">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-499">**Index**</span><span class="sxs-lookup"><span data-stu-id="f22cd-499">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-500">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22cd-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-501">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-502">此 POTS 數據機的索引編號。</span><span class="sxs-lookup"><span data-stu-id="f22cd-502">Index number for this POTS modem.</span></span>

<span data-ttu-id="f22cd-503">範例：0</span><span class="sxs-lookup"><span data-stu-id="f22cd-503">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-504">**IndexEx**</span><span class="sxs-lookup"><span data-stu-id="f22cd-504">**IndexEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-505">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-506">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-507">此 POTS 數據機的裝置實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="f22cd-507">The device instance ID for this POTS modem.</span></span>

<span data-ttu-id="f22cd-508">範例： "1&08"</span><span class="sxs-lookup"><span data-stu-id="f22cd-508">Example: "1&08"</span></span>

<span data-ttu-id="f22cd-509">**Windows server 2012 R2、Windows 8.1、Windows server 2012、Windows 8、Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** 從 Windows Server 2016 和 Windows 10 開始，可以使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="f22cd-509">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is available beginning with Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f22cd-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-511">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f22cd-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-512">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-513">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="f22cd-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-514">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f22cd-514">Date and time the object was installed.</span></span> <span data-ttu-id="f22cd-515">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="f22cd-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f22cd-516">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-517">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f22cd-517">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-518">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22cd-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-520">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f22cd-520">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f22cd-521">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-522">**MaxBaudRateToPhone**</span><span class="sxs-lookup"><span data-stu-id="f22cd-522">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-523">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22cd-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-525">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-525">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-526">用來存取電話系統的最大可設定通訊速度。</span><span class="sxs-lookup"><span data-stu-id="f22cd-526">Maximum settable communication speed for accessing the phone system.</span></span>

<span data-ttu-id="f22cd-527">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-527">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-528">**MaxBaudRateToSerialPort**</span><span class="sxs-lookup"><span data-stu-id="f22cd-528">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-529">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f22cd-529">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-530">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-531">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-531">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-532">外部數據機的 COM 埠可設定的最大通訊速度。</span><span class="sxs-lookup"><span data-stu-id="f22cd-532">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="f22cd-533">如果不適用，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f22cd-533">Enter 0 (zero) if not applicable.</span></span>

<span data-ttu-id="f22cd-534">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-534">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-535">**MaxNumberOfPasswords**</span><span class="sxs-lookup"><span data-stu-id="f22cd-535">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-536">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f22cd-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-537">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-538">數據機本身中可定義的密碼數目。</span><span class="sxs-lookup"><span data-stu-id="f22cd-538">Number of passwords definable in the modem itself.</span></span> <span data-ttu-id="f22cd-539">如果不支援這項功能，請輸入 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="f22cd-539">If this feature is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="f22cd-540">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-540">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-541">**型號**</span><span class="sxs-lookup"><span data-stu-id="f22cd-541">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-542">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-543">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-544">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Model" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-544">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Model")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-545">此 POTS 數據機的型號。</span><span class="sxs-lookup"><span data-stu-id="f22cd-545">Model of this POTS modem.</span></span>

<span data-ttu-id="f22cd-546">範例： "Sportster 56K External"</span><span class="sxs-lookup"><span data-stu-id="f22cd-546">Example: "Sportster 56K External"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-547">**ModemInfPath**</span><span class="sxs-lookup"><span data-stu-id="f22cd-547">**ModemInfPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-548">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-549">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-550">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfPath" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-550">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-551">此數據機 .inf 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="f22cd-551">Path to this modem's .inf file.</span></span> <span data-ttu-id="f22cd-552">此檔案包含數據機和其驅動程式的初始化資訊。</span><span class="sxs-lookup"><span data-stu-id="f22cd-552">This file contains initialization information for the modem and its driver.</span></span>

<span data-ttu-id="f22cd-553">範例： "C： \\ Windows \\ INF"</span><span class="sxs-lookup"><span data-stu-id="f22cd-553">Example: "C:\\Windows\\INF"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-554">**ModemInfSection**</span><span class="sxs-lookup"><span data-stu-id="f22cd-554">**ModemInfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-555">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-555">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-556">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-556">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-557">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfSection" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-557">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-558">數據機 .inf 檔案中的區段名稱，其中包含數據機的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f22cd-558">Name of the section in the modem's .inf file that contains information about the modem.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-559">**ModulationBell**</span><span class="sxs-lookup"><span data-stu-id="f22cd-559">**ModulationBell**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-560">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-561">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-562">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| 調幅 \_ 鐘" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-562">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_Bell")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-563">用來指示數據機將鐘 modulations 用於300和 1200 bps 的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-563">Command string used to instruct the modem to use Bell modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="f22cd-564">範例： "B1"</span><span class="sxs-lookup"><span data-stu-id="f22cd-564">Example: "B1"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-565">**ModulationCCITT**</span><span class="sxs-lookup"><span data-stu-id="f22cd-565">**ModulationCCITT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-566">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-567">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-568">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| \* \_ CCITT" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-568">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_CCITT")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-569">用來指示數據機將 CCITT modulations 用於300和 1200 bps 的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-569">Command string used to instruct the modem to use CCITT modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="f22cd-570">範例： "B0"</span><span class="sxs-lookup"><span data-stu-id="f22cd-570">Example: "B0"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-571">**ModulationScheme**</span><span class="sxs-lookup"><span data-stu-id="f22cd-571">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-572">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f22cd-572">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-573">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-574">數據機的配置。</span><span class="sxs-lookup"><span data-stu-id="f22cd-574">Modulation scheme of the modem.</span></span>

<span data-ttu-id="f22cd-575">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-575">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-576">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f22cd-576">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f22cd-577">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f22cd-577">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f22cd-578">**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="f22cd-578">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="f22cd-579">**鐘 103** (3) </span><span class="sxs-lookup"><span data-stu-id="f22cd-579">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="f22cd-580">**鐘 212A** (4) </span><span class="sxs-lookup"><span data-stu-id="f22cd-580">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="f22cd-581">**V. 22bis** (5) </span><span class="sxs-lookup"><span data-stu-id="f22cd-581">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="f22cd-582">**V. 32** (6) </span><span class="sxs-lookup"><span data-stu-id="f22cd-582">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="f22cd-583">**32bis** (7) </span><span class="sxs-lookup"><span data-stu-id="f22cd-583">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="f22cd-584">**V.** (8) </span><span class="sxs-lookup"><span data-stu-id="f22cd-584">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="f22cd-585">**V. FC** (9) </span><span class="sxs-lookup"><span data-stu-id="f22cd-585">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="f22cd-586">**864** (10) </span><span class="sxs-lookup"><span data-stu-id="f22cd-586">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="f22cd-587">**34bis** (11) </span><span class="sxs-lookup"><span data-stu-id="f22cd-587">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-588">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f22cd-588">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-589">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-590">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-591">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-591">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-592">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="f22cd-592">Label by which the object is known.</span></span> <span data-ttu-id="f22cd-593">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="f22cd-593">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="f22cd-594">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-594">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-595">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f22cd-595">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-596">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-596">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-597">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-597">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-598">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-598">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-599">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f22cd-599">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f22cd-600">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-600">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f22cd-601">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f22cd-601">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-602">**PortSubClass**</span><span class="sxs-lookup"><span data-stu-id="f22cd-602">**PortSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-603">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-604">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-604">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-605">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| PortSubClass" ) ， **Value** ( "Parallel port"，"序列埠"，"數據機" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-605">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|PortSubClass"), **Value** ("Parallel Port", "Serial Port", "Modem")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-606">用於此數據機的埠定義。</span><span class="sxs-lookup"><span data-stu-id="f22cd-606">Definition of the port used for this modem.</span></span>

<dt>



 <span data-ttu-id="f22cd-607"> ( "00" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-607">("00")</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-608">平行埠</span><span class="sxs-lookup"><span data-stu-id="f22cd-608">Parallel Port</span></span>

</dd> <dt>



 <span data-ttu-id="f22cd-609"> ( "01" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-609">("01")</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-610">序列埠</span><span class="sxs-lookup"><span data-stu-id="f22cd-610">Serial Port</span></span>

</dd> <dt>



 <span data-ttu-id="f22cd-611"> ( "02" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-611">("02")</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-612">數據機</span><span class="sxs-lookup"><span data-stu-id="f22cd-612">Modem</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-613">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f22cd-613">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-614">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="f22cd-614">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-615">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-615">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-616">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="f22cd-616">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="f22cd-617">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="f22cd-617">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f22cd-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f22cd-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="f22cd-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f22cd-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="f22cd-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f22cd-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="f22cd-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-622">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="f22cd-622">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f22cd-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="f22cd-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-624">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="f22cd-624">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f22cd-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="f22cd-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-626">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f22cd-626">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="f22cd-627">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="f22cd-627">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="f22cd-628">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-628">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f22cd-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="f22cd-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-630">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="f22cd-630">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f22cd-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="f22cd-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f22cd-632">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="f22cd-632">Timed Power-On Supported</span></span>

<span data-ttu-id="f22cd-633">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="f22cd-633">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-634">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f22cd-634">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-635">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f22cd-635">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-636">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-636">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-637">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="f22cd-637">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="f22cd-638">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="f22cd-638">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="f22cd-639">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-640">**Prefix**</span><span class="sxs-lookup"><span data-stu-id="f22cd-640">**Prefix**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-641">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-642">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-643">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Prefix" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Prefix")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-644">用來存取外接行的撥號首碼。</span><span class="sxs-lookup"><span data-stu-id="f22cd-644">Dialing prefix used to access an outside line.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-645">**屬性**</span><span class="sxs-lookup"><span data-stu-id="f22cd-645">**Properties**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-646">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="f22cd-646">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-647">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-648">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Properties" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-648">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Properties")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-649">此數據機) 的所有屬性 (及其值的清單。</span><span class="sxs-lookup"><span data-stu-id="f22cd-649">List of all the properties (and their values) for this modem.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-650">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="f22cd-650">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-651">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-652">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-653">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ProviderName" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-653">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ProviderName")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-654">提供數據機服務之電腦的網路路徑。</span><span class="sxs-lookup"><span data-stu-id="f22cd-654">Network path to the computer that provides the modem services.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-655">**脈衝**</span><span class="sxs-lookup"><span data-stu-id="f22cd-655">**Pulse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-656">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-656">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-657">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-657">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-658">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| 脈衝" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-658">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Pulse")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-659">用來指示數據機使用脈衝模式進行撥號的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-659">Command string used to instruct the modem to use pulse mode for dialing.</span></span> <span data-ttu-id="f22cd-660">對無法處理按鍵撥號的電話線路而言，必須要有撥盤式撥號。</span><span class="sxs-lookup"><span data-stu-id="f22cd-660">Pulse dialing is necessary for phone lines that are unable to handle tone dialing.</span></span>

<span data-ttu-id="f22cd-661">範例： "P"</span><span class="sxs-lookup"><span data-stu-id="f22cd-661">Example: "P"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-662">**重設**</span><span class="sxs-lookup"><span data-stu-id="f22cd-662">**Reset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-663">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-663">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-664">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-664">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-665">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) (重設) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Reset" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-665">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Reset")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-666">用來重設數據機以進行下一個呼叫的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-666">Command string used to reset the modem for the next call.</span></span>

<span data-ttu-id="f22cd-667">範例： "AT&F"</span><span class="sxs-lookup"><span data-stu-id="f22cd-667">Example: "AT&F"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-668">**ResponsesKeyName**</span><span class="sxs-lookup"><span data-stu-id="f22cd-668">**ResponsesKeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-669">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-669">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-670">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-670">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-671">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ResponsesKeyName" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-671">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ResponsesKeyName")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-672">回應此數據機可能會在連接過程中向作業系統報告。</span><span class="sxs-lookup"><span data-stu-id="f22cd-672">Response this modem might report to the operating system during the connection process.</span></span> <span data-ttu-id="f22cd-673">前兩個字元會指定回應的類型。</span><span class="sxs-lookup"><span data-stu-id="f22cd-673">The first two characters specify the type of response.</span></span> <span data-ttu-id="f22cd-674">第二個字元會指定所進行連接的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f22cd-674">The second two characters specify information about the connection being made.</span></span> <span data-ttu-id="f22cd-675">第二個字元僅用於協調進度或連接回應碼。</span><span class="sxs-lookup"><span data-stu-id="f22cd-675">The second two characters are used only for Negotiation Progress or Connect response codes.</span></span> <span data-ttu-id="f22cd-676">接下來八個字元會指定以每秒位元組數 (bps) 來協商的數據機到數據機線路速度。</span><span class="sxs-lookup"><span data-stu-id="f22cd-676">The next eight characters specify the modem-to-modem line speed negotiated in bits per second (bps).</span></span> <span data-ttu-id="f22cd-677">字元代表32位不帶正負號的長整數格式， (位元組和字組反轉) 。</span><span class="sxs-lookup"><span data-stu-id="f22cd-677">The characters represent a 32-bit unsigned long integer format (byte and word reversed).</span></span> <span data-ttu-id="f22cd-678">最後八個字元表示數據機正在變更為不同的埠或資料終端設備 (DTE) 速度。</span><span class="sxs-lookup"><span data-stu-id="f22cd-678">The last eight characters indicate that the modem is changing to a different port or Data Terminal Equipment (DTE) speed.</span></span> <span data-ttu-id="f22cd-679">通常不會使用此欄位，因為數據機會以鎖定的埠速度建立連線，而不論數據機對數據機或資料通訊設備 (DCE) 速度。</span><span class="sxs-lookup"><span data-stu-id="f22cd-679">Usually this field is not used because modems make connections at a locked port speed regardless of the modem-to-modem or Data Communications Equipment (DCE) speed.</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-680">**RingsBeforeAnswer**</span><span class="sxs-lookup"><span data-stu-id="f22cd-680">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-681">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="f22cd-681">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-682">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-682">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-683">數據機接聽撥入電話之前的響鈴次數。</span><span class="sxs-lookup"><span data-stu-id="f22cd-683">Number of rings before the modem answers an incoming call.</span></span>

<span data-ttu-id="f22cd-684">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-684">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-685">**SpeakerModeDial**</span><span class="sxs-lookup"><span data-stu-id="f22cd-685">**SpeakerModeDial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-686">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-687">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-688">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeDial" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-688">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeDial")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-689">用來在撥號數位之後開啟數據機喇叭的命令字串，並在建立連線時關閉喇叭。</span><span class="sxs-lookup"><span data-stu-id="f22cd-689">Command string used to turn the modem speaker on after dialing a number, and turning the speaker off when a connection has been established.</span></span>

<span data-ttu-id="f22cd-690">範例： "M1"</span><span class="sxs-lookup"><span data-stu-id="f22cd-690">Example: "M1"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-691">**SpeakerModeOff**</span><span class="sxs-lookup"><span data-stu-id="f22cd-691">**SpeakerModeOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-692">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-693">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-693">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-694">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeOff" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-694">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOff")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-695">用來關閉數據機喇叭的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-695">Command string used to turn the modem speaker off.</span></span>

<span data-ttu-id="f22cd-696">範例： "M0"</span><span class="sxs-lookup"><span data-stu-id="f22cd-696">Example: "M0"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-697">**SpeakerModeOn**</span><span class="sxs-lookup"><span data-stu-id="f22cd-697">**SpeakerModeOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-698">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-699">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-700">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeOn" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-700">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOn")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-701">用來開啟數據機喇叭的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-701">Command string used to turn the modem speaker on.</span></span>

<span data-ttu-id="f22cd-702">範例： "M2"</span><span class="sxs-lookup"><span data-stu-id="f22cd-702">Example: "M2"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-703">**SpeakerModeSetup**</span><span class="sxs-lookup"><span data-stu-id="f22cd-703">**SpeakerModeSetup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-704">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-705">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-705">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-706">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerModeSetup" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-706">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeSetup")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-707">用來指示數據機在 (上開啟喇叭的命令字串，直到建立) 的連線為止。</span><span class="sxs-lookup"><span data-stu-id="f22cd-707">Command string used to instruct the modem to turn the speaker on (until a connection is established).</span></span>

<span data-ttu-id="f22cd-708">範例： "M3"</span><span class="sxs-lookup"><span data-stu-id="f22cd-708">Example: "M3"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-709">**SpeakerVolumeHigh**</span><span class="sxs-lookup"><span data-stu-id="f22cd-709">**SpeakerVolumeHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-710">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-711">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-711">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-712">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerVolume \_ High" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-712">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_High")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-713">用來將數據機喇叭設定為最高音量的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-713">Command string used to set the modem speaker to the highest volume.</span></span>

<span data-ttu-id="f22cd-714">範例： "L3"</span><span class="sxs-lookup"><span data-stu-id="f22cd-714">Example: "L3"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-715">**SpeakerVolumeInfo**</span><span class="sxs-lookup"><span data-stu-id="f22cd-715">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-716">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f22cd-716">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-717">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-717">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-718">說明數據機聲音的音量層級。</span><span class="sxs-lookup"><span data-stu-id="f22cd-718">Describes the volume level of the audible tones from the modem.</span></span>

<span data-ttu-id="f22cd-719">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-719">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-720">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="f22cd-720">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f22cd-721">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f22cd-721">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f22cd-722">**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="f22cd-722">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="f22cd-723">**高** (3) </span><span class="sxs-lookup"><span data-stu-id="f22cd-723">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="f22cd-724">**中型** (4) </span><span class="sxs-lookup"><span data-stu-id="f22cd-724">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="f22cd-725">**低** (5) </span><span class="sxs-lookup"><span data-stu-id="f22cd-725">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="f22cd-726">**Off** (6) </span><span class="sxs-lookup"><span data-stu-id="f22cd-726">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="f22cd-727">**自動** (7) </span><span class="sxs-lookup"><span data-stu-id="f22cd-727">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-728">**SpeakerVolumeLow**</span><span class="sxs-lookup"><span data-stu-id="f22cd-728">**SpeakerVolumeLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-729">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-729">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-730">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-730">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-731">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerVolume \_ Low" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-731">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Low")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-732">用來將數據機喇叭設定為最小磁片區的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-732">Command string used to set the modem speaker to the lowest volume.</span></span>

<span data-ttu-id="f22cd-733">範例： "L1"</span><span class="sxs-lookup"><span data-stu-id="f22cd-733">Example: "L1"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-734">**SpeakerVolumeMed**</span><span class="sxs-lookup"><span data-stu-id="f22cd-734">**SpeakerVolumeMed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-735">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-735">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-736">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-736">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-737">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| SpeakerVolume \_ med-v" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-737">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Med")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-738">用來將數據機喇叭設定為媒體音量的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-738">Command string used to set the modem speaker to a medium volume.</span></span>

<span data-ttu-id="f22cd-739">範例： "L2"</span><span class="sxs-lookup"><span data-stu-id="f22cd-739">Example: "L2"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-740">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f22cd-740">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-741">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-741">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-742">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-742">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-743">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-743">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-744">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f22cd-744">Current status of the object.</span></span> <span data-ttu-id="f22cd-745">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="f22cd-745">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f22cd-746">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="f22cd-746">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f22cd-747">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="f22cd-747">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f22cd-748">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="f22cd-748">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f22cd-749">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="f22cd-749">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f22cd-750">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-750">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f22cd-751">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="f22cd-751">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f22cd-752">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-752">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f22cd-753">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-753">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f22cd-754">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-754">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-755">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-755">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f22cd-756">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-756">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f22cd-757">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-757">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f22cd-758">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-758">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f22cd-759">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-759">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f22cd-760">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-760">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f22cd-761">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-761">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f22cd-762">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-762">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f22cd-763">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-763">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-764">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f22cd-764">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-765">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="f22cd-765">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-766">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-766">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-767">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="f22cd-767">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-768">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="f22cd-768">State of the logical device.</span></span> <span data-ttu-id="f22cd-769">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="f22cd-769">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f22cd-770">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-770">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f22cd-771">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="f22cd-771">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f22cd-772">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="f22cd-772">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f22cd-773">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="f22cd-773">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f22cd-774">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="f22cd-774">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f22cd-775">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="f22cd-775">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-776">**StringFormat**</span><span class="sxs-lookup"><span data-stu-id="f22cd-776">**StringFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-777">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-777">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-778">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-778">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-779">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32 \_ API \| 行裝置結構 \| LINEDEVCAPS \| dwStringFormat」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-779">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Line Device Structures\|LINEDEVCAPS\|dwStringFormat")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-780">用於透過數據機傳遞之文字的字元類型。</span><span class="sxs-lookup"><span data-stu-id="f22cd-780">Type of characters used for text passed through the modem.</span></span>

<span data-ttu-id="f22cd-781">值如下：</span><span class="sxs-lookup"><span data-stu-id="f22cd-781">The values are:</span></span>

<dl> <dd><span data-ttu-id="f22cd-782">「ASCII 字串格式」</span><span class="sxs-lookup"><span data-stu-id="f22cd-782">"ASCII string format"</span></span></dd> <dd><span data-ttu-id="f22cd-783">"DBCS 字串格式"</span><span class="sxs-lookup"><span data-stu-id="f22cd-783">"DBCS string format"</span></span></dd> <dd><span data-ttu-id="f22cd-784">「UNICODE 字串格式」</span><span class="sxs-lookup"><span data-stu-id="f22cd-784">"UNICODE string format"</span></span></dd> </dl>

<dt>

<span id="ASCII_string_format"></span><span id="ascii_string_format"></span><span id="ASCII_STRING_FORMAT"></span>

<span data-ttu-id="f22cd-785">**Ascii 字串格式** ( 「ascii 字串格式」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-785">**ASCII string format** ("ASCII string format")</span></span>


</dt> <dd></dd> <dt>

<span id="DBCS_string_format"></span><span id="dbcs_string_format"></span><span id="DBCS_STRING_FORMAT"></span>

<span data-ttu-id="f22cd-786">**Dbcs 字串格式** ( "DBCS 字串格式" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-786">**DBCS string format** ("DBCS string format")</span></span>


</dt> <dd></dd> <dt>

<span id="UNICODE_string_format"></span><span id="unicode_string_format"></span><span id="UNICODE_STRING_FORMAT"></span>

<span data-ttu-id="f22cd-787">**Unicode 字串格式** ( 「unicode 字串格式」 ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-787">**UNICODE string format** ("UNICODE string format")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f22cd-788">**SupportsCallback**</span><span class="sxs-lookup"><span data-stu-id="f22cd-788">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-789">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f22cd-789">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-790">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-790">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-791">若 **為 TRUE**，則表示數據機支援回呼。</span><span class="sxs-lookup"><span data-stu-id="f22cd-791">If **TRUE**, the modem supports callback.</span></span>

<span data-ttu-id="f22cd-792">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-792">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-793">**SupportsSynchronousConnect**</span><span class="sxs-lookup"><span data-stu-id="f22cd-793">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-794">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="f22cd-794">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-795">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-795">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-796">若為 **TRUE**，則支援同步，以及非同步通訊。</span><span class="sxs-lookup"><span data-stu-id="f22cd-796">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

<span data-ttu-id="f22cd-797">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-797">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-798">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f22cd-798">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-799">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-799">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-800">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-800">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-801">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f22cd-801">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-802">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="f22cd-802">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="f22cd-803">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-803">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-804">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f22cd-804">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-805">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-805">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-806">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-806">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-807">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="f22cd-807">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-808">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="f22cd-808">Name of the scoping system.</span></span>

<span data-ttu-id="f22cd-809">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-809">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-810">**結束字元**</span><span class="sxs-lookup"><span data-stu-id="f22cd-810">**Terminator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-811">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-811">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-812">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-812">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-813">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| 結束字元" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-813">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Terminator")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-814">標示命令字串結尾的字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-814">String that marks the end of a command string.</span></span>

<span data-ttu-id="f22cd-815">範例： "<cr"</span><span class="sxs-lookup"><span data-stu-id="f22cd-815">Example: "<cr"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-816">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="f22cd-816">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-817">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f22cd-817">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-818">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-818">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-819">上次重設數據機的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="f22cd-819">Date and time the modem was last reset.</span></span>

<span data-ttu-id="f22cd-820">這個屬性繼承自 [**CIM \_ PotsModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-820">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-821">**語氣**</span><span class="sxs-lookup"><span data-stu-id="f22cd-821">**Tone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-822">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-822">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-823">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-823">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-824">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| 聲調" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-824">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Tone")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-825">指示數據機使用音調模式進行撥號的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-825">Command string that instructs the modem to use tone mode for dialing.</span></span> <span data-ttu-id="f22cd-826">電話線路必須支援音調撥號。</span><span class="sxs-lookup"><span data-stu-id="f22cd-826">The phone line must support tone dialing.</span></span>

<span data-ttu-id="f22cd-827">範例： "T"</span><span class="sxs-lookup"><span data-stu-id="f22cd-827">Example: "T"</span></span>

</dd> <dt>

<span data-ttu-id="f22cd-828">**VoiceSwitchFeature**</span><span class="sxs-lookup"><span data-stu-id="f22cd-828">**VoiceSwitchFeature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22cd-829">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f22cd-829">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-830">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f22cd-830">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22cd-831">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| VoiceSwitchFeature" ) </span><span class="sxs-lookup"><span data-stu-id="f22cd-831">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|VoiceSwitchFeature")</span></span>
</dt> </dl>

<span data-ttu-id="f22cd-832">用來啟動語音訊息語音功能的命令字串。</span><span class="sxs-lookup"><span data-stu-id="f22cd-832">Command strings used to activate the voice capabilities of a voice modem.</span></span>

<span data-ttu-id="f22cd-833">範例： "AT + V"</span><span class="sxs-lookup"><span data-stu-id="f22cd-833">Example: "AT+V"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f22cd-834">備註</span><span class="sxs-lookup"><span data-stu-id="f22cd-834">Remarks</span></span>

<span data-ttu-id="f22cd-835">**Win32 \_ POTSModem** 類別衍生自 [**CIM \_ POTSModem**](cim-potsmodem.md)。</span><span class="sxs-lookup"><span data-stu-id="f22cd-835">The **Win32\_POTSModem** class is derived from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f22cd-836">規格需求</span><span class="sxs-lookup"><span data-stu-id="f22cd-836">Requirements</span></span>



| <span data-ttu-id="f22cd-837">需求</span><span class="sxs-lookup"><span data-stu-id="f22cd-837">Requirement</span></span> | <span data-ttu-id="f22cd-838">值</span><span class="sxs-lookup"><span data-stu-id="f22cd-838">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f22cd-839">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f22cd-839">Minimum supported client</span></span><br/> | <span data-ttu-id="f22cd-840">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f22cd-840">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f22cd-841">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f22cd-841">Minimum supported server</span></span><br/> | <span data-ttu-id="f22cd-842">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f22cd-842">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f22cd-843">命名空間</span><span class="sxs-lookup"><span data-stu-id="f22cd-843">Namespace</span></span><br/>                | <span data-ttu-id="f22cd-844">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f22cd-844">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f22cd-845">MOF</span><span class="sxs-lookup"><span data-stu-id="f22cd-845">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f22cd-846"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f22cd-846"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f22cd-847">DLL</span><span class="sxs-lookup"><span data-stu-id="f22cd-847">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f22cd-848"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f22cd-848"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f22cd-849">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f22cd-849">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22cd-850">**CIM \_ PotsModem**</span><span class="sxs-lookup"><span data-stu-id="f22cd-850">**CIM\_PotsModem**</span></span>](cim-potsmodem.md)
</dt> <dt>

[<span data-ttu-id="f22cd-851">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="f22cd-851">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
