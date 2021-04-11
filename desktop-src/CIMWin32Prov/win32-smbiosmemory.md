---
description: Win32 \_ SMBIOSMemory ABSTRACT WMI 類別代表電腦系統記憶體的內容，如透過系統管理 BIOS (SMBIOS) 介面所見。
ms.assetid: 2f609fc6-f0f5-45a5-9f9a-3873da034d49
ms.tgt_platform: multiple
title: Win32_SMBIOSMemory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SMBIOSMemory
- Win32_SMBIOSMemory.Reset
- Win32_SMBIOSMemory.SetPowerState
- Win32_SMBIOSMemory.Access
- Win32_SMBIOSMemory.AdditionalErrorData
- Win32_SMBIOSMemory.Availability
- Win32_SMBIOSMemory.BlockSize
- Win32_SMBIOSMemory.Caption
- Win32_SMBIOSMemory.ConfigManagerErrorCode
- Win32_SMBIOSMemory.ConfigManagerUserConfig
- Win32_SMBIOSMemory.CorrectableError
- Win32_SMBIOSMemory.CreationClassName
- Win32_SMBIOSMemory.Description
- Win32_SMBIOSMemory.DeviceID
- Win32_SMBIOSMemory.EndingAddress
- Win32_SMBIOSMemory.ErrorAccess
- Win32_SMBIOSMemory.ErrorAddress
- Win32_SMBIOSMemory.ErrorCleared
- Win32_SMBIOSMemory.ErrorData
- Win32_SMBIOSMemory.ErrorDataOrder
- Win32_SMBIOSMemory.ErrorDescription
- Win32_SMBIOSMemory.ErrorInfo
- Win32_SMBIOSMemory.ErrorMethodology
- Win32_SMBIOSMemory.ErrorResolution
- Win32_SMBIOSMemory.ErrorTime
- Win32_SMBIOSMemory.ErrorTransferSize
- Win32_SMBIOSMemory.InstallDate
- Win32_SMBIOSMemory.LastErrorCode
- Win32_SMBIOSMemory.Name
- Win32_SMBIOSMemory.NumberOfBlocks
- Win32_SMBIOSMemory.OtherErrorDescription
- Win32_SMBIOSMemory.PNPDeviceID
- Win32_SMBIOSMemory.PowerManagementCapabilities
- Win32_SMBIOSMemory.PowerManagementSupported
- Win32_SMBIOSMemory.Purpose
- Win32_SMBIOSMemory.StartingAddress
- Win32_SMBIOSMemory.Status
- Win32_SMBIOSMemory.StatusInfo
- Win32_SMBIOSMemory.SystemCreationClassName
- Win32_SMBIOSMemory.SystemLevelAddress
- Win32_SMBIOSMemory.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4dc7a42732dfb00d965f79045254878f690309fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111337"
---
# <a name="win32_smbiosmemory-class"></a><span data-ttu-id="8c17b-103">Win32 \_ SMBIOSMemory 類別</span><span class="sxs-lookup"><span data-stu-id="8c17b-103">Win32\_SMBIOSMemory class</span></span>

<span data-ttu-id="8c17b-104">**Win32 \_ SMBIOSMemory** abstract [WMI 類別](../wmisdk/retrieving-a-class.md)代表電腦系統記憶體的內容，如透過系統管理 BIOS (SMBIOS) 介面所見。</span><span class="sxs-lookup"><span data-stu-id="8c17b-104">The **Win32\_SMBIOSMemory** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a computer system memory as seen through the system management BIOS (SMBIOS) interface.</span></span> <span data-ttu-id="8c17b-105">SMBIOS 介面不會區分非動態、動態和 flash 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8c17b-105">The SMBIOS interface does not distinguish between nonvolatile, volatile, and flash memories.</span></span> <span data-ttu-id="8c17b-106">[**CIM \_ 記憶體**](cim-memory.md)類別是所有類型記憶體的父類別。</span><span class="sxs-lookup"><span data-stu-id="8c17b-106">The [**CIM\_Memory**](cim-memory.md) class is the parent class of all types of memory.</span></span>

