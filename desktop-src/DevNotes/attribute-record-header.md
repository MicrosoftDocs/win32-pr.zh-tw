---
description: 表示屬性記錄。
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: ATTRIBUTE_RECORD_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847015"
---
# <a name="attribute_record_header-structure"></a><span data-ttu-id="7fd92-103">屬性 \_ 記錄 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="7fd92-103">ATTRIBUTE\_RECORD\_HEADER structure</span></span>

<span data-ttu-id="7fd92-104">\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]</span><span class="sxs-lookup"><span data-stu-id="7fd92-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="7fd92-105">表示屬性記錄。</span><span class="sxs-lookup"><span data-stu-id="7fd92-105">Represents an attribute record.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd92-106">語法</span><span class="sxs-lookup"><span data-stu-id="7fd92-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="7fd92-107">成員</span><span class="sxs-lookup"><span data-stu-id="7fd92-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7fd92-108">**TypeCode**</span><span class="sxs-lookup"><span data-stu-id="7fd92-108">**TypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-109">屬性型別程式碼。</span><span class="sxs-lookup"><span data-stu-id="7fd92-109">The attribute type code.</span></span>



| <span data-ttu-id="7fd92-110">值</span><span class="sxs-lookup"><span data-stu-id="7fd92-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="7fd92-111">意義</span><span class="sxs-lookup"><span data-stu-id="7fd92-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="7fd92-112"><dt>**$STANDARD \_資訊**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="7fd92-113">檔案屬性 (例如唯讀和封存) 、時間戳記 (例如檔案建立和上次修改的) ，以及固定連結計數。</span><span class="sxs-lookup"><span data-stu-id="7fd92-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="7fd92-114"><dt>**$ATTRIBUTE \_列出**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="7fd92-115">組成檔案的屬性清單，以及每個屬性所在之 MFT 檔案記錄的檔案參考。</span><span class="sxs-lookup"><span data-stu-id="7fd92-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="7fd92-116"><dt>**$FILE \_名稱**</dt> <dt>0x30<</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="7fd92-117">檔案名（以 Unicode 字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="7fd92-118"><dt>**$OBJECT \_識別碼**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="7fd92-119">連結追蹤服務所指派的64位元組物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fd92-119">An 64-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="7fd92-120"><dt>**$VOLUME \_名稱**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="7fd92-121">磁碟區標籤。</span><span class="sxs-lookup"><span data-stu-id="7fd92-121">The volume label.</span></span> <span data-ttu-id="7fd92-122">存在於 $Volume 檔案中。</span><span class="sxs-lookup"><span data-stu-id="7fd92-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="7fd92-123"><dt>**$VOLUME \_資訊**</dt> <dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="7fd92-124">磁片區資訊。</span><span class="sxs-lookup"><span data-stu-id="7fd92-124">The volume information.</span></span> <span data-ttu-id="7fd92-125">存在於 $Volume 檔案中。</span><span class="sxs-lookup"><span data-stu-id="7fd92-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="7fd92-126"><dt>**$DATA**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="7fd92-127">檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="7fd92-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="7fd92-128"><dt>**$INDEX \_根**</dt> <dt>0x90</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="7fd92-129">用來執行大型目錄的檔案名配置。</span><span class="sxs-lookup"><span data-stu-id="7fd92-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="7fd92-130"><dt>**$INDEX \_配置**</dt> <dt>0xA0</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="7fd92-131">用來執行大型目錄的檔案名配置。</span><span class="sxs-lookup"><span data-stu-id="7fd92-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="7fd92-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="7fd92-133">大型目錄的點陣圖索引。</span><span class="sxs-lookup"><span data-stu-id="7fd92-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="7fd92-134"><dt>**$REPARSE \_點**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="7fd92-135">重新分析點資料。</span><span class="sxs-lookup"><span data-stu-id="7fd92-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="7fd92-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="7fd92-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-137">屬性記錄的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-137">The size of the attribute record, in bytes.</span></span> <span data-ttu-id="7fd92-138">此值會反映記錄變異所需的大小，且一律會四捨五入為最接近的四乘條界限。</span><span class="sxs-lookup"><span data-stu-id="7fd92-138">This value reflects the required size for the record variant and is always rounded to the nearest quadword boundary.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-139">**FormCode**</span><span class="sxs-lookup"><span data-stu-id="7fd92-139">**FormCode**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-140">屬性表單程式碼。</span><span class="sxs-lookup"><span data-stu-id="7fd92-140">The attribute form code.</span></span>



