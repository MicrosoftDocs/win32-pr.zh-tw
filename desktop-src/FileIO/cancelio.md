---
description: 取消所有暫止的輸入和輸出 (由呼叫執行緒針對指定檔案發出的 i/o) 作業。
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: 'CancelIo 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001698"
---
# <a name="cancelio-function"></a><span data-ttu-id="90369-103">CancelIo 函式</span><span class="sxs-lookup"><span data-stu-id="90369-103">CancelIo function</span></span>

<span data-ttu-id="90369-104">取消所有暫止的輸入和輸出 (由呼叫執行緒針對指定檔案發出的 i/o) 作業。</span><span class="sxs-lookup"><span data-stu-id="90369-104">Cancels all pending input and output (I/O) operations that are issued by the calling thread for the specified file.</span></span> <span data-ttu-id="90369-105">此函數不會取消其他執行緒針對檔案控制代碼發出的 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="90369-105">The function does not cancel I/O operations that other threads issue for a file handle.</span></span>

<span data-ttu-id="90369-106">若要取消另一個執行緒的 i/o 作業，請使用 [**CancelIoEx**](cancelioex-func.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="90369-106">To cancel I/O operations from another thread, use the [**CancelIoEx**](cancelioex-func.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="90369-107">語法</span><span class="sxs-lookup"><span data-stu-id="90369-107">Syntax</span></span>


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a><span data-ttu-id="90369-108">參數</span><span class="sxs-lookup"><span data-stu-id="90369-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90369-109">*hFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90369-109">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90369-110">檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="90369-110">A handle to the file.</span></span>

<span data-ttu-id="90369-111">此函式會取消此檔案控制代碼的所有暫止 i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="90369-111">The function cancels all pending I/O operations for this file handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90369-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="90369-112">Return value</span></span>

<span data-ttu-id="90369-113">如果函式成功，則傳回非零的值。</span><span class="sxs-lookup"><span data-stu-id="90369-113">If the function succeeds, the return value is nonzero.</span></span> <span data-ttu-id="90369-114">已成功要求呼叫執行緒針對指定檔案控制代碼發出的所有暫止 i/o 作業的取消作業。</span><span class="sxs-lookup"><span data-stu-id="90369-114">The cancel operation for all pending I/O operations issued by the calling thread for the specified file handle was successfully requested.</span></span> <span data-ttu-id="90369-115">執行緒可以使用 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來判斷 i/o 作業本身何時完成。</span><span class="sxs-lookup"><span data-stu-id="90369-115">The thread can use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to determine when the I/O operations themselves have been completed.</span></span>

<span data-ttu-id="90369-116">如果函式失敗，則傳回值為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="90369-116">If the function fails, the return value is zero (0).</span></span> <span data-ttu-id="90369-117">若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。</span><span class="sxs-lookup"><span data-stu-id="90369-117">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="90369-118">備註</span><span class="sxs-lookup"><span data-stu-id="90369-118">Remarks</span></span>

<span data-ttu-id="90369-119">如果指定的檔案控制代碼有任何正在進行的暫止 i/o 作業，而且這些作業是由呼叫執行緒所發出，則 **CancelIo** 函式會將它們取消。</span><span class="sxs-lookup"><span data-stu-id="90369-119">If there are any pending I/O operations in progress for the specified file handle, and they are issued by the calling thread, the **CancelIo** function cancels them.</span></span> <span data-ttu-id="90369-120">**CancelIo** 只會取消控制碼上的未處理 i/o，而不會變更控制碼的狀態。這表示您無法依賴控制碼的狀態，因為您無法得知作業是否已順利完成或取消。</span><span class="sxs-lookup"><span data-stu-id="90369-120">**CancelIo** cancels only outstanding I/O on the handle, it does not change the state of the handle; this means that you cannot rely on the state of the handle because you cannot know whether the operation was completed successfully or canceled.</span></span>

<span data-ttu-id="90369-121">I/o 作業必須發出為重迭的 i/o。</span><span class="sxs-lookup"><span data-stu-id="90369-121">The I/O operations must be issued as overlapped I/O.</span></span> <span data-ttu-id="90369-122">如果不是，i/o 作業就不會傳回，讓執行緒呼叫 **CancelIo** 函式。</span><span class="sxs-lookup"><span data-stu-id="90369-122">If they are not, the I/O operations do not return to allow the thread to call the **CancelIo** function.</span></span> <span data-ttu-id="90369-123">使用未以檔案 **\_ 旗 \_** 標重迭開啟的檔案控制代碼來呼叫 CancelIo 函式不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="90369-123">Calling the **CancelIo** function with a file handle that is not opened with **FILE\_FLAG\_OVERLAPPED** does nothing.</span></span>

<span data-ttu-id="90369-124">所有已取消且錯誤錯誤作業完成的 i/o 作業都會 **\_ \_ 中止**，且 i/o 作業的所有完成通知都會正常執行。</span><span class="sxs-lookup"><span data-stu-id="90369-124">All I/O operations that are canceled complete with the error **ERROR\_OPERATION\_ABORTED**, and all completion notifications for the I/O operations occur normally.</span></span>

<span data-ttu-id="90369-125">在 Windows 8 和 Windows Server 2012 中，下列技術支援此功能。</span><span class="sxs-lookup"><span data-stu-id="90369-125">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="90369-126">技術</span><span class="sxs-lookup"><span data-stu-id="90369-126">Technology</span></span>                                           | <span data-ttu-id="90369-127">支援</span><span class="sxs-lookup"><span data-stu-id="90369-127">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="90369-128">伺服器訊息區 (SMB) 3.0 通訊協定</span><span class="sxs-lookup"><span data-stu-id="90369-128">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="90369-129">Yes</span><span class="sxs-lookup"><span data-stu-id="90369-129">Yes</span></span><br/> |
| <span data-ttu-id="90369-130">SMB 3.0 透明容錯移轉 (TFO) </span><span class="sxs-lookup"><span data-stu-id="90369-130">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="90369-131">Yes</span><span class="sxs-lookup"><span data-stu-id="90369-131">Yes</span></span><br/> |
| <span data-ttu-id="90369-132">具有向外延展檔案共用的 SMB 3.0 (因此) </span><span class="sxs-lookup"><span data-stu-id="90369-132">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="90369-133">Yes</span><span class="sxs-lookup"><span data-stu-id="90369-133">Yes</span></span><br/> |
| <span data-ttu-id="90369-134">叢集共用磁碟區檔案系統 (CsvFS) </span><span class="sxs-lookup"><span data-stu-id="90369-134">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="90369-135">Yes</span><span class="sxs-lookup"><span data-stu-id="90369-135">Yes</span></span><br/> |
| <span data-ttu-id="90369-136">彈性檔案系統 (ReFS)</span><span class="sxs-lookup"><span data-stu-id="90369-136">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="90369-137">Yes</span><span class="sxs-lookup"><span data-stu-id="90369-137">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="90369-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="90369-138">Requirements</span></span>



| <span data-ttu-id="90369-139">需求</span><span class="sxs-lookup"><span data-stu-id="90369-139">Requirement</span></span> | <span data-ttu-id="90369-140">值</span><span class="sxs-lookup"><span data-stu-id="90369-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90369-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90369-141">Minimum supported client</span></span><br/> | <span data-ttu-id="90369-142">Windows XP \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90369-142">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="90369-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90369-143">Minimum supported server</span></span><br/> | <span data-ttu-id="90369-144">Windows Server 2003 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90369-144">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="90369-145">標頭</span><span class="sxs-lookup"><span data-stu-id="90369-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="90369-146"><dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP (的 WinBase，包括 windows .h) </dt></span><span class="sxs-lookup"><span data-stu-id="90369-146"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="90369-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="90369-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="90369-148"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="90369-148"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="90369-149">DLL</span><span class="sxs-lookup"><span data-stu-id="90369-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90369-150"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90369-150"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="90369-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90369-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90369-152">**CancelIoEx**</span><span class="sxs-lookup"><span data-stu-id="90369-152">**CancelIoEx**</span></span>](cancelioex-func.md)
</dt> <dt>

[<span data-ttu-id="90369-153">**CancelSynchronousIo**</span><span class="sxs-lookup"><span data-stu-id="90369-153">**CancelSynchronousIo**</span></span>](cancelsynchronousio-func.md)
</dt> <dt>

[<span data-ttu-id="90369-154">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="90369-154">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="90369-155">**DeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="90369-155">**DeviceIoControl**</span></span>](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[<span data-ttu-id="90369-156">檔案管理功能</span><span class="sxs-lookup"><span data-stu-id="90369-156">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="90369-157">**LockFileEx**</span><span class="sxs-lookup"><span data-stu-id="90369-157">**LockFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[<span data-ttu-id="90369-158">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="90369-158">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[<span data-ttu-id="90369-159">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="90369-159">**ReadFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[<span data-ttu-id="90369-160">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="90369-160">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="90369-161">同步和非同步 i/o</span><span class="sxs-lookup"><span data-stu-id="90369-161">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[<span data-ttu-id="90369-162">**WriteFile**</span><span class="sxs-lookup"><span data-stu-id="90369-162">**WriteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[<span data-ttu-id="90369-163">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="90369-163">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

