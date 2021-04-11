---
description: CIM \_ PointingDevice 類別代表指向顯示區域的裝置。 任何操作指標的裝置，或指向視覺效果顯示器上的區域，都是此類別的成員。 例如，滑鼠、手寫筆、觸控板或平板電腦。
ms.assetid: b093134a-534a-4680-8fce-d96baff26139
ms.tgt_platform: multiple
title: 'CIM_PointingDevice 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.Availability
- CIM_PointingDevice.Caption
- CIM_PointingDevice.ConfigManagerErrorCode
- CIM_PointingDevice.ConfigManagerUserConfig
- CIM_PointingDevice.CreationClassName
- CIM_PointingDevice.Description
- CIM_PointingDevice.DeviceID
- CIM_PointingDevice.ErrorCleared
- CIM_PointingDevice.ErrorDescription
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.InstallDate
- CIM_PointingDevice.IsLocked
- CIM_PointingDevice.LastErrorCode
- CIM_PointingDevice.Name
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.PNPDeviceID
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.PowerManagementCapabilities
- CIM_PointingDevice.PowerManagementSupported
- CIM_PointingDevice.Resolution
- CIM_PointingDevice.Status
- CIM_PointingDevice.StatusInfo
- CIM_PointingDevice.SystemCreationClassName
- CIM_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3f0a52ac11d927f5cabf171f49fee3a5febaa6a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190996"
---
# <a name="cim_pointingdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="64c06-105">CIM_PointingDevice 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="64c06-105">CIM_PointingDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="64c06-106">**CIM \_ PointingDevice** 類別代表指向顯示區域的裝置。</span><span class="sxs-lookup"><span data-stu-id="64c06-106">The **CIM\_PointingDevice** class represents a device that points to regions on the display.</span></span> <span data-ttu-id="64c06-107">任何操作指標的裝置，或指向視覺效果顯示器上的區域，都是此類別的成員。</span><span class="sxs-lookup"><span data-stu-id="64c06-107">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="64c06-108">例如，滑鼠、手寫筆、觸控板或平板電腦。</span><span class="sxs-lookup"><span data-stu-id="64c06-108">For example, a mouse, stylus, touch pad, or tablet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64c06-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="64c06-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="64c06-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="64c06-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="64c06-111">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="64c06-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="64c06-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="64c06-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c06-113">語法</span><span class="sxs-lookup"><span data-stu-id="64c06-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C535-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Handedness;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="64c06-114">成員</span><span class="sxs-lookup"><span data-stu-id="64c06-114">Members</span></span>

<span data-ttu-id="64c06-115">**CIM \_ PointingDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="64c06-115">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="64c06-116">方法</span><span class="sxs-lookup"><span data-stu-id="64c06-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="64c06-117">屬性</span><span class="sxs-lookup"><span data-stu-id="64c06-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="64c06-118">方法</span><span class="sxs-lookup"><span data-stu-id="64c06-118">Methods</span></span>

<span data-ttu-id="64c06-119">**CIM \_ PointingDevice** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="64c06-119">The **CIM\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="64c06-120">方法</span><span class="sxs-lookup"><span data-stu-id="64c06-120">Method</span></span>                                                                    | <span data-ttu-id="64c06-121">描述</span><span class="sxs-lookup"><span data-stu-id="64c06-121">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64c06-122">**重設**</span><span class="sxs-lookup"><span data-stu-id="64c06-122">**Reset**</span></span>](reset-method-in-class-cim-pointingdevice.md)                 | <span data-ttu-id="64c06-123">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="64c06-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="64c06-124">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="64c06-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="64c06-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="64c06-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pointingdevice.md) | <span data-ttu-id="64c06-126">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="64c06-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="64c06-127">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="64c06-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="64c06-128">屬性</span><span class="sxs-lookup"><span data-stu-id="64c06-128">Properties</span></span>

