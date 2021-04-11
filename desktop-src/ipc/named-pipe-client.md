---
description: 程式碼範例會顯示開啟具名管道的管道用戶端、將管道控制碼設定為訊息讀取模式、使用 WriteFile 函式將要求傳送至伺服器，並使用 ReadFile 函數來讀取伺服器回復。
ms.assetid: 0779242c-45f4-4cd9-9c9f-36cff54c8dee
title: 具名管道用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6318edd7d5b41c701e3112188a896c0529338805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847693"
---
# <a name="named-pipe-client"></a><span data-ttu-id="78af6-103">具名管道用戶端</span><span class="sxs-lookup"><span data-stu-id="78af6-103">Named Pipe Client</span></span>

<span data-ttu-id="78af6-104">具名管道用戶端使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟具名管道的控制碼。</span><span class="sxs-lookup"><span data-stu-id="78af6-104">A named pipe client uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a named pipe.</span></span> <span data-ttu-id="78af6-105">如果管道存在，但其所有實例都忙碌中， **CreateFile** 會傳回 **不正確 \_ 控制碼 \_ 值** ，而且 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回錯誤 \_ 管道 \_ 忙碌。</span><span class="sxs-lookup"><span data-stu-id="78af6-105">If the pipe exists but all of its instances are busy, **CreateFile** returns **INVALID\_HANDLE\_VALUE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_PIPE\_BUSY.</span></span> <span data-ttu-id="78af6-106">發生這種情況時，具名管道用戶端會使用 [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) 函式來等候具名管道的實例變成可用。</span><span class="sxs-lookup"><span data-stu-id="78af6-106">When this happens, the named pipe client uses the [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) function to wait for an instance of the named pipe to become available.</span></span>

<span data-ttu-id="78af6-107">如果指定的存取與伺服器建立管道時 (雙工、輸出或輸入) 指定的存取不相容， [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數就會失敗。</span><span class="sxs-lookup"><span data-stu-id="78af6-107">The [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function fails if the access specified is incompatible with the access specified (duplex, outbound, or inbound) when the server created the pipe.</span></span> <span data-ttu-id="78af6-108">若為雙工管道，用戶端可以指定讀取、寫入或讀取/寫入存取;若為輸出管道 (僅限寫入的伺服器) ，用戶端必須指定唯讀存取;針對輸入管道 (唯讀伺服器) ，用戶端必須指定僅限寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="78af6-108">For a duplex pipe, the client can specify read, write, or read/write access; for an outbound pipe (write-only server), the client must specify read-only access; and for an inbound pipe (read-only server), the client must specify write-only access.</span></span>

<span data-ttu-id="78af6-109">[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)傳回的控制碼預設為位元組讀取模式、封鎖等候模式、停用的重迭模式，以及停用的寫入模式。</span><span class="sxs-lookup"><span data-stu-id="78af6-109">The handle returned by [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) defaults to byte-read mode, blocking-wait mode, overlapped mode disabled, and write-through mode disabled.</span></span> <span data-ttu-id="78af6-110">管道用戶端可以使用 **CreateFile** ，藉由指定檔案旗標重迭， \_ \_ 或透過指定檔案旗標寫入來啟用「寫入」模式，來啟用重迭模式 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="78af6-110">The pipe client can use **CreateFile** to enable overlapped mode by specifying FILE\_FLAG\_OVERLAPPED or to enable write-through mode by specifying FILE\_FLAG\_WRITE\_THROUGH.</span></span> <span data-ttu-id="78af6-111">用戶端可以使用 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) 函式，藉由指定管道 NOWAIT 來啟用非封鎖模式， \_ 或藉由指定管道 READMODE 訊息來啟用訊息讀取模式 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="78af6-111">The client can use the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function to enable nonblocking mode by specifying PIPE\_NOWAIT or to enable message-read mode by specifying PIPE\_READMODE\_MESSAGE.</span></span>

<span data-ttu-id="78af6-112">下列範例顯示的管道用戶端會開啟具名管道、將管道控制碼設定為訊息讀取模式、使用 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 函式將要求傳送至伺服器，並使用 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 函數來讀取伺服器的回復。</span><span class="sxs-lookup"><span data-stu-id="78af6-112">The following example shows a pipe client that opens a named pipe, sets the pipe handle to message-read mode, uses the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to send a request to the server, and uses the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function to read the server's reply.</span></span> <span data-ttu-id="78af6-113">此管道用戶端可搭配本主題底部所列的任何訊息類型伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="78af6-113">This pipe client can be used with any of the message-type servers listed at the bottom of this topic.</span></span> <span data-ttu-id="78af6-114">不過，使用 byte 類型伺服器時，此管道用戶端會在呼叫 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) 變更為訊息讀取模式時失敗。</span><span class="sxs-lookup"><span data-stu-id="78af6-114">With a byte-type server, however, this pipe client fails when it calls [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) to change to message-read mode.</span></span> <span data-ttu-id="78af6-115">由於用戶端是以訊息讀取模式從管道讀取，所以 **ReadFile** 作業可能會在讀取部分訊息之後傳回零。</span><span class="sxs-lookup"><span data-stu-id="78af6-115">Because the client is reading from the pipe in message-read mode, it is possible for the **ReadFile** operation to return zero after reading a partial message.</span></span> <span data-ttu-id="78af6-116">當訊息大於讀取緩衝區時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="78af6-116">This happens when the message is larger than the read buffer.</span></span> <span data-ttu-id="78af6-117">在此情況下， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤 \_ \_ 的資料，而用戶端可以使用 **ReadFile** 的其他呼叫來讀取訊息的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="78af6-117">In this situation, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA, and the client can read the remainder of the message using additional calls to **ReadFile**.</span></span>

<span data-ttu-id="78af6-118">此管道用戶端可搭配 [查看] 下所列的任何管道伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="78af6-118">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpvMessage=TEXT("Default message from client."); 
   TCHAR  chBuf[BUFSIZE]; 
   BOOL   fSuccess = FALSE; 
   DWORD  cbRead, cbToWrite, cbWritten, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1 )
      lpvMessage = argv[1];
 
