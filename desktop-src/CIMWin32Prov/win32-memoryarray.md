---
description: Win32 \_ MEMORYARRAY WMI 類別代表電腦系統記憶體陣列和對應位址的屬性。
ms.assetid: 56ff6960-cde3-4e34-b4df-d2993bafaa62
ms.tgt_platform: multiple
title: Win32_MemoryArray 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArray
- Win32_MemoryArray.Reset
- Win32_MemoryArray.SetPowerState
- Win32_MemoryArray.Access
- Win32_MemoryArray.AdditionalErrorData
- Win32_MemoryArray.Availability
- Win32_MemoryArray.BlockSize
- Win32_MemoryArray.Caption
- Win32_MemoryArray.ConfigManagerErrorCode
- Win32_MemoryArray.ConfigManagerUserConfig
- Win32_MemoryArray.CorrectableError
- Win32_MemoryArray.CreationClassName
- Win32_MemoryArray.Description
- Win32_MemoryArray.DeviceID
- Win32_MemoryArray.EndingAddress
- Win32_MemoryArray.ErrorAccess
- Win32_MemoryArray.ErrorAddress
- Win32_MemoryArray.ErrorCleared
- Win32_MemoryArray.ErrorData
- Win32_MemoryArray.ErrorDataOrder
- Win32_MemoryArray.ErrorDescription
- Win32_MemoryArray.ErrorGranularity
- Win32_MemoryArray.ErrorInfo
- Win32_MemoryArray.ErrorMethodology
- Win32_MemoryArray.ErrorResolution
- Win32_MemoryArray.ErrorTime
- Win32_MemoryArray.ErrorTransferSize
- Win32_MemoryArray.InstallDate
- Win32_MemoryArray.LastErrorCode
- Win32_MemoryArray.Name
- Win32_MemoryArray.NumberOfBlocks
- Win32_MemoryArray.OtherErrorDescription
- Win32_MemoryArray.PNPDeviceID
- Win32_MemoryArray.PowerManagementCapabilities
- Win32_MemoryArray.PowerManagementSupported
- Win32_MemoryArray.Purpose
- Win32_MemoryArray.StartingAddress
- Win32_MemoryArray.Status
- Win32_MemoryArray.StatusInfo
- Win32_MemoryArray.SystemCreationClassName
- Win32_MemoryArray.SystemLevelAddress
- Win32_MemoryArray.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c102d383502bec4808b26a87eb2f6d8445b6c2a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191018"
---
# <a name="win32_memoryarray-class"></a><span data-ttu-id="eb6b8-103">Win32 \_ MemoryArray 類別</span><span class="sxs-lookup"><span data-stu-id="eb6b8-103">Win32\_MemoryArray class</span></span>

<span data-ttu-id="eb6b8-104">**Win32 \_ MemoryArray** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表電腦系統記憶體陣列和對應位址的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-104">The **Win32\_MemoryArray** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of the computer system memory array and mapped addresses.</span></span>

<span data-ttu-id="eb6b8-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="eb6b8-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb6b8-107">語法</span><span class="sxs-lookup"><span data-stu-id="eb6b8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryArray : Win32_SMBIOSMemory
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

## <a name="members"></a><span data-ttu-id="eb6b8-108">成員</span><span class="sxs-lookup"><span data-stu-id="eb6b8-108">Members</span></span>

<span data-ttu-id="eb6b8-109">**Win32 \_ MemoryArray** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="eb6b8-109">The **Win32\_MemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="eb6b8-110">方法</span><span class="sxs-lookup"><span data-stu-id="eb6b8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="eb6b8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="eb6b8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eb6b8-112">方法</span><span class="sxs-lookup"><span data-stu-id="eb6b8-112">Methods</span></span>

<span data-ttu-id="eb6b8-113">**Win32 \_ MemoryArray** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-113">The **Win32\_MemoryArray** class has these methods.</span></span>



