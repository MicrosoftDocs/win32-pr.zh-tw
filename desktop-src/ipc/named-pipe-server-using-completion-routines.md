---
description: 程式碼範例是單一執行緒的管道伺服器，可建立訊息類型管道並使用重迭的作業。
ms.assetid: 8b73485c-c6f7-44df-9e53-308df2c752e7
title: 使用完成常式的具名管道伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa3ac238680de5cee701488bc4cd60f6543d991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972588"
---
# <a name="named-pipe-server-using-completion-routines"></a><span data-ttu-id="66c6c-103">使用完成常式的具名管道伺服器</span><span class="sxs-lookup"><span data-stu-id="66c6c-103">Named Pipe Server Using Completion Routines</span></span>

<span data-ttu-id="66c6c-104">下列範例是建立訊息類型管道並使用重迭作業的單一執行緒管道伺服器。</span><span class="sxs-lookup"><span data-stu-id="66c6c-104">The following example is a single-threaded pipe server that creates a message-type pipe and uses overlapped operations.</span></span> <span data-ttu-id="66c6c-105">它使用擴充的函式 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) 和 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) ，利用完成常式來執行重迭的 i/o，此常式會在作業完成時排入佇列等候執行。</span><span class="sxs-lookup"><span data-stu-id="66c6c-105">It uses the extended functions [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) to perform overlapped I/O using a completion routine, which is queued for execution when the operation is finished.</span></span> <span data-ttu-id="66c6c-106">管道伺服器使用 [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) 函式，它會執行可在完成常式準備好執行時傳回的可提供警示等候作業。</span><span class="sxs-lookup"><span data-stu-id="66c6c-106">The pipe server uses the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function, which performs an alertable wait operation that returns when a completion routine is ready to execute.</span></span> <span data-ttu-id="66c6c-107">當事件物件發出信號時，wait 函式也會傳回，在此範例中，這表示重迭的 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 作業已 (新的用戶端已連線) 完成。</span><span class="sxs-lookup"><span data-stu-id="66c6c-107">The wait function also returns when an event object is signaled, which in this example indicates that the overlapped [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation has finished (a new client has connected).</span></span> <span data-ttu-id="66c6c-108">此管道伺服器可與 [具名管道用戶端](named-pipe-client.md)中所述的管道用戶端搭配使用。</span><span class="sxs-lookup"><span data-stu-id="66c6c-108">This pipe server can be used with the pipe client described in [Named Pipe Client](named-pipe-client.md).</span></span>

<span data-ttu-id="66c6c-109">一開始，管道伺服器會建立管道的單一實例，並啟動重迭的 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 作業。</span><span class="sxs-lookup"><span data-stu-id="66c6c-109">Initially, the pipe server creates a single instance of the pipe and starts an overlapped [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation.</span></span> <span data-ttu-id="66c6c-110">當用戶端連線時，伺服器會配置結構以提供該管道實例的儲存區，然後呼叫 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) 函式來啟動一連串的 i/o 作業，以處理與用戶端的通訊。</span><span class="sxs-lookup"><span data-stu-id="66c6c-110">When a client connects, the server allocates a structure to provide storage for that pipe instance and then calls the [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) function to start a sequence of I/O operations to handle communications with the client.</span></span> <span data-ttu-id="66c6c-111">每個作業都會指定執行序列中下一個作業的完成常式。</span><span class="sxs-lookup"><span data-stu-id="66c6c-111">Each operation specifies a completion routine that performs the next operation in the sequence.</span></span> <span data-ttu-id="66c6c-112">當用戶端已中斷連線且管道實例關閉時，此序列就會終止。</span><span class="sxs-lookup"><span data-stu-id="66c6c-112">The sequence terminates when the client is disconnected and the pipe instance closed.</span></span> <span data-ttu-id="66c6c-113">開始新用戶端的作業序列之後，伺服器會建立另一個管道實例，並等候下一個用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="66c6c-113">After starting the sequence of operations for the new client, the server creates another pipe instance and waits for the next client to connect.</span></span>

<span data-ttu-id="66c6c-114">[**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)和 [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)函數的參數會指定完成常式和重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)指標。</span><span class="sxs-lookup"><span data-stu-id="66c6c-114">The parameters of the [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) functions specify a completion routine and a pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="66c6c-115">此指標會在其 *lpOverLap* 參數中傳遞至完成常式。</span><span class="sxs-lookup"><span data-stu-id="66c6c-115">This pointer is passed to the completion routine in its *lpOverLap* parameter.</span></span> <span data-ttu-id="66c6c-116">因為重 **迭的結構** 會指向為每個管道實例配置之結構中的第一個成員，所以完成常式可以使用其 *lpOverLap* 參數來存取管道實例的結構。</span><span class="sxs-lookup"><span data-stu-id="66c6c-116">Because the **OVERLAPPED** structure points to the first member in the structure allocated for each pipe instance, the completion routine can use its *lpOverLap* parameter to access the structure for the pipe instance.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>

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
} PIPEINST, *LPPIPEINST; 
 
