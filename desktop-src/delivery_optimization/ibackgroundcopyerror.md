---
title: 'IBackgroundCopyError 介面 (>deliveryoptimization .h) '
description: 使用 IBackgroundCopyError 介面判斷錯誤的原因，以及傳輸程式是否可繼續。
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- IBackgroundCopyError 介面
- IBackgroundCopyError 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465077"
---
# <a name="ibackgroundcopyerror-interface"></a><span data-ttu-id="58916-105">IBackgroundCopyError 介面</span><span class="sxs-lookup"><span data-stu-id="58916-105">IBackgroundCopyError interface</span></span>

<span data-ttu-id="58916-106">使用 **IBackgroundCopyError** 介面判斷錯誤的原因，以及傳輸程式是否可繼續。</span><span class="sxs-lookup"><span data-stu-id="58916-106">Use the **IBackgroundCopyError** interface to determine the cause of an error and if the transfer process can proceed.</span></span>

<span data-ttu-id="58916-107">只有當工作的狀態是 BG_JOB_STATE_ERROR 或 BG_JOB_STATE_TRANSIENT_ERROR 時，才會建立錯誤物件。</span><span class="sxs-lookup"><span data-stu-id="58916-107">DO creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="58916-108">當 **IBackgroundCopyXXXX** 介面方法失敗時，請勿建立 error 物件。</span><span class="sxs-lookup"><span data-stu-id="58916-108">DO does not create an error object when an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="58916-109">在開始傳輸資料 (工作的狀態變更為 BG_JOB_STATE_TRANSFERRING) 時，就可以使用 error 物件。</span><span class="sxs-lookup"><span data-stu-id="58916-109">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job.</span></span>

<span data-ttu-id="58916-110">若要取得 **IBackgroundCopyError** 物件，請呼叫 [**IBackgroundCopyJob：： GetError**](ibackgroundcopyjob-geterror.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="58916-110">To get an **IBackgroundCopyError** object, call the [**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="58916-111">成員</span><span class="sxs-lookup"><span data-stu-id="58916-111">Members</span></span>

<span data-ttu-id="58916-112">**IBackgroundCopyError** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="58916-112">The **IBackgroundCopyError** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="58916-113">**IBackgroundCopyError** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="58916-113">**IBackgroundCopyError** also has these types of members:</span></span>

-   [<span data-ttu-id="58916-114">方法</span><span class="sxs-lookup"><span data-stu-id="58916-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="58916-115">方法</span><span class="sxs-lookup"><span data-stu-id="58916-115">Methods</span></span>

<span data-ttu-id="58916-116">**IBackgroundCopyError** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="58916-116">The **IBackgroundCopyError** interface has these methods.</span></span>



| <span data-ttu-id="58916-117">方法</span><span class="sxs-lookup"><span data-stu-id="58916-117">Method</span></span>                                                   | <span data-ttu-id="58916-118">描述</span><span class="sxs-lookup"><span data-stu-id="58916-118">Description</span></span>                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58916-119">**GetError**</span><span class="sxs-lookup"><span data-stu-id="58916-119">**GetError**</span></span>](ibackgroundcopyerror-geterror-method.md) | <span data-ttu-id="58916-120">捕獲錯誤碼，並識別發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="58916-120">Retrieves the error code and identifies the context in which the error occurred.</span></span><br/> |
| [<span data-ttu-id="58916-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="58916-121">**GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)   | <span data-ttu-id="58916-122">捕獲與錯誤相關聯之檔案物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="58916-122">Retrieves an interface pointer to the file object associated with the error.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="58916-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="58916-123">Requirements</span></span>



| <span data-ttu-id="58916-124">需求</span><span class="sxs-lookup"><span data-stu-id="58916-124">Requirement</span></span> | <span data-ttu-id="58916-125">值</span><span class="sxs-lookup"><span data-stu-id="58916-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58916-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58916-126">Minimum supported client</span></span><br/> | <span data-ttu-id="58916-127">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58916-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="58916-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58916-128">Minimum supported server</span></span><br/> | <span data-ttu-id="58916-129">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58916-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="58916-130">標頭</span><span class="sxs-lookup"><span data-stu-id="58916-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="58916-131"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="58916-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="58916-132">Idl</span><span class="sxs-lookup"><span data-stu-id="58916-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="58916-133"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="58916-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="58916-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="58916-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="58916-135"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="58916-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="58916-136">DLL</span><span class="sxs-lookup"><span data-stu-id="58916-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58916-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58916-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="58916-138">IID</span><span class="sxs-lookup"><span data-stu-id="58916-138">IID</span></span><br/>                      | <span data-ttu-id="58916-139">IID_IBackgroundCopyError 定義為19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="58916-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="58916-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58916-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58916-141">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="58916-141">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="58916-142">**IBackgroundCopyJob::GetError**</span><span class="sxs-lookup"><span data-stu-id="58916-142">**IBackgroundCopyJob::GetError**</span></span>](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[<span data-ttu-id="58916-143">**IBackgroundCopyJob：： >getstate**</span><span class="sxs-lookup"><span data-stu-id="58916-143">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[<span data-ttu-id="58916-144">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="58916-144">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