| <span data-ttu-id="eb6b8-114">方法</span><span class="sxs-lookup"><span data-stu-id="eb6b8-114">Method</span></span>            | <span data-ttu-id="eb6b8-115">描述</span><span class="sxs-lookup"><span data-stu-id="eb6b8-115">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb6b8-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-116">**Reset**</span></span>         | <span data-ttu-id="eb6b8-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-117">Not implemented.</span></span> <span data-ttu-id="eb6b8-118">若要執行此方法，請參閱 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="eb6b8-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-119">**SetPowerState**</span></span> | <span data-ttu-id="eb6b8-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-120">Not implemented.</span></span> <span data-ttu-id="eb6b8-121">若要執行此方法，請參閱 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法，以取得檔。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="eb6b8-122">屬性</span><span class="sxs-lookup"><span data-stu-id="eb6b8-122">Properties</span></span>

<span data-ttu-id="eb6b8-123">**Win32 \_ MemoryArray** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-123">The **Win32\_MemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb6b8-124">**存取**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-127">可用的媒體存取類型。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-127">Type of media access available.</span></span>

<span data-ttu-id="eb6b8-128">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6b8-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="eb6b8-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="eb6b8-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-132">可寫入</span><span class="sxs-lookup"><span data-stu-id="eb6b8-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="eb6b8-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="eb6b8-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-136">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="eb6b8-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-138">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-Bit Memory Error Information Information \| 供應商症狀" ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-139">其他錯誤資訊的陣列。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-139">Array of additional error information.</span></span> <span data-ttu-id="eb6b8-140">例如，錯誤檢查和修正 (ECC) 的症狀，或如果使用迴圈冗余檢查 (CRC) **ErrorMethodology** 值，則會傳回檢查位。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based **ErrorMethodology** value is used.</span></span> <span data-ttu-id="eb6b8-141">在後者的情況下，如果已辨識出單一位錯誤，而且已知 CRC 演算法，則可以判斷失敗的確切位。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="eb6b8-142">這種類型的資料 (ECC 的症狀、Check Bit、同位資料或其他廠商提供的資訊) 包含在此欄位中。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="eb6b8-143">只有當 **ErrorInfo** 屬性不等於3時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="eb6b8-144">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-145">**可用性**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-146">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="eb6b8-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-149">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-149">Availability and status of the device.</span></span>

<span data-ttu-id="eb6b8-150">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb6b8-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6b8-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="eb6b8-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-154">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="eb6b8-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="eb6b8-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="eb6b8-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="eb6b8-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="eb6b8-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="eb6b8-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="eb6b8-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="eb6b8-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eb6b8-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="eb6b8-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="eb6b8-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="eb6b8-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-165">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="eb6b8-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-167">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-167">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="eb6b8-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-169">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="eb6b8-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="eb6b8-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-172">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="eb6b8-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-174">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="eb6b8-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-176">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="eb6b8-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-178">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="eb6b8-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-180">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-182">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-184">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="eb6b8-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-185">形成此儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="eb6b8-186">如果未知或區塊概念無效 (例如，針對匯總範圍、記憶體或邏輯磁片) ，請輸入1。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="eb6b8-187">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="eb6b8-188">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-189">**標題**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-192">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-193">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="eb6b8-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-196">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-197">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-198">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-199">Windows 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="eb6b8-200">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="eb6b8-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="eb6b8-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-203">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="eb6b8-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="eb6b8-205">(1)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-206">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="eb6b8-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="eb6b8-208">(2)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="eb6b8-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="eb6b8-210">(3)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-211">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="eb6b8-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="eb6b8-213">(4)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-214">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-214">Device is not working properly.</span></span> <span data-ttu-id="eb6b8-215">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="eb6b8-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="eb6b8-217">(5)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-218">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="eb6b8-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="eb6b8-220">(6)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-221">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="eb6b8-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="eb6b8-223">(7)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="eb6b8-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="eb6b8-225">(8)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-226">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="eb6b8-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="eb6b8-228">(9)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-229">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-229">Device is not working properly.</span></span> <span data-ttu-id="eb6b8-230">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="eb6b8-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="eb6b8-232">(10)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-233">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="eb6b8-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="eb6b8-235">(11)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-236">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="eb6b8-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="eb6b8-238"> (12) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-239">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="eb6b8-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="eb6b8-241">(13)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-242">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="eb6b8-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="eb6b8-244">(14)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-245">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="eb6b8-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="eb6b8-247">(15)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-248">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="eb6b8-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="eb6b8-250">(16)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-251">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="eb6b8-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="eb6b8-253">(17)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-254">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="eb6b8-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="eb6b8-256">(18)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-257">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="eb6b8-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="eb6b8-259">(19)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="eb6b8-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="eb6b8-261">(20)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-262">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="eb6b8-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="eb6b8-264">(21)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-265">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-265">System failure.</span></span> <span data-ttu-id="eb6b8-266">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="eb6b8-267">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="eb6b8-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="eb6b8-269">(22)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-270">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="eb6b8-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="eb6b8-272">(23)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-273">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-273">System failure.</span></span> <span data-ttu-id="eb6b8-274">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="eb6b8-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="eb6b8-276">(24)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-277">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="eb6b8-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="eb6b8-279">(25)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-280">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="eb6b8-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="eb6b8-282">(26)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-283">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="eb6b8-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="eb6b8-285">(27)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-286">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="eb6b8-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="eb6b8-288">(28)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-289">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="eb6b8-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="eb6b8-291">(29)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-292">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-292">Device is disabled.</span></span> <span data-ttu-id="eb6b8-293">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="eb6b8-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="eb6b8-295">(30)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-296">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="eb6b8-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="eb6b8-298"> (31) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-299">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-299">Device is not working properly.</span></span> <span data-ttu-id="eb6b8-300">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-302">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-304">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-305">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="eb6b8-306">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-307">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-308">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-310">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Type" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-311">若 **為 True**，表示最新的錯誤是可修正的。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="eb6b8-312">如果 **ErrorInfo** 設定為3，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="eb6b8-313">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-315">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-317">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-318">第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="eb6b8-319">當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="eb6b8-320">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-321">**說明**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-322">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-324">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-325">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-325">Description of the object.</span></span>

