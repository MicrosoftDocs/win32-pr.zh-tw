---
description: CIM \_ AggregatePSExtent 類別會定義單一儲存裝置上可定址的邏輯區塊數目，但不包括對應為檢查資料的邏輯區塊。
ms.assetid: 6c188955-a963-414d-94f9-b7e1cb5960ed
ms.tgt_platform: multiple
title: CIM_AggregatePSExtent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent
- CIM_AggregatePSExtent.Caption
- CIM_AggregatePSExtent.Description
- CIM_AggregatePSExtent.InstallDate
- CIM_AggregatePSExtent.Name
- CIM_AggregatePSExtent.Status
- CIM_AggregatePSExtent.Availability
- CIM_AggregatePSExtent.ConfigManagerErrorCode
- CIM_AggregatePSExtent.ConfigManagerUserConfig
- CIM_AggregatePSExtent.CreationClassName
- CIM_AggregatePSExtent.DeviceID
- CIM_AggregatePSExtent.PowerManagementCapabilities
- CIM_AggregatePSExtent.ErrorCleared
- CIM_AggregatePSExtent.ErrorDescription
- CIM_AggregatePSExtent.LastErrorCode
- CIM_AggregatePSExtent.PNPDeviceID
- CIM_AggregatePSExtent.PowerManagementSupported
- CIM_AggregatePSExtent.StatusInfo
- CIM_AggregatePSExtent.SystemCreationClassName
- CIM_AggregatePSExtent.SystemName
- CIM_AggregatePSExtent.Access
- CIM_AggregatePSExtent.BlockSize
- CIM_AggregatePSExtent.ErrorMethodology
- CIM_AggregatePSExtent.NumberOfBlocks
- CIM_AggregatePSExtent.Purpose
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: edc3f5b91bc39e18321778dbfdbc53446c6c27d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689036"
---
# <a name="cim_aggregatepsextent-class"></a><span data-ttu-id="78cbf-103">CIM \_ AggregatePSExtent 類別</span><span class="sxs-lookup"><span data-stu-id="78cbf-103">CIM\_AggregatePSExtent class</span></span>

<span data-ttu-id="78cbf-104">**CIM \_ AggregatePSExtent** 類別會定義單一儲存裝置上可定址的邏輯區塊數目，但不包括對應為檢查資料的邏輯區塊。</span><span class="sxs-lookup"><span data-stu-id="78cbf-104">The **CIM\_AggregatePSExtent** class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="78cbf-105">如果已定義磁片區集，則邏輯區塊會包含在單一磁片區集合中。</span><span class="sxs-lookup"><span data-stu-id="78cbf-105">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="78cbf-106">當只需要摘要資訊或使用自動設定時，這是 [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)的替代群組。</span><span class="sxs-lookup"><span data-stu-id="78cbf-106">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

