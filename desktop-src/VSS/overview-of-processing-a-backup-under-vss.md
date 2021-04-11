---
description: 在處理備份時，「要求者」和「寫入器」會協調以提供穩定的系統映射， (陰影複製的磁片區) 來備份資料、將檔案群組在一起，以及將資訊儲存在儲存的資料上。
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: 在 VSS 下處理備份的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318984"
---
# <a name="overview-of-processing-a-backup-under-vss"></a><span data-ttu-id="01907-103">在 VSS 下處理備份的總覽</span><span class="sxs-lookup"><span data-stu-id="01907-103">Overview of Processing a Backup Under VSS</span></span>

<span data-ttu-id="01907-104">在處理備份時，「要求者」和「寫入器」會協調以提供穩定的系統映射， (陰影複製的磁片區) 來備份資料、將檔案群組在一起，以及將資訊儲存在儲存的資料上。</span><span class="sxs-lookup"><span data-stu-id="01907-104">In processing a backup, requester and writers coordinate to provide a stable system image from which to back up data (the shadow copied volume), to group files together on the basis of their usage, and to store information on the saved data.</span></span> <span data-ttu-id="01907-105">這必須在只為寫入器的一般工作流程產生最少量的中斷時完成。</span><span class="sxs-lookup"><span data-stu-id="01907-105">This must all be done while creating only minimal interruption to the writer's normal work flow.</span></span>

<span data-ttu-id="01907-106">要求者會查詢其中繼資料的寫入器、處理此資料、在陰影複製和備份作業開始前通知寫入器，然後在陰影複製和備份作業結束之後再次通知寫入器。</span><span class="sxs-lookup"><span data-stu-id="01907-106">A requester queries writers for their metadata, processes this data, notifies the writers prior to the beginning of the shadow copy and of the backup operations, and then notifies the writers again after the shadow copy and backup operations end.</span></span>

<span data-ttu-id="01907-107">為了回應這些通知，寫入器會提供要備份之檔案的相關資訊，包括指定要協調 ([*元件*](vssgloss-c.md) 的檔案群組) -在陰影複製之前，在其 i/o 作業中暫停，然後在陰影複製完成或備份結束後回到正常操作。</span><span class="sxs-lookup"><span data-stu-id="01907-107">In response to these notifications, the writer provides information about files to be backed up—including specifying groups of files to coordinate ([*components*](vssgloss-c.md))—pauses in its I/O operations prior to a shadow copy, and then returns to normal operation following the completion of a shadow copy or at the end of the backup.</span></span>

<span data-ttu-id="01907-108">在處理備份的過程中，寫入器會透過其唯讀中繼資料來指定其負責的檔案（寫入器元資料檔案 (參閱 [VSS 中繼資料：使用寫入器元資料檔案](working-with-the-writer-metadata-document.md)) 。</span><span class="sxs-lookup"><span data-stu-id="01907-108">In the course of processing the backup, a writer specifies the files it is responsible for through its read-only metadata—the Writer Metadata Document (see [VSS Metadata: Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md)).</span></span> <span data-ttu-id="01907-109">然後，要求者會解讀此中繼資料、選擇要備份的內容，並將這些決策儲存在自己的中繼資料物件中、備份元件檔 (參閱 [VSS 中繼資料：使用備份元件檔](working-with-the-backup-components-document.md)) 。</span><span class="sxs-lookup"><span data-stu-id="01907-109">The requester then interprets this metadata, chooses what to back up, and stores these decisions in its own metadata object, the Backup Components Document (see [VSS Metadata: Working with the Backup Components Document](working-with-the-backup-components-document.md)).</span></span> <span data-ttu-id="01907-110">這份備份元件檔適用于備份和還原作業期間的寫入器檢查和修改。</span><span class="sxs-lookup"><span data-stu-id="01907-110">This Backup Components Document is available for writer inspection and modification during both the backup and restore operations.</span></span>

<span data-ttu-id="01907-111">下圖顯示要求者、VSS 服務、VSS 核心支援、相關的任何 VSS 寫入器，以及任何 VSS 硬體提供者之間的互動。</span><span class="sxs-lookup"><span data-stu-id="01907-111">This diagram shows the interactions between the requester, the VSS service, the VSS kernel support, any VSS writers involved, and any VSS hardware providers.</span></span>

![要求者、備份元件、寫入器與提供者之間的互動](images/vssimpl.png)

<span data-ttu-id="01907-113">若要更充分瞭解執行備份所牽涉到的基本工作，將此總覽細分為下列主題會很有用：</span><span class="sxs-lookup"><span data-stu-id="01907-113">To more fully understand the basic tasks involved in performing a backup, it is useful to break down this overview into the following topics:</span></span>

-   [<span data-ttu-id="01907-114">備份初始化的總覽</span><span class="sxs-lookup"><span data-stu-id="01907-114">Overview of Backup Initialization</span></span>](overview-of-backup-initialization.md)
-   [<span data-ttu-id="01907-115">備份探索階段總覽</span><span class="sxs-lookup"><span data-stu-id="01907-115">Overview of the Backup Discovery Phase</span></span>](overview-of-the-backup-discovery-phase.md)
-   [<span data-ttu-id="01907-116">備份前工作總覽</span><span class="sxs-lookup"><span data-stu-id="01907-116">Overview of Pre-Backup Tasks</span></span>](overview-of-pre-backup-tasks.md)
-   [<span data-ttu-id="01907-117">檔的實際備份總覽</span><span class="sxs-lookup"><span data-stu-id="01907-117">Overview of Actual Backup Of Files</span></span>](overview-of-actual-backup-of-files.md)
-   [<span data-ttu-id="01907-118">備份終止的總覽</span><span class="sxs-lookup"><span data-stu-id="01907-118">Overview of Backup Termination</span></span>](overview-of-backup-termination.md)

 

 



