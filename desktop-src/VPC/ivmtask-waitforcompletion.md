---
title: 'IVMTask WaitForCompletion 方法 (VPCCOMInterfaces .h) '
description: 等候工作完成或指定的逾時間隔。
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- WaitForCompletion 方法 Virtual PC
- WaitForCompletion 方法 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，WaitForCompletion 方法
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967749"
---
# <a name="ivmtaskwaitforcompletion-method"></a><span data-ttu-id="5581b-106">IVMTask：： WaitForCompletion 方法</span><span class="sxs-lookup"><span data-stu-id="5581b-106">IVMTask::WaitForCompletion method</span></span>

<span data-ttu-id="5581b-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="5581b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5581b-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="5581b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5581b-109">等候工作完成或指定的逾時間隔。</span><span class="sxs-lookup"><span data-stu-id="5581b-109">Waits for the task to complete or for the specified time-out interval to elapse.</span></span>

## <a name="syntax"></a><span data-ttu-id="5581b-110">語法</span><span class="sxs-lookup"><span data-stu-id="5581b-110">Syntax</span></span>


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a><span data-ttu-id="5581b-111">參數</span><span class="sxs-lookup"><span data-stu-id="5581b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5581b-112">*timeout* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5581b-112">*timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5581b-113">這個方法在將控制權傳回給呼叫者之前，會等候工作完成的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5581b-113">The time, in milliseconds, that this method will wait for task completion before returning control to the caller.</span></span> <span data-ttu-id="5581b-114">值為-1 時，會指定方法會等候，直到工作完成而沒有時間。其他有效的超時值範圍從0到4000000毫秒。</span><span class="sxs-lookup"><span data-stu-id="5581b-114">A value of -1 specifies that method will wait until the task completes without timing out. Other valid timeout values range from 0 to 4,000,000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5581b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5581b-115">Return value</span></span>

<span data-ttu-id="5581b-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5581b-116">This method can return one of these values.</span></span>



| <span data-ttu-id="5581b-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="5581b-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="5581b-118">Description</span><span class="sxs-lookup"><span data-stu-id="5581b-118">Description</span></span>                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="5581b-119"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5581b-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5581b-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="5581b-120">The operation was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="5581b-121"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="5581b-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="5581b-122">*Timeout* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="5581b-122">The *timeout* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="5581b-123"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5581b-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5581b-124">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5581b-124">An unexpected error has occurred.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="5581b-125">備註</span><span class="sxs-lookup"><span data-stu-id="5581b-125">Remarks</span></span>

<span data-ttu-id="5581b-126">**WaitForCompletion** 方法會讓目前的執行執行緒進入睡眠狀態，直到它傳回為止。</span><span class="sxs-lookup"><span data-stu-id="5581b-126">The **WaitForCompletion** method puts the current execution thread to sleep until it returns.</span></span> <span data-ttu-id="5581b-127">除非在任何情況下完成工作，否則不建議指定無限等候 (timeout =-1) 。</span><span class="sxs-lookup"><span data-stu-id="5581b-127">Specifying an infinite wait (timeout = -1) is not recommended unless it is absolutely critical that the task completes under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="5581b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="5581b-128">Requirements</span></span>



| <span data-ttu-id="5581b-129">需求</span><span class="sxs-lookup"><span data-stu-id="5581b-129">Requirement</span></span> | <span data-ttu-id="5581b-130">值</span><span class="sxs-lookup"><span data-stu-id="5581b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5581b-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5581b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5581b-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5581b-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5581b-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5581b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5581b-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="5581b-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5581b-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5581b-135">End of client support</span></span><br/>    | <span data-ttu-id="5581b-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5581b-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5581b-137">產品</span><span class="sxs-lookup"><span data-stu-id="5581b-137">Product</span></span><br/>                  | <span data-ttu-id="5581b-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5581b-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5581b-139">標頭</span><span class="sxs-lookup"><span data-stu-id="5581b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5581b-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="5581b-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5581b-141">IID</span><span class="sxs-lookup"><span data-stu-id="5581b-141">IID</span></span><br/>                      | <span data-ttu-id="5581b-142">IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="5581b-142">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="5581b-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5581b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5581b-144">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="5581b-144">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

