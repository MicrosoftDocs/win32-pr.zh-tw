---
description: CIM \_ 控制器類別是用來分組其他控制項相關裝置的父類別。 控制器的範例包括 SCSI 控制器、USB 控制器和串列控制器。
ms.assetid: 526d58bb-cdf4-42c2-ae89-7b86d99e2017
ms.tgt_platform: multiple
title: 'CIM_Controller 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller
- CIM_Controller.Caption
- CIM_Controller.Description
- CIM_Controller.InstallDate
- CIM_Controller.Name
- CIM_Controller.Status
- CIM_Controller.Availability
- CIM_Controller.ConfigManagerErrorCode
- CIM_Controller.ConfigManagerUserConfig
- CIM_Controller.CreationClassName
- CIM_Controller.DeviceID
- CIM_Controller.PowerManagementCapabilities
- CIM_Controller.ErrorCleared
- CIM_Controller.ErrorDescription
- CIM_Controller.LastErrorCode
- CIM_Controller.PNPDeviceID
- CIM_Controller.PowerManagementSupported
- CIM_Controller.StatusInfo
- CIM_Controller.SystemCreationClassName
- CIM_Controller.SystemName
- CIM_Controller.MaxNumberControlled
- CIM_Controller.ProtocolSupported
- CIM_Controller.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b23ef846c118c8d0698660175e4be700ea892055
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187695"
---
# <a name="cim_controller-class-cimwin32-wmi-providers"></a><span data-ttu-id="1aabb-104">CIM_Controller 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="1aabb-104">CIM_Controller class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1aabb-105">**CIM \_ 控制器** 類別是用來分組其他控制項相關裝置的父類別。</span><span class="sxs-lookup"><span data-stu-id="1aabb-105">The **CIM\_Controller** class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="1aabb-106">控制器的範例包括 SCSI 控制器、USB 控制器和串列控制器。</span><span class="sxs-lookup"><span data-stu-id="1aabb-106">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

<span data-ttu-id="1aabb-107">**CIM \_ 控制器** 類別是一種抽象概念，適用于具有單一通訊協定堆疊的裝置，其主要是用於與下游 ([**CIM \_ ControlledBy**](cim-controlledby.md)) 裝置的通訊及控制或重設。</span><span class="sxs-lookup"><span data-stu-id="1aabb-107">The **CIM\_Controller** class is an abstraction for devices with a single protocol stack, which exist primarily for communication to, and control or reset of, downstream ([**CIM\_ControlledBy**](cim-controlledby.md)) devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1aabb-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1aabb-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1aabb-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1aabb-110">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1aabb-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1aabb-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1aabb-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aabb-112">語法</span><span class="sxs-lookup"><span data-stu-id="1aabb-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C531-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Controller : CIM_LogicalDevice
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
  uint32   MaxNumberControlled;
  uint16   ProtocolSupported;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="1aabb-113">成員</span><span class="sxs-lookup"><span data-stu-id="1aabb-113">Members</span></span>

<span data-ttu-id="1aabb-114">**CIM \_ 控制器** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1aabb-114">The **CIM\_Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="1aabb-115">方法</span><span class="sxs-lookup"><span data-stu-id="1aabb-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="1aabb-116">屬性</span><span class="sxs-lookup"><span data-stu-id="1aabb-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1aabb-117">方法</span><span class="sxs-lookup"><span data-stu-id="1aabb-117">Methods</span></span>

<span data-ttu-id="1aabb-118">**CIM \_ 控制器** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1aabb-118">The **CIM\_Controller** class has these methods.</span></span>



| <span data-ttu-id="1aabb-119">方法</span><span class="sxs-lookup"><span data-stu-id="1aabb-119">Method</span></span>                                                                | <span data-ttu-id="1aabb-120">描述</span><span class="sxs-lookup"><span data-stu-id="1aabb-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1aabb-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="1aabb-121">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="1aabb-122">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="1aabb-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="1aabb-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1aabb-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="1aabb-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1aabb-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="1aabb-125">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="1aabb-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="1aabb-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1aabb-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1aabb-127">屬性</span><span class="sxs-lookup"><span data-stu-id="1aabb-127">Properties</span></span>

