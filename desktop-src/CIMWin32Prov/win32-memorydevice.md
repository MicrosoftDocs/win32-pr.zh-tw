---
description: Win32 \_ MEMORYDEVICE WMI 類別代表電腦系統記憶體裝置及其相關聯對應位址的屬性。
ms.assetid: d609dca5-2f5f-4f23-8fcc-bcc197d6c24b
ms.tgt_platform: multiple
title: Win32_MemoryDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDevice
- Win32_MemoryDevice.Reset
- Win32_MemoryDevice.SetPowerState
- Win32_MemoryDevice.Access
- Win32_MemoryDevice.AdditionalErrorData
- Win32_MemoryDevice.Availability
- Win32_MemoryDevice.BlockSize
- Win32_MemoryDevice.Caption
- Win32_MemoryDevice.ConfigManagerErrorCode
- Win32_MemoryDevice.ConfigManagerUserConfig
- Win32_MemoryDevice.CorrectableError
- Win32_MemoryDevice.CreationClassName
- Win32_MemoryDevice.Description
- Win32_MemoryDevice.DeviceID
- Win32_MemoryDevice.EndingAddress
- Win32_MemoryDevice.ErrorAccess
- Win32_MemoryDevice.ErrorAddress
- Win32_MemoryDevice.ErrorCleared
- Win32_MemoryDevice.ErrorData
- Win32_MemoryDevice.ErrorDataOrder
- Win32_MemoryDevice.ErrorDescription
- Win32_MemoryDevice.ErrorGranularity
- Win32_MemoryDevice.ErrorInfo
- Win32_MemoryDevice.ErrorMethodology
- Win32_MemoryDevice.ErrorResolution
- Win32_MemoryDevice.ErrorTime
- Win32_MemoryDevice.ErrorTransferSize
- Win32_MemoryDevice.InstallDate
- Win32_MemoryDevice.LastErrorCode
- Win32_MemoryDevice.Name
- Win32_MemoryDevice.NumberOfBlocks
- Win32_MemoryDevice.OtherErrorDescription
- Win32_MemoryDevice.PNPDeviceID
- Win32_MemoryDevice.PowerManagementCapabilities
- Win32_MemoryDevice.PowerManagementSupported
- Win32_MemoryDevice.Purpose
- Win32_MemoryDevice.StartingAddress
- Win32_MemoryDevice.Status
- Win32_MemoryDevice.StatusInfo
- Win32_MemoryDevice.SystemCreationClassName
- Win32_MemoryDevice.SystemLevelAddress
- Win32_MemoryDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 277b868f1b92b9f7c6a0c520c77ab76fac6b544d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936140"
---
# <a name="win32_memorydevice-class"></a><span data-ttu-id="4aebc-103">Win32 \_ MemoryDevice 類別</span><span class="sxs-lookup"><span data-stu-id="4aebc-103">Win32\_MemoryDevice class</span></span>

<span data-ttu-id="4aebc-104">**Win32 \_ MemoryDevice** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表電腦系統記憶體裝置及其相關聯對應位址的屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-104">The **Win32\_MemoryDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a computer system memory device and its associated mapped addresses.</span></span>

<span data-ttu-id="4aebc-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4aebc-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="4aebc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aebc-107">語法</span><span class="sxs-lookup"><span data-stu-id="4aebc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDevice : Win32_SMBIOSMemory
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
  uint16   ErrorGranularity;
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

## <a name="members"></a><span data-ttu-id="4aebc-108">成員</span><span class="sxs-lookup"><span data-stu-id="4aebc-108">Members</span></span>

<span data-ttu-id="4aebc-109">**Win32 \_ MemoryDevice** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="4aebc-109">The **Win32\_MemoryDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="4aebc-110">方法</span><span class="sxs-lookup"><span data-stu-id="4aebc-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4aebc-111">屬性</span><span class="sxs-lookup"><span data-stu-id="4aebc-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4aebc-112">方法</span><span class="sxs-lookup"><span data-stu-id="4aebc-112">Methods</span></span>

<span data-ttu-id="4aebc-113">**Win32 \_ MemoryDevice** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="4aebc-113">The **Win32\_MemoryDevice** class has these methods.</span></span>



