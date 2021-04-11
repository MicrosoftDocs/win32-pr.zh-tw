---
description: CIM \_ VolatileStorage 類別代表 volatile 儲存體的功能和管理。
ms.assetid: c2f7e11e-d7e4-4709-be55-1c94a0b14010
ms.tgt_platform: multiple
title: CIM_VolatileStorage 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolatileStorage
- CIM_VolatileStorage.Access
- CIM_VolatileStorage.AdditionalErrorData
- CIM_VolatileStorage.Availability
- CIM_VolatileStorage.BlockSize
- CIM_VolatileStorage.Cacheable
- CIM_VolatileStorage.CacheType
- CIM_VolatileStorage.Caption
- CIM_VolatileStorage.ConfigManagerErrorCode
- CIM_VolatileStorage.ConfigManagerUserConfig
- CIM_VolatileStorage.CorrectableError
- CIM_VolatileStorage.CreationClassName
- CIM_VolatileStorage.Description
- CIM_VolatileStorage.DeviceID
- CIM_VolatileStorage.EndingAddress
- CIM_VolatileStorage.ErrorAccess
- CIM_VolatileStorage.ErrorAddress
- CIM_VolatileStorage.ErrorCleared
- CIM_VolatileStorage.ErrorData
- CIM_VolatileStorage.ErrorDataOrder
- CIM_VolatileStorage.ErrorDescription
- CIM_VolatileStorage.ErrorInfo
- CIM_VolatileStorage.ErrorMethodology
- CIM_VolatileStorage.ErrorResolution
- CIM_VolatileStorage.ErrorTime
- CIM_VolatileStorage.ErrorTransferSize
- CIM_VolatileStorage.InstallDate
- CIM_VolatileStorage.LastErrorCode
- CIM_VolatileStorage.Name
- CIM_VolatileStorage.NumberOfBlocks
- CIM_VolatileStorage.OtherErrorDescription
- CIM_VolatileStorage.PNPDeviceID
- CIM_VolatileStorage.PowerManagementCapabilities
- CIM_VolatileStorage.PowerManagementSupported
- CIM_VolatileStorage.Purpose
- CIM_VolatileStorage.StartingAddress
- CIM_VolatileStorage.Status
- CIM_VolatileStorage.StatusInfo
- CIM_VolatileStorage.SystemCreationClassName
- CIM_VolatileStorage.SystemLevelAddress
- CIM_VolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99add7401d92d82385a4182e466de8b28ad4fc09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847100"
---
# <a name="cim_volatilestorage-class"></a><span data-ttu-id="4622d-103">CIM \_ VolatileStorage 類別</span><span class="sxs-lookup"><span data-stu-id="4622d-103">CIM\_VolatileStorage class</span></span>

<span data-ttu-id="4622d-104">**CIM \_ VolatileStorage** 類別代表 volatile 儲存體的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="4622d-104">The **CIM\_VolatileStorage** class represents the capabilities and management of volatile storage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4622d-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="4622d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4622d-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="4622d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4622d-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4622d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4622d-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4622d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4622d-109">語法</span><span class="sxs-lookup"><span data-stu-id="4622d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36851DFE-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_VolatileStorage : CIM_Memory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  boolean  Cacheable;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="4622d-110">成員</span><span class="sxs-lookup"><span data-stu-id="4622d-110">Members</span></span>

<span data-ttu-id="4622d-111">**CIM \_ VolatileStorage** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4622d-111">The **CIM\_VolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="4622d-112">方法</span><span class="sxs-lookup"><span data-stu-id="4622d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4622d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="4622d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4622d-114">方法</span><span class="sxs-lookup"><span data-stu-id="4622d-114">Methods</span></span>

<span data-ttu-id="4622d-115">**CIM \_ VolatileStorage** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4622d-115">The **CIM\_VolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="4622d-116">方法</span><span class="sxs-lookup"><span data-stu-id="4622d-116">Method</span></span>                                                                     | <span data-ttu-id="4622d-117">描述</span><span class="sxs-lookup"><span data-stu-id="4622d-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4622d-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="4622d-118">**Reset**</span></span>](reset-method-in-class-cim-volatilestorage.md)                 | <span data-ttu-id="4622d-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="4622d-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="4622d-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="4622d-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="4622d-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4622d-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volatilestorage.md) | <span data-ttu-id="4622d-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="4622d-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="4622d-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="4622d-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4622d-124">屬性</span><span class="sxs-lookup"><span data-stu-id="4622d-124">Properties</span></span>

