---
description: 將 i/o 完成封包張貼至 i/o 完成通訊埠。
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: 'PostQueuedCompletionStatus 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995863"
---
# <a name="postqueuedcompletionstatus-function"></a><span data-ttu-id="f451d-103">PostQueuedCompletionStatus 函式</span><span class="sxs-lookup"><span data-stu-id="f451d-103">PostQueuedCompletionStatus function</span></span>

<span data-ttu-id="f451d-104">將 i/o 完成封包張貼至 i/o 完成通訊埠。</span><span class="sxs-lookup"><span data-stu-id="f451d-104">Posts an I/O completion packet to an I/O completion port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f451d-105">語法</span><span class="sxs-lookup"><span data-stu-id="f451d-105">Syntax</span></span>


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a><span data-ttu-id="f451d-106">參數</span><span class="sxs-lookup"><span data-stu-id="f451d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f451d-107">*CompletionPort* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f451d-107">*CompletionPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f451d-108">I/o 完成通訊埠的控制碼，i/o 完成封包將張貼至此。</span><span class="sxs-lookup"><span data-stu-id="f451d-108">A handle to an I/O completion port to which the I/O completion packet is to be posted.</span></span>

</dd> <dt>

<span data-ttu-id="f451d-109">*dwNumberOfBytesTransferred* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f451d-109">*dwNumberOfBytesTransferred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f451d-110">要透過 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)函數的 *lpNumberOfBytesTransferred* 參數傳回的值。</span><span class="sxs-lookup"><span data-stu-id="f451d-110">The value to be returned through the *lpNumberOfBytesTransferred* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="f451d-111">*dwCompletionKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f451d-111">*dwCompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f451d-112">要透過 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)函數的 *lpCompletionKey* 參數傳回的值。</span><span class="sxs-lookup"><span data-stu-id="f451d-112">The value to be returned through the *lpCompletionKey* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> <dt>

<span data-ttu-id="f451d-113">*lpOverlapped* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f451d-113">*lpOverlapped* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f451d-114">要透過 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)函數的 *lpOverlapped* 參數傳回的值。</span><span class="sxs-lookup"><span data-stu-id="f451d-114">The value to be returned through the *lpOverlapped* parameter of the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f451d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f451d-115">Return value</span></span>

<span data-ttu-id="f451d-116">如果函式成功，則傳回非零的值。</span><span class="sxs-lookup"><span data-stu-id="f451d-116">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="f451d-117">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="f451d-117">If the function fails, the return value is zero.</span></span> <span data-ttu-id="f451d-118">若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 。</span><span class="sxs-lookup"><span data-stu-id="f451d-118">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span></span>

## <a name="remarks"></a><span data-ttu-id="f451d-119">備註</span><span class="sxs-lookup"><span data-stu-id="f451d-119">Remarks</span></span>

<span data-ttu-id="f451d-120">I/o 完成封包會滿足 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函式的未完成呼叫。</span><span class="sxs-lookup"><span data-stu-id="f451d-120">The I/O completion packet will satisfy an outstanding call to the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="f451d-121">此函式會傳回三個值，這些值會傳遞為 **PostQueuedCompletionStatus** 呼叫的第二、第三和第四個參數。</span><span class="sxs-lookup"><span data-stu-id="f451d-121">This function returns with the three values passed as the second, third, and fourth parameters of the call to **PostQueuedCompletionStatus**.</span></span> <span data-ttu-id="f451d-122">系統不會使用或驗證這些值。</span><span class="sxs-lookup"><span data-stu-id="f451d-122">The system does not use or validate these values.</span></span> <span data-ttu-id="f451d-123">尤其是， *lpOverlapped* 參數不需要指向重迭的 [**結構。**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)</span><span class="sxs-lookup"><span data-stu-id="f451d-123">In particular, the *lpOverlapped* parameter need not point to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span>

<span data-ttu-id="f451d-124">在 Windows 8 和 Windows Server 2012 中，下列技術支援此功能。</span><span class="sxs-lookup"><span data-stu-id="f451d-124">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="f451d-125">技術</span><span class="sxs-lookup"><span data-stu-id="f451d-125">Technology</span></span>                                           | <span data-ttu-id="f451d-126">支援</span><span class="sxs-lookup"><span data-stu-id="f451d-126">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="f451d-127">伺服器訊息區 (SMB) 3.0 通訊協定</span><span class="sxs-lookup"><span data-stu-id="f451d-127">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="f451d-128">Yes</span><span class="sxs-lookup"><span data-stu-id="f451d-128">Yes</span></span><br/> |
| <span data-ttu-id="f451d-129">SMB 3.0 透明容錯移轉 (TFO) </span><span class="sxs-lookup"><span data-stu-id="f451d-129">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="f451d-130">Yes</span><span class="sxs-lookup"><span data-stu-id="f451d-130">Yes</span></span><br/> |
| <span data-ttu-id="f451d-131">具有向外延展檔案共用的 SMB 3.0 (因此) </span><span class="sxs-lookup"><span data-stu-id="f451d-131">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="f451d-132">Yes</span><span class="sxs-lookup"><span data-stu-id="f451d-132">Yes</span></span><br/> |
| <span data-ttu-id="f451d-133">叢集共用磁碟區檔案系統 (CsvFS) </span><span class="sxs-lookup"><span data-stu-id="f451d-133">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="f451d-134">Yes</span><span class="sxs-lookup"><span data-stu-id="f451d-134">Yes</span></span><br/> |
| <span data-ttu-id="f451d-135">彈性檔案系統 (ReFS)</span><span class="sxs-lookup"><span data-stu-id="f451d-135">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="f451d-136">Yes</span><span class="sxs-lookup"><span data-stu-id="f451d-136">Yes</span></span><br/> |



 

<span data-ttu-id="f451d-137">CsvFs 將會針對壓縮檔進行重新導向的 IO。</span><span class="sxs-lookup"><span data-stu-id="f451d-137">CsvFs will do redirected IO for compressed files.</span></span>

## <a name="requirements"></a><span data-ttu-id="f451d-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="f451d-138">Requirements</span></span>



| <span data-ttu-id="f451d-139">需求</span><span class="sxs-lookup"><span data-stu-id="f451d-139">Requirement</span></span> | <span data-ttu-id="f451d-140">值</span><span class="sxs-lookup"><span data-stu-id="f451d-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f451d-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f451d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f451d-142">Windows XP \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f451d-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f451d-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f451d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f451d-144">Windows Server 2003 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f451d-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="f451d-145">標頭</span><span class="sxs-lookup"><span data-stu-id="f451d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f451d-146"><dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP (的 WinBase，包括 windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f451d-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f451d-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="f451d-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="f451d-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f451d-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="f451d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="f451d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f451d-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f451d-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="f451d-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f451d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f451d-152">**CreateIoCompletionPort**</span><span class="sxs-lookup"><span data-stu-id="f451d-152">**CreateIoCompletionPort**</span></span>](createiocompletionport.md)
</dt> <dt>

[<span data-ttu-id="f451d-153">檔案管理功能</span><span class="sxs-lookup"><span data-stu-id="f451d-153">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="f451d-154">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="f451d-154">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="f451d-155">**重疊**</span><span class="sxs-lookup"><span data-stu-id="f451d-155">**OVERLAPPED**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

