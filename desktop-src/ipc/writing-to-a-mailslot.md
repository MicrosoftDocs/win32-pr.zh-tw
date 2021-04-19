---
description: 如何寫入信箱。 寫入郵筒類似于寫入至標準磁片檔案。
ms.assetid: a69ba953-cd5c-487f-b9e0-dbd6c44b88b8
title: 寫入郵筒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568727f7a83d46925f3e681f3dec4906903ca8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985074"
---
# <a name="writing-to-a-mailslot"></a><span data-ttu-id="ae204-104">寫入郵筒</span><span class="sxs-lookup"><span data-stu-id="ae204-104">Writing to a Mailslot</span></span>

<span data-ttu-id="ae204-105">寫入郵筒類似于寫入至標準磁片檔案。</span><span class="sxs-lookup"><span data-stu-id="ae204-105">Writing to a mailslot is similar to writing to a standard disk file.</span></span> <span data-ttu-id="ae204-106">下列程式碼會使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)和 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式，在信箱中放入簡短的訊息。</span><span class="sxs-lookup"><span data-stu-id="ae204-106">The following code uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) functions to put a short message in a mailslot.</span></span> <span data-ttu-id="ae204-107">此訊息會廣播至本機電腦上名為「範例郵筒」的郵筒伺服器 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ae204-107">The message is broadcast to the mailslot server named "sample\_mailslot" on the local computer.</span></span> <span data-ttu-id="ae204-108">程式碼會在已建立的郵筒伺服器的假設下運作。</span><span class="sxs-lookup"><span data-stu-id="ae204-108">The code operates under the assumption that the mailslot server was already created.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

LPCTSTR SlotName = TEXT("\\\\.\\mailslot\\sample_mailslot");

BOOL WriteSlot(HANDLE hSlot, LPCTSTR lpszMessage)
{
   BOOL fResult; 
   DWORD cbWritten; 
 
   fResult = WriteFile(hSlot, 
     lpszMessage, 
     (DWORD) (lstrlen(lpszMessage)+1)*sizeof(TCHAR),  
     &cbWritten, 
     (LPOVERLAPPED) NULL); 
 
   if (!fResult) 
   { 
      printf("WriteFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   printf("Slot written to successfully.\n"); 

   return TRUE;
}

int main()
{ 
   HANDLE hFile; 

   hFile = CreateFile(SlotName, 
     GENERIC_WRITE, 
     FILE_SHARE_READ,
     (LPSECURITY_ATTRIBUTES) NULL, 
     OPEN_EXISTING, 
     FILE_ATTRIBUTE_NORMAL, 
     (HANDLE) NULL); 
 
   if (hFile == INVALID_HANDLE_VALUE) 
   { 
      printf("CreateFile failed with %d.\n", GetLastError()); 
      return FALSE; 
   } 
 
   WriteSlot(hFile, TEXT("Message one for mailslot."));
   WriteSlot(hFile, TEXT("Message two for mailslot."));

   Sleep(5000);

   WriteSlot(hFile, TEXT("Message three for mailslot."));
 
   CloseHandle(hFile); 
 
   return TRUE;
}
```



<span data-ttu-id="ae204-109">以下是在執行此範例時，會顯示的輸出，以及 [從信箱讀取](reading-from-a-mailslot.md)時所顯示的信箱伺服器。</span><span class="sxs-lookup"><span data-stu-id="ae204-109">The following is the output that is displayed when this example is run with the mailslot server shown in [Reading from a Mailslot](reading-from-a-mailslot.md).</span></span>

``` syntax
Slot written to successfully.
Slot written to successfully.
Slot written to successfully.
```

 

 
