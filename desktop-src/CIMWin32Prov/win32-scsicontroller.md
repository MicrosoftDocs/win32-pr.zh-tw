---
description: Win32 \_ MICROSOFT.HYPERV.POWERSHELL.SCSICONTROLLER WMI 類別代表執行 Windows 的電腦系統上的 SCSI 控制器。
ms.assetid: 14ed523e-d505-40fa-81d5-3a71eb9f078e
ms.tgt_platform: multiple
title: Win32_SCSIController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIController
- Win32_SCSIController.Reset
- Win32_SCSIController.SetPowerState
- Win32_SCSIController.Availability
- Win32_SCSIController.Caption
- Win32_SCSIController.ConfigManagerErrorCode
- Win32_SCSIController.ConfigManagerUserConfig
- Win32_SCSIController.ControllerTimeouts
- Win32_SCSIController.CreationClassName
- Win32_SCSIController.Description
- Win32_SCSIController.DeviceID
- Win32_SCSIController.DeviceMap
- Win32_SCSIController.DriverName
- Win32_SCSIController.ErrorCleared
- Win32_SCSIController.ErrorDescription
- Win32_SCSIController.HardwareVersion
- Win32_SCSIController.Index
- Win32_SCSIController.InstallDate
- Win32_SCSIController.LastErrorCode
- Win32_SCSIController.Manufacturer
- Win32_SCSIController.MaxDataWidth
- Win32_SCSIController.MaxNumberControlled
- Win32_SCSIController.MaxTransferRate
- Win32_SCSIController.Name
- Win32_SCSIController.PNPDeviceID
- Win32_SCSIController.PowerManagementCapabilities
- Win32_SCSIController.PowerManagementSupported
- Win32_SCSIController.ProtectionManagement
- Win32_SCSIController.ProtocolSupported
- Win32_SCSIController.Status
- Win32_SCSIController.StatusInfo
- Win32_SCSIController.SystemCreationClassName
- Win32_SCSIController.SystemName
- Win32_SCSIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f8ba77d626ada787ed18fd9855333fa813f3ab7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970345"
---
# <a name="win32_scsicontroller-class"></a><span data-ttu-id="c6564-103">Win32 \_ microsoft.hyperv.powershell.scsicontroller 類別</span><span class="sxs-lookup"><span data-stu-id="c6564-103">Win32\_SCSIController class</span></span>

<span data-ttu-id="c6564-104">**Win32 \_ microsoft.hyperv.powershell.scsicontroller** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 的電腦系統上的 SCSI 控制器。</span><span class="sxs-lookup"><span data-stu-id="c6564-104">The **Win32\_SCSIController** [WMI class](../wmisdk/retrieving-a-class.md) represents a SCSI controller on a computer system running Windows.</span></span>

<span data-ttu-id="c6564-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c6564-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c6564-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c6564-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6564-107">語法</span><span class="sxs-lookup"><span data-stu-id="c6564-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SCSIController : CIM_SCSIController
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  uint32   ControllerTimeouts;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  string   DeviceMap;
  string   DriverName;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareVersion;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MaxDataWidth;
  uint32   MaxNumberControlled;
  uint64   MaxTransferRate;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtectionManagement;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="c6564-108">成員</span><span class="sxs-lookup"><span data-stu-id="c6564-108">Members</span></span>

<span data-ttu-id="c6564-109">**Win32 \_ microsoft.hyperv.powershell.scsicontroller** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c6564-109">The **Win32\_SCSIController** class has these types of members:</span></span>

