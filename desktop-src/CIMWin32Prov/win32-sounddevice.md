---
description: 代表執行 Windows 的電腦系統上的音效裝置內容。
ms.assetid: 5471ffe9-60a3-466f-a608-e6268ba73c2b
ms.tgt_platform: multiple
title: Win32_SoundDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SoundDevice
- Win32_SoundDevice.Reset
- Win32_SoundDevice.SetPowerState
- Win32_SoundDevice.Availability
- Win32_SoundDevice.Caption
- Win32_SoundDevice.ConfigManagerErrorCode
- Win32_SoundDevice.ConfigManagerUserConfig
- Win32_SoundDevice.CreationClassName
- Win32_SoundDevice.Description
- Win32_SoundDevice.DeviceID
- Win32_SoundDevice.DMABufferSize
- Win32_SoundDevice.ErrorCleared
- Win32_SoundDevice.ErrorDescription
- Win32_SoundDevice.InstallDate
- Win32_SoundDevice.LastErrorCode
- Win32_SoundDevice.Manufacturer
- Win32_SoundDevice.MPU401Address
- Win32_SoundDevice.Name
- Win32_SoundDevice.PNPDeviceID
- Win32_SoundDevice.PowerManagementCapabilities
- Win32_SoundDevice.PowerManagementSupported
- Win32_SoundDevice.ProductName
- Win32_SoundDevice.Status
- Win32_SoundDevice.StatusInfo
- Win32_SoundDevice.SystemCreationClassName
- Win32_SoundDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73e0ef7cbc71872d26f75311b6d72ac48bbfae8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111484"
---
# <a name="win32_sounddevice-class"></a><span data-ttu-id="49247-103">Win32 \_ SoundDevice 類別</span><span class="sxs-lookup"><span data-stu-id="49247-103">Win32\_SoundDevice class</span></span>

<span data-ttu-id="49247-104">**Win32 \_ SoundDevice** [WMI 類別](../wmisdk/retrieving-a-class.md)代表在執行 Windows 的電腦系統上，聲音裝置的屬性。</span><span class="sxs-lookup"><span data-stu-id="49247-104">The **Win32\_SoundDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a sound device on a computer system running Windows.</span></span>

<span data-ttu-id="49247-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="49247-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="49247-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="49247-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49247-107">語法</span><span class="sxs-lookup"><span data-stu-id="49247-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SoundDevice : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DMABufferSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MPU401Address;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="49247-108">成員</span><span class="sxs-lookup"><span data-stu-id="49247-108">Members</span></span>

<span data-ttu-id="49247-109">**Win32 \_ SoundDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="49247-109">The **Win32\_SoundDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="49247-110">方法</span><span class="sxs-lookup"><span data-stu-id="49247-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="49247-111">屬性</span><span class="sxs-lookup"><span data-stu-id="49247-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="49247-112">方法</span><span class="sxs-lookup"><span data-stu-id="49247-112">Methods</span></span>

<span data-ttu-id="49247-113">**Win32 \_ SoundDevice** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="49247-113">The **Win32\_SoundDevice** class has these methods.</span></span>



| <span data-ttu-id="49247-114">方法</span><span class="sxs-lookup"><span data-stu-id="49247-114">Method</span></span>            | <span data-ttu-id="49247-115">描述</span><span class="sxs-lookup"><span data-stu-id="49247-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49247-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="49247-116">**Reset**</span></span>         | <span data-ttu-id="49247-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="49247-117">Not implemented.</span></span> <span data-ttu-id="49247-118">若要執行此方法，請參閱 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="49247-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="49247-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="49247-119">**SetPowerState**</span></span> | <span data-ttu-id="49247-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="49247-120">Not implemented.</span></span> <span data-ttu-id="49247-121">若要執行此方法，請參閱 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="49247-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="49247-122">屬性</span><span class="sxs-lookup"><span data-stu-id="49247-122">Properties</span></span>

<span data-ttu-id="49247-123">**Win32 \_ SoundDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="49247-123">The **Win32\_SoundDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49247-124">**可用性**</span><span class="sxs-lookup"><span data-stu-id="49247-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="49247-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49247-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-127">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="49247-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="49247-128">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="49247-128">Availability and status of the device.</span></span>

<span data-ttu-id="49247-129">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="49247-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="49247-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49247-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="49247-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="49247-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="49247-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="49247-133">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="49247-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="49247-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="49247-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="49247-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="49247-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="49247-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="49247-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="49247-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="49247-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="49247-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="49247-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="49247-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="49247-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="49247-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="49247-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="49247-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="49247-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="49247-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="49247-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="49247-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="49247-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="49247-144">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="49247-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="49247-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="49247-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="49247-146">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="49247-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="49247-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="49247-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="49247-148">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="49247-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="49247-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="49247-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="49247-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="49247-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="49247-151">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="49247-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="49247-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="49247-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="49247-153">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="49247-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="49247-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="49247-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="49247-155">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="49247-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="49247-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="49247-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="49247-157">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="49247-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="49247-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="49247-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="49247-159">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="49247-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="49247-160">**標題**</span><span class="sxs-lookup"><span data-stu-id="49247-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-163">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="49247-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="49247-164">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="49247-164">Short description of the object.</span></span>