| <span data-ttu-id="7fd92-141">值</span><span class="sxs-lookup"><span data-stu-id="7fd92-141">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="7fd92-142">意義</span><span class="sxs-lookup"><span data-stu-id="7fd92-142">Meaning</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <span data-ttu-id="7fd92-143"><dt>**常駐 \_格式**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-143"><dt>**RESIDENT\_FORM**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="7fd92-144">值會包含在檔案記錄中，並緊接在屬性記錄標頭之後。</span><span class="sxs-lookup"><span data-stu-id="7fd92-144">The value is contained in the file record and immediately follows the attribute record header.</span></span><br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <span data-ttu-id="7fd92-145"><dt>**NONRESIDENT \_表單**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="7fd92-145"><dt>**NONRESIDENT\_FORM**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="7fd92-146">此值會包含在磁片上的其他磁區中。</span><span class="sxs-lookup"><span data-stu-id="7fd92-146">The value is contained in other sectors on the disk.</span></span><br/>                                           |



 

</dd> <dt>

<span data-ttu-id="7fd92-147">**NameLength**</span><span class="sxs-lookup"><span data-stu-id="7fd92-147">**NameLength**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-148">選擇性屬性名稱的大小（以字元為單位），如果沒有屬性名稱，則為0。</span><span class="sxs-lookup"><span data-stu-id="7fd92-148">The size of the optional attribute name, in characters, or 0 if there is no attribute name.</span></span> <span data-ttu-id="7fd92-149">最大屬性名稱長度為255個字元。</span><span class="sxs-lookup"><span data-stu-id="7fd92-149">The maximum attribute name length is 255 characters.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-150">**NameOffset**</span><span class="sxs-lookup"><span data-stu-id="7fd92-150">**NameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-151">屬性名稱從屬性記錄開頭算起的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-151">The offset of the attribute name from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="7fd92-152">如果 **NameLength** 成員為0，則這個成員是未定義的。</span><span class="sxs-lookup"><span data-stu-id="7fd92-152">If the **NameLength** member is 0, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-153">**旗標**</span><span class="sxs-lookup"><span data-stu-id="7fd92-153">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-154">屬性旗標。</span><span class="sxs-lookup"><span data-stu-id="7fd92-154">The attribute flags.</span></span>

<dl> <dt>

<span data-ttu-id="7fd92-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**屬性 \_旗標 \_ 壓縮 \_ 遮罩** (0x00FF) </span><span class="sxs-lookup"><span data-stu-id="7fd92-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE\_FLAG\_COMPRESSION\_MASK** (0x00FF)</span></span>
</dt> <dt>

<span data-ttu-id="7fd92-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**屬性 \_標記 \_ 稀疏** (0x8000) </span><span class="sxs-lookup"><span data-stu-id="7fd92-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE\_FLAG\_SPARSE** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="7fd92-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**屬性 \_旗 \_** 標已加密 (0x4000) </span><span class="sxs-lookup"><span data-stu-id="7fd92-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE\_FLAG\_ENCRYPTED** (0x4000)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="7fd92-158">**執行個體**</span><span class="sxs-lookup"><span data-stu-id="7fd92-158">**Instance**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-159">檔案記錄中這個屬性的唯一實例。</span><span class="sxs-lookup"><span data-stu-id="7fd92-159">The unique instance for this attribute in the file record.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-160">**表單**</span><span class="sxs-lookup"><span data-stu-id="7fd92-160">**Form**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-161">如果 **FormCode** 成員是常駐 \_ 表單，則聯集是 **常駐** 結構。</span><span class="sxs-lookup"><span data-stu-id="7fd92-161">If the **FormCode** member is RESIDENT\_FORM, the union is a **Resident** structure.</span></span> <span data-ttu-id="7fd92-162">如果 **FormCode** 是 NONRESIDENT \_ 格式，則聯集是 **NONRESIDENT** 結構。</span><span class="sxs-lookup"><span data-stu-id="7fd92-162">If **FormCode** is NONRESIDENT\_FORM, the union is a **Nonresident** structure.</span></span>