<span data-ttu-id="4622d-125">**CIM \_ VolatileStorage** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4622d-125">The **CIM\_VolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4622d-126">**存取**</span><span class="sxs-lookup"><span data-stu-id="4622d-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4622d-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-129">媒體的讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="4622d-129">Read/write properties of the media.</span></span>

<span data-ttu-id="4622d-130">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4622d-131">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4622d-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="4622d-132">**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="4622d-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="4622d-133">可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="4622d-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="4622d-134">支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="4622d-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="4622d-135">**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="4622d-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="4622d-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-137">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="4622d-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4622d-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.18 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.13 ") ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="4622d-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4622d-140">其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="4622d-140">Additional error information.</span></span> <span data-ttu-id="4622d-141">例如，錯誤檢查和修正 (ECC) 的症狀，或使用以 CRC 為基礎的錯誤方法時，會傳回檢查位。</span><span class="sxs-lookup"><span data-stu-id="4622d-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="4622d-142">在後者的情況下，如果可辨識單一位錯誤且已知 CRC 演算法，則可以判斷失敗的確切位。</span><span class="sxs-lookup"><span data-stu-id="4622d-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="4622d-143">這種類型的資料 (ECC 的症狀、檢查位或同位資料，或其他廠商提供的資訊) 包含在此欄位中。</span><span class="sxs-lookup"><span data-stu-id="4622d-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="4622d-144">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="4622d-145">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-145">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-146">**可用性**</span><span class="sxs-lookup"><span data-stu-id="4622d-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-147">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4622d-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-149">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="4622d-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-150">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="4622d-150">Availability and status of the device.</span></span>

<span data-ttu-id="4622d-151">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4622d-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4622d-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4622d-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4622d-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="4622d-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="4622d-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-155">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="4622d-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4622d-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="4622d-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="4622d-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="4622d-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4622d-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="4622d-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4622d-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="4622d-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="4622d-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="4622d-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="4622d-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="4622d-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4622d-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="4622d-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="4622d-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="4622d-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="4622d-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="4622d-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4622d-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="4622d-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-166">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="4622d-166">The device is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4622d-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="4622d-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-168">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="4622d-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4622d-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="4622d-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-170">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="4622d-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4622d-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="4622d-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4622d-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="4622d-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-173">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="4622d-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4622d-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="4622d-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-175">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="4622d-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="4622d-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="4622d-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-177">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="4622d-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4622d-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="4622d-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-179">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="4622d-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="4622d-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="4622d-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-181">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="4622d-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="4622d-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-183">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4622d-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-185">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="4622d-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-186">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4622d-186">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="4622d-187">如果變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4622d-187">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="4622d-188">如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="4622d-188">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="4622d-189">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="4622d-190">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4622d-190">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-191">**可快取**</span><span class="sxs-lookup"><span data-stu-id="4622d-191">**Cacheable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-192">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4622d-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-194">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源記憶體資訊 \| 001.5」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-195">若 **為 TRUE**，則可以快取此記憶體。</span><span class="sxs-lookup"><span data-stu-id="4622d-195">If **TRUE**, this memory can be cached.</span></span>

</dd> <dt>

<span data-ttu-id="4622d-196">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="4622d-196">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-197">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4622d-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-199">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 系統資源記憶體資訊 \| 001.6」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-200">與記憶體相容的快取類型。</span><span class="sxs-lookup"><span data-stu-id="4622d-200">Cache type that is compatible with the memory.</span></span> <span data-ttu-id="4622d-201">如果可快取的屬性設定為 **FALSE** **，則此** 屬性沒有意義，而且應該設定為 4 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="4622d-201">If the **Cacheable** property is set to **FALSE**, then this property does not have meaning and should be set to 4 ("Not Applicable").</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4622d-202">**其他** (0) </span><span class="sxs-lookup"><span data-stu-id="4622d-202">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4622d-203">**未知** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="4622d-203">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Back"></span><span id="write-back"></span><span id="WRITE-BACK"></span>

