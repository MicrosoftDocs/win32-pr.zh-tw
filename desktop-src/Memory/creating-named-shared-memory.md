---
description: 若要共用資料，多個處理常式可以使用系統分頁檔案儲存的記憶體對應檔案。
ms.assetid: 17458be2-3ef7-42f2-a717-abf73ac4846f
title: 建立命名的共用記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ac708497ceb12ed099c7a9c0b3788d7a05a925
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970402"
---
# <a name="creating-named-shared-memory"></a><span data-ttu-id="97a2b-103">建立命名的共用記憶體</span><span class="sxs-lookup"><span data-stu-id="97a2b-103">Creating Named Shared Memory</span></span>

<span data-ttu-id="97a2b-104">若要共用資料，多個處理常式可以使用系統分頁檔案儲存的記憶體對應檔案。</span><span class="sxs-lookup"><span data-stu-id="97a2b-104">To share data, multiple processes can use memory-mapped files that the system paging file stores.</span></span>

## <a name="first-process"></a><span data-ttu-id="97a2b-105">第一個進程</span><span class="sxs-lookup"><span data-stu-id="97a2b-105">First Process</span></span>

<span data-ttu-id="97a2b-106">第一個程式會使用 **不正確 \_ 控制碼 \_ 值** 和物件的名稱來呼叫 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga)函數，以建立檔案對應物件。</span><span class="sxs-lookup"><span data-stu-id="97a2b-106">The first process creates the file mapping object by calling the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with **INVALID\_HANDLE\_VALUE** and a name for the object.</span></span> <span data-ttu-id="97a2b-107">藉由使用 **PAGE \_ READWRITE** 旗標，進程具有記憶體的讀取/寫入權限，可透過任何建立的檔案查看。</span><span class="sxs-lookup"><span data-stu-id="97a2b-107">By using the **PAGE\_READWRITE** flag, the process has read/write permission to the memory through any file views that are created.</span></span>

<span data-ttu-id="97a2b-108">然後，此程式會使用 [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) 在呼叫 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 時所傳回的檔案對應物件控制碼，在進程位址空間中建立檔案的視圖。</span><span class="sxs-lookup"><span data-stu-id="97a2b-108">Then the process uses the file mapping object handle that [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) returns in a call to [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) to create a view of the file in the process address space.</span></span> <span data-ttu-id="97a2b-109">**MapViewOfFile** 函式會傳回檔案視圖的指標 `pBuf` 。</span><span class="sxs-lookup"><span data-stu-id="97a2b-109">The **MapViewOfFile** function returns a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="97a2b-110">然後，進程會使用 [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) 函式，將字串寫入至可供其他進程存取的視圖。</span><span class="sxs-lookup"><span data-stu-id="97a2b-110">The process then uses the [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) function to write a string to the view that can be accessed by other processes.</span></span>

<span data-ttu-id="97a2b-111">在檔案對應物件名稱前面加上 "Global \\ "，可讓進程彼此通訊，即使它們位於不同的終端機伺服器會話中也一樣。</span><span class="sxs-lookup"><span data-stu-id="97a2b-111">Prefixing the file mapping object names with "Global\\" allows processes to communicate with each other even if they are in different terminal server sessions.</span></span> <span data-ttu-id="97a2b-112">這需要第一個進程必須具有 [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) 許可權。</span><span class="sxs-lookup"><span data-stu-id="97a2b-112">This requires that the first process must have the [**SeCreateGlobalPrivilege**](../secauthz/privilege-constants.md) privilege.</span></span>

<span data-ttu-id="97a2b-113">當進程不再需要存取檔案對應物件時，它應該呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) 函式。</span><span class="sxs-lookup"><span data-stu-id="97a2b-113">When the process no longer needs access to the file mapping object, it should call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="97a2b-114">當關閉所有控制碼時，系統可以釋放物件使用的分頁檔區段。</span><span class="sxs-lookup"><span data-stu-id="97a2b-114">When all handles are closed, the system can free the section of the paging file that the object uses.</span></span>


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



## <a name="second-process"></a><span data-ttu-id="97a2b-115">第二個處理常式</span><span class="sxs-lookup"><span data-stu-id="97a2b-115">Second Process</span></span>

<span data-ttu-id="97a2b-116">第二個進程可以藉由呼叫 [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) 函式，為對應物件指定相同名稱做為第一個進程，以存取寫入共用記憶體的字串。</span><span class="sxs-lookup"><span data-stu-id="97a2b-116">A second process can access the string written to the shared memory by the first process by calling the [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) function specifying the same name for the mapping object as the first process.</span></span> <span data-ttu-id="97a2b-117">然後，它可以使用 [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) 函式來取得檔案視圖的指標 `pBuf` 。</span><span class="sxs-lookup"><span data-stu-id="97a2b-117">Then it can use the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to obtain a pointer to the file view, `pBuf`.</span></span> <span data-ttu-id="97a2b-118">此程式可以顯示此字串，就像任何其他字串一樣。</span><span class="sxs-lookup"><span data-stu-id="97a2b-118">The process can display this string as it would any other string.</span></span> <span data-ttu-id="97a2b-119">在此範例中，顯示的訊息方塊包含第一個進程所寫入的「來自第一個進程的訊息」訊息。</span><span class="sxs-lookup"><span data-stu-id="97a2b-119">In this example, the message box displayed contains the message "Message from first process" that was written by the first process.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="97a2b-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="97a2b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97a2b-121">共用檔案和記憶體</span><span class="sxs-lookup"><span data-stu-id="97a2b-121">Sharing Files and Memory</span></span>](sharing-files-and-memory.md)
</dt> </dl>

 

 
