---
description: 應用程式可以藉由呼叫 >setcurrentdirectory 函數來變更目前的目錄。
ms.assetid: b08e7739-55d4-4690-9ce5-2a8cb29214e9
title: 變更目前的目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e507d206bcd988a7c00f557bde2b8a0ad39c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981885"
---
# <a name="changing-the-current-directory"></a><span data-ttu-id="fd129-103">變更目前的目錄</span><span class="sxs-lookup"><span data-stu-id="fd129-103">Changing the Current Directory</span></span>

<span data-ttu-id="fd129-104">使用中路徑結尾的目錄稱為「目前的目錄」;它是作用中應用程式開始的目錄，除非已明確變更。</span><span class="sxs-lookup"><span data-stu-id="fd129-104">The directory at the end of the active path is called the current directory; it is the directory in which the active application started, unless it has been explicitly changed.</span></span> <span data-ttu-id="fd129-105">應用程式可以藉由呼叫 [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) 函數來判斷哪個目錄是最新的。</span><span class="sxs-lookup"><span data-stu-id="fd129-105">An application can determine which directory is current by calling the [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) function.</span></span> <span data-ttu-id="fd129-106">有時必須使用 [**>getfullpathname**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) 函式，以確保應用程式需要時，才會包含磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="fd129-106">It is sometimes necessary to use the [**GetFullPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) function to ensure the drive letter is included if the application requires it.</span></span>

> [!Note]  
> <span data-ttu-id="fd129-107">雖然每個進程只能有一個目前的目錄，但如果應用程式使用 [**>setcurrentdirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) 函式來切換磁片區，系統就會記住每個磁片區的最後一個目前路徑 (磁碟機號) 。</span><span class="sxs-lookup"><span data-stu-id="fd129-107">Although each process can have only one current directory, if the application switches volumes by using the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function, the system remembers the last current path for each volume (drive letter).</span></span> <span data-ttu-id="fd129-108">只有在將目前的目錄點變更為不同的磁片區時，才會在指定沒有完整路徑的磁碟機號時，才會出現此行為。</span><span class="sxs-lookup"><span data-stu-id="fd129-108">This behavior will manifest itself only when specifying a drive letter without a fully qualified path when changing the current directory point of reference to a different volume.</span></span> <span data-ttu-id="fd129-109">這適用于 Get 或 Set 作業。</span><span class="sxs-lookup"><span data-stu-id="fd129-109">This applies to either Get or Set operations.</span></span>

 

<span data-ttu-id="fd129-110">應用程式可以藉由呼叫 [**>setcurrentdirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) 函數來變更目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="fd129-110">An application can change the current directory by calling the [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory) function.</span></span>

<span data-ttu-id="fd129-111">下列範例示範如何使用 [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) 和 [**>setcurrentdirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)。</span><span class="sxs-lookup"><span data-stu-id="fd129-111">The following example demonstrates the use of [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory) and [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory).</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>

#define BUFSIZE MAX_PATH
 
void _tmain(int argc, TCHAR **argv) 
{ 
   TCHAR Buffer[BUFSIZE];
   DWORD dwRet;

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }

   dwRet = GetCurrentDirectory(BUFSIZE, Buffer);

   if( dwRet == 0 )
   {
      printf("GetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   if(dwRet > BUFSIZE)
   {
      printf("Buffer too small; need %d characters\n", dwRet);
      return;
   }

   if( !SetCurrentDirectory(argv[1]))
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Set current directory to %s\n"), argv[1]);

   if( !SetCurrentDirectory(Buffer) )
   {
      printf("SetCurrentDirectory failed (%d)\n", GetLastError());
      return;
   }
   _tprintf(TEXT("Restored previous directory (%s)\n"), Buffer);
}
```



 

 



