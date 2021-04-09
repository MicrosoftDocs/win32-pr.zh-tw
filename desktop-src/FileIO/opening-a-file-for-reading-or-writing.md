---
description: 示範如何使用 CreateFile 函數建立新檔案或開啟現有檔案的範例程式碼。
ms.assetid: 04e089a7-c559-4a35-a38b-e1acdf3438d1
title: 開啟檔案進行讀取或寫入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254684538a64a37cd94841812df84808da8374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691088"
---
# <a name="opening-a-file-for-reading-or-writing"></a><span data-ttu-id="9604e-103">開啟檔案進行讀取或寫入</span><span class="sxs-lookup"><span data-stu-id="9604e-103">Opening a File for Reading or Writing</span></span>

<span data-ttu-id="9604e-104">[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式可以建立新的檔案，或開啟現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="9604e-104">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function can create a new file or open an existing file.</span></span> <span data-ttu-id="9604e-105">您必須指定檔案名、建立指示和其他屬性。</span><span class="sxs-lookup"><span data-stu-id="9604e-105">You must specify the file name, creation instructions, and other attributes.</span></span> <span data-ttu-id="9604e-106">當應用程式建立新檔案時，作業系統會將它新增至指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="9604e-106">When an application creates a new file, the operating system adds it to the specified directory.</span></span>

## <a name="example-open-a-file-for-writing"></a><span data-ttu-id="9604e-107">範例：開啟要寫入的檔案</span><span class="sxs-lookup"><span data-stu-id="9604e-107">Example: Open a File for Writing</span></span>

<span data-ttu-id="9604e-108">下列範例會使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 來建立新的檔案，並開啟它進行寫入和 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ，以同步方式將簡單字串寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="9604e-108">The following example uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to create a new file and open it for writing and [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) to write a simple string synchronously to the file.</span></span>

<span data-ttu-id="9604e-109">後續呼叫以 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 開啟此檔案將會失敗，直到控制碼關閉為止。</span><span class="sxs-lookup"><span data-stu-id="9604e-109">A subsequent call to open this file with [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) will fail until the handle is closed.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void DisplayError(LPTSTR lpszFunction);

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    char DataBuffer[] = "This is some test data to write to the file.";
    DWORD dwBytesToWrite = (DWORD)strlen(DataBuffer);
    DWORD dwBytesWritten = 0;
    BOOL bErrorFlag = FALSE;

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error:\tIncorrect number of arguments\n\n");
        _tprintf(TEXT("%s <file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],                // name of the write
                       GENERIC_WRITE,          // open for writing
                       0,                      // do not share
                       NULL,                   // default security
                       CREATE_NEW,             // create new file only
                       FILE_ATTRIBUTE_NORMAL,  // normal file
                       NULL);                  // no attr. template

    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: Unable to open file \"%s\" for write.\n"), argv[1]);
        return;
    }

    _tprintf(TEXT("Writing %d bytes to %s.\n"), dwBytesToWrite, argv[1]);

    bErrorFlag = WriteFile( 
                    hFile,           // open file handle
                    DataBuffer,      // start of data to write
                    dwBytesToWrite,  // number of bytes to write
                    &dwBytesWritten, // number of bytes that were written
                    NULL);            // no overlapped structure

    if (FALSE == bErrorFlag)
    {
        DisplayError(TEXT("WriteFile"));
        printf("Terminal failure: Unable to write to file.\n");
    }
    else
    {
        if (dwBytesWritten != dwBytesToWrite)
        {
            // This is an error because a synchronous write that results in
            // success (WriteFile returns TRUE) should write all data as
            // requested. This would not necessarily be the case for
            // asynchronous writes.
            printf("Error: dwBytesWritten != dwBytesToWrite\n");
        }
        else
        {
            _tprintf(TEXT("Wrote %d bytes to %s successfully.\n"), dwBytesWritten, argv[1]);
        }
    }

    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
