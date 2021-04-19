---
description: 示範如何使用 GetTempFileName 和 GetTempPath 函數建立暫存檔案以進行資料操作的範例程式碼。
ms.assetid: 6254c67d-5d34-499d-b1a4-8cac526dd294
title: 建立和使用暫存檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca18b7b72aab7c53bea95c38147af66f2b7fef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970406"
---
# <a name="creating-and-using-a-temporary-file"></a>建立和使用暫存檔案

應用程式可以使用 [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) 和 [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) 函數來取得暫存檔案的唯一檔案和路徑名稱。 **GetTempFileName** 函式會產生唯一的檔案名，而 **GetTempPath** 函式會將路徑抓取到應該建立暫存檔案的目錄。

下列程式描述應用程式如何建立暫存檔案，以供資料操作之用。

**建立和使用暫存檔案**

1.  應用程式會使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)來開啟使用者提供的來源文字檔。
2.  應用程式會使用 [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha) 和 [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea) 函數來抓取暫存檔案路徑和檔案名，然後使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 來建立暫存檔案。
3.  應用程式會將文字資料的區塊讀入緩衝區、使用 [CharUpperBuffA](/windows/win32/api/winuser/nf-winuser-charupperbuffa) 函式將緩衝區內容轉換成大寫，並將轉換後的緩衝區寫入暫存檔案。
4.  當所有來源檔案都寫入至暫存檔時，應用程式會關閉這兩個檔案，並使用 [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) 函式將暫存檔重新命名為 "allcaps.txt"。

在移至下一個步驟之前，會先檢查先前的步驟是否成功，並在發生錯誤時顯示失敗描述。 應用程式將會在顯示錯誤訊息之後立即終止。

請注意，為了方便示範，我們選擇了文字檔操作，而且可以取代為任何所需的資料操作程式。 資料檔案可以是任何資料類型，而不是只有文字。

[**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)函式會從環境變數抓取完整的路徑字串，但不會事先檢查路徑是否存在或該路徑是否有足夠的存取權限，這是應用程式開發人員的責任。 如需詳細資訊，請參閱 [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)。 在下列範例中，錯誤會被視為終端條件，而應用程式會在將描述性訊息傳送至標準輸出之後結束。 不過，有許多其他選項都存在，例如提示使用者輸入臨時目錄，或直接嘗試使用目前的目錄。

> [!Note]  
> [**GetTempFileName**](/windows/desktop/api/FileAPI/nf-fileapi-gettempfilenamea)函數不需要使用 [**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)函數。

 

下列 c + + 範例示範如何建立暫存檔案，以供資料操作之用。


