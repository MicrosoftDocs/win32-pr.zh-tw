---
description: 示範如何使用 GetFileAttributesEx 函數來取出檔案屬性的範例程式碼。
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: 取出和變更檔案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2609030d1657b78c266ed6b10841159e0df4d40a2e3b07b0fce42e98b45d54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015136"
---
# <a name="retrieving-and-changing-file-attributes"></a>取出和變更檔案屬性

應用程式可以使用 [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 或 [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) 函式來取得檔案屬性。 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)和 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)函數可以設定許多屬性。 但是，應用程式無法設定所有屬性。

本主題中的程式碼範例使用 [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) 函式，將目前目錄中 (.txt) 的所有文本檔案複製到唯讀檔案的新目錄。 必要時，新目錄中的檔案會變更為唯讀。

應用程式會使用 [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) 函式，建立指定為參數的目錄。 目錄還不能存在。

應用程式會使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) 和 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) 函數來搜尋目前目錄中的所有文字檔。 每個文字檔都會複製到 \\ TextRO 目錄中。 複製檔案之後， [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 函式會判斷檔案是否為唯讀。 如果檔案不是唯讀的，則應用程式會將目錄變更為 \\ TextRO，並使用 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) 函式將複製的檔案轉換成隻讀。

複製目前目錄中的所有文字檔之後，應用程式會使用 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數來關閉搜尋控制碼。


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void _tmain(int argc, TCHAR* argv[])
{
   WIN32_FIND_DATA FileData;
   HANDLE          hSearch;
   DWORD           dwAttrs;
   TCHAR           szNewPath[MAX_PATH];   
 
   BOOL            fFinished = FALSE; 

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }
 
// Create a new directory. 
 
   if (!CreateDirectory(argv[1], NULL)) 
   { 
      printf("CreateDirectory failed (%d)\n", GetLastError()); 
      return;
   } 
 
// Start searching for text files in the current directory. 
 
   hSearch = FindFirstFile(TEXT("*.txt"), &FileData); 
   if (hSearch == INVALID_HANDLE_VALUE) 
   { 
      printf("No text files found.\n"); 
      return;
   } 
 
// Copy each .TXT file to the new directory 
// and change it to read only, if not already. 
 
   while (!fFinished) 
   { 
      StringCchPrintf(szNewPath, sizeof(szNewPath)/sizeof(szNewPath[0]), TEXT("%s\\%s"), argv[1], FileData.cFileName);

      if (CopyFile(FileData.cFileName, szNewPath, FALSE))
      { 
         dwAttrs = GetFileAttributes(FileData.cFileName); 
         if (dwAttrs==INVALID_FILE_ATTRIBUTES) return; 

         if (!(dwAttrs & FILE_ATTRIBUTE_READONLY)) 
         { 
            SetFileAttributes(szNewPath, 
                dwAttrs | FILE_ATTRIBUTE_READONLY); 
         } 
      } 
      else 
      { 
         printf("Could not copy file.\n"); 
         return;
      } 
 
      if (!FindNextFile(hSearch, &FileData)) 
      {
         if (GetLastError() == ERROR_NO_MORE_FILES) 
         { 
            _tprintf(TEXT("Copied *.txt to %s\n"), argv[1]); 
            fFinished = TRUE; 
         } 
         else 
         { 
            printf("Could not find next file.\n"); 
            return;
         } 
      }
   } 
 
// Close the search handle. 
 
   FindClose(hSearch);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檔案屬性常數**](file-attribute-constants.md)
</dt> <dt>

[檔案名、路徑和命名空間](naming-a-file.md)
</dt> </dl>

 

 



