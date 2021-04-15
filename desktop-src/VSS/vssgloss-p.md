---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: 'P (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f018a19c1d00ff3c6530e7c45fbca2350df8fec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511513"
---
# <a name="p-volume-shadow-copy-service"></a><span data-ttu-id="05a7c-103">P (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="05a7c-103">P (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="05a7c-104">[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="05a7c-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="05a7c-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**部分檔案支援**</span><span class="sxs-lookup"><span data-stu-id="05a7c-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**partial file support**</span></span>
</dt> <dd>

<span data-ttu-id="05a7c-106">藉由修改相關檔案的各小節來執行備份作業的容量，而不是使用整個檔案。</span><span class="sxs-lookup"><span data-stu-id="05a7c-106">The capacity to implement backup operations by modifying subsections of the files involved, rather than working with the entire files.</span></span> <span data-ttu-id="05a7c-107">另請參閱 [*導向目標*](vssgloss-d.md)。</span><span class="sxs-lookup"><span data-stu-id="05a7c-107">See also [*directed targeting*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="05a7c-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**持續陰影複製**</span><span class="sxs-lookup"><span data-stu-id="05a7c-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**persistent shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="05a7c-109">當要求者釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 物件或電腦重新開機時，不會自動刪除的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="05a7c-109">A shadow copy that is not deleted automatically when the requester releases an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object or when the computer is restarted.</span></span> <span data-ttu-id="05a7c-110">另請參閱 [*自動發行陰影複製*](vssgloss-a.md)、 [*陰影複製*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="05a7c-110">See also [*auto-release shadow copy*](vssgloss-a.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="05a7c-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**叢**</span><span class="sxs-lookup"><span data-stu-id="05a7c-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**</span></span>
</dt> <dd>

<span data-ttu-id="05a7c-112">一種特殊類型的陰影複製磁片區，完整且完全代表陰影複製磁片區，而不需要任何原始磁片區。</span><span class="sxs-lookup"><span data-stu-id="05a7c-112">A special type of shadow copy volume that fully and completely represents a shadow copy volume without the need for either original volume.</span></span> <span data-ttu-id="05a7c-113">這通常也稱為分割鏡像，但本檔使用的是 Plex。</span><span class="sxs-lookup"><span data-stu-id="05a7c-113">This is also commonly known as a split-mirror, but this documentation uses the term Plex.</span></span>

</dd> <dt>

<span data-ttu-id="05a7c-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**PostRestore 事件**</span><span class="sxs-lookup"><span data-stu-id="05a7c-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**PostRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="05a7c-115">表示 VSS 還原已完成的 VSS 事件。</span><span class="sxs-lookup"><span data-stu-id="05a7c-115">A VSS event indicating that a VSS restore has completed.</span></span>

</dd> <dt>

<span data-ttu-id="05a7c-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot 事件**</span><span class="sxs-lookup"><span data-stu-id="05a7c-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="05a7c-117">表示陰影複製已完成的 VSS 事件。</span><span class="sxs-lookup"><span data-stu-id="05a7c-117">A VSS event indicating that a shadow copy has been completed.</span></span> <span data-ttu-id="05a7c-118">另請參閱 [*陰影複製*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="05a7c-118">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="05a7c-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup 事件**</span><span class="sxs-lookup"><span data-stu-id="05a7c-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup event**</span></span>
</dt> <dd>

<span data-ttu-id="05a7c-120">指出即將進行備份作業的 VSS 事件。</span><span class="sxs-lookup"><span data-stu-id="05a7c-120">A VSS event indicating that a backup operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="05a7c-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**PrepareForSnapshot 事件**</span><span class="sxs-lookup"><span data-stu-id="05a7c-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**PrepareForSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="05a7c-122">VSS 事件，指出寫入器應該採取步驟來準備即將進行的陰影複製操作。</span><span class="sxs-lookup"><span data-stu-id="05a7c-122">A VSS event indicating that writers should take steps to prepare for an upcoming shadow copy operation.</span></span> <span data-ttu-id="05a7c-123">另請參閱 [*陰影複製*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="05a7c-123">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="05a7c-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore 事件**</span><span class="sxs-lookup"><span data-stu-id="05a7c-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="05a7c-125">VSS 事件，指出即將進行還原作業。</span><span class="sxs-lookup"><span data-stu-id="05a7c-125">A VSS event indicating that a restore operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="05a7c-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**供應商**</span><span class="sxs-lookup"><span data-stu-id="05a7c-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="05a7c-127">一種作業系統物件，它會攔截並管理 i/o 要求，以建立並代表檔案系統的磁片區陰影複製。</span><span class="sxs-lookup"><span data-stu-id="05a7c-127">An operating system object that intercepts and manages I/O requests to create and represent volume shadow copies to the file system.</span></span> <span data-ttu-id="05a7c-128">另請參閱 [*硬體提供者*](vssgloss-h.md)、 [*軟體提供者*](vssgloss-s.md)。</span><span class="sxs-lookup"><span data-stu-id="05a7c-128">See also [*hardware provider*](vssgloss-h.md), [*software provider*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



