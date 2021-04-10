---
description: 表示 multisector 標頭。
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: MULTI_SECTOR_HEADER 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688619"
---
# <a name="multi_sector_header-structure"></a><span data-ttu-id="114e9-103">多 \_ 磁區 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="114e9-103">MULTI\_SECTOR\_HEADER structure</span></span>

<span data-ttu-id="114e9-104">\[此結構只對 NTFS 磁片區的第3版有效;未來的版本可能會改變。\]</span><span class="sxs-lookup"><span data-stu-id="114e9-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="114e9-105">表示 multisector 標頭。</span><span class="sxs-lookup"><span data-stu-id="114e9-105">Represents the multisector header.</span></span>

## <a name="syntax"></a><span data-ttu-id="114e9-106">語法</span><span class="sxs-lookup"><span data-stu-id="114e9-106">Syntax</span></span>


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a><span data-ttu-id="114e9-107">成員</span><span class="sxs-lookup"><span data-stu-id="114e9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="114e9-108">**簽名**</span><span class="sxs-lookup"><span data-stu-id="114e9-108">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="114e9-109">簽章。</span><span class="sxs-lookup"><span data-stu-id="114e9-109">The signature.</span></span> <span data-ttu-id="114e9-110">此值是使用者的便利性。</span><span class="sxs-lookup"><span data-stu-id="114e9-110">This value is a convenience to the user.</span></span>

</dd> <dt>

<span data-ttu-id="114e9-111">**UpdateSequenceArrayOffset**</span><span class="sxs-lookup"><span data-stu-id="114e9-111">**UpdateSequenceArrayOffset**</span></span>
</dt> <dd>

<span data-ttu-id="114e9-112">更新順序陣列的位移，從這個結構的開頭算起。</span><span class="sxs-lookup"><span data-stu-id="114e9-112">The offset to the update sequence array, from the start of this structure.</span></span> <span data-ttu-id="114e9-113">更新順序陣列必須在第一個磁區的最後一個 USHORT 值之前結束。</span><span class="sxs-lookup"><span data-stu-id="114e9-113">The update sequence array must end before the last USHORT value in the first sector.</span></span>

</dd> <dt>

<span data-ttu-id="114e9-114">**UpdateSequenceArraySize**</span><span class="sxs-lookup"><span data-stu-id="114e9-114">**UpdateSequenceArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="114e9-115">更新順序陣列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="114e9-115">The size of the update sequence array, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="114e9-116">備註</span><span class="sxs-lookup"><span data-stu-id="114e9-116">Remarks</span></span>

<span data-ttu-id="114e9-117">請注意，此結構沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="114e9-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="114e9-118">此結構定義僅適用于主要版本3和次要版本0或1，如 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)所報告。</span><span class="sxs-lookup"><span data-stu-id="114e9-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="114e9-119">Multisector 標頭和更新順序陣列針對實體磁區大小大於或等於序號 stride (512) 或未依順序傳送磁區的裝置，提供不完整的 multisector 傳輸偵測。</span><span class="sxs-lookup"><span data-stu-id="114e9-119">The multisector header and update sequence array provide detection of incomplete multisector transfers for devices that either have a physical sector size greater than or equal to the sequence number stride (512) or that do not transfer sectors out of order.</span></span> <span data-ttu-id="114e9-120">如果有磁區大小小於序號 stride 的裝置，而且有時會依序傳送磁區，則更新序列陣列將不會提供不完整傳輸的絕對偵測。</span><span class="sxs-lookup"><span data-stu-id="114e9-120">If a device exists that has a sector size smaller than the sequence number stride and it sometimes transfers sectors out of order, then the update sequence array will not provide absolute detection of incomplete transfers.</span></span> <span data-ttu-id="114e9-121">序號 stride 設定為夠小的數位，以提供所有已知硬碟的絕對保護。</span><span class="sxs-lookup"><span data-stu-id="114e9-121">The sequence number stride is set to a small enough number to provide absolute protection for all known hard disks.</span></span> <span data-ttu-id="114e9-122">它未設定為較小，或可能有過多的執行時間或空間額外負荷。</span><span class="sxs-lookup"><span data-stu-id="114e9-122">It is not set any smaller or there might be excessive run time or space overhead.</span></span>