<span data-ttu-id="4622d-204">**回寫** (2) </span><span class="sxs-lookup"><span data-stu-id="4622d-204">**Write-Back** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Through"></span><span id="write-through"></span><span id="WRITE-THROUGH"></span>

<span data-ttu-id="4622d-205">**寫入** (3) </span><span class="sxs-lookup"><span data-stu-id="4622d-205">**Write-Through** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4622d-206">**不適用** (4) </span><span class="sxs-lookup"><span data-stu-id="4622d-206">**Not Applicable** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-207">**標題**</span><span class="sxs-lookup"><span data-stu-id="4622d-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-210">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="4622d-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-211">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="4622d-211">Short textual description of the object.</span></span>

<span data-ttu-id="4622d-212">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4622d-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-214">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4622d-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-216">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="4622d-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-217">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4622d-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="4622d-218">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="4622d-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="4622d-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="4622d-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="4622d-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-221">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="4622d-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="4622d-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="4622d-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="4622d-223">(1)</span><span class="sxs-lookup"><span data-stu-id="4622d-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-224">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="4622d-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4622d-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4622d-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="4622d-226">(2)</span><span class="sxs-lookup"><span data-stu-id="4622d-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="4622d-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="4622d-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="4622d-228">(3)</span><span class="sxs-lookup"><span data-stu-id="4622d-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-229">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="4622d-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4622d-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="4622d-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="4622d-231">(4)</span><span class="sxs-lookup"><span data-stu-id="4622d-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-232">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4622d-232">Device is not working properly.</span></span> <span data-ttu-id="4622d-233">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="4622d-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="4622d-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="4622d-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="4622d-235">(5)</span><span class="sxs-lookup"><span data-stu-id="4622d-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-236">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="4622d-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="4622d-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="4622d-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="4622d-238">(6)</span><span class="sxs-lookup"><span data-stu-id="4622d-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-239">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="4622d-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="4622d-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="4622d-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="4622d-241">(7)</span><span class="sxs-lookup"><span data-stu-id="4622d-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="4622d-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="4622d-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="4622d-243">(8)</span><span class="sxs-lookup"><span data-stu-id="4622d-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-244">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="4622d-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="4622d-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="4622d-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="4622d-246">(9)</span><span class="sxs-lookup"><span data-stu-id="4622d-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-247">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4622d-247">Device is not working properly.</span></span> <span data-ttu-id="4622d-248">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="4622d-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="4622d-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="4622d-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="4622d-250">(10)</span><span class="sxs-lookup"><span data-stu-id="4622d-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-251">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="4622d-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="4622d-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="4622d-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="4622d-253">(11)</span><span class="sxs-lookup"><span data-stu-id="4622d-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-254">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="4622d-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="4622d-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="4622d-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="4622d-256"> (12) </span><span class="sxs-lookup"><span data-stu-id="4622d-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-257">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="4622d-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="4622d-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="4622d-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="4622d-259">(13)</span><span class="sxs-lookup"><span data-stu-id="4622d-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-260">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="4622d-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="4622d-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="4622d-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="4622d-262">(14)</span><span class="sxs-lookup"><span data-stu-id="4622d-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-263">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4622d-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="4622d-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="4622d-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="4622d-265">(15)</span><span class="sxs-lookup"><span data-stu-id="4622d-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-266">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4622d-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="4622d-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="4622d-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="4622d-268">(16)</span><span class="sxs-lookup"><span data-stu-id="4622d-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-269">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="4622d-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="4622d-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="4622d-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="4622d-271">(17)</span><span class="sxs-lookup"><span data-stu-id="4622d-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-272">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="4622d-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4622d-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4622d-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="4622d-274">(18)</span><span class="sxs-lookup"><span data-stu-id="4622d-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-275">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4622d-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="4622d-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="4622d-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="4622d-277">(19)</span><span class="sxs-lookup"><span data-stu-id="4622d-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4622d-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="4622d-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="4622d-279">(20)</span><span class="sxs-lookup"><span data-stu-id="4622d-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-280">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="4622d-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="4622d-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="4622d-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="4622d-282">(21)</span><span class="sxs-lookup"><span data-stu-id="4622d-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-283">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="4622d-283">System failure.</span></span> <span data-ttu-id="4622d-284">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="4622d-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="4622d-285">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="4622d-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="4622d-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="4622d-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="4622d-287">(22)</span><span class="sxs-lookup"><span data-stu-id="4622d-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-288">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="4622d-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="4622d-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="4622d-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="4622d-290">(23)</span><span class="sxs-lookup"><span data-stu-id="4622d-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-291">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="4622d-291">System failure.</span></span> <span data-ttu-id="4622d-292">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="4622d-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="4622d-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4622d-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="4622d-294">(24)</span><span class="sxs-lookup"><span data-stu-id="4622d-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-295">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4622d-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4622d-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="4622d-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4622d-297">(25)</span><span class="sxs-lookup"><span data-stu-id="4622d-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-298">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="4622d-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4622d-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="4622d-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4622d-300">(26)</span><span class="sxs-lookup"><span data-stu-id="4622d-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-301">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="4622d-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="4622d-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="4622d-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="4622d-303">(27)</span><span class="sxs-lookup"><span data-stu-id="4622d-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-304">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="4622d-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="4622d-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4622d-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="4622d-306">(28)</span><span class="sxs-lookup"><span data-stu-id="4622d-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-307">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4622d-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="4622d-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="4622d-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="4622d-309">(29)</span><span class="sxs-lookup"><span data-stu-id="4622d-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-310">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="4622d-310">Device is disabled.</span></span> <span data-ttu-id="4622d-311">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="4622d-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="4622d-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="4622d-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="4622d-313">(30)</span><span class="sxs-lookup"><span data-stu-id="4622d-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-314">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="4622d-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4622d-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4622d-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="4622d-316"> (31) </span><span class="sxs-lookup"><span data-stu-id="4622d-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-317">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4622d-317">Device is not working properly.</span></span> <span data-ttu-id="4622d-318">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4622d-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="4622d-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-320">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4622d-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-321">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-322">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="4622d-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-323">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="4622d-323">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="4622d-324">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-325">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="4622d-325">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-326">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4622d-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-327">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-328">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") </span><span class="sxs-lookup"><span data-stu-id="4622d-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-329">若 **為 TRUE**，表示最新的錯誤是可修正的。</span><span class="sxs-lookup"><span data-stu-id="4622d-329">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="4622d-330">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-330">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="4622d-331">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-331">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4622d-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-334">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-335">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4622d-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4622d-336">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="4622d-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4622d-337">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="4622d-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4622d-338">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-339">**說明**</span><span class="sxs-lookup"><span data-stu-id="4622d-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-340">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-342">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="4622d-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-343">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="4622d-343">Textual description of the object.</span></span>