<span data-ttu-id="8c17b-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8c17b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8c17b-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8c17b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c17b-109">語法</span><span class="sxs-lookup"><span data-stu-id="8c17b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FECB095B-F0FA-11d2-8617-0000F8102E5F}"), AMENDMENT]
class Win32_SMBIOSMemory : CIM_StorageExtent
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
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
  uint16e  StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="8c17b-110">成員</span><span class="sxs-lookup"><span data-stu-id="8c17b-110">Members</span></span>

<span data-ttu-id="8c17b-111">**Win32 \_ SMBIOSMemory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8c17b-111">The **Win32\_SMBIOSMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="8c17b-112">方法</span><span class="sxs-lookup"><span data-stu-id="8c17b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8c17b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8c17b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8c17b-114">方法</span><span class="sxs-lookup"><span data-stu-id="8c17b-114">Methods</span></span>

<span data-ttu-id="8c17b-115">**Win32 \_ SMBIOSMemory** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8c17b-115">The **Win32\_SMBIOSMemory** class has these methods.</span></span>



| <span data-ttu-id="8c17b-116">方法</span><span class="sxs-lookup"><span data-stu-id="8c17b-116">Method</span></span>            | <span data-ttu-id="8c17b-117">描述</span><span class="sxs-lookup"><span data-stu-id="8c17b-117">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c17b-118">**重設**</span><span class="sxs-lookup"><span data-stu-id="8c17b-118">**Reset**</span></span>         | <span data-ttu-id="8c17b-119">未實作。</span><span class="sxs-lookup"><span data-stu-id="8c17b-119">Not implemented.</span></span> <span data-ttu-id="8c17b-120">若要執行此方法，請參閱 [**CIM \_ StorageExtent**](cim-storageextent.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="8c17b-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/>                 |
| <span data-ttu-id="8c17b-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8c17b-121">**SetPowerState**</span></span> | <span data-ttu-id="8c17b-122">未實作。</span><span class="sxs-lookup"><span data-stu-id="8c17b-122">Not implemented.</span></span> <span data-ttu-id="8c17b-123">若要執行此方法，請參閱 [**CIM \_ StorageExtent**](cim-storageextent.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="8c17b-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8c17b-124">屬性</span><span class="sxs-lookup"><span data-stu-id="8c17b-124">Properties</span></span>

<span data-ttu-id="8c17b-125">**Win32 \_ SMBIOSMemory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8c17b-125">The **Win32\_SMBIOSMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c17b-126">**存取**</span><span class="sxs-lookup"><span data-stu-id="8c17b-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-127">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8c17b-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-129">存取的類型。</span><span class="sxs-lookup"><span data-stu-id="8c17b-129">Type of access.</span></span>

<span data-ttu-id="8c17b-130">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c17b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8c17b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="8c17b-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="8c17b-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="8c17b-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="8c17b-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-134">可寫入</span><span class="sxs-lookup"><span data-stu-id="8c17b-134">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="8c17b-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="8c17b-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="8c17b-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="8c17b-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-137">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="8c17b-137">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-138">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="8c17b-138">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-140">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 18 \| 32-Bit Memory Error Information Information \| 供應商症狀" ) ， [**最大**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="8c17b-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-141">包含其他錯誤資訊的八位陣列。</span><span class="sxs-lookup"><span data-stu-id="8c17b-141">Array of octets that hold additional error information.</span></span> <span data-ttu-id="8c17b-142">例如，錯誤檢查和修正 (ECC) 的症狀，或使用以 CRC 為基礎的錯誤方法時，會傳回檢查位。</span><span class="sxs-lookup"><span data-stu-id="8c17b-142">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="8c17b-143">在後者的情況下，如果可辨識單一位錯誤，且迴圈的重複檢查 (CRC) 演算法，則可以判斷失敗的確切位。</span><span class="sxs-lookup"><span data-stu-id="8c17b-143">In the latter case, if a single bit error is recognized and the cyclical redundancy check (CRC) algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="8c17b-144">這種類型的資料 (ECC 的症狀、檢查位或同位位資料，或其他廠商提供的資訊) 包含在此欄位中。</span><span class="sxs-lookup"><span data-stu-id="8c17b-144">This type of data (ECC Syndrome, Check Bit or Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="8c17b-145">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-145">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-146">**可用性**</span><span class="sxs-lookup"><span data-stu-id="8c17b-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-147">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8c17b-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-149">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="8c17b-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-150">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="8c17b-150">Availability and status of the device.</span></span>

<span data-ttu-id="8c17b-151">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c17b-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8c17b-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c17b-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8c17b-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8c17b-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="8c17b-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-155">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="8c17b-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8c17b-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="8c17b-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8c17b-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="8c17b-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8c17b-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="8c17b-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8c17b-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="8c17b-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8c17b-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="8c17b-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8c17b-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="8c17b-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8c17b-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="8c17b-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8c17b-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="8c17b-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8c17b-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="8c17b-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8c17b-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="8c17b-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-166">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="8c17b-166">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8c17b-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="8c17b-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-168">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="8c17b-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8c17b-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="8c17b-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-170">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="8c17b-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8c17b-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="8c17b-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8c17b-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="8c17b-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-173">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="8c17b-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8c17b-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="8c17b-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-175">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="8c17b-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8c17b-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="8c17b-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-177">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="8c17b-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8c17b-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="8c17b-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-179">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="8c17b-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8c17b-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="8c17b-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-181">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="8c17b-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="8c17b-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-183">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8c17b-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-185">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](../wmisdk/standard-qualifiers.md) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="8c17b-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-186">形成此儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c17b-186">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="8c17b-187">如果未知或區塊概念無效 (例如，針對匯總範圍、記憶體或邏輯磁片) ，請輸入1。</span><span class="sxs-lookup"><span data-stu-id="8c17b-187">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="8c17b-188">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="8c17b-189">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-190">**標題**</span><span class="sxs-lookup"><span data-stu-id="8c17b-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-193">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-194">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="8c17b-194">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="8c17b-195">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-196">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8c17b-196">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-197">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c17b-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-198">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-199">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-199">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-200">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8c17b-200">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="8c17b-201">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-201">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8c17b-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="8c17b-203"> (0)</span><span class="sxs-lookup"><span data-stu-id="8c17b-203">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-204">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="8c17b-204">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8c17b-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="8c17b-206">(1)</span><span class="sxs-lookup"><span data-stu-id="8c17b-206">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-207">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="8c17b-207">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8c17b-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8c17b-209">(2)</span><span class="sxs-lookup"><span data-stu-id="8c17b-209">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8c17b-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8c17b-211">(3)</span><span class="sxs-lookup"><span data-stu-id="8c17b-211">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-212">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="8c17b-212">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8c17b-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8c17b-214">(4)</span><span class="sxs-lookup"><span data-stu-id="8c17b-214">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-215">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="8c17b-215">Device is not working properly.</span></span> <span data-ttu-id="8c17b-216">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="8c17b-216">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8c17b-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8c17b-218">(5)</span><span class="sxs-lookup"><span data-stu-id="8c17b-218">(5)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-219">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="8c17b-219">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8c17b-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8c17b-221">(6)</span><span class="sxs-lookup"><span data-stu-id="8c17b-221">(6)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-222">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="8c17b-222">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8c17b-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="8c17b-224">(7)</span><span class="sxs-lookup"><span data-stu-id="8c17b-224">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8c17b-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8c17b-226">(8)</span><span class="sxs-lookup"><span data-stu-id="8c17b-226">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-227">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="8c17b-227">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8c17b-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8c17b-229">(9)</span><span class="sxs-lookup"><span data-stu-id="8c17b-229">(9)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-230">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="8c17b-230">Device is not working properly.</span></span> <span data-ttu-id="8c17b-231">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="8c17b-231">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8c17b-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="8c17b-233">(10)</span><span class="sxs-lookup"><span data-stu-id="8c17b-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-234">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="8c17b-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8c17b-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="8c17b-236">(11)</span><span class="sxs-lookup"><span data-stu-id="8c17b-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-237">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="8c17b-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8c17b-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8c17b-239"> (12) </span><span class="sxs-lookup"><span data-stu-id="8c17b-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-240">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="8c17b-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8c17b-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8c17b-242">(13)</span><span class="sxs-lookup"><span data-stu-id="8c17b-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-243">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="8c17b-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8c17b-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8c17b-245">(14)</span><span class="sxs-lookup"><span data-stu-id="8c17b-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-246">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="8c17b-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8c17b-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8c17b-248">(15)</span><span class="sxs-lookup"><span data-stu-id="8c17b-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-249">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="8c17b-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8c17b-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8c17b-251">(16)</span><span class="sxs-lookup"><span data-stu-id="8c17b-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-252">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="8c17b-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8c17b-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8c17b-254">(17)</span><span class="sxs-lookup"><span data-stu-id="8c17b-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-255">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="8c17b-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8c17b-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8c17b-257">(18)</span><span class="sxs-lookup"><span data-stu-id="8c17b-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-258">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8c17b-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8c17b-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="8c17b-260">(19)</span><span class="sxs-lookup"><span data-stu-id="8c17b-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8c17b-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="8c17b-262">(20)</span><span class="sxs-lookup"><span data-stu-id="8c17b-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-263">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="8c17b-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8c17b-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8c17b-265">(21)</span><span class="sxs-lookup"><span data-stu-id="8c17b-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-266">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="8c17b-266">System failure.</span></span> <span data-ttu-id="8c17b-267">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="8c17b-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="8c17b-268">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="8c17b-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8c17b-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="8c17b-270">(22)</span><span class="sxs-lookup"><span data-stu-id="8c17b-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-271">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="8c17b-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8c17b-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8c17b-273">(23)</span><span class="sxs-lookup"><span data-stu-id="8c17b-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-274">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="8c17b-274">System failure.</span></span> <span data-ttu-id="8c17b-275">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="8c17b-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8c17b-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8c17b-277">(24)</span><span class="sxs-lookup"><span data-stu-id="8c17b-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-278">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="8c17b-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8c17b-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8c17b-280">(25)</span><span class="sxs-lookup"><span data-stu-id="8c17b-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-281">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="8c17b-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8c17b-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8c17b-283">(26)</span><span class="sxs-lookup"><span data-stu-id="8c17b-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-284">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="8c17b-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8c17b-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8c17b-286">(27)</span><span class="sxs-lookup"><span data-stu-id="8c17b-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-287">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="8c17b-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8c17b-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8c17b-289">(28)</span><span class="sxs-lookup"><span data-stu-id="8c17b-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-290">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8c17b-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8c17b-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8c17b-292">(29)</span><span class="sxs-lookup"><span data-stu-id="8c17b-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-293">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="8c17b-293">Device is disabled.</span></span> <span data-ttu-id="8c17b-294">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="8c17b-294">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8c17b-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8c17b-296">(30)</span><span class="sxs-lookup"><span data-stu-id="8c17b-296">(30)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-297">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="8c17b-297">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8c17b-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="8c17b-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8c17b-299"> (31) </span><span class="sxs-lookup"><span data-stu-id="8c17b-299">(31)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-300">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="8c17b-300">Device is not working properly.</span></span> <span data-ttu-id="8c17b-301">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="8c17b-301">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-302">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="8c17b-302">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-303">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8c17b-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-305">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-306">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="8c17b-306">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8c17b-307">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-308">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="8c17b-308">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-309">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8c17b-309">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-311">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Type" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-312">若 **為 TRUE**，表示最新的錯誤是可修正的。</span><span class="sxs-lookup"><span data-stu-id="8c17b-312">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="8c17b-313">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-313">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8c17b-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-315">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-317">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8c17b-317">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-318">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="8c17b-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="8c17b-319">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="8c17b-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="8c17b-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-321">**說明**</span><span class="sxs-lookup"><span data-stu-id="8c17b-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-324">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-324">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-325">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="8c17b-325">Description of the object.</span></span>

<span data-ttu-id="8c17b-326">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8c17b-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-330">限定詞： [ **CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8c17b-330">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-331">邏輯裝置的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c17b-331">Unique identifier of the logical device.</span></span>

<span data-ttu-id="8c17b-332">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-333">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="8c17b-333">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-334">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8c17b-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-336">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「SMBIOS \| 類型 19 \| 記憶體裝置對應位址 \| 結束位址」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-336">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-337">結束位址，由應用程式或作業系統參考，且由記憶體控制器針對這個記憶體物件所對應。</span><span class="sxs-lookup"><span data-stu-id="8c17b-337">Ending address, referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="8c17b-338">結束位址是以 kb 來指定。</span><span class="sxs-lookup"><span data-stu-id="8c17b-338">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="8c17b-339">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-339">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-340">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="8c17b-340">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-341">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8c17b-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-342">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-343">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Operation" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-344">造成最後一個錯誤的記憶體存取作業。</span><span class="sxs-lookup"><span data-stu-id="8c17b-344">Memory access operation that caused the last error.</span></span> <span data-ttu-id="8c17b-345">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="8c17b-345">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="8c17b-346">如果 **ErrorInfo** 等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-346">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c17b-347">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8c17b-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c17b-348">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8c17b-348">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="8c17b-349">**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="8c17b-349">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="8c17b-350">**撰寫** (4) </span><span class="sxs-lookup"><span data-stu-id="8c17b-350">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="8c17b-351">**部分寫入** (5) </span><span class="sxs-lookup"><span data-stu-id="8c17b-351">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-352">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="8c17b-352">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-353">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8c17b-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-354">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-355">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Address" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-356">最後一個記憶體錯誤的位址。</span><span class="sxs-lookup"><span data-stu-id="8c17b-356">Address of the last memory error.</span></span> <span data-ttu-id="8c17b-357">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="8c17b-357">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="8c17b-358">如果 **ErrorInfo** 等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-358">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="8c17b-359">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-359">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-360">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8c17b-360">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-361">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8c17b-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-363">若 **為 TRUE**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="8c17b-363">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="8c17b-364">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-365">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="8c17b-365">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-366">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="8c17b-366">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-368">限定詞： [**ArrayType**](../wmisdk/standard-qualifiers.md) ( 「已編制索引」 ) 、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( 「SMBIOS」 ) 、 [**最大**](../wmisdk/standard-qualifiers.md) (64) </span><span class="sxs-lookup"><span data-stu-id="8c17b-368">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-369">最後一個錯誤記憶體存取期間所捕獲的資料陣列。</span><span class="sxs-lookup"><span data-stu-id="8c17b-369">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="8c17b-370">資料會佔用陣列的前 *n* 個八位數位，以保存 **ErrorTransferSize** 屬性所指定的位數。</span><span class="sxs-lookup"><span data-stu-id="8c17b-370">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="8c17b-371">如果 **ErrorTransferSize** 為 0 (零) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-371">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-372">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="8c17b-372">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-373">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8c17b-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-374">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-375">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-376">排序儲存在 **ErrorData** 屬性中的資料。</span><span class="sxs-lookup"><span data-stu-id="8c17b-376">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="8c17b-377">如果 **ErrorTransferSize** 為 0 (零) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-377">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c17b-378">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8c17b-378">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="8c17b-379">**最不重要的位元組先** (1) </span><span class="sxs-lookup"><span data-stu-id="8c17b-379">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="8c17b-380">**最重要的位元組先** (2) </span><span class="sxs-lookup"><span data-stu-id="8c17b-380">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8c17b-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-384">**LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c17b-384">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="8c17b-385">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="8c17b-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-387">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="8c17b-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-389">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 記憶體**](cim-memory.md)」。**OtherErrorDescription**") ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS \| Type 18 \| 32-Bit Memory error Information \| error Type ") </span><span class="sxs-lookup"><span data-stu-id="8c17b-389">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-390">最近發生的錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="8c17b-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="8c17b-391">未使用值12到14。</span><span class="sxs-lookup"><span data-stu-id="8c17b-391">The values 12 through 14 are unused.</span></span> <span data-ttu-id="8c17b-392">更正的功能會在屬性 **CorrectableError** 中指出。</span><span class="sxs-lookup"><span data-stu-id="8c17b-392">The ability to be corrected is indicated in the property **CorrectableError**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c17b-393">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8c17b-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c17b-394">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8c17b-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8c17b-395">**確定** (3) </span><span class="sxs-lookup"><span data-stu-id="8c17b-395">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="8c17b-396">**讀取** (4) 錯誤</span><span class="sxs-lookup"><span data-stu-id="8c17b-396">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="8c17b-397">同位 **錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="8c17b-397">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="8c17b-398">**單一位錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="8c17b-398">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="8c17b-399">**雙位錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="8c17b-399">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="8c17b-400">**多位錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="8c17b-400">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="8c17b-401">**半位元組錯誤** (9) </span><span class="sxs-lookup"><span data-stu-id="8c17b-401">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="8c17b-402">總和 **檢查碼錯誤** (10) </span><span class="sxs-lookup"><span data-stu-id="8c17b-402">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="8c17b-403">**CRC 錯誤** (11) </span><span class="sxs-lookup"><span data-stu-id="8c17b-403">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="8c17b-404">**修正了單一位錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="8c17b-404">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="8c17b-405">**更正錯誤** (13) </span><span class="sxs-lookup"><span data-stu-id="8c17b-405">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="8c17b-406">無法 **更正的錯誤** (14) </span><span class="sxs-lookup"><span data-stu-id="8c17b-406">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-407">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="8c17b-407">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-408">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-409">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-410">限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "ErrorMethodology" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 16 \| 實體記憶體陣列 \| 記憶體錯誤更正" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-410">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-411">有關同位或 CRC 演算法、ECC 或其他使用的機制的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8c17b-411">Details on the parity or CRC algorithms, ECC or other mechanisms used.</span></span>

