---
description: 應用程式可以使用變更通知來監視目錄及其子目錄的內容。
ms.assetid: ad884b15-e040-478b-aa99-d8622198f62a
title: 取得目錄變更通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44375c334c3630aee09bf4a13fc23f87cc91e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691459"
---
# <a name="obtaining-directory-change-notifications"></a><span data-ttu-id="68b47-103">取得目錄變更通知</span><span class="sxs-lookup"><span data-stu-id="68b47-103">Obtaining Directory Change Notifications</span></span>

<span data-ttu-id="68b47-104">應用程式可以使用變更通知來監視目錄及其子目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="68b47-104">An application can monitor the contents of a directory and its subdirectories by using change notifications.</span></span> <span data-ttu-id="68b47-105">等候變更通知類似于讓目錄的讀取作業暫止，並視需要將其子目錄。</span><span class="sxs-lookup"><span data-stu-id="68b47-105">Waiting for a change notification is similar to having a read operation pending against a directory and, if necessary, its subdirectories.</span></span> <span data-ttu-id="68b47-106">當正在監看的目錄中有某些變更時，就會完成讀取操作。</span><span class="sxs-lookup"><span data-stu-id="68b47-106">When something changes within the directory being watched, the read operation is completed.</span></span> <span data-ttu-id="68b47-107">例如，應用程式可以使用這些函式，在受監視目錄中的檔案名變更時，更新目錄清單。</span><span class="sxs-lookup"><span data-stu-id="68b47-107">For example, an application can use these functions to update a directory listing whenever a file name within the monitored directory changes.</span></span>

<span data-ttu-id="68b47-108">應用程式可以使用 [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) 函數來指定觸發變更通知的一組條件。</span><span class="sxs-lookup"><span data-stu-id="68b47-108">An application can specify a set of conditions that trigger a change notification by using the [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) function.</span></span> <span data-ttu-id="68b47-109">這些條件包括檔案名、目錄名稱、屬性、檔案大小、上次寫入時間和安全性的變更。</span><span class="sxs-lookup"><span data-stu-id="68b47-109">The conditions include changes to file names, directory names, attributes, file size, time of last write, and security.</span></span> <span data-ttu-id="68b47-110">此函式也會傳回可使用 [wait 函數](/windows/desktop/Sync/wait-functions)等候的控制碼。</span><span class="sxs-lookup"><span data-stu-id="68b47-110">This function also returns a handle that can be waited on by using the [wait functions](/windows/desktop/Sync/wait-functions).</span></span> <span data-ttu-id="68b47-111">如果符合等待條件， [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) 可以用來提供通知控制碼，等候後續的變更。</span><span class="sxs-lookup"><span data-stu-id="68b47-111">If the wait condition is satisfied, [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification) can be used to provide a notification handle to wait on subsequent changes.</span></span> <span data-ttu-id="68b47-112">不過，這些函式不會指出滿足等候條件的實際變更。</span><span class="sxs-lookup"><span data-stu-id="68b47-112">However, these functions do not indicate the actual change that satisfied the wait condition.</span></span>

<span data-ttu-id="68b47-113">使用 [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) 來關閉通知控制碼。</span><span class="sxs-lookup"><span data-stu-id="68b47-113">Use [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) to close the notification handle.</span></span>

<span data-ttu-id="68b47-114">若要在通知中取出特定變更的相關資訊，請使用 [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) 函數。</span><span class="sxs-lookup"><span data-stu-id="68b47-114">To retrieve information about the specific change as part of the notification, use the [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) function.</span></span> <span data-ttu-id="68b47-115">此函數也可讓您提供完成常式。</span><span class="sxs-lookup"><span data-stu-id="68b47-115">This function also enables you to provide a completion routine.</span></span>

<span data-ttu-id="68b47-116">若要追蹤磁片區的變更，請參閱 [變更日誌](change-journals.md)。</span><span class="sxs-lookup"><span data-stu-id="68b47-116">To track changes on a volume, see [change journals](change-journals.md).</span></span>

<span data-ttu-id="68b47-117">下列範例會監視目錄名稱變更的目錄樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="68b47-117">The following example monitors the directory tree for directory name changes.</span></span> <span data-ttu-id="68b47-118">它也會監視目錄以進行檔案名變更。</span><span class="sxs-lookup"><span data-stu-id="68b47-118">It also monitors a directory for file name changes.</span></span> <span data-ttu-id="68b47-119">此範例會使用 [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) 函數來建立兩個通知控制碼，並使用 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) 函式來等候控制碼。</span><span class="sxs-lookup"><span data-stu-id="68b47-119">The example uses the [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) function to create two notification handles and the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to wait on the handles.</span></span> <span data-ttu-id="68b47-120">每當在樹狀結構中建立或刪除目錄時，此範例應該會更新整個目錄樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="68b47-120">Whenever a directory is created or deleted in the tree, the example should update the entire directory tree.</span></span> <span data-ttu-id="68b47-121">每當在目錄中建立或刪除檔案時，範例都應該重新整理目錄。</span><span class="sxs-lookup"><span data-stu-id="68b47-121">Whenever a file is created or deleted in the directory, the example should refresh the directory.</span></span>