<span data-ttu-id="4622d-344">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4622d-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-348">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4622d-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4622d-349">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="4622d-349">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="4622d-350">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-351">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="4622d-351">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-352">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4622d-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-354">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體陣列對應位址 \| 001.4 "，" MIF。「DMTF \| 記憶體裝置對應位址 \| 001.5」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-355">記憶體物件的結束位址（由應用程式或作業系統所參考並由記憶體控制器所對應）。</span><span class="sxs-lookup"><span data-stu-id="4622d-355">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="4622d-356">結束位址是以 kb 來指定。</span><span class="sxs-lookup"><span data-stu-id="4622d-356">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="4622d-357">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-357">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="4622d-358">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4622d-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-359">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="4622d-359">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-360">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4622d-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-362">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.15 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.10 ") </span><span class="sxs-lookup"><span data-stu-id="4622d-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-363">造成最後一個錯誤的記憶體存取作業。</span><span class="sxs-lookup"><span data-stu-id="4622d-363">Memory access operation that caused the last error.</span></span> <span data-ttu-id="4622d-364">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="4622d-364">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="4622d-365">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-365">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="4622d-366">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-366">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4622d-367">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4622d-367">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4622d-368">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4622d-368">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="4622d-369">**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="4622d-369">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="4622d-370">**撰寫** (4) </span><span class="sxs-lookup"><span data-stu-id="4622d-370">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="4622d-371">**部分寫入** (5) </span><span class="sxs-lookup"><span data-stu-id="4622d-371">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-372">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="4622d-372">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-373">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4622d-373">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-375">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.19 "，" MIF。DMTF \| 記憶體裝置 \| 002.20 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.14 ") </span><span class="sxs-lookup"><span data-stu-id="4622d-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-376">最後一個記憶體錯誤的位址。</span><span class="sxs-lookup"><span data-stu-id="4622d-376">Address of the last memory error.</span></span> <span data-ttu-id="4622d-377">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="4622d-377">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="4622d-378">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-378">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="4622d-379">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-379">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="4622d-380">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4622d-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-381">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4622d-381">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-382">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4622d-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-384">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="4622d-384">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="4622d-385">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-386">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="4622d-386">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-387">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="4622d-387">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4622d-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-389">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體裝置 \| 002.17 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.12 ") ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="4622d-389">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4622d-390">最後一個錯誤記憶體存取期間所捕獲的資料。</span><span class="sxs-lookup"><span data-stu-id="4622d-390">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="4622d-391">資料會佔用陣列的前 *n* 個八位數位，以保存 **ErrorTransferSize** 屬性所指定的位數。</span><span class="sxs-lookup"><span data-stu-id="4622d-391">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="4622d-392">如果 **ErrorTransferSize** 為0，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-392">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="4622d-393">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-394">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="4622d-394">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-395">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4622d-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-397">排序儲存在 **ErrorData** 陣列中的資料。</span><span class="sxs-lookup"><span data-stu-id="4622d-397">Ordering for data stored in the **ErrorData** array.</span></span> <span data-ttu-id="4622d-398">如果 **ErrorTransferSize** 為0，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-398">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="4622d-399">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4622d-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4622d-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-401">不明。</span><span class="sxs-lookup"><span data-stu-id="4622d-401">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="4622d-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**最不重要的位元組先** (1) </span><span class="sxs-lookup"><span data-stu-id="4622d-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-403">最不重要的位元組優先。</span><span class="sxs-lookup"><span data-stu-id="4622d-403">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="4622d-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**最重要的位元組先** (2) </span><span class="sxs-lookup"><span data-stu-id="4622d-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-405">最重要的位元組優先。</span><span class="sxs-lookup"><span data-stu-id="4622d-405">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-406">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4622d-406">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-407">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-409">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="4622d-409">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="4622d-410">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-411">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4622d-411">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-412">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4622d-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-414">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**") </span><span class="sxs-lookup"><span data-stu-id="4622d-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-415">最近發生的錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="4622d-415">Type of error that occurred most recently.</span></span> <span data-ttu-id="4622d-416">因為錯誤類型的語義以及是否可更正它是否可在 DMI 中混合，所以 CIM 架構中的值12-14 是未定義的。</span><span class="sxs-lookup"><span data-stu-id="4622d-416">The values 12-14 are undefined in the CIM schema since the semantics of the type of error and whether or not it was correctable are mixed in DMI.</span></span> <span data-ttu-id="4622d-417">**CorrectableError** 屬性會指出是否可進行更正。</span><span class="sxs-lookup"><span data-stu-id="4622d-417">The **CorrectableError** property indicates whether it was correctable.</span></span>

