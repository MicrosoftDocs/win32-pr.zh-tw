---
description: 具名管道交易是一種用戶端/伺服器通訊，可將寫入作業和讀取作業結合成單一網路操作。 交易會改善用戶端與遠端伺服器之間網路通訊的效能。
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: 具名管道上的交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489039b92b65f57cefc71c5d78a01b1824b1418a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514068"
---
# <a name="transactions-on-named-pipes"></a><span data-ttu-id="8d0e0-104">具名管道上的交易</span><span class="sxs-lookup"><span data-stu-id="8d0e0-104">Transactions on Named Pipes</span></span>

<span data-ttu-id="8d0e0-105">具名管道交易是一種用戶端/伺服器通訊，可將寫入作業和讀取作業結合成單一網路操作。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-105">A named pipe transaction is a client/server communication that combines a write operation and a read operation into a single network operation.</span></span> <span data-ttu-id="8d0e0-106">交易只能用在雙工、訊息類型管道上。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-106">A transaction can be used only on a duplex, message-type pipe.</span></span> <span data-ttu-id="8d0e0-107">交易會改善用戶端與遠端伺服器之間網路通訊的效能。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-107">Transactions improve the performance of network communications between a client and a remote server.</span></span> <span data-ttu-id="8d0e0-108">處理常式可以使用 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) 和 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函數來執行具名管道交易。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-108">Processes can use the [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) and [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) functions to perform named pipe transactions.</span></span>

<span data-ttu-id="8d0e0-109">管道用戶端最常使用 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) 函式將要求訊息寫入具名管道伺服器，並讀取伺服器的回應訊息。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-109">The [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) function is most commonly used by a pipe client to write a request message to the named pipe server and read the server's response message.</span></span> <span data-ttu-id="8d0e0-110">當管道用戶端藉 \_ \| \_ 由呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟其管道控制碼時，必須指定泛型讀取一般寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-110">The pipe client must specify GENERIC\_READ \| GENERIC\_WRITE access when it opens its pipe handle by calling the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="8d0e0-111">然後，管道用戶端會藉由呼叫 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) 函式，將管道控制碼設定為訊息讀取模式。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-111">Then, the pipe client sets the pipe handle to message-read mode by calling the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function.</span></span> <span data-ttu-id="8d0e0-112">如果在 **TransactNamedPipe** 的呼叫中指定的讀取緩衝區不夠大，無法保存伺服器所寫入的整個訊息，則函式會傳回零，而 [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤 \_ 更多 \_ 資料。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-112">If the read buffer specified in the call to **TransactNamedPipe** is not large enough to hold the entire message written by the server, the function returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA.</span></span> <span data-ttu-id="8d0e0-113">用戶端可以藉由呼叫 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)或 [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) 函數來讀取訊息的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-113">The client can read the remainder of the message by calling either the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), or [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) function.</span></span>

<span data-ttu-id="8d0e0-114">[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) 通常是由管道用戶端呼叫，但也可以由管道伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-114">[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) is typically called by pipe clients, but can also be used by a pipe server.</span></span>

<span data-ttu-id="8d0e0-115">下列範例顯示使用 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)的管道用戶端。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-115">The following example shows a pipe client using [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe).</span></span> <span data-ttu-id="8d0e0-116">此管道用戶端可搭配 [查看] 下所列的任何管道伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-116">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
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
         printf("Could not open pipe\n"); 
         return 0;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
      if (! WaitNamedPipe(lpszPipename, 20000) ) 
      {
         printf("Could not open pipe\n"); 
         return 0;
      }
  } 
 
   // The pipe connected; change to message-read mode. 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if (!fSuccess) 
   {
      printf("SetNamedPipeHandleState failed.\n"); 
      return 0;
   }
 
   // Send a message to the pipe server and read the response. 
   fSuccess = TransactNamedPipe( 
      hPipe,                  // pipe handle 
      lpszWrite,              // message to server
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply
      BUFSIZE*sizeof(TCHAR),  // size of read buffer
      &cbRead,                // bytes read
      NULL);                  // not overlapped 

   if (!fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
   {
      printf("TransactNamedPipe failed.\n"); 
      return 0;
   }
 
   while(1)
   { 
      _tprintf(TEXT("%s\n"), chReadBuf);

      // Break if TransactNamedPipe or ReadFile is successful
      if(fSuccess)
         break;

      // Read from the pipe if there is more data in the message.
      fSuccess = ReadFile( 
         hPipe,      // pipe handle 
         chReadBuf,  // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 

      // Exit if an error other than ERROR_MORE_DATA occurs.
      if( !fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
         break;
      else _tprintf( TEXT("%s\n"), chReadBuf); 
   }

   _getch(); 

   CloseHandle(hPipe); 
 
   return 0; 
}
```



<span data-ttu-id="8d0e0-117">管道用戶端會使用 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 將 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)、 [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (（如有必要）) 、 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)和 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式呼叫合併為單一呼叫。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-117">A pipe client uses [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) to combine the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (if necessary), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe), and [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function calls into a single call.</span></span> <span data-ttu-id="8d0e0-118">由於管道控制碼會在函式傳回之前關閉，因此，如果訊息大於讀取緩衝區的指定大小，則訊息中的任何其他位元組都會遺失。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-118">Because the pipe handle is closed before the function returns, any additional bytes in the message are lost if the message is larger than the specified size of the read buffer.</span></span> <span data-ttu-id="8d0e0-119">下列範例是重寫為使用 **CallNamedPipe** 的範例。</span><span class="sxs-lookup"><span data-stu-id="8d0e0-119">The following example is the previous example rewritten to use **CallNamedPipe**.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
   fSuccess = CallNamedPipe( 
      lpszPipename,        // pipe name 
      lpszWrite,           // message to server 
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply 
      BUFSIZE*sizeof(TCHAR),  // size of read buffer 
      &cbRead,                // number of bytes read 
      20000);                 // waits for 20 seconds 
 
   if (fSuccess || GetLastError() == ERROR_MORE_DATA) 
   { 
      _tprintf( TEXT("%s\n"), chReadBuf ); 
    
      // The pipe is closed; no more data can be read. 
 
      if (! fSuccess) 
      {
         printf("\nExtra data in message was lost\n"); 
      }
   }
 
   _getch(); 

   return 0; 
}
```



## <a name="related-topics"></a><span data-ttu-id="8d0e0-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d0e0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d0e0-121">多執行緒管道伺服器</span><span class="sxs-lookup"><span data-stu-id="8d0e0-121">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="8d0e0-122">使用重迭 i/o 的具名管道伺服器</span><span class="sxs-lookup"><span data-stu-id="8d0e0-122">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="8d0e0-123">使用完成常式的具名管道伺服器</span><span class="sxs-lookup"><span data-stu-id="8d0e0-123">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
