---
description: CIM \_ FlatPanel 類別代表平面化面板邏輯裝置的功能和管理。
ms.assetid: 0c515621-4ff9-42af-a281-ac49af6d96ba
ms.tgt_platform: multiple
title: CIM_FlatPanel 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FlatPanel
- CIM_FlatPanel.Availability
- CIM_FlatPanel.Caption
- CIM_FlatPanel.ConfigManagerErrorCode
- CIM_FlatPanel.ConfigManagerUserConfig
- CIM_FlatPanel.CreationClassName
- CIM_FlatPanel.Description
- CIM_FlatPanel.DeviceID
- CIM_FlatPanel.DisplayType
- CIM_FlatPanel.ErrorCleared
- CIM_FlatPanel.ErrorDescription
- CIM_FlatPanel.HorizontalResolution
- CIM_FlatPanel.InstallDate
- CIM_FlatPanel.IsLocked
- CIM_FlatPanel.LastErrorCode
- CIM_FlatPanel.LightSource
- CIM_FlatPanel.Name
- CIM_FlatPanel.PNPDeviceID
- CIM_FlatPanel.PowerManagementCapabilities
- CIM_FlatPanel.PowerManagementSupported
- CIM_FlatPanel.ScanMode
- CIM_FlatPanel.Status
- CIM_FlatPanel.StatusInfo
- CIM_FlatPanel.SupportsColor
- CIM_FlatPanel.SystemCreationClassName
- CIM_FlatPanel.SystemName
- CIM_FlatPanel.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c399383223734d2f8ebe68528352c229a74bfbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936313"
---
# <a name="cim_flatpanel-class"></a><span data-ttu-id="2f2eb-103">CIM \_ FlatPanel 類別</span><span class="sxs-lookup"><span data-stu-id="2f2eb-103">CIM\_FlatPanel class</span></span>

<span data-ttu-id="2f2eb-104">**CIM \_ FlatPanel** 類別代表平面化面板邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-104">The **CIM\_FlatPanel** class represents the capabilities and management of the flat panel logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f2eb-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2f2eb-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2f2eb-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2f2eb-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2eb-109">語法</span><span class="sxs-lookup"><span data-stu-id="2f2eb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE9-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_FlatPanel : CIM_Display
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   HorizontalResolution;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  uint16   LightSource;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ScanMode;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsColor;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="2f2eb-110">成員</span><span class="sxs-lookup"><span data-stu-id="2f2eb-110">Members</span></span>

<span data-ttu-id="2f2eb-111">**CIM \_ FlatPanel** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2f2eb-111">The **CIM\_FlatPanel** class has these types of members:</span></span>

-   [<span data-ttu-id="2f2eb-112">方法</span><span class="sxs-lookup"><span data-stu-id="2f2eb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2f2eb-113">屬性</span><span class="sxs-lookup"><span data-stu-id="2f2eb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2f2eb-114">方法</span><span class="sxs-lookup"><span data-stu-id="2f2eb-114">Methods</span></span>

<span data-ttu-id="2f2eb-115">**CIM \_ FlatPanel** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-115">The **CIM\_FlatPanel** class has these methods.</span></span>



| <span data-ttu-id="2f2eb-116">方法</span><span class="sxs-lookup"><span data-stu-id="2f2eb-116">Method</span></span>                                                               | <span data-ttu-id="2f2eb-117">描述</span><span class="sxs-lookup"><span data-stu-id="2f2eb-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f2eb-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-118">**Reset**</span></span>](reset-method-in-class-cim-flatpanel.md)                 | <span data-ttu-id="2f2eb-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="2f2eb-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="2f2eb-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-flatpanel.md) | <span data-ttu-id="2f2eb-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="2f2eb-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2f2eb-124">屬性</span><span class="sxs-lookup"><span data-stu-id="2f2eb-124">Properties</span></span>

<span data-ttu-id="2f2eb-125">**CIM \_ FlatPanel** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-125">The **CIM\_FlatPanel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f2eb-126">**可用性**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="2f2eb-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-130">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-130">Availability and status of the device.</span></span>

<span data-ttu-id="2f2eb-131">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2f2eb-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f2eb-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2f2eb-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2f2eb-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2f2eb-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2f2eb-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2f2eb-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="2f2eb-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2f2eb-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2f2eb-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2f2eb-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2f2eb-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2f2eb-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2f2eb-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-145">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2f2eb-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-147">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2f2eb-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-149">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2f2eb-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2f2eb-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-152">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2f2eb-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-154">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2f2eb-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-156">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2f2eb-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-158">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2f2eb-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-160">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f2eb-161">**標題**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-164">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-165">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-165">Short textual description of the object.</span></span>