| <span data-ttu-id="4aebc-114">方法</span><span class="sxs-lookup"><span data-stu-id="4aebc-114">Method</span></span>            | <span data-ttu-id="4aebc-115">描述</span><span class="sxs-lookup"><span data-stu-id="4aebc-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aebc-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="4aebc-116">**Reset**</span></span>         | <span data-ttu-id="4aebc-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="4aebc-117">Not implemented.</span></span> <span data-ttu-id="4aebc-118">若要執行此方法，請參閱 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="4aebc-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/>                 |
| <span data-ttu-id="4aebc-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4aebc-119">**SetPowerState**</span></span> | <span data-ttu-id="4aebc-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="4aebc-120">Not implemented.</span></span> <span data-ttu-id="4aebc-121">若要執行此方法，請參閱 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法。</span><span class="sxs-lookup"><span data-stu-id="4aebc-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4aebc-122">屬性</span><span class="sxs-lookup"><span data-stu-id="4aebc-122">Properties</span></span>

<span data-ttu-id="4aebc-123">**Win32 \_ MemoryDevice** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-123">The **Win32\_MemoryDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4aebc-124">**存取**</span><span class="sxs-lookup"><span data-stu-id="4aebc-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4aebc-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-127">媒體存取可用。</span><span class="sxs-lookup"><span data-stu-id="4aebc-127">Media access available.</span></span>

<span data-ttu-id="4aebc-128">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4aebc-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="4aebc-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="4aebc-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="4aebc-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="4aebc-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-132">可寫入</span><span class="sxs-lookup"><span data-stu-id="4aebc-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="4aebc-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="4aebc-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="4aebc-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="4aebc-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="4aebc-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-136">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="4aebc-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-138">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-Bit Memory Error Information Information \| 供應商症狀" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="4aebc-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-139">其他錯誤資訊的陣列。</span><span class="sxs-lookup"><span data-stu-id="4aebc-139">Array of additional error information.</span></span> <span data-ttu-id="4aebc-140">例如，錯誤檢查和修正 (ECC) 的症狀，或如果使用迴圈冗余檢查 (CRC) 型的錯誤方法，則會傳回檢查位。</span><span class="sxs-lookup"><span data-stu-id="4aebc-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based error methodology is used.</span></span> <span data-ttu-id="4aebc-141">在後者的情況下，如果已辨識出單一位錯誤，而且已知 CRC 演算法，則可以判斷失敗的確切位。</span><span class="sxs-lookup"><span data-stu-id="4aebc-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="4aebc-142">這種類型的資料 (ECC 的症狀、Check Bit、同位資料或其他廠商提供的資訊) 包含在此欄位中。</span><span class="sxs-lookup"><span data-stu-id="4aebc-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="4aebc-143">只有當 **ErrorInfo** 屬性不等於3時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="4aebc-144">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-145">**可用性**</span><span class="sxs-lookup"><span data-stu-id="4aebc-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-146">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4aebc-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="4aebc-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-149">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="4aebc-149">Availability and status of the device.</span></span>

