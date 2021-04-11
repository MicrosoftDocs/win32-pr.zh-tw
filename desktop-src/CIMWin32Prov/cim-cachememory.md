---
description: CIM \_ CacheMemory 類別會定義快取記憶體的功能和管理。
ms.assetid: cdf35122-2057-45fa-818b-ce542d8e82b0
ms.tgt_platform: multiple
title: CIM_CacheMemory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory
- CIM_CacheMemory.Caption
- CIM_CacheMemory.Description
- CIM_CacheMemory.InstallDate
- CIM_CacheMemory.Name
- CIM_CacheMemory.Status
- CIM_CacheMemory.Availability
- CIM_CacheMemory.ConfigManagerErrorCode
- CIM_CacheMemory.ConfigManagerUserConfig
- CIM_CacheMemory.CreationClassName
- CIM_CacheMemory.DeviceID
- CIM_CacheMemory.PowerManagementCapabilities
- CIM_CacheMemory.ErrorCleared
- CIM_CacheMemory.ErrorDescription
- CIM_CacheMemory.LastErrorCode
- CIM_CacheMemory.PNPDeviceID
- CIM_CacheMemory.PowerManagementSupported
- CIM_CacheMemory.StatusInfo
- CIM_CacheMemory.SystemCreationClassName
- CIM_CacheMemory.SystemName
- CIM_CacheMemory.Access
- CIM_CacheMemory.BlockSize
- CIM_CacheMemory.NumberOfBlocks
- CIM_CacheMemory.Purpose
- CIM_CacheMemory.ErrorMethodology
- CIM_CacheMemory.AdditionalErrorData
- CIM_CacheMemory.CorrectableError
- CIM_CacheMemory.EndingAddress
- CIM_CacheMemory.ErrorAccess
- CIM_CacheMemory.ErrorAddress
- CIM_CacheMemory.ErrorData
- CIM_CacheMemory.ErrorDataOrder
- CIM_CacheMemory.ErrorInfo
- CIM_CacheMemory.ErrorResolution
- CIM_CacheMemory.ErrorTime
- CIM_CacheMemory.ErrorTransferSize
- CIM_CacheMemory.OtherErrorDescription
- CIM_CacheMemory.StartingAddress
- CIM_CacheMemory.SystemLevelAddress
- CIM_CacheMemory.Associativity
- CIM_CacheMemory.CacheType
- CIM_CacheMemory.FlushTimer
- CIM_CacheMemory.Level
- CIM_CacheMemory.LineSize
- CIM_CacheMemory.ReadPolicy
- CIM_CacheMemory.ReplacementPolicy
- CIM_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b7a7add96c523dae6b683d597ba36953c605d28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847413"
---
# <a name="cim_cachememory-class"></a><span data-ttu-id="c7a9f-103">CIM \_ CacheMemory 類別</span><span class="sxs-lookup"><span data-stu-id="c7a9f-103">CIM\_CacheMemory class</span></span>

<span data-ttu-id="c7a9f-104">**CIM \_ CacheMemory** 類別會定義快取記憶體的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-104">The **CIM\_CacheMemory** class defines the capabilities and management of cache memory.</span></span>

<span data-ttu-id="c7a9f-105">快取記憶體是處理器先搜尋資料的專用或配置的 RAM。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-105">Cache memory is the dedicated or allocated RAM where a processor first searches for data.</span></span> <span data-ttu-id="c7a9f-106">快取記憶體中的資料會快速地傳遞給處理器，而且通常是由其接近處理器 (例如，主要或次要快取) 來描述。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-106">Data in cache memory is quickly delivered to the processor and is usually described by its proximity to the processor (for example, primary or secondary cache).</span></span> <span data-ttu-id="c7a9f-107">磁片磁碟機包含配置用來保存磁片最近讀取或相鄰資料 (以加速抓取) 的磁片磁碟機也會模型化為快取記憶體。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-107">A disk drive that includes RAM allocated for holding the disk's most recently read or adjacent data (to speed up retrieval) is also modeled as cache memory.</span></span>

