---
description: 允許使用者取消緩慢或封鎖的 i/o 要求，可以增強應用程式的可用性和穩定性。
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: 解除擱置中的 i/o 作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d108409eea32cf18a94f83bf7aacd282c60d3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990435"
---
# <a name="canceling-pending-io-operations"></a><span data-ttu-id="88816-103">解除擱置中的 i/o 作業</span><span class="sxs-lookup"><span data-stu-id="88816-103">Canceling Pending I/O Operations</span></span>

<span data-ttu-id="88816-104">允許使用者取消緩慢或封鎖的 i/o 要求，可以增強應用程式的可用性和穩定性。</span><span class="sxs-lookup"><span data-stu-id="88816-104">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span> <span data-ttu-id="88816-105">例如，如果對 [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) 函式的呼叫因為呼叫速度非常緩慢的裝置而遭到封鎖，則取消它可讓您使用新的參數重新呼叫，而不需要終止應用程式。</span><span class="sxs-lookup"><span data-stu-id="88816-105">For example, if a call to the [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) function is blocked because the call is to a very slow device, canceling it enables the call to be made again, with new parameters, without terminating the application.</span></span>

<span data-ttu-id="88816-106">Windows Vista 擴充了取消功能，並包含取消同步作業的支援。</span><span class="sxs-lookup"><span data-stu-id="88816-106">Windows Vista extends the cancellation capabilities and includes support for canceling synchronous operations.</span></span>

<span data-ttu-id="88816-107">**注意**  呼叫 [**CancelIoEx**](cancelioex-func.md) 函數並不保證會取消 i/o 作業;正在處理作業的驅動程式必須支援取消作業，而且作業必須處於可取消的狀態。</span><span class="sxs-lookup"><span data-stu-id="88816-107">**Note**  Calling the [**CancelIoEx**](cancelioex-func.md) function does not guarantee that an I/O operation will be canceled; the driver which is handling the operation must support cancellation and the operation must be in a state that can be canceled.</span></span>

## <a name="cancellation-considerations"></a><span data-ttu-id="88816-108">取消考慮</span><span class="sxs-lookup"><span data-stu-id="88816-108">Cancellation Considerations</span></span>

<span data-ttu-id="88816-109">在設計取消呼叫的程式時，請記住下列考慮：</span><span class="sxs-lookup"><span data-stu-id="88816-109">When programming cancellation calls, keep in mind the following considerations:</span></span>