<span data-ttu-id="64c06-129">**CIM \_ PointingDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="64c06-129">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64c06-130">**可用性**</span><span class="sxs-lookup"><span data-stu-id="64c06-130">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c06-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-133">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="64c06-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-134">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="64c06-134">Availability and status of the device.</span></span>

<span data-ttu-id="64c06-135">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-135">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="64c06-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="64c06-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="64c06-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="64c06-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="64c06-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="64c06-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="64c06-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="64c06-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="64c06-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="64c06-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="64c06-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="64c06-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="64c06-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="64c06-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="64c06-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="64c06-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="64c06-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="64c06-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="64c06-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="64c06-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="64c06-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="64c06-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="64c06-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="64c06-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="64c06-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="64c06-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-149">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="64c06-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="64c06-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="64c06-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-151">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="64c06-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="64c06-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="64c06-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-153">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="64c06-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="64c06-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="64c06-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="64c06-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="64c06-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-156">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="64c06-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="64c06-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="64c06-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-158">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="64c06-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="64c06-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="64c06-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-160">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="64c06-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="64c06-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="64c06-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-162">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="64c06-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="64c06-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="64c06-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-164">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="64c06-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="64c06-165">**標題**</span><span class="sxs-lookup"><span data-stu-id="64c06-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-168">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="64c06-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-169">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="64c06-169">Short textual description of the object.</span></span>

