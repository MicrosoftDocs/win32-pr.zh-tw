---
description: CIM \_ FileSpecification 類別代表系統上或關閉的檔案。
ms.assetid: 25d6cc79-1497-4615-9251-8e00524dff1b
ms.tgt_platform: multiple
title: CIM_FileSpecification 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSpecification
- CIM_FileSpecification.CheckID
- CIM_FileSpecification.Caption
- CIM_FileSpecification.Description
- CIM_FileSpecification.CheckMode
- CIM_FileSpecification.TargetOperatingSystem
- CIM_FileSpecification.Version
- CIM_FileSpecification.SoftwareElementID
- CIM_FileSpecification.SoftwareElementState
- CIM_FileSpecification.Name
- CIM_FileSpecification.CheckSum
- CIM_FileSpecification.CRC1
- CIM_FileSpecification.CRC2
- CIM_FileSpecification.CreateTimeStamp
- CIM_FileSpecification.FileSize
- CIM_FileSpecification.MD5Checksum
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 503cf9678d2be7a3afb3f8c205f0d042b4bcaec2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973170"
---
# <a name="cim_filespecification-class"></a><span data-ttu-id="5abb6-103">CIM \_ FileSpecification 類別</span><span class="sxs-lookup"><span data-stu-id="5abb6-103">CIM\_FileSpecification class</span></span>

<span data-ttu-id="5abb6-104">**CIM \_ FileSpecification** 類別代表系統上或關閉的檔案。</span><span class="sxs-lookup"><span data-stu-id="5abb6-104">The **CIM\_FileSpecification** class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="5abb6-105">檔案位於 [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) 關聯所識別的目錄中。</span><span class="sxs-lookup"><span data-stu-id="5abb6-105">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="5abb6-106">[**Invoke**](invoke-method-in-class-cim-filespecification.md)方法會使用此資訊來檢查檔案是否存在。</span><span class="sxs-lookup"><span data-stu-id="5abb6-106">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="5abb6-107">請注意，不會檢查具有 **Null** 值的屬性。</span><span class="sxs-lookup"><span data-stu-id="5abb6-107">Note that properties with a **Null** value are not checked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5abb6-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="5abb6-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5abb6-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5abb6-110">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5abb6-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5abb6-111">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="5abb6-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5abb6-112">語法</span><span class="sxs-lookup"><span data-stu-id="5abb6-112">Syntax</span></span>

``` syntax
[UUID("{41F377B0-DB2A-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_FileSpecification : CIM_Check
{
  string   CheckID;
  string   Caption;
  string   Description;
  boolean  CheckMode;
  uint16   TargetOperatingSystem;
  string   Version;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Name;
  uint32   CheckSum;
  uint32   CRC1;
  uint32   CRC2;
  datetime CreateTimeStamp;
  uint64   FileSize;
  string   MD5Checksum;
};
```

## <a name="members"></a><span data-ttu-id="5abb6-113">成員</span><span class="sxs-lookup"><span data-stu-id="5abb6-113">Members</span></span>

<span data-ttu-id="5abb6-114">**CIM \_ FileSpecification** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5abb6-114">The **CIM\_FileSpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="5abb6-115">方法</span><span class="sxs-lookup"><span data-stu-id="5abb6-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="5abb6-116">屬性</span><span class="sxs-lookup"><span data-stu-id="5abb6-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5abb6-117">方法</span><span class="sxs-lookup"><span data-stu-id="5abb6-117">Methods</span></span>

<span data-ttu-id="5abb6-118">**CIM \_ FileSpecification** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5abb6-118">The **CIM\_FileSpecification** class has these methods.</span></span>



| <span data-ttu-id="5abb6-119">方法</span><span class="sxs-lookup"><span data-stu-id="5abb6-119">Method</span></span>                                                         | <span data-ttu-id="5abb6-120">描述</span><span class="sxs-lookup"><span data-stu-id="5abb6-120">Description</span></span>                                                      |
|:---------------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="5abb6-121">**調用**</span><span class="sxs-lookup"><span data-stu-id="5abb6-121">**Invoke**</span></span>](invoke-method-in-class-cim-filespecification.md) | <span data-ttu-id="5abb6-122">評估特定檢查。</span><span class="sxs-lookup"><span data-stu-id="5abb6-122">Evaluates a particular check.</span></span> <span data-ttu-id="5abb6-123">不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="5abb6-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5abb6-124">屬性</span><span class="sxs-lookup"><span data-stu-id="5abb6-124">Properties</span></span>