<span data-ttu-id="1aabb-128">**CIM \_ 控制器** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1aabb-128">The **CIM\_Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1aabb-129">**可用性**</span><span class="sxs-lookup"><span data-stu-id="1aabb-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1aabb-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-132">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="1aabb-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-133">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="1aabb-133">Availability and status of the device.</span></span>

<span data-ttu-id="1aabb-134">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1aabb-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1aabb-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1aabb-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="1aabb-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1aabb-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="1aabb-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1aabb-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="1aabb-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1aabb-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="1aabb-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1aabb-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="1aabb-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1aabb-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="1aabb-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1aabb-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="1aabb-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1aabb-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="1aabb-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1aabb-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="1aabb-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1aabb-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="1aabb-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1aabb-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="1aabb-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1aabb-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="1aabb-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-148">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="1aabb-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1aabb-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="1aabb-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-150">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="1aabb-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1aabb-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="1aabb-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-152">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="1aabb-152">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1aabb-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="1aabb-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1aabb-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="1aabb-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-155">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="1aabb-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1aabb-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="1aabb-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-157">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="1aabb-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1aabb-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="1aabb-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-159">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="1aabb-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1aabb-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="1aabb-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-161">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="1aabb-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1aabb-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="1aabb-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-163">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="1aabb-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1aabb-164">**標題**</span><span class="sxs-lookup"><span data-stu-id="1aabb-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-167">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-168">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="1aabb-168">A short textual description of the object.</span></span>

