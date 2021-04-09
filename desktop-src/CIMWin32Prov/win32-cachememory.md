---
description: Win32 \_ CacheMemory&\# 32;WMI 類別代表電腦系統上的內部和外部快取記憶體。
ms.assetid: 9cfb992d-fbac-4e56-b4f3-61c0c93f5852
ms.tgt_platform: multiple
title: Win32_CacheMemory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CacheMemory
- Win32_CacheMemory.Reset
- Win32_CacheMemory.SetPowerState
- Win32_CacheMemory.Access
- Win32_CacheMemory.AdditionalErrorData
- Win32_CacheMemory.Associativity
- Win32_CacheMemory.Availability
- Win32_CacheMemory.BlockSize
- Win32_CacheMemory.CacheSpeed
- Win32_CacheMemory.CacheType
- Win32_CacheMemory.Caption
- Win32_CacheMemory.ConfigManagerErrorCode
- Win32_CacheMemory.ConfigManagerUserConfig
- Win32_CacheMemory.CorrectableError
- Win32_CacheMemory.CreationClassName
- Win32_CacheMemory.CurrentSRAM
- Win32_CacheMemory.Description
- Win32_CacheMemory.DeviceID
- Win32_CacheMemory.EndingAddress
- Win32_CacheMemory.ErrorAccess
- Win32_CacheMemory.ErrorAddress
- Win32_CacheMemory.ErrorCleared
- Win32_CacheMemory.ErrorCorrectType
- Win32_CacheMemory.ErrorData
- Win32_CacheMemory.ErrorDataOrder
- Win32_CacheMemory.ErrorDescription
- Win32_CacheMemory.ErrorInfo
- Win32_CacheMemory.ErrorMethodology
- Win32_CacheMemory.ErrorResolution
- Win32_CacheMemory.ErrorTime
- Win32_CacheMemory.ErrorTransferSize
- Win32_CacheMemory.FlushTimer
- Win32_CacheMemory.InstallDate
- Win32_CacheMemory.InstalledSize
- Win32_CacheMemory.LastErrorCode
- Win32_CacheMemory.Level
- Win32_CacheMemory.LineSize
- Win32_CacheMemory.Location
- Win32_CacheMemory.MaxCacheSize
- Win32_CacheMemory.Name
- Win32_CacheMemory.NumberOfBlocks
- Win32_CacheMemory.OtherErrorDescription
- Win32_CacheMemory.PNPDeviceID
- Win32_CacheMemory.PowerManagementCapabilities
- Win32_CacheMemory.PowerManagementSupported
- Win32_CacheMemory.Purpose
- Win32_CacheMemory.ReadPolicy
- Win32_CacheMemory.ReplacementPolicy
- Win32_CacheMemory.StartingAddress
- Win32_CacheMemory.Status
- Win32_CacheMemory.StatusInfo
- Win32_CacheMemory.SupportedSRAM
- Win32_CacheMemory.SystemCreationClassName
- Win32_CacheMemory.SystemLevelAddress
- Win32_CacheMemory.SystemName
- Win32_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83a8fefbe1104f24f208d232b8f6bc134efefd83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847492"
---
# <a name="win32_cachememory-class"></a><span data-ttu-id="5f150-103">Win32 \_ CacheMemory 類別</span><span class="sxs-lookup"><span data-stu-id="5f150-103">Win32\_CacheMemory class</span></span>

<span data-ttu-id="5f150-104">**Win32 \_ CacheMemory** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表電腦系統上的內部和外部快取記憶體。</span><span class="sxs-lookup"><span data-stu-id="5f150-104">The **Win32\_CacheMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents internal and external cache memory on a computer system.</span></span>

<span data-ttu-id="5f150-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5f150-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5f150-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5f150-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f150-107">語法</span><span class="sxs-lookup"><span data-stu-id="5f150-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B97-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_CacheMemory : CIM_CacheMemory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Associativity;
  uint16   Availability;
  uint64   BlockSize;
  uint32   CacheSpeed;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  uint16   CurrentSRAM[];
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint16   ErrorCorrectType;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  uint32   FlushTimer;
  datetime InstallDate;
  uint32   InstalledSize;
  uint32   LastErrorCode;
  uint16   Level;
  uint32   LineSize;
  uint16   Location;
  uint32   MaxCacheSize;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  uint16   SupportedSRAM[];
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="5f150-108">成員</span><span class="sxs-lookup"><span data-stu-id="5f150-108">Members</span></span>

<span data-ttu-id="5f150-109">**Win32 \_ CacheMemory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5f150-109">The **Win32\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="5f150-110">方法</span><span class="sxs-lookup"><span data-stu-id="5f150-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5f150-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5f150-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5f150-112">方法</span><span class="sxs-lookup"><span data-stu-id="5f150-112">Methods</span></span>

<span data-ttu-id="5f150-113">**Win32 \_ CacheMemory** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5f150-113">The **Win32\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="5f150-114">方法</span><span class="sxs-lookup"><span data-stu-id="5f150-114">Method</span></span>            | <span data-ttu-id="5f150-115">描述</span><span class="sxs-lookup"><span data-stu-id="5f150-115">Description</span></span>                                                                                                                                                                                                  |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f150-116">**重設**</span><span class="sxs-lookup"><span data-stu-id="5f150-116">**Reset**</span></span>         | <span data-ttu-id="5f150-117">未實作。</span><span class="sxs-lookup"><span data-stu-id="5f150-117">Not implemented.</span></span> <span data-ttu-id="5f150-118">若要執行此方法，請參閱 [**CIM \_ CacheMemory**](cim-cachememory.md)中的 [**Reset**](reset-method-in-class-cim-controller.md)方法以取得檔。</span><span class="sxs-lookup"><span data-stu-id="5f150-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="5f150-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5f150-119">**SetPowerState**</span></span> | <span data-ttu-id="5f150-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="5f150-120">Not implemented.</span></span> <span data-ttu-id="5f150-121">若要執行此方法，請參閱 [**CIM \_ CacheMemory**](cim-cachememory.md)中的 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md)方法，以取得檔。</span><span class="sxs-lookup"><span data-stu-id="5f150-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5f150-122">屬性</span><span class="sxs-lookup"><span data-stu-id="5f150-122">Properties</span></span>

