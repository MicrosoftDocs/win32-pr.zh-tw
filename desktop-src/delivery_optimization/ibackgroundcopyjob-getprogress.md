---
title: 'IBackgroundCopyJob GetProgress 方法 (>deliveryoptimization .h) '
description: 抓取作業相關的進度資訊，例如已傳送的位元組和檔案數目。
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- GetProgress 方法
- GetProgress 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetProgress 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d49a040bb5656ae6ef6d926a45b31808623e399b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103955"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a><span data-ttu-id="deb53-106">IBackgroundCopyJob：： GetProgress 方法</span><span class="sxs-lookup"><span data-stu-id="deb53-106">IBackgroundCopyJob::GetProgress method</span></span>

<span data-ttu-id="deb53-107">抓取作業相關的進度資訊，例如已傳送的位元組和檔案數目。</span><span class="sxs-lookup"><span data-stu-id="deb53-107">Retrieves job-related progress information, such as the number of bytes and files transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb53-108">語法</span><span class="sxs-lookup"><span data-stu-id="deb53-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="deb53-109">參數</span><span class="sxs-lookup"><span data-stu-id="deb53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb53-110">*pProgress* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="deb53-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deb53-111">包含可用來計算已完成作業之百分比的資料。</span><span class="sxs-lookup"><span data-stu-id="deb53-111">Contains data that you can use to calculate the percentage of the job that is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb53-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="deb53-112">Return value</span></span>

<span data-ttu-id="deb53-113">這個方法會傳回下列 **HRESULT** 值，以及其他值。</span><span class="sxs-lookup"><span data-stu-id="deb53-113">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="deb53-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="deb53-114">Return code</span></span>                                                                              | <span data-ttu-id="deb53-115">Description</span><span class="sxs-lookup"><span data-stu-id="deb53-115">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="deb53-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="deb53-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="deb53-117">成功取回進度資訊。</span><span class="sxs-lookup"><span data-stu-id="deb53-117">Progress information was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="deb53-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="deb53-118">Requirements</span></span>



| <span data-ttu-id="deb53-119">需求</span><span class="sxs-lookup"><span data-stu-id="deb53-119">Requirement</span></span> | <span data-ttu-id="deb53-120">值</span><span class="sxs-lookup"><span data-stu-id="deb53-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deb53-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="deb53-121">Minimum supported client</span></span><br/> | <span data-ttu-id="deb53-122">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="deb53-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="deb53-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="deb53-123">Minimum supported server</span></span><br/> | <span data-ttu-id="deb53-124">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="deb53-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="deb53-125">標頭</span><span class="sxs-lookup"><span data-stu-id="deb53-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="deb53-126"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="deb53-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="deb53-127">Idl</span><span class="sxs-lookup"><span data-stu-id="deb53-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="deb53-128"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="deb53-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="deb53-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="deb53-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="deb53-130"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="deb53-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="deb53-131">DLL</span><span class="sxs-lookup"><span data-stu-id="deb53-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deb53-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deb53-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="deb53-133">IID</span><span class="sxs-lookup"><span data-stu-id="deb53-133">IID</span></span><br/>                      | <span data-ttu-id="deb53-134">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="deb53-134">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="deb53-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="deb53-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb53-136">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="deb53-136">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