<span data-ttu-id="8c17b-412">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-412">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c17b-413">**其他** ( "其他" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-413">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c17b-414">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-414">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="8c17b-415">**無** ( 「無」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-415">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="8c17b-416">同 **位 ( 「** 同位」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-416">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="8c17b-417">**單一位 ecc** ( 「單一位 ecc」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-417">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="8c17b-418">**多位 ecc** ( 「多重位 ecc」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-418">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="8c17b-419">**Crc** ( 「crc」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-419">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-420">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="8c17b-420">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-421">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8c17b-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-423">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| Error 解決" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-424">最後一個錯誤可以解析的範圍（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8c17b-424">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="8c17b-425">例如，如果錯誤位址解析為位 11 (也就是在一般頁面上) ，則可以將錯誤解析為 4 KB 界限，而這個屬性會設定為4000。</span><span class="sxs-lookup"><span data-stu-id="8c17b-425">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="8c17b-426">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-426">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="8c17b-427">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-427">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-428">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="8c17b-428">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-429">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8c17b-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-431">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-431">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-432">上次發生記憶體錯誤的時間。</span><span class="sxs-lookup"><span data-stu-id="8c17b-432">Time that the last memory error occurred.</span></span> <span data-ttu-id="8c17b-433">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="8c17b-433">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="8c17b-434">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-434">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-435">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="8c17b-435">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-436">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c17b-436">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-437">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-438">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS" ) ， [**單位**](../wmisdk/standard-qualifiers.md) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-438">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-439">造成最後一個錯誤的資料傳輸大小（0 (零) 表示沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="8c17b-439">Size of the data transfer in bits that caused the last error—0 (zero) indicates no error.</span></span> <span data-ttu-id="8c17b-440">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性應該設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="8c17b-440">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-441">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8c17b-441">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-442">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="8c17b-442">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-444">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="8c17b-444">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-445">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8c17b-445">Date and time the object was installed.</span></span> <span data-ttu-id="8c17b-446">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="8c17b-446">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8c17b-447">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-448">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8c17b-448">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-449">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="8c17b-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-450">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-451">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8c17b-451">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8c17b-452">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-453">**名稱**</span><span class="sxs-lookup"><span data-stu-id="8c17b-453">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-454">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-456">限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-456">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-457">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="8c17b-457">Label by which the object is known.</span></span> <span data-ttu-id="8c17b-458">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="8c17b-458">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="8c17b-459">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-459">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-460">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="8c17b-460">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-461">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8c17b-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-462">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-463">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="8c17b-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-464">連續區塊總數，每個區塊會封鎖 **區塊** 屬性中包含的值大小，這會形成此儲存範圍。</span><span class="sxs-lookup"><span data-stu-id="8c17b-464">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="8c17b-465">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="8c17b-465">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="8c17b-466">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="8c17b-466">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="8c17b-467">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-467">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="8c17b-468">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-468">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-469">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8c17b-469">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-470">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-470">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-471">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-472">限定詞： [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 記憶體**](cim-memory.md)」。**ErrorInfo**") ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" SMBIOS ") </span><span class="sxs-lookup"><span data-stu-id="8c17b-472">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-473">如果 **ErrorType** 屬性設定為1，則提供詳細資訊的自由格式字串;否則，此字串沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-473">Free-form string that provides more information if the **ErrorType** property is set to 1; otherwise, this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-474">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8c17b-474">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-475">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-476">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-477">限定詞： [**架構**](../wmisdk/standard-qualifiers.md) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-477">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-478">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c17b-478">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="8c17b-479">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="8c17b-479">Example: "\*PNP030b"</span></span>

