---
description: 代表記憶體相關邏輯裝置的功能和管理。
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: 'CIM_Memory 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513664"
---
# <a name="cim_memory-class-hyper-v-management"></a><span data-ttu-id="ad277-103">CIM_Memory 類別 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="ad277-103">CIM_Memory class (Hyper-V management)</span></span>

<span data-ttu-id="ad277-104">代表記憶體相關邏輯裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="ad277-104">Represents the capabilities and management of memory-related logical devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad277-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad277-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="ad277-106">成員</span><span class="sxs-lookup"><span data-stu-id="ad277-106">Members</span></span>

<span data-ttu-id="ad277-107">**CIM \_ 記憶體** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ad277-107">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="ad277-108">屬性</span><span class="sxs-lookup"><span data-stu-id="ad277-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad277-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ad277-109">Properties</span></span>

<span data-ttu-id="ad277-110">**CIM \_ 記憶體** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-110">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad277-111">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="ad277-111">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-112">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="ad277-112">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ad277-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-114">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. AdditionalErrorData" ) ， **OctetString**， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 005.18 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.13 ") </span><span class="sxs-lookup"><span data-stu-id="ad277-114">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.18", "MIF.DMTF\|Physical Memory Array\|001.13")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-115">包含其他錯誤資訊的八位陣列。</span><span class="sxs-lookup"><span data-stu-id="ad277-115">An array of octets that contains additional error information.</span></span> <span data-ttu-id="ad277-116">例如，ECC 的症狀或使用以 CRC 為基礎的錯誤方法時，會傳回檢查位。</span><span class="sxs-lookup"><span data-stu-id="ad277-116">An example is ECC syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="ad277-117">在後者的情況下，如果可辨識單一位錯誤，而且已知 CRC 演算法，就可以判斷失敗的確切位。</span><span class="sxs-lookup"><span data-stu-id="ad277-117">In the latter case, if a single bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span>

<span data-ttu-id="ad277-118">如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-118">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-119">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="ad277-119">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ad277-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-122">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. CorrectableError" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") </span><span class="sxs-lookup"><span data-stu-id="ad277-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-123">如果最新的錯誤可更正，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="ad277-123">**true** if the most recent error is correctable; otherwise, **false**.</span></span> <span data-ttu-id="ad277-124">如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-124">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="ad277-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-126">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ad277-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-128">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體陣列對應位址 \| 001.4 "，" MIF。DMTF \| 記憶體裝置對應位址 \| 001.5 ") ， **PUnit** (" byte \* 10 ^ 3 ") </span><span class="sxs-lookup"><span data-stu-id="ad277-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-129">由應用程式或作業系統參考的結束位址，以及由記憶體物件的記憶體控制器所對應的結束位址。</span><span class="sxs-lookup"><span data-stu-id="ad277-129">The ending address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="ad277-130">結束位址是以 kb 來指定。</span><span class="sxs-lookup"><span data-stu-id="ad277-130">The ending address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-131">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="ad277-131">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-132">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ad277-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-134">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorAccess" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.10 ") </span><span class="sxs-lookup"><span data-stu-id="ad277-134">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-135">造成最後一個錯誤的記憶體存取作業。</span><span class="sxs-lookup"><span data-stu-id="ad277-135">The memory access operation that caused the last error.</span></span> <span data-ttu-id="ad277-136">如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-136">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ad277-137">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="ad277-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad277-138">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="ad277-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="ad277-139">**閱讀** (3) </span><span class="sxs-lookup"><span data-stu-id="ad277-139">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="ad277-140">**撰寫** (4) </span><span class="sxs-lookup"><span data-stu-id="ad277-140">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="ad277-141">**部分寫入** (5) </span><span class="sxs-lookup"><span data-stu-id="ad277-141">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad277-142">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="ad277-142">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-143">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ad277-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-145">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. StartingAddress" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 005.19 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.14 ") </span><span class="sxs-lookup"><span data-stu-id="ad277-145">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.19", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-146">最後一個記憶體錯誤的位址。</span><span class="sxs-lookup"><span data-stu-id="ad277-146">The address of the last memory error.</span></span> <span data-ttu-id="ad277-147">錯誤的類型是由 **ErrorInfo** 屬性描述。</span><span class="sxs-lookup"><span data-stu-id="ad277-147">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="ad277-148">如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-148">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-149">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="ad277-149">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-150">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="ad277-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ad277-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-152">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorData" ) 、 **OctetString**、 [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "INDEXED" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.12 ") </span><span class="sxs-lookup"><span data-stu-id="ad277-152">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorData"), **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.12")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-153">陣列，其中包含最後一個錯誤記憶體存取期間所捕獲的資料。</span><span class="sxs-lookup"><span data-stu-id="ad277-153">An array that contains data captured during the last erroneous memory access.</span></span> <span data-ttu-id="ad277-154">資料會佔用陣列的前 n 個八位數位，以保存 **ErrorTransferSize** 屬性所指定的位數。</span><span class="sxs-lookup"><span data-stu-id="ad277-154">The data occupies the first n octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span>