<span data-ttu-id="5abb6-125">**CIM \_ FileSpecification** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5abb6-125">The **CIM\_FileSpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5abb6-126">**標題**</span><span class="sxs-lookup"><span data-stu-id="5abb6-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5abb6-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-129">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="5abb6-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-130">主體的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="5abb6-130">A short textual description of the subject.</span></span>

<span data-ttu-id="5abb6-131">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="5abb6-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5abb6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-135">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5abb6-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-136">與其他索引鍵搭配使用來唯一識別檢查的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5abb6-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="5abb6-137">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="5abb6-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-139">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="5abb6-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-141">若 **為 TRUE**，則條件應該存在於環境中。</span><span class="sxs-lookup"><span data-stu-id="5abb6-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="5abb6-142">例如，檔案應該在系統上，因此叫 [**用方法應該**](invoke-method-in-class-cim-check.md) 傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5abb6-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="5abb6-143">如果 **為 FALSE**，則條件不應該存在。</span><span class="sxs-lookup"><span data-stu-id="5abb6-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="5abb6-144">例如，檔案不在系統上，因此 [**Invoke**](invoke-method-in-class-cim-check.md) 方法應該傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5abb6-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="5abb6-145">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-146">**校驗**</span><span class="sxs-lookup"><span data-stu-id="5abb6-146">**CheckSum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-147">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5abb6-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-149">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Software Signature \| 002.4 ") </span><span class="sxs-lookup"><span data-stu-id="5abb6-149">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-150">計算結果為檔案前32個位元組之16位加總的值。</span><span class="sxs-lookup"><span data-stu-id="5abb6-150">Value calculated as the 16-bit sum of the file's first 32 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-151">**CRC1**</span><span class="sxs-lookup"><span data-stu-id="5abb6-151">**CRC1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-152">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5abb6-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-154">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Software Signature \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="5abb6-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-155">使用中間 512 KB 計算的 CRC 值。</span><span class="sxs-lookup"><span data-stu-id="5abb6-155">CRC value calculated using the middle 512 KB.</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-156">**CRC2**</span><span class="sxs-lookup"><span data-stu-id="5abb6-156">**CRC2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="5abb6-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-159">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| Software Signature \| 002.6 ") </span><span class="sxs-lookup"><span data-stu-id="5abb6-159">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-160">檔案中間 512 KB 的 CRC 值（模數3）。</span><span class="sxs-lookup"><span data-stu-id="5abb6-160">CRC value for the middle 512 KB of the file, modulo 3.</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-161">**CreateTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="5abb6-161">**CreateTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-162">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5abb6-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-164">限定詞：已 [**修正**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5abb6-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-165">檔案建立日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5abb6-165">File creation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-166">**說明**</span><span class="sxs-lookup"><span data-stu-id="5abb6-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5abb6-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-169">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5abb6-169">A description of the objects.</span></span>

<span data-ttu-id="5abb6-170">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-170">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-171">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="5abb6-171">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-172">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="5abb6-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-174">限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "kb" ) </span><span class="sxs-lookup"><span data-stu-id="5abb6-174">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-175">檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5abb6-175">Size of the file, in bytes.</span></span>