<span data-ttu-id="4622d-418">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-418">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4622d-419">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4622d-419">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4622d-420">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4622d-420">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4622d-421">**確定** (3) </span><span class="sxs-lookup"><span data-stu-id="4622d-421">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="4622d-422">**讀取** (4) 錯誤</span><span class="sxs-lookup"><span data-stu-id="4622d-422">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="4622d-423">同位 **錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="4622d-423">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="4622d-424">**單一位錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="4622d-424">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="4622d-425">**雙位錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="4622d-425">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="4622d-426">**多位錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="4622d-426">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="4622d-427">**半位元組錯誤** (9) </span><span class="sxs-lookup"><span data-stu-id="4622d-427">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="4622d-428">總和 **檢查碼錯誤** (10) </span><span class="sxs-lookup"><span data-stu-id="4622d-428">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="4622d-429">**CRC 錯誤** (11) </span><span class="sxs-lookup"><span data-stu-id="4622d-429">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="4622d-430">**未定義** 的 (12) </span><span class="sxs-lookup"><span data-stu-id="4622d-430">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="4622d-431">**未定義** (13) </span><span class="sxs-lookup"><span data-stu-id="4622d-431">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="4622d-432">**未定義** (14) </span><span class="sxs-lookup"><span data-stu-id="4622d-432">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-433">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="4622d-433">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-435">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-436">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.7 ") </span><span class="sxs-lookup"><span data-stu-id="4622d-436">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-437">描述儲存範圍所支援之錯誤偵測和更正類型的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="4622d-437">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="4622d-438">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-438">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-439">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="4622d-439">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-440">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4622d-440">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-441">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-442">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.21 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="4622d-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-443">最後一個錯誤可以解析的範圍（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4622d-443">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="4622d-444">例如，如果錯誤位址解析為位 11 (也就是在一般頁面上) ，則可以將錯誤解析為 4 KB 界限，而這個屬性會設定為4000。</span><span class="sxs-lookup"><span data-stu-id="4622d-444">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="4622d-445">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-445">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="4622d-446">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-446">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="4622d-447">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4622d-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-448">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="4622d-448">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-449">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4622d-449">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-451">上次發生記憶體錯誤的時間。</span><span class="sxs-lookup"><span data-stu-id="4622d-451">Time that the last memory error occurred.</span></span> <span data-ttu-id="4622d-452">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="4622d-452">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="4622d-453">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-453">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="4622d-454">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-454">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-455">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="4622d-455">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-456">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4622d-456">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-457">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-458">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.16 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="4622d-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-459">造成最後一個錯誤的資料傳輸大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="4622d-459">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="4622d-460">0表示沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="4622d-460">0 indicates no error.</span></span> <span data-ttu-id="4622d-461">如果 **ErrorInfo** 屬性等於3，"OK"，則此屬性應該設定為0。</span><span class="sxs-lookup"><span data-stu-id="4622d-461">If the **ErrorInfo** property is equal to 3, "OK", then this property should be set to 0.</span></span>

