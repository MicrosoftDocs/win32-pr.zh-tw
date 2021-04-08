---
description: 對磁片區中的檔案或目錄進行任何變更時，該磁片區的 USN 變更日誌會以變更的描述和檔案或目錄的名稱進行更新。
ms.assetid: 9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d
title: 變更日誌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5052ec87830a822270071a6ee00f1c3f7cffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852139"
---
# <a name="change-journals"></a><span data-ttu-id="61630-103">變更日誌</span><span class="sxs-lookup"><span data-stu-id="61630-103">Change Journals</span></span>

<span data-ttu-id="61630-104">自動備份應用程式是程式的其中一個範例，必須檢查磁片區狀態的變更，以執行其工作。</span><span class="sxs-lookup"><span data-stu-id="61630-104">An automatic backup application is one example of a program that must check for changes to the state of a volume to perform its task.</span></span> <span data-ttu-id="61630-105">檢查目錄或檔案中之變更的暴力密碼破解方法是掃描整個磁片區。</span><span class="sxs-lookup"><span data-stu-id="61630-105">The brute force method of checking for changes in directories or files is to scan the entire volume.</span></span> <span data-ttu-id="61630-106">不過，這通常不是可行的方法，因為系統效能會降低。</span><span class="sxs-lookup"><span data-stu-id="61630-106">However, this is often not an acceptable approach because of the decrease in system performance it would cause.</span></span> <span data-ttu-id="61630-107">另一種方法是讓應用程式藉由呼叫 [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) 或 [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) 函式來註冊目錄通知 (，) 以備份目錄。</span><span class="sxs-lookup"><span data-stu-id="61630-107">Another method is for the application to register a directory notification (by calling the [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa) or [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw) functions) for the directories to be backed up.</span></span> <span data-ttu-id="61630-108">這比第一個方法更有效率，不過，它需要應用程式隨時執行。</span><span class="sxs-lookup"><span data-stu-id="61630-108">This is more efficient than the first method, however, it requires that an application be running at all times.</span></span> <span data-ttu-id="61630-109">此外，如果必須備份大量的目錄和檔案，則這類應用程式的處理和記憶體額外負荷可能也會導致作業系統的效能降低。</span><span class="sxs-lookup"><span data-stu-id="61630-109">Also, if a large number of directories and files must be backed up, the amount of processing and memory overhead for such an application might also cause the operating system's performance to decrease.</span></span>

<span data-ttu-id="61630-110">為了避免這些缺點，NTFS 檔案系統會維持更新序號 (USN) 變更日誌。</span><span class="sxs-lookup"><span data-stu-id="61630-110">To avoid these disadvantages, the NTFS file system maintains an update sequence number (USN) change journal.</span></span> <span data-ttu-id="61630-111">對磁片區中的檔案或目錄進行任何變更時，該磁片區的 USN 變更日誌會以變更的描述和檔案或目錄的名稱進行更新。</span><span class="sxs-lookup"><span data-stu-id="61630-111">When any change is made to a file or directory in a volume, the USN change journal for that volume is updated with a description of the change and the name of the file or directory.</span></span>

<span data-ttu-id="61630-112">您也需要變更日誌來復原檔案系統索引，例如在電腦或磁片區失敗之後。</span><span class="sxs-lookup"><span data-stu-id="61630-112">Change journals are also needed to recover file system indexing for example after a computer or volume failure.</span></span> <span data-ttu-id="61630-113">復原索引的能力，是指檔案系統可避免在這種情況下重新編制整個磁片區的耗時處理常式。</span><span class="sxs-lookup"><span data-stu-id="61630-113">The ability to recover indexing means the file system can avoid the time-consuming process of reindexing the entire volume in such cases.</span></span>

<span data-ttu-id="61630-114">下列主題討論變更日誌。</span><span class="sxs-lookup"><span data-stu-id="61630-114">The following topics discuss change journals.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="61630-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="61630-115">In this section</span></span>



| <span data-ttu-id="61630-116">主題</span><span class="sxs-lookup"><span data-stu-id="61630-116">Topic</span></span>                                                                                                                             | <span data-ttu-id="61630-117">描述</span><span class="sxs-lookup"><span data-stu-id="61630-117">Description</span></span>                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61630-118">變更日誌記錄</span><span class="sxs-lookup"><span data-stu-id="61630-118">Change Journal Records</span></span>](change-journal-records.md)<br/>                                                                   | <span data-ttu-id="61630-119">新增、刪除和修改檔案、目錄和其他 NTFS 檔案系統物件時，NTFS 檔案系統會在資料流程中輸入變更日誌記錄，電腦上的每個磁片區都會有一個記錄。</span><span class="sxs-lookup"><span data-stu-id="61630-119">As files, directories, and other NTFS file system objects are added, deleted, and modified, the NTFS file system enters change journal records in streams, one for each volume on the computer.</span></span><br/>                                           |
| [<span data-ttu-id="61630-120">使用變更日誌識別碼</span><span class="sxs-lookup"><span data-stu-id="61630-120">Using the Change Journal Identifier</span></span>](using-the-change-journal-identifier.md)<br/>                                         | <span data-ttu-id="61630-121">NTFS 檔案系統會將不帶正負號的64位識別碼與每個變更日誌產生關聯。</span><span class="sxs-lookup"><span data-stu-id="61630-121">The NTFS file system associates an unsigned 64-bit identifier with each change journal.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="61630-122">建立、修改和刪除變更日誌</span><span class="sxs-lookup"><span data-stu-id="61630-122">Creating, Modifying, and Deleting a Change Journal</span></span>](creating-modifying-and-deleting-a-change-journal.md)<br/>             | <span data-ttu-id="61630-123">系統管理員可以建立、刪除及重新建立變更日誌。</span><span class="sxs-lookup"><span data-stu-id="61630-123">Administrators can create, delete, and re-create change journals.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="61630-124">取得變更日誌作業的磁片區控制碼</span><span class="sxs-lookup"><span data-stu-id="61630-124">Obtaining a Volume Handle for Change Journal Operations</span></span>](obtaining-a-volume-handle-for-change-journal-operations.md)<br/> | <span data-ttu-id="61630-125">若要取得磁片區的控制碼以用於更新序號 (USN) 變更日誌作業，請呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式，並將 *lpFileName* 參數設定為下列格式的字串： \\ \\ 。 \\*X*。</span><span class="sxs-lookup"><span data-stu-id="61630-125">To obtain a handle to a volume for use with update sequence number (USN) change journal operations, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the *lpFileName* parameter set to a string of the following form: \\\\.\\*X*.</span></span><br/> |
| [<span data-ttu-id="61630-126">變更日誌作業</span><span class="sxs-lookup"><span data-stu-id="61630-126">Change Journal Operations</span></span>](change-journal-operations.md)<br/>                                                             | <span data-ttu-id="61630-127">控制與 NTFS 檔案系統更新序號搭配使用的代碼和結構 (USN) 變更日誌。</span><span class="sxs-lookup"><span data-stu-id="61630-127">Control codes and structures to use with the NTFS file system update sequence number (USN) change journal.</span></span><br/>                                                                                                                                |



 

 

 




