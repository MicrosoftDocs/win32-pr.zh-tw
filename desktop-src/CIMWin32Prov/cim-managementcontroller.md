---
description: CIM \_ ManagementController 類別與管理控制器的功能和管理有關。
ms.assetid: 47ad29d1-5021-4469-87c0-bd9403faa70c
ms.tgt_platform: multiple
title: CIM_ManagementController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagementController
- CIM_ManagementController.Availability
- CIM_ManagementController.Caption
- CIM_ManagementController.ConfigManagerErrorCode
- CIM_ManagementController.ConfigManagerUserConfig
- CIM_ManagementController.CreationClassName
- CIM_ManagementController.Description
- CIM_ManagementController.DeviceID
- CIM_ManagementController.ErrorCleared
- CIM_ManagementController.ErrorDescription
- CIM_ManagementController.InstallDate
- CIM_ManagementController.LastErrorCode
- CIM_ManagementController.MaxNumberControlled
- CIM_ManagementController.Name
- CIM_ManagementController.PNPDeviceID
- CIM_ManagementController.PowerManagementCapabilities
- CIM_ManagementController.PowerManagementSupported
- CIM_ManagementController.ProtocolSupported
- CIM_ManagementController.Status
- CIM_ManagementController.StatusInfo
- CIM_ManagementController.SystemCreationClassName
- CIM_ManagementController.SystemName
- CIM_ManagementController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c5eab51a8c8a370086f5cd5ac9215948fcd2e2f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936308"
---
# <a name="cim_managementcontroller-class"></a><span data-ttu-id="1a071-103">CIM \_ ManagementController 類別</span><span class="sxs-lookup"><span data-stu-id="1a071-103">CIM\_ManagementController class</span></span>

