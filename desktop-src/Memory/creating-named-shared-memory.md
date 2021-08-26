---
description: 若要共用資料，多個處理常式可以使用系統分頁檔案儲存的記憶體對應檔案。
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: 建立命名的共用記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fc5ec3d9865d310807d01ac9f76967d4378fc92e4c9588d00b2933a08c953f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869918"
---
# <a name="creating-named-shared-memory"></a>建立命名的共用記憶體

若要共用資料，多個處理常式可以使用系統分頁檔案儲存的記憶體對應檔案。

## <a name="first-process"></a>第一個進程

第一個程式會使用 **不正確 \_ 控制碼 \_ 值** 和物件的名稱來呼叫 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數，以建立檔案對應物件。 藉由使用 **PAGE \_ READWRITE** 旗標，進程具有記憶體的讀取/寫入權限，可透過任何建立的檔案查看。

然後，此程式會使用 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) 在呼叫 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 時所傳回的檔案對應物件控制碼，在進程位址空間中建立檔案的視圖。 **MapViewOfFile** 函式會傳回檔案視圖的指標 `pBuf` 。 然後，進程會使用 [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) 函式，將字串寫入至可供其他進程存取的視圖。

在檔案對應物件名稱前面加上 "Global \\ "，可讓進程彼此通訊，即使它們位於不同的終端機伺服器會話中也一樣。 這需要第一個進程必須具有 [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) 許可權。

當進程不再需要存取檔案對應物件時，它應該呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函式。 當關閉所有控制碼時，系統可以釋放物件使用的分頁檔區段。


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");
TCHAR szMsg[]=TEXT("Message from first process.");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = CreateFileMapping(
                 INVALID_HANDLE_VALUE,    // use paging file
                 NULL,                    // default security
                 PAGE_READWRITE,          // read/write access
                 0,                       // maximum object size (high-order DWORD)
                 BUF_SIZE,                // maximum object size (low-order DWORD)
                 szName);                 // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not create file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }
   pBuf = (LPTSTR) MapViewOfFile(hMapFile,   // handle to map object
                        FILE_MAP_ALL_ACCESS, // read/write permission
                        0,
                        0,
                        BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

       CloseHandle(hMapFile);

      return 1;
   }


   CopyMemory((PVOID)pBuf, szMsg, (_tcslen(szMsg) * sizeof(TCHAR)));
    _getch();

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="second-process"></a>第二個處理常式

第二個進程可以藉由呼叫 [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) 函式，為對應物件指定相同名稱做為第一個進程，以存取寫入共用記憶體的字串。 然後，它可以使用 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 函式來取得檔案視圖的指標 `pBuf` 。 此程式可以顯示此字串，就像任何其他字串一樣。 在此範例中，顯示的訊息方塊包含第一個進程所寫入的「來自第一個進程的訊息」訊息。


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>
#include <tchar.h>
#pragma comment(lib, "user32.lib")

#define BUF_SIZE 256
TCHAR szName[]=TEXT("Global\\MyFileMappingObject");

int _tmain()
{
   HANDLE hMapFile;
   LPCTSTR pBuf;

   hMapFile = OpenFileMapping(
                   FILE_MAP_ALL_ACCESS,   // read/write access
                   FALSE,                 // do not inherit the name
                   szName);               // name of mapping object

   if (hMapFile == NULL)
   {
      _tprintf(TEXT("Could not open file mapping object (%d).\n"),
             GetLastError());
      return 1;
   }

   pBuf = (LPTSTR) MapViewOfFile(hMapFile, // handle to map object
               FILE_MAP_ALL_ACCESS,  // read/write permission
               0,
               0,
               BUF_SIZE);

   if (pBuf == NULL)
   {
      _tprintf(TEXT("Could not map view of file (%d).\n"),
             GetLastError());

      CloseHandle(hMapFile);

      return 1;
   }

   MessageBox(NULL, pBuf, TEXT("Process2"), MB_OK);

   UnmapViewOfFile(pBuf);

   CloseHandle(hMapFile);

   return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[共用檔案和記憶體](sharing-files-and-memory.md)
</dt> </dl>

 

 