> [!Note]  
> <span data-ttu-id="c7a9f-108">快取記憶體不是作業系統或應用層級的緩衝區;它是已配置給快取處理器資料的 RAM。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-108">Cache memory is not an operating-system or application-level buffer; it is RAM that has been allocated for caching processor data.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="c7a9f-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c7a9f-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c7a9f-111">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c7a9f-112">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a9f-113">語法</span><span class="sxs-lookup"><span data-stu-id="c7a9f-113">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B65-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CacheMemory : CIM_Memory
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
  uint16   Associativity;
  uint16   CacheType;
  uint32   FlushTimer;
  uint16   Level;
  uint32   LineSize;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="c7a9f-114">成員</span><span class="sxs-lookup"><span data-stu-id="c7a9f-114">Members</span></span>

<span data-ttu-id="c7a9f-115">**CIM \_ CacheMemory** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c7a9f-115">The **CIM\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="c7a9f-116">方法</span><span class="sxs-lookup"><span data-stu-id="c7a9f-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="c7a9f-117">屬性</span><span class="sxs-lookup"><span data-stu-id="c7a9f-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c7a9f-118">方法</span><span class="sxs-lookup"><span data-stu-id="c7a9f-118">Methods</span></span>

<span data-ttu-id="c7a9f-119">**CIM \_ CacheMemory** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-119">The **CIM\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="c7a9f-120">方法</span><span class="sxs-lookup"><span data-stu-id="c7a9f-120">Method</span></span>                                                                 | <span data-ttu-id="c7a9f-121">描述</span><span class="sxs-lookup"><span data-stu-id="c7a9f-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7a9f-122">**重設**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-122">**Reset**</span></span>](reset-method-in-class-cim-cachememory.md)                 | <span data-ttu-id="c7a9f-123">要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="c7a9f-124">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="c7a9f-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cachememory.md) | <span data-ttu-id="c7a9f-126">定義邏輯裝置的預期電源狀態，以及裝置何時應進入該狀態。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="c7a9f-127">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c7a9f-128">屬性</span><span class="sxs-lookup"><span data-stu-id="c7a9f-128">Properties</span></span>

<span data-ttu-id="c7a9f-129">**CIM \_ CacheMemory** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-129">The **CIM\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7a9f-130">**存取**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-131">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-133">描述媒體的讀取/寫入屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="c7a9f-134">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-135">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="c7a9f-136">**可讀取** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="c7a9f-137">可 **寫入** (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="c7a9f-138">支援 (3) 的 **讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="c7a9f-139">**撰寫一次** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-140">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-141">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="c7a9f-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-143">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.18 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.13 ") ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-144">包含其他錯誤資訊的八位陣列。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="c7a9f-145">例如，錯誤檢查和修正 (ECC) 的症狀，或使用以 CRC 為基礎的錯誤方法時，會傳回檢查位。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="c7a9f-146">在後者的情況下，如果可辨識單一位錯誤且已知 CRC 演算法，則可以判斷失敗的確切位。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="c7a9f-147">這種類型的資料 (ECC 的症狀、檢查位或同位資料，或其他廠商提供的資訊) 包含在此欄位中。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="c7a9f-148">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="c7a9f-149">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-150">**關聯性**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-150">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-151">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-152">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-153">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.15 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-154">列舉，定義系統快取的關聯性。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-154">Enumeration that defines the system cache associativity.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-155">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-156">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-156">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="c7a9f-157">**直接對應** 的 (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-157">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="c7a9f-158">**雙向集合關聯** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-158">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="c7a9f-159">**四向設定關聯** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-159">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="c7a9f-160">**完全關聯** (6) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-160">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="c7a9f-161">**8 向設定關聯** (7) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-161">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="c7a9f-162">**16 向設定關聯** (8) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-162">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-163">**可用性**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-163">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-164">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-166">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.5 "，" MIB。IETF \| 主機-RESOURCES-hrDeviceStatus ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-167">裝置的可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-167">Availability and status of the device.</span></span>

