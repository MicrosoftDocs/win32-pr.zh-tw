---
title: CHANGE_LOG_HEADER 結構
description: 變更記錄標頭。
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- CHANGE_LOG_HEADER 結構系統還原
- PCHANGE_LOG_HEADER 結構指標系統還原
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383994"
---
# <a name="change_log_header-structure"></a><span data-ttu-id="5ef6a-105">變更 \_ 記錄 \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="5ef6a-105">CHANGE\_LOG\_HEADER structure</span></span>

<span data-ttu-id="5ef6a-106">\[此資訊只適用于 Windows XP Service Pack 2 (SP2) 。\]</span><span class="sxs-lookup"><span data-stu-id="5ef6a-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="5ef6a-107">變更記錄標頭。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-107">The change log header.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef6a-108">語法</span><span class="sxs-lookup"><span data-stu-id="5ef6a-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a><span data-ttu-id="5ef6a-109">成員</span><span class="sxs-lookup"><span data-stu-id="5ef6a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ef6a-110">**RecordHeader**</span><span class="sxs-lookup"><span data-stu-id="5ef6a-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="5ef6a-111">[**記錄 \_ 標頭**](record-header.md)結構。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="5ef6a-112">**DwRecordType** 成員應設定為 RecordTypeLogHeader (0) 。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-112">The **dwRecordType** member should be set to RecordTypeLogHeader (0).</span></span> <span data-ttu-id="5ef6a-113">**DwRecordSize** 成員應考慮所有成員，再加上此標頭後面的額外 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-113">The **dwRecordSize** member should account for all the members, plus the extra **DWORD** value that follows this header.</span></span> <span data-ttu-id="5ef6a-114">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-114">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5ef6a-115">**dwMagicNum**</span><span class="sxs-lookup"><span data-stu-id="5ef6a-115">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="5ef6a-116">此成員應設定為0xabcdef12。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-116">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="5ef6a-117">**dwLogVersion**</span><span class="sxs-lookup"><span data-stu-id="5ef6a-117">**dwLogVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5ef6a-118">此成員應設定為2。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-118">This member should be set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="5ef6a-119">**DataHeader**</span><span class="sxs-lookup"><span data-stu-id="5ef6a-119">**DataHeader**</span></span>
</dt> <dd>

<span data-ttu-id="5ef6a-120">[**記錄 \_ 標頭**](record-header.md)結構。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-120">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="5ef6a-121">**DwRecordType** 成員應設定為 **RecordTypeVolumePath** (2) 。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-121">The **dwRecordType** member should be set to **RecordTypeVolumePath** (2).</span></span>

</dd> <dt>

<span data-ttu-id="5ef6a-122">**byteData**</span><span class="sxs-lookup"><span data-stu-id="5ef6a-122">**byteData**</span></span>
</dt> <dd>

<span data-ttu-id="5ef6a-123">指定磁片區路徑之以 null 結束的字串開頭。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-123">The start of a null-terminated string that specifies the volume path.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ef6a-124">備註</span><span class="sxs-lookup"><span data-stu-id="5ef6a-124">Remarks</span></span>

<span data-ttu-id="5ef6a-125">此標頭後面接著應與 **RecordHeader** 的 **dwRecordSize** 成員值相同的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="5ef6a-125">This header is followed by a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef6a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ef6a-126">Requirements</span></span>



| <span data-ttu-id="5ef6a-127">需求</span><span class="sxs-lookup"><span data-stu-id="5ef6a-127">Requirement</span></span> | <span data-ttu-id="5ef6a-128">值</span><span class="sxs-lookup"><span data-stu-id="5ef6a-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ef6a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ef6a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef6a-130">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ef6a-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5ef6a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ef6a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef6a-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="5ef6a-132">None supported</span></span><br/>                            |
| <span data-ttu-id="5ef6a-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5ef6a-133">End of client support</span></span><br/>    | <span data-ttu-id="5ef6a-134">Windows XP 含 SP2</span><span class="sxs-lookup"><span data-stu-id="5ef6a-134">Windows XP with SP2</span></span><br/>                       |



 

 





