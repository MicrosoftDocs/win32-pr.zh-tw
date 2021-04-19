---
description: 標示指定檔案控制代碼的任何未完成 i/o 作業。 此函式只會取消目前進程中的 i/o 作業，不論哪一個執行緒建立了 i/o 作業。
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: 'CancelIoEx 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976853"
---
# <a name="cancelioex-function"></a><span data-ttu-id="5de8a-104">CancelIoEx 函式</span><span class="sxs-lookup"><span data-stu-id="5de8a-104">CancelIoEx function</span></span>

<span data-ttu-id="5de8a-105">標示指定檔案控制代碼的任何未完成 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="5de8a-105">Marks any outstanding I/O operations for the specified file handle.</span></span> <span data-ttu-id="5de8a-106">此函式只會取消目前進程中的 i/o 作業，不論哪一個執行緒建立了 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="5de8a-106">The function only cancels I/O operations in the current process, regardless of which thread created the I/O operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de8a-107">語法</span><span class="sxs-lookup"><span data-stu-id="5de8a-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="5de8a-108">參數</span><span class="sxs-lookup"><span data-stu-id="5de8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de8a-109">*hFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5de8a-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5de8a-110">檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5de8a-110">A handle to the file.</span></span>

</dd> <dt>

<span data-ttu-id="5de8a-111">*lpOverlapped* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="5de8a-111">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5de8a-112">重迭資料結構的指標，其中包含用於非同步 i/o [**的資料。**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)</span><span class="sxs-lookup"><span data-stu-id="5de8a-112">A pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) data structure that contains the data used for asynchronous I/O.</span></span>

<span data-ttu-id="5de8a-113">如果這個參數是 **Null**，就會取消 *hFile* 參數的所有 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="5de8a-113">If this parameter is **NULL**, all I/O requests for the *hFile* parameter are canceled.</span></span>

<span data-ttu-id="5de8a-114">如果這個參數不是 **Null**，則只會將針對具有指定 *lpOverlapped* 重迭結構的檔案發出的特定 i/o 要求標示為已取消，這表示您可以取消一個或多個要求，而 [**CancelIo**](cancelio.md) 函式會取消檔案控制代碼上所有未處理的要求。</span><span class="sxs-lookup"><span data-stu-id="5de8a-114">If this parameter is not **NULL**, only those specific I/O requests that were issued for the file with the specified *lpOverlapped* overlapped structure are marked as canceled, meaning that you can cancel one or more requests, while the [**CancelIo**](cancelio.md) function cancels all outstanding requests on a file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de8a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5de8a-115">Return value</span></span>

