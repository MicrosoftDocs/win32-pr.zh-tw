---
description: FSCTL \_ SRV \_ 要求 \_ RESUME \_ KEY control 程式碼是用來抓取不透明的檔案參考，以與 IOCTL \_ copychunk 可控制項程式碼搭配使用。
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: FSCTL_SRV_REQUEST_RESUME_KEY 控制程式代碼
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847062"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a><span data-ttu-id="5578e-103">FSCTL \_ SRV \_ 要求 \_ 繼續 \_ 按鍵控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="5578e-103">FSCTL\_SRV\_REQUEST\_RESUME\_KEY control code</span></span>

<span data-ttu-id="5578e-104">**FSCTL \_ SRV \_ 要求 \_ RESUME \_ KEY** control 程式碼是用來抓取不透明的檔案參考，以與 [**IOCTL \_ copychunk 可**](ioctl-copychunk.md)控制項程式碼搭配使用。</span><span class="sxs-lookup"><span data-stu-id="5578e-104">The **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** control code is used to retrieve an opaque file reference for use with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span>

<span data-ttu-id="5578e-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="5578e-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="5578e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5578e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5578e-107">*hDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5578e-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5578e-108">要要求其來源檔案索引鍵之檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5578e-108">A handle to the file for which the source file key is to be requested.</span></span> <span data-ttu-id="5578e-109">若要取得此控制碼，請呼叫 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="5578e-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="5578e-110">*dwIoControlCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5578e-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5578e-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="5578e-111">The control code for the operation.</span></span> <span data-ttu-id="5578e-112">針對這項作業，請使用 **FSCTL \_ SRV \_ 要求 \_ 繼續 \_ 金鑰** 。</span><span class="sxs-lookup"><span data-stu-id="5578e-112">Use **FSCTL\_SRV\_REQUEST\_RESUME\_KEY** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="5578e-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="5578e-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="5578e-114">未搭配此作業使用;設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5578e-114">Not used with this operation; set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5578e-115">*nInBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5578e-115">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5578e-116">未搭配此作業使用;設定為零。</span><span class="sxs-lookup"><span data-stu-id="5578e-116">Not used with this operation; set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5578e-117">*lpOutBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5578e-117">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5578e-118">輸出緩衝區的指標， **SRV \_ 要求 \_ 繼續索引 \_ 鍵** 結構。</span><span class="sxs-lookup"><span data-stu-id="5578e-118">A pointer to the output buffer, a **SRV\_REQUEST\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="5578e-119">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="5578e-119">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="5578e-120">*nOutBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5578e-120">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5578e-121">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="5578e-121">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5578e-122">*lpBytesReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5578e-122">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5578e-123">變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5578e-123">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="5578e-124">如果輸出緩衝區太小，則呼叫會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數會傳回 **錯誤 \_ 的 \_ 緩衝區**，而 *lpBytesReturned* 為零。</span><span class="sxs-lookup"><span data-stu-id="5578e-124">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="5578e-125">如果 *lpOverlapped* 參數為 **null**，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="5578e-125">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="5578e-126">即使作業未傳回輸出資料，而且 *lpOutBuffer* 參數為 **Null**， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 仍會使用 *lpBytesReturned*。</span><span class="sxs-lookup"><span data-stu-id="5578e-126">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="5578e-127">在這類作業之後， *lpBytesReturned* 的值就沒有意義。</span><span class="sxs-lookup"><span data-stu-id="5578e-127">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="5578e-128">如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="5578e-128">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="5578e-129">如果 *lpOverlapped* 不是 **Null** ，而且作業傳回資料，則在重迭的作業完成之前， *lpBytesReturned* 是無意義的。</span><span class="sxs-lookup"><span data-stu-id="5578e-129">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="5578e-130">若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數。</span><span class="sxs-lookup"><span data-stu-id="5578e-130">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="5578e-131">如果 *hDevice* 參數與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5578e-131">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="5578e-132">*lpOverlapped* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5578e-132">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5578e-133">重 [**迭結構的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="5578e-133">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="5578e-134">如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 hDevice 參數，則會忽略 *lpOverlapped* 。</span><span class="sxs-lookup"><span data-stu-id="5578e-134">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="5578e-135">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="5578e-135">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="5578e-136">在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 迭結構。</span><span class="sxs-lookup"><span data-stu-id="5578e-136">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="5578e-137">否則，函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="5578e-137">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="5578e-138">針對重迭的作業， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。</span><span class="sxs-lookup"><span data-stu-id="5578e-138">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="5578e-139">否則，必須等到作業完成或發生錯誤時，函數才會傳回。</span><span class="sxs-lookup"><span data-stu-id="5578e-139">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5578e-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="5578e-140">Return value</span></span>