<span data-ttu-id="5f150-123">**Win32 \_ CacheMemory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5f150-123">The **Win32\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f150-124">**存取**</span><span class="sxs-lookup"><span data-stu-id="5f150-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-127">存取的類型。</span><span class="sxs-lookup"><span data-stu-id="5f150-127">Type of access.</span></span>

<span data-ttu-id="5f150-128">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5f150-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="5f150-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="5f150-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-132">可寫入</span><span class="sxs-lookup"><span data-stu-id="5f150-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="5f150-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="5f150-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="5f150-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-135">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="5f150-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-136">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="5f150-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5f150-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-138">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.18 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.13 ") ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="5f150-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5f150-139">包含其他錯誤資訊的八位陣列。</span><span class="sxs-lookup"><span data-stu-id="5f150-139">Array of octets that hold additional error information.</span></span> <span data-ttu-id="5f150-140">例如，ECC 的症狀或使用以 CRC 為基礎的錯誤方法時，會傳回檢查位。</span><span class="sxs-lookup"><span data-stu-id="5f150-140">An example is ECC Syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="5f150-141">在後者的情況下，如果已辨識出單一位錯誤，而且已知 CRC 演算法，則可以判斷失敗的確切位。</span><span class="sxs-lookup"><span data-stu-id="5f150-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="5f150-142">這種類型的資料 (ECC 的症狀、Check Bit、同位資料或其他廠商提供的資訊) 包含在此欄位中。</span><span class="sxs-lookup"><span data-stu-id="5f150-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="5f150-143">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-143">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="5f150-144">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-144">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-145">**關聯性**</span><span class="sxs-lookup"><span data-stu-id="5f150-145">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-146">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-148">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.15 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-149">定義系統快取關聯性的整數列舉。</span><span class="sxs-lookup"><span data-stu-id="5f150-149">An integer enumeration that defines the system cache associativity.</span></span>

<span data-ttu-id="5f150-150">此值來自 SMBIOS 資訊中快取 **資訊** 結構的 **關聯** 性成員。</span><span class="sxs-lookup"><span data-stu-id="5f150-150">This value comes from the **Associativity** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5f150-151">這個屬性繼承自 [**CIM \_ CacheMemory**](cim-cachememory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-151">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-152">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-152">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-153">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-153">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="5f150-154">**直接對應** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-154">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="5f150-155">**雙向集合關聯** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-155">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="5f150-156">**四向設定關聯** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-156">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="5f150-157">**完全關聯** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-157">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="5f150-158">**8 向設定關聯** (7) </span><span class="sxs-lookup"><span data-stu-id="5f150-158">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="5f150-159">**16 向設定關聯** (8) </span><span class="sxs-lookup"><span data-stu-id="5f150-159">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-160">**可用性**</span><span class="sxs-lookup"><span data-stu-id="5f150-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-161">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-163">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="5f150-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-164">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="5f150-164">Availability and status of the device.</span></span>

<span data-ttu-id="5f150-165">此值來自 SMBIOS 資訊中快取 **資訊\*\*\*\*結構的快取設定成員。**</span><span class="sxs-lookup"><span data-stu-id="5f150-165">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5f150-166">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-166">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5f150-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-170">執行中或完整電源</span><span class="sxs-lookup"><span data-stu-id="5f150-170">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5f150-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5f150-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5f150-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5f150-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="5f150-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5f150-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="5f150-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5f150-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="5f150-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5f150-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="5f150-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5f150-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="5f150-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5f150-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="5f150-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5f150-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="5f150-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-181">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="5f150-181">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5f150-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="5f150-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-183">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="5f150-183">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5f150-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="5f150-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-185">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="5f150-185">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5f150-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="5f150-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5f150-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="5f150-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-188">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="5f150-188">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5f150-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="5f150-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-190">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="5f150-190">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5f150-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="5f150-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-192">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="5f150-192">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5f150-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="5f150-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-194">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="5f150-194">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5f150-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="5f150-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-196">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="5f150-196">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-197">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="5f150-197">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-198">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5f150-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-200">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="5f150-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-201">形成此儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f150-201">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="5f150-202">如果未知或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入1。</span><span class="sxs-lookup"><span data-stu-id="5f150-202">If unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="5f150-203">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-203">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="5f150-204">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5f150-204">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-205">**CacheSpeed**</span><span class="sxs-lookup"><span data-stu-id="5f150-205">**CacheSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-206">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5f150-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-208">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 7 \| 快取速度」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「毫微秒」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Cache Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-209">快取的速度。</span><span class="sxs-lookup"><span data-stu-id="5f150-209">Speed of the cache.</span></span>

<span data-ttu-id="5f150-210">此值來自 SMBIOS 資訊中快取 **資訊** 結構的 **快取速度** 成員。</span><span class="sxs-lookup"><span data-stu-id="5f150-210">This value comes from the **Cache Speed** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="5f150-211">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="5f150-211">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-212">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-214">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.9 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-215">快取的類型。</span><span class="sxs-lookup"><span data-stu-id="5f150-215">Type of cache.</span></span>

<span data-ttu-id="5f150-216">此值來自 SMBIOS 資訊中快取 **資訊** 結構的系統快取 **類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="5f150-216">This value comes from the **System Cache Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5f150-217">這個屬性繼承自 [**CIM \_ CacheMemory**](cim-cachememory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-217">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-218">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-218">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-219">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-219">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="5f150-220">**指令** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-220">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="5f150-221">**Data** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-221">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="5f150-222">**整合** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-222">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-223">**標題**</span><span class="sxs-lookup"><span data-stu-id="5f150-223">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-226">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-226">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-227">物件的簡短描述（單行字串）。</span><span class="sxs-lookup"><span data-stu-id="5f150-227">Short description of the object a one-line string.</span></span>