<span data-ttu-id="64c06-170">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="64c06-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-172">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64c06-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-174">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="64c06-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-175">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="64c06-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="64c06-176">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="64c06-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="64c06-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="64c06-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="64c06-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-179">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="64c06-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="64c06-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="64c06-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="64c06-181">(1)</span><span class="sxs-lookup"><span data-stu-id="64c06-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-182">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="64c06-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="64c06-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="64c06-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="64c06-184">(2)</span><span class="sxs-lookup"><span data-stu-id="64c06-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="64c06-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="64c06-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="64c06-186">(3)</span><span class="sxs-lookup"><span data-stu-id="64c06-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-187">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="64c06-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="64c06-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="64c06-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="64c06-189">(4)</span><span class="sxs-lookup"><span data-stu-id="64c06-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-190">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="64c06-190">Device is not working properly.</span></span> <span data-ttu-id="64c06-191">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="64c06-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="64c06-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="64c06-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="64c06-193">(5)</span><span class="sxs-lookup"><span data-stu-id="64c06-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-194">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="64c06-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="64c06-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="64c06-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="64c06-196">(6)</span><span class="sxs-lookup"><span data-stu-id="64c06-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-197">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="64c06-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="64c06-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="64c06-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="64c06-199">(7)</span><span class="sxs-lookup"><span data-stu-id="64c06-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="64c06-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="64c06-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="64c06-201">(8)</span><span class="sxs-lookup"><span data-stu-id="64c06-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-202">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="64c06-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="64c06-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="64c06-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="64c06-204">(9)</span><span class="sxs-lookup"><span data-stu-id="64c06-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-205">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="64c06-205">Device is not working properly.</span></span> <span data-ttu-id="64c06-206">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="64c06-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="64c06-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="64c06-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="64c06-208">(10)</span><span class="sxs-lookup"><span data-stu-id="64c06-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-209">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="64c06-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="64c06-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="64c06-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="64c06-211">(11)</span><span class="sxs-lookup"><span data-stu-id="64c06-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-212">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="64c06-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="64c06-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="64c06-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="64c06-214"> (12) </span><span class="sxs-lookup"><span data-stu-id="64c06-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-215">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="64c06-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="64c06-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="64c06-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="64c06-217">(13)</span><span class="sxs-lookup"><span data-stu-id="64c06-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-218">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="64c06-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="64c06-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="64c06-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="64c06-220">(14)</span><span class="sxs-lookup"><span data-stu-id="64c06-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-221">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="64c06-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="64c06-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="64c06-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="64c06-223">(15)</span><span class="sxs-lookup"><span data-stu-id="64c06-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-224">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="64c06-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="64c06-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="64c06-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="64c06-226">(16)</span><span class="sxs-lookup"><span data-stu-id="64c06-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-227">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="64c06-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="64c06-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="64c06-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="64c06-229">(17)</span><span class="sxs-lookup"><span data-stu-id="64c06-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-230">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="64c06-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="64c06-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="64c06-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="64c06-232">(18)</span><span class="sxs-lookup"><span data-stu-id="64c06-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-233">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="64c06-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="64c06-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="64c06-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="64c06-235">(19)</span><span class="sxs-lookup"><span data-stu-id="64c06-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="64c06-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="64c06-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="64c06-237">(20)</span><span class="sxs-lookup"><span data-stu-id="64c06-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-238">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="64c06-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="64c06-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="64c06-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="64c06-240">(21)</span><span class="sxs-lookup"><span data-stu-id="64c06-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-241">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="64c06-241">System failure.</span></span> <span data-ttu-id="64c06-242">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="64c06-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="64c06-243">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="64c06-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="64c06-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="64c06-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="64c06-245">(22)</span><span class="sxs-lookup"><span data-stu-id="64c06-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-246">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="64c06-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="64c06-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="64c06-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="64c06-248">(23)</span><span class="sxs-lookup"><span data-stu-id="64c06-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-249">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="64c06-249">System failure.</span></span> <span data-ttu-id="64c06-250">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="64c06-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="64c06-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="64c06-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="64c06-252">(24)</span><span class="sxs-lookup"><span data-stu-id="64c06-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-253">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="64c06-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="64c06-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="64c06-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="64c06-255">(25)</span><span class="sxs-lookup"><span data-stu-id="64c06-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-256">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="64c06-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="64c06-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="64c06-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="64c06-258">(26)</span><span class="sxs-lookup"><span data-stu-id="64c06-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-259">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="64c06-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="64c06-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="64c06-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="64c06-261">(27)</span><span class="sxs-lookup"><span data-stu-id="64c06-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-262">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="64c06-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="64c06-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="64c06-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="64c06-264">(28)</span><span class="sxs-lookup"><span data-stu-id="64c06-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-265">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="64c06-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="64c06-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="64c06-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="64c06-267">(29)</span><span class="sxs-lookup"><span data-stu-id="64c06-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-268">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="64c06-268">Device is disabled.</span></span> <span data-ttu-id="64c06-269">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="64c06-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="64c06-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="64c06-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="64c06-271">(30)</span><span class="sxs-lookup"><span data-stu-id="64c06-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-272">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="64c06-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="64c06-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="64c06-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="64c06-274"> (31) </span><span class="sxs-lookup"><span data-stu-id="64c06-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-275">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="64c06-275">Device is not working properly.</span></span> <span data-ttu-id="64c06-276">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="64c06-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="64c06-277">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="64c06-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-278">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="64c06-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-280">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="64c06-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-281">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="64c06-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="64c06-282">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="64c06-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-284">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-286">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="64c06-286">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="64c06-287">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="64c06-287">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="64c06-288">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="64c06-288">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="64c06-289">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-290">**說明**</span><span class="sxs-lookup"><span data-stu-id="64c06-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-291">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-293">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="64c06-293">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-294">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="64c06-294">Textual description of the object.</span></span>

