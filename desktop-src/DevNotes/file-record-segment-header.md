---
description: 表示檔案記錄區段。 這是主要檔案資料表中的每個檔案記錄區段的標頭 (MFT) 。
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: FILE_RECORD_SEGMENT_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187610"
---
# <a name="file_record_segment_header-structure"></a><span data-ttu-id="e1356-104">檔案 \_ 記錄 \_ 區段 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="e1356-104">FILE\_RECORD\_SEGMENT\_HEADER structure</span></span>

<span data-ttu-id="e1356-105">\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]</span><span class="sxs-lookup"><span data-stu-id="e1356-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="e1356-106">表示檔案記錄區段。</span><span class="sxs-lookup"><span data-stu-id="e1356-106">Represents the file record segment.</span></span> <span data-ttu-id="e1356-107">這是主要檔案資料表中的每個檔案記錄區段的標頭 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="e1356-107">This is the header for each file record segment in the master file table (MFT).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1356-108">語法</span><span class="sxs-lookup"><span data-stu-id="e1356-108">Syntax</span></span>


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a><span data-ttu-id="e1356-109">成員</span><span class="sxs-lookup"><span data-stu-id="e1356-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e1356-110">**MultiSectorHeader**</span><span class="sxs-lookup"><span data-stu-id="e1356-110">**MultiSectorHeader**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-111">快取管理員所定義的 multisector 標頭。</span><span class="sxs-lookup"><span data-stu-id="e1356-111">The multisector header defined by the cache manager.</span></span> <span data-ttu-id="e1356-112">[**多 \_ 磁區 \_ 標頭**](multi-sector-header.md)結構一律會包含「檔案」簽章，以及更新順序陣列的位置和大小描述。</span><span class="sxs-lookup"><span data-stu-id="e1356-112">The [**MULTI\_SECTOR\_HEADER**](multi-sector-header.md) structure always contains the signature "FILE" and a description of the location and size of the update sequence array.</span></span>

</dd> <dt>

<span data-ttu-id="e1356-113">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="e1356-113">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="e1356-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e1356-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="e1356-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-116">序號。</span><span class="sxs-lookup"><span data-stu-id="e1356-116">The sequence number.</span></span> <span data-ttu-id="e1356-117">每次釋放檔案記錄區段時，此值就會遞增;如果未使用區段，則為0。</span><span class="sxs-lookup"><span data-stu-id="e1356-117">This value is incremented each time that a file record segment is freed; it is 0 if the segment is not used.</span></span> <span data-ttu-id="e1356-118">檔案參考的 **SequenceNumber** 欄位必須符合此欄位的內容;如果不相符，則檔案參考不正確，而且可能已淘汰。</span><span class="sxs-lookup"><span data-stu-id="e1356-118">The **SequenceNumber** field of a file reference must match the contents of this field; if they do not match, the file reference is incorrect and probably obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="e1356-119">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="e1356-119">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-120">保留的。</span><span class="sxs-lookup"><span data-stu-id="e1356-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e1356-121">**FirstAttributeOffset**</span><span class="sxs-lookup"><span data-stu-id="e1356-121">**FirstAttributeOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-122">第一個屬性記錄的位移，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="e1356-122">The offset of the first attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e1356-123">**旗標**</span><span class="sxs-lookup"><span data-stu-id="e1356-123">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-124">檔案旗標。</span><span class="sxs-lookup"><span data-stu-id="e1356-124">The file flags.</span></span>

<dl> <dt>

<span data-ttu-id="e1356-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**檔案 \_\_ \_ \_ 使用中的記錄區段** (0x0001) </span><span class="sxs-lookup"><span data-stu-id="e1356-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE\_RECORD\_SEGMENT\_IN\_USE** (0x0001)</span></span>
</dt> <dt>

<span data-ttu-id="e1356-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**檔案 \_檔案名 \_ \_ 索引 \_ 存在** (0x0002) </span><span class="sxs-lookup"><span data-stu-id="e1356-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE\_FILE\_NAME\_INDEX\_PRESENT** (0x0002)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="e1356-127">**Reserved3**</span><span class="sxs-lookup"><span data-stu-id="e1356-127">**Reserved3**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-128">保留的。</span><span class="sxs-lookup"><span data-stu-id="e1356-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e1356-129">**BaseFileRecordSegment**</span><span class="sxs-lookup"><span data-stu-id="e1356-129">**BaseFileRecordSegment**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-130">這個檔案的基底檔案記錄區段的檔案參考。</span><span class="sxs-lookup"><span data-stu-id="e1356-130">A file reference to the base file record segment for this file.</span></span> <span data-ttu-id="e1356-131">如果這是基底檔案記錄，則值為0。</span><span class="sxs-lookup"><span data-stu-id="e1356-131">If this is the base file record, the value is 0.</span></span> <span data-ttu-id="e1356-132">請參閱 [**MFT \_ 區段 \_ 參考**](mft-segment-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="e1356-132">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1356-133">**Reserved4**</span><span class="sxs-lookup"><span data-stu-id="e1356-133">**Reserved4**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-134">保留的。</span><span class="sxs-lookup"><span data-stu-id="e1356-134">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e1356-135">**UpdateSequenceArray**</span><span class="sxs-lookup"><span data-stu-id="e1356-135">**UpdateSequenceArray**</span></span>
</dt> <dd>

<span data-ttu-id="e1356-136">更新順序陣列，用來保護檔案記錄區段的 multisector 傳輸。</span><span class="sxs-lookup"><span data-stu-id="e1356-136">The update sequence array to protect multisector transfers of the file record segment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1356-137">備註</span><span class="sxs-lookup"><span data-stu-id="e1356-137">Remarks</span></span>

<span data-ttu-id="e1356-138">請注意，此結構沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="e1356-138">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="e1356-139">此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。</span><span class="sxs-lookup"><span data-stu-id="e1356-139">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="e1356-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1356-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1356-141">主檔案資料表</span><span class="sxs-lookup"><span data-stu-id="e1356-141">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
