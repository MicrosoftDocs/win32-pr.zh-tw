---
description: 多執行緒管道伺服器的程式碼範例。
ms.assetid: 4657e814-0e7f-45b5-8ddb-17ec0c3612ba
title: 多執行緒管道伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f974ad5ce23b850ab900ea4d34a219851528ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851008"
---
# <a name="multithreaded-pipe-server"></a><span data-ttu-id="0a648-103">多執行緒管道伺服器</span><span class="sxs-lookup"><span data-stu-id="0a648-103">Multithreaded Pipe Server</span></span>

<span data-ttu-id="0a648-104">下列範例是多執行緒管道伺服器。</span><span class="sxs-lookup"><span data-stu-id="0a648-104">The following example is a multithreaded pipe server.</span></span> <span data-ttu-id="0a648-105">它有一個具有迴圈的主執行緒，可建立管道實例，並等候管道用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="0a648-105">It has a main thread with a loop that creates a pipe instance and waits for a pipe client to connect.</span></span> <span data-ttu-id="0a648-106">當管道用戶端連接時，管道伺服器會建立一個執行緒來服務該用戶端，然後繼續在主執行緒中執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="0a648-106">When a pipe client connects, the pipe server creates a thread to service that client and then continues to execute the loop in the main thread.</span></span> <span data-ttu-id="0a648-107">管道用戶端可能會在呼叫 [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) 和 [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) 函數之間的間隔內，成功連接到管道實例。</span><span class="sxs-lookup"><span data-stu-id="0a648-107">It is possible for a pipe client to connect successfully to the pipe instance in the interval between calls to the [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) functions.</span></span> <span data-ttu-id="0a648-108">如果發生這種情況， **ConnectNamedPipe** 會傳回零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 \_ \_ 已連接的錯誤管道。</span><span class="sxs-lookup"><span data-stu-id="0a648-108">If this happens, **ConnectNamedPipe** returns zero, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_PIPE\_CONNECTED.</span></span>

<span data-ttu-id="0a648-109">建立用來服務每個管道實例的執行緒會從管道讀取要求，並將回應寫入管道，直到管道用戶端關閉其控制碼為止。</span><span class="sxs-lookup"><span data-stu-id="0a648-109">The thread created to service each pipe instance reads requests from the pipe and writes replies to the pipe until the pipe client closes its handle.</span></span> <span data-ttu-id="0a648-110">發生這種情況時，執行緒會排清管道、中斷連接、關閉其管道控制碼，然後終止。</span><span class="sxs-lookup"><span data-stu-id="0a648-110">When this happens, the thread flushes the pipe, disconnects, closes its pipe handle, and terminates.</span></span> <span data-ttu-id="0a648-111">主執行緒將會執行，直到發生錯誤或進程結束為止。</span><span class="sxs-lookup"><span data-stu-id="0a648-111">The main thread will run until an error occurs or the process is ended.</span></span>

<span data-ttu-id="0a648-112">此管道伺服器可與 [具名管道用戶端](named-pipe-client.md)中所述的管道用戶端搭配使用。</span><span class="sxs-lookup"><span data-stu-id="0a648-112">This pipe server can be used with the pipe client described in [Named Pipe Client](named-pipe-client.md).</span></span>


