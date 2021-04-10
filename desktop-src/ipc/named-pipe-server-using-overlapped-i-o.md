---
description: 使用重迭作業來服務同時連線至多個管道用戶端之單一執行緒管道伺服器的程式碼範例。
ms.assetid: c0ac70cc-4ab9-47e5-b0e6-c0b373d16b25
title: 使用重迭 i/o 的具名管道伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f9134582a50c2053893cf6ee4908e447e3cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944385"
---
# <a name="named-pipe-server-using-overlapped-io"></a><span data-ttu-id="7d5b5-103">使用重迭 i/o 的具名管道伺服器</span><span class="sxs-lookup"><span data-stu-id="7d5b5-103">Named Pipe Server Using Overlapped I/O</span></span>

<span data-ttu-id="7d5b5-104">以下是單一執行緒管道伺服器的範例，此伺服器使用重迭作業來服務同時連線至多個管道用戶端。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-104">The following is an example of a single-threaded pipe server that uses overlapped operations to service simultaneous connections to multiple pipe clients.</span></span> <span data-ttu-id="7d5b5-105">管道伺服器會建立固定數目的管道實例。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-105">The pipe server creates a fixed number of pipe instances.</span></span> <span data-ttu-id="7d5b5-106">每個管道實例都可以連接到個別的管道用戶端。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-106">Each pipe instance can be connected to a separate pipe client.</span></span> <span data-ttu-id="7d5b5-107">當管道用戶端使用其管道實例完成時，伺服器會與用戶端中斷連接，並重複使用管道實例以連接到新的用戶端。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-107">When a pipe client has finished using its pipe instance, the server disconnects from the client and reuses the pipe instance to connect to a new client.</span></span> <span data-ttu-id="7d5b5-108">此管道伺服器可與 [具名管道用戶端](named-pipe-client.md)中所述的管道用戶端搭配使用。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-108">This pipe server can be used with the pipe client described in [Named Pipe Client](named-pipe-client.md).</span></span>

<span data-ttu-id="7d5b5-109">重 [**迭的結構**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 會指定為管線實例上每個 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)和 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 作業中的參數。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-109">The [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure is specified as a parameter in each [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation on the pipe instance.</span></span> <span data-ttu-id="7d5b5-110">雖然此範例顯示不同管道實例上的並行作業，但它會使用重 **迭結構中的事件** 物件，以避免在單一管道實例上進行同步作業。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-110">Although the example shows simultaneous operations on different pipe instances, it avoids simultaneous operations on a single pipe instance by using the event object in the **OVERLAPPED** structure.</span></span> <span data-ttu-id="7d5b5-111">因為每個實例都使用相同的事件物件來進行讀取、寫入和連接作業，所以無法得知哪一個作業的完成會導致事件被設定為使用相同管道實例之同時作業的已發出信號狀態。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-111">Because the same event object is used for read, write, and connect operations for each instance, there is no way to know which operation's completion caused the event to be set to the signaled state for simultaneous operations using the same pipe instance.</span></span>

<span data-ttu-id="7d5b5-112">每個管道實例的事件控制碼都會儲存在傳遞至 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) 函數的陣列中。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-112">The event handles for each pipe instance are stored in an array that is passed to the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function.</span></span> <span data-ttu-id="7d5b5-113">此函式會等候其中一個事件發出信號，並傳回導致等候作業完成之事件的陣列索引。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-113">This function waits for one of the events to be signaled, and returns the array index of the event that caused the wait operation to complete.</span></span> <span data-ttu-id="7d5b5-114">本主題中的範例會使用這個陣列索引來抓取包含管道實例資訊的結構。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-114">The example in this topic uses this array index to retrieve a structure containing information for the pipe instance.</span></span> <span data-ttu-id="7d5b5-115">伺服器會使用結構的 **fPendingIO** 成員來追蹤實例上最近的 i/o 作業是否暫止，而這需要呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-115">The server uses the **fPendingIO** member of the structure to keep track of whether the most recent I/O operation on the instance was pending, which requires a call to the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="7d5b5-116">伺服器會使用結構的 **dwState** 成員，判斷必須針對管道實例執行的下一項作業。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-116">The server uses the **dwState** member of the structure to determine the next operation that must be performed for the pipe instance.</span></span>