<span data-ttu-id="49247-165">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="49247-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-167">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="49247-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49247-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-169">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="49247-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="49247-170">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="49247-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="49247-171">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="49247-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="49247-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="49247-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="49247-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="49247-174">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="49247-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="49247-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="49247-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="49247-176">(1)</span><span class="sxs-lookup"><span data-stu-id="49247-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="49247-177">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="49247-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="49247-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="49247-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="49247-179">(2)</span><span class="sxs-lookup"><span data-stu-id="49247-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="49247-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="49247-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="49247-181">(3)</span><span class="sxs-lookup"><span data-stu-id="49247-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="49247-182">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="49247-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="49247-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="49247-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="49247-184">(4)</span><span class="sxs-lookup"><span data-stu-id="49247-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="49247-185">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="49247-185">Device is not working properly.</span></span> <span data-ttu-id="49247-186">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="49247-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="49247-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="49247-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="49247-188">(5)</span><span class="sxs-lookup"><span data-stu-id="49247-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="49247-189">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="49247-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="49247-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="49247-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="49247-191">(6)</span><span class="sxs-lookup"><span data-stu-id="49247-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="49247-192">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="49247-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="49247-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="49247-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="49247-194">(7)</span><span class="sxs-lookup"><span data-stu-id="49247-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="49247-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="49247-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="49247-196">(8)</span><span class="sxs-lookup"><span data-stu-id="49247-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="49247-197">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="49247-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="49247-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="49247-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="49247-199">(9)</span><span class="sxs-lookup"><span data-stu-id="49247-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="49247-200">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="49247-200">Device is not working properly.</span></span> <span data-ttu-id="49247-201">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="49247-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="49247-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="49247-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="49247-203">(10)</span><span class="sxs-lookup"><span data-stu-id="49247-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="49247-204">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="49247-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="49247-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="49247-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="49247-206">(11)</span><span class="sxs-lookup"><span data-stu-id="49247-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="49247-207">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="49247-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="49247-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="49247-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="49247-209"> (12) </span><span class="sxs-lookup"><span data-stu-id="49247-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="49247-210">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="49247-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="49247-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="49247-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="49247-212">(13)</span><span class="sxs-lookup"><span data-stu-id="49247-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="49247-213">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="49247-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="49247-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="49247-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="49247-215">(14)</span><span class="sxs-lookup"><span data-stu-id="49247-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="49247-216">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="49247-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="49247-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="49247-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="49247-218">(15)</span><span class="sxs-lookup"><span data-stu-id="49247-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="49247-219">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="49247-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="49247-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="49247-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="49247-221">(16)</span><span class="sxs-lookup"><span data-stu-id="49247-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="49247-222">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="49247-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="49247-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="49247-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="49247-224">(17)</span><span class="sxs-lookup"><span data-stu-id="49247-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="49247-225">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="49247-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="49247-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="49247-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="49247-227">(18)</span><span class="sxs-lookup"><span data-stu-id="49247-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="49247-228">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="49247-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="49247-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="49247-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="49247-230">(19)</span><span class="sxs-lookup"><span data-stu-id="49247-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="49247-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="49247-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="49247-232">(20)</span><span class="sxs-lookup"><span data-stu-id="49247-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="49247-233">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="49247-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="49247-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="49247-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="49247-235">(21)</span><span class="sxs-lookup"><span data-stu-id="49247-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="49247-236">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="49247-236">System failure.</span></span> <span data-ttu-id="49247-237">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="49247-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="49247-238">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="49247-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="49247-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="49247-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="49247-240">(22)</span><span class="sxs-lookup"><span data-stu-id="49247-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="49247-241">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="49247-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="49247-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="49247-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="49247-243">(23)</span><span class="sxs-lookup"><span data-stu-id="49247-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="49247-244">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="49247-244">System failure.</span></span> <span data-ttu-id="49247-245">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="49247-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="49247-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="49247-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="49247-247">(24)</span><span class="sxs-lookup"><span data-stu-id="49247-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="49247-248">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="49247-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="49247-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="49247-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="49247-250">(25)</span><span class="sxs-lookup"><span data-stu-id="49247-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="49247-251">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="49247-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="49247-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="49247-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="49247-253">(26)</span><span class="sxs-lookup"><span data-stu-id="49247-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="49247-254">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="49247-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="49247-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="49247-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="49247-256">(27)</span><span class="sxs-lookup"><span data-stu-id="49247-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="49247-257">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="49247-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="49247-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="49247-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="49247-259">(28)</span><span class="sxs-lookup"><span data-stu-id="49247-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="49247-260">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="49247-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="49247-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="49247-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="49247-262">(29)</span><span class="sxs-lookup"><span data-stu-id="49247-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="49247-263">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="49247-263">Device is disabled.</span></span> <span data-ttu-id="49247-264">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="49247-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="49247-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="49247-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="49247-266">(30)</span><span class="sxs-lookup"><span data-stu-id="49247-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="49247-267">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="49247-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="49247-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="49247-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="49247-269"> (31) </span><span class="sxs-lookup"><span data-stu-id="49247-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="49247-270">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="49247-270">Device is not working properly.</span></span> <span data-ttu-id="49247-271">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="49247-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="49247-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="49247-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-273">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="49247-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49247-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-275">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="49247-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="49247-276">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="49247-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="49247-277">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="49247-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-281">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="49247-281">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="49247-282">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="49247-282">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="49247-283">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="49247-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="49247-284">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-285">**說明**</span><span class="sxs-lookup"><span data-stu-id="49247-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-288">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="49247-288">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="49247-289">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="49247-289">Description of the object.</span></span>