<dl> <dt>

<span data-ttu-id="7fd92-163">**居民**</span><span class="sxs-lookup"><span data-stu-id="7fd92-163">**Resident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd92-164">**ValueLength**</span><span class="sxs-lookup"><span data-stu-id="7fd92-164">**ValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-165">屬性值的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-165">The size of the attribute value, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-166">**ValueOffset**</span><span class="sxs-lookup"><span data-stu-id="7fd92-166">**ValueOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-167">從屬性記錄開頭算起的值位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-167">The offset to the value from the start of the attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-168">**已保留**</span><span class="sxs-lookup"><span data-stu-id="7fd92-168">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-169">保留的。</span><span class="sxs-lookup"><span data-stu-id="7fd92-169">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7fd92-170">**Nonresident**</span><span class="sxs-lookup"><span data-stu-id="7fd92-170">**Nonresident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd92-171">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="7fd92-171">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-172">此屬性記錄所涵蓋 (VCN) 的最低虛擬叢集編號。</span><span class="sxs-lookup"><span data-stu-id="7fd92-172">The lowest virtual cluster number (VCN) covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-173">**HighestVcn**</span><span class="sxs-lookup"><span data-stu-id="7fd92-173">**HighestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-174">這個屬性記錄所涵蓋的最高 VCN。</span><span class="sxs-lookup"><span data-stu-id="7fd92-174">The highest VCN covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-175">**MappingPairsOffset**</span><span class="sxs-lookup"><span data-stu-id="7fd92-175">**MappingPairsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-176">從屬性記錄開頭開始對應組陣列的位移，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="7fd92-176">The offset to the mapping pairs array from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="7fd92-177">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="7fd92-177">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-178">**已保留**</span><span class="sxs-lookup"><span data-stu-id="7fd92-178">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-179">保留的。</span><span class="sxs-lookup"><span data-stu-id="7fd92-179">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-180">**AllocatedLength**</span><span class="sxs-lookup"><span data-stu-id="7fd92-180">**AllocatedLength**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-181">設定檔案大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-181">The allocated size of the file, in bytes.</span></span> <span data-ttu-id="7fd92-182">此值是叢集大小的偶數倍數。</span><span class="sxs-lookup"><span data-stu-id="7fd92-182">This value is an even multiple of the cluster size.</span></span> <span data-ttu-id="7fd92-183">如果 **LowestVcn** 成員為非零，則這個成員是不正確。</span><span class="sxs-lookup"><span data-stu-id="7fd92-183">This member is not valid if the **LowestVcn** member is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-184">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="7fd92-184">**FileSize**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-185">檔案大小 (可讀取的最大位元組加 1) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-185">The file size (highest byte that can be read plus 1), in bytes.</span></span> <span data-ttu-id="7fd92-186">如果 **LowestVcn** 為非零值，則此成員無效。</span><span class="sxs-lookup"><span data-stu-id="7fd92-186">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-187">**ValidDataLength**</span><span class="sxs-lookup"><span data-stu-id="7fd92-187">**ValidDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-188">有效的資料長度 (最高初始化的位元組加 1) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-188">The valid data length (highest initialized byte plus 1), in bytes.</span></span> <span data-ttu-id="7fd92-189">此值會舍入到最接近的叢集界限。</span><span class="sxs-lookup"><span data-stu-id="7fd92-189">This value is rounded to the nearest cluster boundary.</span></span> <span data-ttu-id="7fd92-190">如果 **LowestVcn** 為非零值，則此成員無效。</span><span class="sxs-lookup"><span data-stu-id="7fd92-190">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="7fd92-191">**TotalAllocated**</span><span class="sxs-lookup"><span data-stu-id="7fd92-191">**TotalAllocated**</span></span>
</dt> <dd>

