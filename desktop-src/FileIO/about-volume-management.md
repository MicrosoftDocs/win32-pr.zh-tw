---
description: 磁片區是由稱為磁片區管理員的設備磁碟機所執行。
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: 關於磁片區管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994514"
---
# <a name="about-volume-management"></a><span data-ttu-id="bafd2-103">關於磁片區管理</span><span class="sxs-lookup"><span data-stu-id="bafd2-103">About Volume Management</span></span>

<span data-ttu-id="bafd2-104">磁片區是由稱為磁片區管理員的設備磁碟機所執行。</span><span class="sxs-lookup"><span data-stu-id="bafd2-104">Volumes are implemented by a device driver called a volume manager.</span></span> <span data-ttu-id="bafd2-105">範例包括 FtDisk Manager、邏輯磁片管理員 (LDM) ，以及 VERITAS Logical Volume Manager (LVM) 。</span><span class="sxs-lookup"><span data-stu-id="bafd2-105">Examples include the FtDisk Manager, the Logical Disk Manager (LDM), and the VERITAS Logical Volume Manager (LVM).</span></span> <span data-ttu-id="bafd2-106">磁片區管理員提供一層實體抽象化、資料保護 (使用某種形式的 RAID) 和效能。</span><span class="sxs-lookup"><span data-stu-id="bafd2-106">Volume managers provide a layer of physical abstraction, data protection (using some form of RAID), and performance.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bafd2-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="bafd2-107">In this section</span></span>



| <span data-ttu-id="bafd2-108">主題</span><span class="sxs-lookup"><span data-stu-id="bafd2-108">Topic</span></span>                                                                       | <span data-ttu-id="bafd2-109">描述</span><span class="sxs-lookup"><span data-stu-id="bafd2-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bafd2-110">檔案系統識別</span><span class="sxs-lookup"><span data-stu-id="bafd2-110">File System Recognition</span></span>](file-system-recognition.md)<br/>           | <span data-ttu-id="bafd2-111">檔案系統辨識的目標是要讓 Windows 作業系統擁有一個額外的選項，以供有效但無法辨識的檔案系統（非「原始」）使用。</span><span class="sxs-lookup"><span data-stu-id="bafd2-111">The goal of file system recognition is to allow the Windows operating system to have an additional option for a valid but unrecognized file system other than "RAW".</span></span><br/>                                                                                                         |
| [<span data-ttu-id="bafd2-112">命名磁片區</span><span class="sxs-lookup"><span data-stu-id="bafd2-112">Naming a Volume</span></span>](naming-a-volume.md)<br/>                           | <span data-ttu-id="bafd2-113">標籤是指派給磁片區（通常是由使用者使用）的易記名稱，可讓您更容易辨識。</span><span class="sxs-lookup"><span data-stu-id="bafd2-113">A label is a user-friendly name that is assigned to a volume, usually by an end user, to make it easier to recognize.</span></span> <span data-ttu-id="bafd2-114">磁片區可以有標籤、磁碟機號、兩者或兩者皆有。</span><span class="sxs-lookup"><span data-stu-id="bafd2-114">A volume can have a label, a drive letter, both, or neither.</span></span> <span data-ttu-id="bafd2-115">若要設定磁片區的標籤，請使用 [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) 函數。</span><span class="sxs-lookup"><span data-stu-id="bafd2-115">To set the label for a volume, use the [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) function.</span></span><br/> |
| [<span data-ttu-id="bafd2-116">列舉磁片區</span><span class="sxs-lookup"><span data-stu-id="bafd2-116">Enumerating Volumes</span></span>](enumerating-volumes.md)<br/>                   | <span data-ttu-id="bafd2-117">若要在電腦上建立磁片區的完整清單，或輪流操作每個磁片區，您可以列舉磁片區。</span><span class="sxs-lookup"><span data-stu-id="bafd2-117">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="bafd2-118">取得磁片區資訊</span><span class="sxs-lookup"><span data-stu-id="bafd2-118">Obtaining Volume Information</span></span>](obtaining-volume-information.md)<br/> | <span data-ttu-id="bafd2-119">存取指定磁片區上的檔案和目錄之前，您應該使用 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式來判斷檔案系統的功能。</span><span class="sxs-lookup"><span data-stu-id="bafd2-119">Before you access files and directories on a given volume, you should determine the capabilities of the file system by using the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function.</span></span><br/>                                                                              |
| [<span data-ttu-id="bafd2-120">變更日誌</span><span class="sxs-lookup"><span data-stu-id="bafd2-120">Change Journals</span></span>](change-journals.md)<br/>                           | <span data-ttu-id="bafd2-121">對磁片區中的檔案或目錄進行任何變更時，該磁片區的 USN 變更日誌會以變更的描述和檔案或目錄的名稱進行更新。</span><span class="sxs-lookup"><span data-stu-id="bafd2-121">When any change is made to a file or directory in a volume, the USN change journal for that volume is updated with a description of the change and the name of the file or directory.</span></span><br/>                                                                                        |
| [<span data-ttu-id="bafd2-122">裝載的資料夾</span><span class="sxs-lookup"><span data-stu-id="bafd2-122">Mounted Folders</span></span>](volume-mount-points.md)<br/>                       | <span data-ttu-id="bafd2-123">您可以使用掛接的資料夾，將不同的檔案系統（例如 NTFS 檔案系統、16位 FAT 檔案系統，以及在 CD-ROM 光碟機上的 ISO-9660 檔案系統）統一成單一 NTFS 磁片區上的一個邏輯檔案系統。</span><span class="sxs-lookup"><span data-stu-id="bafd2-123">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span><br/>                                                      |
| [<span data-ttu-id="bafd2-124">主檔案資料表</span><span class="sxs-lookup"><span data-stu-id="bafd2-124">Master File Table</span></span>](master-file-table.md)<br/>                       | <span data-ttu-id="bafd2-125">檔案的所有相關資訊，包括其大小、時間和日期戳記、許可權和資料內容，都會儲存在主要檔案資料表中 (MFT) 專案，或儲存在 mft 專案所描述之 MFT 以外的空間中。</span><span class="sxs-lookup"><span data-stu-id="bafd2-125">All information about a file, including its size, time and date stamps, permissions, and data content, is stored either in master file table (MFT) entries, or in space outside the MFT that is described by MFT entries.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="bafd2-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="bafd2-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bafd2-127">[基本磁碟和磁片區技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="bafd2-127">[Basic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="bafd2-128">[動態磁碟與磁片區技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="bafd2-128">[Dynamic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="bafd2-129">磁片區管理參考</span><span class="sxs-lookup"><span data-stu-id="bafd2-129">Volume Management Reference</span></span>](volume-management-reference.md)
</dt> </dl>

 

