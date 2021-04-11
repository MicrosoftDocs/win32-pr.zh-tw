---
description: CIM \_ DiskDrive 類別代表作業系統所見的實體磁片磁碟機。
ms.assetid: 3a63506e-455e-4108-b0c7-03b2af249d61
ms.tgt_platform: multiple
title: 'CIM_DiskDrive 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskDrive
- CIM_DiskDrive.Availability
- CIM_DiskDrive.Capabilities
- CIM_DiskDrive.CapabilityDescriptions
- CIM_DiskDrive.Caption
- CIM_DiskDrive.CompressionMethod
- CIM_DiskDrive.ConfigManagerErrorCode
- CIM_DiskDrive.ConfigManagerUserConfig
- CIM_DiskDrive.CreationClassName
- CIM_DiskDrive.DefaultBlockSize
- CIM_DiskDrive.Description
- CIM_DiskDrive.DeviceID
- CIM_DiskDrive.ErrorCleared
- CIM_DiskDrive.ErrorDescription
- CIM_DiskDrive.ErrorMethodology
- CIM_DiskDrive.InstallDate
- CIM_DiskDrive.LastErrorCode
- CIM_DiskDrive.MaxBlockSize
- CIM_DiskDrive.MaxMediaSize
- CIM_DiskDrive.MinBlockSize
- CIM_DiskDrive.Name
- CIM_DiskDrive.NeedsCleaning
- CIM_DiskDrive.NumberOfMediaSupported
- CIM_DiskDrive.PNPDeviceID
- CIM_DiskDrive.PowerManagementCapabilities
- CIM_DiskDrive.PowerManagementSupported
- CIM_DiskDrive.Status
- CIM_DiskDrive.StatusInfo
- CIM_DiskDrive.SystemCreationClassName
- CIM_DiskDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c68e8fc53898220737f473cc0c13f43d7ad471b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190972"
---
# <a name="cim_diskdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="b12c5-103">CIM_DiskDrive 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="b12c5-103">CIM_DiskDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b12c5-104">**CIM \_ DiskDrive** 類別代表作業系統所見的實體磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b12c5-104">The **CIM\_DiskDrive** class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="b12c5-105">磁片磁碟機功能對應到磁片磁碟機的邏輯和管理特性，在某些情況下，可能不會反映裝置的實體特性。</span><span class="sxs-lookup"><span data-stu-id="b12c5-105">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="b12c5-106">實體磁片磁碟機的介面是此類別的成員。</span><span class="sxs-lookup"><span data-stu-id="b12c5-106">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="b12c5-107">不過，根據另一個邏輯裝置的物件不是此類別的成員。</span><span class="sxs-lookup"><span data-stu-id="b12c5-107">However, an object based on another logical device is not a member of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b12c5-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b12c5-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b12c5-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b12c5-110">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b12c5-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b12c5-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="b12c5-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b12c5-112">語法</span><span class="sxs-lookup"><span data-stu-id="b12c5-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskDrive : CIM_MediaAccessDevice
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="b12c5-113">成員</span><span class="sxs-lookup"><span data-stu-id="b12c5-113">Members</span></span>

<span data-ttu-id="b12c5-114">**CIM \_ DiskDrive** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b12c5-114">The **CIM\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="b12c5-115">方法</span><span class="sxs-lookup"><span data-stu-id="b12c5-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="b12c5-116">屬性</span><span class="sxs-lookup"><span data-stu-id="b12c5-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b12c5-117">方法</span><span class="sxs-lookup"><span data-stu-id="b12c5-117">Methods</span></span>

<span data-ttu-id="b12c5-118">**CIM \_ DiskDrive** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b12c5-118">The **CIM\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="b12c5-119">方法</span><span class="sxs-lookup"><span data-stu-id="b12c5-119">Method</span></span>                                                                | <span data-ttu-id="b12c5-120">描述</span><span class="sxs-lookup"><span data-stu-id="b12c5-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b12c5-121">**重設**</span><span class="sxs-lookup"><span data-stu-id="b12c5-121">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="b12c5-122">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="b12c5-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="b12c5-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="b12c5-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b12c5-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b12c5-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="b12c5-125">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="b12c5-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b12c5-126">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="b12c5-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b12c5-127">屬性</span><span class="sxs-lookup"><span data-stu-id="b12c5-127">Properties</span></span>

