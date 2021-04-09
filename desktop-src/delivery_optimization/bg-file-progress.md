---
title: 'BG_FILE_PROGRESS 結構 (>deliveryoptimization .h) '
description: BG_FILE_PROGRESS 結構會提供檔案相關的進度資訊，例如已傳送的位元組數目。
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- BG_FILE_PROGRESS 結構
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686249"
---
# <a name="bg_file_progress-structure"></a><span data-ttu-id="2891d-104">BG_FILE_PROGRESS 結構</span><span class="sxs-lookup"><span data-stu-id="2891d-104">BG_FILE_PROGRESS structure</span></span>

<span data-ttu-id="2891d-105">**BG_FILE_PROGRESS** 結構會提供檔案相關的進度資訊，例如已傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2891d-105">The **BG_FILE_PROGRESS** structure provides file-related progress information, such as the number of bytes transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="2891d-106">語法</span><span class="sxs-lookup"><span data-stu-id="2891d-106">Syntax</span></span>


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="2891d-107">成員</span><span class="sxs-lookup"><span data-stu-id="2891d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2891d-108">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="2891d-108">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="2891d-109">檔案大小，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="2891d-109">Size of the file in bytes.</span></span> <span data-ttu-id="2891d-110">如果無法判斷檔案的大小 (例如，如果檔案或伺服器) 不存在，則會 DO_UNKNOWN_FILE_SIZE 此值。</span><span class="sxs-lookup"><span data-stu-id="2891d-110">If DO cannot determine the size of the file (for example, if the file or server does not exist), the value is DO_UNKNOWN_FILE_SIZE.</span></span>

<span data-ttu-id="2891d-111">如果您是從檔案下載範圍， **BytesTotal** 會反映您想要從檔案下載的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="2891d-111">If you are downloading ranges from a file, **BytesTotal** reflects the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="2891d-112">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="2891d-112">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="2891d-113">傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2891d-113">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="2891d-114">**Completed**</span><span class="sxs-lookup"><span data-stu-id="2891d-114">**Completed**</span></span>
</dt> <dd>

<span data-ttu-id="2891d-115">若為下載，當使用者可以使用檔案時，此值為 **TRUE** 。否則，此值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2891d-115">For downloads, the value is **TRUE** if the file is available to the user; otherwise, the value is **FALSE**.</span></span> <span data-ttu-id="2891d-116">在呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法之後，使用者可以使用檔案。</span><span class="sxs-lookup"><span data-stu-id="2891d-116">Files are available to the user after calling the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="2891d-117">如果 **Complete** 方法產生暫時性錯誤，則在發生錯誤之前處理的那些檔案可供使用者使用;其他則否。</span><span class="sxs-lookup"><span data-stu-id="2891d-117">If the **Complete** method generates a transient error, those files processed before the error occurred are available to the user; the others are not.</span></span> <span data-ttu-id="2891d-118">當 **完成** 失敗時，請使用 **完成** 的成員來判斷檔案是否可供使用者使用。</span><span class="sxs-lookup"><span data-stu-id="2891d-118">Use the **Completed** member to determine if the file is available to the user when **Complete** fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2891d-119">備註</span><span class="sxs-lookup"><span data-stu-id="2891d-119">Remarks</span></span>

<span data-ttu-id="2891d-120">若要判斷是否已傳送檔案，您可以：</span><span class="sxs-lookup"><span data-stu-id="2891d-120">To determine if DO transferred the file, you can:</span></span>

-   <span data-ttu-id="2891d-121">比較 **BytesTransferred** 與 **BytesTotal**。</span><span class="sxs-lookup"><span data-stu-id="2891d-121">Compare **BytesTransferred** to **BytesTotal**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2891d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2891d-122">Requirements</span></span>



| <span data-ttu-id="2891d-123">需求</span><span class="sxs-lookup"><span data-stu-id="2891d-123">Requirement</span></span> | <span data-ttu-id="2891d-124">值</span><span class="sxs-lookup"><span data-stu-id="2891d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2891d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2891d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2891d-126">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2891d-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2891d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2891d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2891d-128">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2891d-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2891d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2891d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2891d-130"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="2891d-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2891d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2891d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2891d-132">**BG_JOB_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="2891d-132">**BG_JOB_PROGRESS**</span></span>](bg-job-progress.md)
</dt> <dt>

[<span data-ttu-id="2891d-133">**IBackgroundCopyFile：： GetProgress**</span><span class="sxs-lookup"><span data-stu-id="2891d-133">**IBackgroundCopyFile::GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