<span data-ttu-id="1aabb-169">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-170">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1aabb-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-171">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1aabb-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-172">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-173">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-174">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1aabb-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="1aabb-175">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1aabb-176">**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-176">**This device is working properly.**</span></span> <span data-ttu-id="1aabb-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="1aabb-177">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1aabb-178">**這個裝置並未正確設定。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-178">**This device is not configured correctly.**</span></span> <span data-ttu-id="1aabb-179">(1)</span><span class="sxs-lookup"><span data-stu-id="1aabb-179">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1aabb-180">**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-180">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1aabb-181">(2)</span><span class="sxs-lookup"><span data-stu-id="1aabb-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1aabb-182">**這個裝置的驅動程式可能已損毀，或您系統的記憶體或其他資源可能不足。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-182">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1aabb-183">(3)</span><span class="sxs-lookup"><span data-stu-id="1aabb-183">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1aabb-184">**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-184">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1aabb-185">(4)</span><span class="sxs-lookup"><span data-stu-id="1aabb-185">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1aabb-186">**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-186">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1aabb-187">(5)</span><span class="sxs-lookup"><span data-stu-id="1aabb-187">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1aabb-188">**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-188">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1aabb-189">(6)</span><span class="sxs-lookup"><span data-stu-id="1aabb-189">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1aabb-190">**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-190">**Cannot filter.**</span></span> <span data-ttu-id="1aabb-191">(7)</span><span class="sxs-lookup"><span data-stu-id="1aabb-191">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1aabb-192">**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-192">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1aabb-193">(8)</span><span class="sxs-lookup"><span data-stu-id="1aabb-193">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1aabb-194">**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-194">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1aabb-195">(9)</span><span class="sxs-lookup"><span data-stu-id="1aabb-195">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1aabb-196">**這個裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-196">**This device cannot start.**</span></span> <span data-ttu-id="1aabb-197">(10)</span><span class="sxs-lookup"><span data-stu-id="1aabb-197">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1aabb-198">**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-198">**This device failed.**</span></span> <span data-ttu-id="1aabb-199">(11)</span><span class="sxs-lookup"><span data-stu-id="1aabb-199">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1aabb-200">**這個裝置沒有足夠資源可供使用。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-200">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1aabb-201"> (12) </span><span class="sxs-lookup"><span data-stu-id="1aabb-201">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1aabb-202">**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-202">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1aabb-203">(13)</span><span class="sxs-lookup"><span data-stu-id="1aabb-203">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1aabb-204">**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-204">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1aabb-205">(14)</span><span class="sxs-lookup"><span data-stu-id="1aabb-205">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1aabb-206">**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-206">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1aabb-207">(15)</span><span class="sxs-lookup"><span data-stu-id="1aabb-207">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1aabb-208">**Windows 無法識別這個裝置所使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-208">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1aabb-209">(16)</span><span class="sxs-lookup"><span data-stu-id="1aabb-209">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1aabb-210">**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-210">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1aabb-211">(17)</span><span class="sxs-lookup"><span data-stu-id="1aabb-211">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1aabb-212">**重新安裝這個裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-212">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1aabb-213">(18)</span><span class="sxs-lookup"><span data-stu-id="1aabb-213">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1aabb-214">**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-214">**Failure using the VxD loader.**</span></span> <span data-ttu-id="1aabb-215">(19)</span><span class="sxs-lookup"><span data-stu-id="1aabb-215">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1aabb-216">**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-216">**Your registry might be corrupted.**</span></span> <span data-ttu-id="1aabb-217">(20)</span><span class="sxs-lookup"><span data-stu-id="1aabb-217">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1aabb-218">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-218">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1aabb-219">(21)</span><span class="sxs-lookup"><span data-stu-id="1aabb-219">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1aabb-220">**這個裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-220">**This device is disabled.**</span></span> <span data-ttu-id="1aabb-221">(22)</span><span class="sxs-lookup"><span data-stu-id="1aabb-221">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1aabb-222">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-222">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1aabb-223">(23)</span><span class="sxs-lookup"><span data-stu-id="1aabb-223">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1aabb-224">**這個裝置可能不存在、運作不正確、或並未安裝所有的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-224">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1aabb-225">(24)</span><span class="sxs-lookup"><span data-stu-id="1aabb-225">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1aabb-226">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-226">**Windows is still setting up this device.**</span></span> <span data-ttu-id="1aabb-227">(25)</span><span class="sxs-lookup"><span data-stu-id="1aabb-227">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1aabb-228">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-228">**Windows is still setting up this device.**</span></span> <span data-ttu-id="1aabb-229">(26)</span><span class="sxs-lookup"><span data-stu-id="1aabb-229">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1aabb-230">**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-230">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1aabb-231">(27)</span><span class="sxs-lookup"><span data-stu-id="1aabb-231">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1aabb-232">**這個裝置的驅動程式尚未安裝。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-232">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1aabb-233">(28)</span><span class="sxs-lookup"><span data-stu-id="1aabb-233">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1aabb-234">**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-234">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1aabb-235">(29)</span><span class="sxs-lookup"><span data-stu-id="1aabb-235">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1aabb-236">**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-236">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1aabb-237">(30)</span><span class="sxs-lookup"><span data-stu-id="1aabb-237">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1aabb-238">**這個裝置並未正確執行，因為 Windows 無法載入這個裝置必需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1aabb-238">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1aabb-239"> (31) </span><span class="sxs-lookup"><span data-stu-id="1aabb-239">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1aabb-240">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="1aabb-240">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-241">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1aabb-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-243">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-243">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-244">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="1aabb-244">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1aabb-245">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-245">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-246">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1aabb-246">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-249">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1aabb-249">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-250">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="1aabb-250">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1aabb-251">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="1aabb-251">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1aabb-252">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-252">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-253">**說明**</span><span class="sxs-lookup"><span data-stu-id="1aabb-253">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-254">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-255">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-256">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-256">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-257">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="1aabb-257">A textual description of the object.</span></span>