<span data-ttu-id="b12c5-128">**CIM \_ DiskDrive** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b12c5-128">The **CIM\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b12c5-129">**可用性**</span><span class="sxs-lookup"><span data-stu-id="b12c5-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b12c5-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-132">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="b12c5-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-133">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="b12c5-133">Availability and status of the device.</span></span>

<span data-ttu-id="b12c5-134">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b12c5-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b12c5-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-136">其他。</span><span class="sxs-lookup"><span data-stu-id="b12c5-136">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b12c5-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="b12c5-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-138">不明。</span><span class="sxs-lookup"><span data-stu-id="b12c5-138">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b12c5-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="b12c5-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-140">執行中/完整電源。</span><span class="sxs-lookup"><span data-stu-id="b12c5-140">Running/full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b12c5-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="b12c5-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-142">警告。</span><span class="sxs-lookup"><span data-stu-id="b12c5-142">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b12c5-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="b12c5-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-144">測試。</span><span class="sxs-lookup"><span data-stu-id="b12c5-144">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b12c5-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="b12c5-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-146">不適用。</span><span class="sxs-lookup"><span data-stu-id="b12c5-146">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b12c5-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="b12c5-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-148">關閉電源。</span><span class="sxs-lookup"><span data-stu-id="b12c5-148">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b12c5-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="b12c5-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-150">離線。</span><span class="sxs-lookup"><span data-stu-id="b12c5-150">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b12c5-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="b12c5-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-152">關閉責任。</span><span class="sxs-lookup"><span data-stu-id="b12c5-152">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b12c5-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="b12c5-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-154">已降級。</span><span class="sxs-lookup"><span data-stu-id="b12c5-154">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b12c5-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="b12c5-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-156">未安裝。</span><span class="sxs-lookup"><span data-stu-id="b12c5-156">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b12c5-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="b12c5-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-158">安裝錯誤。</span><span class="sxs-lookup"><span data-stu-id="b12c5-158">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b12c5-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="b12c5-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-160">裝置已知處於省電模式，但在此模式中的確切狀態是未知的。</span><span class="sxs-lookup"><span data-stu-id="b12c5-160">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b12c5-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="b12c5-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-162">裝置處於省電狀態，但仍在運作中，而且可能會顯示效能下降。</span><span class="sxs-lookup"><span data-stu-id="b12c5-162">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b12c5-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="b12c5-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-164">裝置無法正常運作，但可能會進入完整電源「快速」。</span><span class="sxs-lookup"><span data-stu-id="b12c5-164">Device is not functioning but could be brought to full power 'quickly'.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b12c5-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="b12c5-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-166">電源週期。</span><span class="sxs-lookup"><span data-stu-id="b12c5-166">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b12c5-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="b12c5-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-168">裝置處於警告狀態，也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="b12c5-168">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b12c5-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="b12c5-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-170">已暫停。</span><span class="sxs-lookup"><span data-stu-id="b12c5-170">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b12c5-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="b12c5-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-172">未就緒。</span><span class="sxs-lookup"><span data-stu-id="b12c5-172">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b12c5-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="b12c5-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-174">尚未設定。</span><span class="sxs-lookup"><span data-stu-id="b12c5-174">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b12c5-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="b12c5-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-176">磁片磁碟機無法使用。</span><span class="sxs-lookup"><span data-stu-id="b12c5-176">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b12c5-177">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="b12c5-177">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-178">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b12c5-178">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-180">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 儲存裝置 \| 001.9 "，" MIF。DMTF \| 儲存裝置 \| 001.11 "，" MIF。DMTF \| 儲存裝置 \| 001.12 "，" MIF。DMTF \| 磁片 \| 003.7 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**CapabilityDescriptions**") </span><span class="sxs-lookup"><span data-stu-id="b12c5-180">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-181">媒體存取裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="b12c5-181">Capabilities of the media access device.</span></span> <span data-ttu-id="b12c5-182">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-182">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b12c5-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b12c5-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-184">不明。</span><span class="sxs-lookup"><span data-stu-id="b12c5-184">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b12c5-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b12c5-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-186">其他。</span><span class="sxs-lookup"><span data-stu-id="b12c5-186">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="b12c5-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**順序存取** (2) </span><span class="sxs-lookup"><span data-stu-id="b12c5-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-188">順序存取。</span><span class="sxs-lookup"><span data-stu-id="b12c5-188">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="b12c5-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**隨機存取** (3) </span><span class="sxs-lookup"><span data-stu-id="b12c5-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-190">隨機存取。</span><span class="sxs-lookup"><span data-stu-id="b12c5-190">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="b12c5-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**支援寫入** (4) </span><span class="sxs-lookup"><span data-stu-id="b12c5-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-192">撰寫。</span><span class="sxs-lookup"><span data-stu-id="b12c5-192">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="b12c5-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**加密** (5) </span><span class="sxs-lookup"><span data-stu-id="b12c5-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-194">加密。</span><span class="sxs-lookup"><span data-stu-id="b12c5-194">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="b12c5-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**壓縮** (6) </span><span class="sxs-lookup"><span data-stu-id="b12c5-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-196">壓縮。</span><span class="sxs-lookup"><span data-stu-id="b12c5-196">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="b12c5-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**支援卸除式媒體** (7) </span><span class="sxs-lookup"><span data-stu-id="b12c5-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-198">卸除式媒體。</span><span class="sxs-lookup"><span data-stu-id="b12c5-198">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="b12c5-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**手動清除** (8) </span><span class="sxs-lookup"><span data-stu-id="b12c5-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-200">手動清除。</span><span class="sxs-lookup"><span data-stu-id="b12c5-200">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="b12c5-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**自動清除** (9) </span><span class="sxs-lookup"><span data-stu-id="b12c5-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-202">自動清除。</span><span class="sxs-lookup"><span data-stu-id="b12c5-202">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="b12c5-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**智慧型通知** (10) </span><span class="sxs-lookup"><span data-stu-id="b12c5-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-204">智慧型通知。</span><span class="sxs-lookup"><span data-stu-id="b12c5-204">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="b12c5-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**支援雙側媒體** (11) </span><span class="sxs-lookup"><span data-stu-id="b12c5-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-206">區分可以從唯讀取一側的裝置存取雙面媒體兩側，且需要開啟媒體的裝置。</span><span class="sxs-lookup"><span data-stu-id="b12c5-206">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="b12c5-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**不需要 Predismount 退出** (12) </span><span class="sxs-lookup"><span data-stu-id="b12c5-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-208">表示不需要明確地從裝置上取出媒體，即可透過選擇器元素來存取。</span><span class="sxs-lookup"><span data-stu-id="b12c5-208">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b12c5-209">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b12c5-209">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-210">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b12c5-210">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-212">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。**功能**") </span><span class="sxs-lookup"><span data-stu-id="b12c5-212">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-213">自由格式字串的陣列，提供 **功能** 陣列中指出之存取裝置功能的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="b12c5-213">Array of free-form strings that provide detailed explanations for access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="b12c5-214">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

