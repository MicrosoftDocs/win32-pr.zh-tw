---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: 'B (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20cabdfa5260f65d1176f6f1d12ac1d805b9dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318404"
---
# <a name="b-volume-shadow-copy-service"></a><span data-ttu-id="ec78e-103">B (磁碟區陰影複製服務) </span><span class="sxs-lookup"><span data-stu-id="ec78e-103">B (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="ec78e-104">[B](vssgloss-a.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="ec78e-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="ec78e-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**後端層級應用程式**</span><span class="sxs-lookup"><span data-stu-id="ec78e-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**back-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-106">指示寫入器收到 VSS 凍結的通知點。</span><span class="sxs-lookup"><span data-stu-id="ec78e-106">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="ec78e-107">初始化為後端層級應用程式的寫入器會在寫入器初始化為前端層級應用程式之後，以及初始化為系統層級應用程式的之前收到通知。</span><span class="sxs-lookup"><span data-stu-id="ec78e-107">Writers that are initialized as back-end level applications are notified after writers initialized as front-end level applications and prior to those initialized as system-level applications.</span></span> <span data-ttu-id="ec78e-108">另請參閱 [*應用層級*](vssgloss-a.md)、 [*前端層級應用程式*](vssgloss-f.md)、 [*系統層級應用程式*](vssgloss-s.md)、 [*寫入器*](vssgloss-w.md)。</span><span class="sxs-lookup"><span data-stu-id="ec78e-108">See also [*application level*](vssgloss-a.md), [*front-end level applications*](vssgloss-f.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec78e-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete 事件**</span><span class="sxs-lookup"><span data-stu-id="ec78e-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete event**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-110">表示 VSS 備份已完成的 VSS 事件。</span><span class="sxs-lookup"><span data-stu-id="ec78e-110">A VSS event indicating that a VSS backup has completed.</span></span> <span data-ttu-id="ec78e-111">在正常作業下，此事件後面應該接著 BackupShutdown 事件。</span><span class="sxs-lookup"><span data-stu-id="ec78e-111">This event should be followed by a BackupShutdown event under normal operation.</span></span> <span data-ttu-id="ec78e-112">另請參閱 *BackupShutdown 事件*。</span><span class="sxs-lookup"><span data-stu-id="ec78e-112">See also *BackupShutdown event*.</span></span>

</dd> <dt>

<span data-ttu-id="ec78e-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**備份元件檔**</span><span class="sxs-lookup"><span data-stu-id="ec78e-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Backup Components Document**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-114">要求者所建立的 XML 檔 (在設定還原或備份作業的過程中，) 使用 **>ivssbackupcomponents** 介面。</span><span class="sxs-lookup"><span data-stu-id="ec78e-114">An XML document created by a requester (using the **IVssBackupComponents** interface) in the course of setting up a restore or backup operation.</span></span> <span data-ttu-id="ec78e-115">備份元件文件包含從參與備份或還原作業的一或多個寫入器明確加入的元件清單。</span><span class="sxs-lookup"><span data-stu-id="ec78e-115">The Backup Components Document contains a list of those explicitly included components, from one or more writers, participating in a backup or restore operation.</span></span> <span data-ttu-id="ec78e-116">不包含隱含加入的元件資訊。</span><span class="sxs-lookup"><span data-stu-id="ec78e-116">It does not contain implicitly included component information.</span></span> <span data-ttu-id="ec78e-117">相反地，寫入器中繼資料文件只會包含可能參與備份的寫入器元件。</span><span class="sxs-lookup"><span data-stu-id="ec78e-117">In contrast, a Writer Metadata Document contains only writer components that may participate in a backup.</span></span>

<span data-ttu-id="ec78e-118">您可以將備份元件檔儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="ec78e-118">A Backup Components Document can be saved to disk.</span></span> <span data-ttu-id="ec78e-119">另請參閱 [*明確元件包含*](vssgloss-e.md)、 [*隱含元件*](vssgloss-i.md)包含。</span><span class="sxs-lookup"><span data-stu-id="ec78e-119">See also [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec78e-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**備份組**</span><span class="sxs-lookup"><span data-stu-id="ec78e-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**backup set**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-121">要備份的檔案。</span><span class="sxs-lookup"><span data-stu-id="ec78e-121">Those files to be backed up.</span></span> <span data-ttu-id="ec78e-122">它包含元件中所選取的檔案，這些檔案包含在元件中（由寫入器層級的 include 語句所表示），而不是已明確包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="ec78e-122">It includes files selected by inclusion in a component, those indicated by writer-level include statements, less those files that have been explicitly included.</span></span>

</dd> <dt>

<span data-ttu-id="ec78e-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown 事件**</span><span class="sxs-lookup"><span data-stu-id="ec78e-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown event**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-124">VSS 事件，指出符合規範的備份應用程式已關閉。</span><span class="sxs-lookup"><span data-stu-id="ec78e-124">A VSS event indicating that a compliant backup application has shut down.</span></span> <span data-ttu-id="ec78e-125">一般來說，這會在 BackupComplete 事件之前。</span><span class="sxs-lookup"><span data-stu-id="ec78e-125">Normally, this is preceded by a BackupComplete event.</span></span> <span data-ttu-id="ec78e-126">但是，如果備份非預期地終止，則不需要先前的 BackupComplete 事件就可以產生此事件。</span><span class="sxs-lookup"><span data-stu-id="ec78e-126">However, if a backup terminates unexpectedly, this event can be generated without a preceding BackupComplete event.</span></span> <span data-ttu-id="ec78e-127">另請參閱 *BackupComplete 事件*。</span><span class="sxs-lookup"><span data-stu-id="ec78e-127">See also *BackupComplete event*.</span></span>

</dd> <dt>

<span data-ttu-id="ec78e-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**備份戳記**</span><span class="sxs-lookup"><span data-stu-id="ec78e-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**backup stamp**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-129">字串，其中包含發生備份時的資訊。</span><span class="sxs-lookup"><span data-stu-id="ec78e-129">A string containing information as to when a backup took place.</span></span> <span data-ttu-id="ec78e-130">除了智慧型至指定類別的所有寫入器實例之外，VSS 對此字串的格式沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="ec78e-130">VSS places no restriction on the format of this string, except that it be intelligible to all the writer instances of a given class.</span></span> <span data-ttu-id="ec78e-131">它可能包含時間和日期資訊、邏輯序號或任何其他資訊，這些資訊將允許相同類別的寫入器判斷上次備份的發生時間。</span><span class="sxs-lookup"><span data-stu-id="ec78e-131">It may contain time and date information, logical sequence numbers, or any other information that will allow a writer of the same class to determine when the last backup has take place.</span></span>

</dd> </dl>

 

 