<span data-ttu-id="5f150-228">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-229">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5f150-229">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-230">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5f150-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-232">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-232">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-233">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5f150-233">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5f150-234">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-234">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5f150-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="5f150-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5f150-236"> (0)</span><span class="sxs-lookup"><span data-stu-id="5f150-236">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-237">裝置運作正常。</span><span class="sxs-lookup"><span data-stu-id="5f150-237">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5f150-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**未正確設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="5f150-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5f150-239">(1)</span><span class="sxs-lookup"><span data-stu-id="5f150-239">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-240">裝置未正確設定。</span><span class="sxs-lookup"><span data-stu-id="5f150-240">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5f150-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="5f150-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5f150-242">(2)</span><span class="sxs-lookup"><span data-stu-id="5f150-242">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5f150-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**此裝置的驅動程式可能已損毀，或您的系統可能記憶體不足或其他資源。**</span><span class="sxs-lookup"><span data-stu-id="5f150-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5f150-244">(3)</span><span class="sxs-lookup"><span data-stu-id="5f150-244">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-245">此裝置的驅動程式可能已損毀，或系統的記憶體或其他資源可能不足。</span><span class="sxs-lookup"><span data-stu-id="5f150-245">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5f150-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="5f150-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5f150-247">(4)</span><span class="sxs-lookup"><span data-stu-id="5f150-247">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-248">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="5f150-248">Device is not working properly.</span></span> <span data-ttu-id="5f150-249">其中一個驅動程式或登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="5f150-249">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5f150-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="5f150-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5f150-251">(5)</span><span class="sxs-lookup"><span data-stu-id="5f150-251">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-252">裝置的驅動程式需要 Windows 無法管理的資源。</span><span class="sxs-lookup"><span data-stu-id="5f150-252">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5f150-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="5f150-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5f150-254">(6)</span><span class="sxs-lookup"><span data-stu-id="5f150-254">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-255">裝置的開機設定與其他裝置發生衝突。</span><span class="sxs-lookup"><span data-stu-id="5f150-255">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5f150-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="5f150-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5f150-257">(7)</span><span class="sxs-lookup"><span data-stu-id="5f150-257">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5f150-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="5f150-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5f150-259">(8)</span><span class="sxs-lookup"><span data-stu-id="5f150-259">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-260">遺漏裝置的驅動程式載入器。</span><span class="sxs-lookup"><span data-stu-id="5f150-260">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5f150-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="5f150-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5f150-262">(9)</span><span class="sxs-lookup"><span data-stu-id="5f150-262">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-263">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="5f150-263">Device is not working properly.</span></span> <span data-ttu-id="5f150-264">控制的固件未正確報告裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="5f150-264">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5f150-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**此裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="5f150-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5f150-266">(10)</span><span class="sxs-lookup"><span data-stu-id="5f150-266">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-267">裝置無法啟動。</span><span class="sxs-lookup"><span data-stu-id="5f150-267">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5f150-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="5f150-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5f150-269">(11)</span><span class="sxs-lookup"><span data-stu-id="5f150-269">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-270">裝置失敗。</span><span class="sxs-lookup"><span data-stu-id="5f150-270">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5f150-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**此裝置找不到足夠的可用資源。**</span><span class="sxs-lookup"><span data-stu-id="5f150-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5f150-272"> (12) </span><span class="sxs-lookup"><span data-stu-id="5f150-272">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-273">裝置找不到足夠的可用資源。</span><span class="sxs-lookup"><span data-stu-id="5f150-273">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5f150-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="5f150-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5f150-275">(13)</span><span class="sxs-lookup"><span data-stu-id="5f150-275">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-276">Windows 無法驗證裝置的資源。</span><span class="sxs-lookup"><span data-stu-id="5f150-276">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5f150-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="5f150-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5f150-278">(14)</span><span class="sxs-lookup"><span data-stu-id="5f150-278">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-279">裝置在重新開機電腦之前無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="5f150-279">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5f150-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="5f150-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5f150-281">(15)</span><span class="sxs-lookup"><span data-stu-id="5f150-281">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-282">裝置因可能的重新列舉問題而無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="5f150-282">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5f150-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows 無法識別此裝置使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="5f150-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5f150-284">(16)</span><span class="sxs-lookup"><span data-stu-id="5f150-284">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-285">Windows 無法識別裝置使用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="5f150-285">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5f150-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="5f150-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5f150-287">(17)</span><span class="sxs-lookup"><span data-stu-id="5f150-287">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-288">裝置正在要求未知的資源類型。</span><span class="sxs-lookup"><span data-stu-id="5f150-288">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5f150-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**重新安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="5f150-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5f150-290">(18)</span><span class="sxs-lookup"><span data-stu-id="5f150-290">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-291">必須重新安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5f150-291">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5f150-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="5f150-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5f150-293">(19)</span><span class="sxs-lookup"><span data-stu-id="5f150-293">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5f150-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="5f150-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5f150-295">(20)</span><span class="sxs-lookup"><span data-stu-id="5f150-295">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-296">登錄可能已損毀。</span><span class="sxs-lookup"><span data-stu-id="5f150-296">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5f150-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="5f150-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5f150-298">(21)</span><span class="sxs-lookup"><span data-stu-id="5f150-298">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-299">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="5f150-299">System failure.</span></span> <span data-ttu-id="5f150-300">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="5f150-300">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5f150-301">Windows 正在移除裝置。</span><span class="sxs-lookup"><span data-stu-id="5f150-301">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5f150-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**此裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="5f150-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5f150-303">(22)</span><span class="sxs-lookup"><span data-stu-id="5f150-303">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-304">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="5f150-304">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5f150-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="5f150-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5f150-306">(23)</span><span class="sxs-lookup"><span data-stu-id="5f150-306">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-307">系統失敗。</span><span class="sxs-lookup"><span data-stu-id="5f150-307">System failure.</span></span> <span data-ttu-id="5f150-308">如果變更設備磁碟機是不正確，請參閱硬體檔。</span><span class="sxs-lookup"><span data-stu-id="5f150-308">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5f150-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**此裝置不存在、未正常運作，或未安裝其所有驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="5f150-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5f150-310">(24)</span><span class="sxs-lookup"><span data-stu-id="5f150-310">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-311">裝置不存在、無法正常運作，或未安裝所有的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="5f150-311">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5f150-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="5f150-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5f150-313">(25)</span><span class="sxs-lookup"><span data-stu-id="5f150-313">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-314">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="5f150-314">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5f150-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="5f150-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5f150-316">(26)</span><span class="sxs-lookup"><span data-stu-id="5f150-316">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-317">Windows 仍在設定裝置。</span><span class="sxs-lookup"><span data-stu-id="5f150-317">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5f150-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="5f150-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5f150-319">(27)</span><span class="sxs-lookup"><span data-stu-id="5f150-319">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-320">裝置沒有有效的記錄檔設定。</span><span class="sxs-lookup"><span data-stu-id="5f150-320">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5f150-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**未安裝此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="5f150-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5f150-322">(28)</span><span class="sxs-lookup"><span data-stu-id="5f150-322">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-323">未安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5f150-323">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5f150-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="5f150-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5f150-325">(29)</span><span class="sxs-lookup"><span data-stu-id="5f150-325">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-326">裝置已停用。</span><span class="sxs-lookup"><span data-stu-id="5f150-326">Device is disabled.</span></span> <span data-ttu-id="5f150-327">裝置固件未提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="5f150-327">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5f150-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="5f150-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5f150-329">(30)</span><span class="sxs-lookup"><span data-stu-id="5f150-329">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-330">裝置正在使用其他裝置正在使用的 IRQ 資源。</span><span class="sxs-lookup"><span data-stu-id="5f150-330">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5f150-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**此裝置無法正常運作，因為 Windows 無法載入此裝置所需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="5f150-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5f150-332"> (31) </span><span class="sxs-lookup"><span data-stu-id="5f150-332">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-333">裝置無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="5f150-333">Device is not working properly.</span></span> <span data-ttu-id="5f150-334">Windows 無法載入所需的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5f150-334">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-335">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5f150-335">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-336">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5f150-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-337">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-338">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-338">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-339">若 **為 True**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="5f150-339">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5f150-340">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-341">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="5f150-341">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-342">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5f150-342">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-344">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-345">若 **為 True**，表示最新的錯誤是可修正的。</span><span class="sxs-lookup"><span data-stu-id="5f150-345">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="5f150-346">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-346">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="5f150-347">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-347">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-348">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5f150-348">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-351">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f150-351">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f150-352">第一個具體類別的名稱，這個類別會出現在建立實例時所使用的繼承鏈中。</span><span class="sxs-lookup"><span data-stu-id="5f150-352">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5f150-353">搭配類別的其他索引鍵屬性使用時，屬性可讓這個類別的所有實例和其子類別都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="5f150-353">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5f150-354">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-355">**CurrentSRAM**</span><span class="sxs-lookup"><span data-stu-id="5f150-355">**CurrentSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-356">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5f150-356">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5f150-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-358">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| TYPE 7 \| Current SRAM Type" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-358">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Current SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-359">靜態隨機存取記憶體類型的陣列 (SRAM) 用於快取記憶體。</span><span class="sxs-lookup"><span data-stu-id="5f150-359">Array of types of Static Random Access Memory (SRAM) being used for the cache memory.</span></span>

