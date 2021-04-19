---
title: 'IBackgroundCopyJob GetId 方法 (>deliveryoptimization .h) '
description: 抓取用來識別佇列中之作業的識別碼。
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId 方法
- GetId 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetId 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106993746"
---
# <a name="ibackgroundcopyjobgetid-method"></a><span data-ttu-id="b5509-106">IBackgroundCopyJob：： GetId 方法</span><span class="sxs-lookup"><span data-stu-id="b5509-106">IBackgroundCopyJob::GetId method</span></span>

<span data-ttu-id="b5509-107">抓取用來識別佇列中之作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5509-107">Retrieves the identifier used to identify the job in the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5509-108">語法</span><span class="sxs-lookup"><span data-stu-id="b5509-108">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a><span data-ttu-id="b5509-109">參數</span><span class="sxs-lookup"><span data-stu-id="b5509-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5509-110">*pJobID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b5509-110">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5509-111">識別 DO 佇列內作業的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b5509-111">GUID that identifies the job within the DO queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5509-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5509-112">Return value</span></span>

<span data-ttu-id="b5509-113">這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b5509-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5509-114">備註</span><span class="sxs-lookup"><span data-stu-id="b5509-114">Remarks</span></span>

<span data-ttu-id="b5509-115">當您 [建立](ibackgroundcopymanager-createjob.md) 作業時，服務會產生識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5509-115">The service generates the identifier when you [create](ibackgroundcopymanager-createjob.md) the job.</span></span> <span data-ttu-id="b5509-116">若要使用識別碼來取得作業的 [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) 介面指標，請呼叫 [**IBackgroundCopyManager：： GetJob**](ibackgroundcopymanager-getjob.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b5509-116">To use the identifier to retrieve an [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer for the job, call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5509-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5509-117">Requirements</span></span>



| <span data-ttu-id="b5509-118">需求</span><span class="sxs-lookup"><span data-stu-id="b5509-118">Requirement</span></span> | <span data-ttu-id="b5509-119">值</span><span class="sxs-lookup"><span data-stu-id="b5509-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5509-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5509-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b5509-121">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5509-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b5509-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5509-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b5509-123">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5509-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b5509-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b5509-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5509-125"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5509-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5509-126">Idl</span><span class="sxs-lookup"><span data-stu-id="b5509-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5509-127"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5509-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b5509-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="b5509-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5509-129"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5509-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b5509-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b5509-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5509-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5509-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b5509-132">IID</span><span class="sxs-lookup"><span data-stu-id="b5509-132">IID</span></span><br/>                      | <span data-ttu-id="b5509-133">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="b5509-133">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b5509-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5509-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5509-135">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="b5509-135">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="b5509-136">**IBackgroundCopyManager：： >batchclient.joboperations.createjob**</span><span class="sxs-lookup"><span data-stu-id="b5509-136">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[<span data-ttu-id="b5509-137">**IBackgroundCopyManager::GetJob**</span><span class="sxs-lookup"><span data-stu-id="b5509-137">**IBackgroundCopyManager::GetJob**</span></span>](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





