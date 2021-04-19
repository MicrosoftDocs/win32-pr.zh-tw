---
description: 示範應用程式如何將一個檔案附加至另一個檔案結尾的範例程式碼，包括如何開啟和關閉檔案、讀取和寫入檔案，以及鎖定和解除鎖定檔案。
ms.assetid: e4d1f842-16a1-47e4-84b4-9bb44aaa1dc5
title: 將一個檔案附加至另一個檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 546d24fe88a2bbf22c190a0caca3b3f98e753720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974476"
---
# <a name="appending-one-file-to-another-file"></a>將一個檔案附加至另一個檔案

本主題中的程式碼範例說明如何開啟和關閉檔案、讀取和寫入檔案，以及鎖定和解除鎖定檔案。

在此範例中，應用程式會將一個檔案附加至另一個檔案的結尾。 首先，應用程式會開啟附加的檔案，其中包含只允許應用程式寫入的許可權。 不過，在附加進程期間，其他進程可以開啟具有唯讀許可權的檔案，以提供所附加檔案的快照集。 然後，檔案會在實際的附加進程期間鎖定，以確保寫入檔案的資料完整性。

此範例不會使用交易。 如果您使用交易作業，則只能有唯讀存取權。 在此情況下，您只會在交易認可作業完成後看到附加的資料。

此範例也會顯示應用程式使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)開啟兩個檔案：

-   One.txt 會開啟以供讀取。
-   Two.txt 會開啟以供寫入和共用讀取。

然後，應用程式會使用 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) 和 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ，藉由讀取和寫入 4 KB 區塊，將 One.txt 的內容附加至 Two.txt 的結尾。 不過，在寫入至第二個檔案之前，應用程式會使用 [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) 將第二個檔案的指標設定為該檔案的結尾，並使用 [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) 來鎖定要寫入的區域。 這可防止另一個執行緒或進程在寫入作業進行時，有重複的控制碼存取區域。 當每個寫入作業完成時， [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) 會用來解除鎖定鎖定的區域。


```C++
#include <windows.h>
#include <stdio.h>

void main()
{
  HANDLE hFile;
  HANDLE hAppend;
  DWORD  dwBytesRead, dwBytesWritten, dwPos;
  BYTE   buff[4096];

  // Open the existing file.

  hFile = CreateFile(TEXT("one.txt"), // open One.txt
            GENERIC_READ,             // open for reading
            0,                        // do not share
            NULL,                     // no security
            OPEN_EXISTING,            // existing file only
            FILE_ATTRIBUTE_NORMAL,    // normal file
            NULL);                    // no attr. template

  if (hFile == INVALID_HANDLE_VALUE)
  {
     printf("Could not open One.txt."); 
     return;
  }

  // Open the existing file, or if the file does not exist,
  // create a new file.

  hAppend = CreateFile(TEXT("two.txt"), // open Two.txt
              FILE_APPEND_DATA,         // open for writing
              FILE_SHARE_READ,          // allow multiple readers
              NULL,                     // no security
              OPEN_ALWAYS,              // open or create
              FILE_ATTRIBUTE_NORMAL,    // normal file
              NULL);                    // no attr. template

  if (hAppend == INVALID_HANDLE_VALUE)
  {
     printf("Could not open Two.txt."); 
     return;
  }

  // Append the first file to the end of the second file.
  // Lock the second file to prevent another process from
  // accessing it while writing to it. Unlock the
  // file when writing is complete.

  while (ReadFile(hFile, buff, sizeof(buff), &dwBytesRead, NULL)
      && dwBytesRead > 0)
    {
    dwPos = SetFilePointer(hAppend, 0, NULL, FILE_END);
    LockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    WriteFile(hAppend, buff, dwBytesRead, &dwBytesWritten, NULL);
    UnlockFile(hAppend, dwPos, 0, dwBytesRead, 0);
    }

  // Close both files.

  CloseHandle(hFile);
  CloseHandle(hAppend);
}
```



 

 