```



## <a name="example-open-a-file-for-reading"></a><span data-ttu-id="9604e-110">範例：開啟要讀取的檔案</span><span class="sxs-lookup"><span data-stu-id="9604e-110">Example: Open a File for Reading</span></span>

<span data-ttu-id="9604e-111">下列範例會使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 來開啟現有的檔案以供讀取和 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) ，以同步方式從檔案讀取最多80個字元。</span><span class="sxs-lookup"><span data-stu-id="9604e-111">The following example uses [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open an existing file for reading and [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) to read up to 80 characters synchronously from the file.</span></span>

<span data-ttu-id="9604e-112">在此情況下，只有當指定的檔案已存在於目前的目錄中時， [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 才會成功。</span><span class="sxs-lookup"><span data-stu-id="9604e-112">In this case, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) succeeds only if the specified file already exists in the current directory.</span></span> <span data-ttu-id="9604e-113">如果呼叫使用相同的存取和共用模式，後續呼叫以 **CreateFile** 開啟此檔案將會成功。</span><span class="sxs-lookup"><span data-stu-id="9604e-113">A subsequent call to open this file with **CreateFile** will succeed if the call uses the same access and sharing modes.</span></span>

<span data-ttu-id="9604e-114">提示：您可以使用您在先前的 WriteFile 範例中所建立的檔案來測試此範例。</span><span class="sxs-lookup"><span data-stu-id="9604e-114">Tip: You can use the file you created with the previous WriteFile example to test this example.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

#define BUFFERSIZE 5
DWORD g_BytesTransferred = 0;

void DisplayError(LPTSTR lpszFunction);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped
);

VOID CALLBACK FileIOCompletionRoutine(
  __in  DWORD dwErrorCode,
  __in  DWORD dwNumberOfBytesTransfered,
  __in  LPOVERLAPPED lpOverlapped )
 {
  _tprintf(TEXT("Error code:\t%x\n"), dwErrorCode);
  _tprintf(TEXT("Number of bytes:\t%x\n"), dwNumberOfBytesTransfered);
  g_BytesTransferred = dwNumberOfBytesTransfered;
 }

//
// Note: this simplified sample assumes the file to read is an ANSI text file
// only for the purposes of output to the screen. CreateFile and ReadFile
// do not use parameters to differentiate between text and binary file types.
//

int __cdecl _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile; 
    DWORD  dwBytesRead = 0;
    char   ReadBuffer[BUFFERSIZE] = {0};
    OVERLAPPED ol = {0};

    printf("\n");
    if( argc != 2 )
    {
        printf("Usage Error: Incorrect number of arguments\n\n");
        _tprintf(TEXT("Usage:\n\t%s <text_file_name>\n"), argv[0]);
        return;
    }

    hFile = CreateFile(argv[1],               // file to open
                       GENERIC_READ,          // open for reading
                       FILE_SHARE_READ,       // share for reading
                       NULL,                  // default security
                       OPEN_EXISTING,         // existing file only
                       FILE_ATTRIBUTE_NORMAL | FILE_FLAG_OVERLAPPED, // normal file
                       NULL);                 // no attr. template
 
    if (hFile == INVALID_HANDLE_VALUE) 
    { 
        DisplayError(TEXT("CreateFile"));
        _tprintf(TEXT("Terminal failure: unable to open file \"%s\" for read.\n"), argv[1]);
        return; 
    }

    // Read one character less than the buffer size to save room for
    // the terminating NULL character. 

    if( FALSE == ReadFileEx(hFile, ReadBuffer, BUFFERSIZE-1, &ol, FileIOCompletionRoutine) )
    {
        DisplayError(TEXT("ReadFile"));
        printf("Terminal failure: Unable to read from file.\n GetLastError=%08x\n", GetLastError());
        CloseHandle(hFile);
        return;
    }
    SleepEx(5000, TRUE);
    dwBytesRead = g_BytesTransferred;
    // This is the section of code that assumes the file is ANSI text. 
    // Modify this block for other data types if needed.

    if (dwBytesRead > 0 && dwBytesRead <= BUFFERSIZE-1)
    {
        ReadBuffer[dwBytesRead]='\0'; // NULL character

        _tprintf(TEXT("Data read from %s (%d bytes): \n"), argv[1], dwBytesRead);
        printf("%s\n", ReadBuffer);
    }
    else if (dwBytesRead == 0)
    {
        _tprintf(TEXT("No data read from file %s\n"), argv[1]);
    }
    else
    {
        printf("\n ** Unexpected value for dwBytesRead ** \n");
    }

    // It is always good practice to close the open file handles even though
    // the app will exit here and clean up open handles anyway.
    
    CloseHandle(hFile);
}

void DisplayError(LPTSTR lpszFunction) 
// Routine Description:
// Retrieve and output the system error message for the last-error code
{ 
    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, 
        NULL );

    lpDisplayBuf = 
        (LPVOID)LocalAlloc( LMEM_ZEROINIT, 
                            ( lstrlen((LPCTSTR)lpMsgBuf)
                              + lstrlen((LPCTSTR)lpszFunction)
                              + 40) // account for format string
                            * sizeof(TCHAR) );
    
    if (FAILED( StringCchPrintf((LPTSTR)lpDisplayBuf, 
                     LocalSize(lpDisplayBuf) / sizeof(TCHAR),
                     TEXT("%s failed with error code %d as follows:\n%s"), 
                     lpszFunction, 
                     dw, 
                     lpMsgBuf)))
    {
        printf("FATAL ERROR: Unable to output error code.\n");
    }
    
    _tprintf(TEXT("ERROR: %s\n"), (LPCTSTR)lpDisplayBuf);

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}

```



## <a name="related-topics"></a><span data-ttu-id="9604e-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="9604e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9604e-116">建立和開啟檔案</span><span class="sxs-lookup"><span data-stu-id="9604e-116">Creating and Opening Files</span></span>](creating-and-opening-files.md)
</dt> </dl>

 

 



