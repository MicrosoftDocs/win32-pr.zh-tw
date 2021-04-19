---
description: '\_ \_ \_ \_ 當讀取資料或將資料寫入遠端檔案時，IOCTL LMR 停用本機緩衝控制程式代碼會停用本機用戶端記憶體中的資料快取。 這是在公用標頭中無法使用的內部定義控制項程式碼。'
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: IOCTL_LMR_DISABLE_LOCAL_BUFFERING 控制程式代碼
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d596402c489caee972e1305f2a32881312fd3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973147"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a><span data-ttu-id="f3521-104">IOCTL \_ LMR \_ 停用 \_ 本機 \_ 緩衝控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="f3521-104">IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING control code</span></span>

<span data-ttu-id="f3521-105">當讀取資料或將資料寫入遠端檔案時， **IOCTL \_ LMR \_ 停用 \_ 本機 \_ 緩衝** 控制程式代碼會停用本機用戶端記憶體中的資料快取。</span><span class="sxs-lookup"><span data-stu-id="f3521-105">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code disables local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="f3521-106">這是在公用標頭中無法使用的內部定義控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="f3521-106">This is an internally-defined control code not available in a public header.</span></span>

<span data-ttu-id="f3521-107">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="f3521-107">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="f3521-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3521-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3521-109">*hDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3521-109">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3521-110">遠端檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f3521-110">A handle to the remote file.</span></span> <span data-ttu-id="f3521-111">若要取得此控制碼，請呼叫 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="f3521-111">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="f3521-112">*dwIoControlCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3521-112">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3521-113">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="f3521-113">The control code for the operation.</span></span> <span data-ttu-id="f3521-114">使用此作業的值0x140390。</span><span class="sxs-lookup"><span data-stu-id="f3521-114">Use the value 0x140390 for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f3521-115">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="f3521-115">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f3521-116">未使用，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3521-116">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3521-117">*nInBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3521-117">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3521-118">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3521-118">The size of the input buffer, in bytes.</span></span> <span data-ttu-id="f3521-119">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f3521-119">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f3521-120">*lpOutBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3521-120">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3521-121">未使用，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3521-121">Not used, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f3521-122">*nOutBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3521-122">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3521-123">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="f3521-123">The size of the output buffer, in bytes.</span></span> <span data-ttu-id="f3521-124">必須為零。</span><span class="sxs-lookup"><span data-stu-id="f3521-124">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f3521-125">*lpBytesReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3521-125">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3521-126">變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3521-126">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="f3521-127">如果輸出緩衝區太小，則呼叫會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數會傳回 **錯誤的 \_ \_ 緩衝區**，而 *lpBytesReturned* 為零。</span><span class="sxs-lookup"><span data-stu-id="f3521-127">If the output buffer is too small, then the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="f3521-128">如果 *lpOverlapped* 參數為 **null**，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="f3521-128">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="f3521-129">即使作業未傳回輸出資料，而且 *lpOutBuffer* 參數為 **Null**， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 仍會使用 *lpBytesReturned*。</span><span class="sxs-lookup"><span data-stu-id="f3521-129">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="f3521-130">在這類作業之後， *lpBytesReturned* 的值就沒有意義。</span><span class="sxs-lookup"><span data-stu-id="f3521-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="f3521-131">如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="f3521-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="f3521-132">如果 *lpOverlapped* 不是 **Null** ，而且作業傳回資料，則在重迭的作業完成之前， *lpBytesReturned* 是無意義的。</span><span class="sxs-lookup"><span data-stu-id="f3521-132">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="f3521-133">若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數。</span><span class="sxs-lookup"><span data-stu-id="f3521-133">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="f3521-134">如果 *hDevice* 參數與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f3521-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="f3521-135">*lpOverlapped* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3521-135">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3521-136">重 [**迭結構的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="f3521-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="f3521-137">如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 hDevice 參數，則會忽略 *lpOverlapped* 。</span><span class="sxs-lookup"><span data-stu-id="f3521-137">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="f3521-138">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="f3521-138">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="f3521-139">在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 迭結構。</span><span class="sxs-lookup"><span data-stu-id="f3521-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="f3521-140">否則，函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="f3521-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="f3521-141">針對重迭的作業， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。</span><span class="sxs-lookup"><span data-stu-id="f3521-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="f3521-142">否則，必須等到作業完成或發生錯誤時，函數才會傳回。</span><span class="sxs-lookup"><span data-stu-id="f3521-142">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3521-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3521-143">Return value</span></span>

<span data-ttu-id="f3521-144">如果作業順利完成， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="f3521-144">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="f3521-145">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f3521-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="f3521-146">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="f3521-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3521-147">備註</span><span class="sxs-lookup"><span data-stu-id="f3521-147">Remarks</span></span>

<span data-ttu-id="f3521-148">**IOCTL \_ LMR 停 \_ 用 \_ 本機 \_ 緩衝** 控制程式代碼是由系統在內部定義為0x140390，而不是在公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="f3521-148">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code is defined internally by the system as 0x140390 and not in a public header file.</span></span> <span data-ttu-id="f3521-149">特殊用途的應用程式會使用它，在讀取資料或將資料寫入遠端檔案時，停用本機用戶端記憶體中的資料快取。</span><span class="sxs-lookup"><span data-stu-id="f3521-149">It is used by special-purpose applications to disable local client-side in-memory caching of data when reading data from or writing data to a remote file.</span></span> <span data-ttu-id="f3521-150">停用本機緩衝之後，設定會維持有效，直到檔案的所有開啟的控制碼都已關閉，且重新導向程式會清除其內部資料結構。</span><span class="sxs-lookup"><span data-stu-id="f3521-150">After local buffering is disabled, the setting remains in effect until all open handles to the file are closed and the redirector cleans up its internal data structures.</span></span>

<span data-ttu-id="f3521-151">一般用途的應用程式不應使用 **IOCTL \_ LMR 停用 \_ \_ 本機 \_ 緩衝**，因為這可能會導致網路流量過高，以及相關聯的效能損失。</span><span class="sxs-lookup"><span data-stu-id="f3521-151">General-purpose applications should not use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING**, because it can result in excessive network traffic and associated loss of performance.</span></span> <span data-ttu-id="f3521-152">在嘗試充分利用網路頻寬的情況下，只有在專門應用程式中透過網路移動大量資料時，才應該使用 **IOCTL \_ LMR \_ 停用 \_ 本機 \_ 緩衝** 控制程式代碼。</span><span class="sxs-lookup"><span data-stu-id="f3521-152">The **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code should be used only in specialized applications moving large amounts of data over the network while attempting to maximize use of network bandwidth.</span></span> <span data-ttu-id="f3521-153">例如， [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) 和 [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) 函數會使用 **IOCTL \_ LMR 停用 \_ \_ 本機 \_ 緩衝** 處理，以改善大型檔案複製的效能。</span><span class="sxs-lookup"><span data-stu-id="f3521-153">For example, the [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) and [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) functions use **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** to improve large file copy performance.</span></span>

<span data-ttu-id="f3521-154">**IOCTL \_LMR \_ 停用 \_ 本機 \_ 緩衝** 並非由本機檔案系統所執行，而且將會失敗，並出現錯誤 **錯誤 \_ 無效 \_** 的函式。</span><span class="sxs-lookup"><span data-stu-id="f3521-154">**IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** is not implemented by local file systems and will fail with the error **ERROR\_INVALID\_FUNCTION**.</span></span> <span data-ttu-id="f3521-155">發出 IOCTL LMR 停用遠端目錄控制碼上的 **\_ \_ \_ 本機 \_ 緩衝** 控制程式代碼將會失敗，且 **\_ 不 \_ 支援錯誤錯誤**。</span><span class="sxs-lookup"><span data-stu-id="f3521-155">Issuing the **IOCTL\_LMR\_DISABLE\_LOCAL\_BUFFERING** control code on remote directory handles will fail with the error **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3521-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3521-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3521-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="f3521-157">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