<span data-ttu-id="1aabb-258">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-258">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-259">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1aabb-259">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-260">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-261">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-262">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1aabb-262">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-263">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="1aabb-263">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="1aabb-264">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-264">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-265">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1aabb-265">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-266">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1aabb-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-268">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="1aabb-268">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="1aabb-269">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-269">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-270">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1aabb-270">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-271">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-273">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="1aabb-273">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="1aabb-274">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-274">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1aabb-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-276">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1aabb-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-278">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="1aabb-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-279">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="1aabb-279">Indicates when the object was installed.</span></span> <span data-ttu-id="1aabb-280">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="1aabb-280">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1aabb-281">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-281">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-282">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1aabb-282">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-283">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1aabb-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-285">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1aabb-285">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1aabb-286">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="1aabb-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-288">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1aabb-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-290">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="1aabb-290">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-291">此控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="1aabb-291">Maximum number of directly addressable entities supported by this controller.</span></span> <span data-ttu-id="1aabb-292">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="1aabb-292">A value of 0 should be used if the number is unknown or unlimited.</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-293">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1aabb-293">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-294">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-296">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-297">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="1aabb-297">Label by which the object is known.</span></span> <span data-ttu-id="1aabb-298">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="1aabb-298">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1aabb-299">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-300">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1aabb-300">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-303">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-304">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="1aabb-304">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1aabb-305">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1aabb-305">Example: "\*PNP030b"</span></span>

