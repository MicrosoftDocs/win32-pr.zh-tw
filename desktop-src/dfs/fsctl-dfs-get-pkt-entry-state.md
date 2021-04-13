---
title: FSCTL_DFS_GET_PKT_ENTRY_STATE 控制碼 (LmDfs.h)
description: FSCTL_DFS_GET_PKT_ENTRY_STATE 控制程式代碼可以取得與 NetDfsGetClientInfo 函式相同的資訊，但可在某些設定中提供更佳的效能，而這些設定在 DFS 伺服器上會有高延遲。
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510669"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a><span data-ttu-id="876f4-103">FSCTL_DFS_GET_PKT_ENTRY_STATE 控制程式代碼</span><span class="sxs-lookup"><span data-stu-id="876f4-103">FSCTL_DFS_GET_PKT_ENTRY_STATE control code</span></span>

<span data-ttu-id="876f4-104">**FSCTL_DFS_GET_PKT_ENTRY_STATE** 控制程式代碼可以取得與 [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)函式相同的資訊，但可在某些設定中提供更佳的效能，而這些設定在 DFS 伺服器上會有高延遲。</span><span class="sxs-lookup"><span data-stu-id="876f4-104">The **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="876f4-105">除非有效能問題，否則不建議使用 **FSCTL_DFS_GET_PKT_ENTRY_STATE** 控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="876f4-105">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="876f4-106">若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。</span><span class="sxs-lookup"><span data-stu-id="876f4-106">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the following parameters.</span></span>

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a><span data-ttu-id="876f4-107">參數</span><span class="sxs-lookup"><span data-stu-id="876f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="876f4-108">*hDevice* [in]</span><span class="sxs-lookup"><span data-stu-id="876f4-108">*hDevice* [in]</span></span>
</dt> <dd>

<span data-ttu-id="876f4-109">裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="876f4-109">A handle to the device.</span></span> <span data-ttu-id="876f4-110">若要取得裝置控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。</span><span class="sxs-lookup"><span data-stu-id="876f4-110">To obtain a device handle, call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span>

</dd> <dt>

<span data-ttu-id="876f4-111">*dwIoControlCode* [in]</span><span class="sxs-lookup"><span data-stu-id="876f4-111">*dwIoControlCode* [in]</span></span>
</dt> <dd>

