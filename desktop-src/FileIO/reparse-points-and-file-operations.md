---
description: 描述重新剖析點如何啟用從大部分 Windows 開發人員預期的行為離開的檔案系統行為。
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: 重新分析點和檔案作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194218"
---
# <a name="reparse-points-and-file-operations"></a><span data-ttu-id="bb86d-103">重新分析點和檔案作業</span><span class="sxs-lookup"><span data-stu-id="bb86d-103">Reparse Points and File Operations</span></span>

<span data-ttu-id="bb86d-104">重新 *分析點* 會啟用離開自大部分 Windows 開發人員可能習慣的行為的檔案系統行為，因此，在撰寫操作檔案的應用程式時，若要存取支援重新分析點的檔案系統，就必須注意這些行為。</span><span class="sxs-lookup"><span data-stu-id="bb86d-104">*Reparse points* enable file system behavior that departs from the behavior most Windows developers may be accustomed to, therefore being aware of these behaviors when writing applications that manipulate files is vital to robust and reliable applications intended to access file systems that support reparse points.</span></span> <span data-ttu-id="bb86d-105">這些考慮的範圍取決於特定的重新分析點（可供使用者定義）的特定執行和相關檔案系統篩選器行為。</span><span class="sxs-lookup"><span data-stu-id="bb86d-105">The extent of these considerations will depend on the specific implementation and associated file system filter behavior of a particular reparse point, which can be user-defined.</span></span> <span data-ttu-id="bb86d-106">如需詳細資訊，請參閱重新 [分析點](reparse-points.md)。</span><span class="sxs-lookup"><span data-stu-id="bb86d-106">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="bb86d-107">請考慮下列有關 NTFS 重新分析點執行的範例，其中包括掛接的資料夾、連結的檔案和 Microsoft 遠端存放伺服器：</span><span class="sxs-lookup"><span data-stu-id="bb86d-107">Consider the following examples regarding NTFS reparse point implementations, which include mounted folders, linked files, and the Microsoft Remote Storage Server:</span></span>

-   <span data-ttu-id="bb86d-108">使用檔案 [資料流程](file-streams.md)的備份應用程式應該在使用重新分析點來備份檔案時，指定 [**WIN32 \_ 資料流程 \_ 識別碼**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id)結構中的 **備份重新 \_ 分析 \_ 資料**。</span><span class="sxs-lookup"><span data-stu-id="bb86d-108">Backup applications that use [file streams](file-streams.md) should specify **BACKUP\_REPARSE\_DATA** in the [**WIN32\_STREAM\_ID**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) structure when backing up files with reparse points.</span></span>
-   <span data-ttu-id="bb86d-109">使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式的應用程式應該在開啟檔案時，指定檔案 **旗標開啟重新 \_ \_ \_ 分析 \_ 點** 旗標（如果它是重新分析點）。</span><span class="sxs-lookup"><span data-stu-id="bb86d-109">Applications that use the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function should specify the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag when opening the file if it is a reparse point.</span></span> <span data-ttu-id="bb86d-110">如需詳細資訊，請參閱 [建立及開啟](creating-and-opening-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="bb86d-110">For more information, see [Creating and Opening Files](creating-and-opening-files.md).</span></span>
-   <span data-ttu-id="bb86d-111">重新 [整理](defragmenting-files.md) 檔案的程式需要對重新剖析點進行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="bb86d-111">The process of [defragmenting files](defragmenting-files.md) requires special handling for reparse points.</span></span>
-   <span data-ttu-id="bb86d-112">病毒偵測應用程式應該搜尋指出連結檔案的重新分析點。</span><span class="sxs-lookup"><span data-stu-id="bb86d-112">Virus detection applications should search for reparse points that indicate linked files.</span></span>
-   <span data-ttu-id="bb86d-113">大部分的應用程式都應該針對已移至長期儲存的檔案採取特殊動作，如果只是通知使用者可能需要一段時間才能取出檔案。</span><span class="sxs-lookup"><span data-stu-id="bb86d-113">Most applications should take special actions for files that have been moved to long-term storage, if only to notify the user that it may take a while to retrieve the file.</span></span>
-   <span data-ttu-id="bb86d-114">[**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid)函式會根據檔案 **旗標開啟重新 \_ \_ \_ 分析 \_ 點** 旗標的使用，開啟檔案或重新分析點。</span><span class="sxs-lookup"><span data-stu-id="bb86d-114">The [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) function will either open the file or the reparse point, depending on the use of the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span>
-   <span data-ttu-id="bb86d-115">符號連結（作為重新分析點）有特定的程式 [設計考慮](symbolic-link-programming-considerations.md) 。</span><span class="sxs-lookup"><span data-stu-id="bb86d-115">Symbolic links, as reparse points, have certain [programming considerations](symbolic-link-programming-considerations.md) specific to them.</span></span>
-   <span data-ttu-id="bb86d-116">讀取更新序號的磁片區管理活動 (USN) 變更日誌記錄在使用 [**USN \_ 記錄**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 和 [**讀取 \_ usn \_ 日誌 \_ 資料**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) 結構時，需要重新剖析點的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="bb86d-116">Volume management activities for reading update sequence number (USN) change journal records require special handling for reparse points when using the [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**READ\_USN\_JOURNAL\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb86d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb86d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb86d-118">判斷目錄是否為裝載的資料夾</span><span class="sxs-lookup"><span data-stu-id="bb86d-118">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[<span data-ttu-id="bb86d-119">建立載入的資料夾</span><span class="sxs-lookup"><span data-stu-id="bb86d-119">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[<span data-ttu-id="bb86d-120">檔案系統函數的符號連結效果</span><span class="sxs-lookup"><span data-stu-id="bb86d-120">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
