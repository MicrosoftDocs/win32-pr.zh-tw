---
description: 同時捕獲多個完成埠專案。
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: 'GetQueuedCompletionStatusEx 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985694"
---
# <a name="getqueuedcompletionstatusex-function"></a><span data-ttu-id="00d61-103">GetQueuedCompletionStatusEx 函式</span><span class="sxs-lookup"><span data-stu-id="00d61-103">GetQueuedCompletionStatusEx function</span></span>

<span data-ttu-id="00d61-104">同時捕獲多個完成埠專案。</span><span class="sxs-lookup"><span data-stu-id="00d61-104">Retrieves multiple completion port entries simultaneously.</span></span> <span data-ttu-id="00d61-105">它會等候與指定完成埠相關聯的暫止 i/o 作業完成。</span><span class="sxs-lookup"><span data-stu-id="00d61-105">It waits for pending I/O operations that are associated with the specified completion port to complete.</span></span>

<span data-ttu-id="00d61-106">若要一次清除一個自動完成封包，請使用 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數。</span><span class="sxs-lookup"><span data-stu-id="00d61-106">To dequeue I/O completion packets one at a time, use the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d61-107">語法</span><span class="sxs-lookup"><span data-stu-id="00d61-107">Syntax</span></span>


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a><span data-ttu-id="00d61-108">參數</span><span class="sxs-lookup"><span data-stu-id="00d61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d61-109">*CompletionPort* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00d61-109">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d61-110">完成埠的控制碼。</span><span class="sxs-lookup"><span data-stu-id="00d61-110">A handle to the completion port.</span></span> <span data-ttu-id="00d61-111">若要建立完成埠，請使用 [**CreateIoCompletionPort**](createiocompletionport.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="00d61-111">To create a completion port, use the [**CreateIoCompletionPort**](createiocompletionport.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="00d61-112">*lpCompletionPortEntries* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="00d61-112">*lpCompletionPortEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00d61-113">在輸入時，指向預先配置的重迭 [**\_ 專案**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) 結構陣列。</span><span class="sxs-lookup"><span data-stu-id="00d61-113">On input, points to a pre-allocated array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures.</span></span>

<span data-ttu-id="00d61-114">在輸出時，會接收包含專案之重迭 [**\_ 專案**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="00d61-114">On output, receives an array of [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structures that hold the entries.</span></span> <span data-ttu-id="00d61-115">陣列元素的數目是由 *ulNumEntriesRemoved* 所提供。</span><span class="sxs-lookup"><span data-stu-id="00d61-115">The number of array elements is provided by *ulNumEntriesRemoved*.</span></span>

<span data-ttu-id="00d61-116">每個 i/o 期間傳送的位元組數、表示每個 i/o 發生之檔案的完成索引鍵，以及每個原始 i/o 中所使用的重迭結構位址，全都會在 *lpCompletionPortEntries* 陣列中傳回。</span><span class="sxs-lookup"><span data-stu-id="00d61-116">The number of bytes transferred during each I/O, the completion key that indicates on which file each I/O occurred, and the overlapped structure address used in each original I/O are all returned in the *lpCompletionPortEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="00d61-117">*ulCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00d61-117">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d61-118">要移除的專案數目上限。</span><span class="sxs-lookup"><span data-stu-id="00d61-118">The maximum number of entries to remove.</span></span>

</dd> <dt>

<span data-ttu-id="00d61-119">*ulNumEntriesRemoved* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="00d61-119">*ulNumEntriesRemoved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00d61-120">變數的指標，此變數會接收實際移除的專案數。</span><span class="sxs-lookup"><span data-stu-id="00d61-120">A pointer to a variable that receives the number of entries actually removed.</span></span>

</dd> <dt>

<span data-ttu-id="00d61-121">*dwMilliseconds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00d61-121">*dwMilliseconds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d61-122">呼叫端願意等候完成封包出現在完成埠上的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="00d61-122">The number of milliseconds that the caller is willing to wait for a completion packet to appear at the completion port.</span></span> <span data-ttu-id="00d61-123">如果完成封包未出現在指定的時間內，則函式會超時並傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="00d61-123">If a completion packet does not appear within the specified time, the function times out and returns **FALSE**.</span></span>

<span data-ttu-id="00d61-124">如果 *dwMilliseconds* 是 **無限** (0xffffffff) ，函式永遠不會有時間。如果 *dwMilliseconds* 為零，而且沒有可清除佇列的 i/o 作業，則函式會立即發生時間。</span><span class="sxs-lookup"><span data-stu-id="00d61-124">If *dwMilliseconds* is **INFINITE** (0xFFFFFFFF), the function will never time out. If *dwMilliseconds* is zero and there is no I/O operation to dequeue, the function will time out immediately.</span></span>

</dd> <dt>

<span data-ttu-id="00d61-125">*fAlertable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00d61-125">*fAlertable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d61-126">如果此參數為 **FALSE**，則函式不會傳回，直到超時期間經過或抓取專案為止。</span><span class="sxs-lookup"><span data-stu-id="00d61-126">If this parameter is **FALSE**, the function does not return until the time-out period has elapsed or an entry is retrieved.</span></span>

<span data-ttu-id="00d61-127">如果參數為 **TRUE** 且沒有可用的專案，則函式會執行可提供警示等候。</span><span class="sxs-lookup"><span data-stu-id="00d61-127">If the parameter is **TRUE** and there are no available entries, the function performs an alertable wait.</span></span> <span data-ttu-id="00d61-128">當系統將 i/o 完成常式或 APC 排入執行緒，而且執行緒執行函式時，執行緒會傳回。</span><span class="sxs-lookup"><span data-stu-id="00d61-128">The thread returns when the system queues an I/O completion routine or APC to the thread and the thread executes the function.</span></span>

<span data-ttu-id="00d61-129">當指定的 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 或 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 函式已完成，且呼叫的執行緒是起始作業的執行緒時，就會將完成常式排入佇列。</span><span class="sxs-lookup"><span data-stu-id="00d61-129">A completion routine is queued when the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function in which it was specified has completed, and the calling thread is the thread that initiated the operation.</span></span> <span data-ttu-id="00d61-130">當您呼叫 [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc)時，系統會將 APC 排入佇列。</span><span class="sxs-lookup"><span data-stu-id="00d61-130">An APC is queued when you call [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d61-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="00d61-131">Return value</span></span>

<span data-ttu-id="00d61-132">如果成功或零 (**FALSE** ，則傳回非零 (**TRUE**) ) 否則為零。</span><span class="sxs-lookup"><span data-stu-id="00d61-132">Returns nonzero (**TRUE**) if successful or zero (**FALSE**) otherwise.</span></span>

<span data-ttu-id="00d61-133">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="00d61-133">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="00d61-134">備註</span><span class="sxs-lookup"><span data-stu-id="00d61-134">Remarks</span></span>

<span data-ttu-id="00d61-135">此函式會將具有指定完成埠的執行緒產生關聯。</span><span class="sxs-lookup"><span data-stu-id="00d61-135">This function associates a thread with the specified completion port.</span></span> <span data-ttu-id="00d61-136">執行緒最多可與一個完成埠相關聯。</span><span class="sxs-lookup"><span data-stu-id="00d61-136">A thread can be associated with at most one completion port.</span></span>

<span data-ttu-id="00d61-137">當至少有一個暫止 i/o 完成時，此函式會傳回 **TRUE** ，但可能有一或多個 i/o 作業失敗。</span><span class="sxs-lookup"><span data-stu-id="00d61-137">This function returns **TRUE** when at least one pending I/O is completed, but it is possible that one or more I/O operations failed.</span></span> <span data-ttu-id="00d61-138">請注意，此函式的使用者會透過查看每個重迭 [**\_ 專案**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)中包含在 **lpOverlapped** 成員的狀態，來檢查 *lpCompletionPortEntries* 參數中傳回的專案清單，以判斷哪一個對應至任何可能的失敗 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="00d61-138">Note that it is up to the user of this function to check the list of returned entries in the *lpCompletionPortEntries* parameter to determine which of them correspond to any possible failed I/O operations by looking at the status contained in the **lpOverlapped** member in each [**OVERLAPPED\_ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).</span></span>

<span data-ttu-id="00d61-139">未清除任何 i/o 作業時，此函數會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="00d61-139">This function returns **FALSE** when no I/O operation was dequeued.</span></span> <span data-ttu-id="00d61-140">這通常表示處理此呼叫的參數時發生錯誤，或 *CompletionPort* 控制碼已關閉或無效。</span><span class="sxs-lookup"><span data-stu-id="00d61-140">This typically means that an error occurred while processing the parameters to this call, or that the *CompletionPort* handle was closed or is otherwise invalid.</span></span> <span data-ttu-id="00d61-141">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式會提供延伸的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="00d61-141">The [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function provides extended error information.</span></span>

<span data-ttu-id="00d61-142">如果對 [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 的呼叫失敗，因為與其相關聯的控制碼已關閉，則函式會傳回 **FALSE** ，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤已 **放棄的 \_ \_ 等候 \_ 0**。</span><span class="sxs-lookup"><span data-stu-id="00d61-142">If a call to [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) fails because the handle associated with it is closed, the function returns **FALSE** and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return **ERROR\_ABANDONED\_WAIT\_0**.</span></span>

<span data-ttu-id="00d61-143">伺服器應用程式可能會有數個執行緒呼叫相同完成埠的 **GetQueuedCompletionStatusEx** 函式。</span><span class="sxs-lookup"><span data-stu-id="00d61-143">Server applications may have several threads calling the **GetQueuedCompletionStatusEx** function for the same completion port.</span></span> <span data-ttu-id="00d61-144">當 i/o 作業完成時，會以先進先出的順序將它們排入此埠。</span><span class="sxs-lookup"><span data-stu-id="00d61-144">As I/O operations complete, they are queued to this port in first-in-first-out order.</span></span> <span data-ttu-id="00d61-145">如果執行緒正在主動等候此呼叫，一個或多個佇列的要求只會完成該執行緒的呼叫。</span><span class="sxs-lookup"><span data-stu-id="00d61-145">If a thread is actively waiting on this call, one or more queued requests complete the call for that thread only.</span></span>

<span data-ttu-id="00d61-146">如需 i/o 完成埠理論、使用方式和相關聯函式的詳細資訊，請參閱 [I/o 完成埠](i-o-completion-ports.md)。</span><span class="sxs-lookup"><span data-stu-id="00d61-146">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="00d61-147">在 Windows 8 和 Windows Server 2012 中，下列技術支援此功能。</span><span class="sxs-lookup"><span data-stu-id="00d61-147">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="00d61-148">技術</span><span class="sxs-lookup"><span data-stu-id="00d61-148">Technology</span></span>                                           | <span data-ttu-id="00d61-149">支援</span><span class="sxs-lookup"><span data-stu-id="00d61-149">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="00d61-150">伺服器訊息區 (SMB) 3.0 通訊協定</span><span class="sxs-lookup"><span data-stu-id="00d61-150">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="00d61-151">Yes</span><span class="sxs-lookup"><span data-stu-id="00d61-151">Yes</span></span><br/> |
| <span data-ttu-id="00d61-152">SMB 3.0 透明容錯移轉 (TFO) </span><span class="sxs-lookup"><span data-stu-id="00d61-152">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="00d61-153">Yes</span><span class="sxs-lookup"><span data-stu-id="00d61-153">Yes</span></span><br/> |
| <span data-ttu-id="00d61-154">具有向外延展檔案共用的 SMB 3.0 (因此) </span><span class="sxs-lookup"><span data-stu-id="00d61-154">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="00d61-155">Yes</span><span class="sxs-lookup"><span data-stu-id="00d61-155">Yes</span></span><br/> |
| <span data-ttu-id="00d61-156">叢集共用磁碟區檔案系統 (CsvFS) </span><span class="sxs-lookup"><span data-stu-id="00d61-156">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="00d61-157">Yes</span><span class="sxs-lookup"><span data-stu-id="00d61-157">Yes</span></span><br/> |
| <span data-ttu-id="00d61-158">彈性檔案系統 (ReFS)</span><span class="sxs-lookup"><span data-stu-id="00d61-158">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="00d61-159">Yes</span><span class="sxs-lookup"><span data-stu-id="00d61-159">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="00d61-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="00d61-160">Requirements</span></span>



| <span data-ttu-id="00d61-161">需求</span><span class="sxs-lookup"><span data-stu-id="00d61-161">Requirement</span></span> | <span data-ttu-id="00d61-162">值</span><span class="sxs-lookup"><span data-stu-id="00d61-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d61-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00d61-163">Minimum supported client</span></span><br/> | <span data-ttu-id="00d61-164">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00d61-164">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                   |
| <span data-ttu-id="00d61-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00d61-165">Minimum supported server</span></span><br/> | <span data-ttu-id="00d61-166">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00d61-166">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="00d61-167">標頭</span><span class="sxs-lookup"><span data-stu-id="00d61-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d61-168"><dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、windows 7、Windows Server 2008 和 Windows Vista (的 WinBase，包括 windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="00d61-168"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="00d61-169">程式庫</span><span class="sxs-lookup"><span data-stu-id="00d61-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="00d61-170"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="00d61-170"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="00d61-171">DLL</span><span class="sxs-lookup"><span data-stu-id="00d61-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00d61-172"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d61-172"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a><span data-ttu-id="00d61-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00d61-173">See also</span></span>

<dl> <dt>

<span data-ttu-id="00d61-174">**總覽主題**</span><span class="sxs-lookup"><span data-stu-id="00d61-174">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="00d61-175">檔案管理功能</span><span class="sxs-lookup"><span data-stu-id="00d61-175">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="00d61-176">I/o 完成埠</span><span class="sxs-lookup"><span data-stu-id="00d61-176">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="00d61-177">使用 Windows 標頭</span><span class="sxs-lookup"><span data-stu-id="00d61-177">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

<span data-ttu-id="00d61-178">**函數**</span><span class="sxs-lookup"><span data-stu-id="00d61-178">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="00d61-179">**ConnectNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="00d61-179">**ConnectNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[<span data-ttu-id="00d61-180">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="00d61-180">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="00d61-181">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="00d61-181">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="00d61-182">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="00d61-182">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="00d61-183">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="00d61-183">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="00d61-184">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="00d61-184">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="00d61-185">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="00d61-185">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="00d61-186">**TransactNamedPipe**</span><span class="sxs-lookup"><span data-stu-id="00d61-186">**TransactNamedPipe**</span></span>](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[<span data-ttu-id="00d61-187">**WaitCommEvent**</span><span class="sxs-lookup"><span data-stu-id="00d61-187">**WaitCommEvent**</span></span>](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[<span data-ttu-id="00d61-188">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="00d61-188">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