<span data-ttu-id="5abb6-176">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-176">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-177">**MD5Checksum**</span><span class="sxs-lookup"><span data-stu-id="5abb6-177">**MD5Checksum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5abb6-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-180">限定詞： [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16) </span><span class="sxs-lookup"><span data-stu-id="5abb6-180">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-181">針對任何檔案或物件計算128位總和檢查碼的演算法。</span><span class="sxs-lookup"><span data-stu-id="5abb6-181">Algorithm for computing a 128-bit checksum for any file or object.</span></span> <span data-ttu-id="5abb6-182">兩個不同檔案產生相同 MD5 總和檢查碼的可能性非常小 (大約1個在 2 ^ 64) 中，而檔案的 MD5 總和檢查碼可用來建立可能唯一識別檔案的可靠內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="5abb6-182">The likelihood of two different files producing the same MD5 checksum is very small (about 1 in 2^64), and the MD5 checksum of a file can be used to construct a reliable content identifier that is likely to uniquely identify the file.</span></span> <span data-ttu-id="5abb6-183">反之亦然。</span><span class="sxs-lookup"><span data-stu-id="5abb6-183">The reverse is also true.</span></span> <span data-ttu-id="5abb6-184">如果兩個檔案的 MD5 總和檢查碼相同，則很有可能是檔案相同。</span><span class="sxs-lookup"><span data-stu-id="5abb6-184">If two files have the same MD5 checksum, it is very likely that the files are identical.</span></span> <span data-ttu-id="5abb6-185">針對 MD5 屬性的 MOF 規格用途，MD5 演算法一律會產生32個字元的字串。</span><span class="sxs-lookup"><span data-stu-id="5abb6-185">For purposes of MOF specification of the MD5 property, the MD5 algorithm always generates a 32-character string.</span></span> <span data-ttu-id="5abb6-186">例如，字串 ">abcdefghijklmnopqrstuvwxyz" 會產生 "c3fcd3d76192e4007dfb496cca67e13b" 字串。</span><span class="sxs-lookup"><span data-stu-id="5abb6-186">For example, the string "abcdefghijklmnopqrstuvwxyz" generates the string "c3fcd3d76192e4007dfb496cca67e13b".</span></span> <span data-ttu-id="5abb6-187">如需有關如何執行 MD5 演算法的詳細資訊，請參閱 [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-187">For more information about implementing the MD5 algorithm, see [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-188">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5abb6-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5abb6-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-191">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) (名稱) 、 [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)、 [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024) </span><span class="sxs-lookup"><span data-stu-id="5abb6-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-192">檔案的名稱，或具有目錄前置詞的檔案名。</span><span class="sxs-lookup"><span data-stu-id="5abb6-192">Either the name of the file or the name of the file with a directory prefix.</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-193">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="5abb6-193">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5abb6-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-196">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementID**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="5abb6-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-197">這是此軟體元素的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5abb6-197">This is an identifier for this software element.</span></span>

<span data-ttu-id="5abb6-198">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-198">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="5abb6-199">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="5abb6-199">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-200">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5abb6-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-202">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**SoftwareElementState**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5abb6-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-203">軟體元素的軟體專案狀態。</span><span class="sxs-lookup"><span data-stu-id="5abb6-203">The software element state of a software element.</span></span>

<span data-ttu-id="5abb6-204">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="5abb6-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>可 **部署** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5abb6-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-206">描述成功散發所需的詳細資料，以及在可安裝狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="5abb6-206">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="5abb6-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>可 **安裝** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="5abb6-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-208">描述成功安裝所需的詳細資料，以及在可執行狀態下建立軟體元素所需的詳細資料 (條件和) 動作 (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="5abb6-208">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="5abb6-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**可執行檔** (2) </span><span class="sxs-lookup"><span data-stu-id="5abb6-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-210">描述成功執行所需的詳細資料，以及在執行狀態下建立軟體元素所需的詳細資料 (條件和動作)  (也就是下一個狀態) 。</span><span class="sxs-lookup"><span data-stu-id="5abb6-210">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="5abb6-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**正在** 執行 (3) </span><span class="sxs-lookup"><span data-stu-id="5abb6-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-212">描述監視和操作開始專案所需的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5abb6-212">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5abb6-213">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="5abb6-213">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-214">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="5abb6-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-216">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**TargetOperatingSystem**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| Software Component Information \| 002.5 ") </span><span class="sxs-lookup"><span data-stu-id="5abb6-216">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-217">Software 元素的目標作業系統。</span><span class="sxs-lookup"><span data-stu-id="5abb6-217">Target operating system of the software element.</span></span>

<span data-ttu-id="5abb6-218">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-218">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5abb6-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="5abb6-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5abb6-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="5abb6-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="5abb6-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2) </span><span class="sxs-lookup"><span data-stu-id="5abb6-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-222">Mac OS</span><span class="sxs-lookup"><span data-stu-id="5abb6-222">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="5abb6-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3) </span><span class="sxs-lookup"><span data-stu-id="5abb6-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-224">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="5abb6-224">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="5abb6-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4) </span><span class="sxs-lookup"><span data-stu-id="5abb6-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="5abb6-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5) </span><span class="sxs-lookup"><span data-stu-id="5abb6-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="5abb6-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**數位 Unix** (6) </span><span class="sxs-lookup"><span data-stu-id="5abb6-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="5abb6-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7) </span><span class="sxs-lookup"><span data-stu-id="5abb6-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-229">開啟 VM</span><span class="sxs-lookup"><span data-stu-id="5abb6-229">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="5abb6-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8) </span><span class="sxs-lookup"><span data-stu-id="5abb6-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-231">HP-UX</span><span class="sxs-lookup"><span data-stu-id="5abb6-231">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="5abb6-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9) </span><span class="sxs-lookup"><span data-stu-id="5abb6-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="5abb6-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10) </span><span class="sxs-lookup"><span data-stu-id="5abb6-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="5abb6-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11) </span><span class="sxs-lookup"><span data-stu-id="5abb6-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="5abb6-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12) </span><span class="sxs-lookup"><span data-stu-id="5abb6-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="5abb6-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JAVAVM** (13) </span><span class="sxs-lookup"><span data-stu-id="5abb6-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-237">適用于 JAVA 的 Microsoft 虛擬機器 (VM) </span><span class="sxs-lookup"><span data-stu-id="5abb6-237">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="5abb6-238"><span id="MSDOS"></span><span id="msdos"></span>**Msdos.sys** (14) </span><span class="sxs-lookup"><span data-stu-id="5abb6-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="5abb6-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15) </span><span class="sxs-lookup"><span data-stu-id="5abb6-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-240">Windows 3。x</span><span class="sxs-lookup"><span data-stu-id="5abb6-240">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="5abb6-241"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16) </span><span class="sxs-lookup"><span data-stu-id="5abb6-241"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-242">Windows 95</span><span class="sxs-lookup"><span data-stu-id="5abb6-242">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="5abb6-243"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17) </span><span class="sxs-lookup"><span data-stu-id="5abb6-243"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-244">Windows 98</span><span class="sxs-lookup"><span data-stu-id="5abb6-244">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="5abb6-245"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18) </span><span class="sxs-lookup"><span data-stu-id="5abb6-245"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-246">Windows NT</span><span class="sxs-lookup"><span data-stu-id="5abb6-246">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="5abb6-247"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19) </span><span class="sxs-lookup"><span data-stu-id="5abb6-247"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-248">Windows CE</span><span class="sxs-lookup"><span data-stu-id="5abb6-248">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="5abb6-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20) </span><span class="sxs-lookup"><span data-stu-id="5abb6-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-250">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="5abb6-250">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="5abb6-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21) </span><span class="sxs-lookup"><span data-stu-id="5abb6-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="5abb6-252"><span id="OSF"></span><span id="osf"></span>**憑證** (22) </span><span class="sxs-lookup"><span data-stu-id="5abb6-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="5abb6-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23) </span><span class="sxs-lookup"><span data-stu-id="5abb6-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="5abb6-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>相依 **UNIX** (24) </span><span class="sxs-lookup"><span data-stu-id="5abb6-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="5abb6-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25) </span><span class="sxs-lookup"><span data-stu-id="5abb6-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="5abb6-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26) </span><span class="sxs-lookup"><span data-stu-id="5abb6-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="5abb6-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27) </span><span class="sxs-lookup"><span data-stu-id="5abb6-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="5abb6-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28) </span><span class="sxs-lookup"><span data-stu-id="5abb6-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="5abb6-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29) </span><span class="sxs-lookup"><span data-stu-id="5abb6-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="5abb6-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30) </span><span class="sxs-lookup"><span data-stu-id="5abb6-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="5abb6-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31) </span><span class="sxs-lookup"><span data-stu-id="5abb6-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="5abb6-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32) </span><span class="sxs-lookup"><span data-stu-id="5abb6-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-263">系列</span><span class="sxs-lookup"><span data-stu-id="5abb6-263">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="5abb6-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33) </span><span class="sxs-lookup"><span data-stu-id="5abb6-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-265">串聯 NSK</span><span class="sxs-lookup"><span data-stu-id="5abb6-265">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="5abb6-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34) </span><span class="sxs-lookup"><span data-stu-id="5abb6-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-267">將 NT</span><span class="sxs-lookup"><span data-stu-id="5abb6-267">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="5abb6-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35) </span><span class="sxs-lookup"><span data-stu-id="5abb6-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-269">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="5abb6-269">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="5abb6-270"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36) </span><span class="sxs-lookup"><span data-stu-id="5abb6-270"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="5abb6-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37) </span><span class="sxs-lookup"><span data-stu-id="5abb6-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="5abb6-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38) </span><span class="sxs-lookup"><span data-stu-id="5abb6-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="5abb6-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39) </span><span class="sxs-lookup"><span data-stu-id="5abb6-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="5abb6-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**互動式 UNIX** (40) </span><span class="sxs-lookup"><span data-stu-id="5abb6-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="5abb6-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41) </span><span class="sxs-lookup"><span data-stu-id="5abb6-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-276">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="5abb6-276">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="5abb6-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42) </span><span class="sxs-lookup"><span data-stu-id="5abb6-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="5abb6-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43) </span><span class="sxs-lookup"><span data-stu-id="5abb6-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="5abb6-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44) </span><span class="sxs-lookup"><span data-stu-id="5abb6-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="5abb6-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45) </span><span class="sxs-lookup"><span data-stu-id="5abb6-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-281">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="5abb6-281">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="5abb6-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**符合 Kernel** (46) </span><span class="sxs-lookup"><span data-stu-id="5abb6-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="5abb6-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47) </span><span class="sxs-lookup"><span data-stu-id="5abb6-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="5abb6-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48) </span><span class="sxs-lookup"><span data-stu-id="5abb6-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="5abb6-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49) </span><span class="sxs-lookup"><span data-stu-id="5abb6-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="5abb6-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50) </span><span class="sxs-lookup"><span data-stu-id="5abb6-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="5abb6-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51) </span><span class="sxs-lookup"><span data-stu-id="5abb6-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="5abb6-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52) </span><span class="sxs-lookup"><span data-stu-id="5abb6-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="5abb6-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53) </span><span class="sxs-lookup"><span data-stu-id="5abb6-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="5abb6-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54) </span><span class="sxs-lookup"><span data-stu-id="5abb6-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="5abb6-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55) </span><span class="sxs-lookup"><span data-stu-id="5abb6-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="5abb6-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56) </span><span class="sxs-lookup"><span data-stu-id="5abb6-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="5abb6-293">掌上作業系統</span><span class="sxs-lookup"><span data-stu-id="5abb6-293">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="5abb6-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57) </span><span class="sxs-lookup"><span data-stu-id="5abb6-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="5abb6-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58) </span><span class="sxs-lookup"><span data-stu-id="5abb6-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="5abb6-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**專用** (59) </span><span class="sxs-lookup"><span data-stu-id="5abb6-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="5abb6-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60) </span><span class="sxs-lookup"><span data-stu-id="5abb6-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="5abb6-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61) </span><span class="sxs-lookup"><span data-stu-id="5abb6-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5abb6-299">**版本**</span><span class="sxs-lookup"><span data-stu-id="5abb6-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5abb6-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5abb6-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5abb6-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5abb6-302">限定詞： [**傳播**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ SoftwareElement**](cim-softwareelement.md)。**Version**") ， [**CIM \_ key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 元件 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="5abb6-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="5abb6-303">作業的版本。</span><span class="sxs-lookup"><span data-stu-id="5abb6-303">Version of the operation.</span></span>

<span data-ttu-id="5abb6-304">作業的版本應該採用下列其中一種形式：</span><span class="sxs-lookup"><span data-stu-id="5abb6-304">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="5abb6-305"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="5abb6-305"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="5abb6-306"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="5abb6-306"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="5abb6-307">這個屬性繼承自 [**CIM \_ 檢查**](cim-check.md)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-307">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5abb6-308">備註</span><span class="sxs-lookup"><span data-stu-id="5abb6-308">Remarks</span></span>

<span data-ttu-id="5abb6-309">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="5abb6-309">WMI does not implement this class.</span></span> <span data-ttu-id="5abb6-310">針對衍生自 **CIM \_ FileSpecification** 的類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="5abb6-310">For classes derived from **CIM\_FileSpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5abb6-311">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="5abb6-311">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5abb6-312">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5abb6-312">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5abb6-313">規格需求</span><span class="sxs-lookup"><span data-stu-id="5abb6-313">Requirements</span></span>



| <span data-ttu-id="5abb6-314">需求</span><span class="sxs-lookup"><span data-stu-id="5abb6-314">Requirement</span></span> | <span data-ttu-id="5abb6-315">值</span><span class="sxs-lookup"><span data-stu-id="5abb6-315">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5abb6-316">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5abb6-316">Minimum supported client</span></span><br/> | <span data-ttu-id="5abb6-317">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5abb6-317">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5abb6-318">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5abb6-318">Minimum supported server</span></span><br/> | <span data-ttu-id="5abb6-319">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5abb6-319">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5abb6-320">命名空間</span><span class="sxs-lookup"><span data-stu-id="5abb6-320">Namespace</span></span><br/>                | <span data-ttu-id="5abb6-321">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5abb6-321">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5abb6-322">MOF</span><span class="sxs-lookup"><span data-stu-id="5abb6-322">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5abb6-323"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5abb6-323"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5abb6-324">DLL</span><span class="sxs-lookup"><span data-stu-id="5abb6-324">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5abb6-325"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5abb6-325"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5abb6-326">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5abb6-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5abb6-327">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="5abb6-327">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

