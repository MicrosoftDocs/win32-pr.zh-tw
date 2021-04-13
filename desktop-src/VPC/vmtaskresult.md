---
title: 'VMTaskResult 列舉 (VPCCOMInterfaces) '
description: 指定工作的結果。
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- VMTaskResult 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903425ca8036e1862df7042f16946fc0f2e9cc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509328"
---
# <a name="vmtaskresult-enumeration"></a><span data-ttu-id="04d42-104">VMTaskResult 列舉</span><span class="sxs-lookup"><span data-stu-id="04d42-104">VMTaskResult enumeration</span></span>

<span data-ttu-id="04d42-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="04d42-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="04d42-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="04d42-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="04d42-107">指定工作的結果。</span><span class="sxs-lookup"><span data-stu-id="04d42-107">Specifies the result of a task.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d42-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="04d42-108">Syntax</span></span>


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a><span data-ttu-id="04d42-109">常數</span><span class="sxs-lookup"><span data-stu-id="04d42-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="04d42-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult \_ 成功**</span><span class="sxs-lookup"><span data-stu-id="04d42-110"><span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult\_Success**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-111">工作成功。</span><span class="sxs-lookup"><span data-stu-id="04d42-111">The task was successful.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult 已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="04d42-112"><span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult\_Cancelled**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-113">工作已取消。</span><span class="sxs-lookup"><span data-stu-id="04d42-113">The task was canceled.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult \_ UnexpectedError**</span><span class="sxs-lookup"><span data-stu-id="04d42-114"><span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult\_UnexpectedError**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-115">工作發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="04d42-115">The task had an unexpected error.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult \_ OutOfMemoryError**</span><span class="sxs-lookup"><span data-stu-id="04d42-116"><span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult\_OutOfMemoryError**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-117">沒有足夠的記憶體可完成工作。</span><span class="sxs-lookup"><span data-stu-id="04d42-117">There was not enough memory for the task to complete.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult \_ DiskRelatedError**</span><span class="sxs-lookup"><span data-stu-id="04d42-118"><span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult\_DiskRelatedError**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-119">工作寫入磁片時發生錯誤 (請確定有足夠的磁碟空間) 。</span><span class="sxs-lookup"><span data-stu-id="04d42-119">The task had an error while writing to disk (make sure there is enough disk space).</span></span>

</dd> <dt>

<span data-ttu-id="04d42-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult \_ IncompatibleSavedStateError**</span><span class="sxs-lookup"><span data-stu-id="04d42-120"><span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult\_IncompatibleSavedStateError**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-121">因為儲存的狀態不相容，所以無法還原虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="04d42-121">The virtual machine could not restore because the saved state was incompatible.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult \_ >timeouterror**</span><span class="sxs-lookup"><span data-stu-id="04d42-122"><span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult\_TimeOutError**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-123">工作已超時。</span><span class="sxs-lookup"><span data-stu-id="04d42-123">The task timed out.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult \_ IllegalValueError**</span><span class="sxs-lookup"><span data-stu-id="04d42-124"><span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult\_IllegalValueError**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-125">工作處理時讀取了不合法的喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="04d42-125">An illegal preference value was read while the task was processing.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult \_ ThreadCrashError**</span><span class="sxs-lookup"><span data-stu-id="04d42-126"><span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult\_ThreadCrashError**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-127">與工作相關聯的執行緒已損毀。</span><span class="sxs-lookup"><span data-stu-id="04d42-127">A thread associated with the task crashed.</span></span>

</dd> <dt>

<span data-ttu-id="04d42-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult \_ ShutdownAbort**</span><span class="sxs-lookup"><span data-stu-id="04d42-128"><span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult\_ShutdownAbort**</span></span>
</dt> <dd>

<span data-ttu-id="04d42-129">要求的關機已中止。</span><span class="sxs-lookup"><span data-stu-id="04d42-129">The shutdown requested was aborted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04d42-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="04d42-130">Requirements</span></span>



| <span data-ttu-id="04d42-131">需求</span><span class="sxs-lookup"><span data-stu-id="04d42-131">Requirement</span></span> | <span data-ttu-id="04d42-132">值</span><span class="sxs-lookup"><span data-stu-id="04d42-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d42-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04d42-133">Minimum supported client</span></span><br/> | <span data-ttu-id="04d42-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04d42-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04d42-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04d42-135">Minimum supported server</span></span><br/> | <span data-ttu-id="04d42-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="04d42-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="04d42-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="04d42-137">End of client support</span></span><br/>    | <span data-ttu-id="04d42-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04d42-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="04d42-139">產品</span><span class="sxs-lookup"><span data-stu-id="04d42-139">Product</span></span><br/>                  | <span data-ttu-id="04d42-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="04d42-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="04d42-141">標頭</span><span class="sxs-lookup"><span data-stu-id="04d42-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="04d42-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="04d42-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d42-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04d42-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d42-144">**IVMTask：： Result**</span><span class="sxs-lookup"><span data-stu-id="04d42-144">**IVMTask::Result**</span></span>](ivmtask-result.md)
</dt> </dl>

 