<span data-ttu-id="49247-290">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="49247-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-294">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "DeviceId" ) ， [**Key**](../wmisdk/key-qualifier.md)， [**MaxLen**](../wmisdk/standard-qualifiers.md) (260) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ control \\ \\ MediaResources \\ \\ wave \| DeviceId" ) </span><span class="sxs-lookup"><span data-stu-id="49247-294">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\wave\|DeviceID")</span></span>
</dt> </dl>

<span data-ttu-id="49247-295">聲音裝置的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="49247-295">Unique identifier of the sound device.</span></span>

<span data-ttu-id="49247-296">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-297">**DMABufferSize**</span><span class="sxs-lookup"><span data-stu-id="49247-297">**DMABufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-298">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="49247-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49247-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-300">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="49247-300">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="49247-301">直接記憶體存取緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="49247-301">Size of the Direct Memory Access buffer.</span></span>

<span data-ttu-id="49247-302">範例: 4</span><span class="sxs-lookup"><span data-stu-id="49247-302">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="49247-303">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="49247-303">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-304">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="49247-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49247-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49247-306">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="49247-306">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="49247-307">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-308">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="49247-308">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49247-311">自由格式字串提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="49247-311">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="49247-312">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="49247-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-314">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="49247-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49247-315">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-316">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="49247-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="49247-317">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="49247-317">Date and time the object was installed.</span></span> <span data-ttu-id="49247-318">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="49247-318">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="49247-319">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-320">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="49247-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-321">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="49247-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49247-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49247-323">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="49247-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="49247-324">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-325">**製造商**</span><span class="sxs-lookup"><span data-stu-id="49247-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-326">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-328">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="49247-328">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="49247-329">聲音裝置的製造商。</span><span class="sxs-lookup"><span data-stu-id="49247-329">Manufacturer of the sound device.</span></span>

<span data-ttu-id="49247-330">範例：「創意實驗室」</span><span class="sxs-lookup"><span data-stu-id="49247-330">Example: "Creative Labs"</span></span>

</dd> <dt>

<span data-ttu-id="49247-331">**MPU401Address**</span><span class="sxs-lookup"><span data-stu-id="49247-331">**MPU401Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-332">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="49247-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49247-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-334">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="49247-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="49247-335">指派給音效裝置 MPU-401 埠的開始 i/o 位址。</span><span class="sxs-lookup"><span data-stu-id="49247-335">Starting I/O address assigned to the MPU-401 port of the sound device.</span></span>

<span data-ttu-id="49247-336">範例：300</span><span class="sxs-lookup"><span data-stu-id="49247-336">Example: 300</span></span>

</dd> <dt>

<span data-ttu-id="49247-337">**名稱**</span><span class="sxs-lookup"><span data-stu-id="49247-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-338">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-340">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="49247-340">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="49247-341">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="49247-341">Label by which the object is known.</span></span> <span data-ttu-id="49247-342">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="49247-342">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="49247-343">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="49247-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-345">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-347">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="49247-347">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="49247-348">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="49247-348">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="49247-349">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="49247-350">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="49247-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="49247-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="49247-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-352">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="49247-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="49247-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49247-354">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="49247-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="49247-355">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="49247-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49247-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="49247-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="49247-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="49247-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="49247-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="49247-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="49247-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="49247-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="49247-360">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="49247-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="49247-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="49247-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="49247-362">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="49247-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="49247-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="49247-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="49247-364">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="49247-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="49247-365">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="49247-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="49247-366">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-366">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="49247-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="49247-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="49247-368">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="49247-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="49247-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="49247-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="49247-370">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="49247-370">Timed Power-On Supported</span></span>

