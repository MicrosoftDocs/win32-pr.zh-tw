---
title: 'BG_JOB_PROGRESS 結構 (>deliveryoptimization .h) '
description: BG_JOB_PROGRESS 結構會提供作業相關的進度資訊，例如已傳送的位元組和檔案數目。 針對上傳作業，進度會套用至上傳檔案，而不是回復檔。
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- BG_JOB_PROGRESS 結構
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509088"
---
# <a name="bg_job_progress-structure"></a><span data-ttu-id="5d3a0-105">BG_JOB_PROGRESS 結構</span><span class="sxs-lookup"><span data-stu-id="5d3a0-105">BG_JOB_PROGRESS structure</span></span>

<span data-ttu-id="5d3a0-106">**BG_JOB_PROGRESS** 結構會提供作業相關的進度資訊，例如已傳送的位元組和檔案數目。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-106">The **BG_JOB_PROGRESS** structure provides job-related progress information, such as the number of bytes and files transferred.</span></span> <span data-ttu-id="5d3a0-107">針對上傳作業，進度會套用至上傳檔案，而不是回復檔。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-107">For upload jobs, the progress applies to the upload file, not the reply file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d3a0-108">語法</span><span class="sxs-lookup"><span data-stu-id="5d3a0-108">Syntax</span></span>


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="5d3a0-109">成員</span><span class="sxs-lookup"><span data-stu-id="5d3a0-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d3a0-110">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="5d3a0-110">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="5d3a0-111">要針對作業中的所有檔案傳送的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-111">Total number of bytes to transfer for all files in the job.</span></span> <span data-ttu-id="5d3a0-112">如果值為 BG_SIZE_UNKNOWN，則不會判斷作業中所有檔案的總大小。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-112">If the value is BG_SIZE_UNKNOWN, the total size of all files in the job has not been determined.</span></span> <span data-ttu-id="5d3a0-113">如果無法判斷其中一個檔案的大小，則不會設定此值。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-113">DO does not set this value if it cannot determine the size of one of the files.</span></span> <span data-ttu-id="5d3a0-114">例如，如果指定的檔案或伺服器不存在，就無法判斷檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-114">For example, if the specified file or server does not exist, DO cannot determine the size of the file.</span></span>

<span data-ttu-id="5d3a0-115">如果您要從檔案下載範圍， **BytesTotal** 會包含您想要從檔案下載的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-115">If you are downloading ranges from the file, **BytesTotal** includes the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="5d3a0-116">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="5d3a0-116">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="5d3a0-117">傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-117">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="5d3a0-118">**FilesTotal**</span><span class="sxs-lookup"><span data-stu-id="5d3a0-118">**FilesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="5d3a0-119">要針對此作業傳送的檔案總數。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-119">Total number of files to transfer for this job.</span></span>

</dd> <dt>

<span data-ttu-id="5d3a0-120">**FilesTransferred**</span><span class="sxs-lookup"><span data-stu-id="5d3a0-120">**FilesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="5d3a0-121">傳輸的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="5d3a0-121">Number of files transferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d3a0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d3a0-122">Requirements</span></span>



| <span data-ttu-id="5d3a0-123">需求</span><span class="sxs-lookup"><span data-stu-id="5d3a0-123">Requirement</span></span> | <span data-ttu-id="5d3a0-124">值</span><span class="sxs-lookup"><span data-stu-id="5d3a0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d3a0-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d3a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5d3a0-126">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d3a0-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5d3a0-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d3a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5d3a0-128">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d3a0-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5d3a0-129">標頭</span><span class="sxs-lookup"><span data-stu-id="5d3a0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d3a0-130"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d3a0-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d3a0-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d3a0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d3a0-132">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="5d3a0-132">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="5d3a0-133">**IBackgroundCopyJob：： GetProgress**</span><span class="sxs-lookup"><span data-stu-id="5d3a0-133">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





