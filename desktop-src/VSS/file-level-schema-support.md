---
description: 寫入器可以藉由指定檔案規格備份類型（以位元遮罩表示），或使用 VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型列舉的成員位或成員，來微調檔案集層級的各種備份效能。
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: 檔案層級架構支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945231"
---
# <a name="file-level-schema-support"></a><span data-ttu-id="50045-103">檔案層級架構支援</span><span class="sxs-lookup"><span data-stu-id="50045-103">File Level Schema Support</span></span>

<span data-ttu-id="50045-104">寫入器可以藉由指定檔案規格備份類型（以位元遮罩表示），或使用 [**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)列舉的成員位或成員，來微調檔案 [*集*](vssgloss-f.md)層級的各種備份效能。</span><span class="sxs-lookup"><span data-stu-id="50045-104">Writers can fine-tune the performance of various types of backup at the [*file set*](vssgloss-f.md) level by indicating through a file specification backup type, indicated by a bit mask or bitwise OR of the members of the [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) enumeration.</span></span>

<span data-ttu-id="50045-105">針對指定的備份類型，寫入器會指出下列各項：</span><span class="sxs-lookup"><span data-stu-id="50045-105">For specified types of backup, the writer indicates the following:</span></span>

-   <span data-ttu-id="50045-106">是否需要將磁片區陰影複製，以正確地備份檔案集。</span><span class="sxs-lookup"><span data-stu-id="50045-106">Whether it will be necessary to shadow copy the volume to properly back up a file set.</span></span> <span data-ttu-id="50045-107">比方說，如果檔案集中的檔案不是由寫入器獨佔開啟，而且可以確保它是穩定的，就不需要陰影複製。</span><span class="sxs-lookup"><span data-stu-id="50045-107">For instance, if the files in a file set are not exclusively opened by the writer and it can ensure that it is stable, a shadow copy is not needed.</span></span>
-   <span data-ttu-id="50045-108">無論要求者是否需要以這樣的方式來執行備份，不論上次修改時間或其他問題為何，都會還原備份的檔案集檔案的版本。</span><span class="sxs-lookup"><span data-stu-id="50045-108">Whether the requester has to perform the backup in such a way that, regardless of last modification time or other issues, the version of the file set's files current at backup will be restored.</span></span> <span data-ttu-id="50045-109">一般而言，這表示會在備份過程中複製檔案集。</span><span class="sxs-lookup"><span data-stu-id="50045-109">Typically, this means that the file set is copied as part of the backup.</span></span>

<span data-ttu-id="50045-110">表示陰影複製需求的 [**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) 值為：</span><span class="sxs-lookup"><span data-stu-id="50045-110">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate shadow copy requirement are:</span></span>

-   <span data-ttu-id="50045-111">VSS \_ FSBT \_ 需要所有的 \_ 快照 \_ 集</span><span class="sxs-lookup"><span data-stu-id="50045-111">VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="50045-112">VSS \_ FSBT \_ \_ 需要完整快照 \_ 集</span><span class="sxs-lookup"><span data-stu-id="50045-112">VSS\_FSBT\_FULL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="50045-113">\_需要 VSS FSBT \_ 差異 \_ 快照 \_ 集</span><span class="sxs-lookup"><span data-stu-id="50045-113">VSS\_FSBT\_DIFFERENTIAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="50045-114">\_需要 VSS FSBT \_ 增量 \_ 快照 \_ 集</span><span class="sxs-lookup"><span data-stu-id="50045-114">VSS\_FSBT\_INCREMENTAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="50045-115">\_需要 VSS FSBT \_ 記錄 \_ 快照 \_ 集</span><span class="sxs-lookup"><span data-stu-id="50045-115">VSS\_FSBT\_LOG\_SNAPSHOT\_REQUIRED</span></span>

<span data-ttu-id="50045-116">[**VSS \_ 檔 \_ 規格 \_ 備份 \_ 類型**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)的值，表示備份檔案的需求如下：</span><span class="sxs-lookup"><span data-stu-id="50045-116">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate the requirement to back up a file are:</span></span>

-   <span data-ttu-id="50045-117">VSS \_ FSBT \_ \_ 需要所有備份 \_</span><span class="sxs-lookup"><span data-stu-id="50045-117">VSS\_FSBT\_ALL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="50045-118">VSS \_ FSBT \_ \_ 需要完整備份 \_</span><span class="sxs-lookup"><span data-stu-id="50045-118">VSS\_FSBT\_FULL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="50045-119">\_需要 VSS FSBT \_ 差異 \_ 備份 \_</span><span class="sxs-lookup"><span data-stu-id="50045-119">VSS\_FSBT\_DIFFERENTIAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="50045-120">\_需要 VSS FSBT \_ 增量 \_ 備份 \_</span><span class="sxs-lookup"><span data-stu-id="50045-120">VSS\_FSBT\_INCREMENTAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="50045-121">\_需要 VSS FSBT \_ 記錄 \_ 備份 \_</span><span class="sxs-lookup"><span data-stu-id="50045-121">VSS\_FSBT\_LOG\_BACKUP\_REQUIRED</span></span>

<span data-ttu-id="50045-122">根據預設，檔案集會標記為 VSS \_ FSBT \_ 所有 \_ 需要備份的 \_ \| vss \_ FSBT \_ 所有 \_ 需要的快照集 \_ ，這表示在處理檔案集的檔案時一律需要陰影複製，而且應該將檔案複製到所有類型的備份中。</span><span class="sxs-lookup"><span data-stu-id="50045-122">By default, file sets are tagged with a file specification backup type of VSS\_FSBT\_ALL\_BACKUP\_REQUIRED \| VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED, meaning that a shadow copy is always required in handling the file set's files, and that the files should be copied in all types of backup.</span></span>

 

 



