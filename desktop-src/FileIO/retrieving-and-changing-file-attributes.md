---
description: 示範如何使用 GetFileAttributesEx 函數來取出檔案屬性的範例程式碼。
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: 取出和變更檔案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c980ddd6390f016b2057392f42f6bf645859307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980599"
---
# <a name="retrieving-and-changing-file-attributes"></a><span data-ttu-id="9cc36-103">取出和變更檔案屬性</span><span class="sxs-lookup"><span data-stu-id="9cc36-103">Retrieving and Changing File Attributes</span></span>

<span data-ttu-id="9cc36-104">應用程式可以使用 [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 或 [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) 函式來取得檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc36-104">An application can retrieve the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function.</span></span> <span data-ttu-id="9cc36-105">[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)和 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)函數可以設定許多屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc36-105">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) functions can set many of the attributes.</span></span> <span data-ttu-id="9cc36-106">但是，應用程式無法設定所有屬性。</span><span class="sxs-lookup"><span data-stu-id="9cc36-106">However, applications cannot set all attributes.</span></span>

<span data-ttu-id="9cc36-107">本主題中的程式碼範例會使用 [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) 函式，將目前目錄中 ( .txt) 的所有文字檔，複製到唯讀檔案的新目錄。</span><span class="sxs-lookup"><span data-stu-id="9cc36-107">The code example in this topic uses the [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) function to copy all text files (.txt) in the current directory to a new directory of read-only files.</span></span> <span data-ttu-id="9cc36-108">必要時，新目錄中的檔案會變更為唯讀。</span><span class="sxs-lookup"><span data-stu-id="9cc36-108">Files in the new directory are changed to read only, if necessary.</span></span>

<span data-ttu-id="9cc36-109">應用程式會使用 [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) 函式，建立指定為參數的目錄。</span><span class="sxs-lookup"><span data-stu-id="9cc36-109">The application creates the directory specified as a parameter by using the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) function.</span></span> <span data-ttu-id="9cc36-110">目錄還不能存在。</span><span class="sxs-lookup"><span data-stu-id="9cc36-110">The directory must not exist already.</span></span>

<span data-ttu-id="9cc36-111">應用程式會使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) 和 [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) 函數來搜尋目前目錄中的所有文字檔。</span><span class="sxs-lookup"><span data-stu-id="9cc36-111">The application searches the current directory for all text files by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions.</span></span> <span data-ttu-id="9cc36-112">每個文字檔都會複製到 \\ TextRO 目錄中。</span><span class="sxs-lookup"><span data-stu-id="9cc36-112">Each text file is copied to the \\TextRO directory.</span></span> <span data-ttu-id="9cc36-113">複製檔案之後， [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 函式會判斷檔案是否為唯讀。</span><span class="sxs-lookup"><span data-stu-id="9cc36-113">After a file is copied, the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function determines whether or not a file is read only.</span></span> <span data-ttu-id="9cc36-114">如果檔案不是唯讀的，則應用程式會將目錄變更為 \\ TextRO，並使用 [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) 函式將複製的檔案轉換成隻讀。</span><span class="sxs-lookup"><span data-stu-id="9cc36-114">If the file is not read only, the application changes directories to \\TextRO and converts the copied file to read only by using the [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) function.</span></span>

<span data-ttu-id="9cc36-115">複製目前目錄中的所有文字檔之後，應用程式會使用 [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) 函數來關閉搜尋控制碼。</span><span class="sxs-lookup"><span data-stu-id="9cc36-115">After all text files in the current directory are copied, the application closes the search handle by using the [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9cc36-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9cc36-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cc36-117">**檔案屬性常數**</span><span class="sxs-lookup"><span data-stu-id="9cc36-117">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> <dt>

[<span data-ttu-id="9cc36-118">檔案名、路徑和命名空間</span><span class="sxs-lookup"><span data-stu-id="9cc36-118">File Names, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



