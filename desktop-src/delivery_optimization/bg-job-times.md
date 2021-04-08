---
title: 'BG_JOB_TIMES 結構 (>deliveryoptimization .h) '
description: BG_JOB_TIMES 結構會提供作業相關的時間戳記。
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- BG_JOB_TIMES 結構
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685613"
---
# <a name="bg_job_times-structure"></a><span data-ttu-id="f2e02-104">BG_JOB_TIMES 結構</span><span class="sxs-lookup"><span data-stu-id="f2e02-104">BG_JOB_TIMES structure</span></span>

<span data-ttu-id="f2e02-105">**BG_JOB_TIMES** 結構會提供作業相關的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f2e02-105">The **BG_JOB_TIMES** structure provides job-related time stamps.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e02-106">語法</span><span class="sxs-lookup"><span data-stu-id="f2e02-106">Syntax</span></span>


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a><span data-ttu-id="f2e02-107">成員</span><span class="sxs-lookup"><span data-stu-id="f2e02-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f2e02-108">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="f2e02-108">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="f2e02-109">建立作業的時間。</span><span class="sxs-lookup"><span data-stu-id="f2e02-109">Time the job was created.</span></span> <span data-ttu-id="f2e02-110">時間會指定為 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)。</span><span class="sxs-lookup"><span data-stu-id="f2e02-110">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="f2e02-111">**ModificationTime**</span><span class="sxs-lookup"><span data-stu-id="f2e02-111">**ModificationTime**</span></span>
</dt> <dd>

<span data-ttu-id="f2e02-112">上次修改作業或傳輸位元組的時間。</span><span class="sxs-lookup"><span data-stu-id="f2e02-112">Time the job was last modified or bytes were transferred.</span></span> <span data-ttu-id="f2e02-113">在 [ \* *IBackgroundCopyJob \** _](/previous-versions//mt811348(v=vs.85))介面中新增檔案或呼叫任何 set 方法會變更此值。</span><span class="sxs-lookup"><span data-stu-id="f2e02-113">Adding files or calling any of the set methods in the [\**IBackgroundCopyJob\** _](/previous-versions//mt811348(v=vs.85)) interfaces changes this value.</span></span> <span data-ttu-id="f2e02-114">此外，變更作業的狀態以及呼叫 [_ *暫* \*](ibackgroundcopyjob-suspend.md)止、[**繼續**](ibackgroundcopyjob-resume.md)、[**取消**](ibackgroundcopyjob-cancel.md)和 [**完成**](ibackgroundcopyjob-complete.md)方法會變更此值。</span><span class="sxs-lookup"><span data-stu-id="f2e02-114">In addition, changes to the state of the job and calling the [_ *Suspend*\*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md), and [**Complete**](ibackgroundcopyjob-complete.md) methods change this value.</span></span> <span data-ttu-id="f2e02-115">時間會指定為 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)。</span><span class="sxs-lookup"><span data-stu-id="f2e02-115">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="f2e02-116">**TransferCompletionTime**</span><span class="sxs-lookup"><span data-stu-id="f2e02-116">**TransferCompletionTime**</span></span>
</dt> <dd>

<span data-ttu-id="f2e02-117">工作進入 BG_JOB_STATE_TRANSFERRED 狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="f2e02-117">Time the job entered the BG_JOB_STATE_TRANSFERRED state.</span></span> <span data-ttu-id="f2e02-118">時間會指定為 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)。</span><span class="sxs-lookup"><span data-stu-id="f2e02-118">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2e02-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2e02-119">Requirements</span></span>



| <span data-ttu-id="f2e02-120">需求</span><span class="sxs-lookup"><span data-stu-id="f2e02-120">Requirement</span></span> | <span data-ttu-id="f2e02-121">值</span><span class="sxs-lookup"><span data-stu-id="f2e02-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e02-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2e02-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e02-123">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2e02-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f2e02-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2e02-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e02-125">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2e02-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f2e02-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f2e02-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2e02-127"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="f2e02-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2e02-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2e02-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e02-129">**IBackgroundCopyJob::GetTimes**</span><span class="sxs-lookup"><span data-stu-id="f2e02-129">**IBackgroundCopyJob::GetTimes**</span></span>](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