<span data-ttu-id="2f2eb-166">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-168">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-170">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-171">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2f2eb-172">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2f2eb-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2f2eb-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-175">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2f2eb-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2f2eb-177">(1)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-178">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2f2eb-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2f2eb-180">(2)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2f2eb-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2f2eb-182">(3)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-183">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2f2eb-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2f2eb-185">(4)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-186">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-186">Device is not working properly.</span></span> <span data-ttu-id="2f2eb-187">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2f2eb-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2f2eb-189">(5)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-190">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2f2eb-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2f2eb-192">(6)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-193">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2f2eb-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2f2eb-195">(7)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2f2eb-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2f2eb-197">(8)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-198">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2f2eb-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2f2eb-200">(9)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-201">裝置無法正常運作;控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2f2eb-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2f2eb-203">(10)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-204">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2f2eb-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2f2eb-206">(11)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-207">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2f2eb-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2f2eb-209"> (12) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-210">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2f2eb-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2f2eb-212">(13)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-213">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2f2eb-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2f2eb-215">(14)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-216">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2f2eb-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2f2eb-218">(15)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-219">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2f2eb-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2f2eb-221">(16)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-222">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2f2eb-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2f2eb-224">(17)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-225">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2f2eb-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2f2eb-227">(18)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-228">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2f2eb-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2f2eb-230">(19)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2f2eb-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2f2eb-232">(20)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-233">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2f2eb-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2f2eb-235">(21)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-236">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-236">System failure.</span></span> <span data-ttu-id="2f2eb-237">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2f2eb-238">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2f2eb-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2f2eb-240">(22)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-241">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2f2eb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2f2eb-243">(23)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-244">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-244">System failure.</span></span> <span data-ttu-id="2f2eb-245">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2f2eb-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2f2eb-247">(24)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-248">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2f2eb-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2f2eb-250">(25)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-251">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2f2eb-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2f2eb-253">(26)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-254">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2f2eb-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2f2eb-256">(27)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-257">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2f2eb-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2f2eb-259">(28)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-260">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2f2eb-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2f2eb-262">(29)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-263">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2f2eb-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2f2eb-265">(30)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-266">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2f2eb-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2f2eb-268"> (31) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-269">裝置無法正常運作;Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f2eb-270">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-271">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-273">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-274">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2f2eb-275">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-277">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-279">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-280">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2f2eb-281">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2f2eb-282">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-283">**說明**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-284">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-286">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-287">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-287">Textual description of the object.</span></span>

<span data-ttu-id="2f2eb-288">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-290">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-292">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-293">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2f2eb-294">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-295">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-295">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-296">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-296">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-298">列舉，描述平面顯示的類型。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-298">Enumeration that describes the type of flat panel display.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f2eb-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2f2eb-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>

<span data-ttu-id="2f2eb-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**被動式矩陣 LCD** (2) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**Passive Matrix LCD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>

<span data-ttu-id="2f2eb-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**主動式矩陣 LCD** (3) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**Active Matrix LCD** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>

<span data-ttu-id="2f2eb-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**CHOLESTERIC LCD** (4) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**Cholesteric LCD** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>

<span data-ttu-id="2f2eb-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**欄位排放顯示** (5) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**Field Emission Display** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-305">現場排放</span><span class="sxs-lookup"><span data-stu-id="2f2eb-305">Field emission</span></span>

</dd> <dt>

<span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>

<span data-ttu-id="2f2eb-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**電磁 Luminescent 顯示器** (6) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**Electro Luminescent Display** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-307">電磁 luminescent</span><span class="sxs-lookup"><span data-stu-id="2f2eb-307">Electro luminescent</span></span>

</dd> <dt>

<span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>

<span data-ttu-id="2f2eb-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**天然氣等離子** (7) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**Gas Plasma** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="LED"></span><span id="led"></span>

