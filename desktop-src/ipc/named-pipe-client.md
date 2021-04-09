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
# <a name="named-pipe-client"></a>具名管道用戶端

具名管道用戶端使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟具名管道的控制碼。 如果管道存在，但其所有實例都忙碌中， **CreateFile** 會傳回 **不正確 \_ 控制碼 \_ 值** ，而且 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式會傳回錯誤 \_ 管道 \_ 忙碌。 發生這種情況時，具名管道用戶端會使用 [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) 函式來等候具名管道的實例變成可用。

如果指定的存取與伺服器建立管道時 (雙工、輸出或輸入) 指定的存取不相容， [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函數就會失敗。 若為雙工管道，用戶端可以指定讀取、寫入或讀取/寫入存取;若為輸出管道 (僅限寫入的伺服器) ，用戶端必須指定唯讀存取;針對輸入管道 (唯讀伺服器) ，用戶端必須指定僅限寫入存取權。

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)傳回的控制碼預設為位元組讀取模式、封鎖等候模式、停用的重迭模式，以及停用的寫入模式。 管道用戶端可以使用 **CreateFile** ，藉由指定檔案旗標重迭， \_ \_ 或透過指定檔案旗標寫入來啟用「寫入」模式，來啟用重迭模式 \_ \_ \_ 。 用戶端可以使用 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) 函式，藉由指定管道 NOWAIT 來啟用非封鎖模式， \_ 或藉由指定管道 READMODE 訊息來啟用訊息讀取模式 \_ \_ 。

下列範例顯示的管道用戶端會開啟具名管道、將管道控制碼設定為訊息讀取模式、使用 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 函式將要求傳送至伺服器，並使用 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 函數來讀取伺服器的回復。 此管道用戶端可搭配本主題底部所列的任何訊息類型伺服器使用。 不過，使用 byte 類型伺服器時，此管道用戶端會在呼叫 [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) 變更為訊息讀取模式時失敗。 由於用戶端是以訊息讀取模式從管道讀取，所以 **ReadFile** 作業可能會在讀取部分訊息之後傳回零。 當訊息大於讀取緩衝區時，就會發生這種情況。 在此情況下， [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤 \_ \_ 的資料，而用戶端可以使用 **ReadFile** 的其他呼叫來讀取訊息的其餘部分。

此管道用戶端可搭配 [查看] 下所列的任何管道伺服器使用。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[多執行緒管道伺服器](multithreaded-pipe-server.md)
</dt> <dt>

[使用重迭 i/o 的具名管道伺服器](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[使用完成常式的具名管道伺服器](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