<span data-ttu-id="c7a9f-168">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-168">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c7a9f-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>執行中 **/完整電源** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c7a9f-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**警告** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c7a9f-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c7a9f-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c7a9f-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**關閉** (7) 的電源</span><span class="sxs-lookup"><span data-stu-id="c7a9f-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c7a9f-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off 行** (8) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c7a9f-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off** (9) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c7a9f-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (10) **降級**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c7a9f-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**未安裝** (11) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c7a9f-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**安裝錯誤** (12) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c7a9f-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>省 **電-未知的** (13) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-182">裝置已知處於省電模式，但其確切狀態不明。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-182">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c7a9f-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>省 **電-低電源模式** (14) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-184">裝置處於省電狀態，但仍在運作中，而且可能會出現效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-184">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c7a9f-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>省 **電-待命** (15) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-186">裝置無法正常運作，但可快速進入完整電源。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-186">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c7a9f-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span> (16) 的 **電源週期**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c7a9f-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>省 **電-警告** (17) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-189">裝置處於警告狀態，但也處於省電模式。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-189">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c7a9f-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>已 **暫停** (18) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-191">裝置已暫停。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-191">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c7a9f-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**未就緒** (19) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-193">裝置未就緒。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-193">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c7a9f-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**未設定** (20) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-195">裝置未設定。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-195">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c7a9f-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**靜止** (21) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-197">裝置為靜音。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-197">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-198">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-198">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-199">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-201">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageAllocationUnits ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-202">形成儲存範圍之區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-202">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="c7a9f-203">如果變數區塊大小，則應該指定最大區塊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-203">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="c7a9f-204">如果區塊大小未知，或區塊概念無效 (例如，針對匯總延伸區、記憶體或邏輯磁片) ，請輸入 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-204">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="c7a9f-205">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c7a9f-206">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-207">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-207">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-208">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-210">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.9 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-211">指定指令緩存、資料快取或兩者。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-211">Specifies instruction caching, data caching, or both.</span></span> <span data-ttu-id="c7a9f-212">也可以定義「其他」和「未知」。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-212">"Other" and "Unknown" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-213">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-213">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-214">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-214">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="c7a9f-215">**指令** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-215">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="c7a9f-216">**Data** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-216">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="c7a9f-217">**整合** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-217">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-218">**標題**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-221">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-222">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-222">A short textual description of the object.</span></span>

<span data-ttu-id="c7a9f-223">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-225">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-227">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-228">Win32 設定管理員錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-228">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c7a9f-229">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c7a9f-230">**此裝置運作正常。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-230">**This device is working properly.**</span></span> <span data-ttu-id="c7a9f-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-231">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c7a9f-232">**這個裝置並未正確設定。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-232">**This device is not configured correctly.**</span></span> <span data-ttu-id="c7a9f-233">(1)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-233">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c7a9f-234">**Windows 無法載入此裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-234">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c7a9f-235">(2)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c7a9f-236">**這個裝置的驅動程式可能已損毀，或您系統的記憶體或其他資源可能不足。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-236">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c7a9f-237">(3)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-237">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c7a9f-238">**此裝置無法正常運作。其中一個驅動程式或您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-238">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c7a9f-239">(4)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-239">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c7a9f-240">**此裝置的驅動程式需要 Windows 無法管理的資源。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-240">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c7a9f-241">(5)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-241">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c7a9f-242">**此裝置的開機設定與其他裝置發生衝突。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-242">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c7a9f-243">(6)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-243">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c7a9f-244">**無法篩選。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-244">**Cannot filter.**</span></span> <span data-ttu-id="c7a9f-245">(7)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-245">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c7a9f-246">**裝置的驅動程式載入器已遺失。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-246">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c7a9f-247">(8)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-247">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c7a9f-248">**此裝置無法正常運作，因為控制固件未正確報告裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-248">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c7a9f-249">(9)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-249">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c7a9f-250">**這個裝置無法啟動。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-250">**This device cannot start.**</span></span> <span data-ttu-id="c7a9f-251">(10)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-251">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c7a9f-252">**此裝置失敗。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-252">**This device failed.**</span></span> <span data-ttu-id="c7a9f-253">(11)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-253">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c7a9f-254">**這個裝置沒有足夠資源可供使用。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-254">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c7a9f-255"> (12) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-255">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c7a9f-256">**Windows 無法驗證此裝置的資源。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-256">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c7a9f-257">(13)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-257">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c7a9f-258">**在您重新開機電腦之前，此裝置無法正常運作。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-258">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c7a9f-259">(14)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-259">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c7a9f-260">**此裝置無法正常運作，因為可能有重新列舉的問題。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-260">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c7a9f-261">(15)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-261">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c7a9f-262">**Windows 無法識別這個裝置所使用的所有資源。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-262">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c7a9f-263">(16)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-263">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c7a9f-264">**此裝置要求的資源類型不明。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-264">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c7a9f-265">(17)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-265">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c7a9f-266">**重新安裝這個裝置的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-266">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c7a9f-267">(18)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-267">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c7a9f-268">**使用 VxD 載入器失敗。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-268">**Failure using the VxD loader.**</span></span> <span data-ttu-id="c7a9f-269">(19)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-269">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c7a9f-270">**您的登錄可能已損毀。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-270">**Your registry might be corrupted.**</span></span> <span data-ttu-id="c7a9f-271">(20)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-271">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c7a9f-272">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。Windows 正在移除此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-272">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c7a9f-273">(21)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-273">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c7a9f-274">**這個裝置已停用。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-274">**This device is disabled.**</span></span> <span data-ttu-id="c7a9f-275">(22)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-275">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c7a9f-276">**系統失敗：嘗試變更此裝置的驅動程式。如果無法運作，請參閱您的硬體檔。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-276">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c7a9f-277">(23)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-277">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c7a9f-278">**這個裝置可能不存在、運作不正確、或並未安裝所有的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-278">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c7a9f-279">(24)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-279">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c7a9f-280">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-280">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c7a9f-281">(25)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-281">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c7a9f-282">**Windows 仍在設定此裝置。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-282">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c7a9f-283">(26)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-283">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c7a9f-284">**此裝置沒有有效的記錄檔設定。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-284">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c7a9f-285">(27)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-285">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c7a9f-286">**這個裝置的驅動程式尚未安裝。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-286">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c7a9f-287">(28)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-287">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c7a9f-288">**此裝置已停用，因為裝置的固件未提供所需的資源。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-288">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c7a9f-289">(29)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-289">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c7a9f-290">**此裝置正在使用其他裝置正在使用的插斷要求 (IRQ) 資源。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-290">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c7a9f-291">(30)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-291">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c7a9f-292">**這個裝置並未正確執行，因為 Windows 無法載入這個裝置必需的驅動程式。**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-292">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c7a9f-293"> (31) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-293">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-295">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-297">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-298">若 **為 TRUE**，則裝置會使用使用者定義的設定。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c7a9f-299">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-300">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-300">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-301">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-303">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-304">若 **為 TRUE**，表示最新的錯誤是可修正的。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-304">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="c7a9f-305">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-305">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="c7a9f-306">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-306">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-308">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-310">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-311">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c7a9f-312">搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c7a9f-313">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-314">**說明**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-315">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-316">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-317">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-318">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-318">A textual description of the object.</span></span>