<span data-ttu-id="1aabb-306">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-307">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1aabb-307">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-308">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1aabb-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-310">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="1aabb-310">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="1aabb-311">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1aabb-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1aabb-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-313">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="1aabb-313">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1aabb-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="1aabb-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-315">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="1aabb-315">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1aabb-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="1aabb-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-317">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="1aabb-317">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1aabb-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="1aabb-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-319">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="1aabb-319">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1aabb-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="1aabb-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-321">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="1aabb-321">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1aabb-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="1aabb-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-323">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="1aabb-323">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="1aabb-324">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="1aabb-324">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="1aabb-325">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-325">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1aabb-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="1aabb-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-327">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="1aabb-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1aabb-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="1aabb-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1aabb-329">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="1aabb-329">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1aabb-330">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1aabb-330">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-331">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1aabb-331">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-333">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="1aabb-333">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="1aabb-334">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="1aabb-334">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1aabb-335">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="1aabb-335">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="1aabb-336">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="1aabb-336">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1aabb-337">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-338">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="1aabb-338">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-339">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1aabb-339">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-341">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="1aabb-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-342">控制器用來存取「受控制」裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1aabb-342">The protocol used by the controller to access 'controlled' devices.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1aabb-343">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1aabb-343">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1aabb-344">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="1aabb-344">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="1aabb-345">**EISA** (3) </span><span class="sxs-lookup"><span data-stu-id="1aabb-345">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="1aabb-346">**ISA** (4) </span><span class="sxs-lookup"><span data-stu-id="1aabb-346">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="1aabb-347">**PCI** (5) </span><span class="sxs-lookup"><span data-stu-id="1aabb-347">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="1aabb-348">**ATA/ATAPI** (6) </span><span class="sxs-lookup"><span data-stu-id="1aabb-348">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="1aabb-349">**彈性磁片** (7) </span><span class="sxs-lookup"><span data-stu-id="1aabb-349">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="1aabb-350">**1496** (8) </span><span class="sxs-lookup"><span data-stu-id="1aabb-350">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="1aabb-351">**SCSI 平行介面** (9) </span><span class="sxs-lookup"><span data-stu-id="1aabb-351">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="1aabb-352">**SCSI 光纖通道通訊協定** (10) </span><span class="sxs-lookup"><span data-stu-id="1aabb-352">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="1aabb-353">**SCSI 序列匯流排通訊協定** (11) </span><span class="sxs-lookup"><span data-stu-id="1aabb-353">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="1aabb-354">**SCSI 序列匯流排通訊協定-2 (1394)** (12) </span><span class="sxs-lookup"><span data-stu-id="1aabb-354">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="1aabb-355">**SCSI 序列儲存架構** (13) </span><span class="sxs-lookup"><span data-stu-id="1aabb-355">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="1aabb-356">**VESA** (14) </span><span class="sxs-lookup"><span data-stu-id="1aabb-356">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="1aabb-357">**PCMCIA** (15) </span><span class="sxs-lookup"><span data-stu-id="1aabb-357">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="1aabb-358">**通用序列匯流排** (16) </span><span class="sxs-lookup"><span data-stu-id="1aabb-358">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="1aabb-359">**平行通訊協定** (17) </span><span class="sxs-lookup"><span data-stu-id="1aabb-359">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="1aabb-360">**ESCON** (18) </span><span class="sxs-lookup"><span data-stu-id="1aabb-360">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="1aabb-361">**診斷** (19) </span><span class="sxs-lookup"><span data-stu-id="1aabb-361">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="1aabb-362">**I2C** (20) </span><span class="sxs-lookup"><span data-stu-id="1aabb-362">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="1aabb-363">**Power** (21) </span><span class="sxs-lookup"><span data-stu-id="1aabb-363">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="1aabb-364">**HIPPI** (22) </span><span class="sxs-lookup"><span data-stu-id="1aabb-364">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="1aabb-365">**MultiBus** (23) </span><span class="sxs-lookup"><span data-stu-id="1aabb-365">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="1aabb-366">**Vm** (24) </span><span class="sxs-lookup"><span data-stu-id="1aabb-366">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="1aabb-367">**IPI** (25) </span><span class="sxs-lookup"><span data-stu-id="1aabb-367">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="1aabb-368">**IEEE-488** (26) </span><span class="sxs-lookup"><span data-stu-id="1aabb-368">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="1aabb-369">**RS232** (27) </span><span class="sxs-lookup"><span data-stu-id="1aabb-369">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="1aabb-370">**IEEE 802.3 10BASE5** (28) </span><span class="sxs-lookup"><span data-stu-id="1aabb-370">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="1aabb-371">**IEEE 802.3 10BASE2** (29) </span><span class="sxs-lookup"><span data-stu-id="1aabb-371">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="1aabb-372">**IEEE 802.3 1BASE5** (30) </span><span class="sxs-lookup"><span data-stu-id="1aabb-372">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="1aabb-373">**IEEE 802.3 10BROAD36** (31) </span><span class="sxs-lookup"><span data-stu-id="1aabb-373">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="1aabb-374">**IEEE 802.3 100BASEVG** (32) </span><span class="sxs-lookup"><span data-stu-id="1aabb-374">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="1aabb-375">**IEEE 802.5 權杖-環形** (33) </span><span class="sxs-lookup"><span data-stu-id="1aabb-375">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="1aabb-376">**ANSI x3t 9.5 FDDI** (34) </span><span class="sxs-lookup"><span data-stu-id="1aabb-376">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="1aabb-377">**MCA** (35) </span><span class="sxs-lookup"><span data-stu-id="1aabb-377">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="1aabb-378">**ESDI** (36) </span><span class="sxs-lookup"><span data-stu-id="1aabb-378">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="1aabb-379">**IDE** (37) </span><span class="sxs-lookup"><span data-stu-id="1aabb-379">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="1aabb-380">**CMD** (38) </span><span class="sxs-lookup"><span data-stu-id="1aabb-380">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="1aabb-381">**ST506** (39) </span><span class="sxs-lookup"><span data-stu-id="1aabb-381">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="1aabb-382">**」 Dssi 小組** (40) </span><span class="sxs-lookup"><span data-stu-id="1aabb-382">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="1aabb-383">**QIC2** (41) </span><span class="sxs-lookup"><span data-stu-id="1aabb-383">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="1aabb-384">**增強型 ATA/IDE** (42) </span><span class="sxs-lookup"><span data-stu-id="1aabb-384">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="1aabb-385">**AGP** (43) </span><span class="sxs-lookup"><span data-stu-id="1aabb-385">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="1aabb-386">**TWIRP (雙向紅外線)** (44) </span><span class="sxs-lookup"><span data-stu-id="1aabb-386">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="1aabb-387">**(快速紅外線)** (45) 的杉樹</span><span class="sxs-lookup"><span data-stu-id="1aabb-387">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="1aabb-388">**SIR (串列紅外線)** (46) </span><span class="sxs-lookup"><span data-stu-id="1aabb-388">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="1aabb-389">**IrBus** (47) </span><span class="sxs-lookup"><span data-stu-id="1aabb-389">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1aabb-390">**狀態**</span><span class="sxs-lookup"><span data-stu-id="1aabb-390">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-391">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-393">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-393">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-394">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="1aabb-394">String that indicates the current status of the object.</span></span> <span data-ttu-id="1aabb-395">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="1aabb-395">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="1aabb-396">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="1aabb-396">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="1aabb-397">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="1aabb-397">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="1aabb-398">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="1aabb-398">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1aabb-399">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="1aabb-399">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1aabb-400">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="1aabb-400">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1aabb-401">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1aabb-402">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="1aabb-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1aabb-403">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1aabb-404">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1aabb-405">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1aabb-406">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1aabb-407">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1aabb-408">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1aabb-409">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1aabb-410">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1aabb-411">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1aabb-412">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1aabb-413">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1aabb-414">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="1aabb-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1aabb-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1aabb-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-416">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1aabb-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-418">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="1aabb-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-419">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="1aabb-419">State of the logical device.</span></span> <span data-ttu-id="1aabb-420">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="1aabb-420">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="1aabb-421">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1aabb-422">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1aabb-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1aabb-423">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="1aabb-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1aabb-424">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="1aabb-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1aabb-425">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="1aabb-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1aabb-426">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="1aabb-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1aabb-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1aabb-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-428">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-430">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1aabb-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-431">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1aabb-431">The scoping system's creation class name.</span></span>

