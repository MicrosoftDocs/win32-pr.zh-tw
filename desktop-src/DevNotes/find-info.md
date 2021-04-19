---
description: 包含搜尋內容資訊。
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: FIND_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966627"
---
# <a name="find_info-structure"></a><span data-ttu-id="1b129-103">尋找 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="1b129-103">FIND\_INFO structure</span></span>

<span data-ttu-id="1b129-104">包含搜尋內容資訊。</span><span class="sxs-lookup"><span data-stu-id="1b129-104">Contains search context information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b129-105">語法</span><span class="sxs-lookup"><span data-stu-id="1b129-105">Syntax</span></span>


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a><span data-ttu-id="1b129-106">成員</span><span class="sxs-lookup"><span data-stu-id="1b129-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b129-107">**tiIndex**</span><span class="sxs-lookup"><span data-stu-id="1b129-107">**tiIndex**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-108">要搜尋之索引的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="1b129-108">The **TAGID** for the index to be searched.</span></span>

</dd> <dt>

<span data-ttu-id="1b129-109">**tiCurrent**</span><span class="sxs-lookup"><span data-stu-id="1b129-109">**tiCurrent**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-110">目前所在專案的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="1b129-110">The **TAGID** for the current item that was located.</span></span>

</dd> <dt>

<span data-ttu-id="1b129-111">**tiEndIndex**</span><span class="sxs-lookup"><span data-stu-id="1b129-111">**tiEndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-112">如果索引是唯一的，則為 FindFirst 之後最後一筆記錄的 **TAGID** 。</span><span class="sxs-lookup"><span data-stu-id="1b129-112">The **TAGID** for the last record after FindFirst if the index is UNIQUE.</span></span>

</dd> <dt>

<span data-ttu-id="1b129-113">**tName**</span><span class="sxs-lookup"><span data-stu-id="1b129-113">**tName**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-114">要找出的專案類型。</span><span class="sxs-lookup"><span data-stu-id="1b129-114">The type of the item to be located.</span></span> <span data-ttu-id="1b129-115">請參閱 [標記類型](tag-types.md)。</span><span class="sxs-lookup"><span data-stu-id="1b129-115">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b129-116">**dwIndexRec**</span><span class="sxs-lookup"><span data-stu-id="1b129-116">**dwIndexRec**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-117">用來追蹤下一個尋找作業應從索引中何處開始的內部計數器。</span><span class="sxs-lookup"><span data-stu-id="1b129-117">An internal counter used to track where in the index the next find operation should start.</span></span>

</dd> <dt>

<span data-ttu-id="1b129-118">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="1b129-118">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-119">這個成員可以是0或 **SHIMDB \_ 索引 \_ 唯一索引 \_ 鍵** (0x00000001) ，表示這是唯一索引鍵索引。</span><span class="sxs-lookup"><span data-stu-id="1b129-119">This member can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001), which indicates that this is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="1b129-120">**ullKey**</span><span class="sxs-lookup"><span data-stu-id="1b129-120">**ullKey**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-121">目前專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="1b129-121">The key for the current entry.</span></span>

</dd> <dt>

<span data-ttu-id="1b129-122">**szName**</span><span class="sxs-lookup"><span data-stu-id="1b129-122">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-123">如果標記類型為 **標記 \_ 類型 \_ STRINGREF**) ，則為目前的字串 (。</span><span class="sxs-lookup"><span data-stu-id="1b129-123">The current string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> <dt>

<span data-ttu-id="1b129-124">**dwName**</span><span class="sxs-lookup"><span data-stu-id="1b129-124">**dwName**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-125">目前的 **DWORD** 值 (是否標記類型為 **標記 \_ 類型 \_ DWORD**) 。</span><span class="sxs-lookup"><span data-stu-id="1b129-125">The current **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="1b129-126">**pguidName**</span><span class="sxs-lookup"><span data-stu-id="1b129-126">**pguidName**</span></span>
</dt> <dd>

<span data-ttu-id="1b129-127">目前的 GUID 值 (如果標記類型是 **標記 \_ 類型 \_ BINARY** ，而且標記是 **標記 \_ 資料庫 \_ 識別碼**) 。</span><span class="sxs-lookup"><span data-stu-id="1b129-127">The current GUID value (if the tag type is **TAG\_TYPE\_BINARY** and the TAG is **TAG\_DATABASE\_ID**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b129-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b129-128">Requirements</span></span>



| <span data-ttu-id="1b129-129">需求</span><span class="sxs-lookup"><span data-stu-id="1b129-129">Requirement</span></span> | <span data-ttu-id="1b129-130">值</span><span class="sxs-lookup"><span data-stu-id="1b129-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b129-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b129-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1b129-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b129-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1b129-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b129-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1b129-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b129-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b129-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b129-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b129-136">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="1b129-136">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




