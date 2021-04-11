---
title: 'IBackgroundCopyManager >batchclient.joboperations.createjob 方法 (>deliveryoptimization .h) '
description: 建立作業。
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- '>batchclient.joboperations.createjob 方法'
- '>batchclient.joboperations.createjob 方法，IBackgroundCopyManager 介面'
- IBackgroundCopyManager 介面，>batchclient.joboperations.createjob 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/27/2021
ms.locfileid: "104027609"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a><span data-ttu-id="31a0d-106">IBackgroundCopyManager：： >batchclient.joboperations.createjob 方法</span><span class="sxs-lookup"><span data-stu-id="31a0d-106">IBackgroundCopyManager::CreateJob method</span></span>

<span data-ttu-id="31a0d-107">建立作業。</span><span class="sxs-lookup"><span data-stu-id="31a0d-107">Creates a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a0d-108">語法</span><span class="sxs-lookup"><span data-stu-id="31a0d-108">Syntax</span></span>


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="31a0d-109">參數</span><span class="sxs-lookup"><span data-stu-id="31a0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a0d-110">*pDisplayName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31a0d-110">*pDisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a0d-111">以 Null 終止的字串，其中包含作業的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="31a0d-111">Null-terminated string that contains a display name for the job.</span></span> <span data-ttu-id="31a0d-112">通常，顯示名稱會用來識別使用者介面中的作業。</span><span class="sxs-lookup"><span data-stu-id="31a0d-112">Typically, the display name is used to identify the job in a user interface.</span></span> <span data-ttu-id="31a0d-113">請注意，有一個以上的作業可能會有相同的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="31a0d-113">Note that more than one job may have the same display name.</span></span> <span data-ttu-id="31a0d-114">不得為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="31a0d-114">Must not be **NULL**.</span></span> <span data-ttu-id="31a0d-115">名稱限制為256個字元，不包括 null 結束字元。</span><span class="sxs-lookup"><span data-stu-id="31a0d-115">The name is limited to 256 characters, not including the null terminator.</span></span>

</dd> <dt>

<span data-ttu-id="31a0d-116">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31a0d-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a0d-117">傳送作業的類型，例如 BG_JOB_TYPE_DOWNLOAD。</span><span class="sxs-lookup"><span data-stu-id="31a0d-117">Type of transfer job, such as BG_JOB_TYPE_DOWNLOAD.</span></span> <span data-ttu-id="31a0d-118">如需傳輸類型的清單，請參閱 [**BG_JOB_TYPE**](bg-job-type.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="31a0d-118">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="31a0d-119">*pJobID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="31a0d-119">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31a0d-120">可唯一識別佇列中的作業。</span><span class="sxs-lookup"><span data-stu-id="31a0d-120">Uniquely identifies your job in the queue.</span></span> <span data-ttu-id="31a0d-121">當您呼叫 [**IBackgroundCopyManager：： GetJob**](ibackgroundcopymanager-getjob.md) 方法以從佇列取得工作時，請使用此識別碼。</span><span class="sxs-lookup"><span data-stu-id="31a0d-121">Use this identifier when you call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method to get a job from the queue.</span></span>

</dd> <dt>

<span data-ttu-id="31a0d-122">*ppJob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="31a0d-122">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31a0d-123">[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)介面指標，可讓您用來修改作業的屬性，並指定要傳送的檔案。</span><span class="sxs-lookup"><span data-stu-id="31a0d-123">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer that you use to modify the job's properties and specify the files to be transferred.</span></span> <span data-ttu-id="31a0d-124">若要啟動佇列中的作業，請呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="31a0d-124">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span> <span data-ttu-id="31a0d-125">完成時釋放 *ppJob* 。</span><span class="sxs-lookup"><span data-stu-id="31a0d-125">Release *ppJob* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a0d-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="31a0d-126">Return value</span></span>

<span data-ttu-id="31a0d-127">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="31a0d-127">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="31a0d-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="31a0d-128">Return code</span></span>                                                                              | <span data-ttu-id="31a0d-129">Description</span><span class="sxs-lookup"><span data-stu-id="31a0d-129">Description</span></span>                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="31a0d-130"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="31a0d-130"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="31a0d-131">已成功產生新的作業。</span><span class="sxs-lookup"><span data-stu-id="31a0d-131">Successfully generated the new job.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31a0d-132">備註</span><span class="sxs-lookup"><span data-stu-id="31a0d-132">Remarks</span></span>

<span data-ttu-id="31a0d-133">只有建立作業的使用者或具有系統管理員許可權的使用者可以 [將檔案新增至作業](https://www.bing.com/search?q=add+files+to+the+job) ，並 [變更作業的屬性](https://www.bing.com/search?q=change+the+job's+properties)。</span><span class="sxs-lookup"><span data-stu-id="31a0d-133">Only the user who creates the job or a user with administrator privileges can [add files to the job](https://www.bing.com/search?q=add+files+to+the+job) and [change the job's properties](https://www.bing.com/search?q=change+the+job's+properties).</span></span>

## <a name="requirements"></a><span data-ttu-id="31a0d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="31a0d-134">Requirements</span></span>



| <span data-ttu-id="31a0d-135">需求</span><span class="sxs-lookup"><span data-stu-id="31a0d-135">Requirement</span></span> | <span data-ttu-id="31a0d-136">值</span><span class="sxs-lookup"><span data-stu-id="31a0d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a0d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31a0d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="31a0d-138">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31a0d-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="31a0d-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31a0d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="31a0d-140">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31a0d-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="31a0d-141">標頭</span><span class="sxs-lookup"><span data-stu-id="31a0d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="31a0d-142"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="31a0d-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="31a0d-143">Idl</span><span class="sxs-lookup"><span data-stu-id="31a0d-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31a0d-144"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="31a0d-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="31a0d-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="31a0d-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="31a0d-146"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="31a0d-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="31a0d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="31a0d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31a0d-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31a0d-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="31a0d-149">IID</span><span class="sxs-lookup"><span data-stu-id="31a0d-149">IID</span></span><br/>                      | <span data-ttu-id="31a0d-150">IID_IBackgroundCopyManager 定義為5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="31a0d-150">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="31a0d-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31a0d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a0d-152">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="31a0d-152">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="31a0d-153">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="31a0d-153">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="31a0d-154">**IBackgroundCopyJob：： Resume**</span><span class="sxs-lookup"><span data-stu-id="31a0d-154">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>