<span data-ttu-id="c7a9f-319">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-323">限定詞： [ **CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-324">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-324">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c7a9f-325">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-326">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-326">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-327">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-328">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-329">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體陣列對應位址 \| 001.4 "，" MIF。「DMTF \| 記憶體裝置對應位址 \| 001.5」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-330">由應用程式或作業系統參考，且由記憶體控制器針對這個記憶體物件所對應的結束位址。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-330">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="c7a9f-331">結束位址是以 kb 來指定。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-331">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="c7a9f-332">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-332">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c7a9f-333">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-333">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-334">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-334">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-335">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-337">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.15 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.10 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-338">造成最後一個錯誤的記憶體存取作業。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-338">Memory access operation that caused the last error.</span></span> <span data-ttu-id="c7a9f-339">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-339">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="c7a9f-340">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-340">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="c7a9f-341">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-342">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-342">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-343">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-343">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="c7a9f-344">**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-344">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="c7a9f-345">**撰寫** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-345">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="c7a9f-346">**部分寫入** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-346">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-347">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-347">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-348">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-349">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-350">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.19 "，" MIF。DMTF \| 記憶體裝置 \| 002.20 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.14 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-350">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-351">最後一個記憶體錯誤的位址。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-351">Address of the last memory error.</span></span> <span data-ttu-id="c7a9f-352">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-352">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="c7a9f-353">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-353">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="c7a9f-354">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-354">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c7a9f-355">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-355">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-357">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-359">若 **為 TRUE**，則表示 **LastErrorCode** 屬性中報告的錯誤現在已清除。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-359">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c7a9f-360">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-361">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-361">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-362">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="c7a9f-362">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-364">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體裝置 \| 002.17 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.12 ") ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-364">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-365">最後一個錯誤記憶體存取期間所捕獲的資料。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-365">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="c7a9f-366">資料會佔用陣列的前 *n* 個八位，必須有這個陣列來保存 **ErrorTransferSize** 屬性所指定的位數。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-366">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="c7a9f-367">如果 **ErrorTransferSize** 為0，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-367">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="c7a9f-368">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-368">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-369">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-369">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-370">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-371">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-372">儲存在 **ErrorData** 屬性中的資料順序。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-372">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="c7a9f-373">如果 **ErrorTransferSize** 為0，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-373">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="c7a9f-374">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-374">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-376">不明。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-376">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="c7a9f-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**最不重要的位元組先** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-378">最不重要的位元組優先。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-378">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="c7a9f-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**最重要的位元組先** (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-380">最重要的位元組優先。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-380">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-384">自由格式的字串，提供 **LastErrorCode** 屬性中所記錄之錯誤的相關資訊，以及要執行的更正動作。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-384">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c7a9f-385">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-387">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-389">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Memory**](cim-memory.md).**OtherErrorDescription**") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-390">最近發生的錯誤類型。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="c7a9f-391">CIM 架構中的值12到14未定義，因為 DMI 混合了錯誤類型的語義以及是否可進行更正。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-391">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="c7a9f-392">在 **CorrectableError** 屬性中指出錯誤是否可更正。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-392">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<span data-ttu-id="c7a9f-393">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-395">其他。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-395">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-397">不明。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-397">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c7a9f-398"><span id="OK"></span><span id="ok"></span>**確定** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-399">正常。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-399">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="c7a9f-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**讀取** (4) 錯誤</span><span class="sxs-lookup"><span data-stu-id="c7a9f-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-401">讀取錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-401">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="c7a9f-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>同位 **錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-403">同位錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-403">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="c7a9f-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**單一位錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-405">單一位錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-405">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="c7a9f-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**雙位錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-407">雙位錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-407">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="c7a9f-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**多位錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-409">多位錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-409">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="c7a9f-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**半位元組錯誤** (9) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-411">半個錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-411">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="c7a9f-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>總和 **檢查碼錯誤** (10) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-413">總和檢查碼錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-413">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="c7a9f-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC 錯誤** (11) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-415">CRC 錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-415">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="c7a9f-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**未定義** 的 (12) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-417">未定義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-417">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="c7a9f-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**未定義** (13) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-419">未定義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-419">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="c7a9f-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**未定義** (14) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-421">未定義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-421">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-422">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-422">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-423">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-425">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.7 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-426">指出是否使用同位或 CRC 演算法、ECC 或其他機制。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-426">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="c7a9f-427">也可以提供演算法的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-427">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="c7a9f-428">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-428">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-429">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-429">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-430">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-431">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-432">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.21 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.15 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-433">指定可解決最後一個錯誤的範圍（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-433">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="c7a9f-434">例如，如果錯誤位址解析為位 11 (也就是在一般頁面上) ，則可以將錯誤解析為 4 KB 界限，而這個屬性會設定為4000。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-434">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="c7a9f-435">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-435">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="c7a9f-436">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-436">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c7a9f-437">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-437">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-438">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-438">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-439">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-440">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-441">上次發生記憶體錯誤的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-441">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="c7a9f-442">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-442">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="c7a9f-443">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-443">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="c7a9f-444">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-444">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-445">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-445">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-446">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-446">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-447">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-448">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 002.16 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.11 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-449">造成最後一個錯誤的資料傳輸大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-449">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="c7a9f-450">值為0表示沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-450">A value of 0 indicates no error.</span></span> <span data-ttu-id="c7a9f-451">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性應該設定為0。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-451">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