<span data-ttu-id="ad277-155">如果 **ErrorTransferSize** 屬性包含 "0" (確定) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-155">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-156">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="ad277-156">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-157">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ad277-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-159">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorDataOrder" ) </span><span class="sxs-lookup"><span data-stu-id="ad277-159">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorDataOrder")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-160">儲存在 **ErrorData** 屬性中的資料排序。</span><span class="sxs-lookup"><span data-stu-id="ad277-160">The ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="ad277-161">「最小的位元組優先」 (值 = 1) 或「最重要的位元組優先」 (2) 可加以指定。</span><span class="sxs-lookup"><span data-stu-id="ad277-161">"Least Significant Byte First" (value=1) or "Most Significant Byte First" (2) can be specified.</span></span> <span data-ttu-id="ad277-162">如果 **ErrorTransferSize** 屬性包含 "0" (確定) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-162">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad277-163">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ad277-163">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="ad277-164">**最不重要的位元組先** (1) </span><span class="sxs-lookup"><span data-stu-id="ad277-164">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="ad277-165">**最重要的位元組先** (2) </span><span class="sxs-lookup"><span data-stu-id="ad277-165">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad277-166">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ad277-166">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-167">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="ad277-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-169">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「CIM \_ MemoryError」 ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體裝置 \| 005.12 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.8 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Memory**.**OtherErrorDescription**") </span><span class="sxs-lookup"><span data-stu-id="ad277-169">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-170">最後發生之錯誤的類型。</span><span class="sxs-lookup"><span data-stu-id="ad277-170">The type of the last error to occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ad277-171">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="ad277-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ad277-172">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="ad277-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ad277-173">**確定** (3) </span><span class="sxs-lookup"><span data-stu-id="ad277-173">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="ad277-174">**讀取** (4) 錯誤</span><span class="sxs-lookup"><span data-stu-id="ad277-174">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="ad277-175">同位 **錯誤** (5) </span><span class="sxs-lookup"><span data-stu-id="ad277-175">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="ad277-176">**單一位錯誤** (6) </span><span class="sxs-lookup"><span data-stu-id="ad277-176">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="ad277-177">**雙位錯誤** (7) </span><span class="sxs-lookup"><span data-stu-id="ad277-177">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="ad277-178">**多位錯誤** (8) </span><span class="sxs-lookup"><span data-stu-id="ad277-178">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="ad277-179">**半位元組錯誤** (9) </span><span class="sxs-lookup"><span data-stu-id="ad277-179">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="ad277-180">總和 **檢查碼錯誤** (10) </span><span class="sxs-lookup"><span data-stu-id="ad277-180">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="ad277-181">**CRC 錯誤** (11) </span><span class="sxs-lookup"><span data-stu-id="ad277-181">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="ad277-182">**未定義** 的 (12) </span><span class="sxs-lookup"><span data-stu-id="ad277-182">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="ad277-183">**未定義** (13) </span><span class="sxs-lookup"><span data-stu-id="ad277-183">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="ad277-184">**未定義** (14) </span><span class="sxs-lookup"><span data-stu-id="ad277-184">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad277-185">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="ad277-185">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ad277-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-187">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-188">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "ErrorMethodology" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.7 ") </span><span class="sxs-lookup"><span data-stu-id="ad277-188">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-189">指出記憶體物件是否使用同位演算法、CRC 演算法、ECC 或其他機制。</span><span class="sxs-lookup"><span data-stu-id="ad277-189">Indicates whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used by the memory object.</span></span> <span data-ttu-id="ad277-190">也可以提供演算法的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ad277-190">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-191">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="ad277-191">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-192">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ad277-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-194">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorResolution" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 記憶體裝置 \| 005.21 "，" MIF。DMTF \| 實體記憶體陣列 \| 001.15 ") ， **PUnit** (" byte ") </span><span class="sxs-lookup"><span data-stu-id="ad277-194">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.21", "MIF.DMTF\|Physical Memory Array\|001.15"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-195">可以解決最後一個錯誤的範圍（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad277-195">The range, in bytes, in which the last error can be resolved.</span></span> <span data-ttu-id="ad277-196">例如，如果錯誤位址解析為位11，例如一般頁面，然後，錯誤可以解析成4K 界限，而這個屬性會設定為 "4000"。</span><span class="sxs-lookup"><span data-stu-id="ad277-196">For example, if error addresses are resolved to bit 11, such as on a typical page basis; then the errors can be resolved to 4K boundaries, and this property is set to "4000".</span></span> <span data-ttu-id="ad277-197">如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-197">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-198">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="ad277-198">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-199">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="ad277-199">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-201">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorTime" ) </span><span class="sxs-lookup"><span data-stu-id="ad277-201">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTime")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-202">上次發生記憶體錯誤的時間。</span><span class="sxs-lookup"><span data-stu-id="ad277-202">The time when the last memory error occurred.</span></span> <span data-ttu-id="ad277-203">如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-203">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-204">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="ad277-204">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-205">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad277-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-207">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_ MemoryError. ErrorTransferSize" ) ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bits" ) ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體記憶體陣列 \| 001.11 ") ， **PUnit** (" bit ") </span><span class="sxs-lookup"><span data-stu-id="ad277-207">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTransferSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.11"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-208">造成最後一個錯誤的資料傳輸大小（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad277-208">The size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="ad277-209">"0" 表示無錯誤。</span><span class="sxs-lookup"><span data-stu-id="ad277-209">"0" indicates no error.</span></span> <span data-ttu-id="ad277-210">如果 **ErrorInfo** 屬性包含 "3" (確定) ，則不會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ad277-210">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-211">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ad277-211">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-212">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ad277-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-214">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「cim \_ MemoryError. OtherErrorDescription」 ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**cim \_ 記憶體**」。**ErrorInfo**」 ) </span><span class="sxs-lookup"><span data-stu-id="ad277-214">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-215">錯誤類型的描述（當 **ErrorType** 屬性設定為 "1" (其他) 時）。</span><span class="sxs-lookup"><span data-stu-id="ad277-215">A description of the error type, when the **ErrorType** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="ad277-216">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="ad277-216">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-217">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="ad277-217">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-219">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「kb」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 記憶體陣列對應位址 \| 001.3 "，" MIF。DMTF \| 記憶體裝置對應位址 \| 001.4 ") ， **PUnit** (" byte \* 10 ^ 3 ") </span><span class="sxs-lookup"><span data-stu-id="ad277-219">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-220">由應用程式或作業系統參考的起始位址，以及由記憶體物件的記憶體控制器所對應的起始位址。</span><span class="sxs-lookup"><span data-stu-id="ad277-220">The starting address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="ad277-221">起始位址的指定單位為 kb。</span><span class="sxs-lookup"><span data-stu-id="ad277-221">The starting address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-222">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="ad277-222">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-223">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ad277-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad277-225">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "CIM \_MemoryError.SystemLevelAddress" ) </span><span class="sxs-lookup"><span data-stu-id="ad277-225">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.SystemLevelAddress")</span></span>
</dt> </dl>