<span data-ttu-id="5578e-141">如果作業順利完成， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="5578e-141">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="5578e-142">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5578e-142">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="5578e-143">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="5578e-143">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="5578e-144">備註</span><span class="sxs-lookup"><span data-stu-id="5578e-144">Remarks</span></span>

<span data-ttu-id="5578e-145">此控制項程式碼沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="5578e-145">This control code has no associated header file.</span></span> <span data-ttu-id="5578e-146">您必須定義控制項程式碼和資料結構，如下所示。</span><span class="sxs-lookup"><span data-stu-id="5578e-146">You must define the control code and data structures as follows.</span></span>

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

<span data-ttu-id="5578e-147">這些成員可以依照下列方式描述。</span><span class="sxs-lookup"><span data-stu-id="5578e-147">These members can be described as follows.</span></span>



| <span data-ttu-id="5578e-148">member</span><span class="sxs-lookup"><span data-stu-id="5578e-148">Member</span></span>                                                                                                                       | <span data-ttu-id="5578e-149">描述</span><span class="sxs-lookup"><span data-stu-id="5578e-149">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5578e-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span><span class="sxs-lookup"><span data-stu-id="5578e-150"><span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**</span></span><br/>                 | <span data-ttu-id="5578e-151">識別伺服器之原始程式檔的不透明值。</span><span class="sxs-lookup"><span data-stu-id="5578e-151">An opaque value that identifies the source file to the server.</span></span><br/>                                                                                                   |
| <span data-ttu-id="5578e-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="5578e-152"><span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**Timestamp**</span></span><br/>                 | <span data-ttu-id="5578e-153">識別開啟檔案之時間的不透明值。</span><span class="sxs-lookup"><span data-stu-id="5578e-153">An opaque value that identifies the time when the file was opened.</span></span><br/>                                                                                               |
| <span data-ttu-id="5578e-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**</span><span class="sxs-lookup"><span data-stu-id="5578e-154"><span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**</span></span><br/>                                         | <span data-ttu-id="5578e-155">識別開啟檔案之進程的不透明值。</span><span class="sxs-lookup"><span data-stu-id="5578e-155">An opaque value that identifies the process that opened the file.</span></span><br/>                                                                                                |
| <span data-ttu-id="5578e-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**關鍵**</span><span class="sxs-lookup"><span data-stu-id="5578e-156"><span id="Key"></span><span id="key"></span><span id="KEY"></span>**Key**</span></span><br/>                                         | <span data-ttu-id="5578e-157">**SRV \_ RESUME \_ 鍵** 結構。</span><span class="sxs-lookup"><span data-stu-id="5578e-157">A **SRV\_RESUME\_KEY** structure.</span></span> <span data-ttu-id="5578e-158">若要執行伺服器端複製作業，請將此結構與 [**IOCTL \_ copychunk 可**](ioctl-copychunk.md) 控制項程式碼搭配使用。</span><span class="sxs-lookup"><span data-stu-id="5578e-158">To perform a server-side copy operation, use this structure with the [**IOCTL\_COPYCHUNK**](ioctl-copychunk.md) control code.</span></span><br/> |
| <span data-ttu-id="5578e-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**CoNtextLength**</span><span class="sxs-lookup"><span data-stu-id="5578e-159"><span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**ContextLength**</span></span><br/> | <span data-ttu-id="5578e-160">這個成員是保留供系統使用;請勿使用。</span><span class="sxs-lookup"><span data-stu-id="5578e-160">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |
| <span data-ttu-id="5578e-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**上下文**</span><span class="sxs-lookup"><span data-stu-id="5578e-161"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**Context**</span></span><br/>                         | <span data-ttu-id="5578e-162">這個成員是保留供系統使用;請勿使用。</span><span class="sxs-lookup"><span data-stu-id="5578e-162">This member is reserved for system use; do not use.</span></span><br/>                                                                                                              |



 

## <a name="see-also"></a><span data-ttu-id="5578e-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5578e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5578e-164">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="5578e-164">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="5578e-165">**IOCTL \_ COPYCHUNK 可**</span><span class="sxs-lookup"><span data-stu-id="5578e-165">**IOCTL\_COPYCHUNK**</span></span>](ioctl-copychunk.md)
</dt> </dl>

 

 