VOID DisconnectAndClose(LPPIPEINST); 
BOOL CreateAndConnectInstance(LPOVERLAPPED); 
BOOL ConnectToNewClient(HANDLE, LPOVERLAPPED); 
VOID GetAnswerToRequest(LPPIPEINST); 

VOID WINAPI CompletedWriteRoutine(DWORD, DWORD, LPOVERLAPPED); 
VOID WINAPI CompletedReadRoutine(DWORD, DWORD, LPOVERLAPPED); 
 
HANDLE hPipe; 
 
int _tmain(VOID) 
{ 
   HANDLE hConnectEvent; 
   OVERLAPPED oConnect; 
   LPPIPEINST lpPipeInst; 
   DWORD dwWait, cbRet; 
   BOOL fSuccess, fPendingIO; 
 
// Create one event object for the connect operation. 
 
   hConnectEvent = CreateEvent( 
      NULL,    // default security attribute
      TRUE,    // manual reset event 
      TRUE,    // initial state = signaled 
      NULL);   // unnamed event object 

   if (hConnectEvent == NULL) 
   {
      printf("CreateEvent failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   oConnect.hEvent = hConnectEvent; 
 
// Call a subroutine to create one instance, and wait for 
// the client to connect. 
 
   fPendingIO = CreateAndConnectInstance(&oConnect); 
 
   while (1) 
   { 
   // Wait for a client to connect, or for a read or write 
   // operation to be completed, which causes a completion 
   // routine to be queued for execution. 
 
      dwWait = WaitForSingleObjectEx( 
         hConnectEvent,  // event object to wait for 
         INFINITE,       // waits indefinitely 
         TRUE);          // alertable wait enabled 
 
      switch (dwWait) 
      { 
      // The wait conditions are satisfied by a completed connect 
      // operation. 
         case 0: 
         // If an operation is pending, get the result of the 
         // connect operation. 
 
         if (fPendingIO) 
         { 
            fSuccess = GetOverlappedResult( 
               hPipe,     // pipe handle 
               &oConnect, // OVERLAPPED structure 
               &cbRet,    // bytes transferred 
               FALSE);    // does not wait 
            if (!fSuccess) 
            {
               printf("ConnectNamedPipe (%d)\n", GetLastError()); 
               return 0;
            }
         } 
 
         // Allocate storage for this instance. 
 
            lpPipeInst = (LPPIPEINST) GlobalAlloc( 
               GPTR, sizeof(PIPEINST)); 
            if (lpPipeInst == NULL) 
            {
               printf("GlobalAlloc failed (%d)\n", GetLastError()); 
               return 0;
            }
 
            lpPipeInst->hPipeInst = hPipe; 
 
         // Start the read operation for this client. 
         // Note that this same routine is later used as a 
         // completion routine after a write operation. 
 
            lpPipeInst->cbToWrite = 0; 
            CompletedWriteRoutine(0, 0, (LPOVERLAPPED) lpPipeInst); 
 
         // Create new pipe instance for the next client. 
 
            fPendingIO = CreateAndConnectInstance( 
               &oConnect); 
            break; 
 
      // The wait is satisfied by a completed read or write 
      // operation. This allows the system to execute the 
      // completion routine. 
 
         case WAIT_IO_COMPLETION: 
            break; 
 
      // An error occurred in the wait function. 
 
         default: 
         {
            printf("WaitForSingleObjectEx (%d)\n", GetLastError()); 
            return 0;
         }
      } 
   } 
   return 0; 
} 
 
// CompletedWriteRoutine(DWORD, DWORD, LPOVERLAPPED) 
// This routine is called as a completion routine after writing to 
// the pipe, or when a new client has connected to a pipe instance.
// It starts another read operation. 
 
VOID WINAPI CompletedWriteRoutine(DWORD dwErr, DWORD cbWritten, 
   LPOVERLAPPED lpOverLap) 
{ 
   LPPIPEINST lpPipeInst; 
   BOOL fRead = FALSE; 
 
// lpOverlap points to storage for this instance. 
 
   lpPipeInst = (LPPIPEINST) lpOverLap; 
 
// The write operation has finished, so read the next request (if 
// there is no error). 
 
   if ((dwErr == 0) && (cbWritten == lpPipeInst->cbToWrite)) 
      fRead = ReadFileEx( 
         lpPipeInst->hPipeInst, 
         lpPipeInst->chRequest, 
         BUFSIZE*sizeof(TCHAR), 
         (LPOVERLAPPED) lpPipeInst, 
         (LPOVERLAPPED_COMPLETION_ROUTINE) CompletedReadRoutine); 
 
// Disconnect if an error occurred. 
 
   if (! fRead) 
      DisconnectAndClose(lpPipeInst); 
} 
 
// CompletedReadRoutine(DWORD, DWORD, LPOVERLAPPED) 
// This routine is called as an I/O completion routine after reading 
// a request from the client. It gets data and writes it to the pipe. 
 
VOID WINAPI CompletedReadRoutine(DWORD dwErr, DWORD cbBytesRead, 
    LPOVERLAPPED lpOverLap) 
{ 
   LPPIPEINST lpPipeInst; 
   BOOL fWrite = FALSE; 
 
// lpOverlap points to storage for this instance. 
 
   lpPipeInst = (LPPIPEINST) lpOverLap; 
 
// The read operation has finished, so write a response (if no 
// error occurred). 
 
   if ((dwErr == 0) && (cbBytesRead != 0)) 
   { 
      GetAnswerToRequest(lpPipeInst); 
 
      fWrite = WriteFileEx( 
         lpPipeInst->hPipeInst, 
         lpPipeInst->chReply, 
         lpPipeInst->cbToWrite, 
         (LPOVERLAPPED) lpPipeInst, 
         (LPOVERLAPPED_COMPLETION_ROUTINE) CompletedWriteRoutine); 
   } 
 
// Disconnect if an error occurred. 
 
   if (! fWrite) 
      DisconnectAndClose(lpPipeInst); 
} 
 
// DisconnectAndClose(LPPIPEINST) 
// This routine is called when an error occurs or the client closes 
// its handle to the pipe. 
 
VOID DisconnectAndClose(LPPIPEINST lpPipeInst) 
{ 
// Disconnect the pipe instance. 
 
   if (! DisconnectNamedPipe(lpPipeInst->hPipeInst) ) 
   {
      printf("DisconnectNamedPipe failed with %d.\n", GetLastError());
   }
 
// Close the handle to the pipe instance. 
 
   CloseHandle(lpPipeInst->hPipeInst); 
 
// Release the storage for the pipe instance. 
 
   if (lpPipeInst != NULL) 
      GlobalFree(lpPipeInst); 
} 
 
// CreateAndConnectInstance(LPOVERLAPPED) 
// This function creates a pipe instance and connects to the client. 
// It returns TRUE if the connect operation is pending, and FALSE if 
// the connection has been completed. 
 
BOOL CreateAndConnectInstance(LPOVERLAPPED lpoOverlap) 
{ 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
   hPipe = CreateNamedPipe( 
      lpszPipename,             // pipe name 
      PIPE_ACCESS_DUPLEX |      // read/write access 
      FILE_FLAG_OVERLAPPED,     // overlapped mode 
      PIPE_TYPE_MESSAGE |       // message-type pipe 
      PIPE_READMODE_MESSAGE |   // message read mode 
      PIPE_WAIT,                // blocking mode 
      PIPE_UNLIMITED_INSTANCES, // unlimited instances 
      BUFSIZE*sizeof(TCHAR),    // output buffer size 
      BUFSIZE*sizeof(TCHAR),    // input buffer size 
      PIPE_TIMEOUT,             // client time-out 
      NULL);                    // default security attributes
   if (hPipe == INVALID_HANDLE_VALUE) 
   {
      printf("CreateNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
// Call a subroutine to connect to the new client. 
 
   return ConnectToNewClient(hPipe, lpoOverlap); 
}

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



## <a name="related-topics"></a><span data-ttu-id="66c6c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="66c6c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66c6c-118">具名管道用戶端</span><span class="sxs-lookup"><span data-stu-id="66c6c-118">Named Pipe Client</span></span>](named-pipe-client.md)
</dt> </dl>

 

 