<span data-ttu-id="ad277-226">如果 **ErrorAddress** 屬性中的位址資訊是系統層級的位址，則為 **true** ，如果是實體位址，則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="ad277-226">**true** if the address information in the **ErrorAddress** property is a system-level address, **false** if it is a physical address.</span></span>

</dd> <dt>

<span data-ttu-id="ad277-227">**揮發 性**</span><span class="sxs-lookup"><span data-stu-id="ad277-227">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad277-228">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ad277-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ad277-229">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ad277-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad277-230">如果記憶體是暫時性的，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="ad277-230">**true** if the memory is volatile; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad277-231">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad277-231">Requirements</span></span>



| <span data-ttu-id="ad277-232">需求</span><span class="sxs-lookup"><span data-stu-id="ad277-232">Requirement</span></span> | <span data-ttu-id="ad277-233">值</span><span class="sxs-lookup"><span data-stu-id="ad277-233">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad277-234">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad277-234">Minimum supported client</span></span><br/> | <span data-ttu-id="ad277-235">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ad277-235">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ad277-236">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad277-236">Minimum supported server</span></span><br/> | <span data-ttu-id="ad277-237">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad277-237">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ad277-238">命名空間</span><span class="sxs-lookup"><span data-stu-id="ad277-238">Namespace</span></span><br/>                | <span data-ttu-id="ad277-239">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ad277-239">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ad277-240">MOF</span><span class="sxs-lookup"><span data-stu-id="ad277-240">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad277-241"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ad277-241"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad277-242">DLL</span><span class="sxs-lookup"><span data-stu-id="ad277-242">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad277-243"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad277-243"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ad277-244">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad277-244">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad277-245">**CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="ad277-245">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

