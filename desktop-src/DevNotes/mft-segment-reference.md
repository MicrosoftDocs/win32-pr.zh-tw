---
description: 代表主要檔案資料表中 (MFT) 的位址。 位址會以迴圈的重複使用序號標記，此序號是在 MFT 區段參考有效時所設定。
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: MFT_SEGMENT_REFERENCE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109929"
---
# <a name="mft_segment_reference-structure"></a><span data-ttu-id="bd5db-104">MFT \_ 區段 \_ 參考結構</span><span class="sxs-lookup"><span data-stu-id="bd5db-104">MFT\_SEGMENT\_REFERENCE structure</span></span>

<span data-ttu-id="bd5db-105">\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]</span><span class="sxs-lookup"><span data-stu-id="bd5db-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="bd5db-106">代表主要檔案資料表中 (MFT) 的位址。</span><span class="sxs-lookup"><span data-stu-id="bd5db-106">Represents an address in the master file table (MFT).</span></span> <span data-ttu-id="bd5db-107">位址會以迴圈的重複使用序號標記，此序號是在 MFT 區段參考有效時所設定。</span><span class="sxs-lookup"><span data-stu-id="bd5db-107">The address is tagged with a circularly reused sequence number that is set at the time the MFT segment reference was valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5db-108">語法</span><span class="sxs-lookup"><span data-stu-id="bd5db-108">Syntax</span></span>


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a><span data-ttu-id="bd5db-109">成員</span><span class="sxs-lookup"><span data-stu-id="bd5db-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd5db-110">**SegmentNumberLowPart**</span><span class="sxs-lookup"><span data-stu-id="bd5db-110">**SegmentNumberLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="bd5db-111">區段編號的低部分。</span><span class="sxs-lookup"><span data-stu-id="bd5db-111">The low part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="bd5db-112">**SegmentNumberHighPart**</span><span class="sxs-lookup"><span data-stu-id="bd5db-112">**SegmentNumberHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="bd5db-113">區段編號的最高部分。</span><span class="sxs-lookup"><span data-stu-id="bd5db-113">The high part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="bd5db-114">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="bd5db-114">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="bd5db-115">非零的序號。</span><span class="sxs-lookup"><span data-stu-id="bd5db-115">The nonzero sequence number.</span></span> <span data-ttu-id="bd5db-116">0值為 reserved。</span><span class="sxs-lookup"><span data-stu-id="bd5db-116">The value 0 is reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd5db-117">備註</span><span class="sxs-lookup"><span data-stu-id="bd5db-117">Remarks</span></span>

<span data-ttu-id="bd5db-118">請注意，此結構沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="bd5db-118">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="bd5db-119">此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。</span><span class="sxs-lookup"><span data-stu-id="bd5db-119">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="bd5db-120">檔案 **\_ 參考** 資料類型的定義如下。</span><span class="sxs-lookup"><span data-stu-id="bd5db-120">The **FILE\_REFERENCE** data type is defined as follows.</span></span>

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a><span data-ttu-id="bd5db-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd5db-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5db-122">主檔案資料表</span><span class="sxs-lookup"><span data-stu-id="bd5db-122">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