<span data-ttu-id="8c17b-480">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-481">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8c17b-481">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-482">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="8c17b-482">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-483">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-484">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="8c17b-484">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8c17b-485">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c17b-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="8c17b-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8c17b-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="8c17b-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8c17b-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="8c17b-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8c17b-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="8c17b-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-490">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="8c17b-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8c17b-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="8c17b-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-492">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="8c17b-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8c17b-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="8c17b-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-494">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="8c17b-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8c17b-495">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="8c17b-495">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="8c17b-496">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](../wmisdk/designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-496">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8c17b-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="8c17b-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-498">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="8c17b-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8c17b-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="8c17b-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8c17b-500">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="8c17b-500">Timed Power-On Supported</span></span>

<span data-ttu-id="8c17b-501">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="8c17b-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8c17b-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-503">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8c17b-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-504">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-505">若 **為 TRUE**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="8c17b-505">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="8c17b-506">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="8c17b-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="8c17b-507">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-508">**目的**</span><span class="sxs-lookup"><span data-stu-id="8c17b-508">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-509">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-509">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-510">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-511">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="8c17b-511">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="8c17b-512">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-512">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-513">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="8c17b-513">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-514">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="8c17b-514">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-515">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-516">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「SMBIOS \| 類型 19 \| 記憶體裝置對應位址 \| 起始位址」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-516">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-517">由應用程式或作業系統參考的起始位址，並由記憶體控制器針對這個記憶體物件所對應。</span><span class="sxs-lookup"><span data-stu-id="8c17b-517">Beginning address that is referenced by an application or operating system, and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="8c17b-518">起始位址的指定單位為 kb。</span><span class="sxs-lookup"><span data-stu-id="8c17b-518">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="8c17b-519">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-519">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-520">**狀態**</span><span class="sxs-lookup"><span data-stu-id="8c17b-520">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-521">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-522">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-523">限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-523">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-524">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="8c17b-524">Current status of the object.</span></span> <span data-ttu-id="8c17b-525">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="8c17b-525">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8c17b-526">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="8c17b-526">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8c17b-527">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="8c17b-527">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8c17b-528">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="8c17b-528">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8c17b-529">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="8c17b-529">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8c17b-530">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-530">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8c17b-531">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="8c17b-531">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8c17b-532">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-532">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8c17b-533">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-533">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8c17b-534">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-534">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c17b-535">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-535">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8c17b-536">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-536">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8c17b-537">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-537">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8c17b-538">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-538">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8c17b-539">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-539">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8c17b-540">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-540">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8c17b-541">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-541">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8c17b-542">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-542">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8c17b-543">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-543">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-544">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8c17b-544">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-545">資料類型： **uint16e**</span><span class="sxs-lookup"><span data-stu-id="8c17b-545">Data type: **uint16e**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-546">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-547">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="8c17b-547">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-548">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="8c17b-548">State of the logical device.</span></span> <span data-ttu-id="8c17b-549">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="8c17b-549">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="8c17b-550">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c17b-551">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="8c17b-551">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c17b-552">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8c17b-552">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8c17b-553">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="8c17b-553">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8c17b-554">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="8c17b-554">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8c17b-555">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="8c17b-555">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8c17b-556">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8c17b-556">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-557">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-558">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-559">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8c17b-559">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-560">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="8c17b-560">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="8c17b-561">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-561">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-562">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="8c17b-562">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-563">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="8c17b-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-564">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-565">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Address" ) </span><span class="sxs-lookup"><span data-stu-id="8c17b-565">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-566">若 **為 TRUE**， **ErrorAddress** 屬性中的位址資訊就是系統層級的位址。</span><span class="sxs-lookup"><span data-stu-id="8c17b-566">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="8c17b-567">如果為 **FALSE**，則為實體位址。</span><span class="sxs-lookup"><span data-stu-id="8c17b-567">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="8c17b-568">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="8c17b-568">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="8c17b-569">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8c17b-569">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c17b-570">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8c17b-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-571">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8c17b-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c17b-572">限定詞： [**傳播**](../wmisdk/standard-qualifiers.md) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8c17b-572">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8c17b-573">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c17b-573">Name of the scoping system.</span></span>

