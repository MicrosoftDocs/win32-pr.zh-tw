---
description: 下列範例會使用 SetFileTime 函式，將檔案的上次寫入時間設定為目前的系統時間。
ms.assetid: b4a70c01-d5ce-47e8-9918-9c9176894240
title: 將檔案時間變更為目前的時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3d4b6189514196c5f8a332c259da9f8f8d7417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945491"
---
# <a name="changing-a-file-time-to-the-current-time"></a>將檔案時間變更為目前的時間

下列範例會使用 [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) 函式，將檔案的上次寫入時間設定為目前的系統時間。

NTFS 檔案系統會以 UTC 格式儲存時間值，因此不會受到時區或日光節約時間變更的影響。 FAT 檔案系統會根據電腦的本機時間來儲存時間值。

檔案必須使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟，並使用「檔案 \_ 寫入 \_ 屬性」存取。


```C++
#include <windows.h>

// SetFileToCurrentTime - sets last write time to current system time
// Return value - TRUE if successful, FALSE otherwise
// hFile  - must be a valid file handle

BOOL SetFileToCurrentTime(HANDLE hFile)
{
    FILETIME ft;
    SYSTEMTIME st;
    BOOL f;

    GetSystemTime(&st);              // Gets the current system time
    SystemTimeToFileTime(&st, &ft);  // Converts the current system time to file time format
    f = SetFileTime(hFile,           // Sets last-write time of the file 
        (LPFILETIME) NULL,           // to the converted current system time 
        (LPFILETIME) NULL, 
        &ft);    

    return f;
}
```



 

 
