---
description: CIM \_ AlarmDevice 類別是一種警示裝置，可發出與問題狀況相關的聲音或可見指示。
ms.assetid: 1f64aea4-d0a4-480b-9802-e2c21e71c754
ms.tgt_platform: multiple
title: CIM_AlarmDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice
- CIM_AlarmDevice.Caption
- CIM_AlarmDevice.Description
- CIM_AlarmDevice.InstallDate
- CIM_AlarmDevice.Name
- CIM_AlarmDevice.Status
- CIM_AlarmDevice.Availability
- CIM_AlarmDevice.ConfigManagerErrorCode
- CIM_AlarmDevice.ConfigManagerUserConfig
- CIM_AlarmDevice.CreationClassName
- CIM_AlarmDevice.DeviceID
- CIM_AlarmDevice.PowerManagementCapabilities
- CIM_AlarmDevice.ErrorCleared
- CIM_AlarmDevice.ErrorDescription
- CIM_AlarmDevice.LastErrorCode
- CIM_AlarmDevice.PNPDeviceID
- CIM_AlarmDevice.PowerManagementSupported
- CIM_AlarmDevice.StatusInfo
- CIM_AlarmDevice.SystemCreationClassName
- CIM_AlarmDevice.SystemName
- CIM_AlarmDevice.AudibleAlarm
- CIM_AlarmDevice.Urgency
- CIM_AlarmDevice.VisibleAlarm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 622a6031f36140e23514b925835cebae84b35025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510635"
---
# <a name="cim_alarmdevice-class"></a><span data-ttu-id="1ca68-103">CIM \_ AlarmDevice 類別</span><span class="sxs-lookup"><span data-stu-id="1ca68-103">CIM\_AlarmDevice class</span></span>

<span data-ttu-id="1ca68-104">**CIM \_ AlarmDevice** 類別是一種警示裝置，可發出與問題狀況相關的聲音或可見指示。</span><span class="sxs-lookup"><span data-stu-id="1ca68-104">The **CIM\_AlarmDevice** class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