> [!Note]  
> <span data-ttu-id="b12c5-215">這個陣列的每個專案都與位於相同索引的 **功能** 陣列中的專案相關。</span><span class="sxs-lookup"><span data-stu-id="b12c5-215">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="b12c5-216">**標題**</span><span class="sxs-lookup"><span data-stu-id="b12c5-216">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-219">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-220">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="b12c5-220">Short textual description of the object.</span></span>

<span data-ttu-id="b12c5-221">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-222">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="b12c5-222">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-223">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-225">自由格式字串，表示用來壓縮邏輯檔案的演算法或工具。</span><span class="sxs-lookup"><span data-stu-id="b12c5-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="b12c5-226">如果壓縮配置未知或未描述，請使用「未知」。</span><span class="sxs-lookup"><span data-stu-id="b12c5-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="b12c5-227">如果已壓縮邏輯檔案，但壓縮配置未知或未描述，請使用「壓縮」。</span><span class="sxs-lookup"><span data-stu-id="b12c5-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="b12c5-228">如果邏輯檔案未壓縮，請使用「未壓縮」。</span><span class="sxs-lookup"><span data-stu-id="b12c5-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="b12c5-229">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-229">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="b12c5-230"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-230">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-231">壓縮配置未知或未描述。</span><span class="sxs-lookup"><span data-stu-id="b12c5-231">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="b12c5-232"> ( 「壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-232">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-233">邏輯檔案已壓縮，但壓縮配置未知或未描述</span><span class="sxs-lookup"><span data-stu-id="b12c5-233">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="b12c5-234"> ( 「未壓縮」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-234">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-235">如果邏輯檔案未壓縮</span><span class="sxs-lookup"><span data-stu-id="b12c5-235">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b12c5-236">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b12c5-236">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-237">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b12c5-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-239">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-240">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b12c5-240">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b12c5-241">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-241">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b12c5-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b12c5-243"> (0)</span><span class="sxs-lookup"><span data-stu-id="b12c5-243">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-244">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="b12c5-244">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b12c5-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b12c5-246">(1)</span><span class="sxs-lookup"><span data-stu-id="b12c5-246">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-247">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="b12c5-247">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b12c5-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b12c5-249">(2)</span><span class="sxs-lookup"><span data-stu-id="b12c5-249">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b12c5-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b12c5-251">(3)</span><span class="sxs-lookup"><span data-stu-id="b12c5-251">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-252">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="b12c5-252">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b12c5-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b12c5-254">(4)</span><span class="sxs-lookup"><span data-stu-id="b12c5-254">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-255">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b12c5-255">Device is not working properly.</span></span> <span data-ttu-id="b12c5-256">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="b12c5-256">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b12c5-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b12c5-258">(5)</span><span class="sxs-lookup"><span data-stu-id="b12c5-258">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-259">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="b12c5-259">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b12c5-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b12c5-261">(6)</span><span class="sxs-lookup"><span data-stu-id="b12c5-261">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-262">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="b12c5-262">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b12c5-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b12c5-264">(7)</span><span class="sxs-lookup"><span data-stu-id="b12c5-264">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b12c5-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b12c5-266">(8)</span><span class="sxs-lookup"><span data-stu-id="b12c5-266">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-267">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="b12c5-267">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b12c5-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b12c5-269">(9)</span><span class="sxs-lookup"><span data-stu-id="b12c5-269">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-270">裝置無法正常運作;控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="b12c5-270">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b12c5-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b12c5-272">(10)</span><span class="sxs-lookup"><span data-stu-id="b12c5-272">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-273">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="b12c5-273">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b12c5-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b12c5-275">(11)</span><span class="sxs-lookup"><span data-stu-id="b12c5-275">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-276">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="b12c5-276">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b12c5-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b12c5-278"> (12) </span><span class="sxs-lookup"><span data-stu-id="b12c5-278">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-279">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="b12c5-279">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b12c5-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b12c5-281">(13)</span><span class="sxs-lookup"><span data-stu-id="b12c5-281">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-282">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="b12c5-282">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b12c5-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b12c5-284">(14)</span><span class="sxs-lookup"><span data-stu-id="b12c5-284">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-285">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b12c5-285">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b12c5-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b12c5-287">(15)</span><span class="sxs-lookup"><span data-stu-id="b12c5-287">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-288">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="b12c5-288">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b12c5-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b12c5-290">(16)</span><span class="sxs-lookup"><span data-stu-id="b12c5-290">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-291">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="b12c5-291">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b12c5-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b12c5-293">(17)</span><span class="sxs-lookup"><span data-stu-id="b12c5-293">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-294">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="b12c5-294">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b12c5-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b12c5-296">(18)</span><span class="sxs-lookup"><span data-stu-id="b12c5-296">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-297">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b12c5-297">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b12c5-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b12c5-299">(19)</span><span class="sxs-lookup"><span data-stu-id="b12c5-299">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b12c5-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b12c5-301">(20)</span><span class="sxs-lookup"><span data-stu-id="b12c5-301">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-302">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="b12c5-302">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b12c5-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b12c5-304">(21)</span><span class="sxs-lookup"><span data-stu-id="b12c5-304">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-305">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="b12c5-305">System failure.</span></span> <span data-ttu-id="b12c5-306">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="b12c5-306">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b12c5-307">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="b12c5-307">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b12c5-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b12c5-309">(22)</span><span class="sxs-lookup"><span data-stu-id="b12c5-309">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-310">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="b12c5-310">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b12c5-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b12c5-312">(23)</span><span class="sxs-lookup"><span data-stu-id="b12c5-312">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-313">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="b12c5-313">System failure.</span></span> <span data-ttu-id="b12c5-314">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="b12c5-314">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b12c5-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b12c5-316">(24)</span><span class="sxs-lookup"><span data-stu-id="b12c5-316">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-317">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b12c5-317">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b12c5-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b12c5-319">(25)</span><span class="sxs-lookup"><span data-stu-id="b12c5-319">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-320">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="b12c5-320">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b12c5-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b12c5-322">(26)</span><span class="sxs-lookup"><span data-stu-id="b12c5-322">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-323">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="b12c5-323">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b12c5-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b12c5-325">(27)</span><span class="sxs-lookup"><span data-stu-id="b12c5-325">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-326">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="b12c5-326">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b12c5-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b12c5-328">(28)</span><span class="sxs-lookup"><span data-stu-id="b12c5-328">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-329">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b12c5-329">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b12c5-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b12c5-331">(29)</span><span class="sxs-lookup"><span data-stu-id="b12c5-331">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-332">裝置已停用;裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="b12c5-332">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b12c5-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b12c5-334">(30)</span><span class="sxs-lookup"><span data-stu-id="b12c5-334">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-335">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="b12c5-335">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b12c5-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="b12c5-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b12c5-337"> (31) </span><span class="sxs-lookup"><span data-stu-id="b12c5-337">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-338">裝置無法正常運作;Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b12c5-338">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b12c5-339">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b12c5-339">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-340">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b12c5-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-342">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-343">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="b12c5-343">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b12c5-344">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-345">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b12c5-345">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-348">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b12c5-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-349">建立實例時所使用)  (或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="b12c5-349">Name of the class (or subclass) used in the creation of an instance.</span></span> <span data-ttu-id="b12c5-350">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="b12c5-350">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b12c5-351">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-352">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b12c5-352">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-353">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b12c5-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-355">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-355">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-356">裝置的預設區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b12c5-356">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="b12c5-357">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-357">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b12c5-358">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-359">**說明**</span><span class="sxs-lookup"><span data-stu-id="b12c5-359">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-362">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-363">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="b12c5-363">Textual description of the object.</span></span>

<span data-ttu-id="b12c5-364">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-365">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b12c5-365">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-366">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-368">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b12c5-368">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-369">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="b12c5-369">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b12c5-370">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-371">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b12c5-371">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-372">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b12c5-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-374">若 **為 TRUE**，則會清除 **LastErrorCode** 屬性中所報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b12c5-374">If **TRUE**, the error reported in the **LastErrorCode** property is cleared.</span></span>

<span data-ttu-id="b12c5-375">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-376">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b12c5-376">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-377">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-378">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-379">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="b12c5-379">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b12c5-380">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-380">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-381">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="b12c5-381">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-384">描述裝置所支援之錯誤偵測和更正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="b12c5-384">Free-form string that describes the type of error detection and correction supported by the device.</span></span>

<span data-ttu-id="b12c5-385">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-385">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-386">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b12c5-386">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-387">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b12c5-387">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-389">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="b12c5-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-390">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b12c5-390">Date and time when the object was installed.</span></span> <span data-ttu-id="b12c5-391">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="b12c5-391">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b12c5-392">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b12c5-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-394">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b12c5-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-396">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b12c5-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b12c5-397">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-398">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b12c5-398">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-399">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b12c5-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-400">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-401">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-402">裝置所存取媒體的最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b12c5-402">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="b12c5-403">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b12c5-404">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-405">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="b12c5-405">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-406">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b12c5-406">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-407">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-408">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 順序存取裝置 \| 001.2 「) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-409">裝置所支援媒體的大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="b12c5-409">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="b12c5-410">Kb 會被視為位元組數目乘以 1000 (而不是位元組數乘以 1024) 。</span><span class="sxs-lookup"><span data-stu-id="b12c5-410">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="b12c5-411">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b12c5-412">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-413">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="b12c5-413">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-414">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b12c5-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-416">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-417">裝置所存取媒體的區塊大小下限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b12c5-417">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="b12c5-418">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b12c5-419">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-420">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b12c5-420">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-423">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-423">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-424">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="b12c5-424">Label by which the object is known.</span></span> <span data-ttu-id="b12c5-425">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="b12c5-425">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b12c5-426">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-427">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="b12c5-427">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-428">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b12c5-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-430">若 **為 TRUE**，則媒體存取裝置需要清除。</span><span class="sxs-lookup"><span data-stu-id="b12c5-430">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="b12c5-431">在 [ **功能** 陣列] 屬性中，是否可能指出手動或自動清除。</span><span class="sxs-lookup"><span data-stu-id="b12c5-431">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="b12c5-432">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-432">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-433">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="b12c5-433">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-434">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b12c5-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-436">當媒體存取裝置支援多個個別媒體時，這個屬性會定義可支援或插入的最大數目。</span><span class="sxs-lookup"><span data-stu-id="b12c5-436">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="b12c5-437">這個屬性繼承自 [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-437">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-438">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b12c5-438">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-439">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-441">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-441">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-442">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b12c5-442">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b12c5-443">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b12c5-444">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b12c5-444">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-445">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b12c5-445">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-446">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b12c5-446">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-448">邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="b12c5-448">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="b12c5-449">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b12c5-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b12c5-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-451">不明。</span><span class="sxs-lookup"><span data-stu-id="b12c5-451">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b12c5-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="b12c5-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-453">不支援。</span><span class="sxs-lookup"><span data-stu-id="b12c5-453">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b12c5-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="b12c5-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-455">停用。</span><span class="sxs-lookup"><span data-stu-id="b12c5-455">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b12c5-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="b12c5-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-457">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="b12c5-457">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b12c5-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="b12c5-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-459">裝置可以根據使用或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="b12c5-459">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b12c5-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="b12c5-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-461">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b12c5-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b12c5-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="b12c5-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-463">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="b12c5-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b12c5-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="b12c5-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b12c5-465">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="b12c5-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b12c5-466">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b12c5-466">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-467">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b12c5-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-468">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-469">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="b12c5-469">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b12c5-470">如果 **為 False**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="b12c5-470">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b12c5-471">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="b12c5-471">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b12c5-472">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="b12c5-472">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b12c5-473">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-474">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b12c5-474">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-475">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-476">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-477">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-478">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b12c5-478">Current status of the object.</span></span>

<span data-ttu-id="b12c5-479">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-479">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b12c5-480">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="b12c5-480">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b12c5-481">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-481">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b12c5-482">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-482">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b12c5-483">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-483">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b12c5-484">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-484">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b12c5-485">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-485">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b12c5-486">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-486">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b12c5-487">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-487">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b12c5-488">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-488">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b12c5-489">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-489">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b12c5-490">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-490">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b12c5-491">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-491">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b12c5-492">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="b12c5-492">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b12c5-493">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b12c5-493">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-494">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b12c5-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-495">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-496">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="b12c5-496">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-497">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="b12c5-497">State of the logical device.</span></span> <span data-ttu-id="b12c5-498">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="b12c5-498">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b12c5-499">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-499">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b12c5-500">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b12c5-500">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b12c5-501">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="b12c5-501">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b12c5-502">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="b12c5-502">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b12c5-503">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="b12c5-503">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b12c5-504">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="b12c5-504">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b12c5-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b12c5-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-506">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-508">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b12c5-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-509">設定系統的 **CreationClassName** 屬性範圍。</span><span class="sxs-lookup"><span data-stu-id="b12c5-509">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="b12c5-510">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12c5-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b12c5-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b12c5-512">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b12c5-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-513">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b12c5-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b12c5-514">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b12c5-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b12c5-515">範圍系統的 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b12c5-515">Scoping system's **Name** property.</span></span>

<span data-ttu-id="b12c5-516">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b12c5-517">備註</span><span class="sxs-lookup"><span data-stu-id="b12c5-517">Remarks</span></span>

<span data-ttu-id="b12c5-518">**Cim \_ DiskDrive** 類別衍生自 [**cim \_ MediaAccessDevice**](cim-mediaaccessdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-518">The **CIM\_DiskDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b12c5-519">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="b12c5-519">WMI does not implement this class.</span></span> <span data-ttu-id="b12c5-520">請參閱衍生自 **CIM \_ DiskDrive** 之類別的 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="b12c5-520">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_DiskDrive**.</span></span>

<span data-ttu-id="b12c5-521">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b12c5-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b12c5-522">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b12c5-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b12c5-523">規格需求</span><span class="sxs-lookup"><span data-stu-id="b12c5-523">Requirements</span></span>



| <span data-ttu-id="b12c5-524">需求</span><span class="sxs-lookup"><span data-stu-id="b12c5-524">Requirement</span></span> | <span data-ttu-id="b12c5-525">值</span><span class="sxs-lookup"><span data-stu-id="b12c5-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b12c5-526">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b12c5-526">Minimum supported client</span></span><br/> | <span data-ttu-id="b12c5-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b12c5-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b12c5-528">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b12c5-528">Minimum supported server</span></span><br/> | <span data-ttu-id="b12c5-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b12c5-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b12c5-530">命名空間</span><span class="sxs-lookup"><span data-stu-id="b12c5-530">Namespace</span></span><br/>                | <span data-ttu-id="b12c5-531">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b12c5-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b12c5-532">MOF</span><span class="sxs-lookup"><span data-stu-id="b12c5-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b12c5-533"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b12c5-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b12c5-534">DLL</span><span class="sxs-lookup"><span data-stu-id="b12c5-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b12c5-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b12c5-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b12c5-536">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b12c5-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b12c5-537">**CIM \_ MediaAccessDevice**</span><span class="sxs-lookup"><span data-stu-id="b12c5-537">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