<span data-ttu-id="876f4-112">作業的控制項程式碼。</span><span class="sxs-lookup"><span data-stu-id="876f4-112">The control code for the operation.</span></span> <span data-ttu-id="876f4-113">使用 **FSCTL_DFS_GET_PKT_ENTRY_STATE** 進行此作業。</span><span class="sxs-lookup"><span data-stu-id="876f4-113">Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="876f4-114">*lpInBuffer*</span><span class="sxs-lookup"><span data-stu-id="876f4-114">*lpInBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="876f4-115">[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)結構的位址和後面的 1-3 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="876f4-115">Address of a [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure and the 1-3 Unicode strings that follow.</span></span>

</dd> <dt>

<span data-ttu-id="876f4-116">*nInBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="876f4-116">*nInBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="876f4-117">*LpInBuffer* 參數所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="876f4-117">Size, in bytes, of the buffer pointed to by the *lpInBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="876f4-118">*lpOutBuffer* [out]</span><span class="sxs-lookup"><span data-stu-id="876f4-118">*lpOutBuffer* [out]</span></span>
</dt> <dd>

<span data-ttu-id="876f4-119">**DFS_INFO_ \#** 結構的位址，以及 **DFS_INFO_ \#** 結構所指向的任何字串和結構。</span><span class="sxs-lookup"><span data-stu-id="876f4-119">Address of a **DFS_INFO_\#** structure and any strings and structures pointed to by the **DFS_INFO_\#** structure.</span></span> <span data-ttu-id="876f4-120">傳回的特定結構取決於傳入輸入緩衝區之 [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)結構中的 **層級** 成員。</span><span class="sxs-lookup"><span data-stu-id="876f4-120">The specific structure returned depends on the **Level** member in the [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) structure passed in the input buffer.</span></span>

</dd> <dt>

<span data-ttu-id="876f4-121">*nOutBufferSize* [in]</span><span class="sxs-lookup"><span data-stu-id="876f4-121">*nOutBufferSize* [in]</span></span>
</dt> <dd>

<span data-ttu-id="876f4-122">*LpOutBuffer* 參數所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="876f4-122">Size, in bytes, of the buffer pointed to by the *lpOutBuffer* parameter.</span></span> <span data-ttu-id="876f4-123">由於傳回的 **DFS_INFO_ \#** 結構所參考的字串和結構也在輸出緩衝區中，這個緩衝區應大於指定的 **DFS_INFO_ \#** 結構。</span><span class="sxs-lookup"><span data-stu-id="876f4-123">Due to the strings and structures referenced by the returned **DFS_INFO_\#** structure that are also in the output buffer, this buffer should be larger than the **DFS_INFO_\#** structure specified.</span></span>

</dd> <dt>

<span data-ttu-id="876f4-124">*lpBytesReturned* [out]</span><span class="sxs-lookup"><span data-stu-id="876f4-124">*lpBytesReturned* [out]</span></span>
</dt> <dd>

<span data-ttu-id="876f4-125">變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="876f4-125">A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.</span></span>

<span data-ttu-id="876f4-126">如果輸出緩衝區太小，但至少足以容納 **DWORD**，則呼叫會失敗、 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 **ERROR_MORE_DATA**，而且輸出緩衝區的第一個 **DWORD** 會包含所需的大小。</span><span class="sxs-lookup"><span data-stu-id="876f4-126">If the output buffer is too small, but at least large enough to hold a **DWORD**, the call fails, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_MORE_DATA**, and the first **DWORD** of the output buffer contains the size that would have been required.</span></span> <span data-ttu-id="876f4-127">如果輸出緩衝區無法保存 **DWORD** ，則呼叫會失敗並出現 **ERROR_INSUFFICIENT_BUFFER**，且 *lpBytesReturned* 為零。</span><span class="sxs-lookup"><span data-stu-id="876f4-127">If the output buffer cannot hold a **DWORD** then the call fails with **ERROR_INSUFFICIENT_BUFFER**, and *lpBytesReturned* is zero.</span></span>

<span data-ttu-id="876f4-128">如果 *lpOverlapped* 為 **null**，則 *lpBytesReturned* 不可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="876f4-128">If *lpOverlapped* is **NULL**, *lpBytesReturned* cannot be **NULL**.</span></span> <span data-ttu-id="876f4-129">即使作業未傳回輸出資料，而且 *lpOutBuffer* 為 **Null**， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 也會使用 *lpBytesReturned*。</span><span class="sxs-lookup"><span data-stu-id="876f4-129">Even when an operation returns no output data and *lpOutBuffer* is **NULL**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) makes use of *lpBytesReturned*.</span></span> <span data-ttu-id="876f4-130">在這類作業之後， *lpBytesReturned* 的值就沒有意義。</span><span class="sxs-lookup"><span data-stu-id="876f4-130">After such an operation, the value of *lpBytesReturned* is meaningless.</span></span>

<span data-ttu-id="876f4-131">如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="876f4-131">If *lpOverlapped* is not **NULL**, *lpBytesReturned* can be **NULL**.</span></span> <span data-ttu-id="876f4-132">如果這個參數不是 **Null** ，而且作業傳回資料，則 *lpBytesReturned* 會在重迭的作業完成之前無意義。</span><span class="sxs-lookup"><span data-stu-id="876f4-132">If this parameter is not **NULL** and the operation returns data, *lpBytesReturned* is meaningless until the overlapped operation has completed.</span></span> <span data-ttu-id="876f4-133">若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)。</span><span class="sxs-lookup"><span data-stu-id="876f4-133">To retrieve the number of bytes returned, call [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult).</span></span> <span data-ttu-id="876f4-134">如果 *hDevice* 參數與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)來取得傳回的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="876f4-134">If the *hDevice* parameter is associated with an I/O completion port, you can retrieve the number of bytes returned by calling [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).</span></span>