<span data-ttu-id="1ca68-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ca68-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1ca68-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1ca68-106">Properties are listed in alphabetic order, not MOF order.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ca68-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1ca68-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1ca68-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1ca68-109">語法</span><span class="sxs-lookup"><span data-stu-id="1ca68-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B66-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AlarmDevice : CIM_LogicalDevice
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
  boolean  AudibleAlarm;
  uint16   Urgency;
  boolean  VisibleAlarm;
};
```

## <a name="members"></a><span data-ttu-id="1ca68-110">成員</span><span class="sxs-lookup"><span data-stu-id="1ca68-110">Members</span></span>

<span data-ttu-id="1ca68-111">**CIM \_ AlarmDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1ca68-111">The **CIM\_AlarmDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="1ca68-112">方法</span><span class="sxs-lookup"><span data-stu-id="1ca68-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1ca68-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1ca68-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1ca68-114">方法</span><span class="sxs-lookup"><span data-stu-id="1ca68-114">Methods</span></span>

<span data-ttu-id="1ca68-115">**CIM \_ AlarmDevice** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1ca68-115">The **CIM\_AlarmDevice** class has these methods.</span></span>



| <span data-ttu-id="1ca68-116">方法</span><span class="sxs-lookup"><span data-stu-id="1ca68-116">Method</span></span>                                                                 | <span data-ttu-id="1ca68-117">描述</span><span class="sxs-lookup"><span data-stu-id="1ca68-117">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ca68-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="1ca68-118">**Reset**</span></span>](reset-method-in-class-cim-alarmdevice.md)                 | <span data-ttu-id="1ca68-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="1ca68-119">Requests a logical device reset.</span></span> <span data-ttu-id="1ca68-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1ca68-120">Not implemented by WMI.</span></span><br/>                                                                     |
| [<span data-ttu-id="1ca68-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1ca68-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-alarmdevice.md) | <span data-ttu-id="1ca68-122">設定邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="1ca68-122">Sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="1ca68-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1ca68-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="1ca68-124">**SetUrgency**</span><span class="sxs-lookup"><span data-stu-id="1ca68-124">**SetUrgency**</span></span>](seturgency-method-in-class-cim-alarmdevice.md)       | <span data-ttu-id="1ca68-125">設定警示所需的緊急程度等級。</span><span class="sxs-lookup"><span data-stu-id="1ca68-125">Sets the desired urgency level for the alarm.</span></span> <span data-ttu-id="1ca68-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1ca68-126">Not implemented by WMI.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="1ca68-127">屬性</span><span class="sxs-lookup"><span data-stu-id="1ca68-127">Properties</span></span>

<span data-ttu-id="1ca68-128">**CIM \_ AlarmDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1ca68-128">The **CIM\_AlarmDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ca68-129">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="1ca68-129">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-130">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ca68-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-132">若 **為 TRUE**，則會聽見警示。</span><span class="sxs-lookup"><span data-stu-id="1ca68-132">If **TRUE**, the alarm is audible.</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-133">**可用性**</span><span class="sxs-lookup"><span data-stu-id="1ca68-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ca68-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-136">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="1ca68-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-137">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="1ca68-137">Availability and status of the device.</span></span>

<span data-ttu-id="1ca68-138">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1ca68-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1ca68-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1ca68-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="1ca68-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1ca68-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="1ca68-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1ca68-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="1ca68-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1ca68-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="1ca68-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1ca68-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="1ca68-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1ca68-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="1ca68-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1ca68-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="1ca68-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1ca68-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="1ca68-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1ca68-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="1ca68-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1ca68-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="1ca68-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1ca68-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="1ca68-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1ca68-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="1ca68-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-152">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="1ca68-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1ca68-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="1ca68-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-154">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="1ca68-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1ca68-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="1ca68-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-156">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="1ca68-156">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1ca68-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="1ca68-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1ca68-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="1ca68-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-159">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="1ca68-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1ca68-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="1ca68-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-161">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="1ca68-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1ca68-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="1ca68-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-163">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="1ca68-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1ca68-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="1ca68-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-165">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="1ca68-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1ca68-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="1ca68-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-167">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="1ca68-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1ca68-168">**標題**</span><span class="sxs-lookup"><span data-stu-id="1ca68-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-169">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-171">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-172">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="1ca68-172">A short textual description of the object.</span></span>

<span data-ttu-id="1ca68-173">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1ca68-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-175">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1ca68-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-177">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-178">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1ca68-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="1ca68-179">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1ca68-180">**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-180">**This device is working properly.**</span></span> <span data-ttu-id="1ca68-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="1ca68-181">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1ca68-182">**這個裝置並未正確設定。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-182">**This device is not configured correctly.**</span></span> <span data-ttu-id="1ca68-183">(1)</span><span class="sxs-lookup"><span data-stu-id="1ca68-183">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1ca68-184">**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-184">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1ca68-185">(2)</span><span class="sxs-lookup"><span data-stu-id="1ca68-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1ca68-186">**這個裝置的驅動程式可能已損毀，或您系統的記憶體或其他資源可能不足。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-186">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1ca68-187">(3)</span><span class="sxs-lookup"><span data-stu-id="1ca68-187">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1ca68-188">**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-188">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1ca68-189">(4)</span><span class="sxs-lookup"><span data-stu-id="1ca68-189">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1ca68-190">**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-190">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1ca68-191">(5)</span><span class="sxs-lookup"><span data-stu-id="1ca68-191">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1ca68-192">**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-192">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1ca68-193">(6)</span><span class="sxs-lookup"><span data-stu-id="1ca68-193">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1ca68-194">**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-194">**Cannot filter.**</span></span> <span data-ttu-id="1ca68-195">(7)</span><span class="sxs-lookup"><span data-stu-id="1ca68-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1ca68-196">**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-196">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1ca68-197">(8)</span><span class="sxs-lookup"><span data-stu-id="1ca68-197">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1ca68-198">**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-198">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1ca68-199">(9)</span><span class="sxs-lookup"><span data-stu-id="1ca68-199">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1ca68-200">**這個裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-200">**This device cannot start.**</span></span> <span data-ttu-id="1ca68-201">(10)</span><span class="sxs-lookup"><span data-stu-id="1ca68-201">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1ca68-202">**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-202">**This device failed.**</span></span> <span data-ttu-id="1ca68-203">(11)</span><span class="sxs-lookup"><span data-stu-id="1ca68-203">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1ca68-204">**這個裝置沒有足夠資源可供使用。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-204">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1ca68-205"> (12) </span><span class="sxs-lookup"><span data-stu-id="1ca68-205">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1ca68-206">**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-206">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1ca68-207">(13)</span><span class="sxs-lookup"><span data-stu-id="1ca68-207">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1ca68-208">**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-208">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1ca68-209">(14)</span><span class="sxs-lookup"><span data-stu-id="1ca68-209">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1ca68-210">**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-210">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1ca68-211">(15)</span><span class="sxs-lookup"><span data-stu-id="1ca68-211">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1ca68-212">**Windows 無法識別這個裝置所使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-212">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1ca68-213">(16)</span><span class="sxs-lookup"><span data-stu-id="1ca68-213">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1ca68-214">**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-214">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1ca68-215">(17)</span><span class="sxs-lookup"><span data-stu-id="1ca68-215">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1ca68-216">**重新安裝這個裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-216">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1ca68-217">(18)</span><span class="sxs-lookup"><span data-stu-id="1ca68-217">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1ca68-218">**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-218">**Failure using the VxD loader.**</span></span> <span data-ttu-id="1ca68-219">(19)</span><span class="sxs-lookup"><span data-stu-id="1ca68-219">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1ca68-220">**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-220">**Your registry might be corrupted.**</span></span> <span data-ttu-id="1ca68-221">(20)</span><span class="sxs-lookup"><span data-stu-id="1ca68-221">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1ca68-222">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-222">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1ca68-223">(21)</span><span class="sxs-lookup"><span data-stu-id="1ca68-223">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1ca68-224">**這個裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-224">**This device is disabled.**</span></span> <span data-ttu-id="1ca68-225">(22)</span><span class="sxs-lookup"><span data-stu-id="1ca68-225">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1ca68-226">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-226">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1ca68-227">(23)</span><span class="sxs-lookup"><span data-stu-id="1ca68-227">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1ca68-228">**這個裝置可能不存在、運作不正確、或並未安裝所有的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-228">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1ca68-229">(24)</span><span class="sxs-lookup"><span data-stu-id="1ca68-229">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1ca68-230">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-230">**Windows is still setting up this device.**</span></span> <span data-ttu-id="1ca68-231">(25)</span><span class="sxs-lookup"><span data-stu-id="1ca68-231">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1ca68-232">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-232">**Windows is still setting up this device.**</span></span> <span data-ttu-id="1ca68-233">(26)</span><span class="sxs-lookup"><span data-stu-id="1ca68-233">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1ca68-234">**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-234">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1ca68-235">(27)</span><span class="sxs-lookup"><span data-stu-id="1ca68-235">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1ca68-236">**這個裝置的驅動程式尚未安裝。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-236">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1ca68-237">(28)</span><span class="sxs-lookup"><span data-stu-id="1ca68-237">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1ca68-238">**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-238">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1ca68-239">(29)</span><span class="sxs-lookup"><span data-stu-id="1ca68-239">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1ca68-240">**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-240">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1ca68-241">(30)</span><span class="sxs-lookup"><span data-stu-id="1ca68-241">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1ca68-242">**這個裝置並未正確執行，因為 Windows 無法載入這個裝置必需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1ca68-242">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1ca68-243"> (31) </span><span class="sxs-lookup"><span data-stu-id="1ca68-243">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1ca68-244">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="1ca68-244">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-245">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ca68-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-247">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-247">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-248">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="1ca68-248">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1ca68-249">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-249">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-250">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1ca68-250">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-253">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1ca68-253">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-254">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ca68-254">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1ca68-255">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="1ca68-255">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1ca68-256">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-256">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-257">**說明**</span><span class="sxs-lookup"><span data-stu-id="1ca68-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-260">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-260">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-261">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="1ca68-261">A textual description of the object.</span></span>

<span data-ttu-id="1ca68-262">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-263">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1ca68-263">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-265">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-266">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1ca68-266">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-267">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="1ca68-267">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="1ca68-268">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-268">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-269">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1ca68-269">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-270">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ca68-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-271">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-272">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="1ca68-272">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="1ca68-273">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-273">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-274">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1ca68-274">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-275">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-276">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-277">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="1ca68-277">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="1ca68-278">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1ca68-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-280">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1ca68-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-282">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="1ca68-282">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-283">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="1ca68-283">Indicates when the object was installed.</span></span> <span data-ttu-id="1ca68-284">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="1ca68-284">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1ca68-285">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-285">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-286">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1ca68-286">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-287">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1ca68-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-288">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-289">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1ca68-289">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1ca68-290">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-291">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1ca68-291">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-292">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-293">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-294">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-295">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="1ca68-295">Label by which the object is known.</span></span> <span data-ttu-id="1ca68-296">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="1ca68-296">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1ca68-297">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-297">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-298">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1ca68-298">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-299">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-300">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-301">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-301">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-302">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ca68-302">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1ca68-303">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1ca68-303">Example: "\*PNP030b"</span></span>

<span data-ttu-id="1ca68-304">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-305">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1ca68-305">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-306">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1ca68-306">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-308">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="1ca68-308">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="1ca68-309">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1ca68-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1ca68-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-311">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="1ca68-311">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1ca68-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="1ca68-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-313">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="1ca68-313">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1ca68-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="1ca68-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-315">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="1ca68-315">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1ca68-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="1ca68-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-317">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="1ca68-317">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1ca68-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="1ca68-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-319">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="1ca68-319">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1ca68-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="1ca68-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-321">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="1ca68-321">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="1ca68-322">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="1ca68-322">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="1ca68-323">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-323">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1ca68-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="1ca68-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-325">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="1ca68-325">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1ca68-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="1ca68-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-327">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="1ca68-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1ca68-328">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1ca68-328">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-329">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ca68-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-331">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="1ca68-331">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="1ca68-332">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="1ca68-332">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1ca68-333">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="1ca68-333">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="1ca68-334">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="1ca68-334">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1ca68-335">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-336">**狀態**</span><span class="sxs-lookup"><span data-stu-id="1ca68-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-339">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-339">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-340">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="1ca68-340">String that indicates the current status of the object.</span></span> <span data-ttu-id="1ca68-341">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="1ca68-341">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="1ca68-342">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="1ca68-342">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="1ca68-343">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="1ca68-343">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="1ca68-344">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="1ca68-344">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1ca68-345">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="1ca68-345">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1ca68-346">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="1ca68-346">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1ca68-347">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1ca68-348">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="1ca68-348">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1ca68-349">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-349">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1ca68-350">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-350">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1ca68-351">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-351">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1ca68-352">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-352">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1ca68-353">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-353">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1ca68-354">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-354">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1ca68-355">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-355">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1ca68-356">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-356">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1ca68-357">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-357">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1ca68-358">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-358">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1ca68-359">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-359">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1ca68-360">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="1ca68-360">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1ca68-361">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1ca68-361">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-362">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ca68-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-364">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="1ca68-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-365">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="1ca68-365">State of the logical device.</span></span> <span data-ttu-id="1ca68-366">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="1ca68-366">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="1ca68-367">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1ca68-368">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1ca68-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1ca68-369">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="1ca68-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1ca68-370">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="1ca68-370">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1ca68-371">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="1ca68-371">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1ca68-372">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="1ca68-372">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1ca68-373">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1ca68-373">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-376">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1ca68-376">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-377">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1ca68-377">The scoping system's creation class name.</span></span>

<span data-ttu-id="1ca68-378">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-379">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1ca68-379">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-380">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1ca68-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-381">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-382">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1ca68-382">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-383">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ca68-383">The scoping system's name.</span></span>

<span data-ttu-id="1ca68-384">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ca68-385">**急迫性**</span><span class="sxs-lookup"><span data-stu-id="1ca68-385">**Urgency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-386">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1ca68-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-388">列舉值，指出警示閃爍、震動或發出聲音聲音的相對頻率。</span><span class="sxs-lookup"><span data-stu-id="1ca68-388">Enumerated value that indicates the relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1ca68-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1ca68-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-390">不明。</span><span class="sxs-lookup"><span data-stu-id="1ca68-390">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1ca68-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1ca68-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-392">其他。</span><span class="sxs-lookup"><span data-stu-id="1ca68-392">Other.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1ca68-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (2) </span><span class="sxs-lookup"><span data-stu-id="1ca68-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-394">不支援。</span><span class="sxs-lookup"><span data-stu-id="1ca68-394">Not supported.</span></span>

</dd> <dt>

<span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>

<span data-ttu-id="1ca68-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**資訊** (3) </span><span class="sxs-lookup"><span data-stu-id="1ca68-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informational** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-396">資訊。</span><span class="sxs-lookup"><span data-stu-id="1ca68-396">Informational.</span></span>

</dd> <dt>

<span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>

<span data-ttu-id="1ca68-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**非關鍵性** (4) </span><span class="sxs-lookup"><span data-stu-id="1ca68-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Non-Critical** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-398">非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="1ca68-398">Non-critical.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="1ca68-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (5) </span><span class="sxs-lookup"><span data-stu-id="1ca68-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-400">嚴重。</span><span class="sxs-lookup"><span data-stu-id="1ca68-400">Critical.</span></span>

</dd> <dt>

<span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>

<span data-ttu-id="1ca68-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**無法** 復原的 (6) </span><span class="sxs-lookup"><span data-stu-id="1ca68-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Unrecoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1ca68-402">無法.</span><span class="sxs-lookup"><span data-stu-id="1ca68-402">Unrecoverable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1ca68-403">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="1ca68-403">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ca68-404">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1ca68-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1ca68-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1ca68-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ca68-406">若 **為 TRUE**，則會顯示警示。</span><span class="sxs-lookup"><span data-stu-id="1ca68-406">If **TRUE**, the alarm is visible.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ca68-407">備註</span><span class="sxs-lookup"><span data-stu-id="1ca68-407">Remarks</span></span>

<span data-ttu-id="1ca68-408">**Cim \_ AlarmDevice** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca68-408">The **CIM\_AlarmDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1ca68-409">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="1ca68-409">WMI does not implement this class.</span></span>

<span data-ttu-id="1ca68-410">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1ca68-410">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1ca68-411">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1ca68-411">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ca68-412">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ca68-412">Requirements</span></span>



| <span data-ttu-id="1ca68-413">需求</span><span class="sxs-lookup"><span data-stu-id="1ca68-413">Requirement</span></span> | <span data-ttu-id="1ca68-414">值</span><span class="sxs-lookup"><span data-stu-id="1ca68-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca68-415">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ca68-415">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca68-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ca68-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1ca68-417">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ca68-417">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca68-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ca68-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1ca68-419">命名空間</span><span class="sxs-lookup"><span data-stu-id="1ca68-419">Namespace</span></span><br/>                | <span data-ttu-id="1ca68-420">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1ca68-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1ca68-421">MOF</span><span class="sxs-lookup"><span data-stu-id="1ca68-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ca68-422"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ca68-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ca68-423">DLL</span><span class="sxs-lookup"><span data-stu-id="1ca68-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ca68-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ca68-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ca68-425">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ca68-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ca68-426">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="1ca68-426">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

