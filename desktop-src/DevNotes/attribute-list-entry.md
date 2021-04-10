---
description: 表示屬性清單中的專案。
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: ATTRIBUTE_LIST_ENTRY 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847016"
---
# <a name="attribute_list_entry-structure"></a><span data-ttu-id="7c1a5-103">屬性 \_ 清單 \_ 專案結構</span><span class="sxs-lookup"><span data-stu-id="7c1a5-103">ATTRIBUTE\_LIST\_ENTRY structure</span></span>

<span data-ttu-id="7c1a5-104">\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]</span><span class="sxs-lookup"><span data-stu-id="7c1a5-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="7c1a5-105">表示屬性清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-105">Represents an entry in the attribute list.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c1a5-106">語法</span><span class="sxs-lookup"><span data-stu-id="7c1a5-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a><span data-ttu-id="7c1a5-107">成員</span><span class="sxs-lookup"><span data-stu-id="7c1a5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c1a5-108">**AttributeTypeCode**</span><span class="sxs-lookup"><span data-stu-id="7c1a5-108">**AttributeTypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="7c1a5-109">屬性型別程式碼。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-109">The attribute type code.</span></span>



| <span data-ttu-id="7c1a5-110">值</span><span class="sxs-lookup"><span data-stu-id="7c1a5-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="7c1a5-111">意義</span><span class="sxs-lookup"><span data-stu-id="7c1a5-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="7c1a5-112"><dt>**$STANDARD \_資訊**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="7c1a5-113">檔案屬性 (例如唯讀和封存) 、時間戳記 (例如檔案建立和上次修改的) ，以及固定連結計數。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="7c1a5-114"><dt>**$ATTRIBUTE \_列出**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="7c1a5-115">組成檔案的屬性清單，以及每個屬性所在之 MFT 檔案記錄的檔案參考。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="7c1a5-116"><dt>**$FILE \_名稱**</dt> <dt>0x30<</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="7c1a5-117">檔案名（以 Unicode 字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="7c1a5-118"><dt>**$OBJECT \_識別碼**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="7c1a5-119">連結追蹤服務所指派的16位元組物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-119">An 16-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="7c1a5-120"><dt>**$VOLUME \_名稱**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="7c1a5-121">磁碟區標籤。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-121">The volume label.</span></span> <span data-ttu-id="7c1a5-122">存在於 $Volume 檔案中。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="7c1a5-123"><dt>**$VOLUME \_資訊**</dt> <dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="7c1a5-124">磁片區資訊。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-124">The volume information.</span></span> <span data-ttu-id="7c1a5-125">存在於 $Volume 檔案中。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="7c1a5-126"><dt>**$DATA**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="7c1a5-127">檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="7c1a5-128"><dt>**$INDEX \_根**</dt> <dt>0x90</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="7c1a5-129">用來執行大型目錄的檔案名配置。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="7c1a5-130"><dt>**$INDEX \_配置**</dt> <dt>0xA0</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="7c1a5-131">用來執行大型目錄的檔案名配置。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="7c1a5-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="7c1a5-133">大型目錄的點陣圖索引。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="7c1a5-134"><dt>**$REPARSE \_點**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="7c1a5-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="7c1a5-135">重新分析點資料。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="7c1a5-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="7c1a5-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="7c1a5-137">此結構的大小，加上選擇性的名稱緩衝區（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-137">The size of this structure, plus the optional name buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7c1a5-138">**AttributeNameLength**</span><span class="sxs-lookup"><span data-stu-id="7c1a5-138">**AttributeNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="7c1a5-139">選用屬性名稱的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-139">The size of the optional attribute name, in characters.</span></span> <span data-ttu-id="7c1a5-140">如果名稱存在，此值為非零值，且結構後面緊接著指定字元數的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-140">If a name exists, this value is nonzero and the structure is followed immediately by a Unicode string of the specified number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="7c1a5-141">**AttributeNameOffset**</span><span class="sxs-lookup"><span data-stu-id="7c1a5-141">**AttributeNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="7c1a5-142">保留的。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-142">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7c1a5-143">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="7c1a5-143">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="7c1a5-144">此屬性 (VCN) 的最低虛擬叢集編號。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-144">The lowest virtual cluster number (VCN) for this attribute.</span></span> <span data-ttu-id="7c1a5-145">除非屬性需要多個檔案記錄區段，而且這個專案是第一個區段的參考，否則這個成員是零。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-145">This member is zero unless the attribute requires multiple file record segments and unless this entry is a reference to a segment other than the first one.</span></span> <span data-ttu-id="7c1a5-146">在此情況下，此值是參考區段所描述的最小 VCN。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-146">In this case, this value is the lowest VCN that is described by the referenced segment.</span></span>

</dd> <dt>

<span data-ttu-id="7c1a5-147">**SegmentReference**</span><span class="sxs-lookup"><span data-stu-id="7c1a5-147">**SegmentReference**</span></span>
</dt> <dd>

<span data-ttu-id="7c1a5-148">主要檔案資料表 (屬性所在的 MFT) 區段。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-148">The master file table (MFT) segment in which the attribute resides.</span></span> <span data-ttu-id="7c1a5-149">請參閱 [**MFT \_ 區段 \_ 參考**](mft-segment-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-149">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c1a5-150">**已保留**</span><span class="sxs-lookup"><span data-stu-id="7c1a5-150">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="7c1a5-151">保留的。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-151">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7c1a5-152">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="7c1a5-152">**AttributeName**</span></span>
</dt> <dd>

<span data-ttu-id="7c1a5-153">選擇性屬性名稱的開頭。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-153">The start of the optional attribute name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c1a5-154">備註</span><span class="sxs-lookup"><span data-stu-id="7c1a5-154">Remarks</span></span>

<span data-ttu-id="7c1a5-155">[屬性] 清單是以雙線對齊的 **屬性 \_ 清單 \_ 專案** 結構的排序清單。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-155">The attributes list is an ordered list of quadword-aligned **ATTRIBUTE\_LIST\_ENTRY** structures.</span></span> <span data-ttu-id="7c1a5-156">這份清單會先依屬性類型代碼排序，然後依屬性名稱 (（如果有) ）。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-156">This list is ordered first by the attribute type code and then by the attribute name (if present).</span></span> <span data-ttu-id="7c1a5-157">兩個屬性都不能有相同的類型代碼、名稱和最低的 VCN。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-157">No two attributes can have the same type code, name, and lowest VCN.</span></span> <span data-ttu-id="7c1a5-158">因此，每個類型的程式碼最多隻能有一個屬性，沒有名稱。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-158">Therefore, there can be at most one attribute for each type code without a name.</span></span>

<span data-ttu-id="7c1a5-159">此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-159">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="7c1a5-160">請注意，此結構沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="7c1a5-160">Note that there is no associated header file for this structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c1a5-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c1a5-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c1a5-162">主檔案資料表</span><span class="sxs-lookup"><span data-stu-id="7c1a5-162">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