<span data-ttu-id="4622d-462">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-462">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-463">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4622d-463">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-464">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4622d-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-466">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="4622d-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-467">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4622d-467">Date and time the object was installed.</span></span> <span data-ttu-id="4622d-468">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="4622d-468">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4622d-469">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-469">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-470">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4622d-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-471">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4622d-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-473">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4622d-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="4622d-474">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-475">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4622d-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-476">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-478">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="4622d-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-479">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="4622d-479">Label by which the object is known.</span></span> <span data-ttu-id="4622d-480">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4622d-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4622d-481">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="4622d-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-483">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4622d-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-484">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-485">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="4622d-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-486">連續區塊總數，每個區塊會封鎖 **區塊** 屬性中包含的值大小，這會形成此儲存範圍。</span><span class="sxs-lookup"><span data-stu-id="4622d-486">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="4622d-487">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="4622d-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="4622d-488">如果 **區塊** 的值是 1 (一個) ，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="4622d-488">If the value of **BlockSize** is 1 (one), then this property is the total size of the storage extent.</span></span>

<span data-ttu-id="4622d-489">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="4622d-490">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4622d-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-491">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4622d-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-492">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-493">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-494">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 記憶體**](cim-memory.md)」。**ErrorInfo**」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-495">提供其他資訊的自由格式字串（如果 **ErrorType** 屬性設定為 1 ( "Other" ) ）。</span><span class="sxs-lookup"><span data-stu-id="4622d-495">Free-form string that provides additional information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="4622d-496">如果1以外的值 (一個) ，則這個字串沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-496">If a value other than 1 (one), this string has no meaning.</span></span>