<span data-ttu-id="5f150-360">此值來自 SMBIOS 資訊中快取 **資訊** 結構的 **目前 SRAM 類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="5f150-360">This value comes from the **Current SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-361">**其他** (0) </span><span class="sxs-lookup"><span data-stu-id="5f150-361">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-362">**未知** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-362">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="5f150-363">**非高** 載 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-363">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="5f150-364">高 **載 (3**) </span><span class="sxs-lookup"><span data-stu-id="5f150-364">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="5f150-365">**管線** 高載 (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-365">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="5f150-366">**同步** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-366">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="5f150-367">**非同步** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-367">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-368">**說明**</span><span class="sxs-lookup"><span data-stu-id="5f150-368">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-369">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-371">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-371">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-372">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5f150-372">Description of the object.</span></span>

<span data-ttu-id="5f150-373">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-374">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5f150-374">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-375">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-376">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-377">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DeviceId" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-377">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-378">**Win32 \_ CacheMemory** 實例所代表之快取的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f150-378">Unique identifier of the cache represented by an instance of **Win32\_CacheMemory**.</span></span>

<span data-ttu-id="5f150-379">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5f150-380">範例：「Cache Memory 1」</span><span class="sxs-lookup"><span data-stu-id="5f150-380">Example: "Cache Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="5f150-381">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="5f150-381">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-382">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5f150-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-384">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體陣列對應位址 \| 001.4 "，" MIF。「DMTF \| 記憶體裝置對應位址 \| 001.5」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-385">這個記憶體物件的結束位址，由應用程式或作業系統所參考並由記憶體控制器所對應。</span><span class="sxs-lookup"><span data-stu-id="5f150-385">Ending address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="5f150-386">結束位址是以 kb 來指定。</span><span class="sxs-lookup"><span data-stu-id="5f150-386">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="5f150-387">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-387">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="5f150-388">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5f150-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-389">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="5f150-389">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-390">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-392">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.15 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.10 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-393">造成最後一個錯誤的記憶體存取作業。</span><span class="sxs-lookup"><span data-stu-id="5f150-393">Memory access operation that caused the last error.</span></span> <span data-ttu-id="5f150-394">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="5f150-394">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="5f150-395">如果 **ErrorInfo** 等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-395">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="5f150-396">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-396">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-397">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-398">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="5f150-399">**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-399">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="5f150-400">**撰寫** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-400">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="5f150-401">**部分寫入** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-401">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-402">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="5f150-402">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-403">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5f150-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-405">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.19 "，" MIF。DMTF \| 記憶體裝置 \| 002.20 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.14 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-406">最後一個記憶體錯誤的位址。</span><span class="sxs-lookup"><span data-stu-id="5f150-406">Address of the last memory error.</span></span> <span data-ttu-id="5f150-407">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="5f150-407">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="5f150-408">如果 **ErrorInfo** 等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-408">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="5f150-409">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-409">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="5f150-410">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5f150-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-411">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5f150-411">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-412">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5f150-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-413">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-414">若 **為 True**，則表示 **LastErrorCode** 中回報的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="5f150-414">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="5f150-415">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-416">**ErrorCorrectType**</span><span class="sxs-lookup"><span data-stu-id="5f150-416">**ErrorCorrectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-417">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-418">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-419">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 7 \| Error 矯正 type" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Error Correction Type")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-420">快取記憶體所使用的錯誤修正方法。</span><span class="sxs-lookup"><span data-stu-id="5f150-420">Error correction method used by the cache memory.</span></span>