-   [<span data-ttu-id="c6564-110">方法</span><span class="sxs-lookup"><span data-stu-id="c6564-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c6564-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c6564-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c6564-112">方法</span><span class="sxs-lookup"><span data-stu-id="c6564-112">Methods</span></span>

<span data-ttu-id="c6564-113">**Win32 \_ microsoft.hyperv.powershell.scsicontroller** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c6564-113">The **Win32\_SCSIController** class has these methods.</span></span>



| <span data-ttu-id="c6564-114">方法</span><span class="sxs-lookup"><span data-stu-id="c6564-114">Method</span></span>            | <span data-ttu-id="c6564-115">描述</span><span class="sxs-lookup"><span data-stu-id="c6564-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6564-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="c6564-116">**Reset**</span></span>         | <span data-ttu-id="c6564-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="c6564-117">Not implemented.</span></span> <span data-ttu-id="c6564-118">若要執行此方法，請參閱 [**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="c6564-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/>                 |
| <span data-ttu-id="c6564-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c6564-119">**SetPowerState**</span></span> | <span data-ttu-id="c6564-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="c6564-120">Not implemented.</span></span> <span data-ttu-id="c6564-121">若要執行此方法，請參閱 [**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="c6564-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c6564-122">屬性</span><span class="sxs-lookup"><span data-stu-id="c6564-122">Properties</span></span>

<span data-ttu-id="c6564-123">**Win32 \_ microsoft.hyperv.powershell.scsicontroller** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c6564-123">The **Win32\_SCSIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6564-124">**可用性**</span><span class="sxs-lookup"><span data-stu-id="c6564-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c6564-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-127">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="c6564-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-128">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="c6564-128">Availability and status of the device.</span></span>

<span data-ttu-id="c6564-129">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c6564-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c6564-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6564-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c6564-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c6564-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="c6564-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-133">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="c6564-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c6564-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="c6564-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c6564-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="c6564-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c6564-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="c6564-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c6564-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="c6564-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c6564-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="c6564-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c6564-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="c6564-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c6564-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="c6564-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c6564-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="c6564-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c6564-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="c6564-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c6564-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="c6564-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-144">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="c6564-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c6564-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="c6564-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-146">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="c6564-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c6564-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="c6564-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-148">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="c6564-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c6564-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="c6564-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c6564-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="c6564-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-151">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="c6564-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c6564-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="c6564-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-153">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="c6564-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c6564-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="c6564-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-155">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="c6564-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c6564-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="c6564-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-157">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="c6564-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c6564-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="c6564-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-159">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="c6564-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c6564-160">**標題**</span><span class="sxs-lookup"><span data-stu-id="c6564-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-163">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-164">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="c6564-164">Short description of the object.</span></span>

<span data-ttu-id="c6564-165">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c6564-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-167">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c6564-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-169">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-170">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c6564-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c6564-171">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c6564-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="c6564-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c6564-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="c6564-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-174">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="c6564-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c6564-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c6564-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c6564-176">(1)</span><span class="sxs-lookup"><span data-stu-id="c6564-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-177">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="c6564-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c6564-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c6564-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c6564-179">(2)</span><span class="sxs-lookup"><span data-stu-id="c6564-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c6564-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="c6564-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c6564-181">(3)</span><span class="sxs-lookup"><span data-stu-id="c6564-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-182">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="c6564-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c6564-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c6564-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c6564-184">(4)</span><span class="sxs-lookup"><span data-stu-id="c6564-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-185">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c6564-185">Device is not working properly.</span></span> <span data-ttu-id="c6564-186">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="c6564-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c6564-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="c6564-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c6564-188">(5)</span><span class="sxs-lookup"><span data-stu-id="c6564-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-189">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="c6564-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c6564-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="c6564-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c6564-191">(6)</span><span class="sxs-lookup"><span data-stu-id="c6564-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-192">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="c6564-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c6564-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="c6564-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c6564-194">(7)</span><span class="sxs-lookup"><span data-stu-id="c6564-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c6564-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="c6564-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c6564-196">(8)</span><span class="sxs-lookup"><span data-stu-id="c6564-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-197">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="c6564-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c6564-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c6564-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c6564-199">(9)</span><span class="sxs-lookup"><span data-stu-id="c6564-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-200">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c6564-200">Device is not working properly.</span></span> <span data-ttu-id="c6564-201">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="c6564-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c6564-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="c6564-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c6564-203">(10)</span><span class="sxs-lookup"><span data-stu-id="c6564-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-204">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="c6564-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c6564-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="c6564-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c6564-206">(11)</span><span class="sxs-lookup"><span data-stu-id="c6564-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-207">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="c6564-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c6564-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="c6564-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c6564-209"> (12) </span><span class="sxs-lookup"><span data-stu-id="c6564-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-210">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="c6564-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c6564-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c6564-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c6564-212">(13)</span><span class="sxs-lookup"><span data-stu-id="c6564-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-213">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="c6564-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c6564-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="c6564-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c6564-215">(14)</span><span class="sxs-lookup"><span data-stu-id="c6564-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-216">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c6564-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c6564-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="c6564-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c6564-218">(15)</span><span class="sxs-lookup"><span data-stu-id="c6564-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-219">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c6564-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c6564-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="c6564-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c6564-221">(16)</span><span class="sxs-lookup"><span data-stu-id="c6564-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-222">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="c6564-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c6564-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="c6564-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c6564-224">(17)</span><span class="sxs-lookup"><span data-stu-id="c6564-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-225">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="c6564-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c6564-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c6564-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c6564-227">(18)</span><span class="sxs-lookup"><span data-stu-id="c6564-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-228">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c6564-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c6564-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="c6564-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c6564-230">(19)</span><span class="sxs-lookup"><span data-stu-id="c6564-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c6564-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c6564-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c6564-232">(20)</span><span class="sxs-lookup"><span data-stu-id="c6564-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-233">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="c6564-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c6564-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c6564-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c6564-235">(21)</span><span class="sxs-lookup"><span data-stu-id="c6564-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-236">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="c6564-236">System failure.</span></span> <span data-ttu-id="c6564-237">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="c6564-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c6564-238">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="c6564-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c6564-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="c6564-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c6564-240">(22)</span><span class="sxs-lookup"><span data-stu-id="c6564-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-241">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="c6564-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c6564-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="c6564-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c6564-243">(23)</span><span class="sxs-lookup"><span data-stu-id="c6564-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-244">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="c6564-244">System failure.</span></span> <span data-ttu-id="c6564-245">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="c6564-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c6564-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c6564-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c6564-247">(24)</span><span class="sxs-lookup"><span data-stu-id="c6564-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-248">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="c6564-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c6564-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c6564-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c6564-250">(25)</span><span class="sxs-lookup"><span data-stu-id="c6564-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-251">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="c6564-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c6564-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c6564-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c6564-253">(26)</span><span class="sxs-lookup"><span data-stu-id="c6564-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-254">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="c6564-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c6564-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="c6564-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c6564-256">(27)</span><span class="sxs-lookup"><span data-stu-id="c6564-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-257">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="c6564-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c6564-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c6564-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c6564-259">(28)</span><span class="sxs-lookup"><span data-stu-id="c6564-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-260">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c6564-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c6564-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="c6564-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c6564-262">(29)</span><span class="sxs-lookup"><span data-stu-id="c6564-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-263">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="c6564-263">Device is disabled.</span></span> <span data-ttu-id="c6564-264">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="c6564-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c6564-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="c6564-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c6564-266">(30)</span><span class="sxs-lookup"><span data-stu-id="c6564-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-267">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="c6564-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c6564-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c6564-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c6564-269"> (31) </span><span class="sxs-lookup"><span data-stu-id="c6564-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-270">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c6564-270">Device is not working properly.</span></span> <span data-ttu-id="c6564-271">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c6564-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c6564-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c6564-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-273">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c6564-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-275">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-276">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="c6564-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c6564-277">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-278">**ControllerTimeouts**</span><span class="sxs-lookup"><span data-stu-id="c6564-278">**ControllerTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-279">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c6564-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6564-281">**TimeOfLastReset** 值之後發生的超時時間。</span><span class="sxs-lookup"><span data-stu-id="c6564-281">Number of time-outs that have occurred after the **TimeOfLastReset** value.</span></span>

<span data-ttu-id="c6564-282">這個屬性繼承自 [**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-282">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c6564-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-284">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-286">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c6564-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c6564-287">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="c6564-287">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c6564-288">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="c6564-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c6564-289">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-290">**說明**</span><span class="sxs-lookup"><span data-stu-id="c6564-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-291">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-293">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-294">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c6564-294">Description of the object.</span></span>

<span data-ttu-id="c6564-295">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c6564-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-299">限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| 硬體 \\ \\ DeviceMap \\ \\ Scsi" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-300">具有系統上其他裝置之 SCSI 控制器的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6564-300">Unique identifier of the SCSI controller with other devices on the system.</span></span>

<span data-ttu-id="c6564-301">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-302">**DeviceMap**</span><span class="sxs-lookup"><span data-stu-id="c6564-302">**DeviceMap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-305">限定詞：已 [**淘汰**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| 硬體 \\ \\ DeviceMap \\ \\ Scsi \| ScsiPort" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-305">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-306">此 SCSI 控制器列出裝置的順序。</span><span class="sxs-lookup"><span data-stu-id="c6564-306">Order in which the devices are listed with this SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="c6564-307">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="c6564-307">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-308">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-310">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| PortDriver" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|PortDriver")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-311">SCSI 控制器的驅動程式檔案名。</span><span class="sxs-lookup"><span data-stu-id="c6564-311">Driver file name of the SCSI controller.</span></span>

<span data-ttu-id="c6564-312">範例： "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="c6564-312">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="c6564-313">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c6564-313">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-314">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c6564-314">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6564-316">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="c6564-316">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="c6564-317">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-318">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c6564-318">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6564-321">自由格式字串提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c6564-321">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="c6564-322">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-323">**HardwareVersion**</span><span class="sxs-lookup"><span data-stu-id="c6564-323">**HardwareVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-326">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Enum \\ \\ Root \| HWRevision" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|HWRevision")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-327">SCSI 控制器的硬體版本號碼。</span><span class="sxs-lookup"><span data-stu-id="c6564-327">Hardware version number of the SCSI controller.</span></span>

<span data-ttu-id="c6564-328">範例： "1.25"</span><span class="sxs-lookup"><span data-stu-id="c6564-328">Example: "1.25"</span></span>

</dd> <dt>

<span data-ttu-id="c6564-329">**Index**</span><span class="sxs-lookup"><span data-stu-id="c6564-329">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-330">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c6564-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-332">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| 硬體 \\ \\ DeviceMap \\ \\ Scsi \| ScsiPort" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-333">系統登錄中 SCSI 控制器的索引編號。</span><span class="sxs-lookup"><span data-stu-id="c6564-333">Index number of the SCSI controller in the system registry.</span></span>

<span data-ttu-id="c6564-334">範例：0</span><span class="sxs-lookup"><span data-stu-id="c6564-334">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="c6564-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c6564-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-336">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c6564-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-338">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="c6564-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-339">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c6564-339">Date and time the object was installed.</span></span> <span data-ttu-id="c6564-340">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="c6564-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c6564-341">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c6564-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-343">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c6564-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6564-345">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c6564-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c6564-346">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-347">**製造商**</span><span class="sxs-lookup"><span data-stu-id="c6564-347">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-348">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-350">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Enum \\ \\ Root \| 製造業" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-351">SCSI 控制器製造商的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6564-351">Name of the SCSI controller manufacturer.</span></span>

<span data-ttu-id="c6564-352">範例： "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="c6564-352">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="c6564-353">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="c6564-353">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-354">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c6564-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-356">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-356">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-357">SCSI 控制器支援的最大資料寬度 () 位。</span><span class="sxs-lookup"><span data-stu-id="c6564-357">Maximum data width (in bits) supported by the SCSI controller.</span></span>

<span data-ttu-id="c6564-358">這個屬性繼承自 [**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-358">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-359">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="c6564-359">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-360">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c6564-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-362">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="c6564-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-363">此控制器可支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="c6564-363">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="c6564-364">值為 0 (零) 如果數位未知，則應使用此值。</span><span class="sxs-lookup"><span data-stu-id="c6564-364">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="c6564-365">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-365">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-366">**MaxTransferRate**</span><span class="sxs-lookup"><span data-stu-id="c6564-366">**MaxTransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-367">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c6564-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-369">限定詞： [**單位**](../wmisdk/standard-qualifiers.md) ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-369">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-370">SCSI 控制器支援的最大傳輸速率 (每秒位數) 。</span><span class="sxs-lookup"><span data-stu-id="c6564-370">Maximum transfer rate (in bits per second) supported by the SCSI controller.</span></span>

<span data-ttu-id="c6564-371">這個屬性繼承自 [**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-371">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<span data-ttu-id="c6564-372">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-373">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c6564-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-376">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-377">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="c6564-377">Label by which the object is known.</span></span> <span data-ttu-id="c6564-378">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="c6564-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c6564-379">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c6564-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-381">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-382">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-383">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-383">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-384">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6564-384">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c6564-385">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c6564-386">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c6564-386">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c6564-387">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c6564-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-388">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c6564-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c6564-389">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6564-390">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="c6564-390">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c6564-391">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="c6564-391">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6564-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c6564-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c6564-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="c6564-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c6564-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="c6564-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c6564-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c6564-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-396">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="c6564-396">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c6564-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="c6564-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-398">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="c6564-398">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c6564-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="c6564-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-400">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c6564-400">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c6564-401">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="c6564-401">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c6564-402">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-402">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c6564-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="c6564-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-404">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="c6564-404">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c6564-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="c6564-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c6564-406">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="c6564-406">Timed Power-On Supported</span></span>

<span data-ttu-id="c6564-407">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="c6564-407">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c6564-408">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c6564-408">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-409">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c6564-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6564-411">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="c6564-411">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="c6564-412">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="c6564-412">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c6564-413">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-414">**ProtectionManagement**</span><span class="sxs-lookup"><span data-stu-id="c6564-414">**ProtectionManagement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-415">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c6564-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-417">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 儲存控制器 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="c6564-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Controller\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-418">支援 SCSI 控制器以提供冗余或防止裝置故障。</span><span class="sxs-lookup"><span data-stu-id="c6564-418">Support of the SCSI controller for redundancy or protection against device failures.</span></span>

<span data-ttu-id="c6564-419">這個屬性繼承自 [**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-419">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c6564-420">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c6564-420">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6564-421">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c6564-421">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>

<span data-ttu-id="c6564-422">未 **受保護** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="c6564-422">**Unprotected** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>

<span data-ttu-id="c6564-423">**Protected** (4) </span><span class="sxs-lookup"><span data-stu-id="c6564-423">**Protected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="c6564-424">**透過 SCC (的 SCSI-3 控制器命令)** (5) 進行保護</span><span class="sxs-lookup"><span data-stu-id="c6564-424">**Protected through SCC (SCSI-3 Controller Command)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="c6564-425">**透過 SCC-2 (的 SCSI-3 控制器命令來保護)** (6) </span><span class="sxs-lookup"><span data-stu-id="c6564-425">**Protected through SCC-2 (SCSI-3 Controller Command)** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c6564-426">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="c6564-426">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-427">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c6564-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-429">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="c6564-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-430">控制器用來存取「受控制」裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c6564-430">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="c6564-431">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-431">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="c6564-432">下列清單顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="c6564-432">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c6564-433">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c6564-433">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6564-434">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c6564-434">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="c6564-435">**EISA** (3) </span><span class="sxs-lookup"><span data-stu-id="c6564-435">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="c6564-436">**ISA** (4) </span><span class="sxs-lookup"><span data-stu-id="c6564-436">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="c6564-437">**PCI** (5) </span><span class="sxs-lookup"><span data-stu-id="c6564-437">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="c6564-438">**ATA/ATAPI** (6) </span><span class="sxs-lookup"><span data-stu-id="c6564-438">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="c6564-439">**彈性磁片** (7) </span><span class="sxs-lookup"><span data-stu-id="c6564-439">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="c6564-440">**1496** (8) </span><span class="sxs-lookup"><span data-stu-id="c6564-440">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="c6564-441">**SCSI 平行介面** (9) </span><span class="sxs-lookup"><span data-stu-id="c6564-441">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="c6564-442">**SCSI 光纖通道通訊協定** (10) </span><span class="sxs-lookup"><span data-stu-id="c6564-442">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="c6564-443">**SCSI 序列匯流排通訊協定** (11) </span><span class="sxs-lookup"><span data-stu-id="c6564-443">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="c6564-444">**SCSI 序列匯流排通訊協定-2 (1394)** (12) </span><span class="sxs-lookup"><span data-stu-id="c6564-444">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="c6564-445">**SCSI 序列儲存架構** (13) </span><span class="sxs-lookup"><span data-stu-id="c6564-445">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="c6564-446">**VESA** (14) </span><span class="sxs-lookup"><span data-stu-id="c6564-446">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="c6564-447">**PCMCIA** (15) </span><span class="sxs-lookup"><span data-stu-id="c6564-447">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="c6564-448">**通用序列匯流排** (16) </span><span class="sxs-lookup"><span data-stu-id="c6564-448">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="c6564-449">**平行通訊協定** (17) </span><span class="sxs-lookup"><span data-stu-id="c6564-449">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="c6564-450">**ESCON** (18) </span><span class="sxs-lookup"><span data-stu-id="c6564-450">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="c6564-451">**診斷** (19) </span><span class="sxs-lookup"><span data-stu-id="c6564-451">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="c6564-452">**I2C** (20) </span><span class="sxs-lookup"><span data-stu-id="c6564-452">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="c6564-453">**Power** (21) </span><span class="sxs-lookup"><span data-stu-id="c6564-453">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="c6564-454">**HIPPI** (22) </span><span class="sxs-lookup"><span data-stu-id="c6564-454">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="c6564-455">**MultiBus** (23) </span><span class="sxs-lookup"><span data-stu-id="c6564-455">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="c6564-456">**Vm** (24) </span><span class="sxs-lookup"><span data-stu-id="c6564-456">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="c6564-457">**IPI** (25) </span><span class="sxs-lookup"><span data-stu-id="c6564-457">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="c6564-458">**IEEE-488** (26) </span><span class="sxs-lookup"><span data-stu-id="c6564-458">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="c6564-459">**RS232** (27) </span><span class="sxs-lookup"><span data-stu-id="c6564-459">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="c6564-460">**IEEE 802.3 10BASE5** (28) </span><span class="sxs-lookup"><span data-stu-id="c6564-460">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="c6564-461">**IEEE 802.3 10BASE2** (29) </span><span class="sxs-lookup"><span data-stu-id="c6564-461">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="c6564-462">**IEEE 802.3 1BASE5** (30) </span><span class="sxs-lookup"><span data-stu-id="c6564-462">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="c6564-463">**IEEE 802.3 10BROAD36** (31) </span><span class="sxs-lookup"><span data-stu-id="c6564-463">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="c6564-464">**IEEE 802.3 100BASEVG** (32) </span><span class="sxs-lookup"><span data-stu-id="c6564-464">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="c6564-465">**IEEE 802.5 權杖-環形** (33) </span><span class="sxs-lookup"><span data-stu-id="c6564-465">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="c6564-466">**ANSI x3t 9.5 FDDI** (34) </span><span class="sxs-lookup"><span data-stu-id="c6564-466">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="c6564-467">**MCA** (35) </span><span class="sxs-lookup"><span data-stu-id="c6564-467">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="c6564-468">**ESDI** (36) </span><span class="sxs-lookup"><span data-stu-id="c6564-468">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="c6564-469">**IDE** (37) </span><span class="sxs-lookup"><span data-stu-id="c6564-469">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="c6564-470">**CMD** (38) </span><span class="sxs-lookup"><span data-stu-id="c6564-470">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="c6564-471">**ST506** (39) </span><span class="sxs-lookup"><span data-stu-id="c6564-471">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="c6564-472">**」 Dssi 小組** (40) </span><span class="sxs-lookup"><span data-stu-id="c6564-472">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="c6564-473">**QIC2** (41) </span><span class="sxs-lookup"><span data-stu-id="c6564-473">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="c6564-474">**增強型 ATA/IDE** (42) </span><span class="sxs-lookup"><span data-stu-id="c6564-474">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="c6564-475">**AGP** (43) </span><span class="sxs-lookup"><span data-stu-id="c6564-475">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="c6564-476">**TWIRP (雙向紅外線)** (44) </span><span class="sxs-lookup"><span data-stu-id="c6564-476">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="c6564-477">**(快速紅外線)** (45) 的杉樹</span><span class="sxs-lookup"><span data-stu-id="c6564-477">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="c6564-478">**SIR (串列紅外線)** (46) </span><span class="sxs-lookup"><span data-stu-id="c6564-478">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="c6564-479">**IrBus** (47) </span><span class="sxs-lookup"><span data-stu-id="c6564-479">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c6564-480">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c6564-480">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-481">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-483">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-483">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-484">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c6564-484">Current status of the object.</span></span> <span data-ttu-id="c6564-485">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="c6564-485">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c6564-486">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="c6564-486">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c6564-487">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="c6564-487">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c6564-488">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="c6564-488">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c6564-489">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="c6564-489">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c6564-490">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-490">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c6564-491">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="c6564-491">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c6564-492">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="c6564-492">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c6564-493">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-493">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c6564-494">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-494">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6564-495">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-495">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c6564-496">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-496">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c6564-497">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-497">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c6564-498">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-498">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c6564-499">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-499">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c6564-500">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-500">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c6564-501">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="c6564-501">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c6564-502">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-502">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c6564-503">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="c6564-503">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c6564-504">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c6564-504">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-505">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c6564-505">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-506">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-507">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="c6564-507">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c6564-508">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="c6564-508">State of the logical device.</span></span> <span data-ttu-id="c6564-509">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="c6564-509">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c6564-510">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c6564-511">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c6564-511">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c6564-512">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c6564-512">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c6564-513">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c6564-513">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c6564-514">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="c6564-514">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c6564-515">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="c6564-515">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c6564-516">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c6564-516">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-517">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-518">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-518">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-519">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c6564-519">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c6564-520">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c6564-520">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="c6564-521">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-522">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c6564-522">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-523">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c6564-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6564-525">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c6564-525">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c6564-526">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6564-526">Name of the scoping system.</span></span>

<span data-ttu-id="c6564-527">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6564-528">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="c6564-528">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6564-529">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c6564-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c6564-530">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c6564-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6564-531">上次重設此控制器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c6564-531">Date and time this controller was last reset.</span></span> <span data-ttu-id="c6564-532">這可能表示控制器關閉或重新初始化。</span><span class="sxs-lookup"><span data-stu-id="c6564-532">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="c6564-533">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-533">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6564-534">備註</span><span class="sxs-lookup"><span data-stu-id="c6564-534">Remarks</span></span>

<span data-ttu-id="c6564-535">**Win32 \_ microsoft.hyperv.powershell.scsicontroller** 類別衍生自 [**CIM \_ microsoft.hyperv.powershell.scsicontroller**](cim-scsicontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="c6564-535">The **Win32\_SCSIController** class is derived from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6564-536">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6564-536">Requirements</span></span>



| <span data-ttu-id="c6564-537">需求</span><span class="sxs-lookup"><span data-stu-id="c6564-537">Requirement</span></span> | <span data-ttu-id="c6564-538">值</span><span class="sxs-lookup"><span data-stu-id="c6564-538">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6564-539">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6564-539">Minimum supported client</span></span><br/> | <span data-ttu-id="c6564-540">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6564-540">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6564-541">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6564-541">Minimum supported server</span></span><br/> | <span data-ttu-id="c6564-542">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6564-542">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6564-543">命名空間</span><span class="sxs-lookup"><span data-stu-id="c6564-543">Namespace</span></span><br/>                | <span data-ttu-id="c6564-544">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c6564-544">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6564-545">MOF</span><span class="sxs-lookup"><span data-stu-id="c6564-545">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6564-546"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6564-546"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6564-547">DLL</span><span class="sxs-lookup"><span data-stu-id="c6564-547">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6564-548"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6564-548"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6564-549">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6564-549">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6564-550">**CIM \_ microsoft.hyperv.powershell.scsicontroller**</span><span class="sxs-lookup"><span data-stu-id="c6564-550">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dt>

[<span data-ttu-id="c6564-551">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="c6564-551">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