<span data-ttu-id="7d5b5-117">重迭的 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)和 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 作業可以在函數傳回時完成。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-117">Overlapped [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operations can finish by the time the function returns.</span></span> <span data-ttu-id="7d5b5-118">否則，如果作業暫止，則在函數傳回之前 [**，指定的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 重迭結構中的事件物件會設定為未收到信號狀態。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-118">Otherwise, if the operation is pending, the event object in the specified [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure is set to the nonsignaled state before the function returns.</span></span> <span data-ttu-id="7d5b5-119">當暫止的作業完成時，系統會將事件物件的狀態設定為已發出信號。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-119">When the pending operation finishes, the system sets the state of the event object to signaled.</span></span> <span data-ttu-id="7d5b5-120">如果作業在函數傳回之前完成，則不會變更事件物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-120">The state of the event object is not changed if the operation finishes before the function returns.</span></span>

<span data-ttu-id="7d5b5-121">因為此範例使用手動重設事件物件，所以 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) 函數不會將事件物件的狀態變更為未收到信號。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-121">Because the example uses manual-reset event objects, the state of an event object is not changed to nonsignaled by the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function.</span></span> <span data-ttu-id="7d5b5-122">這點很重要，因為此範例會依賴處於信號狀態中的事件物件，但有暫止的作業除外。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-122">This is important, because the example relies on the event objects remaining in the signaled state, except when there is a pending operation.</span></span>

<span data-ttu-id="7d5b5-123">如果 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)或 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 傳回時作業已完成，則函式的傳回值會指出結果。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-123">If the operation has already finished when [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), or [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) returns, the function's return value indicates the result.</span></span> <span data-ttu-id="7d5b5-124">針對讀取和寫入作業，也會傳回已傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-124">For read and write operations, the number of bytes transferred is also returned.</span></span> <span data-ttu-id="7d5b5-125">如果作業仍在暫止狀態， **ReadFile**、 **WriteFile** 或 **ConnectNamedPipe** 函數會傳回零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回錯誤 \_ IO \_ 暫止。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-125">If the operation is still pending, the **ReadFile**, **WriteFile**, or **ConnectNamedPipe** function returns zero and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_IO\_PENDING.</span></span> <span data-ttu-id="7d5b5-126">在此情況下，請在作業完成之後使用 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函式來取得結果。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-126">In this case, use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to retrieve the results after the operation has finished.</span></span> <span data-ttu-id="7d5b5-127">**GetOverlappedResult** 只會傳回暫止作業的結果。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-127">**GetOverlappedResult** returns only the results of pending operations.</span></span> <span data-ttu-id="7d5b5-128">它不會報告在重迭 **ReadFile**、 **WriteFile** 或 **ConnectNamedPipe** 函數傳回之前完成的作業結果。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-128">It does not report the results of operations that were completed before the overlapped **ReadFile**, **WriteFile**, or **ConnectNamedPipe** function returned.</span></span>

<span data-ttu-id="7d5b5-129">從用戶端中斷連線之前，您必須等待指出用戶端已完成的信號。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-129">Before disconnecting from a client, you must wait for a signal indicating the client has finished.</span></span> <span data-ttu-id="7d5b5-130"> (清除檔案緩衝區將會導致重迭 i/o 的用途，因為排清作業會在等候用戶端清空管道時封鎖伺服器執行緒的執行。在此範例中，此信號是在管道用戶端關閉其控制碼之後，嘗試從管道讀取所產生的錯誤 ) 。</span><span class="sxs-lookup"><span data-stu-id="7d5b5-130">(Flushing the file buffers would defeat the purpose of overlapped I/O, because the flush operation would block the execution of the server thread while it waits for the client to empty the pipe.) In this example, the signal is the error generated by trying to read from the pipe after the pipe client closes its handle.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>
 
#define CONNECTING_STATE 0 
#define READING_STATE 1 
#define WRITING_STATE 2 
#define INSTANCES 4 
#define PIPE_TIMEOUT 5000
#define BUFSIZE 4096
 
