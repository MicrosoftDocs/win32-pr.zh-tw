---
description: Win32 \_ SERIALPORT WMI 類別代表執行 Windows 的電腦系統上的序列埠。
ms.assetid: f2e5cc5a-a12b-4079-92e1-6bb62fe797a0
ms.tgt_platform: multiple
title: Win32_SerialPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPort
- Win32_SerialPort.Reset
- Win32_SerialPort.SetPowerState
- Win32_SerialPort.Availability
- Win32_SerialPort.Binary
- Win32_SerialPort.Capabilities
- Win32_SerialPort.CapabilityDescriptions
- Win32_SerialPort.Caption
- Win32_SerialPort.ConfigManagerErrorCode
- Win32_SerialPort.ConfigManagerUserConfig
- Win32_SerialPort.CreationClassName
- Win32_SerialPort.Description
- Win32_SerialPort.DeviceID
- Win32_SerialPort.ErrorCleared
- Win32_SerialPort.ErrorDescription
- Win32_SerialPort.InstallDate
- Win32_SerialPort.LastErrorCode
- Win32_SerialPort.MaxBaudRate
- Win32_SerialPort.MaximumInputBufferSize
- Win32_SerialPort.MaximumOutputBufferSize
- Win32_SerialPort.MaxNumberControlled
- Win32_SerialPort.Name
- Win32_SerialPort.OSAutoDiscovered
- Win32_SerialPort.PNPDeviceID
- Win32_SerialPort.PowerManagementCapabilities
- Win32_SerialPort.PowerManagementSupported
- Win32_SerialPort.ProtocolSupported
- Win32_SerialPort.ProviderType
- Win32_SerialPort.SettableBaudRate
- Win32_SerialPort.SettableDataBits
- Win32_SerialPort.SettableFlowControl
- Win32_SerialPort.SettableParity
- Win32_SerialPort.SettableParityCheck
- Win32_SerialPort.SettableRLSD
- Win32_SerialPort.SettableStopBits
- Win32_SerialPort.Status
- Win32_SerialPort.StatusInfo
- Win32_SerialPort.Supports16BitMode
- Win32_SerialPort.SupportsDTRDSR
- Win32_SerialPort.SupportsElapsedTimeouts
- Win32_SerialPort.SupportsIntTimeouts
- Win32_SerialPort.SupportsParityCheck
- Win32_SerialPort.SupportsRLSD
- Win32_SerialPort.SupportsRTSCTS
- Win32_SerialPort.SupportsSpecialCharacters
- Win32_SerialPort.SupportsXOnXOff
- Win32_SerialPort.SupportsXOnXOffSet
- Win32_SerialPort.SystemCreationClassName
- Win32_SerialPort.SystemName
- Win32_SerialPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7fc2f25bc88d880ba9b10f10b5efde284a62624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110160"
---
# <a name="win32_serialport-class"></a><span data-ttu-id="dc61d-103">Win32 \_ SerialPort 類別</span><span class="sxs-lookup"><span data-stu-id="dc61d-103">Win32\_SerialPort class</span></span>

<span data-ttu-id="dc61d-104">**Win32 \_ SerialPort** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 的電腦系統上的序列埠。</span><span class="sxs-lookup"><span data-stu-id="dc61d-104">The **Win32\_SerialPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a serial port on a computer system running Windows.</span></span>

<span data-ttu-id="dc61d-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dc61d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dc61d-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="dc61d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc61d-107">語法</span><span class="sxs-lookup"><span data-stu-id="dc61d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPort : CIM_SerialController
{
  uint16   Availability;
  boolean  Binary;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
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
  uint32   MaxBaudRate;
  uint32   MaximumInputBufferSize;
  uint32   MaximumOutputBufferSize;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   ProviderType;
  boolean  SettableBaudRate;
  boolean  SettableDataBits;
  boolean  SettableFlowControl;
  boolean  SettableParity;
  boolean  SettableParityCheck;
  boolean  SettableRLSD;
  boolean  SettableStopBits;
  string   Status;
  uint16   StatusInfo;
  boolean  Supports16BitMode;
  boolean  SupportsDTRDSR;
  boolean  SupportsElapsedTimeouts;
  boolean  SupportsIntTimeouts;
  boolean  SupportsParityCheck;
  boolean  SupportsRLSD;
  boolean  SupportsRTSCTS;
  boolean  SupportsSpecialCharacters;
  boolean  SupportsXOnXOff;
  boolean  SupportsXOnXOffSet;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="dc61d-108">成員</span><span class="sxs-lookup"><span data-stu-id="dc61d-108">Members</span></span>

<span data-ttu-id="dc61d-109">**Win32 \_ SerialPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dc61d-109">The **Win32\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="dc61d-110">方法</span><span class="sxs-lookup"><span data-stu-id="dc61d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dc61d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="dc61d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dc61d-112">方法</span><span class="sxs-lookup"><span data-stu-id="dc61d-112">Methods</span></span>

<span data-ttu-id="dc61d-113">**Win32 \_ SerialPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dc61d-113">The **Win32\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="dc61d-114">方法</span><span class="sxs-lookup"><span data-stu-id="dc61d-114">Method</span></span>            | <span data-ttu-id="dc61d-115">描述</span><span class="sxs-lookup"><span data-stu-id="dc61d-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc61d-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="dc61d-116">**Reset**</span></span>         | <span data-ttu-id="dc61d-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="dc61d-117">Not implemented.</span></span> <span data-ttu-id="dc61d-118">若要執行此方法，請參閱 [**CIM \_ SerialController**](cim-serialcontroller.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="dc61d-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="dc61d-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dc61d-119">**SetPowerState**</span></span> | <span data-ttu-id="dc61d-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="dc61d-120">Not implemented.</span></span> <span data-ttu-id="dc61d-121">若要執行此方法，請參閱 [**CIM \_ SerialController**](cim-serialcontroller.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="dc61d-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dc61d-122">屬性</span><span class="sxs-lookup"><span data-stu-id="dc61d-122">Properties</span></span>

<span data-ttu-id="dc61d-123">**Win32 \_ SerialPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="dc61d-123">The **Win32\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc61d-124">**可用性**</span><span class="sxs-lookup"><span data-stu-id="dc61d-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dc61d-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-127">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="dc61d-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-128">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="dc61d-128">Availability and status of the device.</span></span>

<span data-ttu-id="dc61d-129">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc61d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="dc61d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc61d-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="dc61d-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dc61d-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="dc61d-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-133">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="dc61d-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dc61d-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="dc61d-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dc61d-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="dc61d-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dc61d-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="dc61d-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dc61d-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="dc61d-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dc61d-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="dc61d-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dc61d-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="dc61d-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dc61d-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="dc61d-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dc61d-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="dc61d-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dc61d-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="dc61d-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dc61d-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="dc61d-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-144">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="dc61d-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dc61d-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="dc61d-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-146">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="dc61d-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dc61d-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="dc61d-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-148">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="dc61d-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dc61d-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="dc61d-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dc61d-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="dc61d-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-151">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="dc61d-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dc61d-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="dc61d-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-153">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="dc61d-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dc61d-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="dc61d-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-155">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="dc61d-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dc61d-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="dc61d-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-157">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="dc61d-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dc61d-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="dc61d-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-159">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="dc61d-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc61d-160">**二進位**</span><span class="sxs-lookup"><span data-stu-id="dc61d-160">**Binary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-161">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-163">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-164">若為 **TRUE**，則表示序列埠是針對二進位資料傳輸而設定。</span><span class="sxs-lookup"><span data-stu-id="dc61d-164">If **TRUE**, the serial port is configured for binary data transfer.</span></span> <span data-ttu-id="dc61d-165">由於 Windows API 不支援非二進位模式傳送，因此此屬性必須為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="dc61d-165">Because the Windows API does not support nonbinary mode transfers, this property must be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-166">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="dc61d-166">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-167">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="dc61d-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-169">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) (」 MIF。DMTF \| 序列埠 \| 004.7 ") ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md)。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="dc61d-169">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-170">序列控制器的晶片層級相容性陣列。</span><span class="sxs-lookup"><span data-stu-id="dc61d-170">Array of chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="dc61d-171">此屬性描述可能在晶片硬體中固有之串列控制器的緩衝和其他功能。</span><span class="sxs-lookup"><span data-stu-id="dc61d-171">This property describes the buffering and other capabilities of the serial controller that may be inherent in the chip hardware.</span></span> <span data-ttu-id="dc61d-172">屬性是列舉的整數。</span><span class="sxs-lookup"><span data-stu-id="dc61d-172">The property is an enumerated integer.</span></span>