<span data-ttu-id="64c06-295">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="64c06-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-299">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="64c06-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="64c06-300">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="64c06-300">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="64c06-301">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-302">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="64c06-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-303">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="64c06-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c06-305">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="64c06-305">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="64c06-306">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="64c06-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-308">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c06-310">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="64c06-310">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="64c06-311">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-312">**Handedness**</span><span class="sxs-lookup"><span data-stu-id="64c06-312">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-313">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c06-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c06-315">設定右手邊或左邊操作的指標裝置。</span><span class="sxs-lookup"><span data-stu-id="64c06-315">Configuration of the pointing device for right-hand or left-hand operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="64c06-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="64c06-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="64c06-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (1) </span><span class="sxs-lookup"><span data-stu-id="64c06-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="64c06-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**右手操作** (2) </span><span class="sxs-lookup"><span data-stu-id="64c06-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-319">右手邊操作</span><span class="sxs-lookup"><span data-stu-id="64c06-319">Right-hand operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="64c06-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>左手 **操作** (3) </span><span class="sxs-lookup"><span data-stu-id="64c06-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-321">左方操作</span><span class="sxs-lookup"><span data-stu-id="64c06-321">Left-hand operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="64c06-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="64c06-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-323">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="64c06-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-325">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="64c06-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-326">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="64c06-326">Date and time the object was installed.</span></span> <span data-ttu-id="64c06-327">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="64c06-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="64c06-328">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-329">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="64c06-329">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-330">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="64c06-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c06-332">若 **為 TRUE**，則會鎖定裝置，防止使用者輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="64c06-332">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="64c06-333">這個屬性繼承自 [**CIM \_ UserDevice**](cim-userdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-333">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="64c06-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-335">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64c06-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c06-337">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="64c06-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="64c06-338">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-339">**名稱**</span><span class="sxs-lookup"><span data-stu-id="64c06-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-342">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="64c06-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-343">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="64c06-343">Label by which the object is known.</span></span> <span data-ttu-id="64c06-344">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="64c06-344">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="64c06-345">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-345">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-346">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="64c06-346">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-347">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="64c06-347">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c06-349">指標裝置上的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="64c06-349">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="64c06-350">範例： "2"</span><span class="sxs-lookup"><span data-stu-id="64c06-350">Example: "2"</span></span>

</dd> <dt>

<span data-ttu-id="64c06-351">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="64c06-351">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-354">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="64c06-354">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-355">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="64c06-355">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="64c06-356">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="64c06-357">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="64c06-357">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="64c06-358">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="64c06-358">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-359">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c06-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-361">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 指標裝置 \| 001.1」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-361">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-362">指標裝置的類型。</span><span class="sxs-lookup"><span data-stu-id="64c06-362">Type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="64c06-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="64c06-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="64c06-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="64c06-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="64c06-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**滑鼠** (3) </span><span class="sxs-lookup"><span data-stu-id="64c06-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="64c06-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**追蹤球** (4) </span><span class="sxs-lookup"><span data-stu-id="64c06-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-367">跟蹤</span><span class="sxs-lookup"><span data-stu-id="64c06-367">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="64c06-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**追蹤點** (5) </span><span class="sxs-lookup"><span data-stu-id="64c06-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="64c06-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**滑行點** (6) </span><span class="sxs-lookup"><span data-stu-id="64c06-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="64c06-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**觸控板** (7) </span><span class="sxs-lookup"><span data-stu-id="64c06-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="64c06-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**觸控式螢幕** (8) </span><span class="sxs-lookup"><span data-stu-id="64c06-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="64c06-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**滑鼠-光學感應器** (9) </span><span class="sxs-lookup"><span data-stu-id="64c06-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-373">滑鼠光學感應器</span><span class="sxs-lookup"><span data-stu-id="64c06-373">Mouse   optical sensor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="64c06-374">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="64c06-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-375">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="64c06-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="64c06-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c06-377">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="64c06-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="64c06-378">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="64c06-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="64c06-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="64c06-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="64c06-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="64c06-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="64c06-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="64c06-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="64c06-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="64c06-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-383">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="64c06-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="64c06-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="64c06-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-385">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="64c06-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="64c06-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="64c06-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-387">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="64c06-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="64c06-388">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="64c06-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="64c06-389">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="64c06-389">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="64c06-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="64c06-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-391">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="64c06-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="64c06-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="64c06-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="64c06-393">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="64c06-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="64c06-394">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="64c06-394">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-395">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="64c06-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64c06-397">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="64c06-397">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="64c06-398">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="64c06-398">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="64c06-399">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="64c06-399">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="64c06-400">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="64c06-400">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="64c06-401">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-402">**解決方法**</span><span class="sxs-lookup"><span data-stu-id="64c06-402">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-403">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="64c06-403">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-405">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每英寸計數」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-405">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-406">追蹤解析。</span><span class="sxs-lookup"><span data-stu-id="64c06-406">Tracking resolution.</span></span>

<span data-ttu-id="64c06-407">範例： "0"</span><span class="sxs-lookup"><span data-stu-id="64c06-407">Example: "0"</span></span>

</dd> <dt>

<span data-ttu-id="64c06-408">**狀態**</span><span class="sxs-lookup"><span data-stu-id="64c06-408">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-409">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-411">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="64c06-411">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-412">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="64c06-412">Current status of the object.</span></span> <span data-ttu-id="64c06-413">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="64c06-414">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="64c06-414">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="64c06-415">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="64c06-415">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="64c06-416">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-416">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="64c06-417">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-417">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="64c06-418">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-418">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="64c06-419">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-419">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="64c06-420">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-420">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="64c06-421">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-421">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="64c06-422">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-422">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="64c06-423">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-423">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="64c06-424">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="64c06-424">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="64c06-425">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-425">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="64c06-426">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="64c06-426">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="64c06-427">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="64c06-427">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-428">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="64c06-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-430">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="64c06-430">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="64c06-431">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="64c06-431">State of the logical device.</span></span> <span data-ttu-id="64c06-432">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="64c06-432">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="64c06-433">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-433">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="64c06-434">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="64c06-434">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="64c06-435">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="64c06-435">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="64c06-436">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="64c06-436">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="64c06-437">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="64c06-437">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="64c06-438">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="64c06-438">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="64c06-439">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="64c06-439">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-440">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-442">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="64c06-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="64c06-443">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="64c06-443">Scoping system's creation class name.</span></span>

<span data-ttu-id="64c06-444">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c06-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="64c06-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64c06-446">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="64c06-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64c06-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="64c06-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64c06-448">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="64c06-448">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="64c06-449">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="64c06-449">Scoping system's name.</span></span>

<span data-ttu-id="64c06-450">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64c06-451">備註</span><span class="sxs-lookup"><span data-stu-id="64c06-451">Remarks</span></span>

<span data-ttu-id="64c06-452">**Cim \_ PointingDevice** 類別衍生自 [**cim \_ UserDevice**](cim-userdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-452">The **CIM\_PointingDevice** class is derived from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

<span data-ttu-id="64c06-453">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="64c06-453">WMI does not implement this class.</span></span> <span data-ttu-id="64c06-454">針對衍生自 **CIM \_ POINTINGDEVICE** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="64c06-454">For WMI classes derived from **CIM\_PointingDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="64c06-455">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="64c06-455">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="64c06-456">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="64c06-456">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="64c06-457">規格需求</span><span class="sxs-lookup"><span data-stu-id="64c06-457">Requirements</span></span>



| <span data-ttu-id="64c06-458">需求</span><span class="sxs-lookup"><span data-stu-id="64c06-458">Requirement</span></span> | <span data-ttu-id="64c06-459">值</span><span class="sxs-lookup"><span data-stu-id="64c06-459">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64c06-460">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64c06-460">Minimum supported client</span></span><br/> | <span data-ttu-id="64c06-461">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64c06-461">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64c06-462">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64c06-462">Minimum supported server</span></span><br/> | <span data-ttu-id="64c06-463">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64c06-463">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64c06-464">命名空間</span><span class="sxs-lookup"><span data-stu-id="64c06-464">Namespace</span></span><br/>                | <span data-ttu-id="64c06-465">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="64c06-465">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64c06-466">MOF</span><span class="sxs-lookup"><span data-stu-id="64c06-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64c06-467"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="64c06-467"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64c06-468">DLL</span><span class="sxs-lookup"><span data-stu-id="64c06-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64c06-469"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64c06-469"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64c06-470">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64c06-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c06-471">**CIM \_ UserDevice**</span><span class="sxs-lookup"><span data-stu-id="64c06-471">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

