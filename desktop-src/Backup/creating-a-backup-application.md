---
title: 建立備份應用程式
description: 若要在磁帶上執行輸入或輸出，備份應用程式必須先取得磁帶裝置的控制碼。 下列程式碼範例說明如何使用 CreateFile 函式來開啟磁帶裝置。
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- 備份應用程式備份
- 建立備份應用程式備份
- 備份備份，建立應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77409a0c74ee61e333b92dad8b22d9c68ed92eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023846"
---
# <a name="creating-a-backup-application"></a><span data-ttu-id="b3e4e-107">建立備份應用程式</span><span class="sxs-lookup"><span data-stu-id="b3e4e-107">Creating a Backup Application</span></span>

<span data-ttu-id="b3e4e-108">若要在磁帶上執行輸入或輸出，備份應用程式必須先取得磁帶裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-108">To perform input or output on a tape, a backup application must first obtain a handle of the tape device.</span></span> <span data-ttu-id="b3e4e-109">下列程式碼範例說明如何使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟磁帶裝置。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-109">The following code sample shows you how to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a tape device.</span></span>


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



<span data-ttu-id="b3e4e-110">若要將目錄樹狀目錄備份到磁帶，應用程式必須使用 [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) 和 [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) 函式來跨越目錄樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-110">To back up a directory tree to a tape, an application must use the [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) functions to traverse the directory tree.</span></span> <span data-ttu-id="b3e4e-111">每次找到檔案時，應用程式都應該使用 [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) 函式來取得檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-111">Each time a file is found, the application should get the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) function.</span></span>

<span data-ttu-id="b3e4e-112">如果有永久連結，應用程式應該決定連結數目，並將檔案的唯一識別碼儲存在資料表中，以供日後比較。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-112">If there are hard links, an application should determine the number of links, and save the unique identifier of the file in a table for future comparisons.</span></span> <span data-ttu-id="b3e4e-113">第一次找到檔案時，應用程式應該使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 來開啟檔案，並使用 [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) 函式來開始備份。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-113">The first time a file is found, the application should use [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open the file, and the [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) function to begin the backup.</span></span> <span data-ttu-id="b3e4e-114">然後，它可以重複使用 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) 函式，將 **BackupRead** 所使用的緩衝區中的所有資訊傳送至磁帶。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-114">Then it can use the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function repeatedly to transfer all the information in the buffer used by **BackupRead** to the tape.</span></span> <span data-ttu-id="b3e4e-115">第二次發現檔案時 (在) 有永久連結時，根據檔案識別碼的表格進行檢查，應用程式可以將一般檔案資訊寫入磁帶，然後再以具有 **備份 \_ 連結** 識別碼的資料流程來寫入。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-115">The second time a file is found (checked against the table of file identifiers when there are hard links), the application can write the general file information to the tape, followed by a stream that has an identifier that is **BACKUP\_LINK**.</span></span>

<span data-ttu-id="b3e4e-116">從磁帶還原檔案到磁片時，應用程式必須使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)、 [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)和 [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) 功能。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-116">When restoring files from tape to disk, an application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite), and [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) functions.</span></span> <span data-ttu-id="b3e4e-117">針對磁帶上的每個檔案，應用程式應該使用 **CreateFile** 在磁片上建立新的檔案，並使用 **BackupWrite** 來開始還原檔案。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-117">For each file on a tape, the application should use **CreateFile** to create a new file on disk, and **BackupWrite** to begin restoring the file.</span></span> <span data-ttu-id="b3e4e-118">然後，應用程式應該重複使用 **ReadFile** ，直到檔案的所有資訊都從磁帶讀取到由 **BackupWrite** 填滿的緩衝區為止。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-118">Then the application should use **ReadFile** repeatedly until all the information for the file is read from the tape into the buffer filled by **BackupWrite**.</span></span>

<span data-ttu-id="b3e4e-119">如果 [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) 緩衝區中的其中一個資料流程有 **備份 \_ 連結** 資料流程識別碼，應用程式必須建立永久連結。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-119">If one of the streams in the [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) buffer has a **BACKUP\_LINK** stream identifier, the application must establish a hard link.</span></span> <span data-ttu-id="b3e4e-120">如果建立連結所需的資料不存在， **BackupWrite** 就會失敗。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-120">If the data needed to establish the link does not exist, **BackupWrite** fails.</span></span> <span data-ttu-id="b3e4e-121">應用程式可以使用預先存在的目錄來找出並還原原始資料，也可以通知使用者要還原的檔案資料位於不同的位置。</span><span class="sxs-lookup"><span data-stu-id="b3e4e-121">The application can use a pre-existing catalog to locate and restore the original data, or it can notify the user that the file data to be restored is in a different location.</span></span>

 

 