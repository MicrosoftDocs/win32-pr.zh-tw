---
title: 'IBackgroundCopyFile2 SetRemoteName 方法 (>deliveryoptimization .h) '
description: 在下載作業中，將遠端名稱變更為新的 URL。
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- SetRemoteName 方法
- SetRemoteName 方法，IBackgroundCopyFile2 介面
- IBackgroundCopyFile2 介面，SetRemoteName 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465073"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a><span data-ttu-id="2bab0-106">IBackgroundCopyFile2：： SetRemoteName 方法</span><span class="sxs-lookup"><span data-stu-id="2bab0-106">IBackgroundCopyFile2::SetRemoteName method</span></span>

<span data-ttu-id="2bab0-107">在下載作業中，將遠端名稱變更為新的 URL。</span><span class="sxs-lookup"><span data-stu-id="2bab0-107">Changes the remote name to a new URL in a download job.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bab0-108">語法</span><span class="sxs-lookup"><span data-stu-id="2bab0-108">Syntax</span></span>


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a><span data-ttu-id="2bab0-109">參數</span><span class="sxs-lookup"><span data-stu-id="2bab0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bab0-110">*RemoteName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2bab0-110">*RemoteName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bab0-111">以 Null 終止的字串，其中包含伺服器上的檔案名。</span><span class="sxs-lookup"><span data-stu-id="2bab0-111">Null-terminated string that contains the name of the file on the server.</span></span> <span data-ttu-id="2bab0-112">如需指定遠端名稱的詳細資訊，請參閱 **RemoteName** 成員。</span><span class="sxs-lookup"><span data-stu-id="2bab0-112">For information on specifying the remote name, see the **RemoteName** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bab0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2bab0-113">Return value</span></span>

<span data-ttu-id="2bab0-114">這個方法會傳回下列傳回值以及其他值。</span><span class="sxs-lookup"><span data-stu-id="2bab0-114">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="2bab0-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2bab0-115">Return code</span></span>                                                                                  | <span data-ttu-id="2bab0-116">Description</span><span class="sxs-lookup"><span data-stu-id="2bab0-116">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2bab0-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="2bab0-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="2bab0-118">Success</span><span class="sxs-lookup"><span data-stu-id="2bab0-118">Success</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="2bab0-119"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2bab0-119"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2bab0-120">新的遠端名稱是不正確 URL，或新的 URL 太長 (URL) 不能超過2200個字元。</span><span class="sxs-lookup"><span data-stu-id="2bab0-120">The new remote name is an invalid URL or the new URL is too long (the URL cannot exceed 2,200 characters).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2bab0-121">備註</span><span class="sxs-lookup"><span data-stu-id="2bab0-121">Remarks</span></span>

<span data-ttu-id="2bab0-122">一般來說，如果您想要變更用來傳送檔案的 URL，或想要變更檔案名或路徑，則可以呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2bab0-122">Typically, you call this method if you want to change the URL used to transfer the file or if you want to change the file name or path.</span></span>

<span data-ttu-id="2bab0-123">當這個方法傳回時，不會序列化。</span><span class="sxs-lookup"><span data-stu-id="2bab0-123">This method does not serialize when it returns.</span></span> <span data-ttu-id="2bab0-124">若要將變更序列化，請 [**暫停**](ibackgroundcopyjob-suspend.md) 作業、呼叫這個方法 (如果變更作業中的多個檔案，請使用迴圈) ，然後 [**繼續**](ibackgroundcopyjob-resume.md) 工作。</span><span class="sxs-lookup"><span data-stu-id="2bab0-124">To serialize the change, [**suspend**](ibackgroundcopyjob-suspend.md) the job, call this method (if changing multiple files in the job, use a loop), and [**resume**](ibackgroundcopyjob-resume.md) the job.</span></span> <span data-ttu-id="2bab0-125">呼叫 **IBackgroundCopyJob：： Resume** 方法會序列化變更。</span><span class="sxs-lookup"><span data-stu-id="2bab0-125">Calling the **IBackgroundCopyJob::Resume** method serializes the change.</span></span>

<span data-ttu-id="2bab0-126">如果新遠端名稱的時間戳記或檔案大小與先前的遠端名稱不同，或新伺服器不支援 HTTP 遠端名稱) 的檢查點繼續 (，請重新開機下載。</span><span class="sxs-lookup"><span data-stu-id="2bab0-126">If the time stamp or file size of the new remote name is different from the previous remote name or the new server does not support checkpoint resume (for HTTP remote names), DO restarts the download.</span></span> <span data-ttu-id="2bab0-127">否則，就會從新伺服器上的相同位置繼續轉移。</span><span class="sxs-lookup"><span data-stu-id="2bab0-127">Otherwise, the transfer resumes from the same position on the new server.</span></span> <span data-ttu-id="2bab0-128">請勿重新開機已傳送的檔案。</span><span class="sxs-lookup"><span data-stu-id="2bab0-128">DO does not restart already transferred files.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bab0-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bab0-129">Requirements</span></span>



| <span data-ttu-id="2bab0-130">需求</span><span class="sxs-lookup"><span data-stu-id="2bab0-130">Requirement</span></span> | <span data-ttu-id="2bab0-131">值</span><span class="sxs-lookup"><span data-stu-id="2bab0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bab0-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bab0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2bab0-133">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bab0-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2bab0-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bab0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2bab0-135">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bab0-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2bab0-136">標頭</span><span class="sxs-lookup"><span data-stu-id="2bab0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bab0-137"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bab0-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2bab0-138">Idl</span><span class="sxs-lookup"><span data-stu-id="2bab0-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bab0-139"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bab0-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2bab0-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="2bab0-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="2bab0-141"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bab0-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2bab0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2bab0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bab0-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bab0-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2bab0-144">IID</span><span class="sxs-lookup"><span data-stu-id="2bab0-144">IID</span></span><br/>                      | <span data-ttu-id="2bab0-145">IID_IBackgroundCopyFile2 定義為83e81b93-0873-474d-8a8c-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="2bab0-145">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2bab0-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bab0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bab0-147">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="2bab0-147">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