<span data-ttu-id="eb6b8-326">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-328">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-329">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-330">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-331">記憶體陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-331">Unique identifier of the memory array.</span></span>

<span data-ttu-id="eb6b8-332">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="eb6b8-333">範例：「記憶體陣列1」</span><span class="sxs-lookup"><span data-stu-id="eb6b8-333">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-334">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-335">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-337">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 19 \| 記憶體裝置對應位址 \| 結束位址」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-338">應用程式或作業系統所參考的結束位址。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="eb6b8-339">此記憶體位址是由記憶體控制器針對這個記憶體物件所對應。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="eb6b8-340">此值來自 SMBIOS 版本資訊中的 **記憶體陣列對應位址** 結構。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-340">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="eb6b8-341">針對 SMBIOS 版本2.1 到2.6，此值來自 **結束位址** 成員。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-341">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Ending Address** member.</span></span> <span data-ttu-id="eb6b8-342">針對 SMBIOS 2.7 版 +，此值來自于 **擴充的結束位址** 成員。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-342">For SMBIOS version 2.7+ the value comes from the **Extended Ending Address** member.</span></span>

<span data-ttu-id="eb6b8-343">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-343">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="eb6b8-344">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-345">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-345">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-346">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-348">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Operation" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-348">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-349">造成最後一個錯誤的記憶體存取作業類型。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-349">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="eb6b8-350">只有當 **ErrorInfo** 未設定為3時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-350">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="eb6b8-351">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-351">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb6b8-352">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-352">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6b8-353">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-353">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="eb6b8-354">**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-354">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="eb6b8-355">**撰寫** (4) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-355">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="eb6b8-356">**部分寫入** (5) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-356">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-357">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-357">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-358">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-360">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Address" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-361">最後一個記憶體錯誤的位址。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-361">Address of the last memory error.</span></span> <span data-ttu-id="eb6b8-362">只有當 **ErrorInfo** 未設定為3時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-362">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="eb6b8-363">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-363">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="eb6b8-364">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-365">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-366">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-368">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-368">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="eb6b8-369">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-370">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-371">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="eb6b8-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-373">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 、 [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS」 ) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-374">從最後一個記憶體存取所捕捉到的資料陣列，但發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-374">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="eb6b8-375">資料會佔用陣列的前 *n* 個八位數位，以保存 **ErrorTransferSize** 屬性所指定的位數。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-375">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="eb6b8-376">如果 **ErrorTransferSize** 為 0 (零) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-376">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="eb6b8-377">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-377">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-378">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-379">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-381">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-382">排序儲存在 **ErrorData** 屬性中的資料。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-382">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="eb6b8-383">只有當 **ErrorTransferSize** 為 0 (零) 時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-383">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="eb6b8-384">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-384">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6b8-385">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-385">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="eb6b8-386">**最不重要的位元組先** (1) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-386">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="eb6b8-387">**最重要的位元組先** (2) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-387">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-388">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-388">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-389">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-390">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-391">**LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-391">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="eb6b8-392">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-393">**ErrorGranularity**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-393">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-394">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-395">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-396">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| Error 細微性" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-397">可以解決錯誤的層級。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-397">Level where the error can be resolved.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="eb6b8-398">**1** (其他) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-398">**1** (Other)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="eb6b8-399">**2** (未知) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-399">**2** (Unknown)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="eb6b8-400">**3** (裝置層級) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-400">**3** (Device level)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="eb6b8-401">**4** (記憶體分割區層級) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-401">**4** (Memory partition level)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-402">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-402">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-403">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-405">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 記憶體**](cim-memory.md)」。**OtherErrorDescription**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS \| Type 18 \| 32-Bit Memory error Information \| error Type ") </span><span class="sxs-lookup"><span data-stu-id="eb6b8-405">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-406">最近發生的錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-406">Type of error that occurred most recently.</span></span> <span data-ttu-id="eb6b8-407">值12-14 （指出錯誤是否可更正）不會與這個屬性一起使用，但這項資訊可在 **CorrectableError** 屬性中找到。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-407">The values 12-14, which indicate whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="eb6b8-408">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-408">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb6b8-409">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6b8-410">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="eb6b8-411">**確定** (3) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-411">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="eb6b8-412">**讀取** (4) 錯誤</span><span class="sxs-lookup"><span data-stu-id="eb6b8-412">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="eb6b8-413">同位 **錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-413">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="eb6b8-414">**單一位錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-414">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="eb6b8-415">**雙位錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-415">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="eb6b8-416">**多位錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-416">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="eb6b8-417">**半位元組錯誤** (9) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-417">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="eb6b8-418">總和 **檢查碼錯誤** (10) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-418">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="eb6b8-419">**CRC 錯誤** (11) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-419">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="eb6b8-420">**修正了單一位錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-420">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="eb6b8-421">**更正錯誤** (13) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-421">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="eb6b8-422">無法 **更正的錯誤** (14) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-422">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-423">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-423">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-426">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 16 \| 實體記憶體陣列 \| 記憶體錯誤更正" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-427">記憶體硬體所使用的錯誤檢查類型。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-427">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="eb6b8-428">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="eb6b8-429">值如下：</span><span class="sxs-lookup"><span data-stu-id="eb6b8-429">The values are:</span></span>