// Try to open a named pipe; wait for it, if necessary. 
 
   while (1) 
   { 
      hPipe = CreateFile( 
         lpszPipename,   // pipe name 
         GENERIC_READ |  // read and write access 
         GENERIC_WRITE, 
         0,              // no sharing 
         NULL,           // default security attributes
         OPEN_EXISTING,  // opens existing pipe 
         0,              // default attributes 
         NULL);          // no template file 
 
   // Break if the pipe handle is valid. 
 
      if (hPipe != INVALID_HANDLE_VALUE) 
         break; 
 
      // Exit if an error other than ERROR_PIPE_BUSY occurs. 
 
      if (GetLastError() != ERROR_PIPE_BUSY) 
      {
         _tprintf( TEXT("Could not open pipe. GLE=%d\n"), GetLastError() ); 
         return -1;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
 
      if ( ! WaitNamedPipe(lpszPipename, 20000)) 
      { 
         printf("Could not open pipe: 20 second wait timed out."); 
         return -1;
      } 
   } 
 
// The pipe connected; change to message-read mode. 
 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if ( ! fSuccess) 
   {
      _tprintf( TEXT("SetNamedPipeHandleState failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }
 
// Send a message to the pipe server. 
 
   cbToWrite = (lstrlen(lpvMessage)+1)*sizeof(TCHAR);
   _tprintf( TEXT("Sending %d byte message: \"%s\"\n"), cbToWrite, lpvMessage); 

   fSuccess = WriteFile( 
      hPipe,                  // pipe handle 
      lpvMessage,             // message 
      cbToWrite,              // message length 
      &cbWritten,             // bytes written 
      NULL);                  // not overlapped 

   if ( ! fSuccess) 
   {
      _tprintf( TEXT("WriteFile to pipe failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }

   printf("\nMessage sent to server, receiving reply as follows:\n");
 
   do 
   { 
   // Read from the pipe. 
 
      fSuccess = ReadFile( 
         hPipe,    // pipe handle 
         chBuf,    // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 
 
      if ( ! fSuccess && GetLastError() != ERROR_MORE_DATA )
         break; 
 
      _tprintf( TEXT("\"%s\"\n"), chBuf ); 
   } while ( ! fSuccess);  // repeat loop if ERROR_MORE_DATA 

   if ( ! fSuccess)
   {
      _tprintf( TEXT("ReadFile from pipe failed. GLE=%d\n"), GetLastError() );
      return -1;
   }

   printf("\n<End of message, press ENTER to terminate connection and exit>");
   _getch();
 
   CloseHandle(hPipe); 
 
   return 0; 
}
```



## <a name="related-topics"></a><span data-ttu-id="78af6-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="78af6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78af6-120">多執行緒管道伺服器</span><span class="sxs-lookup"><span data-stu-id="78af6-120">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="78af6-121">使用重迭 i/o 的具名管道伺服器</span><span class="sxs-lookup"><span data-stu-id="78af6-121">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="78af6-122">使用完成常式的具名管道伺服器</span><span class="sxs-lookup"><span data-stu-id="78af6-122">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