<span data-ttu-id="4622d-497">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4622d-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-499">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-500">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-501">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="4622d-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-502">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="4622d-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="4622d-503">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4622d-504">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="4622d-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="4622d-505">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4622d-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-506">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4622d-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4622d-507">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-508">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="4622d-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="4622d-509">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="4622d-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4622d-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4622d-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4622d-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="4622d-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4622d-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="4622d-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4622d-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="4622d-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-514">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="4622d-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4622d-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="4622d-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-516">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="4622d-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4622d-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="4622d-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-518">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4622d-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="4622d-519">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="4622d-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="4622d-520">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="4622d-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4622d-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="4622d-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-522">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="4622d-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4622d-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="4622d-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4622d-524">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="4622d-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-525">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4622d-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-526">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4622d-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-527">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-528">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="4622d-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="4622d-529">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="4622d-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="4622d-530">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="4622d-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="4622d-531">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="4622d-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="4622d-532">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-533">**目的**</span><span class="sxs-lookup"><span data-stu-id="4622d-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-534">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-535">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-536">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="4622d-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="4622d-537">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-538">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="4622d-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-539">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4622d-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-540">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-541">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體陣列對應位址 \| 001.3 "，" MIF。「DMTF \| 記憶體裝置對應位址 \| 001.4」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-542">記憶體物件的起始位址（由應用程式或作業系統所參考並由記憶體控制器所對應）。</span><span class="sxs-lookup"><span data-stu-id="4622d-542">Beginning address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="4622d-543">起始位址的指定單位為 kb。</span><span class="sxs-lookup"><span data-stu-id="4622d-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="4622d-544">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="4622d-545">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4622d-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-546">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4622d-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-547">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-548">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-549">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="4622d-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-550">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4622d-550">Current status of the object.</span></span> <span data-ttu-id="4622d-551">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4622d-552">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="4622d-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4622d-553">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4622d-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4622d-554">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4622d-555">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4622d-556">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4622d-557">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4622d-558">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4622d-559">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4622d-560">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4622d-561">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4622d-562">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="4622d-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4622d-563">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4622d-564">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="4622d-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4622d-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-566">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4622d-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-567">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-568">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="4622d-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4622d-569">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="4622d-569">State of the logical device.</span></span> <span data-ttu-id="4622d-570">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="4622d-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="4622d-571">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4622d-572">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4622d-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4622d-573">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4622d-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4622d-574">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="4622d-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4622d-575">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="4622d-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4622d-576">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="4622d-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4622d-577">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4622d-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-578">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-579">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-580">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4622d-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4622d-581">設定系統建立類別名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="4622d-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="4622d-582">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-583">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="4622d-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-584">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4622d-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-585">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4622d-586">若 **為 TRUE**， **ErrorAddress** 屬性中的位址資訊為系統層級的位址;如果為 **FALSE**，則為實體位址。</span><span class="sxs-lookup"><span data-stu-id="4622d-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address; if **FALSE**, it is a physical address.</span></span> <span data-ttu-id="4622d-587">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="4622d-587">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="4622d-588">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-588">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4622d-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4622d-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4622d-590">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4622d-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4622d-591">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4622d-591">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4622d-592">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4622d-592">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4622d-593">設定系統名稱的範圍。</span><span class="sxs-lookup"><span data-stu-id="4622d-593">Scoping system's name.</span></span>

<span data-ttu-id="4622d-594">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4622d-595">備註</span><span class="sxs-lookup"><span data-stu-id="4622d-595">Remarks</span></span>

<span data-ttu-id="4622d-596">**Cim \_ VolatileStorage** 類別衍生自 [**cim \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="4622d-596">The **CIM\_VolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="4622d-597">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="4622d-597">WMI does not implement this class.</span></span>

<span data-ttu-id="4622d-598">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="4622d-598">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4622d-599">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4622d-599">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4622d-600">規格需求</span><span class="sxs-lookup"><span data-stu-id="4622d-600">Requirements</span></span>



| <span data-ttu-id="4622d-601">需求</span><span class="sxs-lookup"><span data-stu-id="4622d-601">Requirement</span></span> | <span data-ttu-id="4622d-602">值</span><span class="sxs-lookup"><span data-stu-id="4622d-602">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4622d-603">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4622d-603">Minimum supported client</span></span><br/> | <span data-ttu-id="4622d-604">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4622d-604">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4622d-605">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4622d-605">Minimum supported server</span></span><br/> | <span data-ttu-id="4622d-606">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4622d-606">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4622d-607">命名空間</span><span class="sxs-lookup"><span data-stu-id="4622d-607">Namespace</span></span><br/>                | <span data-ttu-id="4622d-608">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4622d-608">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4622d-609">MOF</span><span class="sxs-lookup"><span data-stu-id="4622d-609">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4622d-610"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4622d-610"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4622d-611">DLL</span><span class="sxs-lookup"><span data-stu-id="4622d-611">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4622d-612"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4622d-612"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4622d-613">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4622d-613">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4622d-614">**CIM \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="4622d-614">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

