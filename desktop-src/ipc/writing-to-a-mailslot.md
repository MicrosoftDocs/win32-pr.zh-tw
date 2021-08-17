---
description: 如何寫入信箱。 寫入郵筒類似于寫入至標準磁片檔案。
ms.assetid: a69ba953-cd5c-487f-b9e0-dbd6c44b88b8
title: 寫入郵筒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d13c31fd6b24217267b394f80c2dcdf551b6949f8692811173021fb78326f2f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359307"
---
# <a name="writing-to-a-mailslot"></a>寫入郵筒

寫入郵筒類似于寫入至標準磁片檔案。 下列程式碼會使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)、 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)和 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式，在信箱中放入簡短的訊息。 此訊息會廣播至本機電腦上名為「範例郵筒」的郵筒伺服器 \_ 。 程式碼會在已建立的郵筒伺服器的假設下運作。


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



以下是在執行此範例時，會顯示的輸出，以及 [從信箱讀取](reading-from-a-mailslot.md)時所顯示的信箱伺服器。

``` syntax
Slot written to successfully.
Slot written to successfully.
Slot written to successfully.
```

 

 