<span data-ttu-id="5f150-421">此值來自 SMBIOS 資訊中快取 **資訊** 結構的 **錯誤更正類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="5f150-421">This value comes from the **Error Correction Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="5f150-422">**保留** (0) </span><span class="sxs-lookup"><span data-stu-id="5f150-422">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-423">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-423">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-424">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-424">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5f150-425">**無** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-425">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="5f150-426">同 **位 (4**) </span><span class="sxs-lookup"><span data-stu-id="5f150-426">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="5f150-427">**單一位 ECC** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-427">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="5f150-428">**多位 ECC** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-428">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-429">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="5f150-429">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-430">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="5f150-430">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5f150-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-432">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體裝置 \| 002.17 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.12 ") ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="5f150-432">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5f150-433">最後一個錯誤記憶體存取期間所捕獲的資料陣列。</span><span class="sxs-lookup"><span data-stu-id="5f150-433">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="5f150-434">資料會佔用陣列的前 *n* 個八位數位，以保存 **ErrorTransferSize** 屬性所指定的位數。</span><span class="sxs-lookup"><span data-stu-id="5f150-434">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="5f150-435">如果 **ErrorTransferSize** 為 0 (零) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-435">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="5f150-436">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-436">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-437">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="5f150-437">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-438">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-439">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-440">排序儲存在 **ErrorData** 屬性中的資料。</span><span class="sxs-lookup"><span data-stu-id="5f150-440">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="5f150-441">如果 **ErrorTransferSize** 為 0 (零) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-441">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="5f150-442">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-443">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5f150-443">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="5f150-444">**最不重要的位元組先** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-444">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="5f150-445">**最重要的位元組先** (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-445">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-446">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5f150-446">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-447">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-448">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-449">有關 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及任何可能採取之矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5f150-449">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="5f150-450">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-451">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5f150-451">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-452">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-453">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-454">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**") </span><span class="sxs-lookup"><span data-stu-id="5f150-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-455">最近發生的錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="5f150-455">Type of error that occurred most recently.</span></span> <span data-ttu-id="5f150-456">CIM 架構中的值12-14 是未定義的，因為在 DMI 中，它們會混用錯誤類型的語義以及是否可更正。</span><span class="sxs-lookup"><span data-stu-id="5f150-456">The values 12-14 are undefined in the CIM schema because in DMI they mix the semantics of the type of error and whether it was correctable or not.</span></span> <span data-ttu-id="5f150-457">後者會在屬性 **CorrectableError** 中指出。</span><span class="sxs-lookup"><span data-stu-id="5f150-457">The latter is indicated in the property **CorrectableError**.</span></span>

<span data-ttu-id="5f150-458">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-459">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-460">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-460">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5f150-461">**確定** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-461">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="5f150-462">**讀取** (4) 錯誤</span><span class="sxs-lookup"><span data-stu-id="5f150-462">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="5f150-463">同位 **錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-463">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="5f150-464">**單一位錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-464">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="5f150-465">**雙位錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="5f150-465">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="5f150-466">**多位錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="5f150-466">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="5f150-467">**半位元組錯誤** (9) </span><span class="sxs-lookup"><span data-stu-id="5f150-467">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="5f150-468">總和 **檢查碼錯誤** (10) </span><span class="sxs-lookup"><span data-stu-id="5f150-468">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="5f150-469">**CRC 錯誤** (11) </span><span class="sxs-lookup"><span data-stu-id="5f150-469">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="5f150-470">**未定義** 的 (12) </span><span class="sxs-lookup"><span data-stu-id="5f150-470">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="5f150-471">**未定義** (13) </span><span class="sxs-lookup"><span data-stu-id="5f150-471">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="5f150-472">**未定義** (14) </span><span class="sxs-lookup"><span data-stu-id="5f150-472">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-473">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="5f150-473">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-474">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-475">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-476">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.7 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-476">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-477">有關同位或 CRC 演算法、ECC 或其他使用的機制的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5f150-477">Details on the parity or CRC algorithms, ECC, or other mechanisms used.</span></span>

