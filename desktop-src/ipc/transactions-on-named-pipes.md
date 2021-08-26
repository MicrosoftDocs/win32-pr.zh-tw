---
description: 具名管道交易是一種用戶端/伺服器通訊，可將寫入作業和讀取作業結合成單一網路操作。 交易會改善用戶端與遠端伺服器之間網路通訊的效能。
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: 具名管道上的交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524f9ae453eb958efd59d8ef6ee5adfda12dd2701e4c719be51299e2873913dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963898"
---
# <a name="transactions-on-named-pipes"></a>具名管道上的交易

具名管道交易是一種用戶端/伺服器通訊，可將寫入作業和讀取作業結合成單一網路操作。 交易只能用在雙工、訊息類型管道上。 交易會改善用戶端與遠端伺服器之間網路通訊的效能。 處理常式可以使用 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) 和 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 函數來執行具名管道交易。

管道用戶端最常使用 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) 函式將要求訊息寫入具名管道伺服器，並讀取伺服器的回應訊息。 當管道用戶端藉 \_ \| \_ 由呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟其管道控制碼時，必須指定泛型讀取一般寫入存取權。 然後，管道用戶端會藉由呼叫 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) 函式，將管道控制碼設定為訊息讀取模式。 如果在 **TransactNamedPipe** 的呼叫中指定的讀取緩衝區不夠大，無法保存伺服器所寫入的整個訊息，則函式會傳回零，而 [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤 \_ 更多 \_ 資料。 用戶端可以藉由呼叫 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)、 [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)或 [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) 函數來讀取訊息的其餘部分。

[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) 通常是由管道用戶端呼叫，但也可以由管道伺服器使用。

下列範例顯示使用 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)的管道用戶端。 此管道用戶端可搭配 [查看] 下所列的任何管道伺服器使用。


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



管道用戶端會使用 [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) 將 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)、 [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (（如有必要）) 、 [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)和 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式呼叫合併為單一呼叫。 由於管道控制碼會在函式傳回之前關閉，因此，如果訊息大於讀取緩衝區的指定大小，則訊息中的任何其他位元組都會遺失。 下列範例是重寫為使用 **CallNamedPipe** 的範例。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[多執行緒管道伺服器](multithreaded-pipe-server.md)
</dt> <dt>

[使用重迭 i/o 的具名管道伺服器](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[使用完成常式的具名管道伺服器](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
