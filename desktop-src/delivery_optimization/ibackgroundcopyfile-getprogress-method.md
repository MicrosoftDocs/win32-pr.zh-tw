---
title: 'IBackgroundCopyFile GetProgress 方法 (>deliveryoptimization .h) '
description: 捕獲檔案傳輸進度的資訊。
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- GetProgress 方法
- GetProgress 方法，IBackgroundCopyFile 介面
- IBackgroundCopyFile 介面，GetProgress 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465080"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a><span data-ttu-id="29c22-106">IBackgroundCopyFile：： GetProgress 方法</span><span class="sxs-lookup"><span data-stu-id="29c22-106">IBackgroundCopyFile::GetProgress method</span></span>

<span data-ttu-id="29c22-107">捕獲檔案傳輸進度的資訊。</span><span class="sxs-lookup"><span data-stu-id="29c22-107">Retrieves information on the progress of the file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="29c22-108">語法</span><span class="sxs-lookup"><span data-stu-id="29c22-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="29c22-109">參數</span><span class="sxs-lookup"><span data-stu-id="29c22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29c22-110">*pProgress* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="29c22-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29c22-111">結構，其成員表示檔案傳輸的進度。</span><span class="sxs-lookup"><span data-stu-id="29c22-111">Structure whose members indicate the progress of the file transfer.</span></span> <span data-ttu-id="29c22-112">如需可用進度資訊類型的詳細資訊，請參閱 [**BG_FILE_PROGRESS**](bg-file-progress.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="29c22-112">For details on the type of progress information available, see the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29c22-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="29c22-113">Return value</span></span>

<span data-ttu-id="29c22-114">這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="29c22-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="29c22-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="29c22-115">Requirements</span></span>



| <span data-ttu-id="29c22-116">需求</span><span class="sxs-lookup"><span data-stu-id="29c22-116">Requirement</span></span> | <span data-ttu-id="29c22-117">值</span><span class="sxs-lookup"><span data-stu-id="29c22-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c22-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29c22-118">Minimum supported client</span></span><br/> | <span data-ttu-id="29c22-119">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29c22-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="29c22-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29c22-120">Minimum supported server</span></span><br/> | <span data-ttu-id="29c22-121">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29c22-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="29c22-122">標頭</span><span class="sxs-lookup"><span data-stu-id="29c22-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="29c22-123"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="29c22-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="29c22-124">Idl</span><span class="sxs-lookup"><span data-stu-id="29c22-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="29c22-125"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="29c22-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="29c22-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="29c22-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="29c22-127"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="29c22-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="29c22-128">DLL</span><span class="sxs-lookup"><span data-stu-id="29c22-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29c22-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29c22-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="29c22-130">IID</span><span class="sxs-lookup"><span data-stu-id="29c22-130">IID</span></span><br/>                      | <span data-ttu-id="29c22-131">IID_IBackgroundCopyFile 定義為01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="29c22-131">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="29c22-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29c22-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29c22-133">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="29c22-133">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="29c22-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="29c22-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="29c22-135">**IBackgroundCopyJob：： GetProgress**</span><span class="sxs-lookup"><span data-stu-id="29c22-135">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