<span data-ttu-id="5f150-478">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-478">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-479">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="5f150-479">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-480">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5f150-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-481">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-482">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.21 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="5f150-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-483">最後一個錯誤可以解析的範圍（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f150-483">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="5f150-484">例如，如果錯誤位址解析為位 11 (也就是在一般頁面上) ，則可以將錯誤解析為 4 KB 界限，而這個屬性會設定為4000。</span><span class="sxs-lookup"><span data-stu-id="5f150-484">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="5f150-485">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-485">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="5f150-486">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-486">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="5f150-487">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5f150-487">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-488">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="5f150-488">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-489">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5f150-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-490">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-491">上次發生記憶體錯誤的時間。</span><span class="sxs-lookup"><span data-stu-id="5f150-491">Time that the last memory error occurred.</span></span> <span data-ttu-id="5f150-492">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="5f150-492">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="5f150-493">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-493">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="5f150-494">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-494">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-495">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="5f150-495">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-496">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5f150-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-497">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-498">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.16 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="5f150-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-499">造成最後一個錯誤的資料傳輸大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f150-499">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="5f150-500">0 (零) 表示沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f150-500">0 (zero) indicates no error.</span></span> <span data-ttu-id="5f150-501">如果 **ErrorInfo** 屬性等於 3 (確定) ，則此屬性應該設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5f150-501">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="5f150-502">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-502">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-503">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="5f150-503">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-504">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5f150-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-505">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-506">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.14 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" seconds ") </span><span class="sxs-lookup"><span data-stu-id="5f150-506">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-507">在快取中排清之前，可能會在快取中保留的最大時間量（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f150-507">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="5f150-508">值為 0 (零) 表示快取排清不是由排清計時器所控制。</span><span class="sxs-lookup"><span data-stu-id="5f150-508">A value of 0 (zero) indicates that a cache flush is not controlled by a flushing timer.</span></span>

