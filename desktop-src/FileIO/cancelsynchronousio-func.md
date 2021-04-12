---
description: 將指定之執行緒所發出的暫止同步 i/o 作業標示為已取消。
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: 'CancelSynchronousIo 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513997"
---
# <a name="cancelsynchronousio-function"></a><span data-ttu-id="5427b-103">CancelSynchronousIo 函式</span><span class="sxs-lookup"><span data-stu-id="5427b-103">CancelSynchronousIo function</span></span>

<span data-ttu-id="5427b-104">將指定之執行緒所發出的暫止同步 i/o 作業標示為已取消。</span><span class="sxs-lookup"><span data-stu-id="5427b-104">Marks pending synchronous I/O operations that are issued by the specified thread as canceled.</span></span>

## <a name="syntax"></a><span data-ttu-id="5427b-105">語法</span><span class="sxs-lookup"><span data-stu-id="5427b-105">Syntax</span></span>


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a><span data-ttu-id="5427b-106">參數</span><span class="sxs-lookup"><span data-stu-id="5427b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5427b-107">*hThread* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5427b-107">*hThread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5427b-108">執行緒的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5427b-108">A handle to the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5427b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5427b-109">Return value</span></span>

<span data-ttu-id="5427b-110">如果函式成功，則傳回非零的值。</span><span class="sxs-lookup"><span data-stu-id="5427b-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="5427b-111">如果函式失敗，則傳回值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5427b-111">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="5427b-112">若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。</span><span class="sxs-lookup"><span data-stu-id="5427b-112">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="5427b-113">如果此函式找不到要取消的要求，則傳回值為 0 (零) ，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 則找 **不到錯誤 \_ \_**。</span><span class="sxs-lookup"><span data-stu-id="5427b-113">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5427b-114">備註</span><span class="sxs-lookup"><span data-stu-id="5427b-114">Remarks</span></span>

<span data-ttu-id="5427b-115">呼叫端必須讓 [執行緒 \_ 終止](/windows/desktop/ProcThread/thread-security-and-access-rights) 存取權。</span><span class="sxs-lookup"><span data-stu-id="5427b-115">The caller must have the [THREAD\_TERMINATE](/windows/desktop/ProcThread/thread-security-and-access-rights) access right.</span></span>

<span data-ttu-id="5427b-116">如果指定的執行緒有任何正在進行的暫止 i/o 作業， **CancelSynchronousIo** 函式會將它們標示為取消。</span><span class="sxs-lookup"><span data-stu-id="5427b-116">If there are any pending I/O operations in progress for the specified thread, the **CancelSynchronousIo** function marks them for cancellation.</span></span> <span data-ttu-id="5427b-117">大部分的作業類型都可以立即取消;其他作業可能會在實際取消之前繼續完成，並通知呼叫者。</span><span class="sxs-lookup"><span data-stu-id="5427b-117">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="5427b-118">**CancelSynchronousIo** 函數不會等候所有已取消的作業完成。</span><span class="sxs-lookup"><span data-stu-id="5427b-118">The **CancelSynchronousIo** function does not wait for all canceled operations to complete.</span></span> <span data-ttu-id="5427b-119">如需詳細資訊，請參閱 [I/o 完成/取消指導方針](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)。</span><span class="sxs-lookup"><span data-stu-id="5427b-119">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

<span data-ttu-id="5427b-120">正在取消的作業會以三個狀態之一完成：您必須檢查完成狀態以判斷完成狀態。</span><span class="sxs-lookup"><span data-stu-id="5427b-120">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="5427b-121">有三種狀態：</span><span class="sxs-lookup"><span data-stu-id="5427b-121">The three statuses are:</span></span>

-   <span data-ttu-id="5427b-122">**作業正常完成。**</span><span class="sxs-lookup"><span data-stu-id="5427b-122">**The operation completed normally.**</span></span> <span data-ttu-id="5427b-123">即使作業已取消，也可能會發生這種情況，因為取消要求可能尚未及時提交來取消作業。</span><span class="sxs-lookup"><span data-stu-id="5427b-123">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="5427b-124">**已取消作業。**</span><span class="sxs-lookup"><span data-stu-id="5427b-124">**The operation was canceled.**</span></span> <span data-ttu-id="5427b-125">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數傳回錯誤作業已 **\_ \_ 中止**。</span><span class="sxs-lookup"><span data-stu-id="5427b-125">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="5427b-126">**作業失敗，發生另一個錯誤。**</span><span class="sxs-lookup"><span data-stu-id="5427b-126">**The operation failed with another error.**</span></span> <span data-ttu-id="5427b-127">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數會傳回相關的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5427b-127">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="5427b-128">在 Windows 8 和 Windows Server 2012 中，下列技術支援此功能。</span><span class="sxs-lookup"><span data-stu-id="5427b-128">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="5427b-129">技術</span><span class="sxs-lookup"><span data-stu-id="5427b-129">Technology</span></span>                                           | <span data-ttu-id="5427b-130">支援</span><span class="sxs-lookup"><span data-stu-id="5427b-130">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="5427b-131">伺服器訊息區 (SMB) 3.0 通訊協定</span><span class="sxs-lookup"><span data-stu-id="5427b-131">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="5427b-132">Yes</span><span class="sxs-lookup"><span data-stu-id="5427b-132">Yes</span></span><br/> |
| <span data-ttu-id="5427b-133">SMB 3.0 透明容錯移轉 (TFO) </span><span class="sxs-lookup"><span data-stu-id="5427b-133">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="5427b-134">Yes</span><span class="sxs-lookup"><span data-stu-id="5427b-134">Yes</span></span><br/> |
| <span data-ttu-id="5427b-135">具有向外延展檔案共用的 SMB 3.0 (因此) </span><span class="sxs-lookup"><span data-stu-id="5427b-135">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="5427b-136">Yes</span><span class="sxs-lookup"><span data-stu-id="5427b-136">Yes</span></span><br/> |
| <span data-ttu-id="5427b-137">叢集共用磁碟區檔案系統 (CsvFS) </span><span class="sxs-lookup"><span data-stu-id="5427b-137">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="5427b-138">Yes</span><span class="sxs-lookup"><span data-stu-id="5427b-138">Yes</span></span><br/> |
| <span data-ttu-id="5427b-139">彈性檔案系統 (ReFS)</span><span class="sxs-lookup"><span data-stu-id="5427b-139">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="5427b-140">Yes</span><span class="sxs-lookup"><span data-stu-id="5427b-140">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5427b-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="5427b-141">Requirements</span></span>



| <span data-ttu-id="5427b-142">需求</span><span class="sxs-lookup"><span data-stu-id="5427b-142">Requirement</span></span> | <span data-ttu-id="5427b-143">值</span><span class="sxs-lookup"><span data-stu-id="5427b-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5427b-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5427b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5427b-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5427b-145">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                          |
| <span data-ttu-id="5427b-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5427b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5427b-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5427b-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="5427b-148">標頭</span><span class="sxs-lookup"><span data-stu-id="5427b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="5427b-149"><dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、windows 7、Windows Server 2008 和 Windows Vista (的 WinBase，包括 windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5427b-149"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5427b-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="5427b-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="5427b-151"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5427b-151"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="5427b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="5427b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5427b-153"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5427b-153"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="5427b-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5427b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5427b-155">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="5427b-155">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="5427b-156">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="5427b-156">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="5427b-157">檔案管理功能</span><span class="sxs-lookup"><span data-stu-id="5427b-157">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="5427b-158">同步和非同步 i/o</span><span class="sxs-lookup"><span data-stu-id="5427b-158">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