```C++
//
//  This application opens a file specified by the user and uses
//  a temporary file to convert the file to upper case letters.
//  Note that the given source file is assumed to be an ASCII text file
//  and the new file created is overwritten each time the application is
//  run.
//

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUFSIZE 1024

void PrintError(LPCTSTR errDesc);

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile     = INVALID_HANDLE_VALUE;
    HANDLE hTempFile = INVALID_HANDLE_VALUE; 

    BOOL fSuccess  = FALSE;
    DWORD dwRetVal = 0;
    UINT uRetVal   = 0;

    DWORD dwBytesRead    = 0;
    DWORD dwBytesWritten = 0; 

    TCHAR szTempFileName[MAX_PATH];  
    TCHAR lpTempPathBuffer[MAX_PATH];
    char  chBuffer[BUFSIZE]; 

    LPCTSTR errMsg;

    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <file>\n"), argv[0]);
        return -1;
    }

    //  Opens the existing file. 
    hFile = CreateFile(argv[1],               // file name 
                       GENERIC_READ,          // open for reading 
                       0,                     // do not share 
                       NULL,                  // default security 
                       OPEN_EXISTING,         // existing file only 
                       FILE_ATTRIBUTE_NORMAL, // normal file 
                       NULL);                 // no template 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("First CreateFile failed"));
        return (1);
    } 

     //  Gets the temp path env string (no guarantee it's a valid path).
    dwRetVal = GetTempPath(MAX_PATH,          // length of the buffer
                           lpTempPathBuffer); // buffer for path 
    if (dwRetVal > MAX_PATH || (dwRetVal == 0))
    {
        PrintError(TEXT("GetTempPath failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (2);
    }

    //  Generates a temporary file name. 
    uRetVal = GetTempFileName(lpTempPathBuffer, // directory for tmp files
                              TEXT("DEMO"),     // temp file name prefix 
                              0,                // create unique name 
                              szTempFileName);  // buffer for name 
    if (uRetVal == 0)
    {
        PrintError(TEXT("GetTempFileName failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (3);
    }

    //  Creates the new file to write to for the upper-case version.
    hTempFile = CreateFile((LPTSTR) szTempFileName, // file name 
                           GENERIC_WRITE,        // open for write 
                           0,                    // do not share 
                           NULL,                 // default security 
                           CREATE_ALWAYS,        // overwrite existing
                           FILE_ATTRIBUTE_NORMAL,// normal file 
                           NULL);                // no template 
    if (hTempFile == INVALID_HANDLE_VALUE) 
    { 
        PrintError(TEXT("Second CreateFile failed"));
        if (!CloseHandle(hFile))
        {
            PrintError(TEXT("CloseHandle(hFile) failed"));
            return (7);
        }
        return (4);
    } 

    //  Reads BUFSIZE blocks to the buffer and converts all characters in 
    //  the buffer to upper case, then writes the buffer to the temporary 
    //  file. 
    do 
    {
        if (ReadFile(hFile, chBuffer, BUFSIZE, &dwBytesRead, NULL)) 
        {
            //  Replaces lower case letters with upper case
            //  in place (using the same buffer). The return
            //  value is the number of replacements performed,
            //  which we aren't interested in for this demo.
            CharUpperBuffA(chBuffer, dwBytesRead); 

            fSuccess = WriteFile(hTempFile, 
                                 chBuffer, 
                                 dwBytesRead,
                                 &dwBytesWritten, 
                                 NULL); 
            if (!fSuccess) 
            {
                PrintError(TEXT("WriteFile failed"));
                return (5);
            }
        } 
        else
        {
            PrintError(TEXT("ReadFile failed"));
            return (6);
        }
    //  Continues until the whole file is processed.
    } while (dwBytesRead == BUFSIZE); 

    //  The handles to the files are no longer needed, so
    //  they are closed prior to moving the new file.
    if (!CloseHandle(hFile)) 
    {
       PrintError(TEXT("CloseHandle(hFile) failed"));
       return (7);
    }
    
    if (!CloseHandle(hTempFile)) 
    {
       PrintError(TEXT("CloseHandle(hTempFile) failed"));
       return (8);
    }

    //  Moves the temporary file to the new text file, allowing for differnt
    //  drive letters or volume names.
    fSuccess = MoveFileEx(szTempFileName, 
                          TEXT("AllCaps.txt"), 
                          MOVEFILE_REPLACE_EXISTING | MOVEFILE_COPY_ALLOWED);
    if (!fSuccess)
    { 
        PrintError(TEXT("MoveFileEx failed"));
        return (9);
    }
    else 
        _tprintf(TEXT("All-caps version of %s written to AllCaps.txt\n"), argv[1]);
    return (0);
}

//  ErrorMessage support function.
//  Retrieves the system error message for the GetLastError() code.
//  Note: caller must use LocalFree() on the returned LPCTSTR buffer.
LPCTSTR ErrorMessage(DWORD error) 
{ 
    LPVOID lpMsgBuf;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER 
                   | FORMAT_MESSAGE_FROM_SYSTEM 
                   | FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL,
                  error,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR) &lpMsgBuf,
                  0,
                  NULL);

    return((LPCTSTR)lpMsgBuf);
}

//  PrintError support function.
//  Simple wrapper function for error output.
void PrintError(LPCTSTR errDesc)
{
        LPCTSTR errMsg = ErrorMessage(GetLastError());
        _tprintf(TEXT("\n** ERROR ** %s: %s\n"), errDesc, errMsg);
        LocalFree((LPVOID)errMsg);
}
```



 

 