<span data-ttu-id="dc61d-173">這個屬性繼承自 [**CIM \_ SerialController**](cim-serialcontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-173">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc61d-174">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="dc61d-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc61d-175">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="dc61d-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="dc61d-176">**XT/相容** (3) </span><span class="sxs-lookup"><span data-stu-id="dc61d-176">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="dc61d-177">**16450 相容** (4) </span><span class="sxs-lookup"><span data-stu-id="dc61d-177">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="dc61d-178">**16550 相容** (5) </span><span class="sxs-lookup"><span data-stu-id="dc61d-178">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="dc61d-179">**16550A 相容** (6) </span><span class="sxs-lookup"><span data-stu-id="dc61d-179">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="dc61d-180">**8251 相容** (160) </span><span class="sxs-lookup"><span data-stu-id="dc61d-180">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="dc61d-181">**8251FIFO 相容** (161) </span><span class="sxs-lookup"><span data-stu-id="dc61d-181">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc61d-182">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dc61d-182">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-183">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="dc61d-183">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-185">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( "Indexed" ) ， [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( "[**CIM \_ SerialController**](cim-serialcontroller.md)。**功能**") </span><span class="sxs-lookup"><span data-stu-id="dc61d-185">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-186">自由格式字串的陣列，為 **功能** 陣列中指出的任何序列控制器功能提供更詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="dc61d-186">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="dc61d-187">請注意，這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="dc61d-187">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="dc61d-188">這個屬性繼承自 [**CIM \_ SerialController**](cim-serialcontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-188">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-189">**標題**</span><span class="sxs-lookup"><span data-stu-id="dc61d-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-192">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-193">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="dc61d-193">Short description of the object.</span></span>

<span data-ttu-id="dc61d-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dc61d-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-196">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dc61d-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-198">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-198">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-199">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc61d-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="dc61d-200">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="dc61d-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="dc61d-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="dc61d-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-203">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="dc61d-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="dc61d-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="dc61d-205">(1)</span><span class="sxs-lookup"><span data-stu-id="dc61d-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-206">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="dc61d-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dc61d-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="dc61d-208">(2)</span><span class="sxs-lookup"><span data-stu-id="dc61d-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="dc61d-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="dc61d-210">(3)</span><span class="sxs-lookup"><span data-stu-id="dc61d-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-211">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="dc61d-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dc61d-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="dc61d-213">(4)</span><span class="sxs-lookup"><span data-stu-id="dc61d-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-214">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="dc61d-214">Device is not working properly.</span></span> <span data-ttu-id="dc61d-215">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="dc61d-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="dc61d-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="dc61d-217">(5)</span><span class="sxs-lookup"><span data-stu-id="dc61d-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-218">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="dc61d-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="dc61d-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="dc61d-220">(6)</span><span class="sxs-lookup"><span data-stu-id="dc61d-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-221">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="dc61d-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="dc61d-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="dc61d-223">(7)</span><span class="sxs-lookup"><span data-stu-id="dc61d-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="dc61d-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="dc61d-225">(8)</span><span class="sxs-lookup"><span data-stu-id="dc61d-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-226">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="dc61d-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="dc61d-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="dc61d-228">(9)</span><span class="sxs-lookup"><span data-stu-id="dc61d-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-229">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="dc61d-229">Device is not working properly.</span></span> <span data-ttu-id="dc61d-230">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="dc61d-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="dc61d-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="dc61d-232">(10)</span><span class="sxs-lookup"><span data-stu-id="dc61d-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-233">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="dc61d-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="dc61d-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="dc61d-235">(11)</span><span class="sxs-lookup"><span data-stu-id="dc61d-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-236">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="dc61d-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="dc61d-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="dc61d-238"> (12) </span><span class="sxs-lookup"><span data-stu-id="dc61d-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-239">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="dc61d-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="dc61d-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="dc61d-241">(13)</span><span class="sxs-lookup"><span data-stu-id="dc61d-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-242">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="dc61d-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="dc61d-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="dc61d-244">(14)</span><span class="sxs-lookup"><span data-stu-id="dc61d-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-245">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="dc61d-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="dc61d-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="dc61d-247">(15)</span><span class="sxs-lookup"><span data-stu-id="dc61d-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-248">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="dc61d-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="dc61d-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="dc61d-250">(16)</span><span class="sxs-lookup"><span data-stu-id="dc61d-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-251">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="dc61d-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="dc61d-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="dc61d-253">(17)</span><span class="sxs-lookup"><span data-stu-id="dc61d-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-254">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="dc61d-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dc61d-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="dc61d-256">(18)</span><span class="sxs-lookup"><span data-stu-id="dc61d-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-257">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="dc61d-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="dc61d-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="dc61d-259">(19)</span><span class="sxs-lookup"><span data-stu-id="dc61d-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dc61d-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="dc61d-261">(20)</span><span class="sxs-lookup"><span data-stu-id="dc61d-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-262">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="dc61d-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="dc61d-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="dc61d-264">(21)</span><span class="sxs-lookup"><span data-stu-id="dc61d-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-265">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="dc61d-265">System failure.</span></span> <span data-ttu-id="dc61d-266">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="dc61d-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="dc61d-267">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="dc61d-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="dc61d-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="dc61d-269">(22)</span><span class="sxs-lookup"><span data-stu-id="dc61d-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-270">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="dc61d-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="dc61d-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="dc61d-272">(23)</span><span class="sxs-lookup"><span data-stu-id="dc61d-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-273">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="dc61d-273">System failure.</span></span> <span data-ttu-id="dc61d-274">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="dc61d-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="dc61d-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="dc61d-276">(24)</span><span class="sxs-lookup"><span data-stu-id="dc61d-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-277">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="dc61d-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dc61d-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dc61d-279">(25)</span><span class="sxs-lookup"><span data-stu-id="dc61d-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-280">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="dc61d-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dc61d-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dc61d-282">(26)</span><span class="sxs-lookup"><span data-stu-id="dc61d-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-283">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="dc61d-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="dc61d-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="dc61d-285">(27)</span><span class="sxs-lookup"><span data-stu-id="dc61d-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-286">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="dc61d-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="dc61d-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="dc61d-288">(28)</span><span class="sxs-lookup"><span data-stu-id="dc61d-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-289">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="dc61d-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="dc61d-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="dc61d-291">(29)</span><span class="sxs-lookup"><span data-stu-id="dc61d-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-292">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="dc61d-292">Device is disabled.</span></span> <span data-ttu-id="dc61d-293">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="dc61d-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="dc61d-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="dc61d-295">(30)</span><span class="sxs-lookup"><span data-stu-id="dc61d-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-296">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="dc61d-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dc61d-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="dc61d-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="dc61d-298"> (31) </span><span class="sxs-lookup"><span data-stu-id="dc61d-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-299">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="dc61d-299">Device is not working properly.</span></span> <span data-ttu-id="dc61d-300">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="dc61d-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc61d-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="dc61d-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-302">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-304">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-304">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-305">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="dc61d-305">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="dc61d-306">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc61d-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-308">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-310">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dc61d-310">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-311">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="dc61d-311">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="dc61d-312">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="dc61d-312">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dc61d-313">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-314">**說明**</span><span class="sxs-lookup"><span data-stu-id="dc61d-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-315">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-317">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-317">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-318">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="dc61d-318">Description of the object.</span></span>

<span data-ttu-id="dc61d-319">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dc61d-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-323">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| 硬體 \\ \\ DeviceMap \\ \\ SerialComm" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-323">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-324">序列埠的唯一識別碼與系統上的其他裝置。</span><span class="sxs-lookup"><span data-stu-id="dc61d-324">Unique identifier of the serial port with other devices on the system.</span></span>

<span data-ttu-id="dc61d-325">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="dc61d-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-327">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-329">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="dc61d-329">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="dc61d-330">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dc61d-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-332">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-334">自由格式字串提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dc61d-334">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="dc61d-335">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-336">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dc61d-336">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-337">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dc61d-337">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-339">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="dc61d-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-340">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="dc61d-340">Date and time the object was installed.</span></span> <span data-ttu-id="dc61d-341">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="dc61d-341">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dc61d-342">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-343">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dc61d-343">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-344">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dc61d-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-346">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc61d-346">Last error code reported by the logical device.</span></span>

<span data-ttu-id="dc61d-347">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-347">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-348">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="dc61d-348">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-349">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dc61d-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-351">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 序列埠 \| 004.6 「) ， [**單位**](../wmisdk/standard-qualifiers.md) ( 每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-352">序列控制器支援的最大傳輸速率 (每秒位數) 。</span><span class="sxs-lookup"><span data-stu-id="dc61d-352">Maximum baud rate (in bits per second) supported by the serial controller.</span></span>

<span data-ttu-id="dc61d-353">這個屬性繼承自 [**CIM \_ SerialController**](cim-serialcontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-353">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-354">**MaximumInputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="dc61d-354">**MaximumInputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-355">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dc61d-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-357">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxRxQueue" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxRxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-358">序列埠驅動程式內部輸入緩衝區的大小上限。</span><span class="sxs-lookup"><span data-stu-id="dc61d-358">Maximum size of the serial port driver's internal input buffer.</span></span> <span data-ttu-id="dc61d-359">值為 0 (零) 表示序列提供者未加諸任何最大值。</span><span class="sxs-lookup"><span data-stu-id="dc61d-359">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-360">**MaximumOutputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="dc61d-360">**MaximumOutputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-361">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dc61d-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-363">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxTxQueue" ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxTxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-364">序列埠驅動程式內部輸出緩衝區的大小上限。</span><span class="sxs-lookup"><span data-stu-id="dc61d-364">Maximum size of the serial port driver's internal output buffer.</span></span> <span data-ttu-id="dc61d-365">值為 0 (零) 表示序列提供者未加諸任何最大值。</span><span class="sxs-lookup"><span data-stu-id="dc61d-365">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-366">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="dc61d-366">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-367">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dc61d-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-369">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="dc61d-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-370">此控制器可支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="dc61d-370">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="dc61d-371">值為 0 (零) 如果數位未知，則應使用此值。</span><span class="sxs-lookup"><span data-stu-id="dc61d-371">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="dc61d-372">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-372">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-373">**名稱**</span><span class="sxs-lookup"><span data-stu-id="dc61d-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-376">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-377">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="dc61d-377">Label by which the object is known.</span></span> <span data-ttu-id="dc61d-378">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="dc61d-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="dc61d-379">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-380">**OSAutoDiscovered**</span><span class="sxs-lookup"><span data-stu-id="dc61d-380">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-381">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-383">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| 硬體 \\ \\ DESCRIPTION \\ \\ SYSTEM \\ \\ MultifunctionAdapter" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\DESCRIPTION\\\\SYSTEM\\\\MultifunctionAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-384">若 **為 TRUE**，則作業系統會自動探索此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="dc61d-384">If **TRUE**, the instances of this class were automatically discovered by the operating system.</span></span> <span data-ttu-id="dc61d-385">例如，如果硬體是透過主控台新增，作業系統會藉由從這個類別的實例查詢硬體來尋找此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="dc61d-385">If, for example, hardware was added through Control Panel, the operating system finds instances of this class by querying hardware from the instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="dc61d-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-387">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-389">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-389">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-390">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc61d-390">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="dc61d-391">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dc61d-392">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="dc61d-392">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="dc61d-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-394">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="dc61d-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-396">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="dc61d-396">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="dc61d-397">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="dc61d-397">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc61d-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="dc61d-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dc61d-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="dc61d-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dc61d-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="dc61d-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dc61d-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="dc61d-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-402">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="dc61d-402">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dc61d-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="dc61d-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-404">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="dc61d-404">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dc61d-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="dc61d-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-406">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="dc61d-406">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="dc61d-407">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="dc61d-407">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="dc61d-408">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-408">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dc61d-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="dc61d-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-410">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="dc61d-410">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dc61d-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="dc61d-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-412">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="dc61d-412">Timed Power-On Supported</span></span>

<span data-ttu-id="dc61d-413">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="dc61d-413">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc61d-414">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="dc61d-414">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-415">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-417">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="dc61d-417">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="dc61d-418">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="dc61d-418">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="dc61d-419">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-420">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="dc61d-420">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-421">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dc61d-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-423">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="dc61d-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-424">控制器用來存取「受控制」裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dc61d-424">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="dc61d-425">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-425">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="dc61d-426">下列清單顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="dc61d-426">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc61d-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="dc61d-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc61d-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="dc61d-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="dc61d-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3) </span><span class="sxs-lookup"><span data-stu-id="dc61d-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="dc61d-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4) </span><span class="sxs-lookup"><span data-stu-id="dc61d-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="dc61d-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5) </span><span class="sxs-lookup"><span data-stu-id="dc61d-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="dc61d-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6) </span><span class="sxs-lookup"><span data-stu-id="dc61d-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dc61d-433">ATA 或 ATAPI</span><span class="sxs-lookup"><span data-stu-id="dc61d-433">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="dc61d-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**彈性磁片** (7) </span><span class="sxs-lookup"><span data-stu-id="dc61d-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="dc61d-435"><span id="1496"></span>**1496** (8) </span><span class="sxs-lookup"><span data-stu-id="dc61d-435"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="dc61d-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI 平行介面** (9) </span><span class="sxs-lookup"><span data-stu-id="dc61d-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="dc61d-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI 光纖通道通訊協定** (10) </span><span class="sxs-lookup"><span data-stu-id="dc61d-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="dc61d-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI 序列匯流排通訊協定** (11) </span><span class="sxs-lookup"><span data-stu-id="dc61d-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="dc61d-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI 序列匯流排通訊協定-2 (1394)** (12) </span><span class="sxs-lookup"><span data-stu-id="dc61d-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="dc61d-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI 序列儲存架構** (13) </span><span class="sxs-lookup"><span data-stu-id="dc61d-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="dc61d-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14) </span><span class="sxs-lookup"><span data-stu-id="dc61d-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="dc61d-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15) </span><span class="sxs-lookup"><span data-stu-id="dc61d-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="dc61d-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**通用序列匯流排** (16) </span><span class="sxs-lookup"><span data-stu-id="dc61d-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="dc61d-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**平行通訊協定** (17) </span><span class="sxs-lookup"><span data-stu-id="dc61d-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="dc61d-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18) </span><span class="sxs-lookup"><span data-stu-id="dc61d-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="dc61d-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**診斷** (19) </span><span class="sxs-lookup"><span data-stu-id="dc61d-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="dc61d-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20) </span><span class="sxs-lookup"><span data-stu-id="dc61d-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="dc61d-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21) </span><span class="sxs-lookup"><span data-stu-id="dc61d-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="dc61d-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22) </span><span class="sxs-lookup"><span data-stu-id="dc61d-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="dc61d-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23) </span><span class="sxs-lookup"><span data-stu-id="dc61d-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="dc61d-451"><span id="VME"></span><span id="vme"></span>**Vm** (24) </span><span class="sxs-lookup"><span data-stu-id="dc61d-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="dc61d-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25) </span><span class="sxs-lookup"><span data-stu-id="dc61d-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="dc61d-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26) </span><span class="sxs-lookup"><span data-stu-id="dc61d-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="dc61d-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27) </span><span class="sxs-lookup"><span data-stu-id="dc61d-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="dc61d-455"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28) </span><span class="sxs-lookup"><span data-stu-id="dc61d-455"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="dc61d-456"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29) </span><span class="sxs-lookup"><span data-stu-id="dc61d-456"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="dc61d-457"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30) </span><span class="sxs-lookup"><span data-stu-id="dc61d-457"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="dc61d-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31) </span><span class="sxs-lookup"><span data-stu-id="dc61d-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="dc61d-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32) </span><span class="sxs-lookup"><span data-stu-id="dc61d-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="dc61d-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 權杖-環形** (33) </span><span class="sxs-lookup"><span data-stu-id="dc61d-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="dc61d-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9.5 FDDI** (34) </span><span class="sxs-lookup"><span data-stu-id="dc61d-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="dc61d-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35) </span><span class="sxs-lookup"><span data-stu-id="dc61d-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="dc61d-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36) </span><span class="sxs-lookup"><span data-stu-id="dc61d-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="dc61d-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37) </span><span class="sxs-lookup"><span data-stu-id="dc61d-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="dc61d-465"><span id="CMD"></span><span id="cmd"></span>**CMD** (38) </span><span class="sxs-lookup"><span data-stu-id="dc61d-465"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="dc61d-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39) </span><span class="sxs-lookup"><span data-stu-id="dc61d-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="dc61d-467"><span id="DSSI"></span><span id="dssi"></span>**」 Dssi 小組** (40) </span><span class="sxs-lookup"><span data-stu-id="dc61d-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="dc61d-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41) </span><span class="sxs-lookup"><span data-stu-id="dc61d-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="dc61d-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**增強型 ATA/IDE** (42) </span><span class="sxs-lookup"><span data-stu-id="dc61d-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="dc61d-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43) </span><span class="sxs-lookup"><span data-stu-id="dc61d-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="dc61d-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (雙向紅外線)** (44) </span><span class="sxs-lookup"><span data-stu-id="dc61d-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="dc61d-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**(快速紅外線)** (45) 的杉樹</span><span class="sxs-lookup"><span data-stu-id="dc61d-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="dc61d-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (串列紅外線)** (46) </span><span class="sxs-lookup"><span data-stu-id="dc61d-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="dc61d-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47) </span><span class="sxs-lookup"><span data-stu-id="dc61d-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc61d-475">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="dc61d-475">**ProviderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-476">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-478">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvSubType" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvSubType")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-479">通訊提供者類型。</span><span class="sxs-lookup"><span data-stu-id="dc61d-479">Communications provider type.</span></span>