<span data-ttu-id="78cbf-107">自動設定可能會導致定義上千個 [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="78cbf-107">Automatic configuration can result in thousands of [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) classes being defined.</span></span> <span data-ttu-id="78cbf-108">已定義 **CIM \_ AggregatePSExtent** 類別，因此不需要模型化個別範圍。</span><span class="sxs-lookup"><span data-stu-id="78cbf-108">The **CIM\_AggregatePSExtent** class was defined so that individual extents would not have to be modeled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78cbf-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="78cbf-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="78cbf-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="78cbf-111">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="78cbf-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="78cbf-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="78cbf-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="78cbf-113">語法</span><span class="sxs-lookup"><span data-stu-id="78cbf-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D0E255C-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AggregatePSExtent : CIM_StorageExtent
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
  uint16   Access;
  uint64   BlockSize;
  string   ErrorMethodology;
  uint64   NumberOfBlocks;
  string   Purpose;
};
```

## <a name="members"></a><span data-ttu-id="78cbf-114">成員</span><span class="sxs-lookup"><span data-stu-id="78cbf-114">Members</span></span>

<span data-ttu-id="78cbf-115">**CIM \_ AggregatePSExtent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="78cbf-115">The **CIM\_AggregatePSExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="78cbf-116">方法</span><span class="sxs-lookup"><span data-stu-id="78cbf-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="78cbf-117">屬性</span><span class="sxs-lookup"><span data-stu-id="78cbf-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="78cbf-118">方法</span><span class="sxs-lookup"><span data-stu-id="78cbf-118">Methods</span></span>

<span data-ttu-id="78cbf-119">**CIM \_ AggregatePSExtent** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="78cbf-119">The **CIM\_AggregatePSExtent** class has these methods.</span></span>



| <span data-ttu-id="78cbf-120">方法</span><span class="sxs-lookup"><span data-stu-id="78cbf-120">Method</span></span>                                                                       | <span data-ttu-id="78cbf-121">描述</span><span class="sxs-lookup"><span data-stu-id="78cbf-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78cbf-122">**重設**</span><span class="sxs-lookup"><span data-stu-id="78cbf-122">**Reset**</span></span>](reset-method-in-class-cim-aggregatepsextent.md)                 | <span data-ttu-id="78cbf-123">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="78cbf-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="78cbf-124">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="78cbf-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="78cbf-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="78cbf-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepsextent.md) | <span data-ttu-id="78cbf-126">定義邏輯裝置的預期電源狀態，以及裝置何時應進入該狀態。</span><span class="sxs-lookup"><span data-stu-id="78cbf-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="78cbf-127">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="78cbf-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="78cbf-128">屬性</span><span class="sxs-lookup"><span data-stu-id="78cbf-128">Properties</span></span>

<span data-ttu-id="78cbf-129">**CIM \_ AggregatePSExtent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="78cbf-129">The **CIM\_AggregatePSExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78cbf-130">**存取**</span><span class="sxs-lookup"><span data-stu-id="78cbf-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="78cbf-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-133">描述媒體的讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="78cbf-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="78cbf-134">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78cbf-135">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="78cbf-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="78cbf-136">**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="78cbf-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="78cbf-137">可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="78cbf-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="78cbf-138">支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="78cbf-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="78cbf-139">**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="78cbf-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78cbf-140">**可用性**</span><span class="sxs-lookup"><span data-stu-id="78cbf-140">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-141">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="78cbf-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-143">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="78cbf-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-144">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="78cbf-144">Availability and status of the device.</span></span>

<span data-ttu-id="78cbf-145">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-145">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78cbf-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="78cbf-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78cbf-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="78cbf-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="78cbf-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="78cbf-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="78cbf-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="78cbf-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="78cbf-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="78cbf-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="78cbf-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="78cbf-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="78cbf-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="78cbf-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="78cbf-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="78cbf-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="78cbf-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="78cbf-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="78cbf-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="78cbf-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="78cbf-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="78cbf-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="78cbf-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="78cbf-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="78cbf-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="78cbf-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-159">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="78cbf-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="78cbf-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="78cbf-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-161">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="78cbf-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="78cbf-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="78cbf-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-163">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="78cbf-163">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="78cbf-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="78cbf-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="78cbf-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="78cbf-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-166">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="78cbf-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="78cbf-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="78cbf-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-168">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="78cbf-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="78cbf-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="78cbf-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-170">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="78cbf-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="78cbf-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="78cbf-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-172">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="78cbf-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="78cbf-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="78cbf-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-174">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="78cbf-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78cbf-175">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="78cbf-175">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-176">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="78cbf-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-177">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-178">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="78cbf-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-179">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="78cbf-179">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="78cbf-180">如果變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="78cbf-180">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="78cbf-181">如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="78cbf-181">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="78cbf-182">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="78cbf-183">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-183">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-184">**標題**</span><span class="sxs-lookup"><span data-stu-id="78cbf-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-187">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-188">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="78cbf-188">A short textual description of the object.</span></span>

<span data-ttu-id="78cbf-189">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-190">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="78cbf-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-191">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="78cbf-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-193">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-194">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="78cbf-194">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="78cbf-195">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="78cbf-196">**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-196">**This device is working properly.**</span></span> <span data-ttu-id="78cbf-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="78cbf-197">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="78cbf-198">**這個裝置並未正確設定。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-198">**This device is not configured correctly.**</span></span> <span data-ttu-id="78cbf-199">(1)</span><span class="sxs-lookup"><span data-stu-id="78cbf-199">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="78cbf-200">**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-200">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="78cbf-201">(2)</span><span class="sxs-lookup"><span data-stu-id="78cbf-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="78cbf-202">**這個裝置的驅動程式可能已損毀，或您系統的記憶體或其他資源可能不足。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-202">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="78cbf-203">(3)</span><span class="sxs-lookup"><span data-stu-id="78cbf-203">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="78cbf-204">**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-204">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="78cbf-205">(4)</span><span class="sxs-lookup"><span data-stu-id="78cbf-205">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="78cbf-206">**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-206">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="78cbf-207">(5)</span><span class="sxs-lookup"><span data-stu-id="78cbf-207">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="78cbf-208">**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-208">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="78cbf-209">(6)</span><span class="sxs-lookup"><span data-stu-id="78cbf-209">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="78cbf-210">**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-210">**Cannot filter.**</span></span> <span data-ttu-id="78cbf-211">(7)</span><span class="sxs-lookup"><span data-stu-id="78cbf-211">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="78cbf-212">**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-212">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="78cbf-213">(8)</span><span class="sxs-lookup"><span data-stu-id="78cbf-213">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="78cbf-214">**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-214">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="78cbf-215">(9)</span><span class="sxs-lookup"><span data-stu-id="78cbf-215">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="78cbf-216">**這個裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-216">**This device cannot start.**</span></span> <span data-ttu-id="78cbf-217">(10)</span><span class="sxs-lookup"><span data-stu-id="78cbf-217">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="78cbf-218">**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-218">**This device failed.**</span></span> <span data-ttu-id="78cbf-219">(11)</span><span class="sxs-lookup"><span data-stu-id="78cbf-219">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="78cbf-220">**這個裝置沒有足夠資源可供使用。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-220">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="78cbf-221"> (12) </span><span class="sxs-lookup"><span data-stu-id="78cbf-221">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="78cbf-222">**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-222">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="78cbf-223">(13)</span><span class="sxs-lookup"><span data-stu-id="78cbf-223">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="78cbf-224">**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-224">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="78cbf-225">(14)</span><span class="sxs-lookup"><span data-stu-id="78cbf-225">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="78cbf-226">**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-226">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="78cbf-227">(15)</span><span class="sxs-lookup"><span data-stu-id="78cbf-227">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="78cbf-228">**Windows 無法識別這個裝置所使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-228">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="78cbf-229">(16)</span><span class="sxs-lookup"><span data-stu-id="78cbf-229">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="78cbf-230">**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-230">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="78cbf-231">(17)</span><span class="sxs-lookup"><span data-stu-id="78cbf-231">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="78cbf-232">**重新安裝這個裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-232">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="78cbf-233">(18)</span><span class="sxs-lookup"><span data-stu-id="78cbf-233">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="78cbf-234">**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-234">**Failure using the VxD loader.**</span></span> <span data-ttu-id="78cbf-235">(19)</span><span class="sxs-lookup"><span data-stu-id="78cbf-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="78cbf-236">**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-236">**Your registry might be corrupted.**</span></span> <span data-ttu-id="78cbf-237">(20)</span><span class="sxs-lookup"><span data-stu-id="78cbf-237">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="78cbf-238">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-238">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="78cbf-239">(21)</span><span class="sxs-lookup"><span data-stu-id="78cbf-239">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="78cbf-240">**這個裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-240">**This device is disabled.**</span></span> <span data-ttu-id="78cbf-241">(22)</span><span class="sxs-lookup"><span data-stu-id="78cbf-241">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="78cbf-242">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-242">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="78cbf-243">(23)</span><span class="sxs-lookup"><span data-stu-id="78cbf-243">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="78cbf-244">**這個裝置可能不存在、運作不正確、或並未安裝所有的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-244">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="78cbf-245">(24)</span><span class="sxs-lookup"><span data-stu-id="78cbf-245">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="78cbf-246">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="78cbf-247">(25)</span><span class="sxs-lookup"><span data-stu-id="78cbf-247">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="78cbf-248">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-248">**Windows is still setting up this device.**</span></span> <span data-ttu-id="78cbf-249">(26)</span><span class="sxs-lookup"><span data-stu-id="78cbf-249">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="78cbf-250">**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-250">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="78cbf-251">(27)</span><span class="sxs-lookup"><span data-stu-id="78cbf-251">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="78cbf-252">**這個裝置的驅動程式尚未安裝。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-252">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="78cbf-253">(28)</span><span class="sxs-lookup"><span data-stu-id="78cbf-253">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="78cbf-254">**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-254">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="78cbf-255">(29)</span><span class="sxs-lookup"><span data-stu-id="78cbf-255">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="78cbf-256">**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-256">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="78cbf-257">(30)</span><span class="sxs-lookup"><span data-stu-id="78cbf-257">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="78cbf-258">**這個裝置並未正確執行，因為 Windows 無法載入這個裝置必需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="78cbf-258">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="78cbf-259"> (31) </span><span class="sxs-lookup"><span data-stu-id="78cbf-259">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78cbf-260">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="78cbf-260">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-261">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="78cbf-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-263">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-263">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-264">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="78cbf-264">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="78cbf-265">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-266">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="78cbf-266">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-269">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78cbf-269">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-270">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="78cbf-270">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="78cbf-271">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="78cbf-271">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="78cbf-272">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-273">**說明**</span><span class="sxs-lookup"><span data-stu-id="78cbf-273">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-276">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-277">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="78cbf-277">A textual description of the object.</span></span>

<span data-ttu-id="78cbf-278">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-278">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-279">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="78cbf-279">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-280">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-282">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78cbf-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-283">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="78cbf-283">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="78cbf-284">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-285">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="78cbf-285">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-286">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="78cbf-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-288">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="78cbf-288">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="78cbf-289">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-290">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="78cbf-290">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-291">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-293">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="78cbf-293">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="78cbf-294">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-295">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="78cbf-295">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-296">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-298">描述儲存範圍所支援之錯誤偵測和更正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="78cbf-298">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="78cbf-299">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-299">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="78cbf-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-301">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="78cbf-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-303">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="78cbf-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-304">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="78cbf-304">Indicates when the object was installed.</span></span> <span data-ttu-id="78cbf-305">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="78cbf-305">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="78cbf-306">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-307">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="78cbf-307">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-308">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="78cbf-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-310">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="78cbf-310">Last error code reported by the logical device.</span></span>

<span data-ttu-id="78cbf-311">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-312">**名稱**</span><span class="sxs-lookup"><span data-stu-id="78cbf-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-315">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-315">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-316">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="78cbf-316">Label by which the object is known.</span></span> <span data-ttu-id="78cbf-317">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="78cbf-317">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="78cbf-318">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-319">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="78cbf-319">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-320">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="78cbf-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-322">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="78cbf-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-323">連續區塊的數目，每個區塊會封鎖 **區塊** 屬性中包含的值大小，以形成儲存區。</span><span class="sxs-lookup"><span data-stu-id="78cbf-323">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="78cbf-324">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="78cbf-324">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="78cbf-325">如果 **區塊** 的值是 1 (一個) ，此屬性就是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="78cbf-325">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="78cbf-326">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-326">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="78cbf-327">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-327">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-328">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="78cbf-328">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-331">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-332">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="78cbf-332">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="78cbf-333">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="78cbf-333">Example: "\*PNP030b"</span></span>

<span data-ttu-id="78cbf-334">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="78cbf-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-336">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="78cbf-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-338">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="78cbf-338">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="78cbf-339">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78cbf-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="78cbf-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-341">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="78cbf-341">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="78cbf-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="78cbf-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-343">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="78cbf-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="78cbf-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="78cbf-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-345">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="78cbf-345">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="78cbf-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="78cbf-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-347">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="78cbf-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="78cbf-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="78cbf-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-349">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="78cbf-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="78cbf-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="78cbf-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-351">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="78cbf-351">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="78cbf-352">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="78cbf-352">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="78cbf-353">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="78cbf-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="78cbf-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-355">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="78cbf-355">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="78cbf-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="78cbf-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="78cbf-357">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="78cbf-357">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="78cbf-358">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="78cbf-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-359">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="78cbf-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-360">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-361">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="78cbf-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="78cbf-362">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="78cbf-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="78cbf-363">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="78cbf-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="78cbf-364">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="78cbf-364">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="78cbf-365">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-366">**目的**</span><span class="sxs-lookup"><span data-stu-id="78cbf-366">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-367">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-368">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-369">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="78cbf-369">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="78cbf-370">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-370">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-371">**狀態**</span><span class="sxs-lookup"><span data-stu-id="78cbf-371">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-372">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-374">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-375">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="78cbf-375">String that indicates the current status of the object.</span></span> <span data-ttu-id="78cbf-376">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="78cbf-376">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="78cbf-377">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="78cbf-377">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="78cbf-378">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="78cbf-378">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="78cbf-379">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="78cbf-379">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="78cbf-380">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="78cbf-380">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="78cbf-381">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="78cbf-381">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="78cbf-382">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-382">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="78cbf-383">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="78cbf-383">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="78cbf-384">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-384">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="78cbf-385">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-385">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="78cbf-386">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-386">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78cbf-387">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-387">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="78cbf-388">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-388">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="78cbf-389">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-389">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="78cbf-390">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-390">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="78cbf-391">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-391">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="78cbf-392">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-392">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="78cbf-393">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-393">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="78cbf-394">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-394">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="78cbf-395">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="78cbf-395">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78cbf-396">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="78cbf-396">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-397">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="78cbf-397">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-398">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-399">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="78cbf-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-400">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="78cbf-400">State of the logical device.</span></span> <span data-ttu-id="78cbf-401">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="78cbf-401">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="78cbf-402">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="78cbf-403">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="78cbf-403">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="78cbf-404">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="78cbf-404">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="78cbf-405">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="78cbf-405">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="78cbf-406">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="78cbf-406">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="78cbf-407">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="78cbf-407">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="78cbf-408">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="78cbf-408">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-409">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-411">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78cbf-411">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-412">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="78cbf-412">The scoping system's creation class name.</span></span>

<span data-ttu-id="78cbf-413">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="78cbf-414">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="78cbf-414">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78cbf-415">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="78cbf-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-416">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="78cbf-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78cbf-417">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="78cbf-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="78cbf-418">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="78cbf-418">The scoping system's name.</span></span>

<span data-ttu-id="78cbf-419">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78cbf-420">備註</span><span class="sxs-lookup"><span data-stu-id="78cbf-420">Remarks</span></span>

<span data-ttu-id="78cbf-421">**Cim \_ AggregatePSExtent** 類別衍生自 [**cim \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="78cbf-421">The **CIM\_AggregatePSExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="78cbf-422">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="78cbf-422">WMI does not implement this class.</span></span>

<span data-ttu-id="78cbf-423">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="78cbf-423">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="78cbf-424">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="78cbf-424">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="78cbf-425">規格需求</span><span class="sxs-lookup"><span data-stu-id="78cbf-425">Requirements</span></span>



| <span data-ttu-id="78cbf-426">需求</span><span class="sxs-lookup"><span data-stu-id="78cbf-426">Requirement</span></span> | <span data-ttu-id="78cbf-427">值</span><span class="sxs-lookup"><span data-stu-id="78cbf-427">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78cbf-428">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78cbf-428">Minimum supported client</span></span><br/> | <span data-ttu-id="78cbf-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78cbf-429">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78cbf-430">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78cbf-430">Minimum supported server</span></span><br/> | <span data-ttu-id="78cbf-431">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78cbf-431">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78cbf-432">命名空間</span><span class="sxs-lookup"><span data-stu-id="78cbf-432">Namespace</span></span><br/>                | <span data-ttu-id="78cbf-433">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="78cbf-433">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78cbf-434">MOF</span><span class="sxs-lookup"><span data-stu-id="78cbf-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78cbf-435"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="78cbf-435"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78cbf-436">DLL</span><span class="sxs-lookup"><span data-stu-id="78cbf-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78cbf-437"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78cbf-437"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78cbf-438">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78cbf-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78cbf-439">**CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="78cbf-439">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="78cbf-440">CIM 類別</span><span class="sxs-lookup"><span data-stu-id="78cbf-440">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

