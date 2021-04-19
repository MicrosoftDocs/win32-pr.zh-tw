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
# <a name="canceling-pending-io-operations"></a>解除擱置中的 i/o 作業

允許使用者取消緩慢或封鎖的 i/o 要求，可以增強應用程式的可用性和穩定性。 例如，如果對 [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) 函式的呼叫因為呼叫速度非常緩慢的裝置而遭到封鎖，則取消它可讓您使用新的參數重新呼叫，而不需要終止應用程式。

Windows Vista 擴充了取消功能，並包含取消同步作業的支援。

**注意**  呼叫 [**CancelIoEx**](cancelioex-func.md) 函數並不保證會取消 i/o 作業;正在處理作業的驅動程式必須支援取消作業，而且作業必須處於可取消的狀態。

## <a name="cancellation-considerations"></a>取消考慮

在設計取消呼叫的程式時，請記住下列考慮：

-   無法保證基礎驅動程式正確支援取消。
-   取消非同步 i/o 時，如果未提供任何重迭的結構給 [**CancelIoEx**](cancelioex-func.md) 函式，此函式會嘗試取消進程中所有線程上檔案的所有未處理 i/o。 每個執行緒都是個別處理的，因此在處理過執行緒之後，可能會先在檔案上啟動另一個 i/o，然後所有其他執行緒都已取消檔案的 i/o，因而導致同步處理問題。
-   取消非同步 i/o 時，請勿重複使用目標取消的重迭結構。 當 i/o 作業完成 (成功或取消狀態) 之後，系統就不會再使用重迭的結構，而且可以重複使用。
-   當取消同步 i/o 時，呼叫 [**CancelSynchronousIo**](cancelsynchronousio-func.md) 函式會嘗試取消執行緒上任何目前的同步呼叫。 您必須小心確保呼叫的同步處理正確;在一系列呼叫中發生錯誤的呼叫可能會遭到取消。 例如，如果針對同步作業呼叫 **CancelSynchronousIo** 函式，X，運算 Y 只會在該作業 X 完成後啟動， (正常運作，或發生錯誤) 。 如果呼叫運算 X 的執行緒接著開始另一個對 X 的同步呼叫，則取消呼叫可能會中斷這個新的 i/o 要求。
-   取消同步 i/o 時，請注意，每當應用程式的不同部分之間共用執行緒（例如，使用執行緒集區執行緒）時，就可以存在競爭情形。

## <a name="operations-that-cannot-be-canceled"></a>無法取消的作業

某些函數無法使用 [**CancelIo**](cancelio.md)、 [**CancelIoEx**](cancelioex-func.md)或 [**CancelSynchronousIo**](cancelsynchronousio-func.md) 函式取消。 其中有些函式已擴充為允許取消 (例如， [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) 函式) ，您應該改用這些函數。 除了支援取消之外，這些函數也有內建的回呼，可在追蹤作業進度時支援您。 下列函數不支援取消：

-   [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)-使用 [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
-   [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)-使用 [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)-使用 [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

如需詳細資訊，請參閱 [I/o 完成/取消指導方針](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)。

## <a name="canceling-asynchronous-io"></a>取消非同步 i/o

您可以從發出 i/o 作業之進程中的任何執行緒取消非同步 i/o。 您必須指定用來執行 i/o 的控制碼，並選擇性地指定用來執行 i/o 的重迭結構。 您可以檢查重迭結構或完成回呼中傳回的狀態，以判斷是否發生取消。 已 **\_ \_ 中止的錯誤** 作業狀態表示作業已取消。

下列範例顯示的常式會使用超時，並嘗試讀取作業，如果超時時間過期，則使用 [**CancelIoEx**](cancelioex-func.md) 函式來取消。


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



## <a name="canceling-synchronous-io"></a>正在取消同步 i/o

您可以從發出 i/o 作業之進程中的任何執行緒取消同步 i/o。 您必須指定目前正在執行 i/o 作業的執行緒控制碼。

下列範例顯示兩個常式：

-   **SynchronousIoWorker** 函式是一個工作者執行緒，它會從 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式的呼叫開始，執行一些同步檔案 i/o。 如果常式成功，則此常式後面會接著其他作業，這些作業不包含在此。 全域變數 *gCompletionStatus* 可以用來判斷所有作業是否成功，或作業失敗或已取消。 全域變數 *dwOperationInProgress* 會指出檔案 i/o 是否仍在進行中。

    **注意**  在此範例中，UI 執行緒也可以檢查工作者執行緒是否存在。

    **SynchronousIoWorker** 函式中不需要其他手動檢查，以確保如果在檔案 i/o 呼叫之間的短暫期間內要求取消，則會取消其餘的作業。

-   **MainUIThreadMessageHandler** 函式會在 UI 執行緒的視窗程式內模擬訊息處理常式。 使用者會要求一組同步檔案作業，方法是按一下會產生使用者定義視窗訊息的控制項， (在 **\_ MYSYNCOPS**) 所標記的區段中。 這會使用 **CreateFileThread** 函式建立新的執行緒，此函式接著會啟動 **SynchronousIoWorker** 函數。 當背景工作執行緒執行要求的 i/o 時，UI 執行緒會繼續處理訊息。 如果使用者決定取消未完成的作業 (通常是按一下 [取消] 按鈕) ，則由 **WM) \_ MYCANCEL** 所標記之區段中 (的常式會使用 **CreateFileThread** 函數所傳回的執行緒控制碼來呼叫 [**CancelSynchronousIo**](cancelsynchronousio-func.md)函數。 **CancelSynchronousIo** 函數會在取消嘗試之後立即傳回。 最後，使用者或應用程式稍後可能會要求其他相依于檔案作業是否已完成的操作。 在此情況下，由 **WM \_ PROCESSDATA** 標示之區段中的常式 () 會先確認作業已完成，然後執行清除作業。

    **注意**  在此範例中，由於作業順序中的任何位置都可能發生取消，因此呼叫端可能必須確保狀態一致或至少被瞭解，然後再繼續進行。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[同步和非同步 i/o](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