<span data-ttu-id="dc61d-480">值如下：</span><span class="sxs-lookup"><span data-stu-id="dc61d-480">The values are:</span></span>

<dl> <dd><span data-ttu-id="dc61d-481">「傳真裝置」</span><span class="sxs-lookup"><span data-stu-id="dc61d-481">"FAX Device"</span></span></dd> <dd><span data-ttu-id="dc61d-482">"LAT Protocol"</span><span class="sxs-lookup"><span data-stu-id="dc61d-482">"LAT Protocol"</span></span></dd> <dd><span data-ttu-id="dc61d-483">「數據機裝置」</span><span class="sxs-lookup"><span data-stu-id="dc61d-483">"Modem Device"</span></span></dd> <dd><span data-ttu-id="dc61d-484">「網路橋接器」</span><span class="sxs-lookup"><span data-stu-id="dc61d-484">"Network Bridge"</span></span></dd> <dd><span data-ttu-id="dc61d-485">「平行埠」</span><span class="sxs-lookup"><span data-stu-id="dc61d-485">"Parallel Port"</span></span></dd> <dd><span data-ttu-id="dc61d-486">"RS232 序列埠"</span><span class="sxs-lookup"><span data-stu-id="dc61d-486">"RS232 Serial Port"</span></span></dd> <dd><span data-ttu-id="dc61d-487">"RS422 Port"</span><span class="sxs-lookup"><span data-stu-id="dc61d-487">"RS422 Port"</span></span></dd> <dd><span data-ttu-id="dc61d-488">"RS423 Port"</span><span class="sxs-lookup"><span data-stu-id="dc61d-488">"RS423 Port"</span></span></dd> <dd><span data-ttu-id="dc61d-489">"RS449 Port"</span><span class="sxs-lookup"><span data-stu-id="dc61d-489">"RS449 Port"</span></span></dd> <dd><span data-ttu-id="dc61d-490">「掃描器裝置」</span><span class="sxs-lookup"><span data-stu-id="dc61d-490">"Scanner Device"</span></span></dd> <dd><span data-ttu-id="dc61d-491">「TCP/IP TelNet」</span><span class="sxs-lookup"><span data-stu-id="dc61d-491">"TCP/IP TelNet"</span></span></dd> <dd><span data-ttu-id="dc61d-492">"X. 25"</span><span class="sxs-lookup"><span data-stu-id="dc61d-492">"X.25"</span></span></dd> <dd><span data-ttu-id="dc61d-493">未知</span><span class="sxs-lookup"><span data-stu-id="dc61d-493">"Unspecified"</span></span></dd> </dl>