```C++
#include <windows.h> 
#include <stdio.h> 
#include <tchar.h>
#include <strsafe.h>

#define BUFSIZE 512
 
DWORD WINAPI InstanceThread(LPVOID); 
VOID GetAnswerToRequest(LPTSTR, LPTSTR, LPDWORD); 
 
int _tmain(VOID) 
{ 
   BOOL   fConnected = FALSE; 
   DWORD  dwThreadId = 0; 
   HANDLE hPipe = INVALID_HANDLE_VALUE, hThread = NULL; 
   LPCTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
// The main loop creates an instance of the named pipe and 
// then waits for a client to connect to it. When the client 
// connects, a thread is created to handle communications 
// with that client, and this loop is free to wait for the
// next client connect request. It is an infinite loop.
 
   for (;;) 
   { 
      _tprintf( TEXT("\nPipe Server: Main thread awaiting client connection on %s\n"), lpszPipename);
      hPipe = CreateNamedPipe( 
          lpszPipename,             // pipe name 
          PIPE_ACCESS_DUPLEX,       // read/write access 
          PIPE_TYPE_MESSAGE |       // message type pipe 
          PIPE_READMODE_MESSAGE |   // message-read mode 
          PIPE_WAIT,                // blocking mode 
          PIPE_UNLIMITED_INSTANCES, // max. instances  
          BUFSIZE,                  // output buffer size 
          BUFSIZE,                  // input buffer size 
          0,                        // client time-out 
          NULL);                    // default security attribute 

      if (hPipe == INVALID_HANDLE_VALUE) 
      {
          _tprintf(TEXT("CreateNamedPipe failed, GLE=%d.\n"), GetLastError()); 
          return -1;
      }
 
      // Wait for the client to connect; if it succeeds, 
      // the function returns a nonzero value. If the function
      // returns zero, GetLastError returns ERROR_PIPE_CONNECTED. 
 
      fConnected = ConnectNamedPipe(hPipe, NULL) ? 
         TRUE : (GetLastError() == ERROR_PIPE_CONNECTED); 
 
      if (fConnected) 
      { 
         printf("Client connected, creating a processing thread.\n"); 
      
         // Create a thread for this client. 
         hThread = CreateThread( 
            NULL,              // no security attribute 
            0,                 // default stack size 
            InstanceThread,    // thread proc
            (LPVOID) hPipe,    // thread parameter 
            0,                 // not suspended 
            &dwThreadId);      // returns thread ID 

         if (hThread == NULL) 
         {
            _tprintf(TEXT("CreateThread failed, GLE=%d.\n"), GetLastError()); 
            return -1;
         }
         else CloseHandle(hThread); 
       } 
      else 
        // The client could not connect, so close the pipe. 
         CloseHandle(hPipe); 
   } 

   return 0; 
} 
 
DWORD WINAPI InstanceThread(LPVOID lpvParam)
// This routine is a thread processing function to read from and reply to a client
// via the open pipe connection passed from the main loop. Note this allows
// the main loop to continue executing, potentially creating more threads of
// of this procedure to run concurrently, depending on the number of incoming
// client connections.
{ 
   HANDLE hHeap      = GetProcessHeap();
   TCHAR* pchRequest = (TCHAR*)HeapAlloc(hHeap, 0, BUFSIZE*sizeof(TCHAR));
   TCHAR* pchReply   = (TCHAR*)HeapAlloc(hHeap, 0, BUFSIZE*sizeof(TCHAR));

   DWORD cbBytesRead = 0, cbReplyBytes = 0, cbWritten = 0; 
   BOOL fSuccess = FALSE;
   HANDLE hPipe  = NULL;

   // Do some extra error checking since the app will keep running even if this
   // thread fails.

   if (lpvParam == NULL)
   {
       printf( "\nERROR - Pipe Server Failure:\n");
       printf( "   InstanceThread got an unexpected NULL value in lpvParam.\n");
       printf( "   InstanceThread exitting.\n");
       if (pchReply != NULL) HeapFree(hHeap, 0, pchReply);
       if (pchRequest != NULL) HeapFree(hHeap, 0, pchRequest);
       return (DWORD)-1;
   }

   if (pchRequest == NULL)
   {
       printf( "\nERROR - Pipe Server Failure:\n");
       printf( "   InstanceThread got an unexpected NULL heap allocation.\n");
       printf( "   InstanceThread exitting.\n");
       if (pchReply != NULL) HeapFree(hHeap, 0, pchReply);
       return (DWORD)-1;
   }

   if (pchReply == NULL)
   {
       printf( "\nERROR - Pipe Server Failure:\n");
       printf( "   InstanceThread got an unexpected NULL heap allocation.\n");
       printf( "   InstanceThread exitting.\n");
       if (pchRequest != NULL) HeapFree(hHeap, 0, pchRequest);
       return (DWORD)-1;
   }

   // Print verbose messages. In production code, this should be for debugging only.
   printf("InstanceThread created, receiving and processing messages.\n");

// The thread's parameter is a handle to a pipe object instance. 
 
   hPipe = (HANDLE) lpvParam; 

// Loop until done reading
   while (1) 
   { 
   // Read client requests from the pipe. This simplistic code only allows messages
   // up to BUFSIZE characters in length.
      fSuccess = ReadFile( 
         hPipe,        // handle to pipe 
         pchRequest,    // buffer to receive data 
         BUFSIZE*sizeof(TCHAR), // size of buffer 
         &cbBytesRead, // number of bytes read 
         NULL);        // not overlapped I/O 

      if (!fSuccess || cbBytesRead == 0)
      {   
          if (GetLastError() == ERROR_BROKEN_PIPE)
          {
              _tprintf(TEXT("InstanceThread: client disconnected.\n")); 
          }
          else
          {
              _tprintf(TEXT("InstanceThread ReadFile failed, GLE=%d.\n"), GetLastError()); 
          }
          break;
      }

   // Process the incoming message.
      GetAnswerToRequest(pchRequest, pchReply, &cbReplyBytes); 
 
   // Write the reply to the pipe. 
      fSuccess = WriteFile( 
         hPipe,        // handle to pipe 
         pchReply,     // buffer to write from 
         cbReplyBytes, // number of bytes to write 
         &cbWritten,   // number of bytes written 
         NULL);        // not overlapped I/O 

      if (!fSuccess || cbReplyBytes != cbWritten)
      {   
          _tprintf(TEXT("InstanceThread WriteFile failed, GLE=%d.\n"), GetLastError()); 
          break;
      }
  }

// Flush the pipe to allow the client to read the pipe's contents 
// before disconnecting. Then disconnect the pipe, and close the 
// handle to this pipe instance. 
 
   FlushFileBuffers(hPipe); 
   DisconnectNamedPipe(hPipe); 
   CloseHandle(hPipe); 

   HeapFree(hHeap, 0, pchRequest);
   HeapFree(hHeap, 0, pchReply);

   printf("InstanceThread exiting.\n");
   return 1;
}

VOID GetAnswerToRequest( LPTSTR pchRequest, 
                         LPTSTR pchReply, 
                         LPDWORD pchBytes )
// This routine is a simple function to print the client request to the console
// and populate the reply buffer with a default data string. This is where you
// would put the actual client request processing code that runs in the context
// of an instance thread. Keep in mind the main thread will continue to wait for
// and receive other client connections while the instance thread is working.
{
    _tprintf( TEXT("Client Request String:\"%s\"\n"), pchRequest );

    // Check the outgoing message to make sure it's not too long for the buffer.
    if (FAILED(StringCchCopy( pchReply, BUFSIZE, TEXT("default answer from server") )))
    {
        *pchBytes = 0;
        pchReply[0] = 0;
        printf("StringCchCopy failed, no outgoing message.\n");
        return;
    }
    *pchBytes = (lstrlen(pchReply)+1)*sizeof(TCHAR);
}
```



## <a name="related-topics"></a><span data-ttu-id="0a648-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a648-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a648-114">具名管道用戶端</span><span class="sxs-lookup"><span data-stu-id="0a648-114">Named Pipe Client</span></span>](named-pipe-client.md)
</dt> </dl>

 

 
