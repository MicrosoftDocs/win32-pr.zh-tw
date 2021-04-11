---
description: 顯示如何使用基本 NTFS 檔案系統資料流程的範例程式碼。
ms.assetid: 9cd5f418-404c-40f5-aa51-ef4d2a5f238e
title: 使用資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc73a3524d45eeead4cd6c0d508925e6caa5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194112"
---
# <a name="using-streams"></a>使用資料流程

本主題中的範例將示範如何使用基本 NTFS 檔案系統資料流程。

這個範例會建立名為 "Testfile.txt" 的檔案，其大小為16個位元組。 不過，檔案也有一個額外的：： $DATA 資料流程類型（名為 "Stream"），它會新增額外的23個位元組，而不是由作業系統報告。 因此，當您查看檔案的 [檔案大小] 屬性時，您只會看到檔案的預設：： $DATA 資料流程的大小。


```C++
#include <windows.h>
#include <stdio.h>

void main( )
 {
  HANDLE hFile, hStream;
  DWORD dwRet;

  hFile = CreateFile( TEXT("TestFile"), // Filename
                      GENERIC_WRITE,    // Desired access
                      FILE_SHARE_WRITE, // Share flags
                      NULL,             // Security Attributes
                      OPEN_ALWAYS,      // Creation Disposition
                      0,                // Flags and Attributes
                      NULL );           // OVERLAPPED pointer
  if( hFile == INVALID_HANDLE_VALUE )
   {
    printf( "Cannot open TestFile\n" );
    return;
   }
  else
   {
    WriteFile( hFile,              // Handle
               "This is TestFile", // Data to be written
               16,                 // Size of data, in bytes
               &dwRet,             // Number of bytes written
               NULL );             // OVERLAPPED pointer
    CloseHandle( hFile );
    hFile = INVALID_HANDLE_VALUE;
   }

  hStream = CreateFile( TEXT("TestFile:Stream"), // Filename
                        GENERIC_WRITE,           // Desired access
                        FILE_SHARE_WRITE,        // Share flags
                        NULL,                    // Security Attributes
                        OPEN_ALWAYS,             // Creation Disposition
                        0,                       // Flags and Attributes
                        NULL );                  // OVERLAPPED pointer
  if( hStream == INVALID_HANDLE_VALUE )
    printf( "Cannot open TestFile:Stream\n" );
  else
   {
    WriteFile( hStream,                   // Handle
               "This is TestFile:Stream", // Data to be written
               23,                        // Size of data
               &dwRet,                    // Number of bytes written
               NULL);                     // OVERLAPPED pointer
    CloseHandle( hStream );
    hStream = INVALID_HANDLE_VALUE;
   }
}
```



如果您在命令提示字元中輸入 **Type testfile.txt** ，它會顯示下列輸出：

``` syntax
This is TestFile
```

但是，如果您輸入單字 **類型 testfile.txt： Stream**，則會產生下列錯誤：

「檔案名、目錄名稱或磁片區標籤語法不正確。」

若要查看 Testfile.txt： stream 中的內容，請使用下列其中一個命令：

**其他 < Testfile.txt： Stream**

**其他 < Testfile.txt： Stream： $DATA**

顯示的文字如下所示：

``` syntax
This is TestFile:Stream
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案資料流程](file-streams.md)
</dt> </dl>

 

 