<span data-ttu-id="c7a9f-452">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-452">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-453">**FlushTimer**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-453">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-454">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-454">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-455">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-456">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.14 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" seconds ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-457">在快取中排清之前，可能會在快取中保留的最大時間量（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-457">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="c7a9f-458">值為0表示快取排清並非由排清計時器所控制。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-458">A value of 0 indicates that a cache flush is not controlled by a flushing timer.</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-460">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-461">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-462">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-463">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-463">Indicates when the object was installed.</span></span> <span data-ttu-id="c7a9f-464">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-464">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c7a9f-465">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-466">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-466">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-467">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-468">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-469">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-469">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c7a9f-470">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-471">**Level**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-471">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-472">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-473">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-474">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.2 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-475">指定這是否為主要、次要或第三快取。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-475">Specifies whether this is the primary, secondary or tertiary cache.</span></span> <span data-ttu-id="c7a9f-476">也可以定義「其他」、「未知」和「不適用」。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-476">"Other", "Unknown", and "Not Applicable" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-478">其他。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-478">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-480">不明。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-480">Unknown.</span></span>

</dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="c7a9f-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**主要** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-482">主要：</span><span class="sxs-lookup"><span data-stu-id="c7a9f-482">Primary.</span></span>

</dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="c7a9f-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**次要** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-484">二 次。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-484">Secondary.</span></span>

</dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="c7a9f-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**第三** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-486">第三。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-486">Tertiary.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c7a9f-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**不適用** (6) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-488">不適用。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-488">Not applicable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-489">**LineSize**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-489">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-490">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-490">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-491">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-492">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.10 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-492">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-493">單一快取 bucket 或行的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-493">Size, in bytes, of a single cache bucket or line.</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-494">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-494">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-495">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-496">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-497">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-497">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-498">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-498">Label by which the object is known.</span></span> <span data-ttu-id="c7a9f-499">子類別化時，可以將這個屬性覆寫為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-499">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c7a9f-500">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-500">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-501">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-501">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-502">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-502">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-503">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-504">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| 主機-RESOURCES-hrStorageSize ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-505">連續區塊的數目，每個區塊會封鎖 **區塊** 屬性中包含的值大小，以形成儲存區。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-505">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="c7a9f-506">您可以將 [ **區塊** ] 屬性的值乘以這個屬性的值，以計算儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-506">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="c7a9f-507">如果 **區塊** 的值是 1 (一個) ，此屬性就是儲存區的總大小。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-507">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="c7a9f-508">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-508">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c7a9f-509">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-509">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-510">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-510">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-511">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-512">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-513">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 記憶體**](cim-memory.md)」。**ErrorInfo**」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-513">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-514">如果 **ErrorType** 屬性設定為 1 ( "Other" ) ，則提供資訊的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-514">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="c7a9f-515">如果未設定為1，則此字串沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-515">If it is not set to 1, then this string has no meaning.</span></span>

<span data-ttu-id="c7a9f-516">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-516">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-517">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-517">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-518">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-520">限定詞： [**架構**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32" ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-520">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-521">指出邏輯裝置的 Win32 隨插即用裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-521">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c7a9f-522">範例： " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c7a9f-522">Example: "\*PNP030b"</span></span>

<span data-ttu-id="c7a9f-523">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-524">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-524">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-525">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c7a9f-525">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-526">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-527">指出邏輯裝置的特定電源相關功能。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-527">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="c7a9f-528">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-530">電源相關的容量未知。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-530">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c7a9f-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-532">此裝置不支援與電源相關的容量。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-532">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c7a9f-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**已停用** (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-534">電源相關容量已停用。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-534">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c7a9f-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-536">電源管理功能目前已啟用，但實際的功能組不明，或資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-536">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c7a9f-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**自動輸入的省電模式** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-538">裝置可以根據使用方式或其他準則來變更其電源狀態。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-538">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c7a9f-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>可 **設定的電源狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-540">支援 **SetPowerState** 方法。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-540">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="c7a9f-541">這個方法可在父 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 類別上找到，並且可以實作為。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-541">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="c7a9f-542">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-542">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c7a9f-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>支援 (6) 的 **電源迴圈**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-544">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) 。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-544">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c7a9f-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**支援的 (7) 上的電源已超時**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-546">您可以叫用 **SetPowerState** 方法，並將 *>powerstate* 參數設定為 5 ( 「電源週期」 ) ，並將 *時間* 參數設定為特定日期和時間（或間隔），以進行電源開啟。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-546">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-547">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-547">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-548">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-548">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-549">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-550">若 **為 TRUE**，則裝置可以受電源管理，也就是進入省電狀態。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-550">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c7a9f-551">如果 **為 FALSE**，則整數值 1 ( 「不支援」 ) 應該是 **PowerManagementCapabilities** 陣列中的唯一專案。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-551">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c7a9f-552">這個屬性不會指出電源管理功能目前是否已啟用，或啟用時支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-552">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c7a9f-553">如需詳細資訊，請參閱 **PowerManagementCapabilities** 陣列。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-553">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c7a9f-554">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-554">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-555">**目的**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-555">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-556">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-557">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-557">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-558">描述媒體及其用途的自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-558">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="c7a9f-559">這個屬性繼承自 [**CIM \_ StorageExtent**](cim-storageextent.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-559">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-560">**ReadPolicy**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-560">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-561">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-562">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-563">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.13 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-563">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-564">快取為了處理讀取要求所採用的原則。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-564">Policy employed by the cache for handling read requests.</span></span> <span data-ttu-id="c7a9f-565">如果讀取原則是個別決定的，也就是每個要求，則應該指定值 6 ( 「每個 i/o 的判斷」 ) 。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-565">If the read policy is determined individually, that is, for each request, then the value 6 ("Determination per I/O") should be specified.</span></span> <span data-ttu-id="c7a9f-566">「其他」和「未知」也是有效的值。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-566">"Other" and "Unknown" are also valid values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-568">其他。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-568">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-570">不明。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-570">Unknown.</span></span>

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="c7a9f-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-572">讀取。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-572">Read.</span></span>

</dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="c7a9f-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**預先讀取** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-574">預先讀取。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-574">Read-ahead.</span></span>

</dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="c7a9f-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**讀取和預先讀取** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Read and Read-Ahead** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-576">讀取和預先讀取。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-576">Read and read-ahead.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="c7a9f-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**每個 i/o 的判斷** (6) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-578">每個 i/o 的判斷。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-578">Determination per I/O.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-579">**ReplacementPolicy**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-579">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-580">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-580">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-581">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-582">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.12 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-583">整數列舉，描述判斷應重複使用哪些快取行或 bucket 的演算法。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-583">Integer enumeration describing the algorithm that determines which cache lines or buckets should be re-used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-585">其他。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-585">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-587">不明。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-587">Unknown.</span></span>

</dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="c7a9f-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**最近使用的最少 (LRU)** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-589">最近使用的 (LRU) 最少。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-589">Least recently used (LRU).</span></span>

</dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="c7a9f-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>先進先 **出 (FIFO)** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**First In First Out (FIFO)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-591">先進先出 (FIFO) 。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-591">First-in, first-out (FIFO).</span></span>

</dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="c7a9f-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**第一次先出 (LIFO)** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-593">後進先出 (LIFO) 。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-593">Last-in, first-out (LIFO).</span></span>

</dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="c7a9f-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**最常使用的 (LFU)** (6) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-595">最常使用的 (LFU。 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-595">Least frequently used (LFU.)</span></span>

</dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="c7a9f-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**最常使用的 (MFU)** (7) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-597">最常使用的 (MFU) 。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-597">Most frequently used (MFU).</span></span>

</dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="c7a9f-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**資料相依多重演算法** (8) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-599">與資料相關的多個演算法。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-599">Data-dependent multiple algorithms.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-600">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-600">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-601">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-601">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-602">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-603">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體陣列對應位址 \| 001.3 "，" MIF。「DMTF \| 記憶體裝置對應位址 \| 001.4」 ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-603">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-604">這個記憶體物件的起始位址，由應用程式或作業系統參考，並且由記憶體控制器所參考。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-604">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="c7a9f-605">起始位址的指定單位為 kb。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-605">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="c7a9f-606">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-606">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="c7a9f-607">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-607">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-608">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-608">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-609">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-609">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-610">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-610">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-611">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-611">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-612">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-612">String that indicates the current status of the object.</span></span> <span data-ttu-id="c7a9f-613">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-613">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c7a9f-614">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-614">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c7a9f-615">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-615">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c7a9f-616">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-616">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c7a9f-617">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-617">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c7a9f-618">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-618">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c7a9f-619">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-619">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c7a9f-620">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="c7a9f-620">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c7a9f-621">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-621">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c7a9f-622">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-622">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c7a9f-623">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-623">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-624">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-624">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c7a9f-625">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-625">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c7a9f-626">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-626">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c7a9f-627">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-627">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c7a9f-628">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-628">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c7a9f-629">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-629">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c7a9f-630">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-630">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c7a9f-631">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-631">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c7a9f-632">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-632">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-633">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-633">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-634">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-634">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-635">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-636">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 操作狀態 \| 003.3 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-637">邏輯裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-637">State of the logical device.</span></span> <span data-ttu-id="c7a9f-638">如果此屬性不適用於邏輯裝置，則應該使用值 5 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-638">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="c7a9f-639">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-640">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-640">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-641">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-641">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c7a9f-642">**已啟用** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-642">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c7a9f-643">**已停用** (4) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-643">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c7a9f-644">**不適用** (5) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-644">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c7a9f-645">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-645">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-646">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-647">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-648">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**CreationClassName**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-648">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-649">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-649">The scoping system's creation class name.</span></span>

<span data-ttu-id="c7a9f-650">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-650">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-651">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-651">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-652">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-652">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-653">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-653">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-654">指出 **ErrorAddress** 屬性中的位址資訊是否為系統層級位址 (**TRUE**) 或 (**FALSE**) 的實體位址。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-654">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="c7a9f-655">如果 **ErrorInfo** 屬性等於 3 ( 「確定」 ) ，則此屬性沒有任何意義。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-655">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="c7a9f-656">這個屬性繼承自 [**CIM \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-656">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-657">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-657">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-658">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-659">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-659">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-660">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 系統**](cim-system.md)」。**名稱**") ， [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c7a9f-660">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-661">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-661">The scoping system's name.</span></span>

<span data-ttu-id="c7a9f-662">這個屬性繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-662">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7a9f-663">**WritePolicy**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-663">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7a9f-664">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-664">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-665">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c7a9f-665">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7a9f-666">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| System Cache \| 003.5 ") </span><span class="sxs-lookup"><span data-stu-id="c7a9f-666">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="c7a9f-667">定義快取是寫回或寫入，還是會針對每個輸入/輸出個別定義此資訊。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-667">Defines whether the cache is write-back or write-through, or whether the information "Varies with Address" or is defined individually for each input/output.</span></span> <span data-ttu-id="c7a9f-668">也可以指定「其他」和「未知」。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-668">"Other" and "Unknown" also can be specified.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c7a9f-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-670">其他。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-670">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c7a9f-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-672">不明。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-672">Unknown.</span></span>

</dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="c7a9f-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**回寫** (3) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write Back** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-674">寫回。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-674">Write back.</span></span>

</dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="c7a9f-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**透過** (4) 撰寫</span><span class="sxs-lookup"><span data-stu-id="c7a9f-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Write Through** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-676">寫入。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-676">Write through.</span></span>

</dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="c7a9f-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**因位址 (5 而異**) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varies with Address** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-678">因位址而異。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-678">Varies with address.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="c7a9f-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**每個 i/o 的判斷** (6) </span><span class="sxs-lookup"><span data-stu-id="c7a9f-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c7a9f-680">每個 i/o 的判斷。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-680">Determination per I/O.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7a9f-681">備註</span><span class="sxs-lookup"><span data-stu-id="c7a9f-681">Remarks</span></span>

<span data-ttu-id="c7a9f-682">**Cim \_ CacheMemory** 類別衍生自 [**cim \_ 記憶體**](cim-memory.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-682">The **CIM\_CacheMemory** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="c7a9f-683">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-683">WMI does not implement this class.</span></span> <span data-ttu-id="c7a9f-684">如需衍生自 **CIM \_ CacheMemory** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-684">For more information about classes derived from **CIM\_CacheMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c7a9f-685">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-685">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c7a9f-686">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c7a9f-686">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7a9f-687">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7a9f-687">Requirements</span></span>



| <span data-ttu-id="c7a9f-688">需求</span><span class="sxs-lookup"><span data-stu-id="c7a9f-688">Requirement</span></span> | <span data-ttu-id="c7a9f-689">值</span><span class="sxs-lookup"><span data-stu-id="c7a9f-689">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a9f-690">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7a9f-690">Minimum supported client</span></span><br/> | <span data-ttu-id="c7a9f-691">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7a9f-691">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c7a9f-692">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7a9f-692">Minimum supported server</span></span><br/> | <span data-ttu-id="c7a9f-693">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7a9f-693">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c7a9f-694">命名空間</span><span class="sxs-lookup"><span data-stu-id="c7a9f-694">Namespace</span></span><br/>                | <span data-ttu-id="c7a9f-695">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c7a9f-695">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c7a9f-696">MOF</span><span class="sxs-lookup"><span data-stu-id="c7a9f-696">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7a9f-697"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7a9f-697"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7a9f-698">DLL</span><span class="sxs-lookup"><span data-stu-id="c7a9f-698">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7a9f-699"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7a9f-699"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7a9f-700">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7a9f-700">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a9f-701">**CIM \_ 記憶體**</span><span class="sxs-lookup"><span data-stu-id="c7a9f-701">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