<span data-ttu-id="4aebc-150">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4aebc-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4aebc-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4aebc-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="4aebc-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="4aebc-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-154">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="4aebc-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4aebc-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="4aebc-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="4aebc-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="4aebc-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4aebc-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="4aebc-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4aebc-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="4aebc-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="4aebc-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="4aebc-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="4aebc-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="4aebc-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4aebc-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="4aebc-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="4aebc-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="4aebc-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="4aebc-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="4aebc-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4aebc-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="4aebc-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-165">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="4aebc-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4aebc-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="4aebc-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-167">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="4aebc-167">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4aebc-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="4aebc-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-169">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="4aebc-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4aebc-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="4aebc-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4aebc-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="4aebc-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-172">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="4aebc-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4aebc-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="4aebc-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-174">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="4aebc-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="4aebc-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="4aebc-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-176">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="4aebc-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4aebc-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="4aebc-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-178">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="4aebc-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="4aebc-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="4aebc-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-180">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="4aebc-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="4aebc-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-182">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4aebc-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-184">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="4aebc-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-185">形成此儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4aebc-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="4aebc-186">如果未知或區塊概念無效 (例如，針對匯總範圍、記憶體或邏輯磁片) ，請輸入1。</span><span class="sxs-lookup"><span data-stu-id="4aebc-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="4aebc-187">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="4aebc-188">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-189">**標題**</span><span class="sxs-lookup"><span data-stu-id="4aebc-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-192">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-193">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="4aebc-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="4aebc-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4aebc-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-196">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4aebc-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-198">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-199">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4aebc-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="4aebc-200">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="4aebc-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="4aebc-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="4aebc-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-203">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="4aebc-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="4aebc-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="4aebc-205">(1)</span><span class="sxs-lookup"><span data-stu-id="4aebc-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-206">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="4aebc-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4aebc-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="4aebc-208">(2)</span><span class="sxs-lookup"><span data-stu-id="4aebc-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="4aebc-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="4aebc-210">(3)</span><span class="sxs-lookup"><span data-stu-id="4aebc-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-211">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="4aebc-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4aebc-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="4aebc-213">(4)</span><span class="sxs-lookup"><span data-stu-id="4aebc-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-214">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4aebc-214">Device is not working properly.</span></span> <span data-ttu-id="4aebc-215">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="4aebc-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="4aebc-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="4aebc-217">(5)</span><span class="sxs-lookup"><span data-stu-id="4aebc-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-218">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="4aebc-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="4aebc-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="4aebc-220">(6)</span><span class="sxs-lookup"><span data-stu-id="4aebc-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-221">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="4aebc-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="4aebc-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="4aebc-223">(7)</span><span class="sxs-lookup"><span data-stu-id="4aebc-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="4aebc-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="4aebc-225">(8)</span><span class="sxs-lookup"><span data-stu-id="4aebc-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-226">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="4aebc-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="4aebc-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="4aebc-228">(9)</span><span class="sxs-lookup"><span data-stu-id="4aebc-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-229">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4aebc-229">Device is not working properly.</span></span> <span data-ttu-id="4aebc-230">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="4aebc-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="4aebc-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="4aebc-232">(10)</span><span class="sxs-lookup"><span data-stu-id="4aebc-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-233">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="4aebc-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="4aebc-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="4aebc-235">(11)</span><span class="sxs-lookup"><span data-stu-id="4aebc-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-236">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="4aebc-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="4aebc-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="4aebc-238"> (12) </span><span class="sxs-lookup"><span data-stu-id="4aebc-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-239">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="4aebc-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="4aebc-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="4aebc-241">(13)</span><span class="sxs-lookup"><span data-stu-id="4aebc-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-242">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="4aebc-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="4aebc-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="4aebc-244">(14)</span><span class="sxs-lookup"><span data-stu-id="4aebc-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-245">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4aebc-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="4aebc-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="4aebc-247">(15)</span><span class="sxs-lookup"><span data-stu-id="4aebc-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-248">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4aebc-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="4aebc-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="4aebc-250">(16)</span><span class="sxs-lookup"><span data-stu-id="4aebc-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-251">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="4aebc-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="4aebc-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="4aebc-253">(17)</span><span class="sxs-lookup"><span data-stu-id="4aebc-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-254">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="4aebc-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4aebc-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="4aebc-256">(18)</span><span class="sxs-lookup"><span data-stu-id="4aebc-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-257">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4aebc-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="4aebc-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="4aebc-259">(19)</span><span class="sxs-lookup"><span data-stu-id="4aebc-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4aebc-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="4aebc-261">(20)</span><span class="sxs-lookup"><span data-stu-id="4aebc-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-262">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="4aebc-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="4aebc-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="4aebc-264">(21)</span><span class="sxs-lookup"><span data-stu-id="4aebc-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-265">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="4aebc-265">System failure.</span></span> <span data-ttu-id="4aebc-266">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="4aebc-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="4aebc-267">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="4aebc-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="4aebc-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="4aebc-269">(22)</span><span class="sxs-lookup"><span data-stu-id="4aebc-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-270">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="4aebc-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="4aebc-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="4aebc-272">(23)</span><span class="sxs-lookup"><span data-stu-id="4aebc-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-273">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="4aebc-273">System failure.</span></span> <span data-ttu-id="4aebc-274">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="4aebc-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="4aebc-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="4aebc-276">(24)</span><span class="sxs-lookup"><span data-stu-id="4aebc-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-277">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4aebc-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4aebc-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4aebc-279">(25)</span><span class="sxs-lookup"><span data-stu-id="4aebc-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-280">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="4aebc-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4aebc-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4aebc-282">(26)</span><span class="sxs-lookup"><span data-stu-id="4aebc-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-283">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="4aebc-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="4aebc-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="4aebc-285">(27)</span><span class="sxs-lookup"><span data-stu-id="4aebc-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-286">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="4aebc-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="4aebc-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="4aebc-288">(28)</span><span class="sxs-lookup"><span data-stu-id="4aebc-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-289">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4aebc-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="4aebc-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="4aebc-291">(29)</span><span class="sxs-lookup"><span data-stu-id="4aebc-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-292">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="4aebc-292">Device is disabled.</span></span> <span data-ttu-id="4aebc-293">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="4aebc-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="4aebc-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="4aebc-295">(30)</span><span class="sxs-lookup"><span data-stu-id="4aebc-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-296">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="4aebc-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4aebc-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="4aebc-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="4aebc-298"> (31) </span><span class="sxs-lookup"><span data-stu-id="4aebc-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-299">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="4aebc-299">Device is not working properly.</span></span> <span data-ttu-id="4aebc-300">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4aebc-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="4aebc-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-302">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4aebc-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-304">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-305">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="4aebc-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="4aebc-306">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="4aebc-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-308">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4aebc-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-310">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Type" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-311">若 **為 True**，表示最新的錯誤是可修正的。</span><span class="sxs-lookup"><span data-stu-id="4aebc-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="4aebc-312">如果 **ErrorInfo** 設定為3，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="4aebc-313">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4aebc-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-315">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-317">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4aebc-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-318">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="4aebc-318">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="4aebc-319">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="4aebc-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4aebc-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-321">**說明**</span><span class="sxs-lookup"><span data-stu-id="4aebc-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-324">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-325">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="4aebc-325">Description of the object.</span></span>

