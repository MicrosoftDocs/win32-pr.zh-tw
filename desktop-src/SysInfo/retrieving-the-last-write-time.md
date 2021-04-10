---
description: 下列範例會使用 GetFileTime 函數來取出檔案的上次寫入時間。 它會根據目前的時區設定，將時間轉換為當地時間，並建立可向使用者顯示的日期和時間字串。
ms.assetid: 54509a35-fa6a-4ee6-90f8-36c9ef55e1bc
title: 正在抓取 Last-Write 時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2332a55744eda1ea93853e6967f0cf1b4d45046d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193889"
---
# <a name="retrieving-the-last-write-time"></a><span data-ttu-id="afab8-104">正在抓取 Last-Write 時間</span><span class="sxs-lookup"><span data-stu-id="afab8-104">Retrieving the Last-Write Time</span></span>

<span data-ttu-id="afab8-105">下列範例會使用 [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) 函數來取出檔案的上次寫入時間。</span><span class="sxs-lookup"><span data-stu-id="afab8-105">The following example uses the [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) function to retrieve the last-write time for a file.</span></span> <span data-ttu-id="afab8-106">它會根據目前的時區設定，將時間轉換為當地時間，並建立可向使用者顯示的日期和時間字串。</span><span class="sxs-lookup"><span data-stu-id="afab8-106">It converts the time to local time based on the current time-zone settings, and creates a date and time string that can be shown to the user.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>

// GetLastWriteTime - Retrieves the last-write time and converts
//                    the time to a string
//
// Return value - TRUE if successful, FALSE otherwise
// hFile      - Valid file handle
// lpszString - Pointer to buffer to receive string

BOOL GetLastWriteTime(HANDLE hFile, LPTSTR lpszString, DWORD dwSize)
{
    FILETIME ftCreate, ftAccess, ftWrite;
    SYSTEMTIME stUTC, stLocal;
    DWORD dwRet;

    // Retrieve the file times for the file.
    if (!GetFileTime(hFile, &ftCreate, &ftAccess, &ftWrite))
        return FALSE;

    // Convert the last-write time to local time.
    FileTimeToSystemTime(&ftWrite, &stUTC);
    SystemTimeToTzSpecificLocalTime(NULL, &stUTC, &stLocal);

    // Build a string showing the date and time.
    dwRet = StringCchPrintf(lpszString, dwSize, 
        TEXT("%02d/%02d/%d  %02d:%02d"),
        stLocal.wMonth, stLocal.wDay, stLocal.wYear,
        stLocal.wHour, stLocal.wMinute);

    if( S_OK == dwRet )
        return TRUE;
    else return FALSE;
}

int _tmain(int argc, TCHAR *argv[])
{
    HANDLE hFile;
    TCHAR szBuf[MAX_PATH];

    if( argc != 2 )
    {
        printf("This sample takes a file name as a parameter\n");
        return 0;
    }
    hFile = CreateFile(argv[1], GENERIC_READ, FILE_SHARE_READ, NULL,
        OPEN_EXISTING, 0, NULL);

    if(hFile == INVALID_HANDLE_VALUE)
    {
        printf("CreateFile failed with %d\n", GetLastError());
        return 0;
    }
    if(GetLastWriteTime( hFile, szBuf, MAX_PATH ))
        _tprintf(TEXT("Last write time is: %s\n"), szBuf);
        
    CloseHandle(hFile);    
}
```



## <a name="related-topics"></a><span data-ttu-id="afab8-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="afab8-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afab8-108">**FileTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="afab8-108">**FileTimeToSystemTime**</span></span>](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
</dt> <dt>

[<span data-ttu-id="afab8-109">**SystemTimeToTzSpecificLocalTime**</span><span class="sxs-lookup"><span data-stu-id="afab8-109">**SystemTimeToTzSpecificLocalTime**</span></span>](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
</dt> </dl>

 

 