<span data-ttu-id="5f150-509">這個屬性繼承自 [**CIM \_ CacheMemory**](cim-cachememory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-509">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5f150-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-511">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5f150-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-512">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-513">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-513">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-514">物件的安裝日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5f150-514">Date and time the object was installed.</span></span> <span data-ttu-id="5f150-515">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="5f150-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5f150-516">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-517">**InstalledSize**</span><span class="sxs-lookup"><span data-stu-id="5f150-517">**InstalledSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-518">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5f150-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-520">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 7 \| 已安裝大小" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-520">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Installed Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-521">已安裝之快取記憶體的目前大小。</span><span class="sxs-lookup"><span data-stu-id="5f150-521">Current size of the installed cache memory.</span></span>

<span data-ttu-id="5f150-522">此值來自 SMBIOS 資訊中的快取 **資訊** 結構的 **已安裝大小** 成員。</span><span class="sxs-lookup"><span data-stu-id="5f150-522">This value comes from the **Installed Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="5f150-523">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5f150-523">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-524">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5f150-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-525">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-526">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5f150-526">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5f150-527">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-528">**Level**</span><span class="sxs-lookup"><span data-stu-id="5f150-528">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-529">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-529">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-530">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-531">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.2 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-531">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-532">快取的層級。</span><span class="sxs-lookup"><span data-stu-id="5f150-532">Level of the cache.</span></span>

<span data-ttu-id="5f150-533">此值來自 SMBIOS 資訊中快取 **資訊\*\*\*\*結構的快取設定成員。**</span><span class="sxs-lookup"><span data-stu-id="5f150-533">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5f150-534">這個屬性繼承自 [**CIM \_ CacheMemory**](cim-cachememory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-534">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="5f150-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**主要** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="5f150-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**次要** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="5f150-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**第三** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5f150-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-541">**LineSize**</span><span class="sxs-lookup"><span data-stu-id="5f150-541">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-542">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5f150-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-543">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-544">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.10 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="5f150-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-545">單一快取 bucket 或行的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f150-545">Size, in bytes, of a single cache bucket or line.</span></span>

<span data-ttu-id="5f150-546">這個屬性繼承自 [**CIM \_ CacheMemory**](cim-cachememory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-546">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-547">**位置**</span><span class="sxs-lookup"><span data-stu-id="5f150-547">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-548">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-548">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-549">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-550">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 7 \| Location" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-550">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-551">快取記憶體的實體位置。</span><span class="sxs-lookup"><span data-stu-id="5f150-551">Physical location of the cache memory.</span></span>

<span data-ttu-id="5f150-552">此值來自 SMBIOS 資訊中快取 **資訊\*\*\*\*結構的快取設定成員。**</span><span class="sxs-lookup"><span data-stu-id="5f150-552">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="5f150-553">**內部** (0) </span><span class="sxs-lookup"><span data-stu-id="5f150-553">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="External"></span><span id="external"></span><span id="EXTERNAL"></span>

<span data-ttu-id="5f150-554">**外部** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-554">**External** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="5f150-555">**保留** (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-555">**Reserved** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-556">**未知** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-556">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-557">**MaxCacheSize**</span><span class="sxs-lookup"><span data-stu-id="5f150-557">**MaxCacheSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-558">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5f150-558">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-559">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-560">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「SMBIOS \| 類型 7 \| 最大快取大小」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-560">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Maximum Cache Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-561">可安裝到此特定快取記憶體的最大快取大小。</span><span class="sxs-lookup"><span data-stu-id="5f150-561">Maximum cache size installable to this particular cache memory.</span></span>

<span data-ttu-id="5f150-562">此值來自 SMBIOS 資訊中快取 **資訊** 結構的 **最大** 快取大小成員。</span><span class="sxs-lookup"><span data-stu-id="5f150-562">This value comes from the **Maximum Cache Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="5f150-563">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5f150-563">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-564">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-564">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-565">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-565">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-566">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-566">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-567">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="5f150-567">Label by which the object is known.</span></span> <span data-ttu-id="5f150-568">子類別化時，可以將屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="5f150-568">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="5f150-569">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-569">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-570">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="5f150-570">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-571">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5f150-571">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-572">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-573">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="5f150-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-574">連續區塊總數，每個區塊會封鎖 **區塊** 屬性中包含的值大小，這會形成此儲存範圍。</span><span class="sxs-lookup"><span data-stu-id="5f150-574">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="5f150-575">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="5f150-575">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="5f150-576">如果 **區塊** 的值是1，則這個屬性是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="5f150-576">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="5f150-577">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-577">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="5f150-578">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5f150-578">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-579">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5f150-579">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-580">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-581">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-582">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 記憶體**](cim-memory.md)」。**ErrorInfo**」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-582">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-583">如果 **ErrorType** 屬性設定為1，則為提供詳細資訊的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="5f150-583">Free-form string providing more information if the **ErrorType** property is set to 1, Other.</span></span> <span data-ttu-id="5f150-584">否則，此字串沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-584">Otherwise, this string has no meaning.</span></span>

<span data-ttu-id="5f150-585">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-585">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-586">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5f150-586">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-587">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-588">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-589">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-589">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-590">Windows 隨插即用邏輯裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f150-590">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5f150-591">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5f150-592">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5f150-592">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="5f150-593">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5f150-593">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-594">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5f150-594">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5f150-595">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-595">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-596">邏輯裝置的特定電源相關功能陣列。</span><span class="sxs-lookup"><span data-stu-id="5f150-596">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5f150-597">這個屬性繼承自 **CIM \_ LogicalDevice**。</span><span class="sxs-lookup"><span data-stu-id="5f150-597">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5f150-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5f150-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5f150-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5f150-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-602">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="5f150-602">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5f150-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-604">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="5f150-604">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5f150-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-606">支援 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5f150-606">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5f150-607">這個方法可在父 **CIM \_ LogicalDevice** 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="5f150-607">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5f150-608">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="5f150-608">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5f150-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="5f150-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-610">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) 。</span><span class="sxs-lookup"><span data-stu-id="5f150-610">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5f150-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="5f150-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5f150-612">支援計時 Power-On</span><span class="sxs-lookup"><span data-stu-id="5f150-612">Timed Power-On Supported</span></span>

<span data-ttu-id="5f150-613">您可以叫用 [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) 方法，並將 *>powerstate* 參數設定為 5 (電源週期) ，並將 *時間* 設定為特定日期和時間（或間隔）以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="5f150-613">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-614">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5f150-614">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-615">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5f150-615">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-616">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-616">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-617">若 **為 True**，則裝置可以是電源管理 (可進入暫停模式，依此類推) 。</span><span class="sxs-lookup"><span data-stu-id="5f150-617">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="5f150-618">屬性不表示電源管理功能目前已啟用，只有邏輯裝置能夠進行電源管理。</span><span class="sxs-lookup"><span data-stu-id="5f150-618">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="5f150-619">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-619">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-620">**目的**</span><span class="sxs-lookup"><span data-stu-id="5f150-620">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-621">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-621">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-622">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-623">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="5f150-623">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="5f150-624">此值來自 SMBIOS 資訊中快取 **資訊** 結構的 **通訊端指定** 成員。</span><span class="sxs-lookup"><span data-stu-id="5f150-624">This value comes from the **Socket Designation** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5f150-625">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-625">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-626">**ReadPolicy**</span><span class="sxs-lookup"><span data-stu-id="5f150-626">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-627">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-627">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-628">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-629">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.13 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-629">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-630">快取應用來處理讀取要求的原則。</span><span class="sxs-lookup"><span data-stu-id="5f150-630">Policy that shall be employed by the cache for handling read requests.</span></span>

<span data-ttu-id="5f150-631">這個屬性繼承自 [**CIM \_ CacheMemory**](cim-cachememory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-631">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-632">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-632">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-633">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-633">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="5f150-634">**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-634">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="5f150-635">**預先讀取** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-635">**Read-Ahead** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="5f150-636">**讀取和預先讀取** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-636">**Read and Read-Ahead** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="5f150-637">**每個 i/o 的判斷** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-637">**Determination Per I/O** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-638">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="5f150-638">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-639">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-639">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-640">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-640">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-641">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.12 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-641">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-642">演算法來決定應該重複使用的快取行或值區。</span><span class="sxs-lookup"><span data-stu-id="5f150-642">Algorithm to determine which cache lines or buckets should be reused.</span></span>

<span data-ttu-id="5f150-643">這個屬性繼承自 [**CIM \_ CacheMemory**](cim-cachememory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-643">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-644">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-644">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-645">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-645">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="5f150-646">**最近使用的最少 (LRU)** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-646">**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="5f150-647">先進先 **出 (FIFO)** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-647">**First In First Out (FIFO)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="5f150-648">**第一次先出 (LIFO)** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-648">**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="5f150-649">**最常使用的 (LFU)** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-649">**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="5f150-650">**最常使用的 (MFU)** (7) </span><span class="sxs-lookup"><span data-stu-id="5f150-650">**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="5f150-651">**資料相依多重演算法** (8) </span><span class="sxs-lookup"><span data-stu-id="5f150-651">**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-652">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="5f150-652">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-653">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5f150-653">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-654">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-654">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-655">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體陣列對應位址 \| 001.3 "，" MIF。「DMTF \| 記憶體裝置對應位址 \| 001.4」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-655">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-656">這個記憶體物件的起始位址，由應用程式或作業系統參考，並且由記憶體控制器所參考。</span><span class="sxs-lookup"><span data-stu-id="5f150-656">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="5f150-657">起始位址的指定單位為 kb。</span><span class="sxs-lookup"><span data-stu-id="5f150-657">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="5f150-658">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-658">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="5f150-659">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5f150-659">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-660">**狀態**</span><span class="sxs-lookup"><span data-stu-id="5f150-660">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-661">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-662">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-663">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-663">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-664">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5f150-664">Current status of the object.</span></span> <span data-ttu-id="5f150-665">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="5f150-665">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5f150-666">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="5f150-666">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5f150-667">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="5f150-667">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5f150-668">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="5f150-668">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5f150-669">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="5f150-669">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5f150-670">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-670">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5f150-671">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="5f150-671">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5f150-672">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="5f150-672">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5f150-673">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-673">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5f150-674">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-674">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-675">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-675">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5f150-676">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-676">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5f150-677">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-677">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5f150-678">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-678">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5f150-679">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-679">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5f150-680">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-680">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5f150-681">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-681">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5f150-682">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-682">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5f150-683">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="5f150-683">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-684">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5f150-684">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-685">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-685">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-686">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-687">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-687">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-688">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="5f150-688">State of the logical device.</span></span> <span data-ttu-id="5f150-689">如果此屬性不適用於邏輯裝置，則應該使用值 5 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="5f150-689">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5f150-690">此值來自 SMBIOS 資訊中快取 **資訊\*\*\*\*結構的快取設定成員。**</span><span class="sxs-lookup"><span data-stu-id="5f150-690">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5f150-691">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-691">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-692">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-692">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-693">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-693">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5f150-694">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-694">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5f150-695">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-695">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5f150-696">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-696">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-697">**SupportedSRAM**</span><span class="sxs-lookup"><span data-stu-id="5f150-697">**SupportedSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-698">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="5f150-698">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5f150-699">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-700">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| type 7 \| 支援的 SRAM 類型" ) </span><span class="sxs-lookup"><span data-stu-id="5f150-700">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Supported SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-701">支援的靜態隨機存取記憶體類型陣列 (SRAM 可用於快取記憶體的) 。</span><span class="sxs-lookup"><span data-stu-id="5f150-701">Array of supported types of Static Random Access Memory (SRAM) that can be used for the cache memory.</span></span>

<span data-ttu-id="5f150-702">此值來自 SMBIOS 資訊中快取 **資訊** 結構 **支援的 SRAM 類型** 成員。</span><span class="sxs-lookup"><span data-stu-id="5f150-702">This value comes from the **Supported SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-703">**其他** (0) </span><span class="sxs-lookup"><span data-stu-id="5f150-703">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-704">**未知** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-704">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="5f150-705">**非高** 載 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-705">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="5f150-706">高 **載 (3**) </span><span class="sxs-lookup"><span data-stu-id="5f150-706">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="5f150-707">**管線** 高載 (4) </span><span class="sxs-lookup"><span data-stu-id="5f150-707">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="5f150-708">**同步** (5) </span><span class="sxs-lookup"><span data-stu-id="5f150-708">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="5f150-709">**非同步** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-709">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5f150-710">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5f150-710">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-711">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-711">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-712">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-713">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f150-713">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f150-714">範圍電腦之 **CreationClassName** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="5f150-714">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="5f150-715">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-715">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-716">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="5f150-716">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-717">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5f150-717">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-718">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-718">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f150-719">若 **為 True**，則屬性 **ErrorAddress** 中的位址資訊為系統層級的位址。</span><span class="sxs-lookup"><span data-stu-id="5f150-719">If **True**, the address information in the property **ErrorAddress** is a system-level address.</span></span> <span data-ttu-id="5f150-720">如果為 **False**，則為實體位址。</span><span class="sxs-lookup"><span data-stu-id="5f150-720">If **False**, it is a physical address.</span></span> <span data-ttu-id="5f150-721">如果 **ErrorInfo** 屬性等於3，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="5f150-721">If the **ErrorInfo** property is equal to 3, then this property has no meaning.</span></span>

<span data-ttu-id="5f150-722">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-722">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-723">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5f150-723">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-724">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5f150-724">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-725">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-726">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5f150-726">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5f150-727">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f150-727">Name of the scoping system.</span></span>

<span data-ttu-id="5f150-728">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-728">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5f150-729">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="5f150-729">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f150-730">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5f150-730">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5f150-731">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5f150-731">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f150-732">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.5 ") </span><span class="sxs-lookup"><span data-stu-id="5f150-732">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="5f150-733">寫入原則定義。</span><span class="sxs-lookup"><span data-stu-id="5f150-733">Write policy definition.</span></span>

<span data-ttu-id="5f150-734">此值來自 SMBIOS 資訊中快取 **資訊\*\*\*\*結構的快取設定成員。**</span><span class="sxs-lookup"><span data-stu-id="5f150-734">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="5f150-735">這個屬性繼承自 [**CIM \_ CacheMemory**](cim-cachememory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-735">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5f150-736">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5f150-736">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5f150-737">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="5f150-737">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="5f150-738">**回寫** (3) </span><span class="sxs-lookup"><span data-stu-id="5f150-738">**Write Back** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="5f150-739">**透過** (4) 撰寫</span><span class="sxs-lookup"><span data-stu-id="5f150-739">**Write Through** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="5f150-740">**因位址 (5 而異**) </span><span class="sxs-lookup"><span data-stu-id="5f150-740">**Varies with Address** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="5f150-741">**每個 i/o 的判斷** (6) </span><span class="sxs-lookup"><span data-stu-id="5f150-741">**Determination Per I/O** (6)</span></span>


<span data-ttu-id="5f150-742"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5f150-742"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5f150-743">備註</span><span class="sxs-lookup"><span data-stu-id="5f150-743">Remarks</span></span>

<span data-ttu-id="5f150-744">**Win32 \_ CacheMemory** 類別衍生自 [**CIM \_ CacheMemory**](cim-cachememory.md)。</span><span class="sxs-lookup"><span data-stu-id="5f150-744">The **Win32\_CacheMemory** class is derived from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f150-745">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f150-745">Requirements</span></span>



| <span data-ttu-id="5f150-746">需求</span><span class="sxs-lookup"><span data-stu-id="5f150-746">Requirement</span></span> | <span data-ttu-id="5f150-747">值</span><span class="sxs-lookup"><span data-stu-id="5f150-747">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f150-748">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f150-748">Minimum supported client</span></span><br/> | <span data-ttu-id="5f150-749">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f150-749">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f150-750">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f150-750">Minimum supported server</span></span><br/> | <span data-ttu-id="5f150-751">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f150-751">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f150-752">命名空間</span><span class="sxs-lookup"><span data-stu-id="5f150-752">Namespace</span></span><br/>                | <span data-ttu-id="5f150-753">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5f150-753">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f150-754">MOF</span><span class="sxs-lookup"><span data-stu-id="5f150-754">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f150-755"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f150-755"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f150-756">DLL</span><span class="sxs-lookup"><span data-stu-id="5f150-756">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f150-757"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f150-757"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f150-758">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f150-758">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f150-759">**CIM \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="5f150-759">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dt>

[<span data-ttu-id="5f150-760">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="5f150-760">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