<span data-ttu-id="5de8a-116">如果函式成功，則傳回非零的值。</span><span class="sxs-lookup"><span data-stu-id="5de8a-116">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="5de8a-117">已成功要求指定檔案控制代碼之呼叫進程發出的所有暫止 i/o 作業的取消作業。</span><span class="sxs-lookup"><span data-stu-id="5de8a-117">The cancel operation for all pending I/O operations issued by the calling process for the specified file handle was successfully requested.</span></span> <span data-ttu-id="5de8a-118">應用程式不能釋放或重複使用 [**與已**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 取消之 i/o 作業相關聯的重迭結構，直到它們完成為止。</span><span class="sxs-lookup"><span data-stu-id="5de8a-118">The application must not free or reuse the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the canceled I/O operations until they have completed.</span></span> <span data-ttu-id="5de8a-119">執行緒可以使用 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來判斷 i/o 作業本身何時完成。</span><span class="sxs-lookup"><span data-stu-id="5de8a-119">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="5de8a-120">如果函式失敗，則傳回值為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5de8a-120">If the function fails, the return value is 0 (zero).</span></span> <span data-ttu-id="5de8a-121">若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。</span><span class="sxs-lookup"><span data-stu-id="5de8a-121">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="5de8a-122">如果此函式找不到要取消的要求，則傳回值為 0 (零) ，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 則找 **不到錯誤 \_ \_**。</span><span class="sxs-lookup"><span data-stu-id="5de8a-122">If this function cannot find a request to cancel, the return value is 0 (zero), and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_NOT\_FOUND**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5de8a-123">備註</span><span class="sxs-lookup"><span data-stu-id="5de8a-123">Remarks</span></span>

<span data-ttu-id="5de8a-124">**CancelIoEx** 函數可讓您取消呼叫執行緒以外線程中的要求。</span><span class="sxs-lookup"><span data-stu-id="5de8a-124">The **CancelIoEx** function allows you to cancel requests in threads other than the calling thread.</span></span> <span data-ttu-id="5de8a-125">[**CancelIo**](cancelio.md)函式只會取消呼叫 **CancelIo** 函式之相同執行緒中的要求。</span><span class="sxs-lookup"><span data-stu-id="5de8a-125">The [**CancelIo**](cancelio.md) function only cancels requests in the same thread that called the **CancelIo** function.</span></span> <span data-ttu-id="5de8a-126">**CancelIoEx** 只會取消控制碼上的未處理 i/o，而不會變更控制碼的狀態。這表示您無法依賴控制碼的狀態，因為您無法得知作業是否已順利完成或取消。</span><span class="sxs-lookup"><span data-stu-id="5de8a-126">**CancelIoEx** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="5de8a-127">如果指定的檔案控制代碼有任何正在進行的暫止 i/o 作業， **CancelIoEx** 函式會將它們標示為取消。</span><span class="sxs-lookup"><span data-stu-id="5de8a-127">If there are any pending I/O operations in progress for the specified file handle, the **CancelIoEx** function marks them for cancellation.</span></span> <span data-ttu-id="5de8a-128">大部分的作業類型都可以立即取消;其他作業可能會在實際取消之前繼續完成，並通知呼叫者。</span><span class="sxs-lookup"><span data-stu-id="5de8a-128">Most types of operations can be canceled immediately; other operations can continue toward completion before they are actually canceled and the caller is notified.</span></span> <span data-ttu-id="5de8a-129">**CancelIoEx** 函數不會等候所有已取消的作業完成。</span><span class="sxs-lookup"><span data-stu-id="5de8a-129">The **CancelIoEx** function does not wait for all canceled operations to complete.</span></span>

<span data-ttu-id="5de8a-130">如果檔案控制代碼與完成埠相關聯，且已成功取消同步作業，i/o 完成封包就不會排入埠佇列中。</span><span class="sxs-lookup"><span data-stu-id="5de8a-130">If the file handle is associated with a completion port, an I/O completion packet is not queued to the port if a synchronous operation is successfully canceled.</span></span> <span data-ttu-id="5de8a-131">如果非同步作業仍在擱置中，取消作業將會將 i/o 完成封包排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="5de8a-131">For asynchronous operations still pending, the cancel operation will queue an I/O completion packet.</span></span>

<span data-ttu-id="5de8a-132">正在取消的作業會以三個狀態之一完成：您必須檢查完成狀態以判斷完成狀態。</span><span class="sxs-lookup"><span data-stu-id="5de8a-132">The operation being canceled is completed with one of three statuses; you must check the completion status to determine the completion state.</span></span> <span data-ttu-id="5de8a-133">有三種狀態：</span><span class="sxs-lookup"><span data-stu-id="5de8a-133">The three statuses are:</span></span>

-   <span data-ttu-id="5de8a-134">作業正常完成。</span><span class="sxs-lookup"><span data-stu-id="5de8a-134">The operation completed normally.</span></span> <span data-ttu-id="5de8a-135">即使作業已取消，也可能會發生這種情況，因為取消要求可能尚未及時提交來取消作業。</span><span class="sxs-lookup"><span data-stu-id="5de8a-135">This can occur even if the operation was canceled, because the cancel request might not have been submitted in time to cancel the operation.</span></span>
-   <span data-ttu-id="5de8a-136">已取消作業。</span><span class="sxs-lookup"><span data-stu-id="5de8a-136">The operation was canceled.</span></span> <span data-ttu-id="5de8a-137">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數傳回錯誤作業已 **\_ \_ 中止**。</span><span class="sxs-lookup"><span data-stu-id="5de8a-137">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_OPERATION\_ABORTED**.</span></span>
-   <span data-ttu-id="5de8a-138">作業失敗，發生另一個錯誤。</span><span class="sxs-lookup"><span data-stu-id="5de8a-138">The operation failed with another error.</span></span> <span data-ttu-id="5de8a-139">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數會傳回相關的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5de8a-139">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns the relevant error code.</span></span>

<span data-ttu-id="5de8a-140">在 Windows 8 和 Windows Server 2012 中，下列技術支援此功能。</span><span class="sxs-lookup"><span data-stu-id="5de8a-140">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="5de8a-141">技術</span><span class="sxs-lookup"><span data-stu-id="5de8a-141">Technology</span></span>                                           | <span data-ttu-id="5de8a-142">支援</span><span class="sxs-lookup"><span data-stu-id="5de8a-142">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="5de8a-143">伺服器訊息區 (SMB) 3.0 通訊協定</span><span class="sxs-lookup"><span data-stu-id="5de8a-143">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="5de8a-144">Yes</span><span class="sxs-lookup"><span data-stu-id="5de8a-144">Yes</span></span><br/> |
| <span data-ttu-id="5de8a-145">SMB 3.0 透明容錯移轉 (TFO) </span><span class="sxs-lookup"><span data-stu-id="5de8a-145">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="5de8a-146">Yes</span><span class="sxs-lookup"><span data-stu-id="5de8a-146">Yes</span></span><br/> |
| <span data-ttu-id="5de8a-147">具有向外延展檔案共用的 SMB 3.0 (因此) </span><span class="sxs-lookup"><span data-stu-id="5de8a-147">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="5de8a-148">Yes</span><span class="sxs-lookup"><span data-stu-id="5de8a-148">Yes</span></span><br/> |
| <span data-ttu-id="5de8a-149">叢集共用磁碟區檔案系統 (CsvFS) </span><span class="sxs-lookup"><span data-stu-id="5de8a-149">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="5de8a-150">Yes</span><span class="sxs-lookup"><span data-stu-id="5de8a-150">Yes</span></span><br/> |
| <span data-ttu-id="5de8a-151">彈性檔案系統 (ReFS)</span><span class="sxs-lookup"><span data-stu-id="5de8a-151">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="5de8a-152">Yes</span><span class="sxs-lookup"><span data-stu-id="5de8a-152">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5de8a-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="5de8a-153">Requirements</span></span>



| <span data-ttu-id="5de8a-154">需求</span><span class="sxs-lookup"><span data-stu-id="5de8a-154">Requirement</span></span> | <span data-ttu-id="5de8a-155">值</span><span class="sxs-lookup"><span data-stu-id="5de8a-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5de8a-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5de8a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="5de8a-157">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5de8a-157">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="5de8a-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5de8a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="5de8a-159">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5de8a-159">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="5de8a-160">標頭</span><span class="sxs-lookup"><span data-stu-id="5de8a-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="5de8a-161"><dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、windows 7、Windows Server 2008 和 Windows Vista (的 WinBase，包括 windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5de8a-161"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="5de8a-162">程式庫</span><span class="sxs-lookup"><span data-stu-id="5de8a-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="5de8a-163"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5de8a-163"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="5de8a-164">DLL</span><span class="sxs-lookup"><span data-stu-id="5de8a-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5de8a-165"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5de8a-165"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="5de8a-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5de8a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de8a-167">**CancelIo**</span><span class="sxs-lookup"><span data-stu-id="5de8a-167">**CancelIo**</span></span>](cancelio.md)
</dt> <dt>

[<span data-ttu-id="5de8a-168">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="5de8a-168">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="5de8a-169">解除擱置中的 i/o 作業</span><span class="sxs-lookup"><span data-stu-id="5de8a-169">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)
</dt> <dt>

[<span data-ttu-id="5de8a-170">檔案管理功能</span><span class="sxs-lookup"><span data-stu-id="5de8a-170">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="5de8a-171">同步和非同步 i/o</span><span class="sxs-lookup"><span data-stu-id="5de8a-171">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