typedef struct 
{ 
   OVERLAPPED oOverlap; 
   HANDLE hPipeInst; 
   TCHAR chRequest[BUFSIZE]; 
   DWORD cbRead;
   TCHAR chReply[BUFSIZE];
   DWORD cbToWrite; 
   DWORD dwState; 
   BOOL fPendingIO; 
} PIPEINST, *LPPIPEINST; 
 
 
VOID DisconnectAndReconnect(DWORD); 
BOOL ConnectToNewClient(HANDLE, LPOVERLAPPED); 
VOID GetAnswerToRequest(LPPIPEINST); 
 
PIPEINST Pipe[INSTANCES]; 
HANDLE hEvents[INSTANCES]; 
 
int _tmain(VOID) 
{ 
   DWORD i, dwWait, cbRet, dwErr; 
   BOOL fSuccess; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
// The initial loop creates several instances of a named pipe 
// along with an event object for each instance.  An 
// overlapped ConnectNamedPipe operation is started for 
// each instance. 
 
   for (i = 0; i < INSTANCES; i++) 
   { 
 
   // Create an event object for this instance. 
 
      hEvents[i] = CreateEvent( 
         NULL,    // default security attribute 
         TRUE,    // manual-reset event 
         TRUE,    // initial state = signaled 
         NULL);   // unnamed event object 

      if (hEvents[i] == NULL) 
      {
         printf("CreateEvent failed with %d.\n", GetLastError()); 
         return 0;
      }
 
      Pipe[i].oOverlap.hEvent = hEvents[i]; 
 
      Pipe[i].hPipeInst = CreateNamedPipe( 
         lpszPipename,            // pipe name 
         PIPE_ACCESS_DUPLEX |     // read/write access 
         FILE_FLAG_OVERLAPPED,    // overlapped mode 
         PIPE_TYPE_MESSAGE |      // message-type pipe 
         PIPE_READMODE_MESSAGE |  // message-read mode 
         PIPE_WAIT,               // blocking mode 
         INSTANCES,               // number of instances 
         BUFSIZE*sizeof(TCHAR),   // output buffer size 
         BUFSIZE*sizeof(TCHAR),   // input buffer size 
         PIPE_TIMEOUT,            // client time-out 
         NULL);                   // default security attributes 

      if (Pipe[i].hPipeInst == INVALID_HANDLE_VALUE) 
      {
         printf("CreateNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
 
   // Call the subroutine to connect to the new client
 
      Pipe[i].fPendingIO = ConnectToNewClient( 
         Pipe[i].hPipeInst, 
         &Pipe[i].oOverlap); 
 
      Pipe[i].dwState = Pipe[i].fPendingIO ? 
         CONNECTING_STATE : // still connecting 
         READING_STATE;     // ready to read 
   } 
 
   while (1) 
   { 
   // Wait for the event object to be signaled, indicating 
   // completion of an overlapped read, write, or 
   // connect operation. 
 
      dwWait = WaitForMultipleObjects( 
         INSTANCES,    // number of event objects 
         hEvents,      // array of event objects 
         FALSE,        // does not wait for all 
         INFINITE);    // waits indefinitely 
 
   // dwWait shows which pipe completed the operation. 
 
      i = dwWait - WAIT_OBJECT_0;  // determines which pipe 
      if (i < 0 || i > (INSTANCES - 1)) 
      {
         printf("Index out of range.\n"); 
         return 0;
      }
 
   // Get the result if the operation was pending. 
 
      if (Pipe[i].fPendingIO) 
      { 
         fSuccess = GetOverlappedResult( 
            Pipe[i].hPipeInst, // handle to pipe 
            &Pipe[i].oOverlap, // OVERLAPPED structure 
            &cbRet,            // bytes transferred 
            FALSE);            // do not wait 
 
         switch (Pipe[i].dwState) 
         { 
         // Pending connect operation 
            case CONNECTING_STATE: 
               if (! fSuccess) 
               {
                   printf("Error %d.\n", GetLastError()); 
                   return 0;
               }
               Pipe[i].dwState = READING_STATE; 
               break; 
 
         // Pending read operation 
            case READING_STATE: 
               if (! fSuccess || cbRet == 0) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               }
               Pipe[i].cbRead = cbRet;
               Pipe[i].dwState = WRITING_STATE; 
               break; 
 
         // Pending write operation 
            case WRITING_STATE: 
               if (! fSuccess || cbRet != Pipe[i].cbToWrite) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               } 
               Pipe[i].dwState = READING_STATE; 
               break; 
 
            default: 
            {
               printf("Invalid pipe state.\n"); 
               return 0;
            }
         }  
      } 
 
   // The pipe state determines which operation to do next. 
 
      switch (Pipe[i].dwState) 
      { 
      // READING_STATE: 
      // The pipe instance is connected to the client 
      // and is ready to read a request from the client. 
 
         case READING_STATE: 
            fSuccess = ReadFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chRequest, 
               BUFSIZE*sizeof(TCHAR), 
               &Pipe[i].cbRead, 
               &Pipe[i].oOverlap); 
 
         // The read operation completed successfully. 
 
            if (fSuccess && Pipe[i].cbRead != 0) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = WRITING_STATE; 
               continue; 
            } 
 
         // The read operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
      // WRITING_STATE: 
      // The request was successfully read from the client. 
      // Get the reply data and write it to the client. 
 
         case WRITING_STATE: 
            GetAnswerToRequest(&Pipe[i]); 
 
            fSuccess = WriteFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chReply, 
               Pipe[i].cbToWrite, 
               &cbRet, 
               &Pipe[i].oOverlap); 
 
         // The write operation completed successfully. 
 
            if (fSuccess && cbRet == Pipe[i].cbToWrite) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = READING_STATE; 
               continue; 
            } 
 
         // The write operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
         default: 
         {
            printf("Invalid pipe state.\n"); 
            return 0;
         }
      } 
  } 
 
  return 0; 
} 
 
 
// DisconnectAndReconnect(DWORD) 
// This function is called when an error occurs or when the client 
// closes its handle to the pipe. Disconnect from this client, then 
// call ConnectNamedPipe to wait for another client to connect. 
 