> [!Note]
>
> <span data-ttu-id="68b47-122">這個簡單的範例會使用 [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函式來進行終止和清除，但更複雜的應用程式應該一律使用適當的資源管理，例如 [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) 。</span><span class="sxs-lookup"><span data-stu-id="68b47-122">This simplistic example uses the [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) function for termination and cleanup, but more complex applications should always use proper resource management such as [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification) where appropriate.</span></span>

 


```C++
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <tchar.h>

void RefreshDirectory(LPTSTR);
void RefreshTree(LPTSTR);
void WatchDirectory(LPTSTR);

void _tmain(int argc, TCHAR *argv[])
{
    if(argc != 2)
    {
        _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
        return;
    }

    WatchDirectory(argv[1]);
}

void WatchDirectory(LPTSTR lpDir)
{
   DWORD dwWaitStatus; 
   HANDLE dwChangeHandles[2]; 
   TCHAR lpDrive[4];
   TCHAR lpFile[_MAX_FNAME];
   TCHAR lpExt[_MAX_EXT];

   _tsplitpath_s(lpDir, lpDrive, 4, NULL, 0, lpFile, _MAX_FNAME, lpExt, _MAX_EXT);

   lpDrive[2] = (TCHAR)'\\';
   lpDrive[3] = (TCHAR)'\0';
 
// Watch the directory for file creation and deletion. 
 
   dwChangeHandles[0] = FindFirstChangeNotification( 
      lpDir,                         // directory to watch 
      FALSE,                         // do not watch subtree 
      FILE_NOTIFY_CHANGE_FILE_NAME); // watch file name changes 
 
   if (dwChangeHandles[0] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 
// Watch the subtree for directory creation and deletion. 
 
   dwChangeHandles[1] = FindFirstChangeNotification( 
      lpDrive,                       // directory to watch 
      TRUE,                          // watch the subtree 
      FILE_NOTIFY_CHANGE_DIR_NAME);  // watch dir name changes 
 
   if (dwChangeHandles[1] == INVALID_HANDLE_VALUE) 
   {
     printf("\n ERROR: FindFirstChangeNotification function failed.\n");
     ExitProcess(GetLastError()); 
   }
 

// Make a final validation check on our handles.

   if ((dwChangeHandles[0] == NULL) || (dwChangeHandles[1] == NULL))
   {
     printf("\n ERROR: Unexpected NULL from FindFirstChangeNotification.\n");
     ExitProcess(GetLastError()); 
   }

// Change notification is set. Now wait on both notification 
// handles and refresh accordingly. 
 
   while (TRUE) 
   { 
   // Wait for notification.
 
      printf("\nWaiting for notification...\n");

      dwWaitStatus = WaitForMultipleObjects(2, dwChangeHandles, 
         FALSE, INFINITE); 
 
      switch (dwWaitStatus) 
      { 
         case WAIT_OBJECT_0: 
 
         // A file was created, renamed, or deleted in the directory.
         // Refresh this directory and restart the notification.
 
             RefreshDirectory(lpDir); 
             if ( FindNextChangeNotification(dwChangeHandles[0]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_OBJECT_0 + 1: 
 
         // A directory was created, renamed, or deleted.
         // Refresh the tree and restart the notification.
 
             RefreshTree(lpDrive); 
             if (FindNextChangeNotification(dwChangeHandles[1]) == FALSE )
             {
               printf("\n ERROR: FindNextChangeNotification function failed.\n");
               ExitProcess(GetLastError()); 
             }
             break; 
 
         case WAIT_TIMEOUT:

         // A timeout occurred, this would happen if some value other 
         // than INFINITE is used in the Wait call and no changes occur.
         // In a single-threaded environment you might not want an
         // INFINITE wait.
 
            printf("\nNo changes in the timeout period.\n");
            break;

         default: 
            printf("\n ERROR: Unhandled dwWaitStatus.\n");
            ExitProcess(GetLastError());
            break;
      }
   }
}

void RefreshDirectory(LPTSTR lpDir)
{
   // This is where you might place code to refresh your
   // directory listing, but not the subtree because it
   // would not be necessary.

   _tprintf(TEXT("Directory (%s) changed.\n"), lpDir);
}

void RefreshTree(LPTSTR lpDrive)
{
   // This is where you might place code to refresh your
   // directory listing, including the subtree.

   _tprintf(TEXT("Directory tree (%s) changed.\n"), lpDrive);
}
```



 

 
