---
title: 'BG_JOB_TYPE 列舉 (>deliveryoptimization .h) '
description: BG_JOB_TYPE 列舉會定義常數值，以指定傳送作業的類型，例如 [下載]。
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- BG_JOB_TYPE 列舉
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464945"
---
# <a name="bg_job_type-enumeration"></a><span data-ttu-id="3cf1b-104">BG_JOB_TYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="3cf1b-104">BG_JOB_TYPE enumeration</span></span>

<span data-ttu-id="3cf1b-105">**BG_JOB_TYPE** 列舉會定義常數值，以指定傳送作業的類型，例如 [下載]。</span><span class="sxs-lookup"><span data-stu-id="3cf1b-105">The **BG_JOB_TYPE** enumeration defines constant values that specify the type of transfer job, such as download.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf1b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cf1b-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a><span data-ttu-id="3cf1b-107">常數</span><span class="sxs-lookup"><span data-stu-id="3cf1b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3cf1b-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span><span class="sxs-lookup"><span data-stu-id="3cf1b-108"><span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="3cf1b-109">指定作業將檔下載至用戶端。</span><span class="sxs-lookup"><span data-stu-id="3cf1b-109">Specifies that the job downloads files to the client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3cf1b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cf1b-110">Requirements</span></span>



| <span data-ttu-id="3cf1b-111">需求</span><span class="sxs-lookup"><span data-stu-id="3cf1b-111">Requirement</span></span> | <span data-ttu-id="3cf1b-112">值</span><span class="sxs-lookup"><span data-stu-id="3cf1b-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf1b-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3cf1b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf1b-114">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf1b-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3cf1b-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3cf1b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf1b-116">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3cf1b-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3cf1b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="3cf1b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cf1b-118"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf1b-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf1b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cf1b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf1b-120">**IBackgroundCopyJob：： GetType**</span><span class="sxs-lookup"><span data-stu-id="3cf1b-120">**IBackgroundCopyJob::GetType**</span></span>](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[<span data-ttu-id="3cf1b-121">**IBackgroundCopyManager：： >batchclient.joboperations.createjob**</span><span class="sxs-lookup"><span data-stu-id="3cf1b-121">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