-   <span data-ttu-id="88816-110">無法保證基礎驅動程式正確支援取消。</span><span class="sxs-lookup"><span data-stu-id="88816-110">There is no guarantee that underlying drivers correctly support cancellation.</span></span>
-   <span data-ttu-id="88816-111">取消非同步 i/o 時，如果未提供任何重迭的結構給 [**CancelIoEx**](cancelioex-func.md) 函式，此函式會嘗試取消進程中所有線程上檔案的所有未處理 i/o。</span><span class="sxs-lookup"><span data-stu-id="88816-111">When canceling asynchronous I/O, when no overlapped structure is supplied to the [**CancelIoEx**](cancelioex-func.md) function, the function attempts to cancel all outstanding I/O on the file on all threads in the process.</span></span> <span data-ttu-id="88816-112">每個執行緒都是個別處理的，因此在處理過執行緒之後，可能會先在檔案上啟動另一個 i/o，然後所有其他執行緒都已取消檔案的 i/o，因而導致同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="88816-112">Each thread is processed individually, so after a thread has been processed it may start another I/O on the file before all the other threads have had their I/O for the file canceled, causing synchronization issues.</span></span>
-   <span data-ttu-id="88816-113">取消非同步 i/o 時，請勿重複使用目標取消的重迭結構。</span><span class="sxs-lookup"><span data-stu-id="88816-113">When canceling asynchronous I/O, do not reuse overlapped structures with targeted cancellation.</span></span> <span data-ttu-id="88816-114">當 i/o 作業完成 (成功或取消狀態) 之後，系統就不會再使用重迭的結構，而且可以重複使用。</span><span class="sxs-lookup"><span data-stu-id="88816-114">Once the I/O operation completes (either successfully or with a canceled status) then the overlapped structure is no longer in use by the system and can be reused.</span></span>
-   <span data-ttu-id="88816-115">當取消同步 i/o 時，呼叫 [**CancelSynchronousIo**](cancelsynchronousio-func.md) 函式會嘗試取消執行緒上任何目前的同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="88816-115">When canceling synchronous I/O, calling the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function attempts to cancel any current synchronous call on the thread.</span></span> <span data-ttu-id="88816-116">您必須小心確保呼叫的同步處理正確;在一系列呼叫中發生錯誤的呼叫可能會遭到取消。</span><span class="sxs-lookup"><span data-stu-id="88816-116">You must take care to ensure the synchronization of the calls is correct; the wrong call in a series of calls could get canceled.</span></span> <span data-ttu-id="88816-117">例如，如果針對同步作業呼叫 **CancelSynchronousIo** 函式，X，運算 Y 只會在該作業 X 完成後啟動， (正常運作，或發生錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="88816-117">For example, if the **CancelSynchronousIo** function is called for a synchronous operation, X, operation Y only starts after that operation X is completed (normally or with an error).</span></span> <span data-ttu-id="88816-118">如果呼叫運算 X 的執行緒接著開始另一個對 X 的同步呼叫，則取消呼叫可能會中斷這個新的 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="88816-118">If the thread that called operation X then starts another synchronous call to X, the cancel call could interrupt this new I/O request.</span></span>
-   <span data-ttu-id="88816-119">取消同步 i/o 時，請注意，每當應用程式的不同部分之間共用執行緒（例如，使用執行緒集區執行緒）時，就可以存在競爭情形。</span><span class="sxs-lookup"><span data-stu-id="88816-119">When canceling synchronous I/O, be aware that a race condition can exist whenever a thread is shared between different parts of an application, for example, with a thread-pool thread.</span></span>

## <a name="operations-that-cannot-be-canceled"></a><span data-ttu-id="88816-120">無法取消的作業</span><span class="sxs-lookup"><span data-stu-id="88816-120">Operations That Cannot Be Canceled</span></span>

<span data-ttu-id="88816-121">某些函數無法使用 [**CancelIo**](cancelio.md)、 [**CancelIoEx**](cancelioex-func.md)或 [**CancelSynchronousIo**](cancelsynchronousio-func.md) 函式取消。</span><span class="sxs-lookup"><span data-stu-id="88816-121">Some functions cannot be canceled using the [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md), or [**CancelSynchronousIo**](cancelsynchronousio-func.md) function.</span></span> <span data-ttu-id="88816-122">其中有些函式已擴充為允許取消 (例如， [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) 函式) ，您應該改用這些函數。</span><span class="sxs-lookup"><span data-stu-id="88816-122">Some of these functions have been extended to allow cancellation (for example, the [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function) and you should use these instead.</span></span> <span data-ttu-id="88816-123">除了支援取消之外，這些函數也有內建的回呼，可在追蹤作業進度時支援您。</span><span class="sxs-lookup"><span data-stu-id="88816-123">In addition to supporting cancellation, these functions also have built-in callbacks to support you when tracking the progress of the operation.</span></span> <span data-ttu-id="88816-124">下列函數不支援取消：</span><span class="sxs-lookup"><span data-stu-id="88816-124">The following functions do not support cancellation:</span></span>

-   <span data-ttu-id="88816-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)-使用 [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span><span class="sxs-lookup"><span data-stu-id="88816-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)—use [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span></span>
-   <span data-ttu-id="88816-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)-使用 [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="88816-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   <span data-ttu-id="88816-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)-使用 [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="88816-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   [<span data-ttu-id="88816-128">**ReplaceFile**</span><span class="sxs-lookup"><span data-stu-id="88816-128">**ReplaceFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

<span data-ttu-id="88816-129">如需詳細資訊，請參閱 [I/o 完成/取消指導方針](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)。</span><span class="sxs-lookup"><span data-stu-id="88816-129">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

## <a name="canceling-asynchronous-io"></a><span data-ttu-id="88816-130">取消非同步 i/o</span><span class="sxs-lookup"><span data-stu-id="88816-130">Canceling Asynchronous I/O</span></span>

<span data-ttu-id="88816-131">您可以從發出 i/o 作業之進程中的任何執行緒取消非同步 i/o。</span><span class="sxs-lookup"><span data-stu-id="88816-131">You can cancel asynchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="88816-132">您必須指定用來執行 i/o 的控制碼，並選擇性地指定用來執行 i/o 的重迭結構。</span><span class="sxs-lookup"><span data-stu-id="88816-132">You must specify the handle which the I/O was performed on and, optionally, the overlapped structure that was used to perform the I/O.</span></span> <span data-ttu-id="88816-133">您可以檢查重迭結構或完成回呼中傳回的狀態，以判斷是否發生取消。</span><span class="sxs-lookup"><span data-stu-id="88816-133">You can determine if the cancel occurred by examining the status returned in the overlapped structure or in the completion callback.</span></span> <span data-ttu-id="88816-134">已 **\_ \_ 中止的錯誤** 作業狀態表示作業已取消。</span><span class="sxs-lookup"><span data-stu-id="88816-134">A status of **ERROR\_OPERATION\_ABORTED** indicates that the operation was canceled.</span></span>

<span data-ttu-id="88816-135">下列範例顯示的常式會使用超時，並嘗試讀取作業，如果超時時間過期，則使用 [**CancelIoEx**](cancelioex-func.md) 函式來取消。</span><span class="sxs-lookup"><span data-stu-id="88816-135">The following example shows a routine that takes a timeout and attempts a read operation, canceling it with the [**CancelIoEx**](cancelioex-func.md) function if the timeout expires.</span></span>


```C++
#include <windows.h>

BOOL DoCancelableRead(HANDLE hFile,
                 LPVOID lpBuffer,
                 DWORD nNumberOfBytesToRead,
                 LPDWORD lpNumberOfBytesRead,
                 LPOVERLAPPED lpOverlapped,
                 DWORD dwTimeout,
                 LPBOOL pbCancelCalled)
//
// Parameters:
//
//      hFile - An open handle to a readable file or device.
//
//      lpBuffer - A pointer to the buffer to store the data being read.
//
//      nNumberOfBytesToRead - The number of bytes to read from the file or 
//          device. Must be less than or equal to the actual size of
//          the buffer referenced by lpBuffer.
//
//      lpNumberOfBytesRead - A pointer to a DWORD to receive the number 
//          of bytes read after all I/O is complete or canceled.
//
//      lpOverlapped - A pointer to a preconfigured OVERLAPPED structure that
//          has a valid hEvent.
//          If the caller does not properly initialize this structure, this
//          routine will fail.
//
//      dwTimeout - The desired time-out, in milliseconds, for the I/O read.
//          After this time expires, the I/O is canceled.
// 
//      pbCancelCalled - A pointer to a Boolean to notify the caller if this
//          routine attempted to perform an I/O cancel.
//
// Return Value:
//
//      TRUE on success, FALSE on failure.
//
{
    BOOL result;
    DWORD waitTimer;
    BOOL bIoComplete = FALSE;
    const DWORD PollInterval = 100; // milliseconds

    // Initialize "out" parameters
    *pbCancelCalled = FALSE;
    *lpNumberOfBytesRead = 0;

    // Perform the I/O, in this case a read operation.
    result = ReadFile(hFile,
                  lpBuffer,
                  nNumberOfBytesToRead,
                  lpNumberOfBytesRead,
                  lpOverlapped );

    if (result == FALSE) 
    {
        if (GetLastError() != ERROR_IO_PENDING) 
        {
            // The function call failed. ToDo: Error logging and recovery.
            return FALSE; 
        }
    } 
    else 
    {
        // The I/O completed, done.
        return TRUE;
    }
        
    // The I/O is pending, so wait and see if the call times out.
    // If so, cancel the I/O using the CancelIoEx function.

    for (waitTimer = 0; waitTimer < dwTimeout; waitTimer += PollInterval)
    {
        result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, FALSE );
        if (result == FALSE)
        {
            if (GetLastError() != ERROR_IO_PENDING)
            {
                // The function call failed. ToDo: Error logging and recovery.
                return FALSE;
            }
            Sleep(PollInterval);
        }
        else
        {
            bIoComplete = TRUE;
            break;
        }
    }

    if (bIoComplete == FALSE) 
    {
        result = CancelIoEx( hFile, lpOverlapped );
        
        *pbCancelCalled = TRUE;

        if (result == TRUE || GetLastError() != ERROR_NOT_FOUND) 
        {
            // Wait for the I/O subsystem to acknowledge our cancellation.
            // Depending on the timing of the calls, the I/O might complete with a
            // cancellation status, or it might complete normally (if the ReadFile was
            // in the process of completing at the time CancelIoEx was called, or if
            // the device does not support cancellation).
            // This call specifies TRUE for the bWait parameter, which will block
            // until the I/O either completes or is canceled, thus resuming execution, 
            // provided the underlying device driver and associated hardware are functioning 
            // properly. If there is a problem with the driver it is better to stop 
            // responding here than to try to continue while masking the problem.

            result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, TRUE );

            // ToDo: check result and log errors. 
        }
    }

    return result;
}
```



## <a name="canceling-synchronous-io"></a><span data-ttu-id="88816-136">正在取消同步 i/o</span><span class="sxs-lookup"><span data-stu-id="88816-136">Canceling Synchronous I/O</span></span>

<span data-ttu-id="88816-137">您可以從發出 i/o 作業之進程中的任何執行緒取消同步 i/o。</span><span class="sxs-lookup"><span data-stu-id="88816-137">You can cancel synchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="88816-138">您必須指定目前正在執行 i/o 作業的執行緒控制碼。</span><span class="sxs-lookup"><span data-stu-id="88816-138">You must specify the handle to the thread which is currently performing the I/O operation.</span></span>

<span data-ttu-id="88816-139">下列範例顯示兩個常式：</span><span class="sxs-lookup"><span data-stu-id="88816-139">The following example shows two routines:</span></span>

-   <span data-ttu-id="88816-140">**SynchronousIoWorker** 函式是一個工作者執行緒，它會從 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式的呼叫開始，執行一些同步檔案 i/o。</span><span class="sxs-lookup"><span data-stu-id="88816-140">The **SynchronousIoWorker** function is a worker thread that implements some synchronous file I/O, starting with a call to the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="88816-141">如果常式成功，則此常式後面會接著其他作業，這些作業不包含在此。</span><span class="sxs-lookup"><span data-stu-id="88816-141">If the routine is successful, the routine can be followed by additional operations, which are not included here.</span></span> <span data-ttu-id="88816-142">全域變數 *gCompletionStatus* 可以用來判斷所有作業是否成功，或作業失敗或已取消。</span><span class="sxs-lookup"><span data-stu-id="88816-142">The global variable *gCompletionStatus* can be used to determine whether all operations succeeded or whether an operation failed or was canceled.</span></span> <span data-ttu-id="88816-143">全域變數 *dwOperationInProgress* 會指出檔案 i/o 是否仍在進行中。</span><span class="sxs-lookup"><span data-stu-id="88816-143">The global variable *dwOperationInProgress* indicates whether file I/O is still in progress.</span></span>

    <span data-ttu-id="88816-144">**注意**  在此範例中，UI 執行緒也可以檢查工作者執行緒是否存在。</span><span class="sxs-lookup"><span data-stu-id="88816-144">**Note**  In this example, the UI thread could also check for the existence of the worker thread.</span></span>

    <span data-ttu-id="88816-145">**SynchronousIoWorker** 函式中不需要其他手動檢查，以確保如果在檔案 i/o 呼叫之間的短暫期間內要求取消，則會取消其餘的作業。</span><span class="sxs-lookup"><span data-stu-id="88816-145">Additional manual checks, which are not included here, are required in the **SynchronousIoWorker** function is to ensure that if the cancellation was requested during the brief periods between file I/O calls, the rest of the operations will be canceled.</span></span>

-   <span data-ttu-id="88816-146">**MainUIThreadMessageHandler** 函式會在 UI 執行緒的視窗程式內模擬訊息處理常式。</span><span class="sxs-lookup"><span data-stu-id="88816-146">The **MainUIThreadMessageHandler** function simulates the message handler within a UI thread's window procedure.</span></span> <span data-ttu-id="88816-147">使用者會要求一組同步檔案作業，方法是按一下會產生使用者定義視窗訊息的控制項， (在 **\_ MYSYNCOPS**) 所標記的區段中。</span><span class="sxs-lookup"><span data-stu-id="88816-147">The user requests a set of synchronous file operations by clicking a control, which generates a user-defined window message, (in the section marked by **WM\_MYSYNCOPS**).</span></span> <span data-ttu-id="88816-148">這會使用 **CreateFileThread** 函式建立新的執行緒，此函式接著會啟動 **SynchronousIoWorker** 函數。</span><span class="sxs-lookup"><span data-stu-id="88816-148">This creates a new thread using the **CreateFileThread** function, which then starts the **SynchronousIoWorker** function is.</span></span> <span data-ttu-id="88816-149">當背景工作執行緒執行要求的 i/o 時，UI 執行緒會繼續處理訊息。</span><span class="sxs-lookup"><span data-stu-id="88816-149">The UI thread continues to process messages while the worker thread performs the requested I/O.</span></span> <span data-ttu-id="88816-150">如果使用者決定取消未完成的作業 (通常是按一下 [取消] 按鈕) ，則由 **WM) \_ MYCANCEL** 所標記之區段中 (的常式會使用 **CreateFileThread** 函數所傳回的執行緒控制碼來呼叫 [**CancelSynchronousIo**](cancelsynchronousio-func.md)函數。</span><span class="sxs-lookup"><span data-stu-id="88816-150">If the user decides to cancel the unfinished operations (typically by clicking a cancel button), the routine (in the section marked by **WM\_MYCANCEL**) calls the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function using the thread handle returned by the **CreateFileThread** function.</span></span> <span data-ttu-id="88816-151">**CancelSynchronousIo** 函數會在取消嘗試之後立即傳回。</span><span class="sxs-lookup"><span data-stu-id="88816-151">The **CancelSynchronousIo** function returns immediately after the cancellation attempt.</span></span> <span data-ttu-id="88816-152">最後，使用者或應用程式稍後可能會要求其他相依于檔案作業是否已完成的操作。</span><span class="sxs-lookup"><span data-stu-id="88816-152">Finally, the user or application may later request some other operation that depends on whether the file operations have completed.</span></span> <span data-ttu-id="88816-153">在此情況下，由 **WM \_ PROCESSDATA** 標示之區段中的常式 () 會先確認作業已完成，然後執行清除作業。</span><span class="sxs-lookup"><span data-stu-id="88816-153">In this case, the routine (in the section marked by **WM\_PROCESSDATA**) first verifies that the operations have completed and then executes the clean-up operations.</span></span>

    <span data-ttu-id="88816-154">**注意**  在此範例中，由於作業順序中的任何位置都可能發生取消，因此呼叫端可能必須確保狀態一致或至少被瞭解，然後再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="88816-154">**Note**  In this example, since the cancellation could have occurred anywhere in the sequence of operations, it may be necessary for the caller to ensure that the state is consistent, or at least understood, before proceeding.</span></span>


```C++
// User-defined codes for the message-pump, which is outside the scope 
// of this sample. Windows messaging and message pumps are well-documented
// elsewhere.
#define WM_MYSYNCOPS    1
#define WM_MYCANCEL     2
#define WM_PROCESSDATA  3

VOID SynchronousIoWorker( VOID *pv )
{
    LPCSTR lpFileName = (LPCSTR)pv;
    HANDLE hFile;
    g_dwOperationInProgress = TRUE;    
    g_CompletionStatus = ERROR_SUCCESS;
     
    hFile = CreateFileA(lpFileName,
                        GENERIC_READ,
                        0,
                        NULL,
                        OPEN_EXISTING,
                        0,
                        NULL);


    if (hFile != INVALID_HANDLE_VALUE) 
    {
        BOOL result = TRUE;
        // TODO: CreateFile succeeded. 
        // Insert your code to make more synchronous calls with hFile.
        // The result variable is assumed to act as the error flag here,
        // but can be whatever your code needs.
        
        if (result == FALSE) 
        {
            // An operation failed or was canceled. If it was canceled,
            // GetLastError() returns ERROR_OPERATION_ABORTED.

            g_CompletionStatus = GetLastError();            
        }
             
        CloseHandle(hFile);
    } 
    else 
    {
        // CreateFile failed or was canceled. If it was canceled,
        // GetLastError() returns ERROR_OPERATION_ABORTED.
        g_CompletionStatus = GetLastError();
    }

    g_dwOperationInProgress = FALSE;
}  


LRESULT
CALLBACK
MainUIThreadMessageHandler(HWND hwnd,
                           UINT uMsg,
                           WPARAM wParam,
                           LPARAM lParam)
{
    UNREFERENCED_PARAMETER(hwnd);
    UNREFERENCED_PARAMETER(wParam);
    UNREFERENCED_PARAMETER(lParam);
    HANDLE syncThread = INVALID_HANDLE_VALUE;

    //  Insert your initializations here.

    switch (uMsg) 
    {
        // User requested an operation on a file.  Insert your code to 
        // retrieve filename from parameters.
        case WM_MYSYNCOPS:    
            syncThread = CreateThread(
                          NULL,
                          0,
                          (LPTHREAD_START_ROUTINE)SynchronousIoWorker,
                          &g_lpFileName,
                          0,
                          NULL);

            if (syncThread == INVALID_HANDLE_VALUE) 
            {
                // Insert your code to handle the failure.
            }
        break;
    
        // User clicked a cancel button.
        case WM_MYCANCEL:
            if (syncThread != INVALID_HANDLE_VALUE) 
            {
                CancelSynchronousIo(syncThread);
            }
        break;

        // User requested other operations.
        case WM_PROCESSDATA:
            if (!g_dwOperationInProgress) 
            {
                if (g_CompletionStatus == ERROR_OPERATION_ABORTED) 
                {
                    // Insert your cleanup code here.
                } 
                else
                {
                    // Insert code to handle other cases.
                }
            }
        break;
    } 

    return TRUE;
} 
```



## <a name="related-topics"></a><span data-ttu-id="88816-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="88816-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88816-156">同步和非同步 i/o</span><span class="sxs-lookup"><span data-stu-id="88816-156">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



