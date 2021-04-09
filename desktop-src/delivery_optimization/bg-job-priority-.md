---
title: 'BG_JOB_PRIORITY 列舉 (>deliveryoptimization .h) '
description: BG_JOB_PRIORITY 列舉會定義常數值，以指定工作的優先權層級。
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- BG_JOB_PRIORITY 列舉
- BG_JOB_PRIORITY 列舉
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024961"
---
# <a name="bg_job_priority-enumeration"></a><span data-ttu-id="df1ce-105">BG_JOB_PRIORITY 列舉</span><span class="sxs-lookup"><span data-stu-id="df1ce-105">BG_JOB_PRIORITY enumeration</span></span>

<span data-ttu-id="df1ce-106">**BG_JOB_PRIORITY** 列舉會定義常數值，以指定工作的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="df1ce-106">The **BG_JOB_PRIORITY** enumeration defines the constant values that specify the priority level of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="df1ce-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="df1ce-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a><span data-ttu-id="df1ce-108">常數</span><span class="sxs-lookup"><span data-stu-id="df1ce-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="df1ce-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span><span class="sxs-lookup"><span data-stu-id="df1ce-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span></span>
</dt> <dd>

<span data-ttu-id="df1ce-110">在前景中傳送工作。</span><span class="sxs-lookup"><span data-stu-id="df1ce-110">Transfers the job in the foreground.</span></span> <span data-ttu-id="df1ce-111">前景傳輸會與其他應用程式競爭網路頻寬，這可能會妨礙使用者的網路體驗。</span><span class="sxs-lookup"><span data-stu-id="df1ce-111">Foreground transfers compete for network bandwidth with other applications, which can impede the user's network experience.</span></span> <span data-ttu-id="df1ce-112">這是最高的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="df1ce-112">This is the highest priority level.</span></span>

</dd> <dt>

<span data-ttu-id="df1ce-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span><span class="sxs-lookup"><span data-stu-id="df1ce-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="df1ce-114">在背景中傳送作業。</span><span class="sxs-lookup"><span data-stu-id="df1ce-114">Transfers the job in the background.</span></span> <span data-ttu-id="df1ce-115">背景傳輸使用的是較小的網路頻寬百分比。</span><span class="sxs-lookup"><span data-stu-id="df1ce-115">Background transfers use a small percentage of network bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="df1ce-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span><span class="sxs-lookup"><span data-stu-id="df1ce-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="df1ce-117">所有非前景作業的行為都相同。</span><span class="sxs-lookup"><span data-stu-id="df1ce-117">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="df1ce-118">如需詳細資訊，請參閱 BG_JOB_PRIORITY_HIGH 中的批註。</span><span class="sxs-lookup"><span data-stu-id="df1ce-118">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> <dt>

<span data-ttu-id="df1ce-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span><span class="sxs-lookup"><span data-stu-id="df1ce-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="df1ce-120">所有非前景作業的行為都相同。</span><span class="sxs-lookup"><span data-stu-id="df1ce-120">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="df1ce-121">如需詳細資訊，請參閱 BG_JOB_PRIORITY_HIGH 中的批註。</span><span class="sxs-lookup"><span data-stu-id="df1ce-121">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df1ce-122">備註</span><span class="sxs-lookup"><span data-stu-id="df1ce-122">Remarks</span></span>

<span data-ttu-id="df1ce-123">您可以同時進行多個前景和背景傳輸。</span><span class="sxs-lookup"><span data-stu-id="df1ce-123">Multiple foreground and background transfers can take place simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="df1ce-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="df1ce-124">Requirements</span></span>



| <span data-ttu-id="df1ce-125">需求</span><span class="sxs-lookup"><span data-stu-id="df1ce-125">Requirement</span></span> | <span data-ttu-id="df1ce-126">值</span><span class="sxs-lookup"><span data-stu-id="df1ce-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df1ce-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df1ce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="df1ce-128">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df1ce-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="df1ce-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df1ce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="df1ce-130">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df1ce-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="df1ce-131">標頭</span><span class="sxs-lookup"><span data-stu-id="df1ce-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="df1ce-132"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="df1ce-132"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df1ce-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df1ce-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df1ce-134">**IBackgroundCopyJob：： GetPriority**</span><span class="sxs-lookup"><span data-stu-id="df1ce-134">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[<span data-ttu-id="df1ce-135">**IBackgroundCopyJob：： SetPriority**</span><span class="sxs-lookup"><span data-stu-id="df1ce-135">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