VOID DisconnectAndReconnect(DWORD i) 
{ 
// Disconnect the pipe instance. 
 
   if (! DisconnectNamedPipe(Pipe[i].hPipeInst) ) 
   {
      printf("DisconnectNamedPipe failed with %d.\n", GetLastError());
   }
 
// Call a subroutine to connect to the new client. 
 
   Pipe[i].fPendingIO = ConnectToNewClient( 
      Pipe[i].hPipeInst, 
      &Pipe[i].oOverlap); 
 
   Pipe[i].dwState = Pipe[i].fPendingIO ? 
      CONNECTING_STATE : // still connecting 
      READING_STATE;     // ready to read 
} 
 
// ConnectToNewClient(HANDLE, LPOVERLAPPED) 
// This function is called to start an overlapped connect operation. 
// It returns TRUE if an operation is pending or FALSE if the 
// connection has been completed. 
 
BOOL ConnectToNewClient(HANDLE hPipe, LPOVERLAPPED lpo) 
{ 
   BOOL fConnected, fPendingIO = FALSE; 
 
// Start an overlapped connection for this pipe instance. 
   fConnected = ConnectNamedPipe(hPipe, lpo); 
 
// Overlapped ConnectNamedPipe should return zero. 
   if (fConnected) 
   {
      printf("ConnectNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   switch (GetLastError()) 
   { 
   // The overlapped connection in progress. 
      case ERROR_IO_PENDING: 
         fPendingIO = TRUE; 
         break; 
 
   // Client is already connected, so signal an event. 
 
      case ERROR_PIPE_CONNECTED: 
         if (SetEvent(lpo->hEvent)) 
            break; 
 
   // If an error occurs during the connect operation... 
      default: 
      {
         printf("ConnectNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
   } 
 
   return fPendingIO; 
}

VOID GetAnswerToRequest(LPPIPEINST pipe)
{
   _tprintf( TEXT("[%d] %s\n"), pipe->hPipeInst, pipe->chRequest);
   StringCchCopy( pipe->chReply, BUFSIZE, TEXT("Default answer from server") );
   pipe->cbToWrite = (lstrlen(pipe->chReply)+1)*sizeof(TCHAR);
}

```



## <a name="related-topics"></a><span data-ttu-id="7d5b5-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d5b5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d5b5-132">具名管道用戶端</span><span class="sxs-lookup"><span data-stu-id="7d5b5-132">Named Pipe Client</span></span>](named-pipe-client.md)
</dt> </dl>

 

 