</dd> <dt>

<span data-ttu-id="876f4-135">*lpOverlapped* [in]</span><span class="sxs-lookup"><span data-stu-id="876f4-135">*lpOverlapped* [in]</span></span>
</dt> <dd>

<span data-ttu-id="876f4-136">重 [**迭結構的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指標。</span><span class="sxs-lookup"><span data-stu-id="876f4-136">A pointer to an [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="876f4-137">如果在未指定 **FILE_FLAG_OVERLAPPED** 的情況下開啟 *hDevice* ，則會忽略 *lpOverlapped* 。</span><span class="sxs-lookup"><span data-stu-id="876f4-137">If *hDevice* was opened without specifying **FILE_FLAG_OVERLAPPED**, *lpOverlapped* is ignored.</span></span>

<span data-ttu-id="876f4-138">如果使用 **FILE_FLAG_OVERLAPPED** 旗標開啟 *hDevice* ，則會以非同步) 作業的重迭 (來執行此作業。</span><span class="sxs-lookup"><span data-stu-id="876f4-138">If *hDevice* was opened with the **FILE_FLAG_OVERLAPPED** flag, the operation is performed as an overlapped (asynchronous) operation.</span></span> <span data-ttu-id="876f4-139">在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 迭結構。</span><span class="sxs-lookup"><span data-stu-id="876f4-139">In this case, *lpOverlapped* must point to a valid [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure that contains a handle to an event object.</span></span> <span data-ttu-id="876f4-140">否則，函式會以無法預期的方式失敗。</span><span class="sxs-lookup"><span data-stu-id="876f4-140">Otherwise, the function fails in unpredictable ways.</span></span>

<span data-ttu-id="876f4-141">針對重迭的作業， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。</span><span class="sxs-lookup"><span data-stu-id="876f4-141">For overlapped operations, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) returns immediately, and the event object is signaled when the operation has been completed.</span></span> <span data-ttu-id="876f4-142">否則，在作業完成或發生錯誤之前，函數不會傳回。</span><span class="sxs-lookup"><span data-stu-id="876f4-142">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="876f4-143">傳回值</span><span class="sxs-lookup"><span data-stu-id="876f4-143">Return value</span></span>

<span data-ttu-id="876f4-144">如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="876f4-144">If the operation completes successfully, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns a nonzero value.</span></span>

<span data-ttu-id="876f4-145">如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="876f4-145">If the operation fails or is pending, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) returns zero.</span></span> <span data-ttu-id="876f4-146">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="876f4-146">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="876f4-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="876f4-147">Requirements</span></span>

| <span data-ttu-id="876f4-148">需求</span><span class="sxs-lookup"><span data-stu-id="876f4-148">Requirement</span></span> | <span data-ttu-id="876f4-149">值</span><span class="sxs-lookup"><span data-stu-id="876f4-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="876f4-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="876f4-150">Minimum supported client</span></span><br/> | <span data-ttu-id="876f4-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="876f4-151">Windows Vista</span></span><br/>                                                                             |
| <span data-ttu-id="876f4-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="876f4-152">Minimum supported server</span></span><br/> | <span data-ttu-id="876f4-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="876f4-153">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="876f4-154">標頭</span><span class="sxs-lookup"><span data-stu-id="876f4-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="876f4-155"><dt>LmDfs (包含 LmDfs) </dt></span><span class="sxs-lookup"><span data-stu-id="876f4-155"><dt>LmDfs.h (include LmDfs.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="876f4-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="876f4-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876f4-157">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="876f4-157">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="876f4-158">**NetDfsGetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="876f4-158">**NetDfsGetClientInfo**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