<dt>

<span id="FAX_Device"></span><span id="fax_device"></span><span id="FAX_DEVICE"></span>

<span data-ttu-id="dc61d-494">**傳真裝置** ( 「傳真裝置」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-494">**FAX Device** ("FAX Device")</span></span>


</dt> <dd></dd> <dt>

<span id="LAT_Protocol"></span><span id="lat_protocol"></span><span id="LAT_PROTOCOL"></span>

<span data-ttu-id="dc61d-495">**Lat 通訊協定** ( "lat protocol" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-495">**LAT Protocol** ("LAT Protocol")</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Device"></span><span id="modem_device"></span><span id="MODEM_DEVICE"></span>

<span data-ttu-id="dc61d-496">**數據機裝置** ( 「數據機裝置」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-496">**Modem Device** ("Modem Device")</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Bridge"></span><span id="network_bridge"></span><span id="NETWORK_BRIDGE"></span>

<span data-ttu-id="dc61d-497">**網路橋接器** ( 「網路橋接器」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-497">**Network Bridge** ("Network Bridge")</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="dc61d-498">**平行埠** ( 「平行埠」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-498">**Parallel Port** ("Parallel Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS232_Serial_Port"></span><span id="rs232_serial_port"></span><span id="RS232_SERIAL_PORT"></span>

<span data-ttu-id="dc61d-499">**Rs232 序列埠** ( "RS232 序列埠" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-499">**RS232 Serial Port** ("RS232 Serial Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS422_Port"></span><span id="rs422_port"></span><span id="RS422_PORT"></span>

<span data-ttu-id="dc61d-500">**RS422 埠** ( "RS422 port" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-500">**RS422 Port** ("RS422 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS423_Port"></span><span id="rs423_port"></span><span id="RS423_PORT"></span>

<span data-ttu-id="dc61d-501">**RS423 埠** ( "RS423 port" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-501">**RS423 Port** ("RS423 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS449_Port"></span><span id="rs449_port"></span><span id="RS449_PORT"></span>

<span data-ttu-id="dc61d-502">**RS449 埠** ( "RS449 port" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-502">**RS449 Port** ("RS449 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="Scanner_Device"></span><span id="scanner_device"></span><span id="SCANNER_DEVICE"></span>

<span data-ttu-id="dc61d-503">**掃描器裝置** ( 「掃描器裝置」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-503">**Scanner Device** ("Scanner Device")</span></span>


</dt> <dd></dd> <dt>

<span id="TCP_IP_TelNet"></span><span id="tcp_ip_telnet"></span><span id="TCP_IP_TELNET"></span>

<span data-ttu-id="dc61d-504">**Tcp/ip telnet** ( "tcp/ip telnet" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-504">**TCP/IP TelNet** ("TCP/IP TelNet")</span></span>


</dt> <dd></dd> <dt>

<span id="X.25"></span><span id="x.25"></span>

<span data-ttu-id="dc61d-505">**( "x. 25"** ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-505">**X.25** ("X.25")</span></span>


</dt> <dd></dd> <dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="dc61d-506">**未指定** ( 「未指定」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-506">**Unspecified** ("Unspecified")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc61d-507">**SettableBaudRate**</span><span class="sxs-lookup"><span data-stu-id="dc61d-507">**SettableBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-508">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-508">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-509">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-510">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ 波特" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_BAUD")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-511">若 **為 TRUE**，可針對此序列埠變更傳輸速率。</span><span class="sxs-lookup"><span data-stu-id="dc61d-511">If **TRUE**, the baud rate can be changed for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-512">**SettableDataBits**</span><span class="sxs-lookup"><span data-stu-id="dc61d-512">**SettableDataBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-513">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-513">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-514">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-515">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ DATABITS" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-515">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_DATABITS")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-516">若 **為 TRUE**，則可設定此序列埠的資料位。</span><span class="sxs-lookup"><span data-stu-id="dc61d-516">If **TRUE**, data bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-517">**SettableFlowControl**</span><span class="sxs-lookup"><span data-stu-id="dc61d-517">**SettableFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-518">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-520">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ 握手" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_HANDSHAKING")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-521">若 **為 TRUE**，則可為此序列埠設定流程式控制制。</span><span class="sxs-lookup"><span data-stu-id="dc61d-521">If **TRUE**, flow control can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-522">**SettableParity**</span><span class="sxs-lookup"><span data-stu-id="dc61d-522">**SettableParity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-523">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-523">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-525">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP 同位 \_ " ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-525">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-526">若 **為 TRUE**，則可設定此序列埠的同位檢查。</span><span class="sxs-lookup"><span data-stu-id="dc61d-526">If **TRUE**, parity can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-527">**SettableParityCheck**</span><span class="sxs-lookup"><span data-stu-id="dc61d-527">**SettableParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-528">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-529">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-530">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP 同位 \_ \_ 檢查" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-530">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-531">若 **為 TRUE**，則可以設定此序列埠的同位檢查， (是否) 支援同位檢查。</span><span class="sxs-lookup"><span data-stu-id="dc61d-531">If **TRUE**, parity checking can be set for this serial port (if parity checking is supported).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-532">**SettableRLSD**</span><span class="sxs-lookup"><span data-stu-id="dc61d-532">**SettableRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-533">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-533">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-534">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-535">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ RLSD" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-535">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-536">若 **為 TRUE**，則可為此序列埠設定接收的線路信號偵測 (rlsd) 可 (是否) 受支援的 rlsd。</span><span class="sxs-lookup"><span data-stu-id="dc61d-536">If **TRUE**, Received Line Signal Detect (RLSD) can be set for this serial port (if RLSD is supported).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-537">**SettableStopBits**</span><span class="sxs-lookup"><span data-stu-id="dc61d-537">**SettableStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-538">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-538">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-539">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-540">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ STOPBITS" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-540">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_STOPBITS")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-541">若 **為 TRUE**，則可設定此序列埠的停止位。</span><span class="sxs-lookup"><span data-stu-id="dc61d-541">If **TRUE**, stop bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-542">**狀態**</span><span class="sxs-lookup"><span data-stu-id="dc61d-542">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-543">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-543">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-544">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-544">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-545">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-545">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-546">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="dc61d-546">Current status of the object.</span></span> <span data-ttu-id="dc61d-547">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="dc61d-547">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dc61d-548">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="dc61d-548">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="dc61d-549">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="dc61d-549">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dc61d-550">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="dc61d-550">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dc61d-551">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="dc61d-551">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dc61d-552">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-552">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dc61d-553">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="dc61d-553">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dc61d-554">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-554">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dc61d-555">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-555">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dc61d-556">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-556">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc61d-557">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-557">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dc61d-558">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-558">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dc61d-559">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-559">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dc61d-560">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-560">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dc61d-561">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-561">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dc61d-562">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-562">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dc61d-563">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-563">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dc61d-564">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-564">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dc61d-565">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-565">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc61d-566">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dc61d-566">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-567">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="dc61d-567">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-568">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-568">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-569">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="dc61d-569">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-570">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="dc61d-570">State of the logical device.</span></span> <span data-ttu-id="dc61d-571">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="dc61d-571">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="dc61d-572">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-572">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc61d-573">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="dc61d-573">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc61d-574">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="dc61d-574">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dc61d-575">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="dc61d-575">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dc61d-576">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="dc61d-576">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dc61d-577">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="dc61d-577">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc61d-578">**Supports16BitMode**</span><span class="sxs-lookup"><span data-stu-id="dc61d-578">**Supports16BitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-579">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-579">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-580">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-581">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ 16BITMODE" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_16BITMODE")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-582">若 **為 TRUE**，則表示此序列埠支援16位模式。</span><span class="sxs-lookup"><span data-stu-id="dc61d-582">If **TRUE**, 16-bit mode is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-583">**SupportsDTRDSR**</span><span class="sxs-lookup"><span data-stu-id="dc61d-583">**SupportsDTRDSR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-584">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-585">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-585">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-586">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ DTRDSR" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-586">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_DTRDSR")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-587">若 **為 TRUE**，則會在此序列埠上支援 data terminal READY (DTR) 和 data set READY (DSR) 信號。</span><span class="sxs-lookup"><span data-stu-id="dc61d-587">If **TRUE**, data terminal ready (DTR) and data set ready (DSR) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-588">**SupportsElapsedTimeouts**</span><span class="sxs-lookup"><span data-stu-id="dc61d-588">**SupportsElapsedTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-589">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-589">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-590">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-591">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ TOTALTIMEOUTS" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-591">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_TOTALTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-592">若 **為 TRUE**，則表示此序列埠支援經過的時間。</span><span class="sxs-lookup"><span data-stu-id="dc61d-592">If **TRUE**, elapsed time-outs are supported on this serial port.</span></span> <span data-ttu-id="dc61d-593">經過的超時會追蹤資料傳輸之間的總時間量。</span><span class="sxs-lookup"><span data-stu-id="dc61d-593">Elapsed timeouts track the total amount of time between data transmissions.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-594">**SupportsIntTimeouts**</span><span class="sxs-lookup"><span data-stu-id="dc61d-594">**SupportsIntTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-595">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-595">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-596">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-597">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ INTTIMEOUTS" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-597">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_INTTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-598">若 **為 TRUE**，則支援間隔時間超時。</span><span class="sxs-lookup"><span data-stu-id="dc61d-598">If **TRUE**, interval time-outs are supported.</span></span> <span data-ttu-id="dc61d-599">間隔 timeout 是每個資料片段抵達之間的允許時間量。</span><span class="sxs-lookup"><span data-stu-id="dc61d-599">An interval timeout is the amount of time allowed to elapse between the arrival of each piece of data.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-600">**SupportsParityCheck**</span><span class="sxs-lookup"><span data-stu-id="dc61d-600">**SupportsParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-601">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-601">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-602">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-603">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF 同位 \_ \_ 檢查" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-603">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-604">若 **為 TRUE**，則此序列埠支援同位檢查。</span><span class="sxs-lookup"><span data-stu-id="dc61d-604">If **TRUE**, parity checking is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-605">**SupportsRLSD**</span><span class="sxs-lookup"><span data-stu-id="dc61d-605">**SupportsRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-606">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-606">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-607">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-608">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RLSD" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-608">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-609">若 **為 TRUE**，則此序列埠支援接收的線路信號偵測 (RLSD) 。</span><span class="sxs-lookup"><span data-stu-id="dc61d-609">If **TRUE**, Received Line Signal Detect (RLSD) is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-610">**SupportsRTSCTS**</span><span class="sxs-lookup"><span data-stu-id="dc61d-610">**SupportsRTSCTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-611">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-611">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-612">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-612">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-613">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RTSCTS" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-613">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RTSCTS")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-614">若為 **TRUE**，表示已準備好傳送 (RTS) 和清除以傳送 (CTS) 信號會在此序列埠上受到支援。</span><span class="sxs-lookup"><span data-stu-id="dc61d-614">If **TRUE**, ready to send (RTS) and clear to send (CTS) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-615">**SupportsSpecialCharacters**</span><span class="sxs-lookup"><span data-stu-id="dc61d-615">**SupportsSpecialCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-616">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-616">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-617">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-618">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SPECIALCHARS" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-618">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SPECIALCHARS")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-619">若 **為 TRUE**，則支援序列埠控制字元。</span><span class="sxs-lookup"><span data-stu-id="dc61d-619">If **TRUE**, serial port control characters are supported.</span></span> <span data-ttu-id="dc61d-620">這些字元會發出事件的信號，而不是資料。</span><span class="sxs-lookup"><span data-stu-id="dc61d-620">These characters signal events rather than data.</span></span> <span data-ttu-id="dc61d-621">這些字元無法顯示，而是由驅動程式設定。</span><span class="sxs-lookup"><span data-stu-id="dc61d-621">These characters are not displayable and are set by the driver.</span></span> <span data-ttu-id="dc61d-622">其中包括 EofChar、ErrorChar、BreakChar、EventChar、XonChar 和 XoffChar。</span><span class="sxs-lookup"><span data-stu-id="dc61d-622">They include EofChar, ErrorChar, BreakChar, EventChar, XonChar, and XoffChar.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-623">**SupportsXOnXOff**</span><span class="sxs-lookup"><span data-stu-id="dc61d-623">**SupportsXOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-624">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-624">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-625">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-626">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ XONXOFF" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-626">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_XONXOFF")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-627">若 **為 TRUE**，則會在此序列埠上支援 XON 或 XOFF 流程式控制制。</span><span class="sxs-lookup"><span data-stu-id="dc61d-627">If **TRUE**, XON or XOFF flow-control is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-628">**SupportsXOnXOffSet**</span><span class="sxs-lookup"><span data-stu-id="dc61d-628">**SupportsXOnXOffSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-629">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="dc61d-629">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-630">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-631">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Communication 結構 \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SETXCHAR" ) </span><span class="sxs-lookup"><span data-stu-id="dc61d-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SETXCHAR")</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-632">若 **為 TRUE**，表示通訊提供者支援設定 XONor XOFF 流程式控制制設定。</span><span class="sxs-lookup"><span data-stu-id="dc61d-632">If **TRUE**, the communications provider supports configuration of the XONor XOFF flow-control setting.</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-633">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc61d-633">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-634">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-635">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-636">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dc61d-636">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-637">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="dc61d-637">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="dc61d-638">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-638">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-639">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dc61d-639">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-640">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="dc61d-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-641">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-642">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dc61d-642">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-643">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc61d-643">Name of the scoping system.</span></span>

<span data-ttu-id="dc61d-644">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-644">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc61d-645">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="dc61d-645">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc61d-646">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="dc61d-646">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc61d-647">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="dc61d-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc61d-648">上次重設此控制器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="dc61d-648">Date and time this controller was last reset.</span></span> <span data-ttu-id="dc61d-649">這可能表示控制器關閉或重新初始化。</span><span class="sxs-lookup"><span data-stu-id="dc61d-649">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="dc61d-650">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-650">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc61d-651">備註</span><span class="sxs-lookup"><span data-stu-id="dc61d-651">Remarks</span></span>

<span data-ttu-id="dc61d-652">**Win32 \_ SerialPort** 類別衍生自 [**CIM \_ SerialController**](cim-serialcontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="dc61d-652">The **Win32\_SerialPort** class is derived from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dc61d-653">範例</span><span class="sxs-lookup"><span data-stu-id="dc61d-653">Examples</span></span>

<span data-ttu-id="dc61d-654">如需從登錄) 抓取序列埠資訊 (的替代方法，請參閱 [列舉埠](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic 範例。</span><span class="sxs-lookup"><span data-stu-id="dc61d-654">For an alternate method of retrieving serial port information (from the registry), see the [Enumerate Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic sample.</span></span>

<span data-ttu-id="dc61d-655">[列出序列埠屬性](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12)PowerShell 範例會傳回電腦上所安裝之序列埠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dc61d-655">The [List Serial Port Properties](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) PowerShell example returns information about the serial ports installed on a computer.</span></span>

<span data-ttu-id="dc61d-656">下列 VBScript 範例會傳回電腦上所安裝之序列埠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dc61d-656">The following VBScript sample returns information about the serial ports installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SerialPort") 
 
For Each objItem in colItems 
    Wscript.Echo "Binary: " & objItem.Binary 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Maximum Baud Rate: " & objItem.MaxBaudRate 
    Wscript.Echo "Maximum Input Buffer Size: " & objItem.MaximumInputBufferSize 
    Wscript.Echo "Maximum Output Buffer Size: " & _ 
        objItem.MaximumOutputBufferSize 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "OS Auto Discovered: " & objItem.OSAutoDiscovered 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Provider Type: " & objItem.ProviderType 
    Wscript.Echo "Settable Baud Rate: " & objItem.SettableBaudRate 
    Wscript.Echo "Settable Data Bits: " & objItem.SettableDataBits 
    Wscript.Echo "Settable Flow Control: " & objItem.SettableFlowControl 
    Wscript.Echo "Settable Parity: " & objItem.SettableParity 
    Wscript.Echo "Settable Parity Check: " & objItem.SettableParityCheck 
    Wscript.Echo "Settable RLSD: " & objItem.SettableRLSD 
    Wscript.Echo "Settable Stop Bits: " & objItem.SettableStopBits 
    Wscript.Echo "Supports 16-Bit Mode: " & objItem.Supports16BitMode 
    Wscript.Echo "Supports DTRDSR: " & objItem.SupportsDTRDSR 
    Wscript.Echo "Supports Elapsed Timeouts: " & _ 
        objItem.SupportsElapsedTimeouts 
    Wscript.Echo "Supports Int Timeouts: " & objItem.SupportsIntTimeouts 
    Wscript.Echo "Supports Parity Check: " & objItem.SupportsParityCheck 
    Wscript.Echo "Supports RLSD: " & objItem.SupportsRLSD 
    Wscript.Echo "Supports RTSCTS: " & objItem.SupportsRTSCTS 
    Wscript.Echo "Supports Special Characters: " & _ 
        objItem.SupportsSpecialCharacters 
    Wscript.Echo "Supports XOn XOff: " & objItem.SupportsXOnXOff 
    Wscript.Echo "Supports XOn XOff Setting: " & objItem.SupportsXOnXOffSet 
Next
```



## <a name="requirements"></a><span data-ttu-id="dc61d-657">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc61d-657">Requirements</span></span>



| <span data-ttu-id="dc61d-658">需求</span><span class="sxs-lookup"><span data-stu-id="dc61d-658">Requirement</span></span> | <span data-ttu-id="dc61d-659">值</span><span class="sxs-lookup"><span data-stu-id="dc61d-659">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc61d-660">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc61d-660">Minimum supported client</span></span><br/> | <span data-ttu-id="dc61d-661">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc61d-661">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc61d-662">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc61d-662">Minimum supported server</span></span><br/> | <span data-ttu-id="dc61d-663">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc61d-663">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc61d-664">命名空間</span><span class="sxs-lookup"><span data-stu-id="dc61d-664">Namespace</span></span><br/>                | <span data-ttu-id="dc61d-665">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dc61d-665">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc61d-666">MOF</span><span class="sxs-lookup"><span data-stu-id="dc61d-666">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc61d-667"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc61d-667"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc61d-668">DLL</span><span class="sxs-lookup"><span data-stu-id="dc61d-668">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc61d-669"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc61d-669"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc61d-670">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc61d-670">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc61d-671">**CIM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="dc61d-671">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="dc61d-672">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="dc61d-672">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
