---
description: IOCTL \_ copychunk 可控制項程式碼會起始資料範圍的伺服器端複本，也稱為區塊。
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: IOCTL_COPYCHUNK 控制程式代碼
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
ms.openlocfilehash: c425fc53563e6dfc16d2040fb575f47f0f8fdf35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970518"
---
# <a name="ioctl_copychunk-control-code"></a><span data-ttu-id="5eb11-103">IOCTL \_ copychunk 可控制項程式碼</span><span class="sxs-lookup"><span data-stu-id="5eb11-103">IOCTL\_COPYCHUNK control code</span></span>

<span data-ttu-id="5eb11-104">**IOCTL \_ copychunk 可** 控制項程式碼會起始資料範圍的伺服器端複本，也稱為區塊。</span><span class="sxs-lookup"><span data-stu-id="5eb11-104">The **IOCTL\_COPYCHUNK** control code initiates a server-side copy of a range of data, also called a chunk.</span></span>

<span data-ttu-id="5eb11-105">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="5eb11-105">To perform this operation, call the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a><span data-ttu-id="5eb11-106">參數</span><span class="sxs-lookup"><span data-stu-id="5eb11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb11-107">*hDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5eb11-107">*hDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb11-108">檔案的控制碼，該檔案是伺服器端複製作業的目標。</span><span class="sxs-lookup"><span data-stu-id="5eb11-108">A handle to the file that is the target of the server-side copy operation.</span></span> <span data-ttu-id="5eb11-109">若要取得此控制碼，請呼叫 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="5eb11-109">To obtain this handle, call the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="5eb11-110">*dwIoControlCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5eb11-110">*dwIoControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb11-111">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="5eb11-111">The control code for the operation.</span></span> <span data-ttu-id="5eb11-112">使用 **IOCTL \_ copychunk 可** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="5eb11-112">Use **IOCTL\_COPYCHUNK** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="5eb11-113">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="5eb11-113">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="5eb11-114">輸入緩衝區的指標，也就是 **SRV \_ copychunk 可 \_ 複製** 結構。</span><span class="sxs-lookup"><span data-stu-id="5eb11-114">A pointer to the input buffer, a **SRV\_COPYCHUNK\_COPY** structure.</span></span> <span data-ttu-id="5eb11-115">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="5eb11-115">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="5eb11-116">*nInBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5eb11-116">*nInBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb11-117">輸入緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5eb11-117">The size of the input buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5eb11-118">*lpOutBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5eb11-118">*lpOutBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb11-119">輸出緩衝區的指標，也就是 **SRV \_ copychunk 可 \_ 回應** 結構。</span><span class="sxs-lookup"><span data-stu-id="5eb11-119">A pointer to the output buffer, a **SRV\_COPYCHUNK\_RESPONSE** structure.</span></span> <span data-ttu-id="5eb11-120">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="5eb11-120">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="5eb11-121">*nOutBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5eb11-121">*nOutBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb11-122">輸出緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="5eb11-122">The size of the output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5eb11-123">*lpBytesReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5eb11-123">*lpBytesReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb11-124">變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5eb11-124">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="5eb11-125">如果輸出緩衝區太小，則呼叫會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數會傳回 **錯誤 \_ 的 \_ 緩衝區**，而 *lpBytesReturned* 為零。</span><span class="sxs-lookup"><span data-stu-id="5eb11-125">If the output buffer is too small, the call fails, the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR\_INSUFFICIENT\_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="5eb11-126">如果 *lpOverlapped* 參數為 **null**，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="5eb11-126">If the *lpOverlapped* parameter is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="5eb11-127">即使作業未傳回輸出資料，而且 *lpOutBuffer* 參數為 **Null**， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 仍會使用 *lpBytesReturned*。</span><span class="sxs-lookup"><span data-stu-id="5eb11-127">Even when an operation returns no output data and the *lpOutBuffer* parameter is **NULL**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="5eb11-128">在這類作業之後， *lpBytesReturned* 的值就沒有意義。</span><span class="sxs-lookup"><span data-stu-id="5eb11-128">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="5eb11-129">如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="5eb11-129">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="5eb11-130">如果 *lpOverlapped* 不是 **Null** ，而且作業傳回資料，則在重迭的作業完成之前， *lpBytesReturned* 是無意義的。</span><span class="sxs-lookup"><span data-stu-id="5eb11-130">If *lpOverlapped* is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="5eb11-131">若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數。</span><span class="sxs-lookup"><span data-stu-id="5eb11-131">To retrieve the number of bytes returned, call the [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="5eb11-132">如果 *hDevice* 參數與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5eb11-132">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="5eb11-133">*lpOverlapped* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5eb11-133">*lpOverlapped* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb11-134">重 [**迭結構的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="5eb11-134">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="5eb11-135">如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 hDevice 參數，則會忽略 *lpOverlapped* 。</span><span class="sxs-lookup"><span data-stu-id="5eb11-135">If the *hDevice* parameter was opened without specifying **FILE\_FLAG\_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="5eb11-136">如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。</span><span class="sxs-lookup"><span data-stu-id="5eb11-136">If *hDevice* was opened with the **FILE\_FLAG\_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="5eb11-137">在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 迭結構。</span><span class="sxs-lookup"><span data-stu-id="5eb11-137">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="5eb11-138">否則，函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="5eb11-138">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="5eb11-139">針對重迭的作業， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。</span><span class="sxs-lookup"><span data-stu-id="5eb11-139">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="5eb11-140">否則，必須等到作業完成或發生錯誤時，函數才會傳回。</span><span class="sxs-lookup"><span data-stu-id="5eb11-140">Otherwise, the function does not return until the operation has been completed or until an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eb11-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="5eb11-141">Return value</span></span>

<span data-ttu-id="5eb11-142">如果作業順利完成， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="5eb11-142">If the operation completes successfully, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="5eb11-143">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="5eb11-143">If the operation fails or is pending, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="5eb11-144">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="5eb11-144">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="5eb11-145">備註</span><span class="sxs-lookup"><span data-stu-id="5eb11-145">Remarks</span></span>

<span data-ttu-id="5eb11-146">此控制項程式碼沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="5eb11-146">This control code has no associated header file.</span></span> <span data-ttu-id="5eb11-147">您必須定義控制項程式碼和資料結構，如下所示。</span><span class="sxs-lookup"><span data-stu-id="5eb11-147">You must define the control code and data structures as follows.</span></span>

``` syntax
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

<span data-ttu-id="5eb11-148">這些成員可以依照下列方式描述。</span><span class="sxs-lookup"><span data-stu-id="5eb11-148">These members can be described as follows.</span></span>



| <span data-ttu-id="5eb11-149">member</span><span class="sxs-lookup"><span data-stu-id="5eb11-149">Member</span></span>                                                                                                                                       | <span data-ttu-id="5eb11-150">描述</span><span class="sxs-lookup"><span data-stu-id="5eb11-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eb11-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span><span class="sxs-lookup"><span data-stu-id="5eb11-151"><span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**</span></span><br/>                     | <span data-ttu-id="5eb11-152">從原始程式檔開頭到要複製之區塊的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5eb11-152">The offset, in bytes, from the beginning of the source file to the chunk to be copied.</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="5eb11-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span><span class="sxs-lookup"><span data-stu-id="5eb11-153"><span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**</span></span><br/> | <span data-ttu-id="5eb11-154">從目標檔案開頭到要複製區塊的位置位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5eb11-154">The offset, in bytes, from the beginning of the target file to the location where the chunk is to be copied.</span></span><br/>                                                                                                                                                                                                                                               |
| <span data-ttu-id="5eb11-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**長度**</span><span class="sxs-lookup"><span data-stu-id="5eb11-155"><span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**Length**</span></span><br/>                                             | <span data-ttu-id="5eb11-156">要複製之區塊中的資料位元組數。</span><span class="sxs-lookup"><span data-stu-id="5eb11-156">The number of bytes of data in the chunk to be copied.</span></span> <span data-ttu-id="5eb11-157">必須大於零且小於或等於 1 MB。</span><span class="sxs-lookup"><span data-stu-id="5eb11-157">Must be greater than zero and less than or equal to 1 MB.</span></span> <span data-ttu-id="5eb11-158">**長度** \***ChunkCount** 必須小於或等於 16 MB。</span><span class="sxs-lookup"><span data-stu-id="5eb11-158">**Length** \* **ChunkCount** must be less than or equal to 16 MB.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="5eb11-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span><span class="sxs-lookup"><span data-stu-id="5eb11-159"><span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**</span></span><br/>                             | <span data-ttu-id="5eb11-160">索引鍵，表示含有要複製之資料的原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="5eb11-160">A key that represents the source file with the data to be copied.</span></span> <span data-ttu-id="5eb11-161">此金鑰是透過 [**FSCTL \_ SRV \_ 要求 \_ 繼續 \_ 金鑰**](fsctl-srv-request-resume-key.md)取得的。</span><span class="sxs-lookup"><span data-stu-id="5eb11-161">This key is obtained through [**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**](fsctl-srv-request-resume-key.md).</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="5eb11-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span><span class="sxs-lookup"><span data-stu-id="5eb11-162"><span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**</span></span><br/>                             | <span data-ttu-id="5eb11-163">要複製的區塊數目。</span><span class="sxs-lookup"><span data-stu-id="5eb11-163">The number of chunks to be copied.</span></span> <span data-ttu-id="5eb11-164">必須大於零且小於或等於256。</span><span class="sxs-lookup"><span data-stu-id="5eb11-164">Must be greater than zero and less than or equal to 256.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5eb11-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留**</span><span class="sxs-lookup"><span data-stu-id="5eb11-165"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved**</span></span><br/>                                     | <span data-ttu-id="5eb11-166">這個成員是保留供系統使用;請勿使用。</span><span class="sxs-lookup"><span data-stu-id="5eb11-166">This member is reserved for system use; do not use.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5eb11-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**塊**</span><span class="sxs-lookup"><span data-stu-id="5eb11-167"><span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**Chunk**</span></span><br/>                                                 | <span data-ttu-id="5eb11-168">**ChunkCount** **SRV \_ copychunk 可** 結構的陣列，每個要複製的區塊都有一個。</span><span class="sxs-lookup"><span data-stu-id="5eb11-168">An array of **ChunkCount** **SRV\_COPYCHUNK** structures, one for each chunk to be copied.</span></span> <span data-ttu-id="5eb11-169">這個陣列的長度（以位元組為單位）必須是 **ChunkCount** \* sizeof (**SRV \_ copychunk 可**) 。</span><span class="sxs-lookup"><span data-stu-id="5eb11-169">The length, in bytes, of this array must be **ChunkCount** \* sizeof(**SRV\_COPYCHUNK**).</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="5eb11-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span><span class="sxs-lookup"><span data-stu-id="5eb11-170"><span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**</span></span><br/>                 | <span data-ttu-id="5eb11-171">如果作業失敗，並 **出現 \_ 錯誤 \_ 參數無效**，此值會指出伺服器將在單一要求中接受的區塊數目上限，也就是256。</span><span class="sxs-lookup"><span data-stu-id="5eb11-171">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of chunks the server will accept in a single request, which is 256.</span></span> <span data-ttu-id="5eb11-172">否則，此值會指出已成功寫入的區塊數目。</span><span class="sxs-lookup"><span data-stu-id="5eb11-172">Otherwise, this value indicates the number of chunks that were successfully written.</span></span><br/>                                                                                               |
| <span data-ttu-id="5eb11-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="5eb11-173"><span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**</span></span><br/> | <span data-ttu-id="5eb11-174">如果作業失敗，並 **出現 \_ 錯誤 \_ 參數無效**，則這個值會指出伺服器允許在單一區塊中寫入的最大位元組數目，也就是 1 MB。</span><span class="sxs-lookup"><span data-stu-id="5eb11-174">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will allow to be written in a single chunk, which is 1 MB.</span></span> <span data-ttu-id="5eb11-175">否則，此值會指出未成功處理的最後一個區塊中已成功寫入的位元組數目， (是否發生部分寫入) 。</span><span class="sxs-lookup"><span data-stu-id="5eb11-175">Otherwise, this value indicates the number of bytes that were successfully written in the last chunk that was not successfully processed (if a partial write occurred).</span></span><br/> |
| <span data-ttu-id="5eb11-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="5eb11-176"><span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**</span></span><br/> | <span data-ttu-id="5eb11-177">如果作業失敗並 **出現錯誤 \_ \_ 參數無效**，此值會指出伺服器將在單一要求中複製的最大位元組數目，也就是 16 MB。</span><span class="sxs-lookup"><span data-stu-id="5eb11-177">If the operation failed with **ERROR\_INVALID\_PARAMETER**, this value indicates the maximum number of bytes the server will copy in a single request, which is 16 MB.</span></span> <span data-ttu-id="5eb11-178">否則，此值會指出已成功寫入的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5eb11-178">Otherwise, this value indicates the number of bytes that were successfully written.</span></span><br/>                                                                                                 |



 

## <a name="see-also"></a><span data-ttu-id="5eb11-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5eb11-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb11-180">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="5eb11-180">**DeviceIoControl**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="5eb11-181">**FSCTL \_ SRV \_ 要求 \_ 繼續 \_ 金鑰**</span><span class="sxs-lookup"><span data-stu-id="5eb11-181">**FSCTL\_SRV\_REQUEST\_RESUME\_KEY**</span></span>](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