<span data-ttu-id="1a071-104">**CIM \_ ManagementController** 類別與管理控制器的功能和管理有關。</span><span class="sxs-lookup"><span data-stu-id="1a071-104">The **CIM\_ManagementController** class relates to the capabilities and management of a management controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a071-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1a071-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1a071-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1a071-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1a071-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1a071-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1a071-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1a071-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a071-109">語法</span><span class="sxs-lookup"><span data-stu-id="1a071-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{7250D62E-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ManagementController : CIM_Controller
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
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="1a071-110">成員</span><span class="sxs-lookup"><span data-stu-id="1a071-110">Members</span></span>

<span data-ttu-id="1a071-111">**CIM \_ ManagementController** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1a071-111">The **CIM\_ManagementController** class has these types of members:</span></span>

-   [<span data-ttu-id="1a071-112">方法</span><span class="sxs-lookup"><span data-stu-id="1a071-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1a071-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1a071-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1a071-114">方法</span><span class="sxs-lookup"><span data-stu-id="1a071-114">Methods</span></span>

<span data-ttu-id="1a071-115">**CIM \_ ManagementController** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1a071-115">The **CIM\_ManagementController** class has these methods.</span></span>



| <span data-ttu-id="1a071-116">方法</span><span class="sxs-lookup"><span data-stu-id="1a071-116">Method</span></span>                                                                          | <span data-ttu-id="1a071-117">描述</span><span class="sxs-lookup"><span data-stu-id="1a071-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a071-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="1a071-118">**Reset**</span></span>](reset-method-in-class-cim-managementcontroller.md)                 | <span data-ttu-id="1a071-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="1a071-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="1a071-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1a071-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="1a071-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1a071-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-managementcontroller.md) | <span data-ttu-id="1a071-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="1a071-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="1a071-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1a071-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1a071-124">屬性</span><span class="sxs-lookup"><span data-stu-id="1a071-124">Properties</span></span>

<span data-ttu-id="1a071-125">**CIM \_ ManagementController** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1a071-125">The **CIM\_ManagementController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a071-126">**可用性**</span><span class="sxs-lookup"><span data-stu-id="1a071-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1a071-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-129">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="1a071-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-130">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="1a071-130">Availability and status of the device.</span></span>

<span data-ttu-id="1a071-131">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1a071-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1a071-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a071-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="1a071-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1a071-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="1a071-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1a071-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="1a071-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1a071-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="1a071-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1a071-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="1a071-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1a071-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="1a071-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1a071-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="1a071-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1a071-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="1a071-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1a071-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="1a071-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1a071-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="1a071-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1a071-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="1a071-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1a071-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="1a071-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-145">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="1a071-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1a071-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="1a071-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-147">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="1a071-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1a071-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="1a071-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-149">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="1a071-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1a071-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="1a071-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1a071-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="1a071-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-152">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="1a071-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1a071-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="1a071-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-154">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="1a071-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1a071-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="1a071-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-156">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="1a071-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1a071-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="1a071-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-158">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="1a071-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1a071-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="1a071-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-160">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="1a071-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a071-161">**標題**</span><span class="sxs-lookup"><span data-stu-id="1a071-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-164">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="1a071-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-165">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="1a071-165">Short textual description of the object.</span></span>

<span data-ttu-id="1a071-166">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1a071-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-168">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a071-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-170">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="1a071-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-171">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1a071-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="1a071-172">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1a071-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="1a071-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1a071-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="1a071-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-175">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="1a071-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1a071-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1a071-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1a071-177">(1)</span><span class="sxs-lookup"><span data-stu-id="1a071-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-178">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="1a071-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1a071-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1a071-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1a071-180">(2)</span><span class="sxs-lookup"><span data-stu-id="1a071-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1a071-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="1a071-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1a071-182">(3)</span><span class="sxs-lookup"><span data-stu-id="1a071-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-183">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="1a071-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1a071-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="1a071-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1a071-185">(4)</span><span class="sxs-lookup"><span data-stu-id="1a071-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-186">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="1a071-186">Device is not working properly.</span></span> <span data-ttu-id="1a071-187">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="1a071-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1a071-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="1a071-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1a071-189">(5)</span><span class="sxs-lookup"><span data-stu-id="1a071-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-190">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="1a071-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1a071-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="1a071-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1a071-192">(6)</span><span class="sxs-lookup"><span data-stu-id="1a071-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-193">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="1a071-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1a071-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="1a071-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1a071-195">(7)</span><span class="sxs-lookup"><span data-stu-id="1a071-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1a071-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="1a071-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1a071-197">(8)</span><span class="sxs-lookup"><span data-stu-id="1a071-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-198">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="1a071-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1a071-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="1a071-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1a071-200">(9)</span><span class="sxs-lookup"><span data-stu-id="1a071-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-201">裝置無法正常運作;控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="1a071-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1a071-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="1a071-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1a071-203">(10)</span><span class="sxs-lookup"><span data-stu-id="1a071-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-204">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="1a071-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1a071-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="1a071-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1a071-206">(11)</span><span class="sxs-lookup"><span data-stu-id="1a071-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-207">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="1a071-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1a071-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="1a071-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1a071-209"> (12) </span><span class="sxs-lookup"><span data-stu-id="1a071-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-210">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="1a071-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1a071-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="1a071-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1a071-212">(13)</span><span class="sxs-lookup"><span data-stu-id="1a071-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-213">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="1a071-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1a071-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="1a071-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1a071-215">(14)</span><span class="sxs-lookup"><span data-stu-id="1a071-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-216">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="1a071-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1a071-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="1a071-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1a071-218">(15)</span><span class="sxs-lookup"><span data-stu-id="1a071-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-219">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="1a071-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1a071-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="1a071-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1a071-221">(16)</span><span class="sxs-lookup"><span data-stu-id="1a071-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-222">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="1a071-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1a071-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="1a071-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1a071-224">(17)</span><span class="sxs-lookup"><span data-stu-id="1a071-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-225">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="1a071-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1a071-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1a071-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1a071-227">(18)</span><span class="sxs-lookup"><span data-stu-id="1a071-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-228">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="1a071-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1a071-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="1a071-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1a071-230">(19)</span><span class="sxs-lookup"><span data-stu-id="1a071-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1a071-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="1a071-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1a071-232">(20)</span><span class="sxs-lookup"><span data-stu-id="1a071-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-233">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="1a071-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1a071-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1a071-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1a071-235">(21)</span><span class="sxs-lookup"><span data-stu-id="1a071-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-236">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="1a071-236">System failure.</span></span> <span data-ttu-id="1a071-237">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="1a071-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1a071-238">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="1a071-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1a071-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="1a071-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1a071-240">(22)</span><span class="sxs-lookup"><span data-stu-id="1a071-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-241">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="1a071-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1a071-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="1a071-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1a071-243">(23)</span><span class="sxs-lookup"><span data-stu-id="1a071-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-244">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="1a071-244">System failure.</span></span> <span data-ttu-id="1a071-245">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="1a071-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1a071-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1a071-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1a071-247">(24)</span><span class="sxs-lookup"><span data-stu-id="1a071-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-248">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="1a071-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1a071-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1a071-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1a071-250">(25)</span><span class="sxs-lookup"><span data-stu-id="1a071-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-251">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="1a071-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1a071-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="1a071-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1a071-253">(26)</span><span class="sxs-lookup"><span data-stu-id="1a071-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-254">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="1a071-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1a071-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="1a071-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1a071-256">(27)</span><span class="sxs-lookup"><span data-stu-id="1a071-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-257">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="1a071-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1a071-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1a071-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1a071-259">(28)</span><span class="sxs-lookup"><span data-stu-id="1a071-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-260">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="1a071-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1a071-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="1a071-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1a071-262">(29)</span><span class="sxs-lookup"><span data-stu-id="1a071-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-263">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="1a071-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1a071-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="1a071-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1a071-265">(30)</span><span class="sxs-lookup"><span data-stu-id="1a071-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-266">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="1a071-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1a071-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="1a071-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1a071-268"> (31) </span><span class="sxs-lookup"><span data-stu-id="1a071-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-269">裝置無法正常運作;Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="1a071-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a071-270">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="1a071-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-271">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1a071-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-273">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="1a071-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-274">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="1a071-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1a071-275">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1a071-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-277">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-278">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-279">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1a071-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1a071-280">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a071-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1a071-281">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="1a071-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1a071-282">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-283">**說明**</span><span class="sxs-lookup"><span data-stu-id="1a071-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-284">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-285">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-286">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="1a071-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-287">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="1a071-287">Textual description of the object.</span></span>

<span data-ttu-id="1a071-288">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1a071-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-290">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-291">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-292">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1a071-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1a071-293">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="1a071-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="1a071-294">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-295">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1a071-295">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-296">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1a071-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a071-298">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="1a071-298">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="1a071-299">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-300">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1a071-300">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-301">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a071-303">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="1a071-303">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="1a071-304">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1a071-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-306">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1a071-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-307">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-308">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="1a071-308">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-309">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="1a071-309">Date and time the object was installed.</span></span> <span data-ttu-id="1a071-310">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="1a071-310">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1a071-311">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-312">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1a071-312">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-313">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a071-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a071-315">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1a071-315">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1a071-316">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-317">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="1a071-317">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-318">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1a071-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-320">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.9 ") </span><span class="sxs-lookup"><span data-stu-id="1a071-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-321">控制器支援的直接可定址實體數目上限。</span><span class="sxs-lookup"><span data-stu-id="1a071-321">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="1a071-322">如果數位為未知或無限制，則應使用0值。</span><span class="sxs-lookup"><span data-stu-id="1a071-322">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="1a071-323">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-323">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-324">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1a071-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-327">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="1a071-327">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-328">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="1a071-328">Label by which the object is known.</span></span> <span data-ttu-id="1a071-329">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="1a071-329">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="1a071-330">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-331">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1a071-331">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-332">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-333">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-334">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="1a071-334">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-335">邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a071-335">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="1a071-336">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1a071-337">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1a071-337">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1a071-338">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1a071-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-339">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1a071-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1a071-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a071-341">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="1a071-341">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1a071-342">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="1a071-342">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a071-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1a071-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1a071-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="1a071-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1a071-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="1a071-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1a071-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="1a071-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-347">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="1a071-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1a071-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="1a071-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-349">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="1a071-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1a071-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="1a071-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-351">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="1a071-351">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1a071-352">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="1a071-352">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="1a071-353">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="1a071-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1a071-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="1a071-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-355">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="1a071-355">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1a071-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="1a071-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1a071-357">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="1a071-357">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1a071-358">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1a071-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-359">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1a071-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a071-361">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="1a071-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="1a071-362">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="1a071-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="1a071-363">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="1a071-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="1a071-364">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="1a071-364">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="1a071-365">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-366">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="1a071-366">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-367">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1a071-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-369">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 匯流排埠 \| 001.2 "，" MIF。DMTF \| 磁片 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="1a071-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-370">控制器用來存取「受控制」裝置的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1a071-370">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="1a071-371">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-371">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="1a071-372">值為：</span><span class="sxs-lookup"><span data-stu-id="1a071-372">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1a071-373">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1a071-373">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a071-374">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="1a071-374">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="1a071-375">**EISA** (3) </span><span class="sxs-lookup"><span data-stu-id="1a071-375">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="1a071-376">**ISA** (4) </span><span class="sxs-lookup"><span data-stu-id="1a071-376">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="1a071-377">**PCI** (5) </span><span class="sxs-lookup"><span data-stu-id="1a071-377">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="1a071-378">**ATA/ATAPI** (6) </span><span class="sxs-lookup"><span data-stu-id="1a071-378">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="1a071-379">**彈性磁片** (7) </span><span class="sxs-lookup"><span data-stu-id="1a071-379">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="1a071-380">**1496** (8) </span><span class="sxs-lookup"><span data-stu-id="1a071-380">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="1a071-381">**SCSI 平行介面** (9) </span><span class="sxs-lookup"><span data-stu-id="1a071-381">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="1a071-382">**SCSI 光纖通道通訊協定** (10) </span><span class="sxs-lookup"><span data-stu-id="1a071-382">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="1a071-383">**SCSI 序列匯流排通訊協定** (11) </span><span class="sxs-lookup"><span data-stu-id="1a071-383">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="1a071-384">**SCSI 序列匯流排通訊協定-2 (1394)** (12) </span><span class="sxs-lookup"><span data-stu-id="1a071-384">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="1a071-385">**SCSI 序列儲存架構** (13) </span><span class="sxs-lookup"><span data-stu-id="1a071-385">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="1a071-386">**VESA** (14) </span><span class="sxs-lookup"><span data-stu-id="1a071-386">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="1a071-387">**PCMCIA** (15) </span><span class="sxs-lookup"><span data-stu-id="1a071-387">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="1a071-388">**通用序列匯流排** (16) </span><span class="sxs-lookup"><span data-stu-id="1a071-388">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="1a071-389">**平行通訊協定** (17) </span><span class="sxs-lookup"><span data-stu-id="1a071-389">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="1a071-390">**ESCON** (18) </span><span class="sxs-lookup"><span data-stu-id="1a071-390">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="1a071-391">**診斷** (19) </span><span class="sxs-lookup"><span data-stu-id="1a071-391">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="1a071-392">**I2C** (20) </span><span class="sxs-lookup"><span data-stu-id="1a071-392">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="1a071-393">**Power** (21) </span><span class="sxs-lookup"><span data-stu-id="1a071-393">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="1a071-394">**HIPPI** (22) </span><span class="sxs-lookup"><span data-stu-id="1a071-394">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="1a071-395">**MultiBus** (23) </span><span class="sxs-lookup"><span data-stu-id="1a071-395">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="1a071-396">**Vm** (24) </span><span class="sxs-lookup"><span data-stu-id="1a071-396">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="1a071-397">**IPI** (25) </span><span class="sxs-lookup"><span data-stu-id="1a071-397">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="1a071-398">**IEEE-488** (26) </span><span class="sxs-lookup"><span data-stu-id="1a071-398">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="1a071-399">**RS232** (27) </span><span class="sxs-lookup"><span data-stu-id="1a071-399">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="1a071-400">**IEEE 802.3 10BASE5** (28) </span><span class="sxs-lookup"><span data-stu-id="1a071-400">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="1a071-401">**IEEE 802.3 10BASE2** (29) </span><span class="sxs-lookup"><span data-stu-id="1a071-401">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="1a071-402">**IEEE 802.3 1BASE5** (30) </span><span class="sxs-lookup"><span data-stu-id="1a071-402">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="1a071-403">**IEEE 802.3 10BROAD36** (31) </span><span class="sxs-lookup"><span data-stu-id="1a071-403">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="1a071-404">**IEEE 802.3 100BASEVG** (32) </span><span class="sxs-lookup"><span data-stu-id="1a071-404">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="1a071-405">**IEEE 802.5 權杖-環形** (33) </span><span class="sxs-lookup"><span data-stu-id="1a071-405">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="1a071-406">**ANSI x3t 9.5 FDDI** (34) </span><span class="sxs-lookup"><span data-stu-id="1a071-406">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="1a071-407">**MCA** (35) </span><span class="sxs-lookup"><span data-stu-id="1a071-407">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="1a071-408">**ESDI** (36) </span><span class="sxs-lookup"><span data-stu-id="1a071-408">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="1a071-409">**IDE** (37) </span><span class="sxs-lookup"><span data-stu-id="1a071-409">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="1a071-410">**CMD** (38) </span><span class="sxs-lookup"><span data-stu-id="1a071-410">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="1a071-411">**ST506** (39) </span><span class="sxs-lookup"><span data-stu-id="1a071-411">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="1a071-412">**」 Dssi 小組** (40) </span><span class="sxs-lookup"><span data-stu-id="1a071-412">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="1a071-413">**QIC2** (41) </span><span class="sxs-lookup"><span data-stu-id="1a071-413">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="1a071-414">**增強型 ATA/IDE** (42) </span><span class="sxs-lookup"><span data-stu-id="1a071-414">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="1a071-415">**AGP** (43) </span><span class="sxs-lookup"><span data-stu-id="1a071-415">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="1a071-416">**TWIRP (雙向紅外線)** (44) </span><span class="sxs-lookup"><span data-stu-id="1a071-416">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="1a071-417">**(快速紅外線)** (45) 的杉樹</span><span class="sxs-lookup"><span data-stu-id="1a071-417">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="1a071-418">**SIR (串列紅外線)** (46) </span><span class="sxs-lookup"><span data-stu-id="1a071-418">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="1a071-419">**IrBus** (47) </span><span class="sxs-lookup"><span data-stu-id="1a071-419">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1a071-420">**狀態**</span><span class="sxs-lookup"><span data-stu-id="1a071-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-423">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="1a071-423">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-424">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1a071-424">Current status of the object.</span></span>

<span data-ttu-id="1a071-425">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1a071-426">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="1a071-426">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1a071-427">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="1a071-427">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1a071-428">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-428">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1a071-429">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-429">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a071-430">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-430">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1a071-431">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-431">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1a071-432">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-432">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1a071-433">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-433">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1a071-434">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-434">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1a071-435">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-435">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1a071-436">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="1a071-436">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1a071-437">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-437">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1a071-438">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="1a071-438">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1a071-439">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1a071-439">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-440">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1a071-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-442">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="1a071-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1a071-443">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="1a071-443">State of the logical device.</span></span> <span data-ttu-id="1a071-444">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="1a071-444">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1a071-445">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1a071-446">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1a071-446">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a071-447">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="1a071-447">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1a071-448">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="1a071-448">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1a071-449">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="1a071-449">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1a071-450">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="1a071-450">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1a071-451">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1a071-451">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-452">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-454">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1a071-454">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1a071-455">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="1a071-455">Scoping system's creation class name.</span></span>

<span data-ttu-id="1a071-456">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-456">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-457">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1a071-457">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-458">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1a071-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-459">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a071-460">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1a071-460">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1a071-461">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="1a071-461">Scoping system's name.</span></span>

<span data-ttu-id="1a071-462">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-462">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a071-463">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="1a071-463">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a071-464">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1a071-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1a071-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1a071-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a071-466">上次重設此控制器的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="1a071-466">Date and time this controller was last reset.</span></span> <span data-ttu-id="1a071-467">這可能表示控制器關閉或重新初始化。</span><span class="sxs-lookup"><span data-stu-id="1a071-467">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="1a071-468">這個屬性繼承自 [**CIM \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-468">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a071-469">備註</span><span class="sxs-lookup"><span data-stu-id="1a071-469">Remarks</span></span>

<span data-ttu-id="1a071-470">**Cim \_ ManagementController** 類別衍生自 [**cim \_ 控制器**](cim-controller.md)。</span><span class="sxs-lookup"><span data-stu-id="1a071-470">The **CIM\_ManagementController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="1a071-471">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="1a071-471">WMI does not implement this class.</span></span>

<span data-ttu-id="1a071-472">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1a071-472">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1a071-473">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1a071-473">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a071-474">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a071-474">Requirements</span></span>



| <span data-ttu-id="1a071-475">需求</span><span class="sxs-lookup"><span data-stu-id="1a071-475">Requirement</span></span> | <span data-ttu-id="1a071-476">值</span><span class="sxs-lookup"><span data-stu-id="1a071-476">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a071-477">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a071-477">Minimum supported client</span></span><br/> | <span data-ttu-id="1a071-478">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a071-478">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a071-479">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a071-479">Minimum supported server</span></span><br/> | <span data-ttu-id="1a071-480">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a071-480">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a071-481">命名空間</span><span class="sxs-lookup"><span data-stu-id="1a071-481">Namespace</span></span><br/>                | <span data-ttu-id="1a071-482">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1a071-482">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a071-483">MOF</span><span class="sxs-lookup"><span data-stu-id="1a071-483">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a071-484"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a071-484"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a071-485">DLL</span><span class="sxs-lookup"><span data-stu-id="1a071-485">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a071-486"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a071-486"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a071-487">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a071-487">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a071-488">**CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="1a071-488">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