<span data-ttu-id="7fd92-192">配置給檔案的總計 (配置的叢集) 的總和。</span><span class="sxs-lookup"><span data-stu-id="7fd92-192">The total allocated for the file (the sum of the allocated clusters).</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fd92-193">備註</span><span class="sxs-lookup"><span data-stu-id="7fd92-193">Remarks</span></span>

<span data-ttu-id="7fd92-194">請注意，此結構沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="7fd92-194">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="7fd92-195">此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。</span><span class="sxs-lookup"><span data-stu-id="7fd92-195">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="7fd92-196">屬性記錄一律會在四個四個線界限上對齊。</span><span class="sxs-lookup"><span data-stu-id="7fd92-196">Attribute records are always aligned on a quadword boundary.</span></span>

<span data-ttu-id="7fd92-197">如果屬性為 nonresident，屬性記錄標頭會包含抓取資訊的清單，這些資訊會在屬性的 (LCN) 的 VCN 和邏輯群集編號之間提供對應。</span><span class="sxs-lookup"><span data-stu-id="7fd92-197">If the attribute is nonresident, the attribute record header contains a list of retrieval information that provides a mapping between VCN and logical cluster number (LCN) for the attribute.</span></span> <span data-ttu-id="7fd92-198">如果起始資訊無法放入基底檔案區段中，則可以將它本身儲存在外部檔案記錄區段中。</span><span class="sxs-lookup"><span data-stu-id="7fd92-198">If the retrieval information does not fit in the base file segment, it can be stored in an external file record segment by itself.</span></span> <span data-ttu-id="7fd92-199">如果它仍無法放入一個外部檔案記錄區段中，屬性清單中會有一個布建，可針對需要額外抓取資訊的屬性包含多個專案。</span><span class="sxs-lookup"><span data-stu-id="7fd92-199">If it still does not fit into one external file record segment, there is a provision in the attribute list to contain multiple entries for an attribute that requires additional retrieval information.</span></span>

<span data-ttu-id="7fd92-200">對應配對陣列是以壓縮格式儲存，並假設系統會將資訊解壓縮和快取。</span><span class="sxs-lookup"><span data-stu-id="7fd92-200">The mapping pairs array is stored in a compressed form and assumes that the information is decompressed and cached by the system.</span></span> <span data-ttu-id="7fd92-201">它是由一系列的 NextVcn/CurrentLcn 配對所組成。</span><span class="sxs-lookup"><span data-stu-id="7fd92-201">It consists of a series of NextVcn/CurrentLcn pairs.</span></span> <span data-ttu-id="7fd92-202">例如，如果檔案的單一執行8個叢集從 LCN 128 開始，且檔案從 LowestVcn 0 開始，則對應組陣列只會有一個專案，也就是 NextVcn = 8 和 CurrentLcn = 128。</span><span class="sxs-lookup"><span data-stu-id="7fd92-202">For example, if a file has a single run of 8 clusters starting at LCN 128 and the file starts at LowestVcn 0, then the mapping pairs array has just one entry, which is NextVcn=8 and CurrentLcn=128.</span></span> <span data-ttu-id="7fd92-203">陣列是位元組串流，會在依序處理時儲存工作變數的變更。</span><span class="sxs-lookup"><span data-stu-id="7fd92-203">The array is a byte stream that stores the changes to the working variables when processed sequentially.</span></span> <span data-ttu-id="7fd92-204">位元組資料流程會被視為以零結束的三合一資料流程，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7fd92-204">The byte stream is to be interpreted as a zero-terminated stream of triples, as follows:</span></span>