<span data-ttu-id="8c17b-574">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-574">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c17b-575">備註</span><span class="sxs-lookup"><span data-stu-id="8c17b-575">Remarks</span></span>

<span data-ttu-id="8c17b-576">**Win32 \_ SMBIOSMemory** 類別衍生自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="8c17b-576">The **Win32\_SMBIOSMemory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c17b-577">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c17b-577">Requirements</span></span>



| <span data-ttu-id="8c17b-578">需求</span><span class="sxs-lookup"><span data-stu-id="8c17b-578">Requirement</span></span> | <span data-ttu-id="8c17b-579">值</span><span class="sxs-lookup"><span data-stu-id="8c17b-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c17b-580">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c17b-580">Minimum supported client</span></span><br/> | <span data-ttu-id="8c17b-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c17b-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c17b-582">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c17b-582">Minimum supported server</span></span><br/> | <span data-ttu-id="8c17b-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c17b-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c17b-584">命名空間</span><span class="sxs-lookup"><span data-stu-id="8c17b-584">Namespace</span></span><br/>                | <span data-ttu-id="8c17b-585">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8c17b-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c17b-586">MOF</span><span class="sxs-lookup"><span data-stu-id="8c17b-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c17b-587"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c17b-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c17b-588">DLL</span><span class="sxs-lookup"><span data-stu-id="8c17b-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c17b-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c17b-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c17b-590">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c17b-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c17b-591">**CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="8c17b-591">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="8c17b-592">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="8c17b-592">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