<span data-ttu-id="2f2eb-309"><span id="LED"></span><span id="led"></span>**LED** (8) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-309"><span id="LED"></span><span id="led"></span>**LED** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f2eb-310">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-311">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-313">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2f2eb-314">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-316">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-318">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2f2eb-319">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-320">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-320">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-321">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-323">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "圖元" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-323">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-324">水準解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-324">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-325">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-325">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-326">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-328">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="2f2eb-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-329">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-329">Date and time the object was installed.</span></span> <span data-ttu-id="2f2eb-330">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-330">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2f2eb-331">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-331">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-332">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-332">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-333">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-335">若 **為 TRUE**，則會鎖定裝置，防止使用者輸入或輸出。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-335">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="2f2eb-336">這個屬性繼承自 [**CIM \_ UserDevice**](cim-userdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-336">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-338">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-339">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-340">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2f2eb-341">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-342">**LightSource**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-342">**LightSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-343">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-345">顯示照明類型的描述。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-345">Description of the display illumination type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f2eb-346">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-346">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2f2eb-347">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Backlit"></span><span id="backlit"></span><span id="BACKLIT"></span>

<span data-ttu-id="2f2eb-348">**Backlit** (2) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-348">**Backlit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Edgelit"></span><span id="edgelit"></span><span id="EDGELIT"></span>

<span data-ttu-id="2f2eb-349">**Edgelit** (3) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-349">**Edgelit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reflective"></span><span id="reflective"></span><span id="REFLECTIVE"></span>

<span data-ttu-id="2f2eb-350">**反映** (4) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-350">**Reflective** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f2eb-351">**名稱**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-354">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-354">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-355">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-355">Label by which the object is known.</span></span> <span data-ttu-id="2f2eb-356">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-356">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2f2eb-357">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-357">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-358">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-358">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-359">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-361">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-361">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-362">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-362">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="2f2eb-363">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2f2eb-364">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2f2eb-364">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-365">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-365">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-366">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="2f2eb-366">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-368">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-368">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2f2eb-369">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-369">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f2eb-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2f2eb-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2f2eb-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2f2eb-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-374">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-374">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2f2eb-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-376">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-376">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2f2eb-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-378">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2f2eb-379">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-379">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2f2eb-380">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-380">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2f2eb-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-382">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2f2eb-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2f2eb-384">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f2eb-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-386">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-388">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-388">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2f2eb-389">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-389">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2f2eb-390">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-390">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2f2eb-391">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-391">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="2f2eb-392">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-393">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-393">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-394">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-396">表示單一或雙重掃描的掃描模式。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-396">Scan mode that indicates single or dual scan, for example.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f2eb-397">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-397">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2f2eb-398">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Single_Scan"></span><span id="single_scan"></span><span id="SINGLE_SCAN"></span>

<span data-ttu-id="2f2eb-399">**單一掃描** (2) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-399">**Single Scan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual_Scan"></span><span id="dual_scan"></span><span id="DUAL_SCAN"></span>

<span data-ttu-id="2f2eb-400">**雙重掃描** (3) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-400">**Dual Scan** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f2eb-401">**狀態**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-401">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-402">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-403">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-404">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-404">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-405">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-405">Current status of the object.</span></span> <span data-ttu-id="2f2eb-406">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2f2eb-407">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="2f2eb-407">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2f2eb-408">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-408">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2f2eb-409">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-409">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2f2eb-410">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-410">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f2eb-411">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-411">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2f2eb-412">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-412">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2f2eb-413">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-413">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2f2eb-414">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-414">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2f2eb-415">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-415">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2f2eb-416">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-416">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2f2eb-417">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-417">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2f2eb-418">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-418">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2f2eb-419">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-419">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f2eb-420">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-420">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-421">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-423">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="2f2eb-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-424">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-424">State of the logical device.</span></span> <span data-ttu-id="2f2eb-425">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-425">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2f2eb-426">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2f2eb-427">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-427">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f2eb-428">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-428">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2f2eb-429">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-429">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2f2eb-430">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-430">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2f2eb-431">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-431">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f2eb-432">**SupportsColor**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-432">**SupportsColor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-433">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-435">若 **為 TRUE**，則平面面板支援色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-435">If **TRUE**, the flat panel supports color display.</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-436">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-436">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-437">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-438">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-439">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-439">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-440">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-440">Scoping system's creation class name.</span></span>

<span data-ttu-id="2f2eb-441">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-442">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-442">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-443">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-445">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2f2eb-445">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-446">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-446">Scoping system's name.</span></span>

<span data-ttu-id="2f2eb-447">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f2eb-448">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-448">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f2eb-449">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f2eb-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f2eb-451">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "圖元" ) </span><span class="sxs-lookup"><span data-stu-id="2f2eb-451">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="2f2eb-452">垂直解析度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-452">Vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f2eb-453">備註</span><span class="sxs-lookup"><span data-stu-id="2f2eb-453">Remarks</span></span>

<span data-ttu-id="2f2eb-454">**Cim \_ FlatPanel** 類別衍生自 [**cim \_ 顯示**](cim-display.md)。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-454">The **CIM\_FlatPanel** class is derived from [**CIM\_Display**](cim-display.md).</span></span>

<span data-ttu-id="2f2eb-455">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-455">WMI does not implement this class.</span></span>

<span data-ttu-id="2f2eb-456">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-456">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2f2eb-457">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2f2eb-457">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2eb-458">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f2eb-458">Requirements</span></span>



| <span data-ttu-id="2f2eb-459">需求</span><span class="sxs-lookup"><span data-stu-id="2f2eb-459">Requirement</span></span> | <span data-ttu-id="2f2eb-460">值</span><span class="sxs-lookup"><span data-stu-id="2f2eb-460">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2eb-461">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f2eb-461">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2eb-462">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f2eb-462">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f2eb-463">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f2eb-463">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2eb-464">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f2eb-464">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f2eb-465">命名空間</span><span class="sxs-lookup"><span data-stu-id="2f2eb-465">Namespace</span></span><br/>                | <span data-ttu-id="2f2eb-466">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2f2eb-466">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f2eb-467">MOF</span><span class="sxs-lookup"><span data-stu-id="2f2eb-467">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f2eb-468"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f2eb-468"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f2eb-469">DLL</span><span class="sxs-lookup"><span data-stu-id="2f2eb-469">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f2eb-470"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f2eb-470"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f2eb-471">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f2eb-471">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2eb-472">**CIM \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="2f2eb-472">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