<span data-ttu-id="4aebc-326">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4aebc-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-330">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-331">記憶體裝置的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4aebc-331">Unique identifier of the memory device.</span></span>

<span data-ttu-id="4aebc-332">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4aebc-333">範例：「記憶體裝置1」</span><span class="sxs-lookup"><span data-stu-id="4aebc-333">Example: "Memory Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="4aebc-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-335">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4aebc-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-337">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 19 \| 記憶體裝置對應位址 \| 結束位址」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-338">應用程式或作業系統所參考的結束位址。</span><span class="sxs-lookup"><span data-stu-id="4aebc-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="4aebc-339">此記憶體位址是由記憶體控制器針對這個記憶體物件所對應。</span><span class="sxs-lookup"><span data-stu-id="4aebc-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="4aebc-340">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-340">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="4aebc-341">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-341">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-342">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="4aebc-342">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-343">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4aebc-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-344">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-345">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Operation" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-346">造成最後一個錯誤的記憶體存取作業類型。</span><span class="sxs-lookup"><span data-stu-id="4aebc-346">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="4aebc-347">只有當 **ErrorInfo** 未設定為3時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="4aebc-347">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="4aebc-348">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-348">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4aebc-349">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4aebc-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-350">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4aebc-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="4aebc-351">**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="4aebc-351">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="4aebc-352">**撰寫** (4) </span><span class="sxs-lookup"><span data-stu-id="4aebc-352">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="4aebc-353">**部分寫入** (5) </span><span class="sxs-lookup"><span data-stu-id="4aebc-353">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-354">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="4aebc-354">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-355">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4aebc-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-357">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Address" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-357">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-358">最後一個記憶體錯誤的位址。</span><span class="sxs-lookup"><span data-stu-id="4aebc-358">Address of the last memory error.</span></span> <span data-ttu-id="4aebc-359">只有當 **ErrorInfo** 未設定為3時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-359">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="4aebc-360">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-360">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="4aebc-361">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-362">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4aebc-362">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-363">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4aebc-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-365">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="4aebc-365">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="4aebc-366">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-367">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="4aebc-367">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-368">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="4aebc-368">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-370">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS」 ) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="4aebc-370">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-371">從最後一個記憶體存取所捕捉到的資料陣列，但發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4aebc-371">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="4aebc-372">資料會佔用陣列的前 *n* 個八位數位，以保存 **ErrorTransferSize** 屬性所指定的位數。</span><span class="sxs-lookup"><span data-stu-id="4aebc-372">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="4aebc-373">如果 **ErrorTransferSize** 為 0 (零) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-373">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="4aebc-374">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-374">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-375">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="4aebc-375">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-376">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4aebc-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-378">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-379">排序儲存在 **ErrorData** 屬性中的資料。</span><span class="sxs-lookup"><span data-stu-id="4aebc-379">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="4aebc-380">只有當 **ErrorTransferSize** 為 0 (零) 時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-380">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="4aebc-381">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-381">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-382">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4aebc-382">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="4aebc-383">**最不重要的位元組先** (1) </span><span class="sxs-lookup"><span data-stu-id="4aebc-383">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="4aebc-384">**最重要的位元組先** (2) </span><span class="sxs-lookup"><span data-stu-id="4aebc-384">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-385">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4aebc-385">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-386">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-387">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-388">**LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4aebc-388">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="4aebc-389">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-390">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="4aebc-390">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-391">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4aebc-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-392">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-393">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| Error 細微性" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-394">可以解決錯誤的層級。</span><span class="sxs-lookup"><span data-stu-id="4aebc-394">Level where the error can be resolved.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4aebc-395">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4aebc-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-396">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4aebc-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_level"></span><span id="device_level"></span><span id="DEVICE_LEVEL"></span>