<span data-ttu-id="114e9-123">更新順序陣列包含 *n* **USHORT** 值的陣列，其中 *n* 是受保護的結構大小除以序號 stride。</span><span class="sxs-lookup"><span data-stu-id="114e9-123">The update sequence array consists of an array of *n* **USHORT** values, where *n* is the size of the structure being protected divided by the sequence number stride.</span></span> <span data-ttu-id="114e9-124">第一個單字包含更新序號，也就是包含結構寫入磁片的次數的迴圈計數器。</span><span class="sxs-lookup"><span data-stu-id="114e9-124">The first word contains the update sequence number, which is a cyclical counter of the number of times the containing structure has been written to disk.</span></span> <span data-ttu-id="114e9-125">接下來是在最後一次將包含結構寫入磁片時，更新序號所覆寫的 *n* 個儲存的 **USHORT** 值。</span><span class="sxs-lookup"><span data-stu-id="114e9-125">Next are the *n* saved **USHORT** values that were overwritten by the update sequence number the last time the containing structure was written to disk.</span></span>

<span data-ttu-id="114e9-126">每次受保護的結構即將寫入磁片時，每個序號 stride 中的最後一個單字會儲存至序號陣列中的個別位置，然後以下一個更新序號加以覆寫。</span><span class="sxs-lookup"><span data-stu-id="114e9-126">Each time the protected structure is about to be written to disk, the last word in each sequence number stride is saved to its respective position in the sequence number array, then it is overwritten with the next update sequence number.</span></span> <span data-ttu-id="114e9-127">在寫入之後，或每次讀取結構時，序號陣列中儲存的單字會還原為其在結構中的實際位置。</span><span class="sxs-lookup"><span data-stu-id="114e9-127">After the write, or whenever the structure is read, the saved word from the sequence number array is restored to its actual position in the structure.</span></span> <span data-ttu-id="114e9-128">在讀取上儲存的文字之前，每個 stride 結尾的所有序號都會與陣列開頭的實際序號進行比較。</span><span class="sxs-lookup"><span data-stu-id="114e9-128">Before restoring the saved words on reads, all the sequence numbers at the end of each stride are compared with the actual sequence number at the start of the array.</span></span> <span data-ttu-id="114e9-129">如果其中任何一項比較不相等，則會偵測到失敗的 multisector 轉移。</span><span class="sxs-lookup"><span data-stu-id="114e9-129">If any of these comparisons are not equal, then a failed multisector transfer has been detected.</span></span>

<span data-ttu-id="114e9-130">陣列的大小取決於包含結構的大小。</span><span class="sxs-lookup"><span data-stu-id="114e9-130">The size of the array is determined by the size of the containing structure.</span></span> <span data-ttu-id="114e9-131">更新順序陣列應包含在它所保護之結構的標頭結尾，因為它的變數大小。</span><span class="sxs-lookup"><span data-stu-id="114e9-131">The update sequence array should be included at the end of the header of the structure it is protecting because of its variable size.</span></span> <span data-ttu-id="114e9-132">使用者必須確定為包含結構保留正確的空間：結構/512 + 1) \* sizeof (USHORT) 的 (大小。</span><span class="sxs-lookup"><span data-stu-id="114e9-132">The user must ensure that the correct space is reserved for the containing structure: (size of structure / 512 + 1) \* sizeof(USHORT).</span></span>

## <a name="see-also"></a><span data-ttu-id="114e9-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="114e9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114e9-134">主檔案資料表</span><span class="sxs-lookup"><span data-stu-id="114e9-134">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