<span data-ttu-id="49247-371">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="49247-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="49247-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="49247-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-373">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="49247-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49247-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49247-375">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="49247-375">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="49247-376">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="49247-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="49247-377">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-378">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="49247-378">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-379">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-381">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 多媒體結構 \| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) \| szPname" ) </span><span class="sxs-lookup"><span data-stu-id="49247-381">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Multimedia Structures\|[**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)\|szPname")</span></span>
</dt> </dl>

<span data-ttu-id="49247-382">聲音裝置的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="49247-382">Product name of the sound device.</span></span>

<span data-ttu-id="49247-383">範例： "創意 Labs SoundBlaster AWE64PNP"</span><span class="sxs-lookup"><span data-stu-id="49247-383">Example: "Creative Labs SoundBlaster AWE64PNP"</span></span>

</dd> <dt>

<span data-ttu-id="49247-384">**狀態**</span><span class="sxs-lookup"><span data-stu-id="49247-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-385">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-386">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-387">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="49247-387">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="49247-388">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="49247-388">Current status of the object.</span></span> <span data-ttu-id="49247-389">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="49247-389">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="49247-390">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="49247-390">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="49247-391">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="49247-391">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="49247-392">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="49247-392">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="49247-393">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="49247-393">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="49247-394">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-394">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="49247-395">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="49247-395">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="49247-396">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="49247-396">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="49247-397">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-397">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="49247-398">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-398">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49247-399">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-399">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="49247-400">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-400">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="49247-401">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-401">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="49247-402">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-402">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="49247-403">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-403">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="49247-404">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-404">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="49247-405">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="49247-405">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="49247-406">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-406">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="49247-407">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="49247-407">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="49247-408">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="49247-408">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-409">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="49247-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="49247-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-411">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="49247-411">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="49247-412">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="49247-412">State of the logical device.</span></span> <span data-ttu-id="49247-413">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="49247-413">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="49247-414">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="49247-415">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="49247-415">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49247-416">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="49247-416">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="49247-417">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="49247-417">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="49247-418">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="49247-418">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="49247-419">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="49247-419">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="49247-420">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="49247-420">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-423">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="49247-423">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="49247-424">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="49247-424">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="49247-425">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="49247-426">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="49247-426">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49247-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="49247-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49247-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="49247-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49247-429">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="49247-429">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="49247-430">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="49247-430">Name of the scoping system.</span></span>

<span data-ttu-id="49247-431">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49247-432">備註</span><span class="sxs-lookup"><span data-stu-id="49247-432">Remarks</span></span>

<span data-ttu-id="49247-433">**Win32 \_ SoundDevice** 類別衍生自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="49247-433">The **Win32\_SoundDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="49247-434">範例</span><span class="sxs-lookup"><span data-stu-id="49247-434">Examples</span></span>

<span data-ttu-id="49247-435">[清單音效卡屬性](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a)PowerShell 範例會抓取電腦上所安裝之所有音效卡的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="49247-435">The [List Sound Card Properties](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a) PowerShell sample retrieves information about all the sound cards installed in a computer.</span></span>

<span data-ttu-id="49247-436">下列 VBScript 範例會抓取電腦上所安裝之所有音效卡的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="49247-436">The following VBScript sample retrieves information about all the sound cards installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SoundDevice") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "DMA Buffer Size: " & objItem.DMABufferSize 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "MPU 401 Address: " & objItem.MPU401Address 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Product Name: " & objItem.ProductName 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="49247-437">規格需求</span><span class="sxs-lookup"><span data-stu-id="49247-437">Requirements</span></span>



| <span data-ttu-id="49247-438">需求</span><span class="sxs-lookup"><span data-stu-id="49247-438">Requirement</span></span> | <span data-ttu-id="49247-439">值</span><span class="sxs-lookup"><span data-stu-id="49247-439">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49247-440">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49247-440">Minimum supported client</span></span><br/> | <span data-ttu-id="49247-441">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49247-441">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49247-442">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49247-442">Minimum supported server</span></span><br/> | <span data-ttu-id="49247-443">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49247-443">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49247-444">命名空間</span><span class="sxs-lookup"><span data-stu-id="49247-444">Namespace</span></span><br/>                | <span data-ttu-id="49247-445">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="49247-445">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49247-446">MOF</span><span class="sxs-lookup"><span data-stu-id="49247-446">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49247-447"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="49247-447"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49247-448">DLL</span><span class="sxs-lookup"><span data-stu-id="49247-448">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49247-449"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49247-449"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49247-450">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49247-450">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49247-451">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="49247-451">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="49247-452">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="49247-452">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
