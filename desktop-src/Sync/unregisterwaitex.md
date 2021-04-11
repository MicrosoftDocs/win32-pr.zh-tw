---
description: 取消 RegisterWaitForSingleObject 函式所發出的已註冊等候作業。
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: 'UnregisterWaitEx 函式 (Threadpoollegacyapiset) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849434"
---
# <a name="unregisterwaitex-function"></a><span data-ttu-id="52831-103">UnregisterWaitEx 函式</span><span class="sxs-lookup"><span data-stu-id="52831-103">UnregisterWaitEx function</span></span>

<span data-ttu-id="52831-104">取消 [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) 函式所發出的已註冊等候作業。</span><span class="sxs-lookup"><span data-stu-id="52831-104">Cancels a registered wait operation issued by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="52831-105">語法</span><span class="sxs-lookup"><span data-stu-id="52831-105">Syntax</span></span>


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a><span data-ttu-id="52831-106">參數</span><span class="sxs-lookup"><span data-stu-id="52831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52831-107">*WaitHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52831-107">*WaitHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52831-108">等候控制碼。</span><span class="sxs-lookup"><span data-stu-id="52831-108">The wait handle.</span></span> <span data-ttu-id="52831-109">[**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="52831-109">This handle is returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

</dd> <dt>

<span data-ttu-id="52831-110">*CompletionEvent* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="52831-110">*CompletionEvent* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="52831-111">在等候作業取消註冊時，要發出信號的事件物件控制碼。</span><span class="sxs-lookup"><span data-stu-id="52831-111">A handle to the event object to be signaled when the wait operation has been unregistered.</span></span> <span data-ttu-id="52831-112">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="52831-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="52831-113">如果這個參數是 **不正確 \_ 控制碼 \_ 值**，則函式會先等候所有回呼函數完成，然後再傳回。</span><span class="sxs-lookup"><span data-stu-id="52831-113">If this parameter is **INVALID\_HANDLE\_VALUE**, the function waits for all callback functions to complete before returning.</span></span>

<span data-ttu-id="52831-114">如果這個參數是 **Null**，函式會將計時器標示為刪除，並立即傳回。</span><span class="sxs-lookup"><span data-stu-id="52831-114">If this parameter is **NULL**, the function marks the timer for deletion and returns immediately.</span></span> <span data-ttu-id="52831-115">不過，大部分的呼叫端應該等候回呼函式完成，才能執行任何所需的清除。</span><span class="sxs-lookup"><span data-stu-id="52831-115">However, most callers should wait for the callback function to complete so they can perform any needed cleanup.</span></span>

<span data-ttu-id="52831-116">如果呼叫端提供此事件且函式成功，或函式因為 **錯誤 \_ IO \_ 暫** 止而失敗，請不要關閉事件，直到收到信號為止。</span><span class="sxs-lookup"><span data-stu-id="52831-116">If the caller provides this event and the function succeeds or the function fails with **ERROR\_IO\_PENDING**, do not close the event until it is signaled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52831-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="52831-117">Return value</span></span>

<span data-ttu-id="52831-118">如果函式成功，則傳回非零的值。</span><span class="sxs-lookup"><span data-stu-id="52831-118">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="52831-119">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="52831-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="52831-120">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="52831-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="52831-121">備註</span><span class="sxs-lookup"><span data-stu-id="52831-121">Remarks</span></span>

<span data-ttu-id="52831-122">您無法在相同等候作業的回呼函式中進行 **UnregisterWaitEx** 封鎖呼叫。</span><span class="sxs-lookup"><span data-stu-id="52831-122">You cannot make a blocking call to **UnregisterWaitEx** from within a callback function for the same wait operation.</span></span> <span data-ttu-id="52831-123">否則回呼將會等待其本身完成。</span><span class="sxs-lookup"><span data-stu-id="52831-123">Otherwise, the callback will be waiting for itself to finish.</span></span> <span data-ttu-id="52831-124">一般來說，封鎖呼叫 **UnregisterWaitEx** 會在目前的執行緒與回呼之間建立相依性，因此若要在另一個等候作業上封鎖取消註冊呼叫，您必須確定回呼函式不會彼此相依，而且第二個等候作業也不會在第一次作業時執行封鎖取消註冊呼叫。</span><span class="sxs-lookup"><span data-stu-id="52831-124">In general, a blocking call to **UnregisterWaitEx** creates a dependency between the current thread and the callback, so to make a blocking unregister call on another wait operation, you must ensure that the callback functions do not depend on one another and that the second wait operation does not also perform a blocking unregister call on the first operation.</span></span>

<span data-ttu-id="52831-125">在持續性執行緒上進行封鎖 **UnregisterWaitEx** 呼叫時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="52831-125">Be careful when making a blocking **UnregisterWaitEx** call on a persistent thread.</span></span> <span data-ttu-id="52831-126">如果正在取消註冊的等候作業是使用 **Wt. \_ EXECUTEINPERSISTENTTHREAD** 所建立，則可能會發生鎖死。</span><span class="sxs-lookup"><span data-stu-id="52831-126">If the wait operation being unregistered was created with **WT\_EXECUTEINPERSISTENTTHREAD**, a deadlock may occur.</span></span>

<span data-ttu-id="52831-127">在對 **UnregisterWaitEx** 進行非封鎖呼叫之後，不會將任何與 *WaitHandle* 相關聯的新回呼函式排入佇列。</span><span class="sxs-lookup"><span data-stu-id="52831-127">After making non-blocking call to **UnregisterWaitEx**, no new callback functions associated with *WaitHandle* can be queued.</span></span> <span data-ttu-id="52831-128">不過，可能有暫止的回呼函式已排入工作者執行緒佇列中。</span><span class="sxs-lookup"><span data-stu-id="52831-128">However, there may be pending callback functions already queued to worker threads.</span></span>

<span data-ttu-id="52831-129">在某些情況下，如果 *CompletionEvent* 為 **Null**，函式將會失敗，而且 **錯誤 IO 會 \_ \_ 處於擱置狀態**。</span><span class="sxs-lookup"><span data-stu-id="52831-129">Under some conditions, the function will fail with **ERROR\_IO\_PENDING** if *CompletionEvent* is **NULL**.</span></span> <span data-ttu-id="52831-130">這表示有未處理的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="52831-130">This indicates that there are outstanding callback functions.</span></span> <span data-ttu-id="52831-131">這些回呼可能會執行或正在執行中。</span><span class="sxs-lookup"><span data-stu-id="52831-131">Those callbacks either will execute or are in the middle of executing.</span></span>

<span data-ttu-id="52831-132">如果 *CompletionEvent* 是呼叫端所提供事件的控制碼，則函式可能會成功，因為 **錯誤 \_ IO \_ 暫** 止而失敗，或因不同的錯誤碼而失敗。</span><span class="sxs-lookup"><span data-stu-id="52831-132">If *CompletionEvent* is a handle to an event provided by the caller, it is possible for the function to succeed, fail with **ERROR\_IO\_PENDING**, or fail with a different error code.</span></span> <span data-ttu-id="52831-133">如果函式成功，或如果函式因為 **錯誤 \_ IO \_ 暫** 止而失敗，則呼叫端應該一律等候，直到發出事件的信號關閉為止。</span><span class="sxs-lookup"><span data-stu-id="52831-133">If the function succeeds, or if the function fails with **ERROR\_IO\_PENDING**, the caller should always wait until the event is signaled to close the event.</span></span> <span data-ttu-id="52831-134">如果函式失敗，並出現不同的錯誤碼，就不需要等到事件被告知關閉事件。</span><span class="sxs-lookup"><span data-stu-id="52831-134">If the function fails with a different error code, it is not necessary to wait until the event is signaled to close the event.</span></span>

<span data-ttu-id="52831-135">**WINDOWS XP：** 如果 *CompletionEvent* 是呼叫端所提供事件的控制碼，且此函式因為 **錯誤 \_ IO \_ 暫** 止而失敗，則呼叫端應等候事件收到信號，以關閉事件。</span><span class="sxs-lookup"><span data-stu-id="52831-135">**Windows XP:** If *CompletionEvent* is a handle to an event provided by the caller and the function fails with **ERROR\_IO\_PENDING**, the caller should wait until the event is signaled to close the event.</span></span> <span data-ttu-id="52831-136">從 Windows Vista 開始，此行為已變更。</span><span class="sxs-lookup"><span data-stu-id="52831-136">This behavior changed starting with Windows Vista.</span></span>

<span data-ttu-id="52831-137">若要編譯使用此函數的應用程式，請將 **\_ WIN32 \_ WINNT** 定義為0x0500 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="52831-137">To compile an application that uses this function, define **\_WIN32\_WINNT** as 0x0500 or later.</span></span> <span data-ttu-id="52831-138">如需詳細資訊，請參閱 [使用 Windows 標頭](../winprog/using-the-windows-headers.md)。</span><span class="sxs-lookup"><span data-stu-id="52831-138">For more information, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52831-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="52831-139">Requirements</span></span>



| <span data-ttu-id="52831-140">需求</span><span class="sxs-lookup"><span data-stu-id="52831-140">Requirement</span></span> | <span data-ttu-id="52831-141">值</span><span class="sxs-lookup"><span data-stu-id="52831-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52831-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52831-142">Minimum supported client</span></span><br/> | <span data-ttu-id="52831-143">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52831-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="52831-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52831-144">Minimum supported server</span></span><br/> | <span data-ttu-id="52831-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52831-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="52831-146">標頭</span><span class="sxs-lookup"><span data-stu-id="52831-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="52831-147"><dt>Windows 8 和 Windows Server 2012 上的 Threadpoollegacyapiset .h (包含 Windows .h) ;</dt><dt>在 windows 7、Windows server 2008 R2、Windows Vista、Windows server 2008、WINDOWS XP 及 Windows server 2003 上的 WinBase .h (包括 windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="52831-147"><dt>Threadpoollegacyapiset.h on Windows 8 and Windows Server 2012 (include Windows.h); </dt> <dt>WinBase.h on Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003 (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="52831-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="52831-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="52831-149"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="52831-149"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="52831-150">DLL</span><span class="sxs-lookup"><span data-stu-id="52831-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52831-151"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52831-151"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a><span data-ttu-id="52831-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52831-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52831-153">**RegisterWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="52831-153">**RegisterWaitForSingleObject**</span></span>](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[<span data-ttu-id="52831-154">同步處理函式</span><span class="sxs-lookup"><span data-stu-id="52831-154">Synchronization Functions</span></span>](synchronization-functions.md)
</dt> <dt>

[<span data-ttu-id="52831-155">執行緒共用</span><span class="sxs-lookup"><span data-stu-id="52831-155">Thread Pooling</span></span>](../procthread/thread-pooling.md)
</dt> </dl>

 

 