<span data-ttu-id="7fd92-205">count byte = *v* + (*l* \* 16) </span><span class="sxs-lookup"><span data-stu-id="7fd92-205">count byte = *v* + (*l* \* 16)</span></span>

<span data-ttu-id="7fd92-206">其中 *v* 是變更低順序的 VCN 位元組數目，而 *l* 是變更的低順序的 LCN 位元組數目。</span><span class="sxs-lookup"><span data-stu-id="7fd92-206">where *v* is the number of changed low-order VCN bytes and *l* is the number of changed low-order LCN bytes.</span></span>

<span data-ttu-id="7fd92-207">解壓縮演算法如下所示：</span><span class="sxs-lookup"><span data-stu-id="7fd92-207">The decompression algorithm is as follows:</span></span>

1.  <span data-ttu-id="7fd92-208">將 NextVcn 初始化為 `Attribute->LowestVcn` ，並將 CurrentLcn 設為0。</span><span class="sxs-lookup"><span data-stu-id="7fd92-208">Initialize NextVcn to `Attribute->LowestVcn` and CurrentLcn to 0.</span></span>
2.  <span data-ttu-id="7fd92-209">初始化的位元組資料流程指標 `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` 。</span><span class="sxs-lookup"><span data-stu-id="7fd92-209">Initialize the byte stream pointer to `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset`.</span></span>
3.  <span data-ttu-id="7fd92-210">將 CurrentVcn 設定為 NextVcn。</span><span class="sxs-lookup"><span data-stu-id="7fd92-210">Set CurrentVcn to NextVcn.</span></span>
4.  <span data-ttu-id="7fd92-211">讀取資料流程中的下一個位元組。</span><span class="sxs-lookup"><span data-stu-id="7fd92-211">Read the next byte from the stream.</span></span> <span data-ttu-id="7fd92-212">如果是0，則中斷;否則如先前所述，請將 *v* 和 *l* 解壓縮。</span><span class="sxs-lookup"><span data-stu-id="7fd92-212">If it is 0, then break; else extract *v* and *l* as previously described.</span></span>
5.  <span data-ttu-id="7fd92-213">將下一個 *v* 位元組解讀為帶正負號的數量（低序位位元組優先）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-213">Interpret the next *v* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="7fd92-214">將其簽章解壓縮至64位並將它新增至 NextVcn。</span><span class="sxs-lookup"><span data-stu-id="7fd92-214">Unpack it sign-extended into 64 bits and add it to NextVcn.</span></span>
6.  <span data-ttu-id="7fd92-215">將下一個 *l* 位元組解讀為帶正負號的數量（低序位位元組優先）。</span><span class="sxs-lookup"><span data-stu-id="7fd92-215">Interpret the next *l* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="7fd92-216">將其簽章解壓縮至64位並將它新增至 CurrentLcn。</span><span class="sxs-lookup"><span data-stu-id="7fd92-216">Unpack it sign-extended into 64 bits and add it to CurrentLcn.</span></span> <span data-ttu-id="7fd92-217">如果這產生的 CurrentLcn 為0，則從 CurrentVcn 到 NextVcn-1 的 VCNs 尚未配置。</span><span class="sxs-lookup"><span data-stu-id="7fd92-217">If this produces a CurrentLcn of 0, then the VCNs from CurrentVcn to NextVcn–1 are unallocated.</span></span>
7.  <span data-ttu-id="7fd92-218">從 CurrentVcn、NextVcn 和 CurrentLcn 更新快取的對應資訊。</span><span class="sxs-lookup"><span data-stu-id="7fd92-218">Update the cached mapping information from CurrentVcn, NextVcn, and CurrentLcn.</span></span>
8.  <span data-ttu-id="7fd92-219">移至步驟 3。</span><span class="sxs-lookup"><span data-stu-id="7fd92-219">Go to step 3.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fd92-220">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fd92-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd92-221">主檔案資料表</span><span class="sxs-lookup"><span data-stu-id="7fd92-221">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
