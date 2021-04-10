---
title: 'IBackgroundCopyJob EnumFiles 方法 (>deliveryoptimization .h) '
description: 抓取 IEnumBackgroundCopyFiles 介面指標，您可用來列舉作業中的檔案。
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- EnumFiles 方法
- EnumFiles 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，EnumFiles 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104075"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a><span data-ttu-id="af446-106">IBackgroundCopyJob：： EnumFiles 方法</span><span class="sxs-lookup"><span data-stu-id="af446-106">IBackgroundCopyJob::EnumFiles method</span></span>

<span data-ttu-id="af446-107">抓取 [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) 介面指標，您可用來列舉作業中的檔案。</span><span class="sxs-lookup"><span data-stu-id="af446-107">Retrieves an [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="af446-108">語法</span><span class="sxs-lookup"><span data-stu-id="af446-108">Syntax</span></span>


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a><span data-ttu-id="af446-109">參數</span><span class="sxs-lookup"><span data-stu-id="af446-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af446-110">*ppEnumFiles* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="af446-110">*ppEnumFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af446-111">[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) 介面指標，用來列舉作業中的檔案。</span><span class="sxs-lookup"><span data-stu-id="af446-111">[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in the job.</span></span> <span data-ttu-id="af446-112">完成時釋放 *ppEnumFiles* 。</span><span class="sxs-lookup"><span data-stu-id="af446-112">Release *ppEnumFiles* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af446-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="af446-113">Return value</span></span>

<span data-ttu-id="af446-114">這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="af446-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="af446-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="af446-115">Requirements</span></span>



| <span data-ttu-id="af446-116">需求</span><span class="sxs-lookup"><span data-stu-id="af446-116">Requirement</span></span> | <span data-ttu-id="af446-117">值</span><span class="sxs-lookup"><span data-stu-id="af446-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af446-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af446-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af446-119">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af446-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="af446-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af446-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af446-121">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af446-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="af446-122">標頭</span><span class="sxs-lookup"><span data-stu-id="af446-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af446-123"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="af446-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="af446-124">Idl</span><span class="sxs-lookup"><span data-stu-id="af446-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af446-125"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="af446-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="af446-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="af446-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="af446-127"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="af446-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="af446-128">DLL</span><span class="sxs-lookup"><span data-stu-id="af446-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af446-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af446-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="af446-130">IID</span><span class="sxs-lookup"><span data-stu-id="af446-130">IID</span></span><br/>                      | <span data-ttu-id="af446-131">IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="af446-131">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="af446-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af446-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af446-133">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="af446-133">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="af446-134">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="af446-134">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