<span data-ttu-id="1aabb-432">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1aabb-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1aabb-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-436">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1aabb-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-437">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="1aabb-437">The scoping system's name.</span></span>

<span data-ttu-id="1aabb-438">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1aabb-439">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="1aabb-439">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1aabb-440">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1aabb-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1aabb-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1aabb-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1aabb-442">上次重設控制器 (關閉或重新初始化) 的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="1aabb-442">Date and time the controller was last reset (powered down or reinitialized).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1aabb-443">備註</span><span class="sxs-lookup"><span data-stu-id="1aabb-443">Remarks</span></span>

<span data-ttu-id="1aabb-444">**Cim \_ 控制器** 類別衍生自 [**cim \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-444">The **CIM\_Controller** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1aabb-445">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="1aabb-445">WMI does not implement this class.</span></span> <span data-ttu-id="1aabb-446">針對衍生自 **CIM \_ 控制器** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="1aabb-446">For classes derived from **CIM\_Controller**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1aabb-447">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1aabb-447">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1aabb-448">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1aabb-448">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aabb-449">規格需求</span><span class="sxs-lookup"><span data-stu-id="1aabb-449">Requirements</span></span>



| <span data-ttu-id="1aabb-450">需求</span><span class="sxs-lookup"><span data-stu-id="1aabb-450">Requirement</span></span> | <span data-ttu-id="1aabb-451">值</span><span class="sxs-lookup"><span data-stu-id="1aabb-451">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1aabb-452">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1aabb-452">Minimum supported client</span></span><br/> | <span data-ttu-id="1aabb-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1aabb-453">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1aabb-454">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1aabb-454">Minimum supported server</span></span><br/> | <span data-ttu-id="1aabb-455">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1aabb-455">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1aabb-456">命名空間</span><span class="sxs-lookup"><span data-stu-id="1aabb-456">Namespace</span></span><br/>                | <span data-ttu-id="1aabb-457">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1aabb-457">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1aabb-458">MOF</span><span class="sxs-lookup"><span data-stu-id="1aabb-458">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1aabb-459"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1aabb-459"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1aabb-460">DLL</span><span class="sxs-lookup"><span data-stu-id="1aabb-460">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aabb-461"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aabb-461"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aabb-462">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1aabb-462">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aabb-463">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="1aabb-463">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