<span data-ttu-id="4aebc-397">**裝置層級** (3) </span><span class="sxs-lookup"><span data-stu-id="4aebc-397">**Device level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_partition_level"></span><span id="memory_partition_level"></span><span id="MEMORY_PARTITION_LEVEL"></span>

<span data-ttu-id="4aebc-398">**記憶體分割層級** (4) </span><span class="sxs-lookup"><span data-stu-id="4aebc-398">**Memory partition level** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-399">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4aebc-399">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-400">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4aebc-400">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-401">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-402">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 記憶體**](cim-memory.md)」。**OtherErrorDescription**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS \| Type 18 \| 32-Bit Memory error Information \| error Type ") </span><span class="sxs-lookup"><span data-stu-id="4aebc-402">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-403">最近發生的錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="4aebc-403">Type of error that occurred most recently.</span></span> <span data-ttu-id="4aebc-404">值12-14，指出是否可更正錯誤，不會與這個屬性一起使用，但是這項資訊會在 **CorrectableError** 屬性中找到。</span><span class="sxs-lookup"><span data-stu-id="4aebc-404">The values 12-14, indicating whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="4aebc-405">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-405">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4aebc-406">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4aebc-406">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-407">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4aebc-407">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4aebc-408">**確定** (3) </span><span class="sxs-lookup"><span data-stu-id="4aebc-408">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="4aebc-409">**讀取** (4) 錯誤</span><span class="sxs-lookup"><span data-stu-id="4aebc-409">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="4aebc-410">同位 **錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="4aebc-410">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="4aebc-411">**單一位錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="4aebc-411">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="4aebc-412">**雙位錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="4aebc-412">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="4aebc-413">**多位錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="4aebc-413">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="4aebc-414">**半位元組錯誤** (9) </span><span class="sxs-lookup"><span data-stu-id="4aebc-414">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="4aebc-415">總和 **檢查碼錯誤** (10) </span><span class="sxs-lookup"><span data-stu-id="4aebc-415">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="4aebc-416">**CRC 錯誤** (11) </span><span class="sxs-lookup"><span data-stu-id="4aebc-416">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="4aebc-417">**修正了單一位錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="4aebc-417">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="4aebc-418">**更正錯誤** (13) </span><span class="sxs-lookup"><span data-stu-id="4aebc-418">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="4aebc-419">無法 **更正的錯誤** (14) </span><span class="sxs-lookup"><span data-stu-id="4aebc-419">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-420">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="4aebc-420">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-421">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-422">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-423">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 16 \| 實體記憶體陣列 \| 記憶體錯誤更正" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-424">記憶體硬體所使用的錯誤檢查類型。</span><span class="sxs-lookup"><span data-stu-id="4aebc-424">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="4aebc-425">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-425">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="4aebc-426">值如下：</span><span class="sxs-lookup"><span data-stu-id="4aebc-426">The values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4aebc-427">**其他** ( "其他" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-427">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-428">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-428">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="4aebc-429">同 **位 ( 「** 同位」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-429">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="4aebc-430">**單一位 ecc** ( 「單一位 ecc」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-430">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="4aebc-431">**多位 ecc** ( 「多重位 ecc」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-431">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="4aebc-432">**無** ( 「無」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-432">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="4aebc-433">**Crc** ( 「crc」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-433">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-434">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="4aebc-434">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-435">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4aebc-435">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-436">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-437">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| Error 解決" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-438">實際決定造成錯誤的資料量。</span><span class="sxs-lookup"><span data-stu-id="4aebc-438">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="4aebc-439">當 **ErrorInfo** 屬性設定為3時，不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-439">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="4aebc-440">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-440">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="4aebc-441">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-441">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-442">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="4aebc-442">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-443">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4aebc-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-445">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-445">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-446">上次發生記憶體錯誤的時間。</span><span class="sxs-lookup"><span data-stu-id="4aebc-446">Time that the last memory error occurred.</span></span> <span data-ttu-id="4aebc-447">只有當 **ErrorInfo** 未設定為3時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="4aebc-447">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="4aebc-448">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-448">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-449">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="4aebc-449">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-450">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4aebc-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-451">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-452">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-453">資料 (的大小，其中包含上次傳送的錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="4aebc-453">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="4aebc-454">如果沒有任何錯誤，這個屬性會設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="4aebc-454">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="4aebc-455">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-455">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-456">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4aebc-456">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-457">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="4aebc-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-458">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-459">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="4aebc-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-460">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="4aebc-460">Date and time the object was installed.</span></span> <span data-ttu-id="4aebc-461">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="4aebc-461">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4aebc-462">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-462">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-463">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4aebc-463">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-464">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4aebc-464">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-465">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-466">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4aebc-466">Last error code reported by the logical device.</span></span>

<span data-ttu-id="4aebc-467">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-468">**名稱**</span><span class="sxs-lookup"><span data-stu-id="4aebc-468">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-469">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-470">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-471">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-471">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-472">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="4aebc-472">Label by which the object is known.</span></span> <span data-ttu-id="4aebc-473">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-473">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="4aebc-474">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-474">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-475">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="4aebc-475">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-476">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4aebc-476">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-478">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="4aebc-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-479">連續區塊總數，每個區塊會封鎖 **區塊** 屬性中包含的值大小，這會形成此儲存範圍。</span><span class="sxs-lookup"><span data-stu-id="4aebc-479">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="4aebc-480">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="4aebc-480">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="4aebc-481">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="4aebc-481">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="4aebc-482">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-482">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="4aebc-483">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-483">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-484">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4aebc-484">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-485">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-486">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-487">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 記憶體**](cim-memory.md)」。**ErrorInfo**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ") </span><span class="sxs-lookup"><span data-stu-id="4aebc-487">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-488">當 **ErrorInfo** 屬性設定為1時的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="4aebc-488">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="4aebc-489">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-489">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-490">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4aebc-490">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-491">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-492">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-493">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-493">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-494">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="4aebc-494">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="4aebc-495">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-495">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4aebc-496">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="4aebc-496">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-497">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4aebc-497">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-498">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="4aebc-498">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-499">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-500">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="4aebc-500">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="4aebc-501">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="4aebc-501">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="4aebc-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4aebc-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="4aebc-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4aebc-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="4aebc-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4aebc-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="4aebc-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-506">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="4aebc-506">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4aebc-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="4aebc-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-508">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="4aebc-508">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4aebc-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="4aebc-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-510">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4aebc-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="4aebc-511">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="4aebc-511">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="4aebc-512">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-512">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4aebc-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="4aebc-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-514">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="4aebc-514">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4aebc-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="4aebc-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4aebc-516">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="4aebc-516">Timed Power-On Supported</span></span>

<span data-ttu-id="4aebc-517">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="4aebc-517">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-518">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4aebc-518">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-519">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4aebc-519">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-520">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-520">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-521">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="4aebc-521">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="4aebc-522">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="4aebc-522">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="4aebc-523">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-524">**目的**</span><span class="sxs-lookup"><span data-stu-id="4aebc-524">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-525">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-526">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-527">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="4aebc-527">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="4aebc-528">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-528">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-529">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="4aebc-529">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-530">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="4aebc-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-531">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-532">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 19 \| 記憶體裝置對應位址 \| 起始位址」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-532">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-533">應用程式或作業系統所參考的起始位址。</span><span class="sxs-lookup"><span data-stu-id="4aebc-533">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="4aebc-534">此記憶體位址是由記憶體控制器針對這個記憶體物件所對應。</span><span class="sxs-lookup"><span data-stu-id="4aebc-534">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="4aebc-535">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-535">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="4aebc-536">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-536">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-537">**狀態**</span><span class="sxs-lookup"><span data-stu-id="4aebc-537">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-538">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-539">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-540">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-540">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-541">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="4aebc-541">Current status of the object.</span></span> <span data-ttu-id="4aebc-542">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="4aebc-542">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4aebc-543">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="4aebc-543">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4aebc-544">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="4aebc-544">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4aebc-545">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="4aebc-545">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4aebc-546">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="4aebc-546">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4aebc-547">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-547">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4aebc-548">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="4aebc-548">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4aebc-549">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-549">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4aebc-550">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-550">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4aebc-551">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-551">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-552">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-552">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4aebc-553">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-553">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4aebc-554">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-554">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4aebc-555">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-555">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4aebc-556">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-556">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4aebc-557">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-557">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4aebc-558">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-558">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4aebc-559">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-559">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4aebc-560">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-560">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-561">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4aebc-561">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-562">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="4aebc-562">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-563">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-563">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-564">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="4aebc-564">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-565">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="4aebc-565">State of the logical device.</span></span> <span data-ttu-id="4aebc-566">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="4aebc-566">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="4aebc-567">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-567">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4aebc-568">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="4aebc-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4aebc-569">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="4aebc-569">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4aebc-570">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="4aebc-570">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4aebc-571">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="4aebc-571">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4aebc-572">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="4aebc-572">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4aebc-573">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4aebc-573">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-574">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-575">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-575">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-576">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4aebc-576">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-577">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="4aebc-577">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="4aebc-578">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-578">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-579">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="4aebc-579">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-580">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4aebc-580">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-581">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-582">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Address" ) </span><span class="sxs-lookup"><span data-stu-id="4aebc-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-583">若 **為 True**， **ErrorAddress** 屬性中的位址資訊就是系統層級的位址。</span><span class="sxs-lookup"><span data-stu-id="4aebc-583">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="4aebc-584">如果為 **FALSE**，則為實體位址。</span><span class="sxs-lookup"><span data-stu-id="4aebc-584">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="4aebc-585">只有當 **ErrorInfo** 未設定為3時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="4aebc-585">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="4aebc-586">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-586">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="4aebc-587">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4aebc-587">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4aebc-588">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4aebc-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-589">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="4aebc-589">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4aebc-590">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4aebc-590">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4aebc-591">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="4aebc-591">Name of the scoping system.</span></span>

<span data-ttu-id="4aebc-592">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-592">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4aebc-593">備註</span><span class="sxs-lookup"><span data-stu-id="4aebc-593">Remarks</span></span>

<span data-ttu-id="4aebc-594">**Win32 \_ MemoryDevice** 類別衍生自 [**win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="4aebc-594">The **Win32\_MemoryDevice** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4aebc-595">範例</span><span class="sxs-lookup"><span data-stu-id="4aebc-595">Examples</span></span>

<span data-ttu-id="4aebc-596">[列出記憶體裝置](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858)Perl 範例會傳回電腦上所安裝所有記憶體裝置的開始和結束位址。</span><span class="sxs-lookup"><span data-stu-id="4aebc-596">The [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Perl sample returns starting and ending addresses for all memory devices installed on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aebc-597">規格需求</span><span class="sxs-lookup"><span data-stu-id="4aebc-597">Requirements</span></span>



| <span data-ttu-id="4aebc-598">需求</span><span class="sxs-lookup"><span data-stu-id="4aebc-598">Requirement</span></span> | <span data-ttu-id="4aebc-599">值</span><span class="sxs-lookup"><span data-stu-id="4aebc-599">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4aebc-600">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4aebc-600">Minimum supported client</span></span><br/> | <span data-ttu-id="4aebc-601">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4aebc-601">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4aebc-602">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4aebc-602">Minimum supported server</span></span><br/> | <span data-ttu-id="4aebc-603">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4aebc-603">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4aebc-604">命名空間</span><span class="sxs-lookup"><span data-stu-id="4aebc-604">Namespace</span></span><br/>                | <span data-ttu-id="4aebc-605">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4aebc-605">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4aebc-606">MOF</span><span class="sxs-lookup"><span data-stu-id="4aebc-606">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4aebc-607"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4aebc-607"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4aebc-608">DLL</span><span class="sxs-lookup"><span data-stu-id="4aebc-608">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aebc-609"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aebc-609"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aebc-610">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4aebc-610">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aebc-611">**Win32 \_ SMBIOSMemory**</span><span class="sxs-lookup"><span data-stu-id="4aebc-611">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="4aebc-612">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4aebc-612">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