<dl> <dd><span data-ttu-id="eb6b8-430">另外</span><span class="sxs-lookup"><span data-stu-id="eb6b8-430">"Other"</span></span></dd> <dd><span data-ttu-id="eb6b8-431">不明</span><span class="sxs-lookup"><span data-stu-id="eb6b8-431">"Unknown"</span></span></dd> <dd><span data-ttu-id="eb6b8-432">"None"</span><span class="sxs-lookup"><span data-stu-id="eb6b8-432">"None"</span></span></dd> <dd><span data-ttu-id="eb6b8-433">位</span><span class="sxs-lookup"><span data-stu-id="eb6b8-433">"Parity"</span></span></dd> <dd><span data-ttu-id="eb6b8-434">「單一位 ECC」</span><span class="sxs-lookup"><span data-stu-id="eb6b8-434">"Single-bit ECC"</span></span></dd> <dd><span data-ttu-id="eb6b8-435">「多重位 ECC」</span><span class="sxs-lookup"><span data-stu-id="eb6b8-435">"Multi-bit ECC"</span></span></dd> <dd><span data-ttu-id="eb6b8-436">CRC</span><span class="sxs-lookup"><span data-stu-id="eb6b8-436">"CRC"</span></span></dd> </dl>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb6b8-437">**其他** ( "其他" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-437">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6b8-438">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-438">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="eb6b8-439">**無** ( 「無」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-439">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="eb6b8-440">同 **位 ( 「** 同位」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-440">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="eb6b8-441">**單一位 ecc** ( 「單一位 ecc」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-441">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="eb6b8-442">**多位 ecc** ( 「多重位 ecc」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-442">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="eb6b8-443">**Crc** ( 「crc」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-443">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-444">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-444">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-445">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-447">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| Error 解決" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bytes" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-447">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-448">實際決定造成錯誤的資料量。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-448">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="eb6b8-449">當 **ErrorInfo** 屬性設定為3時，不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-449">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="eb6b8-450">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-450">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="eb6b8-451">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-451">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-452">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-452">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-453">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-454">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-455">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-455">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-456">上次發生記憶體錯誤的時間。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-456">Time that the last memory error occurred.</span></span> <span data-ttu-id="eb6b8-457">只有當 **ErrorInfo** 未設定為3時，這個屬性才有效。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-457">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="eb6b8-458">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-458">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-459">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-459">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-460">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-460">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-461">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-462">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-463">資料 (的大小，其中包含上次傳送的錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-463">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="eb6b8-464">如果沒有任何錯誤，這個屬性會設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-464">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="eb6b8-465">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-465">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-466">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-466">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-467">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-467">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-468">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-469">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="eb6b8-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-470">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-470">Date and time the object was installed.</span></span> <span data-ttu-id="eb6b8-471">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-471">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="eb6b8-472">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-472">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-473">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-473">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-474">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-474">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-476">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-476">Last error code reported by the logical device.</span></span>

<span data-ttu-id="eb6b8-477">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-478">**名稱**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-478">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-479">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-480">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-481">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-481">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-482">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-482">Label by which the object is known.</span></span> <span data-ttu-id="eb6b8-483">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-483">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="eb6b8-484">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-484">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-485">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-485">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-486">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-488">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="eb6b8-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-489">連續區塊總數，每個區塊會封鎖 **區塊** 屬性中包含的值大小，這會形成此儲存範圍。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-489">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="eb6b8-490">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-490">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="eb6b8-491">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-491">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="eb6b8-492">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-492">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="eb6b8-493">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-493">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-494">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-494">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-495">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-496">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-497">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 記憶體**](cim-memory.md)」。**ErrorInfo**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ") </span><span class="sxs-lookup"><span data-stu-id="eb6b8-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-498">當 **ErrorInfo** 屬性設定為1時的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-498">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="eb6b8-499">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-499">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-501">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-502">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-503">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-504">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-504">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="eb6b8-505">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="eb6b8-506">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="eb6b8-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-507">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-508">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="eb6b8-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-509">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-510">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="eb6b8-511">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6b8-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="eb6b8-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="eb6b8-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="eb6b8-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-516">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="eb6b8-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-518">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="eb6b8-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-520">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="eb6b8-521">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="eb6b8-522">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="eb6b8-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-524">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="eb6b8-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="eb6b8-526">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="eb6b8-526">Timed Power-On Supported</span></span>

<span data-ttu-id="eb6b8-527">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-527">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-528">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-528">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-529">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-530">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-531">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-531">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="eb6b8-532">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-532">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="eb6b8-533">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-533">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-534">**目的**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-534">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-535">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-536">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-537">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-537">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="eb6b8-538">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-538">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-539">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-539">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-540">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-540">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-541">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-542">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 19 \| 記憶體裝置對應位址 \| 起始位址」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-542">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-543">應用程式或作業系統所參考的起始位址。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-543">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="eb6b8-544">此記憶體位址是由記憶體控制器針對這個記憶體物件所對應。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-544">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="eb6b8-545">此值來自 SMBIOS 版本資訊中的 **記憶體陣列對應位址** 結構。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-545">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="eb6b8-546">針對 SMBIOS 版本2.1 到2.6，此值來自 **起始位址** 成員。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-546">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Starting Address** member.</span></span> <span data-ttu-id="eb6b8-547">針對 SMBIOS 2.7 版 +，此值來自于 **擴充的起始位址** 成員。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-547">For SMBIOS version 2.7+ the value comes from the **Extended Starting Address** member.</span></span>

<span data-ttu-id="eb6b8-548">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-548">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="eb6b8-549">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-549">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-550">**狀態**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-550">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-551">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-552">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-553">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-553">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-554">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-554">Current status of the object.</span></span> <span data-ttu-id="eb6b8-555">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-555">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="eb6b8-556">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-556">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="eb6b8-557">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-557">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="eb6b8-558">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-558">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="eb6b8-559">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-559">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="eb6b8-560">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-560">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="eb6b8-561">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="eb6b8-561">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="eb6b8-562">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-562">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="eb6b8-563">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-563">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eb6b8-564">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-564">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6b8-565">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-565">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="eb6b8-566">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-566">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="eb6b8-567">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-567">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="eb6b8-568">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-568">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="eb6b8-569">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-569">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="eb6b8-570">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-570">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="eb6b8-571">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-571">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="eb6b8-572">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-572">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="eb6b8-573">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-573">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-574">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-574">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-575">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-576">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-577">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="eb6b8-577">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-578">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-578">State of the logical device.</span></span> <span data-ttu-id="eb6b8-579">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-579">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="eb6b8-580">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-580">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb6b8-581">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-581">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6b8-582">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-582">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="eb6b8-583">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-583">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="eb6b8-584">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-584">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="eb6b8-585">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-585">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6b8-586">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-586">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-587">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-588">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-589">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-589">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-590">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-590">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="eb6b8-591">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-592">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-592">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-593">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-593">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-594">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-594">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-595">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 18 \| 32-bit Memory error Information \| error Address" ) </span><span class="sxs-lookup"><span data-stu-id="eb6b8-595">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-596">若 **為 True**， **ErrorAddress** 屬性中的位址資訊就是系統層級的位址。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-596">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="eb6b8-597">如果為 **False**，則為實體位址。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-597">If **False**, it is a physical address.</span></span> <span data-ttu-id="eb6b8-598">只有當 **ErrorInfo** 未設定為3時，才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-598">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="eb6b8-599">這個屬性繼承自 [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-599">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6b8-600">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-600">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6b8-601">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-602">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="eb6b8-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6b8-603">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="eb6b8-603">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="eb6b8-604">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-604">Name of the scoping system.</span></span>

<span data-ttu-id="eb6b8-605">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-605">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb6b8-606">備註</span><span class="sxs-lookup"><span data-stu-id="eb6b8-606">Remarks</span></span>

<span data-ttu-id="eb6b8-607">**Win32 \_ MemoryArray** 類別衍生自 [**win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)。</span><span class="sxs-lookup"><span data-stu-id="eb6b8-607">The **Win32\_MemoryArray** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb6b8-608">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb6b8-608">Requirements</span></span>



| <span data-ttu-id="eb6b8-609">需求</span><span class="sxs-lookup"><span data-stu-id="eb6b8-609">Requirement</span></span> | <span data-ttu-id="eb6b8-610">值</span><span class="sxs-lookup"><span data-stu-id="eb6b8-610">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb6b8-611">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb6b8-611">Minimum supported client</span></span><br/> | <span data-ttu-id="eb6b8-612">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb6b8-612">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb6b8-613">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb6b8-613">Minimum supported server</span></span><br/> | <span data-ttu-id="eb6b8-614">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb6b8-614">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb6b8-615">命名空間</span><span class="sxs-lookup"><span data-stu-id="eb6b8-615">Namespace</span></span><br/>                | <span data-ttu-id="eb6b8-616">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eb6b8-616">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb6b8-617">MOF</span><span class="sxs-lookup"><span data-stu-id="eb6b8-617">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb6b8-618"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb6b8-618"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb6b8-619">DLL</span><span class="sxs-lookup"><span data-stu-id="eb6b8-619">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb6b8-620"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb6b8-620"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb6b8-621">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb6b8-621">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb6b8-622">**Win32 \_ SMBIOSMemory**</span><span class="sxs-lookup"><span data-stu-id="eb6b8-622">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="eb6b8-623">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="eb6b8-623">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

