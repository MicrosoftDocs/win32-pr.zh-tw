---
description: CIM \_ 記憶體類別代表記憶體相關邏輯裝置的功能和管理。
ms.assetid: ddc72aad-5687-4bc1-b402-e27b27eca9be
ms.tgt_platform: multiple
title: 'CIM_Memory 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Caption
- CIM_Memory.Description
- CIM_Memory.InstallDate
- CIM_Memory.Name
- CIM_Memory.Status
- CIM_Memory.Availability
- CIM_Memory.ConfigManagerErrorCode
- CIM_Memory.ConfigManagerUserConfig
- CIM_Memory.CreationClassName
- CIM_Memory.DeviceID
- CIM_Memory.PowerManagementCapabilities
- CIM_Memory.ErrorCleared
- CIM_Memory.ErrorDescription
- CIM_Memory.LastErrorCode
- CIM_Memory.PNPDeviceID
- CIM_Memory.PowerManagementSupported
- CIM_Memory.StatusInfo
- CIM_Memory.SystemCreationClassName
- CIM_Memory.SystemName
- CIM_Memory.Access
- CIM_Memory.BlockSize
- CIM_Memory.NumberOfBlocks
- CIM_Memory.Purpose
- CIM_Memory.ErrorMethodology
- CIM_Memory.AdditionalErrorData
- CIM_Memory.CorrectableError
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorAddress
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorInfo
- CIM_Memory.ErrorResolution
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorTransferSize
- CIM_Memory.OtherErrorDescription
- CIM_Memory.StartingAddress
- CIM_Memory.SystemLevelAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35fbb8467337da1ceab044a42533a6ca8628cf63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111061"
---
# <a name="cim_memory-class-cimwin32-wmi-providers"></a><span data-ttu-id="88ffb-103">CIM_Memory 類別 (CIMWin32 WMI 提供者) </span><span class="sxs-lookup"><span data-stu-id="88ffb-103">CIM_Memory class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="88ffb-104">**CIM \_ 記憶體** 類別代表記憶體相關邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="88ffb-104">The **CIM\_Memory** class represents the capabilities and management of memory-related logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88ffb-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="88ffb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="88ffb-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="88ffb-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="88ffb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="88ffb-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="88ffb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ffb-109">語法</span><span class="sxs-lookup"><span data-stu-id="88ffb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B64-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
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
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
};
```

## <a name="members"></a><span data-ttu-id="88ffb-110">成員</span><span class="sxs-lookup"><span data-stu-id="88ffb-110">Members</span></span>

<span data-ttu-id="88ffb-111">**CIM \_ 記憶體** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="88ffb-111">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="88ffb-112">方法</span><span class="sxs-lookup"><span data-stu-id="88ffb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="88ffb-113">屬性</span><span class="sxs-lookup"><span data-stu-id="88ffb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="88ffb-114">方法</span><span class="sxs-lookup"><span data-stu-id="88ffb-114">Methods</span></span>

<span data-ttu-id="88ffb-115">**CIM \_ 記憶體** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="88ffb-115">The **CIM\_Memory** class has these methods.</span></span>



| <span data-ttu-id="88ffb-116">方法</span><span class="sxs-lookup"><span data-stu-id="88ffb-116">Method</span></span>                                                            | <span data-ttu-id="88ffb-117">描述</span><span class="sxs-lookup"><span data-stu-id="88ffb-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88ffb-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="88ffb-118">**Reset**</span></span>](reset-method-in-class-cim-memory.md)                 | <span data-ttu-id="88ffb-119">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="88ffb-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="88ffb-120">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="88ffb-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="88ffb-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="88ffb-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-memory.md) | <span data-ttu-id="88ffb-122">定義邏輯裝置的預期電源狀態，以及何時應將裝置置於該狀態。</span><span class="sxs-lookup"><span data-stu-id="88ffb-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="88ffb-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="88ffb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="88ffb-124">屬性</span><span class="sxs-lookup"><span data-stu-id="88ffb-124">Properties</span></span>

<span data-ttu-id="88ffb-125">**CIM \_ 記憶體** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="88ffb-125">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88ffb-126">**存取**</span><span class="sxs-lookup"><span data-stu-id="88ffb-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="88ffb-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-129">描述媒體的讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="88ffb-129">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="88ffb-130">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ffb-131">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="88ffb-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="88ffb-132">**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="88ffb-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="88ffb-133">可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="88ffb-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="88ffb-134">支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="88ffb-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="88ffb-135">**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="88ffb-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ffb-136">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="88ffb-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-137">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="88ffb-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.18 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.13 ") ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="88ffb-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-140">包含其他錯誤資訊的八位陣列。</span><span class="sxs-lookup"><span data-stu-id="88ffb-140">Array of octets that hold additional error information.</span></span> <span data-ttu-id="88ffb-141">例如，錯誤檢查和修正 (ECC) 的症狀，或使用以 CRC 為基礎的錯誤方法時，會傳回檢查位。</span><span class="sxs-lookup"><span data-stu-id="88ffb-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="88ffb-142">在後者的情況下，如果可辨識單一位錯誤且已知 CRC 演算法，則可以判斷失敗的確切位。</span><span class="sxs-lookup"><span data-stu-id="88ffb-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="88ffb-143">這種類型的資料 (ECC 的症狀、檢查位或同位資料，或其他廠商提供的資訊) 包含在此欄位中。</span><span class="sxs-lookup"><span data-stu-id="88ffb-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="88ffb-144">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-145">**可用性**</span><span class="sxs-lookup"><span data-stu-id="88ffb-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-146">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="88ffb-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-149">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="88ffb-149">Availability and status of the device.</span></span>

<span data-ttu-id="88ffb-150">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88ffb-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="88ffb-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ffb-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="88ffb-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="88ffb-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="88ffb-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="88ffb-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="88ffb-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="88ffb-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="88ffb-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="88ffb-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="88ffb-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="88ffb-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="88ffb-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="88ffb-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="88ffb-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="88ffb-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="88ffb-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="88ffb-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="88ffb-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="88ffb-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="88ffb-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="88ffb-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="88ffb-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="88ffb-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="88ffb-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-164">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="88ffb-164">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="88ffb-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="88ffb-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-166">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="88ffb-166">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="88ffb-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="88ffb-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-168">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="88ffb-168">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="88ffb-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="88ffb-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="88ffb-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="88ffb-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-171">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="88ffb-171">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="88ffb-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="88ffb-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-173">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="88ffb-173">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="88ffb-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="88ffb-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-175">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="88ffb-175">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="88ffb-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="88ffb-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-177">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="88ffb-177">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="88ffb-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="88ffb-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-179">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="88ffb-179">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="88ffb-180">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="88ffb-180">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-181">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="88ffb-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-183">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-184">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88ffb-184">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="88ffb-185">如果變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88ffb-185">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="88ffb-186">如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="88ffb-186">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="88ffb-187">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="88ffb-188">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-188">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-189">**標題**</span><span class="sxs-lookup"><span data-stu-id="88ffb-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-192">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-193">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="88ffb-193">A short textual description of the object.</span></span>

<span data-ttu-id="88ffb-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="88ffb-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-196">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88ffb-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-198">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-199">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="88ffb-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="88ffb-200">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="88ffb-201">**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-201">**This device is working properly.**</span></span> <span data-ttu-id="88ffb-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="88ffb-202">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="88ffb-203">**這個裝置並未正確設定。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-203">**This device is not configured correctly.**</span></span> <span data-ttu-id="88ffb-204">(1)</span><span class="sxs-lookup"><span data-stu-id="88ffb-204">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="88ffb-205">**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-205">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="88ffb-206">(2)</span><span class="sxs-lookup"><span data-stu-id="88ffb-206">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="88ffb-207">**這個裝置的驅動程式可能已損毀，或您系統的記憶體或其他資源可能不足。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-207">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="88ffb-208">(3)</span><span class="sxs-lookup"><span data-stu-id="88ffb-208">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="88ffb-209">**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-209">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="88ffb-210">(4)</span><span class="sxs-lookup"><span data-stu-id="88ffb-210">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="88ffb-211">**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-211">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="88ffb-212">(5)</span><span class="sxs-lookup"><span data-stu-id="88ffb-212">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="88ffb-213">**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-213">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="88ffb-214">(6)</span><span class="sxs-lookup"><span data-stu-id="88ffb-214">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="88ffb-215">**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-215">**Cannot filter.**</span></span> <span data-ttu-id="88ffb-216">(7)</span><span class="sxs-lookup"><span data-stu-id="88ffb-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="88ffb-217">**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-217">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="88ffb-218">(8)</span><span class="sxs-lookup"><span data-stu-id="88ffb-218">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="88ffb-219">**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-219">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="88ffb-220">(9)</span><span class="sxs-lookup"><span data-stu-id="88ffb-220">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="88ffb-221">**這個裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-221">**This device cannot start.**</span></span> <span data-ttu-id="88ffb-222">(10)</span><span class="sxs-lookup"><span data-stu-id="88ffb-222">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="88ffb-223">**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-223">**This device failed.**</span></span> <span data-ttu-id="88ffb-224">(11)</span><span class="sxs-lookup"><span data-stu-id="88ffb-224">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="88ffb-225">**這個裝置沒有足夠資源可供使用。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-225">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="88ffb-226"> (12) </span><span class="sxs-lookup"><span data-stu-id="88ffb-226">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="88ffb-227">**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-227">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="88ffb-228">(13)</span><span class="sxs-lookup"><span data-stu-id="88ffb-228">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="88ffb-229">**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-229">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="88ffb-230">(14)</span><span class="sxs-lookup"><span data-stu-id="88ffb-230">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="88ffb-231">**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-231">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="88ffb-232">(15)</span><span class="sxs-lookup"><span data-stu-id="88ffb-232">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="88ffb-233">**Windows 無法識別這個裝置所使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-233">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="88ffb-234">(16)</span><span class="sxs-lookup"><span data-stu-id="88ffb-234">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="88ffb-235">**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-235">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="88ffb-236">(17)</span><span class="sxs-lookup"><span data-stu-id="88ffb-236">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="88ffb-237">**重新安裝這個裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-237">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="88ffb-238">(18)</span><span class="sxs-lookup"><span data-stu-id="88ffb-238">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="88ffb-239">**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-239">**Failure using the VxD loader.**</span></span> <span data-ttu-id="88ffb-240">(19)</span><span class="sxs-lookup"><span data-stu-id="88ffb-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="88ffb-241">**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-241">**Your registry might be corrupted.**</span></span> <span data-ttu-id="88ffb-242">(20)</span><span class="sxs-lookup"><span data-stu-id="88ffb-242">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="88ffb-243">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-243">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="88ffb-244">(21)</span><span class="sxs-lookup"><span data-stu-id="88ffb-244">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="88ffb-245">**這個裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-245">**This device is disabled.**</span></span> <span data-ttu-id="88ffb-246">(22)</span><span class="sxs-lookup"><span data-stu-id="88ffb-246">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="88ffb-247">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-247">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="88ffb-248">(23)</span><span class="sxs-lookup"><span data-stu-id="88ffb-248">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="88ffb-249">**這個裝置可能不存在、運作不正確、或並未安裝所有的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-249">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="88ffb-250">(24)</span><span class="sxs-lookup"><span data-stu-id="88ffb-250">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="88ffb-251">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-251">**Windows is still setting up this device.**</span></span> <span data-ttu-id="88ffb-252">(25)</span><span class="sxs-lookup"><span data-stu-id="88ffb-252">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="88ffb-253">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-253">**Windows is still setting up this device.**</span></span> <span data-ttu-id="88ffb-254">(26)</span><span class="sxs-lookup"><span data-stu-id="88ffb-254">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="88ffb-255">**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-255">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="88ffb-256">(27)</span><span class="sxs-lookup"><span data-stu-id="88ffb-256">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="88ffb-257">**這個裝置的驅動程式尚未安裝。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-257">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="88ffb-258">(28)</span><span class="sxs-lookup"><span data-stu-id="88ffb-258">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="88ffb-259">**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-259">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="88ffb-260">(29)</span><span class="sxs-lookup"><span data-stu-id="88ffb-260">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="88ffb-261">**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-261">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="88ffb-262">(30)</span><span class="sxs-lookup"><span data-stu-id="88ffb-262">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="88ffb-263">**這個裝置並未正確執行，因為 Windows 無法載入這個裝置必需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="88ffb-263">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="88ffb-264"> (31) </span><span class="sxs-lookup"><span data-stu-id="88ffb-264">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ffb-265">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="88ffb-265">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-266">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="88ffb-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-268">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-268">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-269">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="88ffb-269">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="88ffb-270">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-271">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="88ffb-271">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-272">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="88ffb-272">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-274">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-274">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-275">若 **為 TRUE**，表示最新的錯誤是可修正的。</span><span class="sxs-lookup"><span data-stu-id="88ffb-275">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="88ffb-276">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-276">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-277">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88ffb-277">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-279">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-280">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="88ffb-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-281">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="88ffb-281">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="88ffb-282">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="88ffb-282">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="88ffb-283">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-284">**說明**</span><span class="sxs-lookup"><span data-stu-id="88ffb-284">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-285">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-286">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-287">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-288">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="88ffb-288">A textual description of the object.</span></span>

<span data-ttu-id="88ffb-289">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-289">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-290">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="88ffb-290">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-291">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-293">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="88ffb-293">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-294">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="88ffb-294">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="88ffb-295">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-296">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="88ffb-296">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-297">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="88ffb-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-299">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體陣列對應位址 \| 001.4 "，" MIF。「DMTF \| 記憶體裝置對應位址 \| 001.5」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-300">由應用程式或作業系統參考，且由記憶體控制器針對這個記憶體物件所對應的結束位址。</span><span class="sxs-lookup"><span data-stu-id="88ffb-300">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="88ffb-301">結束位址是以 kb 來指定。</span><span class="sxs-lookup"><span data-stu-id="88ffb-301">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="88ffb-302">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-302">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-303">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="88ffb-303">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-304">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="88ffb-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-305">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-306">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.15 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.10 ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-306">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-307">造成最後一個錯誤的記憶體存取作業。</span><span class="sxs-lookup"><span data-stu-id="88ffb-307">Memory access operation that caused the last error.</span></span> <span data-ttu-id="88ffb-308">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="88ffb-308">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="88ffb-309">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-309">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88ffb-310">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="88ffb-310">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ffb-311">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="88ffb-311">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="88ffb-312">**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="88ffb-312">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="88ffb-313">**撰寫** (4) </span><span class="sxs-lookup"><span data-stu-id="88ffb-313">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="88ffb-314">**部分寫入** (5) </span><span class="sxs-lookup"><span data-stu-id="88ffb-314">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ffb-315">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="88ffb-315">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-316">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="88ffb-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-317">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-318">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.19 "，" MIF。DMTF \| 記憶體裝置 \| 002.20 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.14 ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-319">最後一個記憶體錯誤的位址。</span><span class="sxs-lookup"><span data-stu-id="88ffb-319">Address of the last memory error.</span></span> <span data-ttu-id="88ffb-320">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="88ffb-320">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="88ffb-321">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-321">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="88ffb-322">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-322">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="88ffb-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-324">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="88ffb-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-326">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="88ffb-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="88ffb-327">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-328">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="88ffb-328">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-329">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="88ffb-329">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-331">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體裝置 \| 002.17 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.12 ") ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="88ffb-331">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-332">最後一個錯誤記憶體存取期間所捕獲的資料。</span><span class="sxs-lookup"><span data-stu-id="88ffb-332">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="88ffb-333">資料會佔用陣列的前 *n* 個八位，必須有這個陣列來保存 **ErrorTransferSize** 屬性所指定的位數。</span><span class="sxs-lookup"><span data-stu-id="88ffb-333">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="88ffb-334">如果 **ErrorTransferSize** 為0，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-334">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-335">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="88ffb-335">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-336">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="88ffb-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-338">儲存在 **ErrorData** 屬性中的資料順序。</span><span class="sxs-lookup"><span data-stu-id="88ffb-338">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="88ffb-339">如果 **ErrorTransferSize** 為0，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-339">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ffb-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="88ffb-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-341">不明。</span><span class="sxs-lookup"><span data-stu-id="88ffb-341">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="88ffb-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**最不重要的位元組先** (1) </span><span class="sxs-lookup"><span data-stu-id="88ffb-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-343">最不重要的位元組優先。</span><span class="sxs-lookup"><span data-stu-id="88ffb-343">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="88ffb-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**最重要的位元組先** (2) </span><span class="sxs-lookup"><span data-stu-id="88ffb-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-345">最重要的位元組優先。</span><span class="sxs-lookup"><span data-stu-id="88ffb-345">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="88ffb-346">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="88ffb-346">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-347">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-349">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="88ffb-349">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="88ffb-350">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-351">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="88ffb-351">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-352">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="88ffb-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-354">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**OtherErrorDescription**") </span><span class="sxs-lookup"><span data-stu-id="88ffb-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-355">最近發生的錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="88ffb-355">Type of error that occurred most recently.</span></span> <span data-ttu-id="88ffb-356">CIM 架構中的值12到14未定義，因為 DMI 混合了錯誤類型的語義以及是否可進行更正。</span><span class="sxs-lookup"><span data-stu-id="88ffb-356">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="88ffb-357">在 **CorrectableError** 屬性中指出錯誤是否可更正。</span><span class="sxs-lookup"><span data-stu-id="88ffb-357">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88ffb-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="88ffb-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-359">其他。</span><span class="sxs-lookup"><span data-stu-id="88ffb-359">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ffb-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="88ffb-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-361">不明。</span><span class="sxs-lookup"><span data-stu-id="88ffb-361">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88ffb-362"><span id="OK"></span><span id="ok"></span>**確定** (3) </span><span class="sxs-lookup"><span data-stu-id="88ffb-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-363">正常。</span><span class="sxs-lookup"><span data-stu-id="88ffb-363">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="88ffb-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**讀取** (4) 錯誤</span><span class="sxs-lookup"><span data-stu-id="88ffb-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-365">讀取錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-365">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="88ffb-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>同位 **錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="88ffb-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-367">同位錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-367">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="88ffb-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**單一位錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="88ffb-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-369">單一位錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-369">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="88ffb-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**雙位錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="88ffb-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-371">雙位錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-371">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="88ffb-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**多位錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="88ffb-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-373">多位錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-373">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="88ffb-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**半位元組錯誤** (9) </span><span class="sxs-lookup"><span data-stu-id="88ffb-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-375">半個錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-375">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="88ffb-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>總和 **檢查碼錯誤** (10) </span><span class="sxs-lookup"><span data-stu-id="88ffb-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-377">總和檢查碼錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-377">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="88ffb-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC 錯誤** (11) </span><span class="sxs-lookup"><span data-stu-id="88ffb-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-379">CRC 錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-379">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="88ffb-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**未定義** 的 (12) </span><span class="sxs-lookup"><span data-stu-id="88ffb-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-381">未定義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-381">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="88ffb-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**未定義** (13) </span><span class="sxs-lookup"><span data-stu-id="88ffb-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-383">未定義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-383">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="88ffb-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**未定義** (14) </span><span class="sxs-lookup"><span data-stu-id="88ffb-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-385">未定義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-385">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="88ffb-386">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="88ffb-386">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-387">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-389">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ErrorMethodology" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.7 ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-390">指出是否使用同位或 CRC 演算法、ECC 或其他機制。</span><span class="sxs-lookup"><span data-stu-id="88ffb-390">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="88ffb-391">也可以提供演算法的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="88ffb-391">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-392">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="88ffb-392">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-393">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="88ffb-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-394">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-395">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.21 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-396">指定可解決最後一個錯誤的範圍（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="88ffb-396">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="88ffb-397">例如，如果錯誤位址解析為位 11 (也就是在一般頁面上) ，則可以將錯誤解析為 4 KB 界限，而這個屬性會設定為4000。</span><span class="sxs-lookup"><span data-stu-id="88ffb-397">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="88ffb-398">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-398">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="88ffb-399">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-400">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="88ffb-400">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-401">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="88ffb-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-403">上次發生記憶體錯誤的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="88ffb-403">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="88ffb-404">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="88ffb-404">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="88ffb-405">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-405">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-406">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="88ffb-406">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-407">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88ffb-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-409">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.16 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-409">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-410">造成最後一個錯誤的資料傳輸大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="88ffb-410">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="88ffb-411">值為0表示沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-411">A value of 0 indicates no error.</span></span> <span data-ttu-id="88ffb-412">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性應該設定為0。</span><span class="sxs-lookup"><span data-stu-id="88ffb-412">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-413">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88ffb-413">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-414">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="88ffb-414">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-416">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-417">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="88ffb-417">Indicates when the object was installed.</span></span> <span data-ttu-id="88ffb-418">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="88ffb-418">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="88ffb-419">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-419">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-420">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="88ffb-420">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-421">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="88ffb-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-423">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="88ffb-423">Last error code reported by the logical device.</span></span>

<span data-ttu-id="88ffb-424">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-424">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-425">**名稱**</span><span class="sxs-lookup"><span data-stu-id="88ffb-425">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-426">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-427">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-428">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-428">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-429">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="88ffb-429">Label by which the object is known.</span></span> <span data-ttu-id="88ffb-430">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="88ffb-430">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="88ffb-431">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-431">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-432">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="88ffb-432">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-433">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="88ffb-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-435">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-436">連續區塊的數目，每個區塊會封鎖 **區塊** 屬性中包含的值大小，以形成儲存區。</span><span class="sxs-lookup"><span data-stu-id="88ffb-436">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="88ffb-437">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="88ffb-437">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="88ffb-438">如果 **區塊** 的值是 1 (一個) ，此屬性就是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="88ffb-438">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="88ffb-439">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-439">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="88ffb-440">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-440">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-441">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="88ffb-441">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-444">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 記憶體**」。**ErrorInfo**」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-444">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-445">如果 **ErrorType** 屬性設定為 1 ( "Other" ) ，則提供資訊的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="88ffb-445">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="88ffb-446">如果未設定為1，則此字串沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-446">If it is not set to 1, then this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-447">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="88ffb-447">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-448">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-449">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-450">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-450">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-451">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="88ffb-451">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="88ffb-452">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="88ffb-452">Example: "\*PNP030b"</span></span>

<span data-ttu-id="88ffb-453">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-454">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="88ffb-454">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-455">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="88ffb-455">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-456">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-457">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="88ffb-457">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="88ffb-458">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ffb-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="88ffb-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-460">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="88ffb-460">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="88ffb-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="88ffb-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-462">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="88ffb-462">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="88ffb-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="88ffb-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-464">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="88ffb-464">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="88ffb-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="88ffb-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-466">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="88ffb-466">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="88ffb-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="88ffb-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-468">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="88ffb-468">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="88ffb-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="88ffb-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-470">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="88ffb-470">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="88ffb-471">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="88ffb-471">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="88ffb-472">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-472">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="88ffb-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="88ffb-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-474">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="88ffb-474">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="88ffb-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="88ffb-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="88ffb-476">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="88ffb-476">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="88ffb-477">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="88ffb-477">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-478">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="88ffb-478">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-479">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-480">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="88ffb-480">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="88ffb-481">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="88ffb-481">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="88ffb-482">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="88ffb-482">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="88ffb-483">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="88ffb-483">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="88ffb-484">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-485">**目的**</span><span class="sxs-lookup"><span data-stu-id="88ffb-485">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-486">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-486">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-488">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="88ffb-488">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="88ffb-489">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-490">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="88ffb-490">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-491">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="88ffb-491">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-492">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-493">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體陣列對應位址 \| 001.3 "，" MIF。「DMTF \| 記憶體裝置對應位址 \| 001.4」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-493">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-494">這個記憶體物件的起始位址，由應用程式或作業系統參考，並且由記憶體控制器所參考。</span><span class="sxs-lookup"><span data-stu-id="88ffb-494">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="88ffb-495">起始位址的指定單位為 kb。</span><span class="sxs-lookup"><span data-stu-id="88ffb-495">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="88ffb-496">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-496">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-497">**狀態**</span><span class="sxs-lookup"><span data-stu-id="88ffb-497">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-498">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-499">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-500">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-500">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-501">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="88ffb-501">String that indicates the current status of the object.</span></span> <span data-ttu-id="88ffb-502">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="88ffb-502">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="88ffb-503">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="88ffb-503">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="88ffb-504">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="88ffb-504">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="88ffb-505">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="88ffb-505">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="88ffb-506">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="88ffb-506">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="88ffb-507">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="88ffb-507">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="88ffb-508">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-508">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="88ffb-509">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="88ffb-509">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88ffb-510">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-510">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="88ffb-511">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-511">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="88ffb-512">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-512">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ffb-513">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-513">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="88ffb-514">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-514">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="88ffb-515">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-515">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="88ffb-516">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-516">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="88ffb-517">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-517">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="88ffb-518">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-518">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="88ffb-519">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-519">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="88ffb-520">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-520">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="88ffb-521">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="88ffb-521">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ffb-522">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="88ffb-522">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-523">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="88ffb-523">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-525">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="88ffb-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-526">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="88ffb-526">State of the logical device.</span></span> <span data-ttu-id="88ffb-527">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="88ffb-527">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="88ffb-528">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="88ffb-529">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="88ffb-529">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88ffb-530">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="88ffb-530">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="88ffb-531">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="88ffb-531">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="88ffb-532">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="88ffb-532">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="88ffb-533">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="88ffb-533">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="88ffb-534">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88ffb-534">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-536">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-537">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="88ffb-537">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-538">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="88ffb-538">The scoping system's creation class name.</span></span>

<span data-ttu-id="88ffb-539">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-539">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-540">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="88ffb-540">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-541">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="88ffb-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-542">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-543">指出 **ErrorAddress** 屬性中的位址資訊是否為系統層級位址 (**TRUE**) 或 (**FALSE**) 的實體位址。</span><span class="sxs-lookup"><span data-stu-id="88ffb-543">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="88ffb-544">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="88ffb-544">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="88ffb-545">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="88ffb-545">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88ffb-546">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="88ffb-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-547">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="88ffb-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88ffb-548">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="88ffb-548">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="88ffb-549">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="88ffb-549">The scoping system's name.</span></span>

<span data-ttu-id="88ffb-550">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88ffb-551">備註</span><span class="sxs-lookup"><span data-stu-id="88ffb-551">Remarks</span></span>

<span data-ttu-id="88ffb-552">**Cim \_ 記憶體** 類別衍生自 [**cim \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-552">The **CIM\_Memory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="88ffb-553">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="88ffb-553">WMI does not implement this class.</span></span> <span data-ttu-id="88ffb-554">針對衍生自 **CIM \_ 記憶體** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="88ffb-554">For classes that are derived from **CIM\_Memory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="88ffb-555">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="88ffb-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="88ffb-556">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="88ffb-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ffb-557">規格需求</span><span class="sxs-lookup"><span data-stu-id="88ffb-557">Requirements</span></span>



| <span data-ttu-id="88ffb-558">需求</span><span class="sxs-lookup"><span data-stu-id="88ffb-558">Requirement</span></span> | <span data-ttu-id="88ffb-559">值</span><span class="sxs-lookup"><span data-stu-id="88ffb-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88ffb-560">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88ffb-560">Minimum supported client</span></span><br/> | <span data-ttu-id="88ffb-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88ffb-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88ffb-562">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88ffb-562">Minimum supported server</span></span><br/> | <span data-ttu-id="88ffb-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88ffb-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88ffb-564">命名空間</span><span class="sxs-lookup"><span data-stu-id="88ffb-564">Namespace</span></span><br/>                | <span data-ttu-id="88ffb-565">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="88ffb-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88ffb-566">MOF</span><span class="sxs-lookup"><span data-stu-id="88ffb-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88ffb-567"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="88ffb-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88ffb-568">DLL</span><span class="sxs-lookup"><span data-stu-id="88ffb-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88ffb-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88ffb-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ffb-570">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88ffb-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ffb-571">**CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="88ffb-571">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

